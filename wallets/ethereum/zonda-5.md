# Zonda 5

**Address:** `0x6edf968da408a9640b8865826429a977a11c5048`

**Chains:** Ethereum, Polygon, Optimism, BSC, Base. The same private key is in use on all five.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

## Attribution

Each of the five major EVM block explorers — Etherscan, PolygonScan, OP Etherscan, BscScan, BaseScan — carries the public name tag "Zonda 5 (Exchange)" on this address.[^1][^2][^3][^4][^5] The label set is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^6] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "Zonda (BitBay)" under the EXCHANGE category.[^7]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-09 (block 12204789); most recent 2026-04-19 (block 24916463); ≥ 10,000 events.
- ERC-20 events: first 2021-04-13 (block 12231426); most recent 2026-05-12 (block 25075921); ≥ 10,000 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2023-08-02 (block 45812984); most recent 2026-04-12 (block 85448141); ≥ 10,000 events.
- ERC-20 events: first 2021-08-08 (block 17763572); most recent 2026-04-10 (block 85349476); ≥ 10,000 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unidentified** otherwise. See [methodology](../methodology.md#flow-profile) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $995,891,634 |
| Gross OUT (USD-equivalent at tx time) | $993,970,893 |
| Total throughput (gross in + out) | $1,989,862,528 |
| Net direction | +$1,920,741 |
| Total events ≥$1k | 98,811 |
| Distinct external counterparties (≥$1k cumulative) | 37,490 |
| Identified counterparties in this section | 5 internal + 14 external (Etherscan-tagged) |
| Counterparties without a public name tag | **37,476, aggregating ~$382,972,008 outbound and ~$584,969,109 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2021-04-09 → 2026-04-19 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13 saved to `case/sources/etherscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 2 `0x781229c7…57fc` | $161,301,730 | $158,659,179 | 488 |
| Zonda 6 `0xd388009f…8046` | $60,769,348 | $46,187,357 | 213 |
| BitBay 879882 `0x879882c5…b54f` | $4,299,650 | $0 | 278 |
| BitBay 3f1eea `0x3f1eea8d…0539` | $0 | $995,620 | 11 |
| Zonda Deposit Funder 1 `0x5bff49ee…9503` | $0 | $500,780 | 1 |

### External destinations — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--|--|
| `0x7ff423f8…4c76` | Binance Deposit: 0x7fF423F83622434edC4Eb3eA8212394a115e4C76 | $34,446,762 | 1,022 |
| `0x48e77e08…296b` | Binance Deposit: 0x48e77E0892972e420034e928060293288B32296b | $18,696,420 | 497 |
| `0x558b6d62…07c9` | Binance Deposit: 0x558b6d6258462E78907F14EA7402f52f1CD807C9 | $15,010,490 | 140 |
| `0x61620b28…d24f` | Binance Deposit: 0x61620b28C86ae7D3C9A1b39b38c4147FAA9FD24f | $9,641,354 | 540 |
| `0x22b8cc8c…3529` | Binance Deposit: 0x22b8cc8Cf448b7ED9f5ac1eE0446508461493529 | $8,308,298 | 530 |
| `0x088ae43b…b519` | Binance Deposit: 0x088Ae43BE934bA729d8D841b41649c4d417bb519 | $8,250,317 | 182 |
| `0xf1618ff2…fe6a` | Gate Deposit: 0xf1618ff2d8038015f401b22e3ba78cd8b67ffe6a | $8,049,973 | 85 |
| `0x71959d55…dcc0` | Binance Deposit: 0x71959d556b7a50287bb669990791f1EB09a4DCc0 | $6,624,187 | 376 |
| `0x15359093…ddf6` | Binance Deposit: 0x1535909303174e7a235C33814d1B1a359b76ddf6 | $5,933,213 | 385 |
| `0x8a63afd3…25b5` | Binance Deposit: 0x8a63AFd33e0d05274B3B6650486D9960785025B5 | $4,921,622 | 275 |
| `0xfae79cff…a9ae` | Binance Deposit: 0xfAe79cFFdFF6893e772940ec4e0CAF36c037a9Ae | $4,127,237 | 56 |
| `0x1936d385…f057` | Binance Deposit: 0x1936d3853c9b7BCf4c3a4105B59D9eFb7984F057 | $3,844,937 | 206 |
| `0x2f9378d5…2aa5` | Binance Deposit: 0x2F9378D573b20199105bCaF6D103Ac88d5442aA5 | $2,166,251 | 13 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0xae2d4617…673f` | Kraken 10 | $400,154 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 37,476 of the 37,495 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$382,972,008 outbound** and **$584,969,109 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 10 unattributed counterparties by gross USD

These are the largest counterparties in the top-500 slice that carry no public name tag on Etherscan and are not in this inventory's roster. Listed here so future verification and any reader's own attribution work can start from the addresses, not from filtered output.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x3ef6683f2553af861f91194d23bdf8522d1f2eda` | $119,457,636 | $0 | 657 / 0 | 2023-05-31 → 2026-01-16 |
| 2 | `0xf9793f372c9aa841f8916f0d3c480d18a9cda72d` | $0 | $46,317,565 | 0 / 244 | 2024-02-27 → 2025-12-15 |
| 3 | `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06` | $43,668,284 | $0 | 212 / 0 | 2022-08-31 → 2024-11-15 |
| 4 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $0 | $42,514,342 | 0 / 98 | 2024-03-28 → 2026-01-10 |
| 5 | `0xa370d3a30a125bb025501bf256eb6eab23d54c98` | $42,177,017 | $0 | 806 / 0 | 2022-12-15 → 2024-11-21 |
| 6 | `0xaad6825c2e63363adebbb79203d45b4ed0ac1862` | $27,273,722 | $0 | 719 / 0 | 2022-12-07 → 2026-02-23 |
| 7 | `0x70a9ffd5ccd90efd82b56e55ff7dc5511c809852` | $23,892,427 | $0 | 154 / 0 | 2022-05-10 → 2024-11-22 |
| 8 | `0x73bfc8b17296cb284b7b116e519c7b84df4e4020` | $20,710,520 | $0 | 1148 / 0 | 2021-06-14 → 2026-03-06 |
| 9 | `0xd3b1ca9dfbb4acf1669c60bd8587122144295b73` | $19,423,422 | $0 | 493 / 0 | 2021-11-14 → 2026-01-11 |
| 10 | `0xb7777ac291408554b0e3fedbe79d7675ac962af8` | $18,799,767 | $0 | 376 / 0 | 2025-12-18 → 2026-04-10 |

**Receipts (for reproduction)**:
- Dune partitioned top-500-per-wallet aggregation: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290, execution `01KRGHZZ2F15AC6PH4PQ2C8AMB`).
- Dune per-wallet totals + distinct-counterparty count (≥$1k cumulative): `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json` (query 7491746) and `case/sources/dune/stage1-distinct-cp-ge1k-2026-05-13.json` (query 7491752).
- Etherscan HTML name-tag receipts: `case/sources/etherscan-name-tags-2026-05-13/<addr>.html` (fetched 2026-05-13 with browser-style User-Agent, ~0.8s pacing).


# Zonda 5 — multichain empty-set note (append to scouting/wallets/ethereum/zonda-5.md)

## Multichain footprint — probed-and-empty chains (2026-05-13)

Beyond Ethereum and Polygon (both ACTIVE — see flow profiles in this file), Zonda 5's multichain footprint has been independently probed and found empty on every other EVM chain it carries an attribution claim on. The same EVM key (`0x6edf968d…5048`) is empty on:

| Chain | Result | Method | Receipt |
|--|--|--|--|
| Optimism | EMPTY (0 events in the most recent 100,000 blocks scanned) | Archive RPC `eth_getLogs` over rolling 100k-block window | `case/sources/zonda5-multichain/op-base/optimism-{in,out}-100k.json` |
| Base | EMPTY (0 events in the most recent 100,000 blocks scanned) | Archive RPC `eth_getLogs` | `case/sources/zonda5-multichain/op-base/base-{in,out}-100k.json` |
| Avalanche C-chain | EMPTY (0 events in 100,000 blocks) | Archive RPC `eth_getLogs` | `case/sources/zonda5-multichain/avax-c-*` (see cross-chain probe matrix) |
| BSC | EMPTY (0 events / 10×10k chunks) | Archive RPC `eth_getLogs` | `case/sources/zonda5-multichain/bsc-*` |
| zkSync Era | UNPROBED for this key (only the F-005 institutional address was zkSync-probed; deferred) | — | — |
| Tron (native + TRX_EVM_RPC) | EMPTY (zero balance + zero txs) | Tronscan API + TRX_EVM_RPC | `case/sources/zonda5-multichain/tron-*` |

The "BSC / Optimism / Base" annotation that appears on this page above for Zonda 5 reflects same-key cross-chain availability of the EOA, not active flow on those chains: the most-recent-window probes return zero events. Historical pre-2024 BSC activity has not been ruled in or out by these recent-window probes; a deeper backward chunked scan is queued in the case's `STAGE-2-QUEUE.md` but has not been run.

**Confidence:** CONFIRMED-empty on the recent-window probes shown above. The longer-history BSC question remains UNPROBED.

## Flow profile (Polygon, Dune-aggregated 2026-05-13)

Full-history aggregation built from Dune `tokens_polygon.transfers` (≥$1,000 USD-equivalent per event). See [methodology](../methodology.md#flow-profile) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $133,447,101 |
| Gross OUT (USD-equivalent at tx time) | $131,913,325 |
| Total throughput | $265,360,426 |
| Net direction | +$1,533,776 |
| Total events ≥$1k | 8,021 |
| Distinct external counterparties (≥$1k cumulative) | 1,677 |
| Identified counterparties in this section | 3 internal + 0 external (PolygonScan-tagged) |
| Counterparties without a public name tag | **1,677, aggregating ~$57,787,733 outbound and ~$99,832,276 inbound across captured rows** |
| Active period | 2023-11-22 → 2026-04-09 |

**Confidence:** CONFIRMED on totals. CONFIRMED on Internal and External-tagged rows below (each PolygonScan tag verified by fresh HTML fetch on 2026-05-13 saved to `case/sources/polygonscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 6 `0xd388009f…8046` | $13,614,690 | $57,282,318 | 159 |
| Zonda 2 `0x781229c7…57fc` | $10,812,322 | $11,723,827 | 49 |
| BitBay 879882 `0x879882c5…b54f` | $6,914,650 | $0 | 544 |

### Unidentified counterparties

**This section is a known incomplete part of the analysis.** 1,677 of the 1,680 Polygon counterparties with ≥$1k cumulative flow carry no PolygonScan public name tag as of 2026-05-13 and do not appear in this inventory's roster. The unidentified rows captured here aggregate **$57,787,733 outbound** and **$99,832,276 inbound**. Entity-attribution work on these counterparties is ongoing.

**Receipts**: `case/sources/dune/polygon-per-wallet-2026-05-13.json` (query 7491823) + `case/sources/dune/polygon-totals-2026-05-13.json` (query 7491829) + `case/sources/polygonscan-name-tags-2026-05-13/<addr>.html`.

## Block-explorer links

- Ethereum: https://etherscan.io/address/0x6edf968da408a9640b8865826429a977a11c5048
- Polygon: https://polygonscan.com/address/0x6edf968da408a9640b8865826429a977a11c5048
- Optimism: https://optimistic.etherscan.io/address/0x6edf968da408a9640b8865826429a977a11c5048
- BSC: https://bscscan.com/address/0x6edf968da408a9640b8865826429a977a11c5048
- Base: https://basescan.org/address/0x6edf968da408a9640b8865826429a977a11c5048

[^1]: Etherscan, public name tag on Zonda 5. https://etherscan.io/address/0x6edf968da408a9640b8865826429a977a11c5048
[^2]: PolygonScan, public name tag on Zonda 5. https://polygonscan.com/address/0x6edf968da408a9640b8865826429a977a11c5048
[^3]: OP Etherscan, public name tag on Zonda 5. https://optimistic.etherscan.io/address/0x6edf968da408a9640b8865826429a977a11c5048
[^4]: BscScan, public name tag on Zonda 5. https://bscscan.com/address/0x6edf968da408a9640b8865826429a977a11c5048
[^5]: BaseScan, public name tag on Zonda 5. https://basescan.org/address/0x6edf968da408a9640b8865826429a977a11c5048
[^6]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^7]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
