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
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
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

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $1,006,912 | $0 | 12 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x39c89eb8…f8ca` | Gate Deposit: 0x39c89eb84fc45dab40bd4d3b273492d64c52f8ca | $350,968 | 11 |
| `0x623ae520…83e6` | Binance Deposit: 0x623AE5203c32EC44541Cc0c17BA72c6f3C5a83E6 | $8,399 | 1 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $1,036,407 | 19 |
| `0xd91efec7…0747` | KuCoin: ERC-20 Batch Transfer | $146,403 | 6 |
| `0x83c41363…627e` | KuCoin 18 | $42,962 | 1 |
| `0x9642b23e…5d4e` | MEXC 16 | $30,016 | 3 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 15 of the 22 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$1,938,638 outbound** and **$53,107 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x896088463f9660410f10c52e002ac1e274920b0d` | $0 | $1,246,865 | 0 / 21 | 2025-03-04 → 2025-11-15 |
| 2 | `0x2657e8a1caa3cfc3c7bb8d5df04fbd88e81c7ae6` | $0 | $422,666 | 0 / 1 | 2025-04-01 → 2025-04-01 |
| 3 | `0xd089de0fc339511ea2b6cfdbd0d596f7bba32f21` | $0 | $79,826 | 0 / 5 | 2025-03-27 → 2025-09-09 |
| 4 | `0x427946418a0a0fa0266d62d934100204eb2768d7` | $0 | $61,123 | 0 / 5 | 2025-02-05 → 2025-09-28 |
| 5 | `0x4b9094cc7fb251c36fc3fc86c89a4e7351d7736c` | $0 | $54,923 | 0 / 6 | 2025-05-02 → 2025-12-02 |
| 6 | `0x533671f6a2e1c20e77af941691790bad3cd3fb9c` | $53,107 | $0 | 5 / 0 | 2025-05-06 → 2025-09-01 |
| 7 | `0x2cb3b96563aa21362963b96e3e0826efe5f16984` | $0 | $11,510 | 0 / 4 | 2025-02-25 → 2025-03-18 |
| 8 | `0xb92b646197e5a3ca863193f2c2b51c1820734e32` | $0 | $10,005 | 0 / 1 | 2025-09-04 → 2025-09-04 |
| 9 | `0x0b8bdfa6cc3fad552db988b019069a3e132e404d` | $0 | $10,003 | 0 / 1 | 2025-02-04 → 2025-02-04 |
| 10 | `0xe1e1fdf680b72703c408b468a4f6c5746f02241c` | $0 | $8,606 | 0 / 1 | 2025-01-25 → 2025-01-25 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x3f1eea8dcda2b5620643aca1987d4780cae80539

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
