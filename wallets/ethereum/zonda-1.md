# Zonda 1

**Address:** `0xf646cbe3b030fb6c2569215f0117dba58badb95e`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda 1 (Exchange)" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2017-12-11 (block 4714328); most recent 2026-03-24 (block 24727471); ≥ 10,000 events.
- ERC-20 events: first 2017-12-20 (block 4766539); most recent 2026-04-04 (block 24807555); 176 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $359,459,604 |
| Gross OUT (USD-equivalent at tx time) | $335,166,159 |
| Total throughput (gross in + out) | $694,625,763 |
| Net direction | +$24,293,444 |
| Total events ≥$1k | 42,818 |
| Distinct external counterparties (≥$1k cumulative) | 27,856 |
| Identified counterparties in this section | 4 internal + 6 external (Etherscan-tagged) |
| Counterparties without a public name tag | **27,850, aggregating ~$144,689,346 outbound and ~$13,595,114 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2017-12-11 → 2026-03-24 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 3 `0x0ff24158…5289` | $309,795,646 | $837,541 | 535 |
| Zonda 2 `0x781229c7…57fc` | $29,646,857 | $1,823,123 | 15 |
| Zonda 5 `0x6edf968d…5048` | $0 | $238,151 | 1 |
| Zonda Deposit Funder 2 `0x818ab3c6…0d8d` | $0 | $99,267 | 6 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x2f9378d5…2aa5` | Binance Deposit: 0x2F9378D573b20199105bCaF6D103Ac88d5442aA5 | $22,236,711 | 157 |
| `0x22b8cc8c…3529` | Binance Deposit: 0x22b8cc8Cf448b7ED9f5ac1eE0446508461493529 | $15,977,154 | 1,507 |
| `0x088ae43b…b519` | Binance Deposit: 0x088Ae43BE934bA729d8D841b41649c4d417bb519 | $3,861,830 | 146 |
| `0x8a63afd3…25b5` | Binance Deposit: 0x8a63AFd33e0d05274B3B6650486D9960785025B5 | $2,868,427 | 96 |
| `0x6543be9d…0fec` | Binance Deposit: 0x6543be9D12b48b7d72E26D1C0595fB88C4840fEC | $2,646,116 | 42 |
| `0x64b4a124…e342` | Binance Deposit: 0x64B4a124032D48e4Fb1499da1FE1412AA771e342 | $2,069,514 | 43 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x3caec6f54993526c9e2744a4fa54a19b90a3bd87` | EXMO 11 | $0 | $2,993 | 0 / 1 |
| `0x98db3a41bf8bf4ded2c92a84ec0705689ddeef8b` | Ramp Network UK 1 | $0 | $1,756 | 0 / 2 |
| `0x42d17b7f3532ec2f7c4e4e5e239baa476846e2cd` | Kanga Exchange 1 | $1,257 | $0 | 1 / 0 |
| `0xfbb1b73c4f0bda4f67dca266ce6ef42f520fbb98` | Bittrex 1 | $0 | $633 | 0 / 1 |
| `0xc88f7666330b4b511358b7742dc2a3234710e7b1` | Blockchain.com 2 | $0 | $234 | 0 / 2 |
| `0x32be343b94f860124dc4fee278fdcbd38c102d88` | Poloniex | $0 | $75 | 0 / 1 |
| `0x876eabf441b2ee5b5b0554fd502a8e0600950cfa` | Bitfinex 3 | $0 | $18 | 0 / 1 |
| `0x3cd751e6b0078be393132286c442345e5dc49699` | Coinbase 4 | $14 | $0 | 1 / 0 |
| `0x0681d8db095565fe8a346fa0277bffde9c0edbbf` | Binance 4 | $11 | $0 | 2 / 0 |
| `0xdc76cd25977e0a5ae17155770273ad58648900d3` | HTX 6 | $0 | $0 | 1 / 0 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 27,850 of the 27,860 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$144,689,346 outbound** and **$13,595,114 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x68ed0dcde71fc3b45d7f8cb84946328b49ee1746` | $0 | $7,226,754 | 0 / 5 | 2020-07-23 → 2021-08-31 |
| 2 | `0xa5ed22920276dfd6fc3bb25b889f59a620ad23e8` | $0 | $5,924,325 | 0 / 63 | 2018-02-02 → 2022-03-29 |
| 3 | `0x0ca1e75f88a1ad6ec5b0b4c92cf135179b2fa107` | $0 | $5,232,272 | 0 / 87 | 2019-02-11 → 2021-12-07 |
| 4 | `0x944da046783f24b6fe6013da23c46e5d1806f0e6` | $0 | $4,704,915 | 0 / 6 | 2017-12-13 → 2018-04-20 |
| 5 | `0x65c349fa4e1c64115c30e731e5e1c29b7c822690` | $0 | $4,566,755 | 0 / 29 | 2021-12-08 → 2022-07-07 |
| 6 | `0xb7db2f3f14726ee4013fc52fe81e6f168acb8fa5` | $0 | $4,304,246 | 0 / 3 | 2021-10-07 → 2022-07-17 |
| 7 | `0x7532e70ad7b53c27e2f5b569f671785a2e5efdc8` | $0 | $4,028,204 | 0 / 3 | 2021-01-09 → 2021-02-23 |
| 8 | `0x0b4439bb98e4391c2ab2c6dd3e3ed5f056db1868` | $0 | $3,626,336 | 0 / 211 | 2018-03-26 → 2022-03-29 |
| 9 | `0x660604c69fb23e7336ac0f5e5f992ece04c8353f` | $0 | $3,276,372 | 0 / 6 | 2022-02-25 → 2022-03-01 |
| 10 | `0xeba129db608bf4f9a75b1127334b369efd1ae690` | $0 | $3,163,564 | 0 / 1006 | 2017-12-13 → 2022-02-13 |
| 11 | `0x375b1d909a65a9f77431ed7e85910d50bdd5978f` | $0 | $2,502,047 | 0 / 197 | 2021-03-26 → 2022-07-20 |
| 12 | `0xb7cc1a4c9a23329f0ee99442a5258f85c8bc0c24` | $2,442,716 | $0 | 6 / 0 | 2017-12-11 → 2017-12-11 |
| 13 | `0xe0b2026e3db1606ef0beb764ccdf7b3cee30db4a` | $0 | $2,391,996 | 0 / 11 | 2018-02-04 → 2019-03-19 |
| 14 | `0x65bcfb0bc8dfdd6c284188c596df8b7aaa12d18b` | $0 | $2,289,640 | 0 / 1 | 2021-08-10 → 2021-08-10 |
| 15 | `0x8913e9491801c8cd83ca0c052655307f75d0a3b4` | $0 | $2,289,543 | 0 / 46 | 2021-05-03 → 2021-07-22 |
| 16 | `0xce27283c276f4aa7a7e302b24bfea7668e264877` | $0 | $2,200,860 | 0 / 2 | 2018-01-17 → 2018-02-05 |
| 17 | `0x99cf3c1098cad62f4ff3654420d4c8b783f97c40` | $0 | $2,002,462 | 0 / 123 | 2021-02-21 → 2022-07-18 |
| 18 | `0x0bb0623f2679e965a3d33552b29cef82b70d208e` | $0 | $1,686,856 | 0 / 6 | 2021-01-07 → 2021-09-05 |
| 19 | `0x32e04e19a63eae6fe19051fc24898ae21444f9c4` | $1,557,576 | $0 | 45 / 0 | 2020-03-21 → 2020-08-11 |
| 20 | `0xe76a41e1dbfbe34004885d5bbbd9c1bb332b0abf` | $0 | $1,470,262 | 0 / 1 | 2021-05-14 → 2021-05-14 |
| 21 | `0x3f6008d1a71bc064985289035e901ef52da481ee` | $0 | $1,459,074 | 0 / 19 | 2019-05-14 → 2022-06-15 |
| 22 | `0x9cabc5e6e46499a99782c645b3848ee8b99ac369` | $0 | $1,429,424 | 0 / 7 | 2021-02-23 → 2022-01-19 |
| 23 | `0xcbf91d30177dca1e71c2a9a29be1a1ba40b02dcf` | $0 | $1,400,840 | 0 / 24 | 2021-01-08 → 2022-04-01 |
| 24 | `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | $1,372,811 | $0 | 31 / 0 | 2020-03-21 → 2020-08-11 |
| 25 | `0xc280ee684fc751bd01fb4e7467808ea1392fade3` | $1,371,895 | $0 | 27 / 0 | 2020-03-21 → 2020-07-23 |
| 26 | `0x71751efff779417361e5b95d12c98bc1c697e9dc` | $0 | $1,339,571 | 0 / 25 | 2021-04-22 → 2021-07-02 |
| 27 | `0x003c2b071959397282a6227ddca9ce68299a2ba6` | $0 | $1,142,121 | 0 / 8 | 2021-01-10 → 2021-03-21 |
| 28 | `0xf2f9b18af21b3e2e17aa6d4e496b3e568c0aa00b` | $0 | $1,121,148 | 0 / 64 | 2018-10-05 → 2020-09-02 |
| 29 | `0x1dec601b3f97ea495f23ae0fb4d8333e38205679` | $0 | $1,061,940 | 0 / 8 | 2021-07-22 → 2022-04-27 |
| 30 | `0x05e3b0f81301791900effc613ee50ba423cc2b3a` | $0 | $1,044,722 | 0 / 12 | 2021-02-24 → 2021-04-23 |
| 31 | `0x570cfeeb0048b71a4a0ac0ee7fa8a669a229bcaa` | $0 | $1,039,783 | 0 / 3 | 2021-03-09 → 2021-03-09 |
| 32 | `0x4bfa5b2664ca061917837f882b2c003263756506` | $0 | $1,013,858 | 0 / 1 | 2021-10-14 → 2021-10-14 |
| 33 | `0x65467a249f00dcf1103c94eef7c51d3bd58dbef9` | $975,086 | $0 | 25 / 0 | 2020-03-26 → 2020-08-02 |
| 34 | `0x213e36b93857e8d76cb7fbe23471b41dc9f819cb` | $0 | $923,380 | 0 / 17 | 2019-05-06 → 2020-02-19 |
| 35 | `0xff9ef460d431b06d5c3f97a7c3852dad11477174` | $0 | $911,096 | 0 / 294 | 2018-11-20 → 2021-09-03 |
| 36 | `0x78dbfcc505d66487f52b7f10e5d0bec0658aeef9` | $0 | $866,352 | 0 / 12 | 2018-01-31 → 2021-10-21 |
| 37 | `0x71de5a1181c10bfaa2256e7bd836fc1eb89c34f3` | $0 | $825,269 | 0 / 2 | 2021-10-28 → 2021-10-28 |
| 38 | `0x33c26ec302ccfc12da94e6c2c08b3233e43e6ec7` | $0 | $794,374 | 0 / 135 | 2021-07-14 → 2021-12-09 |
| 39 | `0x13556e5d0ce2b4ca2d42d0f64091d55c067f4910` | $0 | $697,382 | 0 / 55 | 2020-08-09 → 2022-06-16 |
| 40 | `0x3bd053eacbe10abe688c4b85242951fed75720e3` | $0 | $693,524 | 0 / 5 | 2018-07-17 → 2021-07-04 |
| 41 | `0x44ca4a6d7263626dc35d21826d1e2193795323ff` | $0 | $692,612 | 0 / 1 | 2021-04-02 → 2021-04-02 |
| 42 | `0x2e370711b45011e7627d3648aa6c628cf5440479` | $0 | $680,873 | 0 / 1 | 2022-03-31 → 2022-03-31 |
| 43 | `0xfc3504c941c4cc2b047913cace6d6bc09211247f` | $0 | $671,599 | 0 / 2 | 2021-05-19 → 2021-05-19 |
| 44 | `0x116402c60f094c8b0482a3e27f698963c77251b1` | $668,092 | $0 | 2 / 0 | 2019-09-19 → 2019-12-31 |
| 45 | `0x105e76a9f40e706b6d272c66c0a2cf5bc711f9b1` | $0 | $665,962 | 0 / 4 | 2018-01-22 → 2018-01-24 |
| 46 | `0xff06adbb9cdd0815957096c54c98f5b246961cb0` | $0 | $655,565 | 0 / 3 | 2020-07-11 → 2021-05-07 |
| 47 | `0x6da6fb001e807635e97e67a33668a572d48c9ee6` | $0 | $654,751 | 0 / 42 | 2018-02-02 → 2021-10-07 |
| 48 | `0x52461c597ccf2aaf6f47560a520f178ed28a21e9` | $0 | $651,103 | 0 / 13 | 2017-12-12 → 2018-04-09 |
| 49 | `0x5e393568cd2f698c1884ba6870e387b8f140c937` | $616,164 | $0 | 7 / 0 | 2020-07-17 → 2020-08-09 |
| 50 | `0x7a34d5523e3b608cf12c7de1acbeab39a8ca1a46` | $0 | $597,734 | 0 / 62 | 2017-12-12 → 2019-04-02 |
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-1-counterparties.csv`](zonda-1-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0xf646cbe3b030fb6c2569215f0117dba58badb95e

[^1]: Etherscan, public name tag on Zonda 1. https://etherscan.io/address/0xf646cbe3b030fb6c2569215f0117dba58badb95e
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
