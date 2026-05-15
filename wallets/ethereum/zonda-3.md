# Zonda 3

> **Plain-language summary.** A ZondaCrypto exchange wallet on Ethereum, attributed by three independent primary sources (Etherscan, hildobby, BlockSec). Active 2016-04 → 2022-02 (effectively dormant after early 2022). Observed throughput is $1.13 billion across 31,091 events above $1,000 USD; the wallet has a $177.7 million net outflow over its lifetime, with $309.8 million of that outflow landing on Zonda 1 alone.

**Address:** `0x0ff24158220a14398f047a80a513617ddc4f5289`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan carries the public name tag "Zonda 3 (Exchange)" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2016-04-02 (block 1263048); most recent 2022-10-05 (block 15681057); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).
- ERC-20 events: first 2017-09-07 (block 4249673); most recent 2026-02-21 (block 24508148); 378 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
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

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 1 `0xf646cbe3…b95e` | $837,541 | $309,795,646 | 535 |
| Zonda 4 `0x2b645268…763a` | $0 | $189,202,109 | 93 |
| Zonda 2 `0x781229c7…57fc` | $0 | $134,944,128 | 21 |

### External counterparties — confirmed via public name tag
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0xaa1a6e3e…6444` | ReplaySafeSplit | $86,238 | 4 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xdc76cd25977e0a5ae17155770273ad58648900d3` | HTX 6 | $0 | $0 | 2 / 0 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 16,346 of the 16,350 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$21,329,698 outbound** and **$360,248,631 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | $51,116,423 | $0 | 88 / 0 | 2019-05-02 → 2022-01-07 |
| 2 | `0x32e04e19a63eae6fe19051fc24898ae21444f9c4` | $23,201,036 | $0 | 169 / 0 | 2018-10-30 → 2022-01-08 |
| 3 | `0x98334f075c9ac54f9236ef078fb43e24f2fc9221` | $20,455,173 | $114,839 | 11 / 1 | 2020-03-16 → 2021-04-14 |
| 4 | `0xb7cc1a4c9a23329f0ee99442a5258f85c8bc0c24` | $454 | $20,360,070 | 1 / 60 | 2017-04-27 → 2017-12-08 |
| 5 | `0xc280ee684fc751bd01fb4e7467808ea1392fade3` | $18,784,694 | $0 | 99 / 0 | 2018-07-06 → 2022-01-14 |
| 6 | `0x5e393568cd2f698c1884ba6870e387b8f140c937` | $16,577,683 | $0 | 18 / 0 | 2020-08-20 → 2022-01-08 |
| 7 | `0xa6e2aba95638ee4728ac8a3c0273b10a24dcc593` | $13,834,790 | $0 | 19 / 0 | 2018-02-06 → 2022-01-08 |
| 8 | `0x65467a249f00dcf1103c94eef7c51d3bd58dbef9` | $11,485,725 | $0 | 108 / 0 | 2018-10-30 → 2022-01-09 |
| 9 | `0x1d894c2b7b9310cf31eaa636c083a84765e0a9c2` | $8,182,121 | $0 | 21 / 0 | 2021-01-11 → 2021-12-08 |
| 10 | `0xb9dad752ed6ce59420de624d9f3a96edd52fa032` | $7,854,428 | $0 | 3 / 0 | 2021-03-02 → 2021-09-24 |

