# Zonda 2

**Address:** `0x781229c7a798c33ec788520a6bbe12a79ed657fc`

**Chain:** Ethereum, Polygon.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda 2 (Exchange)" on this address.[^1] Polygonscan carries the same "Zonda 2" name tag on the same address (key reused unchanged across chains).[^4] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-09-01 (block 13140703); most recent 2026-04-13 (block 24869201); ≥ 10,000 events.
- ERC-20 events: first 2021-07-27 (block 12907119); most recent 2026-04-17 (block 24898630); 4,493 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2024-05-01; most recent 2026-03-24; 43 events.
- ERC-20 events (raw, including fake-token poisoning seeds): first 2021-09-10; most recent 2026-03-29; 426 events. Filtered to the canonical Polygon Tether contract (`0xc2132d05…58e8f`, current symbol `USDT0`), real-USDT activity is 64 events spanning 2024-02-06 → 2025-12-06.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $379,572,159 |
| Gross OUT (USD-equivalent at tx time) | $283,461,207 |
| Total throughput (gross in + out) | $663,033,366 |
| Net direction | +$96,110,952 |
| Total events ≥$1k | 4,090 |
| Distinct external counterparties (≥$1k cumulative) | 2,537 |
| Identified counterparties in this section | 5 internal + 0 external (Etherscan-tagged) |
| Counterparties without a public name tag | **2,537, aggregating ~$66,908,332 outbound and ~$76,014,542 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-08-31 → 2026-04-02 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $160,314,937 | $163,474,760 | 555 |
| Zonda 3 `0x0ff24158…5289` | $135,010,756 | $0 | 22 |
| Zonda 1 `0xf646cbe3…b95e` | $1,823,123 | $29,646,857 | 15 |
| Zonda 4 `0x2b645268…763a` | $2,228,043 | $22,219,874 | 10 |
| Zonda 6 `0xd388009f…8046` | $0 | $1,207,505 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 2,537 of the 2,542 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$66,908,332 outbound** and **$76,014,542 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xcae4e8c327647861ee4bb8e96041df53a7317dd9` | $17,135,129 | $42,618,988 | 2 / 8 | 2022-06-14 → 2024-05-08 |
| 2 | `0x1d365ff0dac8837ae25e1c905db44fc71881aa4f` | $0 | $17,131,082 | 0 / 3 | 2024-03-25 → 2024-06-19 |
| 3 | `0x5e393568cd2f698c1884ba6870e387b8f140c937` | $13,759,033 | $0 | 73 / 0 | 2022-01-17 → 2022-08-27 |
| 4 | `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | $4,651,423 | $0 | 33 / 0 | 2022-01-17 → 2022-08-03 |
| 5 | `0xc280ee684fc751bd01fb4e7467808ea1392fade3` | $4,468,687 | $0 | 47 / 0 | 2022-01-17 → 2022-06-28 |
| 6 | `0x29fbc8cbaa1de447ec0edc01b36fce0e5a24082b` | $4,058,982 | $0 | 7 / 0 | 2022-03-22 → 2022-03-30 |
| 7 | `0xa25b76424b676cbb48e1189926c1c8d8fc083f42` | $308,852 | $3,643,149 | 1 / 2 | 2023-10-06 → 2025-08-14 |
| 8 | `0xfc982cab43c3694fd559fe006ff3c4d73794f55c` | $3,349,254 | $0 | 55 / 0 | 2022-01-17 → 2022-09-26 |
| 9 | `0x8c55e56cf813ce34b50dfbcc86762d0fc909aa51` | $0 | $3,127,594 | 0 / 16 | 2025-03-19 → 2025-11-05 |
| 10 | `0x854d0c53986974ed3cc0c2b1d0a87193ac6fadf7` | $2,743,644 | $0 | 12 / 0 | 2022-01-20 → 2022-06-18 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Flow profile (Polygon, Dune-aggregated 2026-05-13)

Full-history aggregation built from Dune `tokens_polygon.transfers` (≥$1,000 USD-equivalent per event). See [methodology](../methodology.md#flow-profile) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $11,723,827 |
| Gross OUT (USD-equivalent at tx time) | $10,829,003 |
| Total throughput | $22,552,830 |
| Net direction | +$894,824 |
| Total events ≥$1k | 50 |
| Distinct external counterparties (≥$1k cumulative) | 1 |
| Identified counterparties in this section | 1 internal + 0 external (PolygonScan-tagged) |
| Counterparties without a public name tag | **1, aggregating ~$16,681 outbound and ~$0 inbound across captured rows** |
| Active period | 2024-04-25 → 2026-01-05 |

**Confidence:** CONFIRMED on totals. CONFIRMED on Internal and External-tagged rows below (each PolygonScan tag verified by fresh HTML fetch on 2026-05-13 saved to `case/sources/polygonscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $11,723,827 | $10,812,322 | 49 |

### Unidentified counterparties

**This section is a known incomplete part of the analysis.** 1 of the 2 Polygon counterparties with ≥$1k cumulative flow carry no PolygonScan public name tag as of 2026-05-13 and do not appear in this inventory's roster. The unidentified rows captured here aggregate **$16,681 outbound** and **$0 inbound**. Entity-attribution work on these counterparties is ongoing.

**Receipts**: `case/sources/dune/polygon-per-wallet-2026-05-13.json` (query 7491823) + `case/sources/dune/polygon-totals-2026-05-13.json` (query 7491829) + `case/sources/polygonscan-name-tags-2026-05-13/<addr>.html`.

## Block-explorer links

- Ethereum: https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
- Polygon: https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc

[^1]: Etherscan, public name tag on Zonda 2. https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
[^4]: Polygonscan, public name tag on Zonda 2. Verified by HTML fetch 2026-05-13. https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
