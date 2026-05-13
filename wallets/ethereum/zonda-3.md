# Zonda 3

**Address:** `0x0ff24158220a14398f047a80a513617ddc4f5289`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda 3 (Exchange)" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2016-04-02 (block 1263048); most recent 2022-10-05 (block 15681057); ≥ 10,000 events.
- ERC-20 events: first 2017-09-07 (block 4249673); most recent 2026-02-21 (block 24508148); 378 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $478,308,976 |
| Gross OUT (USD-equivalent at tx time) | $656,000,188 |
| Total throughput (gross in + out) | $1,134,309,164 |
| Net direction | −$177,691,212 |
| Total events ≥$1k | 31,091 |
| Distinct external counterparties (≥$1k cumulative) | 16,347 |
| Identified counterparties in this section | 3 internal + 1 external (Etherscan-tagged) |
| Counterparties without a public name tag | **16,346, aggregating ~$21,329,698 outbound and ~$360,248,631 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2016-04-02 → 2022-02-28 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 1 `0xf646cbe3…b95e` | $837,541 | $309,795,646 | 535 |
| Zonda 4 `0x2b645268…763a` | $0 | $189,202,109 | 93 |
| Zonda 2 `0x781229c7…57fc` | $0 | $134,944,128 | 21 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0xaa1a6e3e…6444` | ReplaySafeSplit | $86,238 | 4 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 16,346 of the 16,350 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$21,329,698 outbound** and **$360,248,631 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | $51,116,408 | $0 | 87 / 0 | 2019-05-02 → 2022-01-07 |
| 2 | `0x32e04e19a63eae6fe19051fc24898ae21444f9c4` | $23,199,324 | $0 | 167 / 0 | 2018-10-30 → 2022-01-08 |
| 3 | `0x98334f075c9ac54f9236ef078fb43e24f2fc9221` | $20,412,906 | $114,839 | 8 / 1 | 2020-03-16 → 2021-04-14 |
| 4 | `0xb7cc1a4c9a23329f0ee99442a5258f85c8bc0c24` | $0 | $20,359,364 | 0 / 58 | 2017-04-28 → 2017-12-05 |
| 5 | `0xc280ee684fc751bd01fb4e7467808ea1392fade3` | $18,784,694 | $0 | 99 / 0 | 2018-07-06 → 2022-01-14 |
| 6 | `0x5e393568cd2f698c1884ba6870e387b8f140c937` | $16,577,683 | $0 | 18 / 0 | 2020-08-20 → 2022-01-08 |
| 7 | `0xa6e2aba95638ee4728ac8a3c0273b10a24dcc593` | $13,834,790 | $0 | 19 / 0 | 2018-02-06 → 2022-01-08 |
| 8 | `0x65467a249f00dcf1103c94eef7c51d3bd58dbef9` | $11,485,725 | $0 | 108 / 0 | 2018-10-30 → 2022-01-09 |
| 9 | `0x1d894c2b7b9310cf31eaa636c083a84765e0a9c2` | $8,182,121 | $0 | 20 / 0 | 2021-01-11 → 2021-12-08 |
| 10 | `0xb9dad752ed6ce59420de624d9f3a96edd52fa032` | $7,854,428 | $0 | 3 / 0 | 2021-03-02 → 2021-09-24 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x0ff24158220a14398f047a80a513617ddc4f5289

[^1]: Etherscan, public name tag on Zonda 3. https://etherscan.io/address/0x0ff24158220a14398f047a80a513617ddc4f5289
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
