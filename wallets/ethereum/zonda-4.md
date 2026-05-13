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

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 13,774 of the 13,782 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$94,359,736 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

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

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x2b645268e2fbb384b423e50089657395f749763a

[^1]: Etherscan, public name tag on Zonda 4. https://etherscan.io/address/0x2b645268e2fbb384b423e50089657395f749763a
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda 4"`, `added_date="2023-11-23"`. https://dune.com/queries/3237025
