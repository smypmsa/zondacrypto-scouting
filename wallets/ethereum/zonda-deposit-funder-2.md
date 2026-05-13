# Zonda Deposit Funder 2

**Address:** `0x818ab3c61f66e975b8e6290c20999d6749f60d8d`

**Chain:** Ethereum.

**Role:** ZondaCrypto deposit-funder / gas-supplier wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda: Deposit Funder 2" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses on Dune Analytics (entry added 2024-10-06 as "Zonda Gas Supplier 2").[^2] The receipt of the Dune query result is preserved at [`sources/dune/hildobby-3237025-zonda-rows.json`](../../sources/dune/hildobby-3237025-zonda-rows.json).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-12 (block 12223728); most recent 2023-11-06 (block 18515362); ≥ 10,000 events.
- ERC-20 events: first 2021-09-11 (block 13205595); most recent 2023-10-19 (block 18383438); 15 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $401,221 |
| Gross OUT (USD-equivalent at tx time) | $0 |
| Total throughput (gross in + out) | $401,221 |
| Net direction | +$401,221 |
| Total events ≥$1k | 32 |
| Distinct external counterparties (≥$1k cumulative) | 11 |
| Identified counterparties in this section | 3 internal + 0 external (Etherscan-tagged) |
| Counterparties without a public name tag | **11, aggregating ~$0 outbound and ~$0 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-04-12 → 2023-10-19 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $228,347 | $0 | 22 |
| Zonda 1 `0xf646cbe3…b95e` | $99,267 | $0 | 6 |
| Zonda 4 `0x2b645268…763a` | $73,606 | $0 | 4 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 11 of the 14 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$0 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


## Block-explorer link

https://etherscan.io/address/0x818ab3c61f66e975b8e6290c20999d6749f60d8d

[^1]: Etherscan, public name tag "Zonda: Deposit Funder 2". https://etherscan.io/address/0x818ab3c61f66e975b8e6290c20999d6749f60d8d
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda Gas Supplier 2"`, `added_date="2024-10-06"`. https://dune.com/queries/3237025
