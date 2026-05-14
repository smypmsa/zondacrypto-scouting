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

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xae2d4617c862309a3d75a0ffb358c7a5009c673f` | Kraken 10 | $400,254 | $0 | 2 / 0 |
| `0x0d0707963952f2fba59dd06f2b425ace40b492fe` | Gate.io 1 | $262,646 | $0 | 4 / 0 |
| `0x56eddb7aa87536c09ccc2793473599fd21a8b17f` | Binance 17 | $0 | $400 | 0 / 1 |
| `0xdfd5293d8e347dfe59e90efd55b2956a1343963d` | Binance 16 | $0 | $297 | 0 / 1 |
| `0x28c6c06298d514db089934071355e5743bf21d60` | Binance 14 | $246 | $0 | 1 / 0 |
| `0x2982bb64bcd07ac3315c32cb2bb7e5e8a2de7d67` | BitMart 18 | $0 | $148 | 0 / 1 |
| `0xcad621da75a66c7a8f4ff86d30a2bf981bfc8fdd` | KuCoin 10 | $86 | $0 | 1 / 0 |
| `0xcbffcb2c38ecd19468d366d392ac0c1dc7f04bb6` | OKX 30 | $59 | $0 | 1 / 0 |
| `0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43` | Coinbase 10 | $40 | $14 | 2 / 3 |
| `0xb5d85cbf7cb3ee0d56b3bb207d5fc4b82f43f511` | Coinbase 5 | $0 | $45 | 0 / 2 |
| `0x4976a4a02f38326660d17bf34b431dc6e2eb2327` | Binance 20 | $0 | $14 | 0 / 2 |
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $0 | $5 | 0 / 1 |
| `0xf977814e90da44bfa03b6295a0616a897441acec` | Binance 8 | $0 | $0 | 1 / 0 |
| `0x09c30cdcdd971423cb3ba757a47d56c35d06d818` | Revolut 6 | $0 | $0 | 0 / 1 |
| `0x75e89d5979e4f6fba9f97c104c2f0afb3f1dcb88` | MEXC 1 | $0 | $0 | 1 / 0 |
| `0xf16e9b0d03470827a95cdfd0cb8a8a3b46969b91` | KuCoin 9 | $0 | $0 | 2 / 0 |
| `0x4c9df57276dc17dee5635ded208c07b0be32afd0` | Crypto.com 30 | $0 | $0 | 2 / 0 |
| `0x5754284f345afc66a98fbb0a0afe71e0f007b949` | Bitfinex Tether Treasury | $0 | $0 | 1 / 0 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0xae2d4617…673f` | Kraken 10 | $400,154 | 1 |

