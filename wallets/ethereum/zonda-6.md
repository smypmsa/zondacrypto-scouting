# Zonda 6

> **Plain-language summary.** A ZondaCrypto exchange wallet on Ethereum and Polygon, attributed by Etherscan public name tag plus the hildobby CEX-address compilation. Active since 2023-10. Observed Ethereum throughput is $219.2 million across 746 events above $1,000 USD; Zonda 5 is the dominant counterparty on both sides of the ledger. The Polygon side is documented in a related cluster file (the `0xd388…8046` vanity-suffix family).

**Address:** `0xd388009f01bbe5e6d2cb6ba8525ca50b56308046`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan carries the public name tag "Zonda 6 (Exchange)" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2023-10-25 (block 18426326); most recent 2026-03-25 (block 24735249); 830 events.
- ERC-20 events: first 2023-10-25 (block 18426511); most recent 2026-03-29 (block 24762181); 1,217 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2023-10-30 (block 49334959); most recent 2026-03-25 (block 84664939); 575 events.
- ERC-20 events: first 2023-10-31 (block 49362239); most recent 2026-01-14 (block 81623874); 3,123 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $109,635,364 |
| Gross OUT (USD-equivalent at tx time) | $109,575,231 |
| Total throughput (gross in + out) | $219,210,595 |
| Net direction | +$60,133 |
| Total events ≥$1k | 746 |
| Distinct external counterparties (≥$1k cumulative) | 17 |
| Identified counterparties in this section | 3 internal + 11 external (Etherscan-tagged) |
| Counterparties without a public name tag | **6, aggregating ~$5,911,400 outbound and ~$4,602,015 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2023-11-22 → 2026-02-06 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $46,323,884 | $60,916,235 | 216 |
| Zonda 2 `0x781229c7…57fc` | $1,207,505 | $0 | 1 |
| Zonda Deposit Funder 1 `0x5bff49ee…9503` | $500,662 | $0 | 1 |

