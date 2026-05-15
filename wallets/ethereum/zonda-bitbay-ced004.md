# Zonda (BitBay) (0xced0046…2f06)

**Address:** `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from 18+ centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet).

**Confidence:** PARTIAL.

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, and `name_tag = "Zonda (BitBay): Deposit Address"`.[^1] No matching public name tag on Etherscan as of 2026-05-15; no row in hildobby's Dune compilation (query 3237025). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow ($43.7M / 245 events) goes to Zonda 5 alone, with no other recipient. Inbound side is dominated by 18 hildobby-tagged CEX hot wallets across 15+ exchanges (full table below). The deposit-address operational signature is unambiguous.

## Activity (Ethereum, probed 2026-05-15)

- First event: 2022-08-31.
- Most recent event: 2026-03-29.
- Total events: 472 (227 IN + 245 OUT).
- Distinct counterparties: 41.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Reproducible via query `7500518` execution `01KRN6VMSTPTJ0DRTFG49PS11J`.

## Flow profile (Ethereum, Dune-aggregated 2026-05-15)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profile) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $43,598,490 |
| Gross OUT (USD-equivalent at tx time) | $43,668,293 |
| Total throughput (gross in + out) | $87,266,784 |
| Net direction | -$69,803 |
| Distinct counterparties (no threshold) | 41 |
| Identified counterparties in this section | 1 internal + 18 external (hildobby-tagged) |
| Counterparties without a public name tag | **23, of which 12 are above the $10k cumulative cutoff and 11 are below** |
| Active period | 2022-08-31 → 2026-03-29 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged rows (each verified against hildobby `query_3237025`). PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory   [internal flows]

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $43,668,283 | 0 / 212 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x267be1c1…ffdc0` | Kraken 4 | $20,759,886 | 50 |
| `0x77134cbc…35ec` | Bitfinex Hot Wallet | $14,213,566 | 38 |
| `0x9aa65464…6687` | Blockchain.com 6 | $581,005 | 2 |
| `0x1522900b…e428` | Bitstamp 2 | $574,135 | 6 |
| `0xc098b2a3…3a94` | FTX 2 | $544,793 | 26 |
| `0xbb4d1dc5…ad1d` | BTSE 1 | $498,036 | 9 |
| `0xd7efcbb8…17e4` | OKX 34 | $441,338 | 9 |
| `0xde279a5c…bb12` | BTSE 4 | $337,144 | 7 |
| `0xcad621da…8fdd` | KuCoin 10 | $317,872 | 5 |
| `0x416299aa…eef5` | Luno 2 | $307,664 | 3 |
| `0x46340b20…9758` | Crypto.com 2 | $268,749 | 3 |
| `0x28c6c062…1d60` | Binance 14 | $239,521 | 7 |
| `0x56eddb7a…b17f` | Binance 17 | $208,089 | 5 |
| `0x264bd829…7b5` | Paxos 4 | $194,517 | 4 |
| `0xf89d7b9c…aa40` | Bybit 5 | $174,648 | 3 |
| `0x079a8926…dc63` | Bitvavo 19 | $145,094 | 3 |
| `0xb01cb49f…331c` | bitFlyer 2 | $113,802 | 3 |
| `0x74dec05e…f9a1` | Bitpanda 1 | $79,810 | 2 |

(Aggregate hildobby-tagged IN: $39.0M / 18 distinct CEXes-of-record, ~90% of total inbound USD.)

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 41 external counterparties in the full enumeration, 22 carry no public name tag in any free attribution source as of 2026-05-15. The unattributed rows aggregate **$0 outbound** (all outbound is internal-to-Zonda-5) and **$4,556,090 inbound**, of which $2.4M comes from `0x65cbc8aa…ba084` (50 events) and the remaining $2.1M from 11 other addresses each at $50k–$580k cumulative. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-ced004-counterparties.csv](zonda-bitbay-ced004-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: `case/sources/dune/zonda-bitbay-ced004-2026-05-15.json` (query 7500518, execution `01KRN6VMSTPTJ0DRTFG49PS11J`).
- hildobby intersect: query 3237025 results embedded in `case/sources/dune/b12-hubdistrib-funders-hildobby-2026-05-14.json` (17 hits) + `zonda-bitbay-ced004-2026-05-15.json` rolling re-intersect (18 hits at finer-grained event aggregation).
- BlockSec MetaSleuth API v3 response: `case/sources/blocksec/labels-2026-05-15.json` (key `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06`).

## Block-explorer link

https://etherscan.io/address/0xced004645e40f1bd5d11e6562e8fdbe9f4862f06

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-15 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`. Receipt at `case/sources/blocksec/labels-2026-05-15.json`. Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
