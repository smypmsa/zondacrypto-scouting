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
| Identified counterparties in this section | 4 internal + 304 external (Etherscan-tagged) + 2 external (hildobby-tagged) |
| Counterparties without a public name tag | **27,180 (full enumeration), aggregating ~$170,375,177 outbound and ~$2,937 inbound across `no-public-tag` + `below-cutoff` rows** |
| Active period (≥$1k events) | 2020-08-12 → 2022-08-03 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 3 `0x0ff24158…5289` | $189,202,109 | $0 | 93 |
| Zonda 2 `0x781229c7…57fc` | $22,219,874 | $2,228,043 | 10 |
| Zonda Deposit Funder 2 `0x818ab3c6…0d8d` | $0 | $73,606 | 4 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--:|--:|
| `0x2f9378d5…2aa5` | Binance Deposit: 0x2F9378D573b20199105bCaF6D103Ac88d5442aA5 | $16,795,348 | 92 |
| `0x22b8cc8c…3529` | Binance Deposit: 0x22b8cc8Cf448b7ED9f5ac1eE0446508461493529 | $9,565,980 | 404 |
| `0x088ae43b…b519` | Binance Deposit: 0x088Ae43BE934bA729d8D841b41649c4d417bb519 | $2,659,141 | 124 |
| `0x8a63afd3…25b5` | Binance Deposit: 0x8a63AFd33e0d05274B3B6650486D9960785025B5 | $2,412,616 | 77 |
| `0xf1baaae9…ecdd` | Fee Recipient: 0xf1ba...cdd | $1,419,132 | 1 |
| `0x6384098c…e6ea` | Binance Deposit: 0x6384098C92B56ad4c6e7F28d098aca733644e6Ea | $449,341 | 22 |
| `0xbdd22c2f…b476` | Binance Deposit: 0xbdD22c2Fa67010f9A6dCA20a4F0C2C2a9832B476 | $298,881 | 1 |
| `0x4c811713…fa5f` | Binance Deposit: 0x4C8117138b821EA72b973dA96B613Fcb64f2fA5F | $252,886 | 70 |
| `0x98683107…4ecb` | Binance Deposit: 0x98683107A88D2300C071e8fE34e9504872e74eCb | $182,923 | 26 |
| `0x0555449e…99f6` | ByBit Deposit: 0x0555449e8aFa4Ee1a3eca8CF10034Ef4c09099f6 | $168,304 | 10 |
| `0xb114a576…138d` | Binance Deposit: 0xb114a576dfee6e6bbF8bA386D8F89399E9bd138d | $129,252 | 1 |
| `0x8ce3e4d3…7eea` | Fee Recipient: 0x8ce3...eea | $117,151 | 1 |
| `0x3f38522e…cd93` | Binance Deposit: 0x3f38522e2c8953b18ebdb1169f9132ab3067cd93 | $105,863 | 1 |
| `0x8b52ecab…1aa9` | Binance Deposit: 0x8B52ecAB07EC047434DbE1ddcDD1f06eE7Fa1aa9 | $103,969 | 1 |
| `0x56d19c03…e44e` | Binance Deposit: 0x56d19c0312824781acfbc34dfec7f15605abe44e | $101,161 | 7 |
| `0x49db4a49…7526` | Binance Deposit: 0x49db4a49186bf3f38528dd735afccfed1acf7526 | $96,147 | 1 |
| `0x2ccb32b2…542d` | Binance Deposit: 0x2cCB32b2b26bF3A6f5571640612587aA029F542D | $87,826 | 1 |
| `0x2a51c4f1…e9b9` | Binance Deposit: 0x2a51C4F1C7D50B86BB7df7837978E70d2e44E9b9 | $87,638 | 1 |
| `0x2b89ddcc…b532` | Binance Deposit: 0x2b89DdCCA116AFa5D0697e0d978B752fefeAB532 | $82,577 | 6 |
| `0xb55ae8a6…150b` | Fee Recipient: 0xb55a...50b | $77,629 | 3 |
| `0xfca25c20…9752` | Binance Deposit: 0xFca25C2047eC780c9b9FE9407C7FAA70175b9752 | $72,903 | 7 |
| `0xd8ce0162…9db6` | Binance Deposit: 0xD8cE0162004D7871a2956d3C334C6b479b309db6 | $72,892 | 3 |
| `0xf849bc94…acd8` | Binance Deposit: 0xF849bc94Cd941524b0569E41A80106414937ACD8 | $68,639 | 3 |
| `0xff8adfda…d555` | Binance Deposit: 0xff8adfda71495b17a7ad5b7a72e93e323043d555 | $68,248 | 2 |
| `0x937fafd3…0161` | Binance Deposit: 0x937faFD3aaa9b4155E00888317bEe53900f00161 | $65,144 | 3 |
| `0x160a946f…e4ee` | Binance Deposit: 0x160A946f4daA72E76C923A42deA703a430f1e4EE | $62,590 | 2 |
| `0xae2acc0b…8617` | Binance Deposit: 0xAE2ACC0B528B2c9c18df87Fd188DAeAA74538617 | $59,435 | 1 |
| `0x93d8f711…95f9` | Binance Deposit: 0x93d8f711940F2336a7D486fC2a0Ec4357ebc95F9 | $58,470 | 1 |
| `0x99cc80b6…f1d5` | Binance Deposit: 0x99cc80b63a1df3fa99a5197e8e77d56d2032f1d5 | $56,883 | 3 |
| `0x937ed55c…cee0` | Binance Deposit: 0x937Ed55c3b7acE1eB095254Ea06c1C055C0BCeE0 | $55,177 | 8 |
| `0x287e6d4d…95fa` | Binance Deposit: 0x287e6D4DD4d57ede08B9353e13D51d9F7F1f95fA | $52,891 | 4 |
| `0xedc75e17…dff0` | Binance Deposit: 0xedC75e171328EF5b8Bc88b4A2a887fEE52ecDFf0 | $51,264 | 1 |
| `0x913b3626…bf2d` | Binance Deposit: 0x913b362601abec347a493979b0938007c201bf2d | $51,238 | 3 |
| `0x0d4ddf20…8594` | Binance Deposit: 0x0d4DDf20A7cDc017fB9f2162eBdCa71f49508594 | $49,938 | 2 |
| `0xd5b546fe…573e` | ByBit Deposit: 0xd5B546fe5a713b712f92fD97fa894c5b831a573E | $49,661 | 10 |
| `0xbc6a9ba1…e0f6` | Binance Deposit: 0xbc6a9ba126832ecc42ea903666a7e8e7fabbe0f6 | $49,639 | 1 |
| `0x99548c17…71b2` | Binance Deposit: 0x99548c17169ea2d38808a1282c9f4c6f9ecd71b2 | $48,757 | 1 |
| `0x4b53d432…d5fb` | Binance Deposit: 0x4B53d4325960E5819DfE0EF6E78d06690BEcd5fB | $46,811 | 4 |
| `0x9b61510f…a2f2` | Binance Deposit: 0x9B61510f78DBdAa95eC4b51eDE517f7Fd540a2F2 | $45,486 | 8 |
| `0x7460528d…d72b` | Binance Deposit: 0x7460528d4ABAf5502266B97Bd4F7B1D493dBd72b | $44,404 | 4 |
| `0x601c7ac1…1e86` | Binance Deposit: 0x601c7ac18958ae1ae67ecbaa42c6a7f14d971e86 | $44,086 | 1 |
| `0xb5bf47b6…8f8f` | ByBit Deposit: 0xb5bf47B65C12234fdbe3BeFf5EBaDc8D9EE48F8f | $42,684 | 2 |
| `0xb7f6bb09…e9f4` | ByBit Deposit: 0xb7f6bb0969AE3DF281C081932F0068E15a6aE9F4 | $42,410 | 1 |
| `0x78ea0a35…b39c` | Binance Deposit: 0x78EA0A357A1512B352Bb2b905f8347B2C232b39c | $39,770 | 5 |
| `0x4cf14289…f3fa` | Binance Deposit: 0x4cf14289fA7A8915317d685b88241d422Fd2f3fA | $39,669 | 16 |
| `0x75cb2d05…35f9` | Binance Deposit: 0x75Cb2d05B2a7fAb8C6C146178edEEd32203135f9 | $39,274 | 1 |
| `0xdb52f4b5…dfba` | Binance Deposit: 0xDb52f4b57257711da65796c55a5C4A4d9c08dFBa | $38,367 | 1 |
| `0x8598b4e6…da7b` | Binance Deposit: 0x8598b4E69FB2c7338D254D42b65544ed4203dA7b | $38,147 | 1 |
| `0xa6c39395…2406` | Binance Deposit: 0xA6c39395d6F3C53486d52Cc75f530050cDd22406 | $36,693 | 2 |
| `0x586ebf87…b5c8` | Binance Deposit: 0x586ebF87dE17f658F3CcEF92e1a561203c7Cb5C8 | $36,326 | 2 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $3,230 | $0 | 1 / 0 |
| `0x564286362092d8e7936f0549571a803b203aaced` | Binance 3 | $43 | $0 | 1 / 0 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 27,180 of the 27,486 external counterparties in the full enumeration carry no public name tag on Etherscan as of 2026-05-14 (closure-pass) and do not appear in this inventory's roster. The unidentified rows aggregate **$170,375,177 outbound** and **$2,937 inbound** across `no-public-tag` + `below-cutoff` rows. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

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
