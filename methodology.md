# Methodology

How attributions in this repository are established, what each confidence tier means, and how the per-wallet flow profiles and counterparty CSVs are produced.

## Contents

1. [Confidence tiers](#confidence-tiers)
2. [Evidence types](#evidence-types)
3. [Verification](#verification)
4. [Receipts and reproducibility](#receipts-and-reproducibility)
5. [Natural persons](#natural-persons)
6. [Flow profiles](#flow-profiles)
7. [Inventory profile CSV](#inventory-profile-csv)

## Confidence tiers

**CONFIRMED.** Two or more independent primary sources point to the attribution. Examples: a public name tag on a major block explorer plus a deterministic on-chain link to another already-confirmed address; a self-attestation plus an auditor reference; two public-label sets that do not derive from each other.

**PARTIAL.** A single primary source. Recorded but should not be cited without that caveat.

**HEURISTIC.** No primary source. Derived from on-chain pattern, clustering, or behavioural fingerprint. Useful as a working hypothesis only.

## Evidence types

**Self-attestation.** The entity itself pointed at the address — a tweet, video, signed message, or page on its own domain.

**Public name tag.** A label maintained by a major block explorer (Etherscan, PolygonScan, OP Etherscan, BscScan, BaseScan, Solscan, Tronscan), or an aggregated label set such as the hildobby Dune query.

**Smart-contract relation.** The address is the deployer of, deployed by, or owner of an already-attributed contract.

**Transaction relation.** The address received from or sent to an already-attributed address in a specific transaction whose hash is quoted.

**Cluster heuristic.** Bitcoin co-spend or change-output adjacency, or EVM common-deployer-EOA clustering. By itself, HEURISTIC; combined with another evidence type, can support CONFIRMED.

**Behavioural fingerprint.** Holdings shape, transaction-volume pattern, or other indirect evidence. Weakest tier.

## Verification

Every factual claim in this repository carries a citation. Block-explorer URLs are considered durable; for other external sources we prefer mirroring to an `archive.today` or `web.archive.org` snapshot so the citation keeps resolving after the live URL dies.

## Receipts and reproducibility

A "receipt" is the saved response from a primary source at the moment it was queried — the JSON returned by an API, the HTML rendered by a block-explorer page at a given URL, the snapshot of a third-party dataset row. Receipts let a reader re-verify a claim even if the live source later changes or disappears.

This repository handles receipts in two tiers:

1. **Mirrored receipts** are committed under [`sources/`](sources/) and cited by wallet pages via relative path. These are the small-and-singular artefacts that establish a specific attribution: BlockSec MetaSleuth label JSON responses, Dune-query execution JSONs, the WalletExplorer cluster HTML for the BitBay.net cluster. Citing them from this repo makes the underlying byte string immediately re-checkable.
2. **Working-archive receipts** are bulk HTML fetches retained outside the public repo because of size — most notably the Etherscan and PolygonScan public-name-tag HTML pages (tens of thousands of files per closure pass). The public-verifiable artefact in these cases is the **upstream block-explorer URL itself**, cited inline with the retrieval date. The saved HTML proves the tag was visible at that date; the URL proves it is (still) visible now. A reader who wants the saved HTML for a specific address can request it; the canonical primary source remains the block-explorer page.

A citation that uses a `sources/<path>` reference resolves inside this repository. A citation that uses an upstream URL + retrieval date resolves against the live source. Citations to `case/sources/...` are an internal-archive artefact and should not appear in this repository's published pages; if you see one, treat it as a bug.

## Natural persons

Natural persons are referenced by role where possible. Where naming is unavoidable because the person's name is part of the primary record itself (for example a tweet posted from their own handle), the URL is given as-is and no further commentary is added.

## Flow profiles

A per-wallet "Flow profile" section, where present, reports full-history aggregated transfer activity for that address using the standardised data sources and SQL below. The profile is independent of any external narrative; it can be reproduced from the wallet address alone.

### Data sources

- **Ethereum, Polygon, and other EVM chains** — Dune Analytics tables `tokens_<chain>.transfers`, which expose every ERC-20 transfer and native-token transfer with a USD-equivalent value at the time of the transaction. Full-history, multichain, threshold-filterable in one query.
- **Bitcoin** — mempool.space's public REST API: `GET https://mempool.space/api/address/<addr>` for the summary (funded UTXOs, spent UTXOs, tx count) and `GET https://mempool.space/api/address/<addr>/txs/chain[/<last_txid>]` for paginated full transaction history.

### Reproducibility — Dune SQL template

```sql
-- INPUTS: <target_addr> (bare 0x literal, no quotes), <threshold_usd> (e.g. 1000)
WITH flows AS (
  SELECT
    CASE WHEN "from" = <target_addr> THEN 'OUT' ELSE 'IN' END AS direction,
    CASE WHEN "from" = <target_addr> THEN "to" ELSE "from" END AS counterparty,
    symbol, amount, amount_usd, block_time
  FROM tokens_ethereum.transfers       -- swap for tokens_polygon.transfers / etc.
  WHERE ("from" = <target_addr> OR "to" = <target_addr>)
    AND amount_usd >= <threshold_usd>
)
SELECT direction,
       CAST(counterparty AS varchar) AS counterparty,
       symbol,
       COUNT(*)                     AS n_events,
       ROUND(SUM(amount), 4)        AS total_amount,
       ROUND(SUM(amount_usd), 2)    AS total_usd,
       MIN(block_time)              AS first_seen,
       MAX(block_time)              AS last_seen
FROM flows
GROUP BY direction, counterparty, symbol
ORDER BY total_usd DESC NULLS LAST;
```

For a multi-wallet aggregation (used in the cross-wallet CEX off-ramp summary and per-wallet headline-metric tables) replace the `"from" = <target_addr>` predicate with a `JOIN` against an `addrs(zonda_wallet)` `VALUES` clause, and add a per-wallet `ROW_NUMBER()` partition to cap rows per wallet.

### Counterparty classification

Each counterparty surfaced by the aggregation is classified into one of three buckets:

- **Internal** — appears in this inventory's roster (the per-chain wallet pages indexed from `scouting/wallets/README.md`).
- **External — confirmed via public name tag** — the major block explorer for that chain carries a Public Name Tag on the address, verified by a fresh HTML fetch retained in the working archive (see [Receipts and reproducibility](#receipts-and-reproducibility) for the policy on bulk HTML name-tag receipts). The tag string must be visible in the saved HTML when re-grepped — no tag claim is published without a re-greppable receipt.
- **Unidentified** — neither internal nor carrying a public name tag.

Sections naming Unidentified counterparties carry an explicit "incomplete / ongoing" flag. They represent the open part of the analysis and are not to be read as completed work.

### Confidence tiers for flow claims

Within the Flow-profile sections specifically, three claim-tiers apply on top of the repository-wide CONFIRMED / PARTIAL / HEURISTIC scheme:

- **CONFIRMED on totals.** Gross IN, Gross OUT, throughput, event count, active period, and distinct-counterparty count are direct sums over the Dune `tokens_<chain>.transfers` table, reproducible from the wallet address alone. The Dune execution receipt is cited.
- **CONFIRMED on per-counterparty classification, Internal + External-tagged rows only.** Each Internal row is a roster match; each External-tagged row is backed by a fresh public-name-tag HTML receipt.
- **PARTIAL on Unidentified counterparties.** Counterparty identity is the open part of the analysis. Entity-attribution work continues in the case's internal working notes and individual addresses are migrated to the External-tagged bucket as each clears the same primary-citation standard used elsewhere in this inventory.

### Wallet-level confidence interaction

Where the wallet's own attribution is at PARTIAL tier (the BitBay-era wallets in this inventory), the Flow profile section is annotated **PARTIAL — wallet attribution itself is at PARTIAL tier**: the flow numbers themselves remain CONFIRMED (they are direct on-chain reads), but their attribution to ZondaCrypto operations inherits the wallet's PARTIAL tier.

### Threshold

Unless otherwise stated, the Flow profile uses **$1,000 USD-equivalent per event** as the minimum-significance threshold. Below this threshold the activity is treated as dust / noise / address-poisoning seeds and excluded. Distinct-counterparty counts also use a **$1,000 cumulative** secondary threshold.

## Inventory profile CSV

In addition to the Flow profile section (a curated, threshold-filtered narrative view), each wallet page links to a full **counterparty enumeration CSV** (`<slug>-counterparties.csv` or `<slug>-counterparties-polygon.csv`). The CSV is the raw on-chain inventory: every distinct counterparty that ever sent value to, or received value from, the target address, with no USD threshold, no truncation, and no top-N cap.

### Column schema (EVM chains)

| Column | Definition |
|---|---|
| `counterparty_address` | The non-target side of the transfer, normalised to lowercase hex with `0x` prefix. |
| `n_events_in` | Count of distinct ERC-20 / native transfer events delivering value to the target. |
| `n_events_out` | Count of distinct transfer events sending value from the target. |
| `gross_usd_in` | Sum of `amount_usd` over `n_events_in`. NULL prices are coalesced to 0, so unpriced-token rows do not inflate the figure but their counterparty still appears in the file. |
| `gross_usd_out` | Sum of `amount_usd` over `n_events_out`, with the same NULL-coalescing rule. |
| `net_usd` | `gross_usd_in − gross_usd_out`. |
| `symbols` | Comma-separated set of ERC-20 / native token symbols touched between this counterparty and the target. |
| `native_amounts` | For ZND/TMPL ecosystem pages: per-symbol total native-token amount in the form `SYM:amount;SYM:amount`. Blank where the USD column already captures the magnitude. |
| `first_seen` / `last_seen` | ISO 8601 dates (YYYY-MM-DD), earliest and latest transfer block-time observed between the counterparty and the target. |
| `label_source` | One of `internal`, `hildobby`, `etherscan`, `no-public-tag`, `below-cutoff`, `deferred-above-cutoff`. |
| `label_value` | Human-readable tag where applicable; empty for `no-public-tag`, `below-cutoff`, and `deferred-above-cutoff`. |

### Label-source precedence

When more than one source could classify a counterparty, the wallet pages and CSVs apply the following precedence (highest wins):

1. **`internal`** — the counterparty appears in this inventory's own roster of labelled Zonda / BitBay wallets.
2. **`hildobby`** — the counterparty is listed in hildobby's Dune query 3237025 ("All Known EVM CEX Addresses"). The `label_value` is the `distinct_name` column (e.g. `Binance 14`, `Kraken 4`, `Gate.io 1`).
3. **`etherscan`** — the counterparty page on the relevant block explorer (`etherscan.io`, `polygonscan.com`) carries a Public Name Tag, verified by a fresh HTML fetch with browser-style User-Agent at the cited date and grep-checked for the literal string `Public Name Tag` in the saved HTML.
4. **`no-public-tag`** — a fresh HTML fetch of the counterparty's block-explorer page was completed and the saved HTML contains no `Public Name Tag` string. This is distinct from `below-cutoff` (intentionally not fetched per policy) and from `deferred-above-cutoff` (fetch outstanding): the explorer was checked and returned no tag at the cited date.
5. **`below-cutoff`** — the counterparty's cumulative gross USD flow across the entire inventory is below the $10,000 cutoff for fetching Etherscan name tags; no fetch is attempted, and no name-tag claim is made. Published as part of the full enumeration.
6. **`deferred-above-cutoff`** — the counterparty's cumulative gross USD flow is at or above the $10,000 cutoff, but no Etherscan name-tag fetch has been completed in the most recent pass (e.g., the ≥$10k set was too large to fetch exhaustively in a single pass). This is a known, machine-discoverable gap. No name-tag claim is made until a fresh fetch is run on this subset. This bucket is expected to be empty when an inventory profile has been fully closed; if non-empty, the residual count is reported in the inventory's manifest.

### Etherscan-fetch cutoff

Public-name-tag fetches at the `etherscan` source tier are run against the union of counterparties with **cumulative gross USD flow ≥ $10,000 across the entire inventory** (a counterparty appearing at $3k against Zonda 1 and $8k against Zonda 5 has $11k cumulative and clears the cutoff). Counterparties below the cutoff are labelled `below-cutoff` and not fetched. Counterparties at or above the cutoff that have not yet had a fetch completed are labelled `deferred-above-cutoff` so the deferred set is machine-discoverable for a follow-up fetch pass. This makes both the cutoff and the deferred-but-not-yet-completed set explicit; readers can run the fetch themselves at a lower cutoff or against the deferred-above-cutoff subset for broader / completed coverage.

Within the ≥$10k set, fetches are dedup'd against existing HTML receipts retained in the working archive (one batch per fetch date). Fetches are prioritised by descending cumulative gross flow; the per-pass cutoff at which the fetch was stopped is tracked in the working archive's per-pass index.

### Reproducibility — Dune SQL template (no-truncation)

```sql
-- INPUTS: addrs (bare 0x literals; one row per target wallet)
WITH addrs(zonda_wallet, wallet_name) AS (VALUES (0x..., 'Wallet 1'), (0x..., 'Wallet 2')),
flows AS (
  SELECT a.zonda_wallet, a.wallet_name,
    CASE WHEN t."from" = a.zonda_wallet THEN 'OUT' ELSE 'IN' END AS direction,
    CASE WHEN t."from" = a.zonda_wallet THEN t."to" ELSE t."from" END AS counterparty,
    t.symbol, t.amount, COALESCE(t.amount_usd, 0) AS amount_usd, t.block_time
  FROM tokens_ethereum.transfers t       -- or tokens_polygon.transfers, etc.
  JOIN addrs a ON (t."from" = a.zonda_wallet OR t."to" = a.zonda_wallet)
)
-- aggregate to (zonda_wallet, counterparty) granularity, collapsing direction into per-direction columns
SELECT zonda_wallet, CAST(counterparty AS varchar) AS counterparty,
  SUM(CASE WHEN direction='IN' THEN 1 ELSE 0 END) AS n_events_in,
  SUM(CASE WHEN direction='OUT' THEN 1 ELSE 0 END) AS n_events_out,
  ROUND(SUM(CASE WHEN direction='IN' THEN amount_usd ELSE 0 END), 2) AS gross_usd_in,
  ROUND(SUM(CASE WHEN direction='OUT' THEN amount_usd ELSE 0 END), 2) AS gross_usd_out,
  MIN(block_time) AS first_seen, MAX(block_time) AS last_seen,
  array_join(array_agg(DISTINCT symbol), ',') AS symbols
FROM flows
GROUP BY zonda_wallet, counterparty
```

The hildobby join is `LEFT JOIN query_3237025 h ON CAST(h.address AS varchar) = c.counterparty` and surfaces the `cex_name` + `distinct_name` columns directly in the result set; the CEX classification is therefore a Dune-side bulk join rather than a downstream lookup.

### Bitcoin cluster scope

For Bitcoin clusters that exceed a practical per-address enumeration size (BitBay.net cluster's 26,014 addresses being the case in this inventory), the wallet page records a **cluster-level summary** rather than a per-address CSV: cluster size, transaction count, active period, and named-cluster counterparties as recorded by WalletExplorer. Full per-address enumeration is the upstream WalletExplorer page's responsibility; the inventory does not duplicate that content.

