# Zonda (BitBay) (0x879882…b54f)

> **Plain-language summary.** An Ethereum wallet attributed to ZondaCrypto / BitBay by Bubblemaps' `entity_id = "zonda"` label. Single primary source — recorded as PARTIAL tier pending a second independent labelling. Active since March 2021. Top-100 ZND holder at 0.0119% of supply. Underlying transfers are CONFIRMED from on-chain data; their attribution to ZondaCrypto operations inherits the wallet's PARTIAL tier. On Polygon, Arbitrum, and Optimism this address shows a distinctive single-counterparty-per-chain outbound pattern: in each of the three L2s, the single recipient is the same EVM address, `0x6edf968d…5048` — the canonical Zonda 5 multichain key, BlockSec-confirmed on POL and ARB on 2026-05-21 (see [Multichain section](#multichain-pattern--single-recipient-per-chain-is-zonda-5)). Read literally on the on-chain graph, the L2 OUT activity from this address is an intra-inventory rotation feeder into Zonda 5, not an external CEX-customer aggregator.

**Address:** `0x879882c59d9cc548d6c0e7d0238e8aa40858b54f`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps.

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Bubblemaps' `addresses/token-top-holders` endpoint for the ZND token returns this address with `label = "Zonda (BitBay) (0x87…B54F)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

The address is a top-100 ZND holder at 0.0119% of supply.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-28 (block 12327290); most recent 2026-04-02 (block 24792762); 1,259 events.
- ERC-20 events: first 2021-03-31 (block 12147725); most recent 2026-04-02 (block 24792762); 2,112 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

**PARTIAL — wallet attribution itself is at PARTIAL tier;** flow data below is CONFIRMED from on-chain transfers, but the link of these flows to ZondaCrypto operations rests on the wallet's PARTIAL attribution.
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $4,878,528 |
| Gross OUT (USD-equivalent at tx time) | $4,926,877 |
| Total throughput (gross in + out) | $9,805,405 |
| Net direction | −$48,349 |
| Total events ≥$1k | 967 |
| Distinct external counterparties (≥$1k cumulative) | 17 |
| Identified counterparties in this section | 1 internal + 14 external (Etherscan-tagged) |
| Counterparties without a public name tag | **3, aggregating ~$0 outbound and ~$31,500 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-03-31 → 2026-03-27 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $4,926,877 | 417 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x28c6c062…1d60` | Binance 14 | $1,715,594 | 197 |
| `0xdfd5293d…963d` | Binance 16 | $1,307,062 | 150 |
| `0x21a31ee1…5549` | Binance 15 | $1,267,205 | 161 |
| `0x9696f59e…6976` | Binance 18 | $312,919 | 15 |
| `0x56eddb7a…b17f` | Binance 17 | $124,754 | 8 |
| `0xee7ae85f…4055` | Binance: Hot Wallet 34 | $39,766 | 3 |
| `0x85b931a3…d69b` | Binance 10 | $15,490 | 2 |
| `0x56428636…aced` | Binance 3 | $15,395 | 1 |
| `0x42d17b7f…e2cd` | Kanga Exchange 1 | $13,053 | 2 |
| `0x3f5ce5fb…f0be` | Binance | $9,759 | 1 |

<details><summary>Show 4 more rows</summary>

| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0681d8db…dbbf` | Binance 4 | $9,587 | 1 |
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $7,483 | 1 |
| `0xb8001c3e…1ec1` | Cobo: Custody 1 | $4,984 | 2 |
| `0xc2ba04e8…4793` | Bidesk 14 | $3,976 | 1 |

</details>

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 3 of the 18 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$31,500 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xa7512a0d9cc166ff05eb79f3a52095eab114b856` | $29,845 | $0 | 5 / 0 | 2021-06-15 → 2021-07-01 |
| 2 | `0x7bd8efab672250de65ba4ba3bc6c3aa08120a1c3` | $1,687 | $0 | 1 / 0 | 2021-06-16 → 2021-06-16 |
| 3 | `0x5bffc3e304072d8d89335475b5201bd32ac69503` | $0 | $0 | 1 / 0 | 2026-01-14 → 2026-01-14 |
| 4 | `0x6edffd3c53ce226b0b16fbe960e2d69af31c5048` | $0 | $0 | 2 / 0 | 2025-01-14 → 2025-02-05 |
| 5 | `0x9e0d5185791ba456bd4bf32968afc3d805c13adc` | $0 | $0 | 1 / 0 | 2026-03-27 → 2026-03-27 |
| 6 | `0x40f0181e48b8f81ce1a2968eb4573d15d42a3d13` | $0 | $0 | 1 / 0 | 2025-11-02 → 2025-11-02 |
| 7 | `0xd152f549545093347a162dce210e7293f1452150` | $0 | $0 | 1 / 0 | 2024-03-16 → 2024-03-16 |
| 8 | `0x8c8ee12c274d2372890f3ff03e3771cf25ae4327` | $0 | $0 | 1 / 0 | 2025-11-02 → 2025-11-02 |
| 9 | `0x5a1195f555c487f044a777dd39938a1ea37b7aa3` | $0 | $0 | 1 / 0 | 2025-10-28 → 2025-10-28 |
| 10 | `0xf7cede6cb21f73ca4a502a731daf3d2e41bd44cb` | $0 | $0 | 1 / 0 | 2024-04-25 → 2024-04-25 |

<details><summary>Show 12 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0xd5050910347ecaf024421bc5e8f2b2e2e12ea8cb` | $0 | $0 | 1 / 0 | 2024-04-04 → 2024-04-04 |
| 12 | `0x82dfdb2ec1aa6003ed4acba663403d7c2127ff67` | $0 | $0 | 1 / 0 | 2021-09-11 → 2021-09-11 |
| 13 | `0x6ed0faa6fa60392119d5bef42a86bb3822b85048` | $0 | $0 | 0 / 1 | 2023-02-18 → 2023-02-18 |
| 14 | `0x7fc66500c84a76ad7e9c93437bfc5ac33e2ddae9` | $0 | $0 | 2 / 0 | 2024-01-12 → 2024-01-28 |
| 15 | `0x6357d3843d715496257e338a878ab0b72040a918` | $0 | $0 | 1 / 0 | 2026-04-02 → 2026-04-02 |
| 16 | `0xd55210bb6898c021a19de1f58d27b71f095921ee` | $0 | $0 | 1 / 0 | 2024-03-31 → 2024-03-31 |
| 17 | `0x5bff47025d5c87c6b51d0cccfb3de2e1e2499503` | $0 | $0 | 1 / 0 | 2026-01-14 → 2026-01-14 |
| 18 | `0xabc029ff1649b5e764dd28a9e48b1cf716ef225f` | $0 | $0 | 1 / 0 | 2024-06-29 → 2024-06-29 |
| 19 | `0x967da4048cd07ab37855c090aaf366e4ce1b9f48` | $0 | $0 | 2 / 0 | 2023-12-24 → 2024-01-24 |
| 20 | `0xbbcd44263236dfbf8e4705a4eb58226671d74c5e` | $0 | $0 | 1 / 0 | 2026-03-27 → 2026-03-27 |
| 21 | `0xaea46a60368a7bd060eec7df8cba43b7ef41ad85` | $0 | $0 | 1 / 0 | 2024-01-24 → 2024-01-24 |
| 22 | `0x6982508145454ce325ddbe47a25d4ec3d2311933` | $0 | $0 | 2 / 0 | 2024-03-06 → 2024-03-30 |

</details>
## Multichain pattern — single recipient per chain is Zonda 5

Beyond Ethereum, this address transacts on Polygon, Arbitrum, and Optimism. Per a 2026-05-21 Dune re-enumeration over `tokens_<chain>.transfers` (≥$1 USD-equivalent hygiene filter to exclude zero-USD address-poisoner artefacts), the OUT side on each of the three L2s reduces to a single counterparty, and that counterparty is the same EVM address on all three chains:

| Chain | OUT counterparty | Events | Total USD |
|---|---|---:|---:|
| Polygon | `0x6edf968da408a9640b8865826429a977a11c5048` (Zonda 5) | 668 | $6,975,974 |
| Arbitrum | `0x6edf968da408a9640b8865826429a977a11c5048` (Zonda 5) | 189 | $1,567,386 |
| Optimism | `0x6edf968da408a9640b8865826429a977a11c5048` (Zonda 5) | 132 | $1,399,938 |

The recipient address `0x6edf968d…5048` is the canonical Zonda 5 EVM key. It carries primary attribution as `Zonda 5 (Exchange)` on Etherscan / PolygonScan / OP Etherscan / BscScan / BaseScan (see [`zonda-5`](zonda-5.md)) and a primary BlockSec MetaSleuth attribution as `Zonda (BitBay)` on Ethereum (2026-05-12), Polygon (2026-05-21), and Arbitrum (2026-05-21). On the on-chain graph, the L2 OUT side of this address therefore points exclusively at another address in this inventory.

**Confidence.** CONFIRMED on the per-chain magnitudes (direct Dune aggregation; receipt mirrored at [`../../sources/dune/d6f-bb879882-cps-2026-05-21.json`](../../sources/dune/d6f-bb879882-cps-2026-05-21.json)). CONFIRMED on the recipient identity (recipient is an already-attributed inventory address, primary-cited on POL + ARB by BlockSec 2026-05-21; receipt [`../../sources/blocksec/labels-2026-05-21.json`](../../sources/blocksec/labels-2026-05-21.json)). The Ethereum-side aggregate magnitudes for this address (POL $14.0M / ARB $3.1M / OP $2.8M) are mirrored at [`../../sources/dune/d6-multichain-reenum-2026-05-21.json`](../../sources/dune/d6-multichain-reenum-2026-05-21.json).

**Pattern note.** A one-counterparty-per-chain OUT shape, in isolation, is consistent with multiple structural readings (single CEX-customer-deposit aggregator; single MM/OTC settlement counterparty; intra-operator multichain rotation hop). Hex-matching the recipient against the existing inventory disambiguates: the recipient is Zonda 5, already in this inventory, primary-cited as a Zonda-operated exchange wallet — therefore an external-customer-aggregator reading is not supported by the address itself.

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-bitbay-879882-counterparties.csv`](zonda-bitbay-879882-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x879882c59d9cc548d6c0e7d0238e8aa40858b54f

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x28c6c06298d514db089934071355e5743bf21d60` | Binance 14 | $1,750,353 | $0 | 279 / 0 |
| `0xdfd5293d8e347dfe59e90efd55b2956a1343963d` | Binance 16 | $1,336,611 | $0 | 237 / 0 |
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $1,302,841 | $0 | 254 / 0 |
| `0x9696f59e4d72e237be84ffd425dcad154bf96976` | Binance 18 | $312,919 | $0 | 15 / 0 |
| `0x56eddb7aa87536c09ccc2793473599fd21a8b17f` | Binance 17 | $124,754 | $0 | 8 / 0 |
| `0x85b931a32a0725be14285b66f1a22178c672d69b` | Binance 10 | $15,490 | $0 | 2 / 0 |
| `0x564286362092d8e7936f0549571a803b203aaced` | Binance 3 | $15,395 | $0 | 1 / 0 |
| `0x42d17b7f3532ec2f7c4e4e5e239baa476846e2cd` | Kanga Exchange 1 | $13,636 | $0 | 3 / 0 |
| `0x3f5ce5fbfe3e9af3971dd833d26ba9b5c936f0be` | Binance 1 | $9,759 | $0 | 1 / 0 |
| `0x0681d8db095565fe8a346fa0277bffde9c0edbbf` | Binance 4 | $9,587 | $0 | 1 / 0 |

<details><summary>Show 7 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x0d0707963952f2fba59dd06f2b425ace40b492fe` | Gate.io 1 | $7,483 | $0 | 392 / 0 |
| `0xb8001c3ec9aa1985f6c747e25c28324e4a361ec1` | Cobo 6 | $4,984 | $0 | 2 / 0 |
| `0xc2ba04e89016f417e1219af7ef82a5b6a9214793` | Bidesk 14 | $3,976 | $0 | 1 / 0 |
| `0x708396f17127c42383e3b9014072679b2f60b82f` | Binance 11 | $993 | $0 | 1 / 0 |
| `0x2b3bf74b29f59fb8dda41cf3d6a8da28cf8e7921` | BingX 20 | $0 | $0 | 1 / 0 |
| `0x9642b23ed1e01df1092b92641051881a322f5d4e` | MEXC 21 | $0 | $0 | 51 / 0 |
| `0x6d0d19bdddc5ed1dd501430c9621dd37ebd9062d` | BitMart 13 | $0 | $0 | 6 / 0 |

</details>

