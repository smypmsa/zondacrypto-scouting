# Methodology

How attributions in this repository are established and what each confidence tier means.

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

## Natural persons

Natural persons are referenced by role where possible. Where naming is unavoidable because the person's name is part of the primary record itself (for example a tweet posted from their own handle), the URL is given as-is and no further commentary is added.

# Methodology — append to scouting/methodology.md

The following section is intended to be appended verbatim (after the existing "Natural persons" section, or merged into a new "Flow profiles" top-level section).

---

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
- **External — confirmed via public name tag** — the major block explorer for that chain carries a Public Name Tag on the address, verified by a fresh HTML fetch saved alongside the analysis as a receipt (`case/sources/etherscan-name-tags-<date>/<addr>.html` / `case/sources/polygonscan-name-tags-<date>/<addr>.html`). The tag string must be visible in the saved HTML when re-grepped — no tag claim is published without a re-greppable receipt.
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

