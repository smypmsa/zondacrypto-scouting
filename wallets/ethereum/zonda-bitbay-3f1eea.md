# Zonda (BitBay) (0x3f1eea…0539)

**Address:** `0x3f1eea8dcda2b5620643aca1987d4780cae80539`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps.

**Confidence:** PARTIAL.

## Attribution

Bubblemaps' `addresses/expand/magic` endpoint, queried while exploring the neighbourhood of the ZND token's top holders, returns this address with `label = "Zonda (BitBay) (0x3F…0539)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-12-17 (block 21422929); most recent 2025-12-12 (block 23996973); 168 events.
- ERC-20 events: first 2025-01-23 (block 21686402); most recent 2026-03-29 (block 24763072); 3,329 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $2,315,807 |
| Gross OUT (USD-equivalent at tx time) | $2,298,004 |
| Total throughput (gross in + out) | $4,613,811 |
| Net direction | +$17,803 |
| Total events ≥$1k | 112 |
| Distinct external counterparties (≥$1k cumulative) | 21 |
| Identified counterparties in this section | 1 internal + 6 external (Etherscan-tagged) |
| Counterparties without a public name tag | **15, aggregating ~$1,938,638 outbound and ~$53,107 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2025-01-23 → 2025-12-02 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $1,006,912 | $0 | 12 |

### External counterparties — confirmed via public name tag
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x39c89eb8…f8ca` | Gate Deposit: 0x39c89eb84fc45dab40bd4d3b273492d64c52f8ca | $350,968 | 11 |
| `0x623ae520…83e6` | Binance Deposit: 0x623AE5203c32EC44541Cc0c17BA72c6f3C5a83E6 | $8,399 | 1 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x0d0707963952f2fba59dd06f2b425ace40b492fe` | Gate.io 1 | $1,036,407 | $0 | 19 / 0 |
| `0xd91efec7e42f80156d1d9f660a69847188950747` | KuCoin 26 | $146,403 | $0 | 6 / 0 |
| `0x83c41363cbee0081dab75cb841fa24f3db46627e` | KuCoin 36 | $42,962 | $0 | 1 / 0 |
| `0x9642b23ed1e01df1092b92641051881a322f5d4e` | MEXC 21 | $30,016 | $0 | 3 / 0 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $1,036,407 | 19 |
| `0xd91efec7…0747` | KuCoin: ERC-20 Batch Transfer | $146,403 | 6 |
| `0x83c41363…627e` | KuCoin 18 | $42,962 | 1 |
| `0x9642b23e…5d4e` | MEXC 16 | $30,016 | 3 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 15 of the 22 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$1,938,638 outbound** and **$53,107 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x896088463f9660410f10c52e002ac1e274920b0d` | $0 | $1,247,031 | 0 / 23 | 2024-12-30 → 2025-12-12 |
| 2 | `0x2657e8a1caa3cfc3c7bb8d5df04fbd88e81c7ae6` | $0 | $422,666 | 0 / 1 | 2025-04-01 → 2025-04-01 |
| 3 | `0xd089de0fc339511ea2b6cfdbd0d596f7bba32f21` | $0 | $79,829 | 0 / 6 | 2025-03-27 → 2025-09-09 |
| 4 | `0x427946418a0a0fa0266d62d934100204eb2768d7` | $0 | $61,123 | 0 / 5 | 2025-02-05 → 2025-09-28 |
| 5 | `0x4b9094cc7fb251c36fc3fc86c89a4e7351d7736c` | $0 | $54,923 | 0 / 6 | 2025-05-02 → 2025-12-02 |
| 6 | `0x533671f6a2e1c20e77af941691790bad3cd3fb9c` | $53,107 | $0 | 5 / 0 | 2025-05-06 → 2025-09-01 |
| 7 | `0x2cb3b96563aa21362963b96e3e0826efe5f16984` | $0 | $11,510 | 0 / 4 | 2025-02-25 → 2025-03-18 |
| 8 | `0xb92b646197e5a3ca863193f2c2b51c1820734e32` | $0 | $10,005 | 0 / 1 | 2025-09-04 → 2025-09-04 |
| 9 | `0x0b8bdfa6cc3fad552db988b019069a3e132e404d` | $0 | $10,003 | 0 / 1 | 2025-02-04 → 2025-02-04 |
| 10 | `0xe1e1fdf680b72703c408b468a4f6c5746f02241c` | $0 | $8,606 | 0 / 1 | 2025-01-25 → 2025-01-25 |
| 11 | `0xfe62169497c8458a28480ebd8068dd10b040fd5b` | $0 | $7,598 | 0 / 1 | 2025-05-12 → 2025-05-12 |
| 12 | `0xd48becfc52e6530b4ecc40246294fc7b1c0e7312` | $0 | $7,506 | 0 / 2 | 2025-02-28 → 2025-03-14 |
| 13 | `0x9baa14e411a2c7e5d51dcecf931c4f9e646b99ae` | $0 | $7,002 | 0 / 2 | 2025-11-12 → 2025-11-12 |
| 14 | `0xc2d2ecd435510226bb8728542fb18ee03a71d82f` | $0 | $6,003 | 0 / 3 | 2025-01-23 → 2025-01-25 |
| 15 | `0xf716fce157ebe1c470c0c655d0d28688d0916886` | $0 | $5,503 | 0 / 2 | 2025-02-08 → 2025-02-08 |
| 16 | `0x5058612ea1ed55eab27578e592cf4f4ebe0e1b22` | $0 | $387 | 0 / 1 | 2025-07-29 → 2025-07-29 |
| 17 | `0x0e2c4d3c35b158cb69f99bdc322c370f94b19fd4` | $361 | $0 | 1 / 0 | 2024-12-17 → 2024-12-17 |
| 18 | `0x47bb64b2a10e991f3e7db869312fe7d655c82b8e` | $160 | $0 | 1 / 0 | 2024-12-17 → 2024-12-17 |
| 19 | `0xf71647ea781b935cf23dc84a5da14d41460c6886` | $0 | $0 | 3 / 6 | 2025-02-08 → 2025-02-09 |
| 20 | `0x623a7323f0be0601bf8265b9958a5fef3b3f83e6` | $0 | $0 | 1 / 0 | 2025-08-23 → 2025-08-23 |
| 21 | `0x896063b4950123ba5a1cd1a0eec8a008f8c50b0d` | $0 | $0 | 8 / 66 | 2025-03-05 → 2025-12-12 |
| 22 | `0xf716292be3c806503819340c4df1e43c2d0c6886` | $0 | $0 | 2 / 0 | 2025-02-08 → 2025-02-08 |
| 23 | `0xd089c8df9d6af031d1f8397cc5c75793fa5f2f21` | $0 | $0 | 2 / 0 | 2025-08-26 → 2025-09-03 |
| 24 | `0xd0890baafa946e76ba036cde6001b2f442b22f21` | $0 | $0 | 2 / 0 | 2025-03-27 → 2025-03-27 |
| 25 | `0x39c81ebc8da9510702eab4fcc2f1d6b959b2f8ca` | $0 | $0 | 15 / 243 | 2025-02-26 → 2025-04-21 |
| 26 | `0x896082bab54684c13e5c2905bf2771811b590b0d` | $0 | $0 | 11 / 294 | 2025-03-05 → 2025-04-25 |
| 27 | `0x265761f86fa6f79bdd45de35fd6df0bac3e37ae6` | $0 | $0 | 1 / 0 | 2025-04-01 → 2025-04-01 |
| 28 | `0xd089695292d5654b3ab8207d48beb128036f2f21` | $0 | $0 | 1 / 0 | 2025-08-26 → 2025-08-26 |
| 29 | `0x42794096038988c37efb11594e5534b8617868d7` | $0 | $0 | 1 / 0 | 2025-04-01 → 2025-04-01 |
| 30 | `0xd48b6be90160f9ac104753d0e411fc7cb44e7312` | $0 | $0 | 1 / 0 | 2025-03-14 → 2025-03-14 |
| 31 | `0xd089eff8dca5a3c88b229b48f5a0f781d7472f21` | $0 | $0 | 5 / 5 | 2025-03-27 → 2025-09-10 |
| 32 | `0x623abe73f9aa4e1fc09df8f06f94e4095fce83e6` | $0 | $0 | 2 / 0 | 2025-08-23 → 2025-08-23 |
| 33 | `0x39c87112d1add6cf27d0563f31d59429d06bf8ca` | $0 | $0 | 11 / 6 | 2025-03-19 → 2025-12-09 |
| 34 | `0x39c85f86b5f54e9afcb08fb87caa1081701df8ca` | $0 | $0 | 3 / 314 | 2025-03-25 → 2025-09-10 |
| 35 | `0x0cb3ab936e3808deef10f94701f0417762d76984` | $0 | $0 | 1 / 0 | 2025-02-25 → 2025-02-25 |
| 36 | `0x4b90e147252535e988555ecacd92954f6f20736c` | $0 | $0 | 1 / 0 | 2025-05-02 → 2025-05-02 |
| 37 | `0x427989c5f2dac5ea274f95d59fe064d7d90068d7` | $0 | $0 | 2 / 5 | 2025-04-01 → 2025-09-28 |
| 38 | `0x2cb3eb806bc040b70cab0f1287597ceb7bd76984` | $0 | $0 | 1 / 127 | 2025-02-25 → 2025-04-03 |
| 39 | `0x2657909431427eed4df6d5fa860e26e603187ae6` | $0 | $0 | 1 / 2 | 2025-04-01 → 2025-04-01 |
| 40 | `0x427944c44da240a27aa396f32b2fe832129768d7` | $0 | $0 | 1 / 0 | 2025-06-12 → 2025-06-12 |
| 41 | `0x427980206745824daad5d3417d8881f7249868d7` | $0 | $0 | 0 / 3 | 2025-09-28 → 2025-10-03 |
| 42 | `0x265712dafc085bf965442857846bf7fc116c7ae6` | $0 | $0 | 0 / 1 | 2025-04-01 → 2025-04-01 |
| 43 | `0x2cb31e1e6f3673543b7f4a0e8bc04c67bf556984` | $0 | $0 | 0 / 1 | 2025-02-25 → 2025-02-25 |
| 44 | `0x39c86a8eb6c50acc84e0116600c762e94e82f8ca` | $0 | $0 | 1 / 2 | 2025-09-19 → 2025-09-19 |
| 45 | `0xd5430cf61195303fe81ab2123a5ee70b5d9ffc71` | $0 | $0 | 0 / 1 | 2025-12-12 → 2025-12-12 |
| 46 | `0x896bd43439b5240024891b40ac51b3abfc920b0d` | $0 | $0 | 0 / 254 | 2025-03-04 → 2025-10-04 |
| 47 | `0x4b90c2d51aac805d73013914e32e1f0e715e736c` | $0 | $0 | 1 / 3 | 2025-09-02 → 2025-12-02 |
| 48 | `0x4b901c9f427e419e37289ab36127eeb2d998736c` | $0 | $0 | 0 / 2 | 2025-09-03 → 2025-09-20 |
| 49 | `0x265711a85d7192f38ff9b0864512487bb7937ae6` | $0 | $0 | 0 / 18 | 2025-04-01 → 2025-06-01 |
| 50 | `0x5cfd2f9c803b363f240988fea1424e38d09ac155` | $0 | $0 | 1 / 0 | 2025-09-03 → 2025-09-03 |
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-bitbay-3f1eea-counterparties.csv`](zonda-bitbay-3f1eea-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x3f1eea8dcda2b5620643aca1987d4780cae80539

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