### Unidentified counterparties
**This section is a known incomplete part of the analysis.** 37,476 of the 37,495 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$382,972,008 outbound** and **$584,969,109 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x3ef6683f2553af861f91194d23bdf8522d1f2eda` | $120,140,272 | $0 | 793 / 0 | 2023-05-31 → 2026-01-20 |
| 2 | `0xf9793f372c9aa841f8916f0d3c480d18a9cda72d` | $0 | $48,243,283 | 0 / 337 | 2024-02-27 → 2025-12-15 |
| 3 | `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06` | $43,668,293 | $0 | 213 / 0 | 2022-08-31 → 2026-03-26 |
| 4 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $0 | $43,003,709 | 0 / 124 | 2024-03-28 → 2026-01-13 |
| 5 | `0xa370d3a30a125bb025501bf256eb6eab23d54c98` | $42,591,639 | $0 | 919 / 0 | 2022-12-15 → 2026-03-30 |
| 6 | `0xaad6825c2e63363adebbb79203d45b4ed0ac1862` | $27,273,920 | $0 | 720 / 0 | 2022-12-07 → 2026-02-23 |
| 7 | `0x73bfc8b17296cb284b7b116e519c7b84df4e4020` | $24,181,500 | $0 | 2511 / 0 | 2021-04-15 → 2026-04-02 |
| 8 | `0x70a9ffd5ccd90efd82b56e55ff7dc5511c809852` | $24,135,233 | $0 | 157 / 0 | 2022-05-10 → 2026-03-26 |
| 9 | `0xd3b1ca9dfbb4acf1669c60bd8587122144295b73` | $19,563,746 | $0 | 524 / 0 | 2021-11-14 → 2026-03-30 |
| 10 | `0xb7777ac291408554b0e3fedbe79d7675ac962af8` | $19,473,351 | $0 | 502 / 0 | 2025-12-18 → 2026-04-10 |
| 11 | `0x47ef949598e02b90ae2a38624f07b77c18fabb8b` | $16,968,056 | $28 | 2838 / 1 | 2021-04-13 → 2026-04-03 |
| 12 | `0x7dd88a0f2f1599b89c560d9e6e5a77d342687d64` | $0 | $16,928,923 | 0 / 13 | 2025-07-25 → 2025-07-27 |
| 13 | `0xcbc537685c04659d5bddb3d6e2c4149d0e5e4680` | $0 | $16,081,410 | 0 / 66 | 2025-05-29 → 2026-04-07 |
| 14 | `0x1990abd6e49218ab403f01aefeb9d22d07244181` | $0 | $14,754,327 | 0 / 104 | 2025-11-28 → 2026-04-01 |
| 15 | `0x896088463f9660410f10c52e002ac1e274920b0d` | $14,609,119 | $2 | 255 / 1 | 2023-12-08 → 2026-04-10 |
| 16 | `0x25c2f0e18f8945f5395aa971c99e95f808e79dea` | $14,328,650 | $0 | 21 / 0 | 2022-03-30 → 2024-10-28 |
| 17 | `0xf910450ee0d86bd4e3ee4425de0b435edd8543a7` | $13,267,535 | $0 | 411 / 0 | 2022-09-15 → 2026-03-26 |
| 18 | `0xcee4dfde1ce0260afb87f8c917726ab0502fd457` | $12,448,868 | $59 | 327 / 1 | 2021-04-23 → 2025-11-20 |
| 19 | `0x413f54b9308f35e1ae954a111acd059b9083d6b8` | $11,295,199 | $0 | 186 / 0 | 2022-11-02 → 2026-03-26 |
| 20 | `0x097511b9af934c6acb44ba110c24783f57fb4cbb` | $10,926,549 | $0 | 33 / 0 | 2021-06-29 → 2022-01-07 |
| 21 | `0xaabbe35b7dfc5c1f669b4f6558ba7d998c11039b` | $0 | $10,662,176 | 0 / 156 | 2022-10-31 → 2024-12-02 |
| 22 | `0x42b6de749dc4bf0e9f9a0e13a94986587d42498b` | $0 | $10,221,309 | 0 / 9 | 2024-08-28 → 2025-07-25 |
| 23 | `0xeed3b5bb18c81d0dcbc9404b60b016c77e61b555` | $10,180,750 | $0 | 291 / 0 | 2022-03-30 → 2026-04-06 |
| 24 | `0x5ee84d30c7ee57f63f71c92247ff31f95e26916b` | $9,893,084 | $0 | 16 / 0 | 2025-09-22 → 2025-12-15 |
| 25 | `0xda4793ecb8f785837a61864e0b454063d94bfe60` | $9,517,244 | $0 | 40 / 0 | 2025-08-05 → 2025-12-16 |
| 26 | `0x19f0d946c85ed649cf82250f5a07140323e71cc7` | $0 | $9,497,053 | 0 / 16 | 2023-02-15 → 2024-03-07 |
| 27 | `0x43b603d4cdaed3dfa30855c9e354e300094a0a2d` | $0 | $9,197,023 | 0 / 888 | 2023-08-18 → 2026-03-16 |
| 28 | `0xf9d6b16bbf23cedc08846482d8cc5901b6b5d50c` | $9,091,008 | $0 | 1742 / 0 | 2021-04-13 → 2026-04-03 |
| 29 | `0x8c55e56cf813ce34b50dfbcc86762d0fc909aa51` | $1,789,983 | $7,276,007 | 4 / 23 | 2024-08-13 → 2025-11-25 |
| 30 | `0x8d73769a2422f55a9a270fe08b00264ff564696c` | $0 | $8,630,387 | 0 / 298 | 2025-12-22 → 2026-04-13 |
| 31 | `0x05ec9b5421ec93df501054c0a15152da5bb12708` | $8,620,748 | $19 | 80 / 1 | 2022-04-26 → 2025-11-20 |
| 32 | `0x8e96a3e70530f013f4d92f0076d833fdcaa47df4` | $0 | $7,161,653 | 0 / 266 | 2022-09-08 → 2025-11-27 |
| 33 | `0x65c349fa4e1c64115c30e731e5e1c29b7c822690` | $0 | $6,969,419 | 0 / 70 | 2022-01-09 → 2023-12-28 |
| 34 | `0x3372e8c4222c7165c1007fd5d8aefdb720e0a7a1` | $0 | $6,912,875 | 0 / 7 | 2024-03-08 → 2024-08-29 |
| 35 | `0x057d2890018e5cb7efdde1c9c6c042d19b67a4f4` | $6,586,809 | $0 | 80 / 0 | 2022-09-13 → 2026-03-26 |
| 36 | `0x308f672cd0e6111e738262fb65fdf20b811f8b01` | $6,309,144 | $0 | 20 / 0 | 2023-12-13 → 2026-03-30 |
| 37 | `0xf27dc973a47555612d55f0aa5ab021778be7244b` | $0 | $5,984,883 | 0 / 11 | 2024-03-01 → 2024-11-04 |
| 38 | `0xd5e6ad0fce9d6a2fd945284f3bf1cc3a0c78c632` | $5,836,589 | $0 | 20 / 0 | 2025-03-20 → 2026-03-30 |
| 39 | `0x827417b3f50a9927a6055b97a71f36ad3fc23713` | $0 | $5,742,913 | 0 / 192 | 2023-01-12 → 2023-10-17 |
| 40 | `0xec019b1130b869f728f9b496f145bc0e76d8a6cb` | $4,904,960 | $0 | 3 / 0 | 2024-02-18 → 2026-03-26 |
| 41 | `0x36f217d70c84c7362b82d8ef866cc8ffbd020fd1` | $4,825,094 | $0 | 639 / 0 | 2022-02-16 → 2026-03-30 |
| 42 | `0x4b039efd60f4aa2106c6fe4e718b346111ac5cd4` | $4,497,385 | $70 | 458 / 1 | 2021-04-13 → 2026-03-30 |
| 43 | `0x7b464929a7c7c9f59335211a0f699667322b4f14` | $4,393,196 | $17 | 164 / 1 | 2022-04-11 → 2026-03-30 |
| 44 | `0x30ccc62fd085d3dbe11d9fb716dc76ecd67f0ef5` | $0 | $4,311,005 | 0 / 5 | 2022-04-01 → 2022-10-03 |
| 45 | `0x0036934a937dff8fbee41bbed50ed1829067e34e` | $4,306,664 | $0 | 170 / 0 | 2022-08-29 → 2026-03-30 |
| 46 | `0x5fc9611bf4ae9b44201c80f0b27df43e55a57b55` | $3,711,416 | $0 | 10 / 0 | 2024-10-07 → 2026-03-30 |
| 47 | `0x4fc05911251b5bc1dbddb4788c92c19ccf67c8d2` | $3,680,128 | $0 | 596 / 0 | 2021-09-11 → 2026-03-30 |
| 48 | `0x69736878bcc150b58d683bf875cf67485f72a9b2` | $0 | $3,573,814 | 0 / 39 | 2024-10-18 → 2025-09-30 |
| 49 | `0xa7588d1e0b12a41c1750dde919605e51a9443b23` | $0 | $3,561,208 | 0 / 28 | 2024-11-18 → 2025-08-14 |
| 50 | `0x03a283e9293c399ec55239db794a12297529382f` | $0 | $3,385,103 | 0 / 25 | 2022-05-10 → 2022-10-27 |
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

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-5-counterparties.csv`](zonda-5-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

Polygon counterparties are published separately: [`zonda-5-counterparties-polygon.csv`](zonda-5-counterparties-polygon.csv).

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
