# Zonda (BitBay) (0x56d943…4778)

**Address:** `0x56d943aea92b099228b31f01cd12bd4aa39b4778`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps. Bubblemaps further marks it as CEX-related (`is_cex = true`).

**Confidence:** PARTIAL.

## Attribution

Bubblemaps' `addresses/token-top-holders` endpoint for the ZND token returns this address with `label = "Zonda (BitBay) (0x56…4778)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

The address is currently active (latest activity within minutes of the snapshot), holds ~1.2 ETH and ~$22k across 142 tokens, and ranks as a top-100 ZND holder at 0.0055% of supply.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2025-08-04 (block 23066436); most recent 2026-05-13 (block 25085262); ≥ 10,000 events.
- ERC-20 events: first 2025-08-04 (block 23066882); most recent 2026-05-13 (block 25085262); ≥ 10,000 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $3,806,066 |
| Gross OUT (USD-equivalent at tx time) | $207,323 |
| Total throughput (gross in + out) | $4,013,389 |
| Net direction | +$3,598,743 |
| Total events ≥$1k | 829 |
| Distinct external counterparties (≥$1k cumulative) | 455 |
| Identified counterparties in this section | 0 internal + 10 external (Etherscan-tagged) |
| Counterparties without a public name tag | **445, aggregating ~$203,129 outbound and ~$205,309 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2025-08-04 → 2026-05-12 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x674e7b96…7b35` | ByBit Deposit: 0x674E7B96a0f5FB81dAda4A6F9e7B07A7E2067B35 | $3,096 | 3 |
| `0xb61b6f84…4bb0` | Binance Deposit: 0xB61b6f8480BD0581931d64964fb2640fa6134BB0 | $1,099 | 1 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x05ff6964…f381` | Kraken: Hot Wallet 4 | $2,428,358 | 208 |
| `0xf30ba13e…0eb0` | Kraken: Hot Wallet 2 | $915,854 | 386 |
| `0xae2d4617…673f` | Kraken 10 | $163,342 | 14 |
| `0x267be1c1…fdc0` | Kraken 4 | $81,599 | 37 |
| `0x6d0cf1f6…3d26` | Kraken 17 | $6,973 | 6 |
| `0x23d4df46…d9fd` | Kraken 93 | $2,313 | 2 |
| `0x16b2b042…c415` | Kraken 33 | $1,160 | 1 |
| `0x735fd3c5…0a1c` | Kraken 18 | $1,158 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 445 of the 455 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$203,129 outbound** and **$205,309 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x2744dfd9898f0babbc570cc594bbbc84b487a22b` | $187,783 | $0 | 16 / 0 | 2026-04-23 → 2026-05-12 |
| 2 | `0x0895934c201640b85f87c97ac67106c41a801312` | $0 | $131,558 | 0 / 85 | 2025-10-08 → 2026-05-10 |
| 3 | `0xb6be26445f21e41bc69197fe68f697fc1a862f19` | $0 | $41,734 | 0 / 28 | 2025-08-05 → 2025-10-06 |
| 4 | `0xfd2636d89bb1fd7e9858e0a21ea55acf50f1a6d5` | $0 | $12,041 | 0 / 11 | 2025-11-18 → 2025-11-24 |
| 5 | `0x5559e8bc0f49cedef12dc768f7a60d6b030e7032` | $0 | $5,027 | 0 / 5 | 2026-03-01 → 2026-03-02 |
| 6 | `0x2cc8e4721a001f1921298bc9d894aca13630b0c6` | $3,530 | $0 | 3 / 0 | 2025-09-26 → 2026-02-06 |
| 7 | `0xd75f738a45afaa4c1c7a850b3ca477c17f5c94a2` | $2,401 | $0 | 1 / 0 | 2025-09-15 → 2025-09-15 |
| 8 | `0x2cdd6bcf572b0a9f18ead89815a4a787616f772c` | $2,356 | $0 | 2 / 0 | 2025-11-03 → 2026-02-05 |
| 9 | `0x700e0841ce0892969d2f9cf523c6298b3ef056a6` | $2,329 | $0 | 2 / 0 | 2025-09-26 → 2025-11-21 |
| 10 | `0xb38bb97d450cda1ce623c0ac97aef19f4ae7bbb7` | $2,315 | $0 | 2 / 0 | 2025-09-26 → 2025-11-21 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x56d943aea92b099228b31f01cd12bd4aa39b4778

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
