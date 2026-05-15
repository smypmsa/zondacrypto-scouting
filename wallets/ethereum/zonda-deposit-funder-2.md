# Zonda Deposit Funder 2

**Address:** `0x818ab3c61f66e975b8e6290c20999d6749f60d8d`

**Chain:** Ethereum.

**Role:** ZondaCrypto deposit-funder / gas-supplier wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda: Deposit Funder 2" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses on Dune Analytics (entry added 2024-10-06 as "Zonda Gas Supplier 2").[^2] The receipt of the Dune query result is preserved at [`sources/dune/hildobby-3237025-zonda-rows.json`](../../sources/dune/hildobby-3237025-zonda-rows.json).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-12 (block 12223728); most recent 2023-11-06 (block 18515362); ≥ 10,000 events.
- ERC-20 events: first 2021-09-11 (block 13205595); most recent 2023-10-19 (block 18383438); 15 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $401,221 |
| Gross OUT (USD-equivalent at tx time) | $0 |
| Total throughput (gross in + out) | $401,221 |
| Net direction | +$401,221 |
| Total events ≥$1k | 32 |
| Distinct external counterparties (≥$1k cumulative) | 11 |
| Identified counterparties in this section | 3 internal + 0 external (Etherscan-tagged) |
| Counterparties without a public name tag | **11, aggregating ~$0 outbound and ~$0 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-04-12 → 2023-10-19 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $228,347 | $0 | 22 |
| Zonda 1 `0xf646cbe3…b95e` | $99,267 | $0 | 6 |
| Zonda 4 `0x2b645268…763a` | $73,606 | $0 | 4 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 11 of the 14 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `../../sources/dune/inventory-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `../../sources/dune/inventory-per-wallet-totals-2026-05-13.json` (query 7491746) and `../../sources/dune/inventory-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag fetches (2026-05-13, browser-style User-Agent, ~0.8s pacing) retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility).


### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x47ef949598e02b90ae2a38624f07b77c18fabb8b` | $0 | $7,494 | 0 / 254 | 2021-04-12 → 2023-10-20 |
| 2 | `0x73bfc8b17296cb284b7b116e519c7b84df4e4020` | $0 | $4,026 | 0 / 164 | 2021-04-15 → 2023-10-20 |
| 3 | `0x4b039efd60f4aa2106c6fe4e718b346111ac5cd4` | $0 | $3,798 | 0 / 119 | 2021-04-12 → 2022-07-26 |
| 4 | `0xcee4dfde1ce0260afb87f8c917726ab0502fd457` | $0 | $3,487 | 0 / 117 | 2021-04-23 → 2022-11-13 |
| 5 | `0x4fc05911251b5bc1dbddb4788c92c19ccf67c8d2` | $0 | $2,362 | 0 / 101 | 2021-09-11 → 2023-10-24 |
| 6 | `0xf9d6b16bbf23cedc08846482d8cc5901b6b5d50c` | $0 | $1,613 | 0 / 57 | 2021-04-13 → 2022-11-08 |
| 7 | `0x4b209e06a2eb8c718a5dda726e4f6395769c7b8e` | $0 | $1,460 | 0 / 64 | 2021-07-05 → 2023-07-20 |
| 8 | `0x03ff8a841a5ffae262da6e07e82d208a663275e4` | $0 | $1,235 | 0 / 37 | 2021-05-17 → 2022-01-25 |
| 9 | `0xd3b1ca9dfbb4acf1669c60bd8587122144295b73` | $0 | $1,113 | 0 / 50 | 2021-11-14 → 2023-05-12 |
| 10 | `0x6b605df8c0d2d435717383c85b474eb90bf7516d` | $0 | $1,068 | 0 / 49 | 2021-04-15 → 2022-10-24 |
| 11 | `0x7f1ad55c17e86170fe7ceced8c02da5ef38cf0d3` | $0 | $769 | 0 / 22 | 2021-04-15 → 2022-01-17 |
| 12 | `0xc03502b3db745a045804e7f3a64d5133b7f34157` | $0 | $768 | 0 / 27 | 2021-04-15 → 2021-12-15 |
| 13 | `0xa370d3a30a125bb025501bf256eb6eab23d54c98` | $0 | $767 | 0 / 35 | 2022-08-25 → 2023-10-24 |
| 14 | `0x36f217d70c84c7362b82d8ef866cc8ffbd020fd1` | $0 | $649 | 0 / 31 | 2022-02-16 → 2023-10-23 |
| 15 | `0x5dfd711dce615bca6b956537facdd1467aabb58e` | $0 | $465 | 0 / 17 | 2021-04-15 → 2021-11-06 |
| 16 | `0xeb8401f96c65ca4686049b19dd9dcfc773cd1ad0` | $0 | $311 | 0 / 11 | 2021-04-15 → 2022-01-17 |
| 17 | `0xbd5bcb978dca370c03fb5f827e17cf16537121db` | $0 | $300 | 0 / 11 | 2021-04-15 → 2022-10-29 |
| 18 | `0xd42235190e0c2649bcf0c5109014768655a76b78` | $0 | $283 | 0 / 10 | 2021-04-18 → 2022-11-09 |
| 19 | `0xcee2aeec7b1cce085a086063a4b2a7e8bfe63bdb` | $0 | $270 | 0 / 6 | 2021-05-03 → 2021-11-08 |
| 20 | `0xc1cb9303284c6431a9c9efef3fe026514e65ec54` | $0 | $268 | 0 / 13 | 2022-02-23 → 2022-06-10 |
| 21 | `0xd0c0c06d01df226de1d50e8de7016497d34eb718` | $0 | $252 | 0 / 9 | 2021-07-13 → 2022-04-20 |
| 22 | `0xb03850dddcd8c594be41ef66daf21b385ad44953` | $0 | $228 | 0 / 8 | 2021-04-13 → 2022-04-25 |
| 23 | `0x3a15aa46fc095c416a2ac5e969fc19a89749de81` | $0 | $224 | 0 / 10 | 2021-08-13 → 2023-05-23 |
| 24 | `0x20b5eeb4c6da6f07118e2176ab06aa76526ddfd9` | $0 | $209 | 0 / 2 | 2021-04-13 → 2021-04-13 |
| 25 | `0x64dc71dd8dae8728216626c7af3a5831cf165243` | $0 | $209 | 0 / 7 | 2021-09-20 → 2021-11-22 |
| 26 | `0x0267a812b917002260cfc292eaf79b95c9a0e9ce` | $0 | $197 | 0 / 4 | 2021-04-16 → 2021-12-25 |
| 27 | `0xc38f25b642dbe99c7183cbb5bec441d8cbb14c67` | $0 | $194 | 0 / 8 | 2022-02-23 → 2022-10-26 |
| 28 | `0xb757efa032bc27329a66a09bdf515e5a8c0b9b63` | $0 | $191 | 0 / 6 | 2021-10-09 → 2022-01-17 |
| 29 | `0x78acabd169dbb6788cb83acbb7fa27ef84eaf268` | $0 | $191 | 0 / 9 | 2022-02-02 → 2022-05-01 |
| 30 | `0x413f54b9308f35e1ae954a111acd059b9083d6b8` | $0 | $186 | 0 / 9 | 2022-11-02 → 2023-05-16 |
| 31 | `0xa4967f4eb2234acdbba7434b2126970da83efad4` | $0 | $180 | 0 / 8 | 2022-01-08 → 2023-03-18 |
| 32 | `0x94011fd98e0831b57c0a21f9f428c1a22847e5e9` | $0 | $179 | 0 / 7 | 2021-04-15 → 2022-11-12 |
| 33 | `0x4d7e8d2d0527421a0549c3c04f1a75195f1247be` | $0 | $172 | 0 / 9 | 2022-11-18 → 2023-08-29 |
| 34 | `0x9d900884318167cba816b8d9aeb43045b58cc271` | $0 | $163 | 0 / 8 | 2021-07-05 → 2021-11-30 |
| 35 | `0x3a65c64ebb4883694948bc848a2c2664dcdc343f` | $0 | $160 | 0 / 6 | 2021-07-18 → 2022-03-29 |
| 36 | `0x5202e7920c3e3c023659e79cc9916684141537d3` | $0 | $157 | 0 / 3 | 2022-04-02 → 2022-04-02 |
| 37 | `0x02ce235fb60217d2c5402115eb5570858bb4de0f` | $0 | $155 | 0 / 4 | 2021-10-26 → 2021-12-27 |
| 38 | `0x31a3974e9598f0c935aa4aac6654ef48409876c8` | $0 | $153 | 0 / 6 | 2022-03-31 → 2023-07-26 |
| 39 | `0x2d4e808355d619e5bff99c847441d00b7bbcce6a` | $0 | $148 | 0 / 3 | 2022-04-10 → 2022-04-10 |
| 40 | `0x9c15a9243c28bcfe39430588e022afdc72275e98` | $0 | $147 | 0 / 3 | 2022-04-01 → 2022-04-01 |
| 41 | `0xf02bd4b0365dfd3a8647425ca452c7e5be47776c` | $0 | $145 | 0 / 3 | 2022-04-07 → 2022-04-07 |
| 42 | `0xb9f0a8a177162cc5d6e8633de3c880ac714873f0` | $0 | $143 | 0 / 2 | 2021-05-30 → 2021-05-30 |
| 43 | `0x706e3dc6c540f181b527c1562215da3e204ce970` | $0 | $140 | 0 / 2 | 2021-04-15 → 2021-04-16 |
| 44 | `0xeed3b5bb18c81d0dcbc9404b60b016c77e61b555` | $0 | $140 | 0 / 5 | 2022-03-30 → 2023-04-25 |
| 45 | `0x6d337db4f1b03c7edd9451b2891e5210b1f0b55d` | $0 | $136 | 0 / 2 | 2021-11-06 → 2021-11-07 |
| 46 | `0x0a18ec82515053e9b86b503c31277e13b8b6718c` | $0 | $136 | 0 / 2 | 2021-11-06 → 2021-11-07 |
| 47 | `0x7da3a1a0b3bff1049d1da72cdafe253227cfd013` | $0 | $136 | 0 / 2 | 2021-11-06 → 2021-11-07 |
| 48 | `0x10a4b3bf0ef902f319771c9864e4e4cb2ebc2f9b` | $0 | $136 | 0 / 5 | 2021-10-26 → 2022-11-10 |
| 49 | `0xbe466d64dc8ff7b8b962a5c5646a7685ad4aa296` | $0 | $136 | 0 / 2 | 2021-11-06 → 2021-11-07 |
| 50 | `0xa5016bf64a49dc7eb412a83c09a87b107dd83f1b` | $0 | $136 | 0 / 2 | 2021-04-15 → 2021-04-16 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-deposit-funder-2-counterparties.csv`](zonda-deposit-funder-2-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x818ab3c61f66e975b8e6290c20999d6749f60d8d

[^1]: Etherscan, public name tag "Zonda: Deposit Funder 2". https://etherscan.io/address/0x818ab3c61f66e975b8e6290c20999d6749f60d8d
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda Gas Supplier 2"`, `added_date="2024-10-06"`. https://dune.com/queries/3237025

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x89e51fa8ca5d66cd220baed62ed01e8951aa7c40` | Kraken 7 | $0 | $0 | 1 / 0 |

