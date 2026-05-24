# Zonda (BitBay) (0x73bfc8…4020)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $24,181,500 outbound across 2,511 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 33 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0x73bfc8b17296cb284b7b116e519c7b84df4e4020`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-23 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-24 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($24,181,500 across 2,511 events), with no other recipient. Inbound side includes 33 hildobby-tagged CEX hot wallets contributing $22,475,977 (~93% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-24)

- First event: 2021-03-31.
- Most recent event: 2026-04-04.
- Total events (full history at $0 USD floor): 8,375.
- Distinct counterparties: 71.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-73bfc8-2026-05-24.json`](../../sources/dune/zonda-bitbay-73bfc8-2026-05-24.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-24)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $24,149,831 |
| Gross OUT (USD-equivalent at tx time) | $24,181,500 |
| Total throughput (gross in + out) | $48,331,331 |
| Net direction | $-31,668 |
| Distinct counterparties (no threshold) | 71 |
| Identified counterparties in this section | 3 internal + 33 external (hildobby-tagged) |
| Counterparties without a public name tag | **35, of which 3 are above the $10k cumulative cutoff and 32 are below** |
| Active period | 2021-03-31 → 2026-04-04 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $0 | $24,181,500 | 0 / 2511 |
| Zonda Deposit Funder 2 `0x818a…0d8d` | $4,026 | $0 | 164 / 0 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $3,783 | $0 | 2287 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x0d07…92fe` | Gate.io 1 | $6,174,725 | 961 |
| `0x28c6…1d60` | Binance 14 | $4,484,861 | 595 |
| `0x21a3…5549` | Binance 15 | $4,365,564 | 507 |
| `0xdfd5…963d` | Binance 16 | $4,107,387 | 542 |
| `0x3d55…179f` | OKX 23 | $556,275 | 18 |
| `0x5041…081a` | OKX 7 | $390,411 | 14 |
| `0x6cc5…da7b` | OKX 1 | $368,789 | 140 |
| `0x6884…3d6d` | OKX 26 | $313,748 | 11 |
| `0x56ed…b17f` | Binance 17 | $284,624 | 7 |
| `0xf16e…9b91` | KuCoin 9 | $263,930 | 126 |

<details><summary>Show 23 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x9696…6976` | Binance 18 | $253,620 | 6 |
| `0x9642…5d4e` | MEXC 21 | $200,318 | 40 |
| `0x58ed…6a51` | KuCoin 32 | $129,091 | 137 |
| `0xd91e…0747` | KuCoin 26 | $114,969 | 48 |
| `0xa83b…e09e` | Kraken 14 | $89,629 | 14 |
| `0x2982…7d67` | BitMart 18 | $83,368 | 55 |
| `0xf89d…aa40` | Bybit 5 | $79,567 | 30 |
| `0x3f5c…f0be` | Binance 1 | $48,090 | 10 |
| `0x4634…9758` | Crypto.com 2 | $28,563 | 3 |
| `0x5642…aced` | Binance 3 | $22,025 | 3 |
| `0x85b9…d69b` | Binance 10 | $21,690 | 4 |
| `0xa034…7687` | HTX 52 | $19,386 | 15 |
| `0xa1d8…3fbf` | KuCoin 3 | $17,611 | 4 |
| `0x7083…b82f` | Binance 11 | $14,772 | 3 |
| `0x501b…5861` | Kraken 70 | $13,443 | 6 |
| `0x738c…21ea` | KuCoin 12 | $8,211 | 3 |
| `0xd551…92ff` | Binance 2 | $5,997 | 2 |
| `0x6d0d…062d` | BitMart 13 | $5,840 | 1 |
| `0x0681…dbbf` | Binance 4 | $4,887 | 2 |
| `0x6c69…34be` | BingX 11 | $4,326 | 2 |
| `0xa910…22ba` | Poloniex 4 | $259 | 1 |
| `0xd38c…1330` | BingX 17 | $0 | 2 |
| `0x98ec…a128` | OKX 6 | $0 | 1 |

</details>

(Aggregate hildobby-tagged IN: $22,475,977 / 33 distinct hildobby-tagged CEX hot wallets, ~93% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 71 counterparties in the full enumeration, 35 carry no public name tag in any free attribution source as of 2026-05-24. The unattributed rows aggregate **$0 outbound** and **$1,666,046 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-73bfc8-counterparties.csv](zonda-bitbay-73bfc8-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-73bfc8-2026-05-24.json`](../../sources/dune/zonda-bitbay-73bfc8-2026-05-24.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (33 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json) (key `0x73bfc8b17296cb284b7b116e519c7b84df4e4020`).

## Block-explorer link

https://etherscan.io/address/0x73bfc8b17296cb284b7b116e519c7b84df4e4020

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-23 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-23.json`](../../sources/blocksec/labels-2026-05-23.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