### External counterparties — confirmed via public name tag
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x4dbd4fc5…ab3f` | Arbitrum: Delayed Inbox | $15,944,744 | 54 |
| `0x99c9fc46…4be1` | Optimism: Gateway | $11,446,361 | 75 |
| `0xc4922d64…e907` | Circle: Token Minter | $4,159,173 | 30 |
| `0x401f6c98…188b` | Polygon (Matic): Plasma Bridge | $2,204,496 | 18 |
| `0x1231deb6…4eae` | LI.FI: LiFi Diamond | $2,028,335 | 8 |
| `0x3ee18b22…a585` | Wormhole: Token Bridge | $513,732 | 5 |
| `0x00000000…dead` | Null: 0x00...dEaD | $136,624 | 4 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x00000000…0000` | Null: 0x000...000 | $43,050,099 | 198 |
| `0x40ec5b33…bbdf` | Polygon (Matic): ERC20 Bridge | $13,474,783 | 56 |
| `0x8315177a…ed3a` | Arbitrum: Bridge | $50,891 | 1 |
| `0x29e7df7b…2c4e` | Polygon: POL Migrator | $10,140 | 3 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 6 of the 20 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$5,911,400 outbound** and **$4,602,015 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x5307402e7c38cdbfd9a8bc7e9c68669faf29bbad` | $0 | $4,559,406 | 0 / 10 | 2024-07-12 → 2025-04-07 |
| 2 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $4,110,063 | $0 | 6 / 0 | 2024-07-17 → 2025-06-02 |
| 3 | `0x1646a4761aa54f23d7f4d5deb5d393f67d318b80` | $0 | $999,214 | 0 / 10 | 2024-12-20 → 2024-12-27 |
| 4 | `0x67a3512401e418aa3121088ba33fe20db5e7080f` | $354,743 | $352,327 | 12 / 10 | 2025-09-05 → 2025-09-16 |
| 5 | `0x664d2f142cbc89ee9ed20c8e4eeb66c63b9ce663` | $137,834 | $0 | 5 / 0 | 2024-07-02 → 2024-07-02 |
| 6 | `0x436a22ed5fda7e071b3f83f08bdc7f4779024349` | $0 | $1,050 | 0 / 1 | 2026-02-06 → 2026-02-06 |
| 7 | `0x5c7bcd6e7de5423a257d81b442095a1a6ced35c5` | $0 | $812 | 0 / 1 | 2025-04-22 → 2025-04-22 |
| 8 | `0xc6d6c7c7fea0977174d0f0e7ea89b4dc185d62c2` | $399 | $0 | 2 / 0 | 2024-07-02 → 2024-07-02 |
| 9 | `0xa0c68c638235ee32657e8f720a23cec1bfc77c77` | $0 | $307 | 0 / 1 | 2025-01-27 → 2025-01-27 |
| 10 | `0x2f1d2754393356aea6334180da04bab84412d580` | $0 | $23 | 0 / 1 | 2024-12-13 → 2024-12-13 |
| 11 | `0x53071f6efcb2e88101c0d235a876492050c7bbad` | $0 | $0 | 1 / 5 | 2024-07-17 → 2024-07-20 |
| 12 | `0x6edffd3c53ce226b0b16fbe960e2d69af31c5048` | $0 | $0 | 4 / 0 | 2024-08-24 → 2025-03-05 |
| 13 | `0x53076912625517be665f27e49275a3a59529bbad` | $0 | $0 | 1 / 1 | 2024-09-18 → 2024-09-18 |
| 14 | `0x6edfed0777cab20ba8000f8e8fe4dbd0131c5048` | $0 | $0 | 1 / 1 | 2024-09-18 → 2024-09-18 |
| 15 | `0x6edf026c1ac3da32efc61f1de4ed3cf6190c5048` | $0 | $0 | 1 / 1 | 2024-07-22 → 2024-08-02 |
| 16 | `0x6edfaa7b010b3e2857f17b99be4469b9f24e5048` | $0 | $0 | 2 / 63 | 2025-05-16 → 2025-06-30 |
| 17 | `0x6edfbb24b2ec600e84a9f7866a5cde39e4c15048` | $0 | $0 | 1 / 0 | 2025-08-25 → 2025-08-25 |
| 18 | `0x53073cf61b6662a38a4aaee51cb4c6389a29bbad` | $0 | $0 | 1 / 0 | 2024-09-13 → 2024-09-13 |
| 19 | `0x6edf2527128b94b0c93ec23123772dd4fcf95048` | $0 | $0 | 10 / 37 | 2025-05-16 → 2026-01-14 |
| 20 | `0x53075c1cd19d6b9fe5cb702c6a3fd2480e24bbad` | $0 | $0 | 1 / 9 | 2024-07-17 → 2025-04-25 |
| 21 | `0x70fffd5ab47c36db7c85f771068497033d5523fd` | $0 | $0 | 1 / 0 | 2025-10-06 → 2025-10-06 |
| 22 | `0x67a83c055becf4ef3e0299b64d13761a8112080f` | $0 | $0 | 0 / 1 | 2025-09-17 → 2025-09-17 |
| 23 | `0x6ed38ac0dd5f316042ee2418fb0e98b7591c5048` | $0 | $0 | 0 / 67 | 2025-06-17 → 2025-12-31 |
| 24 | `0xb62d08519a7cc5cbebee997468a7ee5546e89931` | $0 | $0 | 1 / 0 | 2025-09-10 → 2025-09-10 |
| 25 | `0x695e449525d42055d368f84e97912032c7410a46` | $0 | $0 | 1 / 0 | 2026-01-05 → 2026-01-05 |
| 26 | `0x6edf7d6a3d9eb2ed68388f1cd92a976068b75048` | $0 | $0 | 2 / 11 | 2024-08-30 → 2025-04-24 |
| 27 | `0x6edfd7e0cd88149b7cbc83e946e4b084269d5048` | $0 | $0 | 7 / 0 | 2025-12-31 → 2026-01-14 |
| 28 | `0xfa6d07fb903fe51f1a3a6357791f1de49deeb2e3` | $0 | $0 | 1 / 0 | 2025-09-04 → 2025-09-04 |
| 29 | `0x7ae02b81f6f0bb03cd71b52aecce2f97f1771623` | $0 | $0 | 1 / 0 | 2024-07-25 → 2024-07-25 |
| 30 | `0x10d280e9f1c91c84fa1a1f03c1b247c198822a0d` | $0 | $0 | 1 / 0 | 2025-09-04 → 2025-09-04 |
| 31 | `0x6edf000f0bf6b570103be8a3a03e83974cb05048` | $0 | $0 | 0 / 1 | 2025-07-17 → 2025-07-17 |
| 32 | `0xc9aa60d7d0fb88570d1673022fe458cb738bfe12` | $0 | $0 | 1 / 0 | 2025-12-12 → 2025-12-12 |
| 33 | `0x059b2051bc369a52dfa4bcbaa77388483279320c` | $0 | $0 | 1 / 0 | 2026-01-14 → 2026-01-14 |
| 34 | `0x3a9b127e87295d90ac0136eba0aaa39db185d341` | $0 | $0 | 1 / 0 | 2025-12-12 → 2025-12-12 |
| 35 | `0x67a39d4780f8de808cab3f00e3592d98e712080f` | $0 | $0 | 2 / 12 | 2025-09-16 → 2026-02-07 |
| 36 | `0x40ec5b32f29468a1fe1eb13ea54d4f264e5bbbdf` | $0 | $0 | 0 / 2 | 2024-04-15 → 2024-04-15 |
| 37 | `0xdc5cb57711ac6ea18bc9e07404a3fa2a9b4913e9` | $0 | $0 | 1 / 0 | 2025-11-24 → 2025-11-24 |
| 38 | `0xf8fb55139b9acac7bb72e3d6de9ab412e01d2528` | $0 | $0 | 1 / 0 | 2025-10-06 → 2025-10-06 |
| 39 | `0x73a15fed60bf67631dc6cd7bc5b6e8da8190acf5` | $0 | $0 | 1 / 0 | 2024-09-01 → 2024-09-01 |
| 40 | `0xdd0d0781fd0045ccb8c4f56ab4229a37f8e86e42` | $0 | $0 | 1 / 0 | 2025-12-02 → 2025-12-02 |
| 41 | `0xf644f3a54d2c2851f56cf36818c88d8bda5037d8` | $0 | $0 | 1 / 0 | 2026-01-05 → 2026-01-05 |
| 42 | `0x6edf2e9f3502a0142e316b1beefba15fd22d5048` | $0 | $0 | 0 / 44 | 2025-06-23 → 2026-02-07 |
| 43 | `0xbb057b406adfbf0930d71f8bac0413132e30bbc3` | $0 | $0 | 1 / 0 | 2025-09-04 → 2025-09-04 |
| 44 | `0xc93113accfb88fc1b7ab832e3d5395e883535691` | $0 | $0 | 1 / 0 | 2025-08-08 → 2025-08-08 |
| 45 | `0xcba360df45bbb3ddd97da98d4b26fc860ebc2d32` | $0 | $0 | 1 / 0 | 2025-12-03 → 2025-12-03 |
| 46 | `0xfffc1fd463d953422ef7b3e4f39ac8fcb6a93825` | $0 | $0 | 1 / 0 | 2025-12-03 → 2025-12-03 |
| 47 | `0xd83c7fdf9d76dec865a0501016439344b6a938f1` | $0 | $0 | 1 / 0 | 2025-09-04 → 2025-09-04 |
| 48 | `0x67a396a170cd44c5c124c9cc4135abbd35e7080f` | $0 | $0 | 0 / 5 | 2025-09-16 → 2025-09-23 |
| 49 | `0x692cd1cce74bfb88947a3e02f6993ce677d54638` | $0 | $0 | 1 / 0 | 2025-12-18 → 2025-12-18 |
| 50 | `0xb9d514814c1780c235e4b973d16210d917e32926` | $0 | $0 | 1 / 0 | 2025-11-15 → 2025-11-15 |
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-6-counterparties.csv`](zonda-6-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0xd388009f01bbe5e6d2cb6ba8525ca50b56308046

[^1]: Etherscan, public name tag on Zonda 6. https://etherscan.io/address/0xd388009f01bbe5e6d2cb6ba8525ca50b56308046
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
