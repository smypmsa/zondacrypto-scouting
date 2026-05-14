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

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $272 | $300,314 | 1 / 2 | 2025-08-14 → 2026-01-30 |
| 2 | `0x1d9937a9a79115280f1b99a84efe355a54faded8` | $250,126 | $0 | 1 / 0 | 2025-09-17 → 2025-09-17 |
| 3 | `0xf4a3b4e54c463d173cb646dcc2f68ce4ed2e130d` | $50,025 | $0 | 1 / 0 | 2025-09-17 → 2025-09-17 |
| 4 | `0xead6a1a634092830314ac4d012737def1cae880d` | $0 | $0 | 0 / 3 | 2025-09-17 → 2025-09-18 |
| 5 | `0x57ecb963e6a1c93b7c00424ab6fbe256a7a588b3` | $0 | $0 | 0 / 7 | 2025-08-15 → 2025-08-29 |
| 6 | `0xe72b1fd3a623bd307ba5bffb8ce17487eed8dde1` | $0 | $0 | 0 / 2 | 2025-08-23 → 2025-08-30 |
| 7 | `0xead6fd0a8ea83d26dc840ea565b4099b0926880d` | $0 | $0 | 5 / 1 | 2025-09-18 → 2025-10-24 |
| 8 | `0xead6db2806788b3c81bccb3c782e60a7cd2d880d` | $0 | $0 | 0 / 7 | 2025-09-20 → 2025-10-03 |
| 9 | `0xe72b422481941e75b2b3aecf0c045408bd32dde1` | $0 | $0 | 0 / 1 | 2025-08-15 → 2025-08-15 |
| 10 | `0xe72b39deafbc06b77c29d65147465e31e2e0dde1` | $0 | $0 | 0 / 3 | 2025-08-15 → 2025-08-30 |
| 11 | `0xe72b6ed4c20fac361a911803fe6189e4c726dde1` | $0 | $0 | 0 / 19 | 2025-08-15 → 2025-08-31 |
| 12 | `0xead6ebdebe365f6efdd1b80c72affcb8fda5880d` | $0 | $0 | 6 / 6 | 2025-09-17 → 2025-10-24 |
| 13 | `0xead64ecd267a88490f7c92a7a8e6d25c15ae880d` | $0 | $0 | 0 / 4 | 2025-09-20 → 2025-09-27 |
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-bitbay-4ff97a-counterparties.csv`](zonda-bitbay-4ff97a-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x4ff97a1bd55f7edb7f0da364d5a8ea2148ab0e4b

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
