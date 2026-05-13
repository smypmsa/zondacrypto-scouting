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

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 27,850 of the 27,860 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$144,689,346 outbound** and **$13,595,114 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x68ed0dcde71fc3b45d7f8cb84946328b49ee1746` | $0 | $7,226,754 | 0 / 5 | 2020-07-23 → 2021-08-31 |
| 2 | `0xa5ed22920276dfd6fc3bb25b889f59a620ad23e8` | $0 | $5,924,325 | 0 / 63 | 2018-02-02 → 2022-03-29 |
| 3 | `0x0ca1e75f88a1ad6ec5b0b4c92cf135179b2fa107` | $0 | $5,232,272 | 0 / 87 | 2019-02-11 → 2021-12-07 |
| 4 | `0x944da046783f24b6fe6013da23c46e5d1806f0e6` | $0 | $4,704,915 | 0 / 6 | 2017-12-13 → 2018-04-20 |
| 5 | `0x65c349fa4e1c64115c30e731e5e1c29b7c822690` | $0 | $4,566,755 | 0 / 29 | 2021-12-08 → 2022-07-07 |
| 6 | `0xb7db2f3f14726ee4013fc52fe81e6f168acb8fa5` | $0 | $4,304,246 | 0 / 3 | 2021-10-07 → 2022-07-17 |
| 7 | `0x7532e70ad7b53c27e2f5b569f671785a2e5efdc8` | $0 | $4,028,204 | 0 / 3 | 2021-01-09 → 2021-02-23 |
| 8 | `0x0b4439bb98e4391c2ab2c6dd3e3ed5f056db1868` | $0 | $3,624,810 | 0 / 209 | 2018-03-26 → 2022-03-29 |
| 9 | `0x660604c69fb23e7336ac0f5e5f992ece04c8353f` | $0 | $3,276,030 | 0 / 5 | 2022-02-25 → 2022-03-01 |
| 10 | `0xeba129db608bf4f9a75b1127334b369efd1ae690` | $0 | $3,027,337 | 0 / 757 | 2017-12-13 → 2022-02-13 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0xf646cbe3b030fb6c2569215f0117dba58badb95e

[^1]: Etherscan, public name tag on Zonda 1. https://etherscan.io/address/0xf646cbe3b030fb6c2569215f0117dba58badb95e
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
