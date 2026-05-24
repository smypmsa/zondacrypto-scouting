# Zonda (BitBay) (0xa370d3…4c98)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $42,591,639 outbound across 919 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 5 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0xa370d3a30a125bb025501bf256eb6eab23d54c98`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-24 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($42,591,639 across 919 events), with no other recipient. Inbound side includes 5 hildobby-tagged CEX hot wallets contributing $42,566,261 (~100% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-24)

- First event: 2022-08-25.
- Most recent event: 2026-03-30.
- Total events (full history at $0 USD floor): 3,141.
- Distinct counterparties: 33.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-a370d3-2026-05-24.json`](../../sources/dune/zonda-bitbay-a370d3-2026-05-24.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-24)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $42,568,423 |
| Gross OUT (USD-equivalent at tx time) | $42,591,639 |
| Total throughput (gross in + out) | $85,160,062 |
| Net direction | $-23,216 |
| Distinct counterparties (no threshold) | 33 |
| Identified counterparties in this section | 3 internal + 5 external (hildobby-tagged) |
| Counterparties without a public name tag | **25, of which 0 are above the $10k cumulative cutoff and 25 are below** |
| Active period | 2022-08-25 → 2026-03-30 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $0 | $42,591,639 | 0 / 919 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $1,395 | $0 | 347 / 0 |
| Zonda Deposit Funder 2 `0x818a…0d8d` | $767 | $0 | 35 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0xdfd5…963d` | Binance 16 | $10,074,399 | 497 |
| `0x56ed…b17f` | Binance 17 | $9,176,294 | 108 |
| `0x21a3…5549` | Binance 15 | $9,039,767 | 453 |
| `0x9696…6976` | Binance 18 | $7,329,165 | 99 |
| `0x28c6…1d60` | Binance 14 | $6,946,635 | 509 |

(Aggregate hildobby-tagged IN: $42,566,261 / 5 distinct hildobby-tagged CEX hot wallets, ~100% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 33 counterparties in the full enumeration, 25 carry no public name tag in any free attribution source as of 2026-05-24. The unattributed rows aggregate **$0 outbound** and **$0 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-a370d3-counterparties.csv](zonda-bitbay-a370d3-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-a370d3-2026-05-24.json`](../../sources/dune/zonda-bitbay-a370d3-2026-05-24.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (5 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json) (key `0xa370d3a30a125bb025501bf256eb6eab23d54c98`).

## Block-explorer link

https://etherscan.io/address/0xa370d3a30a125bb025501bf256eb6eab23d54c98

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-23 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
