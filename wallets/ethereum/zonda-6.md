# Zonda 6

**Address:** `0xd388009f01bbe5e6d2cb6ba8525ca50b56308046`

**Chain:** Ethereum.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

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
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
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

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $46,323,884 | $60,916,235 | 216 |
| Zonda 2 `0x781229c7…57fc` | $1,207,505 | $0 | 1 |
| Zonda Deposit Funder 1 `0x5bff49ee…9503` | $500,662 | $0 | 1 |

### External destinations — confirmed via Etherscan public name tags
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

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 6 of the 20 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$5,911,400 outbound** and **$4,602,015 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x0000000000000000000000000000000000000000` | $43,050,099 | $0 | 198 / 0 | 2025-04-01 → 2026-01-14 |
| 2 | `0x5307402e7c38cdbfd9a8bc7e9c68669faf29bbad` | $0 | $4,559,306 | 0 / 9 | 2024-07-18 → 2025-04-07 |
| 3 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $4,109,963 | $0 | 5 / 0 | 2024-07-22 → 2025-06-02 |
| 4 | `0x1646a4761aa54f23d7f4d5deb5d393f67d318b80` | $0 | $999,197 | 0 / 5 | 2024-12-20 → 2024-12-27 |
| 5 | `0x67a3512401e418aa3121088ba33fe20db5e7080f` | $354,276 | $351,847 | 10 / 8 | 2025-09-05 → 2025-09-16 |
| 6 | `0x664d2f142cbc89ee9ed20c8e4eeb66c63b9ce663` | $137,776 | $0 | 4 / 0 | 2024-07-02 → 2024-07-02 |
| 7 | `0x436a22ed5fda7e071b3f83f08bdc7f4779024349` | $0 | $1,050 | 0 / 1 | 2026-02-06 → 2026-02-06 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0xd388009f01bbe5e6d2cb6ba8525ca50b56308046

[^1]: Etherscan, public name tag on Zonda 6. https://etherscan.io/address/0xd388009f01bbe5e6d2cb6ba8525ca50b56308046
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
