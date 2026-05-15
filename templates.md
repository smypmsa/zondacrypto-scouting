# File templates

Canonical structure for the file types in this repository. Pages that diverge from these templates should be ported back to them. The goal is uniform layout so a reader who has read one page can navigate any other page without re-orienting.

## Wallet file — `wallets/<chain>/<slug>.md`

Sections appear in this order. Every section name is fixed; do not paraphrase. Sections may be empty (declare "none" or "not applicable" — never silently omit). Use H2 (`##`) for top-level sections, H3 (`###`) for sub-tables inside a flow profile.

```markdown
# <Display name> (`0xshort…last4`)

> **Plain-language summary.** One paragraph. What this address is, who
> controls it per the cited primary source, when it has been active, and the
> single most important math finding about it. No interpretation beyond what
> the totals literally say. Aim for ~50–80 words.

**Address** · `0xfull…`
**Chain** · <Ethereum / Polygon / Bitcoin / …>
**Role per primary source** · <one line>
**Confidence** · <CONFIRMED / PARTIAL / HEURISTIC> — <one-line basis>

> *CONFIRMED = two independent primary sources. PARTIAL = single primary
> source. HEURISTIC = on-chain pattern only, working hypothesis.* See
> [glossary](../../glossary.md).

## Attribution

<2–4 sentences. Each factual claim carries an inline link to its primary
source. Footnotes carry the retrieval date and the receipt path or upstream
URL.>

## Activity (probed YYYY-MM-DD)

<Table: first event date, last event date, native event count, ERC-20 event
count. One sentence translating any shorthand (e.g. "≥10k native" means
"more than 10,000 native-token transactions, hitting the indexer API page
cap; the true count is at least that").>

## Flow profile (Dune-aggregated YYYY-MM-DD)

<Two-column metrics table — Gross IN, Gross OUT, throughput, net,
distinct counterparties, active period, identified-vs-unattributed
counts. ≤8 rows.>

**Confidence:** <one sentence on what is CONFIRMED at this section vs PARTIAL.>

### Counterparties also in this inventory

<Table of internal flows. ≤10 rows inline; if more, collapse the rest into
a `<details>` block.>

### External counterparties — confirmed via public name tag

<Etherscan / PolygonScan / hildobby-tagged rows. Top 10 by USD inline;
remainder collapsed.>

### Unattributed counterparties

<One paragraph stating the count, the aggregate inbound USD, the aggregate
outbound USD, and the explicit "this is a known incomplete part of the
analysis" flag. Then either an in-line top-50 table or a pointer to the
CSV. Use the heading "Unattributed" — not "Unidentified".>

## Scope and negative space

<Mandatory section. What this file does NOT cover. Examples: time-period
gaps, related clusters documented elsewhere, attribution work outside the
public primary-citation gate. Bellingcat practice: declare the frame.>

## Reproducibility

- Dune query: <id>, execution <id>
- Receipts: <relative paths into `sources/` for mirrored receipts;
  "working archive" pointer for bulk HTML batches>
- Block-explorer link: <upstream URL>

## Citations

[^1]: <retrieval date, URL, receipt path>
[^2]: …
```

### Standardised heading vocabulary

These names are fixed. Pick the right one and use it verbatim:

- `## Attribution` (not "Source", "Identification", or "Primary citations")
- `## Activity` (not "On-chain activity", "History")
- `## Flow profile` (not "Flow analysis", "Transfers")
- `### Counterparties also in this inventory` (not "Internal flows", "Internal counterparties")
- `### External counterparties — confirmed via public name tag` (not "External counterparties — confirmed via Etherscan public name tags", "Tagged externals")
- `### Unattributed counterparties` (not "Unidentified", "Unknown", "Open")
- `## Scope and negative space` (not "Scope", "Limitations", "Out of scope")
- `## Reproducibility` (not "Methodology", "How to reproduce", "Sources")
- `## Citations` (not "Footnotes", "References", "Sources")

### Counterparty-table size policy

Inline counterparty tables are capped at **10 rows by descending USD** (or by descending event count for native-only token pages where USD is unpriced). The remainder is collapsed:

```markdown
<details>
<summary>Show full table (N rows)</summary>

| Counterparty | … |
| --- | --- |
| ... | ... |

</details>
```

The full enumeration always lives in the companion CSV (`<slug>-counterparties.csv`). The CSV is authoritative for any per-counterparty number.

### Citation style

Use inline links for the primary-source claim itself, footnotes for the receipt path and retrieval date.

```markdown
Etherscan carries the [public name tag "Zonda 1 (Exchange)"][^1] on this address.

[^1]: Fetched 2026-05-13.
   https://etherscan.io/address/0xf646cbe3b030fb6c2569215f0117dba58badb95e
   Receipt retained in the working archive — see
   [methodology § Receipts](../../methodology.md#receipts-and-reproducibility).
```

## Cluster file — `wallets/<chain>/<cluster-slug>.md`

A cluster file documents a single inventory item that covers many addresses (e.g. a WalletExplorer named cluster or an EVM vanity-suffix family). Same overall shape as the wallet template, with two adjustments:

- Replace `## Activity` with `## Cluster identity` — cluster name (verbatim from the upstream source), cluster size, transaction count, time bounds, and the basis-for-attribution sentence.
- Add `## Representative addresses` immediately after `## Cluster identity` — a small (≤20-row) sample table of addresses with their balance, transaction count, and inferred role. State explicitly that these are *examples*, not *the inventory*.

`wallets/bitcoin/bitbay-net-cluster.md` is the reference implementation.

## Observation file — `observations/<topic>.md`

Cross-wallet math summaries (a single metric computed across multiple inventoried wallets). Shape:

```markdown
# <Topic> (chain, method, date)

> **Plain-language summary.** One paragraph. What this summary measures and
> what number it produces.

**Scope.** <One paragraph. Which wallets are in, which are out, and why.>

**Confidence.** <One paragraph. Which rows are CONFIRMED and which inherit a
PARTIAL tier from their source wallets.>

## <Headline table>
<The main metric, computed per source wallet × per dimension.>

## <Aggregation table>
<Roll-up across all source wallets.>

## <Inbound / reverse-direction table, if applicable>

## Methodology cross-link
<Link to the per-wallet pages that contribute and to methodology.md.>

**Receipts.** <Mirrored Dune execution JSONs in `sources/`; bulk HTML
batches in the working archive — see [methodology § Receipts](../methodology.md#receipts-and-reproducibility).>
```

`observations/cex-off-ramp-summary.md` is the reference implementation.

## When to deviate

Deviate only when the data demands it (a wallet that has no on-chain activity has no flow profile to report; declare "none observed" rather than fabricating a table). Style choices (heading wording, section ordering, table size) do not justify deviation — port the page back to template.
