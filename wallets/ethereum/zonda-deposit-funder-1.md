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

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $678,457 | $0 | 14 |
| Zonda 6 `0xd388009f…8046` | $0 | $500,662 | 1 |
| Zonda 2 `0x781229c7…57fc` | $0 | $6,641 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 3 of the 6 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503

[^1]: Etherscan, public name tag "Zonda: Deposit Funder 1". https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda Gas Supplier 1"`, `added_date="2024-10-06"`. https://dune.com/queries/3237025
