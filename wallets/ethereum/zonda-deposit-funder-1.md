# Zonda Deposit Funder 1

**Address:** `0x5bff49eec8f76c066f979a818187b9732ac69503`

**Chain:** Ethereum.

**Role:** ZondaCrypto deposit-funder / gas-supplier wallet. Exchanges typically maintain a small set of EOAs that pre-fund user-deposit addresses with the ETH needed to pay forwarding gas. This is one of them.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda: Deposit Funder 1" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses on Dune Analytics (entry added 2024-10-06 as "Zonda Gas Supplier 1").[^2] The receipt of the Dune query result is preserved at [`sources/dune/hildobby-3237025-zonda-rows.json`](../../sources/dune/hildobby-3237025-zonda-rows.json).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2023-10-31 (block 18468877); most recent 2026-04-27 (block 24972323); ≥ 10,000 events.
- ERC-20 events: first 2023-10-31 (block 18469076); most recent 2026-04-26 (block 24964245); 1,255 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $678,457 |
| Gross OUT (USD-equivalent at tx time) | $507,304 |
| Total throughput (gross in + out) | $1,185,760 |
| Net direction | +$171,153 |
| Total events ≥$1k | 16 |
| Distinct external counterparties (≥$1k cumulative) | 3 |
| Identified counterparties in this section | 3 internal + 0 external (Etherscan-tagged) |
| Counterparties without a public name tag | **3, aggregating ~$0 outbound and ~$0 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2023-10-31 → 2026-01-15 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $678,457 | $0 | 14 |
| Zonda 6 `0xd388009f…8046` | $0 | $500,662 | 1 |
| Zonda 2 `0x781229c7…57fc` | $0 | $6,641 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 3 of the 6 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `../../sources/dune/inventory-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `../../sources/dune/inventory-per-wallet-totals-2026-05-13.json` (query 7491746) and `../../sources/dune/inventory-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag fetches (2026-05-13, browser-style User-Agent, ~0.8s pacing) retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility).


### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x73bfc8b17296cb284b7b116e519c7b84df4e4020` | $0 | $3,783 | 0 / 2287 | 2023-11-14 → 2026-04-01 |
| 2 | `0x47ef949598e02b90ae2a38624f07b77c18fabb8b` | $0 | $3,413 | 0 / 2053 | 2023-11-14 → 2026-03-12 |
| 3 | `0xa370d3a30a125bb025501bf256eb6eab23d54c98` | $0 | $1,395 | 0 / 347 | 2023-10-31 → 2025-09-24 |
| 4 | `0x36f217d70c84c7362b82d8ef866cc8ffbd020fd1` | $0 | $918 | 0 / 345 | 2023-11-14 → 2025-09-23 |
| 5 | `0xf9d6b16bbf23cedc08846482d8cc5901b6b5d50c` | $0 | $783 | 0 / 516 | 2024-05-15 → 2026-04-03 |
| 6 | `0x3ef6683f2553af861f91194d23bdf8522d1f2eda` | $0 | $659 | 0 / 327 | 2023-11-14 → 2026-01-16 |
| 7 | `0x253dc804ac4f46b31e376466cac26843f2c19c3c` | $0 | $577 | 0 / 15 | 2024-03-20 → 2024-03-20 |
| 8 | `0xaad6825c2e63363adebbb79203d45b4ed0ac1862` | $0 | $479 | 0 / 196 | 2024-03-17 → 2024-12-09 |
| 9 | `0x4fc05911251b5bc1dbddb4788c92c19ccf67c8d2` | $0 | $466 | 0 / 122 | 2023-10-31 → 2025-10-19 |
| 10 | `0x0c31084d8752b7d9a7300c29d1b28860c215e598` | $0 | $426 | 0 / 170 | 2023-10-31 → 2026-03-30 |
| 11 | `0xacb419fd96df782752346c10a943c701a35e5262` | $0 | $382 | 0 / 19 | 2024-03-19 → 2025-01-20 |
| 12 | `0xd3b1ca9dfbb4acf1669c60bd8587122144295b73` | $0 | $381 | 0 / 169 | 2024-02-24 → 2025-10-19 |
| 13 | `0x70a9ffd5ccd90efd82b56e55ff7dc5511c809852` | $0 | $305 | 0 / 71 | 2023-11-14 → 2024-03-20 |
| 14 | `0x06fe84a27d583aaddcdcb5bffc965921da097999` | $0 | $300 | 0 / 34 | 2023-10-31 → 2026-03-29 |
| 15 | `0x03a7cedc4c0025a12fb1c6463236f975cb795783` | $0 | $295 | 0 / 7 | 2023-10-31 → 2024-12-13 |
| 16 | `0x4b209e06a2eb8c718a5dda726e4f6395769c7b8e` | $0 | $289 | 0 / 4 | 2023-10-31 → 2024-11-22 |
| 17 | `0xa0ed8da6da0886c45f24e4955e615baf23e663d6` | $0 | $288 | 0 / 2 | 2023-10-31 → 2025-07-30 |
| 18 | `0x14b7d29736a198abd6f41f3b2b77636f46f4e1ef` | $0 | $284 | 0 / 3 | 2023-10-31 → 2024-12-31 |
| 19 | `0x8c08db9403ac861f8ff423be82bb7565f34ba421` | $0 | $280 | 0 / 2 | 2023-10-31 → 2024-09-12 |
| 20 | `0x4063d560015ae3dc1f0832d938443f4a14005eec` | $0 | $279 | 0 / 2 | 2023-10-31 → 2025-04-28 |
| 21 | `0xaba3172d00f0ecc13c612c67d4f63df88b7c1874` | $0 | $275 | 0 / 9 | 2023-10-31 → 2025-01-31 |
| 22 | `0x2ce5f44c5806ae461c0bd6798dcbd045ceb93517` | $0 | $271 | 0 / 2 | 2023-10-31 → 2026-03-31 |
| 23 | `0x573318bf1ebe3eece9ad6777188d6c9dea35de47` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 24 | `0xc3543e6b2dfd04e3995f5ba50023bff0b2a1fdcb` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 25 | `0xf64f71ca5fbb3784d339d39f142320804bdca29b` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 26 | `0x6dca8e11936aabdb8b226fc92ffea1b734d59e3a` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 27 | `0x612f0967467da5e33aa9197ca22fb4962c9d0353` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 28 | `0xaa5aef58786c77d207c6ba1a5011632668e95df9` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 29 | `0x2b35342974e04620c345ca3b6529fd90ce53497d` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 30 | `0x3c05373432ca5bae03b23e2b2d8db1fc5bafd89f` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 31 | `0x419fe3c26a5b7ae9819f0239e4d046841113c806` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 32 | `0x2992531f8725b2375bd1c7fe988aaf4f1b59b7cc` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 33 | `0x360dea8a8d70b89835f2ee8d3f91a2eec3530faf` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 34 | `0x523d3006492c3f61ff40a7a361cbb923876c1ce6` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 35 | `0xb7b477ea423ac7de23bb718bb150e040044dcfe8` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 36 | `0x66a3694650d60135f15414204fab317c97c3e1e4` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 37 | `0xf4a533379349c2cda88bd0bdd1e80f7aaf051c5b` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 38 | `0xb21b192a757d8d59f694c0ec01930384f7650c52` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 39 | `0x347c5feaaada1d660e85762c138ba01d6916f1a4` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 40 | `0x71875bf350a87551c269c8a334ec97ac28eed48f` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 41 | `0x6410084514dfbc98cbec708a5abd98b5efdb7799` | $0 | $270 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 42 | `0x8076e2c90d7d260ec7d1f958ca7587e9a2a81f07` | $0 | $269 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 43 | `0x9036121b90cdc196e6952c4aa3362151981df48c` | $0 | $269 | 0 / 1 | 2023-10-31 → 2023-10-31 |
| 44 | `0x24f7fc80e37a6d69a492bc86de3662951d549783` | $0 | $180 | 0 / 25 | 2024-03-20 → 2025-05-20 |
| 45 | `0x057d2890018e5cb7efdde1c9c6c042d19b67a4f4` | $0 | $157 | 0 / 28 | 2024-03-20 → 2024-12-17 |
| 46 | `0x7b464929a7c7c9f59335211a0f699667322b4f14` | $0 | $144 | 0 / 66 | 2023-11-14 → 2025-11-05 |
| 47 | `0xdc9eb2d46e171b548d8546532a810c920fbbcf60` | $0 | $141 | 0 / 6 | 2024-05-28 → 2024-05-28 |
| 48 | `0x069418cbe8910c041c060960e0cc81227646e3e3` | $0 | $127 | 0 / 324 | 2025-03-04 → 2026-03-19 |
| 49 | `0x503dd7a29505fc4673a3144895f75fb0868f0a21` | $0 | $124 | 0 / 16 | 2024-03-20 → 2024-03-20 |
| 50 | `0x90d6fcaffaccbcf54da4c93983a6a62c55b54c04` | $0 | $118 | 0 / 16 | 2023-11-21 → 2024-03-20 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-deposit-funder-1-counterparties.csv`](zonda-deposit-funder-1-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503

[^1]: Etherscan, public name tag "Zonda: Deposit Funder 1". https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda Gas Supplier 1"`, `added_date="2024-10-06"`. https://dune.com/queries/3237025

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x8894e0a0c962cb723c1976a4421c95949be2d4e3` | Binance 51 | $0 | $0 | 1 / 0 |
| `0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43` | Coinbase 10 | $0 | $0 | 1 / 0 |
| `0xf977814e90da44bfa03b6295a0616a897441acec` | Binance 8 | $0 | $0 | 1 / 0 |

