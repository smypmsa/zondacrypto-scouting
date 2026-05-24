# Zonda (BitBay) (0xf91045…43a7)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $13,267,535 outbound across 411 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 6 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0xf910450ee0d86bd4e3ee4425de0b435edd8543a7`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-24 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($13,267,535 across 411 events), with no other recipient. Inbound side includes 6 hildobby-tagged CEX hot wallets contributing $13,258,829 (~100% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-24)

- First event: 2022-08-25.
- Most recent event: 2026-03-29.
- Total events (full history at $0 USD floor): 1,247.
- Distinct counterparties: 17.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-f91045-2026-05-24.json`](../../sources/dune/zonda-bitbay-f91045-2026-05-24.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-24)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $13,258,836 |
| Gross OUT (USD-equivalent at tx time) | $13,267,535 |
| Total throughput (gross in + out) | $26,526,371 |
| Net direction | $-8,700 |
| Distinct counterparties (no threshold) | 17 |
| Identified counterparties in this section | 2 internal + 6 external (hildobby-tagged) |
| Counterparties without a public name tag | **9, of which 0 are above the $10k cumulative cutoff and 9 are below** |
| Active period | 2022-08-25 → 2026-03-29 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $0 | $13,267,535 | 0 / 411 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $6 | $0 | 2 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x4976…2327` | Binance 20 | $2,685,999 | 158 |
| `0x21a3…5549` | Binance 15 | $2,493,815 | 154 |
| `0xdfd5…963d` | Binance 16 | $2,255,510 | 128 |
| `0x9696…6976` | Binance 18 | $2,060,902 | 131 |
| `0x28c6…1d60` | Binance 14 | $2,010,395 | 126 |
| `0x56ed…b17f` | Binance 17 | $1,752,208 | 119 |

(Aggregate hildobby-tagged IN: $13,258,829 / 6 distinct hildobby-tagged CEX hot wallets, ~100% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 17 counterparties in the full enumeration, 9 carry no public name tag in any free attribution source as of 2026-05-24. The unattributed rows aggregate **$0 outbound** and **$1 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-f91045-counterparties.csv](zonda-bitbay-f91045-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-f91045-2026-05-24.json`](../../sources/dune/zonda-bitbay-f91045-2026-05-24.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (6 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json) (key `0xf910450ee0d86bd4e3ee4425de0b435edd8543a7`).

## Block-explorer link

https://etherscan.io/address/0xf910450ee0d86bd4e3ee4425de0b435edd8543a7

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-23 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
