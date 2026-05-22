# Zonda 2

> **Plain-language summary.** A ZondaCrypto exchange wallet using the same key on Ethereum and Polygon, attributed by four independent primary sources (Etherscan, PolygonScan, hildobby, BlockSec). Active since 2021. Observed Ethereum throughput is $663.0 million across 4,090 events above $1,000 USD with $96.1 million net inflow; Polygon activity is materially smaller (see the Polygon flow profile section below).

**Address:** `0x781229c7a798c33ec788520a6bbe12a79ed657fc`

**Chain:** Ethereum, Polygon.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan carries the public name tag "Zonda 2 (Exchange)" on this address.[^1] Polygonscan carries the same "Zonda 2" name tag on the same address (key reused unchanged across chains).[^4] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-09-01 (block 13140703); most recent 2026-04-13 (block 24869201); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).
- ERC-20 events: first 2021-07-27 (block 12907119); most recent 2026-04-17 (block 24898630); 4,493 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2024-05-01; most recent 2026-03-24; 43 events.
- ERC-20 events (raw, including fake-token poisoning seeds): first 2021-09-10; most recent 2026-03-29; 426 events. Filtered to the canonical Polygon Tether contract (`0xc2132d05…58e8f`, current symbol `USDT0`), real-USDT activity is 64 events spanning 2024-02-06 → 2025-12-06.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
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

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $160,314,937 | $163,474,760 | 555 |
| Zonda 3 `0x0ff24158…5289` | $135,010,756 | $0 | 22 |
| Zonda 1 `0xf646cbe3…b95e` | $1,823,123 | $29,646,857 | 15 |
| Zonda 4 `0x2b645268…763a` | $2,228,043 | $22,219,874 | 10 |
| Zonda 6 `0xd388009f…8046` | $0 | $1,207,505 | 1 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 2,537 of the 2,542 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$66,908,332 outbound** and **$76,014,542 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xcae4e8c327647861ee4bb8e96041df53a7317dd9` | $17,135,129 | $42,619,000 | 2 / 16 | 2022-06-14 → 2024-05-08 |
| 2 | `0x1d365ff0dac8837ae25e1c905db44fc71881aa4f` | $0 | $17,131,086 | 0 / 4 | 2024-03-25 → 2024-06-19 |
| 3 | `0x5e393568cd2f698c1884ba6870e387b8f140c937` | $13,759,033 | $0 | 73 / 0 | 2022-01-17 → 2022-08-27 |
| 4 | `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | $4,652,681 | $0 | 48 / 0 | 2022-01-17 → 2022-08-03 |
| 5 | `0xc280ee684fc751bd01fb4e7467808ea1392fade3` | $4,468,687 | $0 | 47 / 0 | 2022-01-17 → 2022-06-28 |
| 6 | `0x29fbc8cbaa1de447ec0edc01b36fce0e5a24082b` | $4,058,982 | $0 | 8 / 0 | 2022-03-22 → 2022-03-30 |
| 7 | `0xa25b76424b676cbb48e1189926c1c8d8fc083f42` | $308,852 | $3,643,149 | 1 / 2 | 2023-10-06 → 2025-08-14 |
| 8 | `0xfc982cab43c3694fd559fe006ff3c4d73794f55c` | $3,349,254 | $0 | 55 / 0 | 2022-01-17 → 2022-09-26 |
| 9 | `0x8c55e56cf813ce34b50dfbcc86762d0fc909aa51` | $0 | $3,127,594 | 0 / 17 | 2025-03-19 → 2025-11-05 |
| 10 | `0x854d0c53986974ed3cc0c2b1d0a87193ac6fadf7` | $2,743,644 | $0 | 12 / 0 | 2022-01-20 → 2022-06-18 |

