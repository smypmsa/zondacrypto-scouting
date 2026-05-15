# Zonda (BitBay) (0x56d943…4778)

> **Plain-language summary.** An actively-trading Ethereum wallet attributed to ZondaCrypto / BitBay by Bubblemaps (`entity_id = "zonda"`, additionally marked CEX-related). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Top-100 ZND holder at 0.0055% of supply. Underlying transfers are CONFIRMED from on-chain data; their attribution to ZondaCrypto operations inherits the wallet's PARTIAL tier.

**Address:** `0x56d943aea92b099228b31f01cd12bd4aa39b4778`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps. Bubblemaps further marks it as CEX-related (`is_cex = true`).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Bubblemaps' `addresses/token-top-holders` endpoint for the ZND token returns this address with `label = "Zonda (BitBay) (0x56…4778)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

The address is currently active (latest activity within minutes of the snapshot), holds ~1.2 ETH and ~$22k across 142 tokens, and ranks as a top-100 ZND holder at 0.0055% of supply.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2025-08-04 (block 23066436); most recent 2026-05-13 (block 25085262); ≥ 10,000 events.
- ERC-20 events: first 2025-08-04 (block 23066882); most recent 2026-05-13 (block 25085262); ≥ 10,000 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $3,806,066 |
| Gross OUT (USD-equivalent at tx time) | $207,323 |
| Total throughput (gross in + out) | $4,013,389 |
| Net direction | +$3,598,743 |
| Total events ≥$1k | 829 |
| Distinct external counterparties (≥$1k cumulative) | 455 |
| Identified counterparties in this section | 0 internal + 10 external (Etherscan-tagged) |
| Counterparties without a public name tag | **445, aggregating ~$203,129 outbound and ~$205,309 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2025-08-04 → 2026-05-12 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### External counterparties — confirmed via public name tag
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x674e7b96…7b35` | ByBit Deposit: 0x674E7B96a0f5FB81dAda4A6F9e7B07A7E2067B35 | $3,096 | 3 |
| `0xb61b6f84…4bb0` | Binance Deposit: 0xB61b6f8480BD0581931d64964fb2640fa6134BB0 | $1,099 | 1 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xae2d4617c862309a3d75a0ffb358c7a5009c673f` | Kraken 10 | $163,342 | $0 | 14 / 0 |
| `0x267be1c1d684f78cb4f6a176c4911b741e4ffdc0` | Kraken 4 | $81,599 | $0 | 37 / 0 |
| `0x6d0cf1f651f5ae585d24dcaa188d44e389e93d26` | Kraken 55 | $6,973 | $0 | 6 / 0 |
| `0x23d4df4631aa3ca30653d3c29c0eeef607b1d9fd` | Kraken 80 | $2,313 | $0 | 2 / 0 |
| `0x16b2b042f15564bb8585259f535907f375bdc415` | Kraken 43 | $1,160 | $0 | 1 / 0 |
| `0x735fd3c55a8be1aeb3544c7e29eba3ea23500a1c` | Kraken 54 | $1,158 | $0 | 1 / 0 |
| `0x0eefaf34f9ccf41366ab547330c8978be8fd3ff9` | Kraken 94 | $1,158 | $0 | 1 / 0 |
| `0x4e9ce36e442e55ecd9025b9a6e0d88485d628a67` | Binance 6 | $0 | $43 | 0 / 1 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x05ff6964…f381` | Kraken: Hot Wallet 4 | $2,428,358 | 208 |
| `0xf30ba13e…0eb0` | Kraken: Hot Wallet 2 | $915,854 | 386 |
| `0xae2d4617…673f` | Kraken 10 | $163,342 | 14 |
| `0x267be1c1…fdc0` | Kraken 4 | $81,599 | 37 |
| `0x6d0cf1f6…3d26` | Kraken 17 | $6,973 | 6 |
| `0x23d4df46…d9fd` | Kraken 93 | $2,313 | 2 |
| `0x16b2b042…c415` | Kraken 33 | $1,160 | 1 |
| `0x735fd3c5…0a1c` | Kraken 18 | $1,158 | 1 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 445 of the 455 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$203,129 outbound** and **$205,309 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x0895934c201640b85f87c97ac67106c41a801312` | $0 | $823,173 | 0 / 5000 | 2025-10-08 → 2026-05-13 |
| 2 | `0x2744dfd9898f0babbc570cc594bbbc84b487a22b` | $187,783 | $0 | 16 / 0 | 2026-04-23 → 2026-05-12 |
| 3 | `0xb6be26445f21e41bc69197fe68f697fc1a862f19` | $0 | $167,433 | 0 / 805 | 2025-08-04 → 2025-10-08 |
| 4 | `0x5739bd4d9a458a3ba4e82fa53fa36ac0e7296145` | $0 | $39,512 | 0 / 76 | 2025-09-17 → 2025-10-15 |
| 5 | `0xfd2636d89bb1fd7e9858e0a21ea55acf50f1a6d5` | $0 | $37,859 | 0 / 63 | 2025-11-12 → 2025-11-30 |
| 6 | `0x17ae29da50f39968e81186b35e4b222e85a89f93` | $0 | $28,479 | 0 / 223 | 2025-08-04 → 2026-03-03 |
| 7 | `0xe4f872b5403c1a5d57d430fe2d94529228c05b25` | $0 | $27,040 | 0 / 275 | 2025-08-04 → 2026-01-26 |
| 8 | `0x5559e8bc0f49cedef12dc768f7a60d6b030e7032` | $0 | $23,015 | 0 / 93 | 2026-01-14 → 2026-05-12 |
| 9 | `0xb167dfd37b685aebbe6aa3901ccf6b944bdccc49` | $0 | $21,253 | 0 / 489 | 2025-08-04 → 2026-05-12 |
| 10 | `0x61170259dd894f2014c46ceba582bf5c92046ea7` | $0 | $19,265 | 0 / 192 | 2025-11-23 → 2026-04-11 |

