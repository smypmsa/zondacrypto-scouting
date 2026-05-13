# Zonda Deposit Wallet (0x82c829…900c)

**Address:** `0x82c829237159287dac6fc62eb139e6a89195900c`

**Chain:** Ethereum.

**Role:** Deposit-side ZondaCrypto wallet.

**Confidence:** CONFIRMED.

## Attribution

Two independent primary label sources point to this address as a ZondaCrypto wallet:

1. **Bubblemaps** — the `addresses/token-top-holders` API for the ZND token returns this address with `address_details.label = "Zonda Deposit Wallet"` and `entity_id = "zonda"`.[^1]
2. **BlockSec MetaSleuth** — the `address-label/api/v3/labels` endpoint returns `main_entity = "Zonda (BitBay)"` under the `EXCHANGE` category.[^2] The receipt of the BlockSec response is preserved at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json).

In addition, Etherscan's address page shows this wallet transacts directly with `Zonda: Deposit Funder 1` (see [`zonda-deposit-funder-1.md`](zonda-deposit-funder-1.md)), consistent with the deposit-wallet role.

The address is currently a top-100 ZND holder (≈0.046% of supply).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2022-11-28 (block 16068080); most recent 2026-04-03 (block 24796973); 262 events.
- ERC-20 events: first 2022-12-02 (block 16100080); most recent 2026-04-03 (block 24796973); 351 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $460,941 |
| Gross OUT (USD-equivalent at tx time) | $467,870 |
| Total throughput (gross in + out) | $928,811 |
| Net direction | −$6,928 |
| Total events ≥$1k | 228 |
| Distinct external counterparties (≥$1k cumulative) | 18 |
| Identified counterparties in this section | 1 internal + 17 external (Etherscan-tagged) |
| Counterparties without a public name tag | **1, aggregating ~$0 outbound and ~$5,004 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2022-12-02 → 2026-01-21 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $467,870 | 111 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $158,566 | 34 |
| `0xdfd5293d…963d` | Binance 16 | $67,228 | 11 |
| `0x21a31ee1…5549` | Binance 15 | $42,526 | 9 |
| `0x28c6c062…1d60` | Binance 14 | $33,758 | 6 |
| `0xf89d7b9c…aa40` | Bybit: Hot Wallet | $25,347 | 5 |
| `0x9642b23e…5d4e` | MEXC 16 | $19,095 | 3 |
| `0x260b364f…4cea` | Bybit: Opensea User | $17,055 | 2 |
| `0x77134cbc…35ec` | Bitfinex: Hot Wallet | $15,696 | 11 |
| `0x48ec5560…6b0c` | Bitstamp: Wallet | $13,674 | 6 |
| `0xae2d4617…673f` | Kraken 10 | $12,585 | 5 |
| `0x05ff6964…f381` | Kraken: Hot Wallet 4 | $12,169 | 5 |
| `0xa03400e0…7687` | HTX 48 | $10,932 | 7 |
| `0xe7178ad7…d5c6` | Kraken 47 | $10,115 | 5 |
| `0x7f604d59…b752` | Bitstamp 61 | $6,960 | 4 |
| `0xee7ae85f…4055` | Binance: Hot Wallet 34 | $6,772 | 1 |
| `0xd91efec7…0747` | KuCoin: ERC-20 Batch Transfer | $1,742 | 1 |
| `0x56eddb7a…b17f` | Binance 17 | $1,716 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 1 of the 19 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$5,004 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43` | $5,004 | $0 | 1 / 0 | 2025-04-30 → 2025-04-30 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x82c829237159287dac6fc62eb139e6a89195900c

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
[^2]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`. Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