<details><summary>Show 40 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0xa99d00ed83c98d1186b6daa307cf7f651ff7a021` | $2,064,082 | $0 | 62 / 0 | 2022-01-17 → 2022-07-29 |
| 12 | `0xa6e2aba95638ee4728ac8a3c0273b10a24dcc593` | $1,750,010 | $0 | 12 / 0 | 2022-01-20 → 2022-11-11 |
| 13 | `0x32e04e19a63eae6fe19051fc24898ae21444f9c4` | $1,283,456 | $0 | 64 / 0 | 2022-01-17 → 2022-07-20 |
| 14 | `0xbb36fa0e822f7ab08ae8c39599af4157d75c5b73` | $1,044,585 | $0 | 32 / 0 | 2022-01-21 → 2022-07-18 |
| 15 | `0x65467a249f00dcf1103c94eef7c51d3bd58dbef9` | $1,033,125 | $0 | 31 / 0 | 2022-01-17 → 2022-08-27 |
| 16 | `0x25c2f0e18f8945f5395aa971c99e95f808e79dea` | $857,873 | $0 | 3 / 0 | 2022-03-31 → 2022-03-31 |
| 17 | `0x1d894c2b7b9310cf31eaa636c083a84765e0a9c2` | $804,994 | $0 | 4 / 0 | 2022-01-17 → 2022-03-31 |
| 18 | `0x5ce847d94c36e69b2ed20a680ab797d0b95297bc` | $753,054 | $0 | 4 / 0 | 2022-05-04 → 2022-07-13 |
| 19 | `0x72d2db692826fb76053fb800988cc0ff125b4748` | $693,066 | $0 | 4 / 0 | 2022-05-06 → 2022-07-21 |
| 20 | `0x86ff424b20a8199c169752b7f980b935f7a4fc81` | $675,417 | $0 | 85 / 0 | 2022-03-01 → 2022-08-04 |
| 21 | `0xa9651b94bdf0abd9f9870c9a2f56bc2c6efb529f` | $590,595 | $0 | 20 / 0 | 2022-02-06 → 2022-10-08 |
| 22 | `0x5c07d65f14e42a48e600338fcca54596e6097e75` | $398,250 | $0 | 6 / 0 | 2022-02-11 → 2022-05-12 |
| 23 | `0x1990abd6e49218ab403f01aefeb9d22d07244181` | $0 | $387,529 | 0 / 4 | 2024-06-19 → 2025-12-03 |
| 24 | `0x115aaab70238e26b3ec2eea6f7f53c34be5e60b8` | $381,361 | $0 | 3 / 0 | 2022-03-07 → 2022-07-19 |
| 25 | `0xeeaa2e90e3f7c2653c4411285e8d2e5399993beb` | $365,181 | $0 | 3 / 0 | 2022-05-31 → 2022-05-31 |
| 26 | `0xbb6d14c4befd49b1a59020d52688ef71c9cd5e1f` | $351,481 | $0 | 1 / 0 | 2022-01-20 → 2022-01-20 |
| 27 | `0x097511b9af934c6acb44ba110c24783f57fb4cbb` | $307,222 | $0 | 16 / 0 | 2024-01-10 → 2024-01-12 |
| 28 | `0x82dd71713e12387bb3d8685f37a021ef1cdd7a8d` | $292,303 | $0 | 5 / 0 | 2022-02-01 → 2022-03-05 |
| 29 | `0xbcaa734b70441f8b78626962fb2b68d37ab85355` | $214,280 | $0 | 8 / 0 | 2022-01-17 → 2023-03-01 |
| 30 | `0x213d3511ff8b85663fa66b0a122597adf4febe85` | $180,380 | $0 | 39 / 0 | 2022-01-17 → 2022-09-13 |
| 31 | `0xeb258c0af51fd182e5ae23973679e789a68657a3` | $179,384 | $0 | 3 / 0 | 2022-03-07 → 2022-04-08 |
| 32 | `0xf2e274950138ac07e29ebd877f3ddff0556abe64` | $167,771 | $0 | 5 / 0 | 2022-01-17 → 2022-03-19 |
| 33 | `0x5e961d8bf87d3835d1af4bda4f521832e5b5c09a` | $145,323 | $0 | 2 / 0 | 2022-01-28 → 2022-04-15 |
| 34 | `0x30a646300bc581a65cfcfd9939478807f5200600` | $130,700 | $0 | 3 / 0 | 2022-01-28 → 2022-03-09 |
| 35 | `0xac0dcb804f341132e81d96af7278fdd6ce886e7f` | $130,250 | $0 | 1 / 0 | 2022-04-13 → 2022-04-13 |
| 36 | `0xfe264c7f496d7d4bac60905ad03dc21400eade52` | $120,561 | $0 | 13 / 0 | 2022-02-02 → 2022-06-21 |
| 37 | `0xb30ad58a09052e17427ba00c007c7a44402426b6` | $118,767 | $0 | 1 / 0 | 2022-05-27 → 2022-05-27 |
| 38 | `0x5703b3cb982fa82efcfb64f0e2c9048640abad40` | $117,255 | $0 | 2 / 0 | 2022-03-02 → 2022-03-03 |
| 39 | `0xde3119c73aed55623b537604cf3842dc35bb9ce3` | $116,357 | $0 | 4 / 0 | 2022-03-01 → 2022-07-21 |
| 40 | `0xb3a6b7c22a9c4619e4baebc1a9682672160cc332` | $113,762 | $0 | 180 / 0 | 2022-01-17 → 2022-07-24 |
| 41 | `0xc853da7590fceb7d098ad68f6359f1b75abfef47` | $111,606 | $0 | 10 / 0 | 2022-01-28 → 2022-05-03 |
| 42 | `0x46a00e0a982c1c6168c2f0feca8c9760b1f9455f` | $108,167 | $0 | 5 / 0 | 2022-01-31 → 2022-04-29 |
| 43 | `0xbfd8d26b0049cd62612168623a5173f862a2836f` | $104,119 | $0 | 1 / 0 | 2022-04-06 → 2022-04-06 |
| 44 | `0x5705abf3017ae6698800a156eb8a696f064ba036` | $95,923 | $0 | 36 / 0 | 2022-01-17 → 2022-07-04 |
| 45 | `0xe50eaa02477673565f0fa09367b4cf14008c53d0` | $93,233 | $0 | 4 / 0 | 2022-05-27 → 2022-07-20 |
| 46 | `0xd5cbbf63203bddd4a44c98a7dcc7cda32a290aca` | $92,583 | $0 | 4 / 0 | 2022-01-20 → 2023-03-01 |
| 47 | `0x9385aa6ce34647cf3532842b4e9565fd3431a68d` | $89,087 | $0 | 63 / 0 | 2022-01-17 → 2022-05-16 |
| 48 | `0xe8a464e26fa8ba6de27a246024bc1a7d5bf997d7` | $88,420 | $0 | 101 / 0 | 2022-01-17 → 2022-05-06 |
| 49 | `0x92e9f65c2b5738416773c1fb9070b07174aba63e` | $85,615 | $0 | 5 / 0 | 2022-03-18 → 2023-03-01 |
| 50 | `0x227341e7b5aa1ba3aea0907a7c401e0b6c8c602c` | $85,059 | $0 | 3 / 0 | 2022-01-28 → 2022-04-28 |

</details>
## Flow profile (Polygon, Dune-aggregated 2026-05-13)

Full-history aggregation built from Dune `tokens_polygon.transfers` (≥$1,000 USD-equivalent per event). See [methodology](../../methodology.md#flow-profiles) for the SQL.

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

**Confidence:** CONFIRMED on totals. CONFIRMED on Internal and External-tagged rows below (each PolygonScan tag verified by fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $11,723,827 | $10,812,322 | 49 |

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** 1 of the 2 Polygon counterparties with ≥$1k cumulative flow carry no PolygonScan public name tag as of 2026-05-13 and do not appear in this inventory's roster. The unidentified rows captured here aggregate **$16,681 outbound** and **$0 inbound**. Entity-attribution work on these counterparties is ongoing.

**Receipts**: `../../sources/dune/polygon-per-wallet-2026-05-13.json` (query 7491823) + `../../sources/dune/polygon-totals-2026-05-13.json` (query 7491829) (PolygonScan public-name-tag HTML batch retained in the working archive; see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)).

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-2-counterparties.csv`](zonda-2-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

Polygon counterparties are published separately: [`zonda-2-counterparties-polygon.csv`](zonda-2-counterparties-polygon.csv).

## Block-explorer links

- Ethereum: https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
- Polygon: https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc

[^1]: Etherscan, public name tag on Zonda 2. https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
[^4]: Polygonscan, public name tag on Zonda 2. Verified by HTML fetch 2026-05-13. https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x267be1c1d684f78cb4f6a176c4911b741e4ffdc0` | Kraken 4 | $18 | $0 | 1 / 0 |
| `0x89e51fa8ca5d66cd220baed62ed01e8951aa7c40` | Kraken 7 | $7 | $0 | 1 / 0 |
| `0x46340b20830761efd32832a74d7169b29feb9758` | Crypto.com 2 | $0 | $0 | 1 / 0 |

