# Zonda (BitBay) (0x896088…0b0d)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $14,609,119 outbound across 255 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 6 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0x896088463f9660410f10c52e002ac1e274920b0d`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-24 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($14,609,119 across 255 events), with no other recipient. Inbound side includes 6 hildobby-tagged CEX hot wallets contributing $7,194,927 (~49% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-24)

- First event: 2023-12-08.
- Most recent event: 2026-04-11.
- Total events (full history at $0 USD floor): 854.
- Distinct counterparties: 58.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-896088-2026-05-24.json`](../../sources/dune/zonda-bitbay-896088-2026-05-24.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-24)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $14,602,185 |
| Gross OUT (USD-equivalent at tx time) | $14,609,119 |
| Total throughput (gross in + out) | $29,211,304 |
| Net direction | $-6,934 |
| Distinct counterparties (no threshold) | 58 |
| Identified counterparties in this section | 3 internal + 6 external (hildobby-tagged) |
| Counterparties without a public name tag | **49, of which 6 are above the $10k cumulative cutoff and 43 are below** |
| Active period | 2023-12-08 → 2026-04-11 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $2 | $14,609,119 | 1 / 255 |
| Zonda (BitBay) 0x3f1eea…0539 `0x3f1e…0539` | $1,247,031 | $0 | 23 / 0 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $43 | $0 | 55 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x0d07…92fe` | Gate.io 1 | $5,524,138 | 131 |
| `0x58ed…6a51` | KuCoin 32 | $1,204,929 | 49 |
| `0xd91e…0747` | KuCoin 26 | $166,981 | 9 |
| `0x83bd…719b` | OKX 150 | $136,198 | 2 |
| `0x28c6…1d60` | Binance 14 | $81,990 | 1 |
| `0x83c4…627e` | KuCoin 36 | $80,691 | 3 |

(Aggregate hildobby-tagged IN: $7,194,927 / 6 distinct hildobby-tagged CEX hot wallets, ~49% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 58 counterparties in the full enumeration, 49 carry no public name tag in any free attribution source as of 2026-05-24. The unattributed rows aggregate **$0 outbound** and **$6,160,182 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-896088-counterparties.csv](zonda-bitbay-896088-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-896088-2026-05-24.json`](../../sources/dune/zonda-bitbay-896088-2026-05-24.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (6 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json) (key `0x896088463f9660410f10c52e002ac1e274920b0d`).

## Block-explorer link

https://etherscan.io/address/0x896088463f9660410f10c52e002ac1e274920b0d

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-23 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