<details><summary>Show 40 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0x4b52365d18851ab17af795b904552c9bc048bc3c` | $0 | $19,253 | 0 / 48 | 2025-09-26 → 2025-10-23 |
| 12 | `0xf0e89746a02bb93d3a42243d15382902530791e3` | $0 | $19,173 | 0 / 70 | 2026-02-02 → 2026-04-16 |
| 13 | `0x31cfa831ce6877b85ae69b66b6bf302846be89c4` | $0 | $18,703 | 0 / 394 | 2026-02-08 → 2026-04-23 |
| 14 | `0x58422bb6076a9e319140a51454d92bde8749c0d0` | $0 | $17,362 | 0 / 195 | 2025-12-31 → 2026-05-12 |
| 15 | `0xcabbc6def47f26e610750866fe33fed3feb119a4` | $0 | $16,793 | 0 / 51 | 2025-12-28 → 2026-03-04 |
| 16 | `0xa53099533b3be4aab363bb67b965e89bc47d7fe3` | $0 | $16,199 | 0 / 317 | 2025-12-18 → 2026-01-19 |
| 17 | `0xff44c08f3d32fe00761d1512ec864a1804ac7534` | $0 | $15,816 | 0 / 82 | 2025-08-08 → 2025-09-02 |
| 18 | `0x2c08aa8132302ae562ccb2fd51d47711198d7292` | $0 | $15,274 | 0 / 22 | 2026-01-14 → 2026-02-04 |
| 19 | `0x631a897f0dd4501710882f05339f267d447f4d75` | $0 | $14,537 | 0 / 75 | 2025-12-26 → 2026-05-13 |
| 20 | `0xd2b53bc6b9a55ddc2768c2cc8773d6e98d465cc6` | $0 | $13,872 | 0 / 77 | 2025-11-30 → 2026-04-16 |
| 21 | `0x6f28ba3ceed14050944e2a00f33dfab5760a3d46` | $0 | $13,810 | 0 / 24 | 2025-12-14 → 2026-04-12 |
| 22 | `0xe1653a4fa8f60e2f4c2bb6c7fb73d90766d7ad1f` | $0 | $12,908 | 0 / 255 | 2025-11-19 → 2026-05-10 |
| 23 | `0xcfaee73d55778fbe5778a79bee1b9e27222dc5ab` | $0 | $12,465 | 0 / 199 | 2025-10-08 → 2025-12-05 |
| 24 | `0xd340bb8bf2c56f2ddd20e24202f0e81fb9ea948a` | $0 | $12,280 | 0 / 88 | 2026-01-23 → 2026-01-23 |
| 25 | `0x7b4b750b01b00e2e804d218f808dba1dfd2ed5d3` | $0 | $12,159 | 0 / 167 | 2026-04-01 → 2026-05-11 |
| 26 | `0x81aae171a30686f45e77c8051c8ce357eedda5bd` | $0 | $12,055 | 0 / 140 | 2025-08-10 → 2026-01-03 |
| 27 | `0x9ea4c8390c2bcbb095b2131ee9570d10497595cd` | $0 | $11,958 | 0 / 61 | 2025-08-10 → 2026-03-20 |
| 28 | `0xdddf2cf5b07c01f7cd53c2f7396363ba10116427` | $0 | $11,813 | 0 / 95 | 2025-08-29 → 2025-12-27 |
| 29 | `0x05da17b0ab16aaa9508c08b1223f73973a966f4d` | $0 | $11,558 | 0 / 475 | 2026-01-01 → 2026-05-12 |
| 30 | `0xf929723dbcd378055ed77199700f2370337bd8d6` | $0 | $10,771 | 0 / 35 | 2025-10-15 → 2025-12-13 |
| 31 | `0xe4f22361075c1bf442525594ef405238dc6bd504` | $0 | $10,482 | 0 / 138 | 2025-08-20 → 2026-04-09 |
| 32 | `0x9241af0c0fcdf619b4742bf909922b0b30c3d54d` | $0 | $10,454 | 0 / 135 | 2025-12-26 → 2026-05-02 |
| 33 | `0x12a8a70920bcf13038fe66c3706e0726bdb238d3` | $0 | $10,073 | 0 / 42 | 2025-10-11 → 2025-12-26 |
| 34 | `0xab77c233c12ef41f124fb6675c627f27c7a06d72` | $0 | $9,938 | 0 / 61 | 2026-04-13 → 2026-04-14 |
| 35 | `0x50c15b0e6c52fe903d3b69c2da344cd08f6de24f` | $0 | $9,853 | 0 / 71 | 2025-11-29 → 2026-02-04 |
| 36 | `0x26b2b9f11e73e2bcf2672dc8e789f18b62ea3911` | $0 | $9,599 | 0 / 367 | 2026-04-05 → 2026-05-09 |
| 37 | `0xc8cb79c8d9db3b13da86817d48c4427a8bfc724f` | $0 | $9,019 | 0 / 124 | 2026-01-20 → 2026-05-12 |
| 38 | `0xcca52c97838b278ec889bbbe17789693e200ffdf` | $0 | $8,915 | 0 / 369 | 2025-08-04 → 2026-01-01 |
| 39 | `0xdabc080870d5651b38ed4befe3ff0d03d2855591` | $0 | $8,807 | 0 / 94 | 2025-08-29 → 2026-01-05 |
| 40 | `0x420b61e074b772fc3967bff83d69aa40ae3f3acd` | $0 | $8,400 | 0 / 68 | 2025-12-31 → 2026-03-18 |
| 41 | `0xfa83c60c602ac839b6e7fedc669dbf3bd78abfd1` | $0 | $8,157 | 0 / 166 | 2025-10-10 → 2026-05-10 |
| 42 | `0x77b928d963f6b40120c8eb6fa4ffa89828c07e44` | $0 | $8,091 | 0 / 50 | 2026-01-21 → 2026-01-22 |
| 43 | `0x5a00a37a3cf67721c834ca2e617c9961f956f9c4` | $0 | $8,089 | 0 / 47 | 2025-11-26 → 2026-02-10 |
| 44 | `0xef78e90d20ff81a84ab99f9e3fd8a53467b9ea5d` | $0 | $8,082 | 0 / 30 | 2026-03-04 → 2026-04-14 |
| 45 | `0x10cd984619c73605845ca25f79f36be146b6e746` | $0 | $8,052 | 0 / 67 | 2025-10-14 → 2025-12-20 |
| 46 | `0x1106a845ba7550b1ccd9a711799aaffa96234f28` | $0 | $8,019 | 0 / 63 | 2026-02-22 → 2026-03-19 |
| 47 | `0x9106a6bc2b16c170533f38895fa02c257030b4f3` | $0 | $7,702 | 0 / 94 | 2025-11-09 → 2025-12-29 |
| 48 | `0x675a2816eefdf4faaa60096dad8b152828f56098` | $0 | $7,530 | 0 / 14 | 2026-01-04 → 2026-01-14 |
| 49 | `0xaee32e65115bd8619a7985815639382fa76f6fca` | $0 | $7,391 | 0 / 28 | 2025-12-04 → 2025-12-17 |
| 50 | `0xb27ce726630caaceaaf93a1597770b3e39ea2969` | $0 | $7,380 | 0 / 92 | 2025-11-27 → 2026-01-31 |

</details>
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-bitbay-56d943-counterparties.csv`](zonda-bitbay-56d943-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x56d943aea92b099228b31f01cd12bd4aa39b4778

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
