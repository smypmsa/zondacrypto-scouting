# Zonda (BitBay) (0xcee4df…d457)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $12,448,868 outbound across 327 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 20 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0xcee4dfde1ce0260afb87f8c917726ab0502fd457`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-24 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($12,448,868 across 327 events), with no other recipient. Inbound side includes 20 hildobby-tagged CEX hot wallets contributing $12,613,254 (~100% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-24)

- First event: 2021-04-23.
- Most recent event: 2025-11-20.
- Total events (full history at $0 USD floor): 837.
- Distinct counterparties: 25.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-cee4df-2026-05-24.json`](../../sources/dune/zonda-bitbay-cee4df-2026-05-24.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-24)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $12,616,800 |
| Gross OUT (USD-equivalent at tx time) | $12,448,868 |
| Total throughput (gross in + out) | $25,065,668 |
| Net direction | $+167,932 |
| Distinct counterparties (no threshold) | 25 |
| Identified counterparties in this section | 2 internal + 20 external (hildobby-tagged) |
| Counterparties without a public name tag | **3, of which 0 are above the $10k cumulative cutoff and 3 are below** |
| Active period | 2021-04-23 → 2025-11-20 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $59 | $12,448,868 | 1 / 327 |
| Zonda Deposit Funder 2 `0x818a…0d8d` | $3,487 | $0 | 117 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0xdfd5…963d` | Binance 16 | $3,137,024 | 82 |
| `0x28c6…1d60` | Binance 14 | $3,083,175 | 88 |
| `0x21a3…5549` | Binance 15 | $2,440,624 | 69 |
| `0x4c60…68cd` | Kraken 68 | $1,000,596 | 42 |
| `0x26a7…d8b7` | Kraken 41 | $965,166 | 46 |
| `0x89e5…7c40` | Kraken 7 | $400,136 | 3 |
| `0x56ed…b17f` | Binance 17 | $350,744 | 2 |
| `0xa83b…e09e` | Kraken 14 | $290,626 | 24 |
| `0x29d5…274b` | Bitso 2 | $218,086 | 8 |
| `0x9696…6976` | Binance 18 | $180,207 | 2 |

<details><summary>Show 10 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0xc6be…63da` | Kraken 8 | $100,371 | 5 |
| `0xd551…92ff` | Binance 2 | $98,598 | 2 |
| `0x3f5c…f0be` | Binance 1 | $82,667 | 3 |
| `0x85b9…d69b` | Binance 10 | $74,313 | 3 |
| `0x7083…b82f` | Binance 11 | $60,622 | 1 |
| `0x0681…dbbf` | Binance 4 | $57,826 | 1 |
| `0x5642…aced` | Binance 3 | $33,303 | 2 |
| `0xe9f7…b785` | Kraken Hot Wallet | $13,633 | 2 |
| `0x8a10…e76a` | Kraken 42 | $13,023 | 3 |
| `0xe149…1724` | Kraken 71 | $12,515 | 1 |

</details>

(Aggregate hildobby-tagged IN: $12,613,254 / 20 distinct hildobby-tagged CEX hot wallets, ~100% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 25 counterparties in the full enumeration, 3 carry no public name tag in any free attribution source as of 2026-05-24. The unattributed rows aggregate **$0 outbound** and **$0 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-cee4df-counterparties.csv](zonda-bitbay-cee4df-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-cee4df-2026-05-24.json`](../../sources/dune/zonda-bitbay-cee4df-2026-05-24.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (20 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json) (key `0xcee4dfde1ce0260afb87f8c917726ab0502fd457`).

## Block-explorer link

https://etherscan.io/address/0xcee4dfde1ce0260afb87f8c917726ab0502fd457

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-23 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
