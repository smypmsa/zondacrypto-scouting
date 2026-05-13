# Zonda (BitBay) (0x4ff97a…0e4b)

**Address:** `0x4ff97a1bd55f7edb7f0da364d5a8ea2148ab0e4b`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps.

**Confidence:** PARTIAL.

## Attribution

Bubblemaps' `addresses/expand/magic` endpoint, queried while exploring the neighbourhood of the ZND token's top holders, returns this address with `label = "Zonda (BitBay) (0x4f…0E4b)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2025-08-14 (block 23141114); most recent 2026-01-30 (block 24347345); 29 events.
- ERC-20 events: first 2025-08-15 (block 23145136); most recent 2025-10-24 (block 23646321); 72 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $300,152 |
| Gross OUT (USD-equivalent at tx time) | $300,152 |
| Total throughput (gross in + out) | $600,303 |
| Net direction | +$0 |
| Total events ≥$1k | 3 |
| Distinct external counterparties (≥$1k cumulative) | 3 |
| Identified counterparties in this section | 0 internal + 0 external (Etherscan-tagged) |
| Counterparties without a public name tag | **3, aggregating ~$300,152 outbound and ~$300,152 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2025-09-17 → 2025-09-17 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 3 of the 3 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$300,152 outbound** and **$300,152 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $0 | $300,152 | 0 / 1 | 2025-09-17 → 2025-09-17 |
| 2 | `0x1d9937a9a79115280f1b99a84efe355a54faded8` | $250,126 | $0 | 1 / 0 | 2025-09-17 → 2025-09-17 |
| 3 | `0xf4a3b4e54c463d173cb646dcc2f68ce4ed2e130d` | $50,025 | $0 | 1 / 0 | 2025-09-17 → 2025-09-17 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x4ff97a1bd55f7edb7f0da364d5a8ea2148ab0e4b

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
