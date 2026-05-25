# Zonda (BitBay) (0x47ef94…bb8b)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-25). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $16,968,056 outbound across 2,838 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 20 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0x47ef949598e02b90ae2a38624f07b77c18fabb8b`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-25 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-25 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24 (re-used; same source)). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($16,968,056 across 2,838 events), with no other recipient. Inbound side includes 20 hildobby-tagged CEX hot wallets contributing $15,169,976 (~90% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-25)

- First event: 2021-03-31.
- Most recent event: 2026-04-03.
- Total events (full history at $0 USD floor): 10,009.
- Distinct counterparties: 58.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-47ef94-2026-05-25.json`](../../sources/dune/zonda-bitbay-47ef94-2026-05-25.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-25)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $16,815,901 |
| Gross OUT (USD-equivalent at tx time) | $16,968,056 |
| Total throughput (gross in + out) | $33,783,957 |
| Net direction | $-152,156 |
| Distinct counterparties (no threshold) | 58 |
| Identified counterparties in this section | 3 internal + 20 external (hildobby-tagged) |
| Counterparties without a public name tag | **35, of which 2 are above the $10k cumulative cutoff and 33 are below** |
| Active period | 2021-03-31 → 2026-04-03 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24 (re-used; same source)). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $28 | $16,968,056 | 1 / 2838 |
| Zonda Deposit Funder 2 `0x818a…0d8d` | $7,494 | $0 | 254 / 0 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $3,413 | $0 | 2053 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0xdfd5…963d` | Binance 16 | $3,662,794 | 1100 |
| `0x21a3…5549` | Binance 15 | $3,454,170 | 1097 |
| `0x28c6…1d60` | Binance 14 | $3,097,519 | 1191 |
| `0x3f5c…f0be` | Binance 1 | $806,425 | 211 |
| `0xf89d…aa40` | Bybit 5 | $553,541 | 191 |
| `0x56ed…b17f` | Binance 17 | $549,173 | 45 |
| `0xfbb1…bb98` | Bittrex 1 | $482,831 | 354 |
| `0x9696…6976` | Binance 18 | $478,595 | 33 |
| `0x85b9…d69b` | Binance 10 | $456,444 | 92 |
| `0xd551…92ff` | Binance 2 | $396,216 | 78 |

<details><summary>Show 10 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x5642…aced` | Binance 3 | $362,893 | 76 |
| `0x0681…dbbf` | Binance 4 | $359,100 | 75 |
| `0x7083…b82f` | Binance 11 | $332,024 | 68 |
| `0xc2ba…4793` | Bidesk 14 | $67,229 | 6 |
| `0x99bd…96b9` | Bidesk 22 | $54,627 | 6 |
| `0x8bc4…d7f2` | Bidesk 50 | $36,525 | 3 |
| `0x42d1…e2cd` | Kanga Exchange 1 | $17,909 | 3 |
| `0xa1d8…3fbf` | KuCoin 3 | $1,961 | 1 |
| `0x89e5…7c40` | Kraken 7 | $0 | 1 |
| `0x0d07…92fe` | Gate.io 1 | $0 | 8 |

</details>

(Aggregate hildobby-tagged IN: $15,169,976 / 20 distinct hildobby-tagged CEX hot wallets, ~90% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 58 counterparties in the full enumeration, 35 carry no public name tag in any free attribution source as of 2026-05-25. The unattributed rows aggregate **$0 outbound** and **$1,634,990 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-47ef94-counterparties.csv](zonda-bitbay-47ef94-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-47ef94-2026-05-25.json`](../../sources/dune/zonda-bitbay-47ef94-2026-05-25.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (20 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-25.json`](../../sources/blocksec/labels-2026-05-25.json) (key `0x47ef949598e02b90ae2a38624f07b77c18fabb8b`).

## Block-explorer link

https://etherscan.io/address/0x47ef949598e02b90ae2a38624f07b77c18fabb8b

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-25 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-25.json`](../../sources/blocksec/labels-2026-05-25.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
