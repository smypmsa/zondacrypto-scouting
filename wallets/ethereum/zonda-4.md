# Zonda 4

**Address:** `0x2b645268e2fbb384b423e50089657395f749763a`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet. Dormant since approximately 2023-Q3.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda 4" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses on Dune Analytics (entry added 2023-11-23 alongside Zonda 1, 2 and 3).[^2] The receipt of the Dune query result is preserved at [`sources/dune/hildobby-3237025-zonda-rows.json`](../../sources/dune/hildobby-3237025-zonda-rows.json).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2020-08-12 (block 10644338); most recent 2022-10-05 (block 15681063); ≥ 10,000 events.
- ERC-20 events: first 2020-10-26 (block 11131445); most recent 2026-04-16 (block 24892556); 21 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $211,425,213 |
| Gross OUT (USD-equivalent at tx time) | $204,467,998 |
| Total throughput (gross in + out) | $415,893,212 |
| Net direction | +$6,957,215 |
| Total events ≥$1k | 20,144 |
| Distinct external counterparties (≥$1k cumulative) | 13,779 |
| Identified counterparties in this section | 3 internal + 5 external (Etherscan-tagged) |
| Counterparties without a public name tag | **13,774, aggregating ~$94,359,736 outbound and ~$0 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2020-08-12 → 2022-08-03 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 3 `0x0ff24158…5289` | $189,202,109 | $0 | 93 |
| Zonda 2 `0x781229c7…57fc` | $22,219,874 | $2,228,043 | 10 |
| Zonda Deposit Funder 2 `0x818ab3c6…0d8d` | $0 | $73,606 | 4 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x2f9378d5…2aa5` | Binance Deposit: 0x2F9378D573b20199105bCaF6D103Ac88d5442aA5 | $16,795,348 | 92 |
| `0x22b8cc8c…3529` | Binance Deposit: 0x22b8cc8Cf448b7ED9f5ac1eE0446508461493529 | $9,565,980 | 404 |
| `0x088ae43b…b519` | Binance Deposit: 0x088Ae43BE934bA729d8D841b41649c4d417bb519 | $2,659,141 | 124 |
| `0x8a63afd3…25b5` | Binance Deposit: 0x8a63AFd33e0d05274B3B6650486D9960785025B5 | $2,412,616 | 77 |
| `0xf1baaae9…ecdd` | Fee Recipient: 0xf1ba...cdd | $1,419,132 | 1 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $3,230 | $0 | 1 / 0 |
| `0x564286362092d8e7936f0549571a803b203aaced` | Binance 3 | $43 | $0 | 1 / 0 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 13,774 of the 13,782 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$94,359,736 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x68ed0dcde71fc3b45d7f8cb84946328b49ee1746` | $0 | $5,471,007 | 0 / 2 | 2021-05-04 → 2021-10-29 |
| 2 | `0xa5ed22920276dfd6fc3bb25b889f59a620ad23e8` | $0 | $3,879,941 | 0 / 20 | 2020-10-14 → 2022-05-16 |
| 3 | `0x0ca1e75f88a1ad6ec5b0b4c92cf135179b2fa107` | $0 | $3,726,696 | 0 / 19 | 2020-11-18 → 2021-12-01 |
| 4 | `0x65c349fa4e1c64115c30e731e5e1c29b7c822690` | $0 | $3,269,494 | 0 / 21 | 2021-12-15 → 2022-07-11 |
| 5 | `0xb7db2f3f14726ee4013fc52fe81e6f168acb8fa5` | $0 | $2,977,502 | 0 / 3 | 2022-02-24 → 2022-07-16 |
| 6 | `0x8913e9491801c8cd83ca0c052655307f75d0a3b4` | $0 | $2,380,398 | 0 / 47 | 2021-04-28 → 2021-07-13 |
| 7 | `0x99cf3c1098cad62f4ff3654420d4c8b783f97c40` | $0 | $2,324,024 | 0 / 139 | 2021-02-22 → 2022-06-25 |
| 8 | `0x3f6008d1a71bc064985289035e901ef52da481ee` | $0 | $2,199,794 | 0 / 19 | 2021-05-25 → 2022-05-10 |
| 9 | `0xcbf91d30177dca1e71c2a9a29be1a1ba40b02dcf` | $0 | $1,930,384 | 0 / 44 | 2020-10-12 → 2022-05-12 |
| 10 | `0xa1357baf545167a03e5ac599154397c971185b0a` | $0 | $1,842,348 | 0 / 3 | 2021-02-14 → 2021-02-14 |
| 11 | `0x0b4439bb98e4391c2ab2c6dd3e3ed5f056db1868` | $0 | $1,769,475 | 0 / 31 | 2020-10-11 → 2021-12-03 |
| 12 | `0x375b1d909a65a9f77431ed7e85910d50bdd5978f` | $0 | $1,769,292 | 0 / 159 | 2020-12-11 → 2022-07-16 |
| 13 | `0x7532e70ad7b53c27e2f5b569f671785a2e5efdc8` | $0 | $1,593,827 | 0 / 1 | 2021-08-06 → 2021-08-06 |
| 14 | `0xe55c8c59528da3d18c1ee4d35ac9ff7bfe020ada` | $0 | $1,354,868 | 0 / 3 | 2021-05-12 → 2021-05-12 |
| 15 | `0xb605b2d488af1389e00801ee50eef365d7400fea` | $0 | $1,031,259 | 0 / 18 | 2021-04-06 → 2021-11-19 |
| 16 | `0x33c26ec302ccfc12da94e6c2c08b3233e43e6ec7` | $0 | $935,418 | 0 / 198 | 2021-07-05 → 2021-12-03 |
| 17 | `0x04b772e9fc7179a541f9be5ecce28fc056a41a60` | $0 | $909,321 | 0 / 1 | 2020-10-06 → 2020-10-06 |
| 18 | `0xfde9292293171fa4ed63f05cff414f2db414cc55` | $0 | $715,708 | 0 / 57 | 2020-08-14 → 2022-03-18 |
| 19 | `0x7e39b8d7ae17ec470af5d0e640c6c84983ed584c` | $0 | $708,239 | 0 / 3 | 2021-05-12 → 2021-11-01 |
| 20 | `0x78dbfcc505d66487f52b7f10e5d0bec0658aeef9` | $0 | $688,308 | 0 / 9 | 2020-09-03 → 2021-10-31 |
| 21 | `0x607e2f75fc3d1ce3c3bb469f3b1437b59c4293cd` | $0 | $679,684 | 0 / 2 | 2022-02-08 → 2022-02-08 |
| 22 | `0x5554352009ff7a788df23186ad9a1b3ba1306235` | $0 | $678,391 | 0 / 4 | 2020-12-09 → 2020-12-10 |
| 23 | `0x46df70bfa0e2b635f0b2f6ac9ea62f6b8f7260ee` | $0 | $633,517 | 0 / 4 | 2021-03-16 → 2021-05-26 |
| 24 | `0x98334f075c9ac54f9236ef078fb43e24f2fc9221` | $0 | $632,705 | 0 / 3 | 2020-10-15 → 2020-10-19 |
| 25 | `0x0bb0623f2679e965a3d33552b29cef82b70d208e` | $0 | $605,472 | 0 / 6 | 2021-01-06 → 2021-10-05 |
| 26 | `0x20d7e67aca04d5f9f411df98e3ea3e6bac0dd9ae` | $0 | $590,410 | 0 / 2 | 2021-03-15 → 2021-03-15 |
| 27 | `0x1dec601b3f97ea495f23ae0fb4d8333e38205679` | $0 | $582,902 | 0 / 4 | 2021-07-13 → 2022-04-06 |
| 28 | `0x0841e837227b0877f199a4193b43f3a34db3c510` | $0 | $565,990 | 0 / 1 | 2021-04-19 → 2021-04-19 |
| 29 | `0xeba129db608bf4f9a75b1127334b369efd1ae690` | $0 | $556,001 | 0 / 25 | 2020-08-13 → 2022-02-07 |
| 30 | `0x6da6fb001e807635e97e67a33668a572d48c9ee6` | $0 | $539,958 | 0 / 23 | 2020-10-11 → 2021-10-31 |
| 31 | `0xa6175950bc7177a9c93a0f3844e6a0c164161532` | $0 | $539,832 | 0 / 4 | 2022-06-10 → 2022-06-21 |
| 32 | `0x13556e5d0ce2b4ca2d42d0f64091d55c067f4910` | $0 | $513,520 | 0 / 58 | 2020-09-08 → 2022-07-12 |
| 33 | `0xff9ef460d431b06d5c3f97a7c3852dad11477174` | $0 | $496,604 | 0 / 51 | 2020-08-13 → 2022-05-12 |
| 34 | `0x2c41cb44695629c2e0514c0f81640cef9d3b2d47` | $0 | $491,915 | 0 / 4 | 2021-11-24 → 2021-12-03 |
| 35 | `0xf12c4cb357e2c22a3c78fafb5382a223098fbaae` | $0 | $486,518 | 0 / 16 | 2021-11-23 → 2022-06-23 |
| 36 | `0x51996f7d7aa9681b5099112339a14073659f7301` | $0 | $455,563 | 0 / 4 | 2021-08-01 → 2021-09-01 |
| 37 | `0xeed151fd3d484592c359cf8177d72c5d5ef0e54a` | $0 | $440,205 | 0 / 1 | 2022-03-03 → 2022-03-03 |
| 38 | `0xe5cac983f5f01490d2e099e385383239fe87078a` | $0 | $428,090 | 0 / 3 | 2020-09-08 → 2021-01-19 |
| 39 | `0xf2f9b18af21b3e2e17aa6d4e496b3e568c0aa00b` | $0 | $424,110 | 0 / 13 | 2020-09-01 → 2021-04-29 |
| 40 | `0xcfad81d2375062c2a5e0ac27f694585308950b10` | $0 | $419,326 | 0 / 9 | 2021-10-18 → 2021-11-02 |
| 41 | `0x069f68f1100ac2353eb93403e44b29f6e52a1d39` | $0 | $418,634 | 0 / 3 | 2021-02-18 → 2021-05-24 |
| 42 | `0x95c1ef1a09430144700c4b781ec0925d0644c0af` | $0 | $413,307 | 0 / 9 | 2021-01-29 → 2022-03-19 |
| 43 | `0x71751efff779417361e5b95d12c98bc1c697e9dc` | $0 | $387,171 | 0 / 7 | 2021-05-12 → 2021-05-12 |
| 44 | `0x003c2b071959397282a6227ddca9ce68299a2ba6` | $0 | $358,766 | 0 / 2 | 2021-03-21 → 2021-03-21 |
| 45 | `0x05e3b0f81301791900effc613ee50ba423cc2b3a` | $0 | $358,653 | 0 / 4 | 2021-02-22 → 2021-03-15 |
| 46 | `0x156415405fe8c9d7b3e460e76f7bd01a7150dcea` | $0 | $352,139 | 0 / 5 | 2021-05-12 → 2021-08-01 |
| 47 | `0xb9cfff128f426b29be55ddc7c69a14dee4092e78` | $0 | $335,449 | 0 / 5 | 2022-04-22 → 2022-06-22 |
| 48 | `0x2ea024ae1338af5e48ee9179d54f52c90d7b3929` | $0 | $332,032 | 0 / 265 | 2020-10-02 → 2021-09-23 |
| 49 | `0xe6615f7eeec4af5a4535ffbdca2e17d207cf1d81` | $0 | $328,724 | 0 / 4 | 2021-02-19 → 2021-03-04 |
| 50 | `0x6824a2835017d6d01223a945ee6ffed15de433f9` | $0 | $313,518 | 0 / 1 | 2021-04-07 → 2021-04-07 |
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-4-counterparties.csv`](zonda-4-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x2b645268e2fbb384b423e50089657395f749763a

[^1]: Etherscan, public name tag on Zonda 4. https://etherscan.io/address/0x2b645268e2fbb384b423e50089657395f749763a
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda 4"`, `added_date="2023-11-23"`. https://dune.com/queries/3237025
