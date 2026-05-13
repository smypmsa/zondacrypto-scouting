# Zonda (BitBay) (0x879882…b54f)

**Address:** `0x879882c59d9cc548d6c0e7d0238e8aa40858b54f`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps.

**Confidence:** PARTIAL.

## Attribution

Bubblemaps' `addresses/token-top-holders` endpoint for the ZND token returns this address with `label = "Zonda (BitBay) (0x87…B54F)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

The address is a top-100 ZND holder at 0.0119% of supply.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-28 (block 12327290); most recent 2026-04-02 (block 24792762); 1,259 events.
- ERC-20 events: first 2021-03-31 (block 12147725); most recent 2026-04-02 (block 24792762); 2,112 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $4,878,528 |
| Gross OUT (USD-equivalent at tx time) | $4,926,877 |
| Total throughput (gross in + out) | $9,805,405 |
| Net direction | −$48,349 |
| Total events ≥$1k | 967 |
| Distinct external counterparties (≥$1k cumulative) | 17 |
| Identified counterparties in this section | 1 internal + 14 external (Etherscan-tagged) |
| Counterparties without a public name tag | **3, aggregating ~$0 outbound and ~$31,500 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-03-31 → 2026-03-27 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $4,926,877 | 417 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x28c6c062…1d60` | Binance 14 | $1,715,594 | 197 |
| `0xdfd5293d…963d` | Binance 16 | $1,307,062 | 150 |
| `0x21a31ee1…5549` | Binance 15 | $1,267,205 | 161 |
| `0x9696f59e…6976` | Binance 18 | $312,919 | 15 |
| `0x56eddb7a…b17f` | Binance 17 | $124,754 | 8 |
| `0xee7ae85f…4055` | Binance: Hot Wallet 34 | $39,766 | 3 |
| `0x85b931a3…d69b` | Binance 10 | $15,490 | 2 |
| `0x56428636…aced` | Binance 3 | $15,395 | 1 |
| `0x42d17b7f…e2cd` | Kanga Exchange 1 | $13,053 | 2 |
| `0x3f5ce5fb…f0be` | Binance | $9,759 | 1 |
| `0x0681d8db…dbbf` | Binance 4 | $9,587 | 1 |
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $7,483 | 1 |
| `0xb8001c3e…1ec1` | Cobo: Custody 1 | $4,984 | 2 |
| `0xc2ba04e8…4793` | Bidesk 14 | $3,976 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 3 of the 18 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$31,500 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xa7512a0d9cc166ff05eb79f3a52095eab114b856` | $29,813 | $0 | 4 / 0 | 2021-06-15 → 2021-07-01 |
| 2 | `0x7bd8efab672250de65ba4ba3bc6c3aa08120a1c3` | $1,687 | $0 | 1 / 0 | 2021-06-16 → 2021-06-16 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x879882c59d9cc548d6c0e7d0238e8aa40858b54f

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
