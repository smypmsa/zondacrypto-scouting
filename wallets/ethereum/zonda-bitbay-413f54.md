# Zonda (BitBay) (0x413f54…d6b8)

> **Plain-language summary.** An Ethereum deposit address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-25). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: $11,295,199 outbound across 186 events lands on Zonda 5 alone (`0x6edf968d…5048`, the operator's multichain MM wallet), while the inbound side aggregates 10 hildobby-tagged centralised-exchange hot wallets across the wallet's full history.

**Address:** `0x413f54b9308f35e1ae954a111acd059b9083d6b8`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`, captured 2026-05-25 against chain_id=1.[^1] No matching public name tag on Etherscan as of 2026-05-25 (verified by fresh HTML fetch); no matching row in hildobby's Dune compilation (query 3237025, snapshot 2026-05-24 (re-used; same source)). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow goes to Zonda 5 alone ($11,295,199 across 186 events), with no other recipient. Inbound side includes 10 hildobby-tagged CEX hot wallets contributing $11,294,946 (~100% of total inbound USD). The deposit-address operational signature matches the canonical Zonda deposit-address pattern previously CONFIRMED for `0xced004…2f06` and `0x3ef668…2eda`.

## Activity (Ethereum, probed 2026-05-25)

- First event: 2022-11-02.
- Most recent event: 2026-03-26.
- Total events (full history at $0 USD floor): 393.
- Distinct counterparties: 19.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Receipt: [`../../sources/dune/zonda-bitbay-413f54-2026-05-25.json`](../../sources/dune/zonda-bitbay-413f54-2026-05-25.json) (query 7500518).

## Flow profile (Ethereum, Dune-aggregated 2026-05-25)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $11,295,132 |
| Gross OUT (USD-equivalent at tx time) | $11,295,199 |
| Total throughput (gross in + out) | $22,590,332 |
| Net direction | $-67 |
| Distinct counterparties (no threshold) | 19 |
| Identified counterparties in this section | 3 internal + 10 external (hildobby-tagged) |
| Counterparties without a public name tag | **6, of which 0 are above the $10k cumulative cutoff and 6 are below** |
| Active period | 2022-11-02 → 2026-03-26 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against the local inventory roster and hildobby `query_3237025` snapshot 2026-05-24 (re-used; same source)). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf…5048` | $0 | $11,295,199 | 0 / 186 |
| Zonda Deposit Funder 2 `0x818a…0d8d` | $186 | $0 | 9 / 0 |
| Zonda Deposit Funder 1 `0x5bff…9503` | $1 | $0 | 1 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x89e5…7c40` | Kraken 7 | $7,058,469 | 45 |
| `0x267b…fdc0` | Kraken 4 | $2,876,602 | 17 |
| `0xa83b…e09e` | Kraken 14 | $831,062 | 54 |
| `0xc6be…63da` | Kraken 8 | $182,273 | 23 |
| `0x6d0c…3d26` | Kraken 55 | $165,626 | 27 |
| `0xf7cd…c5c9` | Kraken 66 | $76,082 | 9 |
| `0xcdc8…ea9c` | Kraken 40 | $55,088 | 8 |
| `0xe0bb…c37a` | Kraken 73 | $25,080 | 2 |
| `0xea57…c288` | Kraken 65 | $24,663 | 3 |
| `0x6cc5…da7b` | OKX 1 | $0 | 1 |

(Aggregate hildobby-tagged IN: $11,294,946 / 10 distinct hildobby-tagged CEX hot wallets, ~100% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 19 counterparties in the full enumeration, 6 carry no public name tag in any free attribution source as of 2026-05-25. The unattributed rows aggregate **$0 outbound** and **$0 inbound** (most outbound flow is internal to Zonda 5). These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-413f54-counterparties.csv](zonda-bitbay-413f54-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: [`../../sources/dune/zonda-bitbay-413f54-2026-05-25.json`](../../sources/dune/zonda-bitbay-413f54-2026-05-25.json) (query 7500518).
- hildobby intersect: query 3237025 snapshot at [`../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json`](../../sources/dune/hildobby-3237025-snapshot-2026-05-24.json) (10 hits on this wallet's counterparties).
- BlockSec MetaSleuth API v3 response: [`../../sources/blocksec/labels-2026-05-25.json`](../../sources/blocksec/labels-2026-05-25.json) (key `0x413f54b9308f35e1ae954a111acd059b9083d6b8`).

## Block-explorer link

https://etherscan.io/address/0x413f54b9308f35e1ae954a111acd059b9083d6b8

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-25 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, `name_tag = "Zonda (BitBay): Deposit Address"`. Receipt at [`../../sources/blocksec/labels-2026-05-25.json`](../../sources/blocksec/labels-2026-05-25.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