<details><summary>Show 40 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0x116402c60f094c8b0482a3e27f698963c77251b1` | $6,859,847 | $0 | 34 / 0 | 2019-04-25 → 2020-03-19 |
| 12 | `0xfc982cab43c3694fd559fe006ff3c4d73794f55c` | $5,571,540 | $0 | 69 / 0 | 2019-02-26 → 2022-01-09 |
| 13 | `0xaff0d83d0b082a995d0b531419dc23e64f9eced8` | $5,223,515 | $0 | 35 / 0 | 2018-01-10 → 2019-04-30 |
| 14 | `0x87a8be7f9c656f34244740a3765f88469d956d4c` | $4,278,240 | $0 | 911 / 0 | 2017-04-29 → 2018-01-03 |
| 15 | `0xd5cbbf63203bddd4a44c98a7dcc7cda32a290aca` | $3,419,641 | $0 | 31 / 0 | 2018-01-11 → 2022-01-11 |
| 16 | `0x2188f560517b060efcaf4e0f64ad36c76fe4b365` | $3,382,693 | $0 | 253 / 0 | 2016-06-17 → 2018-01-03 |
| 17 | `0xd72dbd90c80db3d02aacf276c4566fe88a269957` | $3,195,869 | $0 | 2 / 0 | 2018-01-11 → 2018-02-06 |
| 18 | `0xbb36fa0e822f7ab08ae8c39599af4157d75c5b73` | $3,062,075 | $0 | 61 / 0 | 2019-01-07 → 2022-01-06 |
| 19 | `0x171fec0f88fd03043baf09b27dacab3ab12c174f` | $3,040,181 | $0 | 48 / 0 | 2018-02-06 → 2021-12-14 |
| 20 | `0x7195c9df9cf0ec76832661900663054b973f0bb0` | $3,033,574 | $0 | 24 / 0 | 2018-01-11 → 2021-09-12 |
| 21 | `0x9e8a3f1a5e26aba7fa2991499cd81c17dbe2d587` | $3,001,174 | $0 | 3 / 0 | 2018-02-06 → 2018-07-06 |
| 22 | `0x854d0c53986974ed3cc0c2b1d0a87193ac6fadf7` | $2,834,540 | $0 | 7 / 0 | 2021-12-08 → 2022-01-06 |
| 23 | `0x6823b226885e989df89caa29d391edb1898f36c1` | $2,751,685 | $0 | 13 / 0 | 2019-06-12 → 2021-09-25 |
| 24 | `0xd9d2897f9c55a8b856b707096e8005d62ba2d067` | $2,721,907 | $0 | 1 / 0 | 2021-10-14 → 2021-10-14 |
| 25 | `0xaed7606fdf68b58eed5075a0de69b678e943100f` | $2,264,554 | $0 | 2 / 0 | 2021-04-09 → 2021-06-16 |
| 26 | `0x24c15c7a1c1acd479dc3b388c1fb85a26ef457c8` | $2,177,508 | $0 | 37 / 0 | 2018-02-06 → 2021-03-02 |
| 27 | `0x20fc46a61a656aa4fdc9c420b1b7f15e488159c5` | $2,147,784 | $0 | 25 / 0 | 2018-09-24 → 2021-12-08 |
| 28 | `0x82b89c806f91e25aebf1705346e93ed3c2ea96ca` | $2,065,633 | $0 | 5 / 0 | 2018-02-07 → 2018-10-30 |
| 29 | `0x88440b9e7ed400ac83e9784c3aa408b83a962f3c` | $2,022,808 | $0 | 48 / 0 | 2018-09-24 → 2019-08-12 |
| 30 | `0x025f494bf966812e697b5a4d92178c681a30a396` | $1,988,032 | $0 | 2 / 0 | 2021-03-02 → 2021-06-16 |
| 31 | `0xbcaa734b70441f8b78626962fb2b68d37ab85355` | $1,897,056 | $0 | 64 / 0 | 2018-01-11 → 2022-01-09 |
| 32 | `0xf2e274950138ac07e29ebd877f3ddff0556abe64` | $1,863,791 | $0 | 41 / 0 | 2020-09-07 → 2021-12-29 |
| 33 | `0xc46d4952673664b6ae335f9d6cf5dc52dbcc42f1` | $1,837,388 | $0 | 2 / 0 | 2018-01-09 → 2018-01-11 |
| 34 | `0x9cb1bcf9ecfeaf8f47ef23e7fe6c272682c46252` | $1,774,295 | $0 | 6 / 0 | 2018-02-07 → 2019-01-07 |
| 35 | `0xa99d00ed83c98d1186b6daa307cf7f651ff7a021` | $1,747,388 | $0 | 38 / 0 | 2021-04-25 → 2022-01-07 |
| 36 | `0x0861c4e2b5d45a5499c34e9caf84df242dc076b2` | $1,608,355 | $0 | 4 / 0 | 2018-01-10 → 2021-06-16 |
| 37 | `0x213d3511ff8b85663fa66b0a122597adf4febe85` | $1,563,434 | $0 | 168 / 0 | 2018-10-29 → 2022-01-05 |
| 38 | `0xaf50bc71f6b1a8781a0cfa491043a262a18de0fc` | $1,520,149 | $0 | 107 / 0 | 2017-06-08 → 2018-01-03 |
| 39 | `0x7ed2aefe83a720608126f65de162bf3edec6d8b6` | $1,464,593 | $0 | 22 / 0 | 2019-09-23 → 2021-04-04 |
| 40 | `0xd34dfa5e04bb4c276f4b3bd43bc8b1f6199b7f64` | $1,391,894 | $0 | 62 / 0 | 2017-06-06 → 2018-01-03 |
| 41 | `0x4c8384f5196cf0d3f090286c66378b416acf871e` | $1,383,997 | $0 | 6 / 0 | 2019-05-13 → 2019-06-27 |
| 42 | `0xbcb1f502ea43936b9096ed322cd57dcc1620287b` | $1,363,870 | $0 | 178 / 0 | 2016-05-27 → 2018-01-03 |
| 43 | `0xc52535bcbd06f7ff0a2be48880fdf1ece503d66b` | $1,333,002 | $0 | 6 / 0 | 2020-08-02 → 2021-12-29 |
| 44 | `0x9bb9768aa06abc0943cbcb54e5e6de085813ec0e` | $1,292,866 | $0 | 32 / 0 | 2018-01-10 → 2021-12-21 |
| 45 | `0x10b487935db01346af242263808f099b3f742fdc` | $1,226,318 | $0 | 13 / 0 | 2019-10-25 → 2021-01-11 |
| 46 | `0x21ff9986b2f82266706cfa6ebac517fbcb5462ab` | $1,211,009 | $0 | 42 / 0 | 2018-01-10 → 2021-06-16 |
| 47 | `0xc95101d7636c52c34a96865ffc4d3967629b90a7` | $1,163,268 | $0 | 10 / 0 | 2018-02-07 → 2021-12-08 |
| 48 | `0xebf4fc31f55238c980116d40acb74cd63b65fd48` | $1,144,579 | $0 | 1 / 0 | 2021-04-04 → 2021-04-04 |
| 49 | `0xd2ad546da83e6225c53d5fba1795a2a36dab9a59` | $1,093,361 | $0 | 3 / 0 | 2018-02-06 → 2018-07-06 |
| 50 | `0x1e1d6bc2afe39a5ecd3ce675c32d26604f78e912` | $1,027,352 | $0 | 2 / 0 | 2018-04-06 → 2021-10-14 |

</details>
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-3-counterparties.csv`](zonda-3-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x0ff24158220a14398f047a80a513617ddc4f5289

[^1]: Etherscan, public name tag on Zonda 3. https://etherscan.io/address/0x0ff24158220a14398f047a80a513617ddc4f5289
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
