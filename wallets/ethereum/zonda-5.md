# Zonda 5

> **Plain-language summary.** A ZondaCrypto exchange wallet using the same private key across five EVM chains (Ethereum, Polygon, Optimism, BSC, Base), with active flow on Ethereum and Polygon and empty recent-window probes on the other three. Attributed by all five major EVM block explorers plus hildobby and BlockSec. Observed Ethereum throughput is $1.99 billion across 98,811 events above $1,000 USD; $122.0 million of outbound flow lands on Binance-tagged deposit addresses.

**Address:** `0x6edf968da408a9640b8865826429a977a11c5048`

**Chains:** Ethereum, Polygon, Optimism, BSC, Base. The same private key is in use on all five.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Each of the five major EVM block explorers — Etherscan, PolygonScan, OP Etherscan, BscScan, BaseScan — carries the public name tag "Zonda 5 (Exchange)" on this address.[^1][^2][^3][^4][^5] The label set is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^6] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "Zonda (BitBay)" under the EXCHANGE category.[^7]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-04-09 (block 12204789); most recent 2026-04-19 (block 24916463); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).
- ERC-20 events: first 2021-04-13 (block 12231426); most recent 2026-05-12 (block 25075921); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2023-08-02 (block 45812984); most recent 2026-04-12 (block 85448141); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).
- ERC-20 events: first 2021-08-08 (block 17763572); most recent 2026-04-10 (block 85349476); ≥ 10,000 events (the indexer’s per-page cap — the true count is at least that; the full count is recovered from Dune in the Flow profile section below).

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $995,891,634 |
| Gross OUT (USD-equivalent at tx time) | $993,970,893 |
| Total throughput (gross in + out) | $1,989,862,528 |
| Net direction | +$1,920,741 |
| Total events ≥$1k | 98,811 |
| Distinct external counterparties (≥$1k cumulative) | 37,490 |
| Identified counterparties in this section | 17 internal + 1,477 external (Etherscan-tagged) + 18 external (hildobby-tagged) + 2 external (BlockSec MetaSleuth) |
| Counterparties without a public name tag | **156,716 (full enumeration), aggregating ~$513,077,072 outbound and ~$659,604,569 inbound across `no-public-tag` + `below-cutoff` rows** (three former entries reclassified 2026-05-18 — see *Counterparties also in this inventory* + *External counterparties — confirmed via BlockSec MetaSleuth*) |
| Active period (≥$1k events) | 2021-04-09 → 2026-04-19 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 2 `0x781229c7…57fc` | $161,301,730 | $158,659,179 | 488 |
| BitBay 3ef668 `0x3ef6683f…2eda` | $120,140,272 | $0 | 793 |
| Zonda 6 `0xd388009f…8046` | $60,769,348 | $46,187,357 | 213 |
| BitBay 879882 `0x879882c5…b54f` | $4,299,650 | $0 | 278 |
| BitBay 3f1eea `0x3f1eea8d…0539` | $0 | $995,620 | 11 |
| Zonda Deposit Funder 1 `0x5bff49ee…9503` | $0 | $500,780 | 1 |

### External counterparties — confirmed via public name tag
| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--:|--:|
| `0x7ff423f8…4c76` | Binance Deposit: 0x7fF423F83622434edC4Eb3eA8212394a115e4C76 | $34,476,272 | 1,031 |
| `0x48e77e08…296b` | Binance Deposit: 0x48e77E0892972e420034e928060293288B32296b | $19,906,357 | 750 |
| `0x558b6d62…07c9` | Binance Deposit: 0x558b6d6258462E78907F14EA7402f52f1CD807C9 | $15,010,490 | 140 |
| `0x61620b28…d24f` | Binance Deposit: 0x61620b28C86ae7D3C9A1b39b38c4147FAA9FD24f | $11,391,405 | 1,424 |
| `0x22b8cc8c…3529` | Binance Deposit: 0x22b8cc8Cf448b7ED9f5ac1eE0446508461493529 | $9,427,000 | 804 |
| `0x088ae43b…b519` | Binance Deposit: 0x088Ae43BE934bA729d8D841b41649c4d417bb519 | $9,191,091 | 286 |
| `0xf1618ff2…fe6a` | Gate Deposit: 0xf1618ff2d8038015f401b22e3ba78cd8b67ffe6a | $8,068,111 | 100 |
| `0x71959d55…dcc0` | Binance Deposit: 0x71959d556b7a50287bb669990791f1EB09a4DCc0 | $6,884,074 | 504 |
| `0x15359093…ddf6` | Binance Deposit: 0x1535909303174e7a235C33814d1B1a359b76ddf6 | $6,199,415 | 436 |
| `0x1936d385…f057` | Binance Deposit: 0x1936d3853c9b7BCf4c3a4105B59D9eFb7984F057 | $6,163,590 | 500 |

<details><summary>Show 40 more rows</summary>

| Counterparty | Tag (Etherscan) | Outbound USD | Events |
|--|--|--:|--:|
| `0x8a63afd3…25b5` | Binance Deposit: 0x8a63AFd33e0d05274B3B6650486D9960785025B5 | $4,940,376 | 283 |
| `0xfae79cff…a9ae` | Binance Deposit: 0xfAe79cFFdFF6893e772940ec4e0CAF36c037a9Ae | $4,142,002 | 57 |
| `0xb8228778…a7e8` | Binance Deposit: 0xb8228778465623b00B3544E6ba8e4e620C21A7e8 | $3,109,794 | 91 |
| `0xef0d5ff4…a0c7` | Gate Deposit: 0xef0d5ff4cf63a6abdab4b1d151d1d9600feaa0c7 | $2,705,584 | 502 |
| `0xe70a98cb…44df` | Binance Deposit: 0xe70A98cbfD42125e4c940cDf328E67032d6044DF | $2,668,338 | 52 |
| `0x2f9378d5…2aa5` | Binance Deposit: 0x2F9378D573b20199105bCaF6D103Ac88d5442aA5 | $2,410,750 | 23 |
| `0x2caa72af…6c94` | Binance Deposit: 0x2caA72Af5eb6714f16401E254b5735A24ADC6C94 | $2,404,350 | 42 |
| `0x901c8da4…da23` | Binance Deposit: 0x901c8dA41AA29ACc315CCB520e87Ada75f30da23 | $2,351,120 | 142 |
| `0x213000a6…8bec` | Binance Deposit: 0x213000A65dA8b1b64E31C63Ba39B9a8809f28beC | $2,076,461 | 54 |
| `0x160a946f…e4ee` | Binance Deposit: 0x160A946f4daA72E76C923A42deA703a430f1e4EE | $1,961,637 | 100 |
| `0x190e2fd1…4c60` | Gate Deposit: 0x190e2fd1ee908f6615285c1714827354f74f4c60 | $1,904,386 | 308 |
| `0x1d7367b9…fb48` | Binance Deposit: 0x1D7367b9f4c2ED928115eb7809B6E5D98A7fFB48 | $1,868,384 | 30 |
| `0x6384098c…e6ea` | Binance Deposit: 0x6384098C92B56ad4c6e7F28d098aca733644e6Ea | $1,844,596 | 159 |
| `0x4936166c…6754` | Gate Deposit: 0x4936166c9129fee5f4cf1ffa4500ba3a3f846754 | $1,762,815 | 44 |
| `0x0477193d…d368` | Binance Deposit: 0x0477193db9BB8Cc28371500671d67E469909D368 | $1,360,745 | 232 |
| `0x6c5403c0…fc94` | Binance Deposit: 0x6C5403c04956f8106cE7dE444b3B02261edefC94 | $1,270,640 | 32 |
| `0xe8dca932…da41` | ByBit Deposit: 0xE8dcA93289304044682d100F570ddD8eD80DDa41 | $1,244,174 | 104 |
| `0x30d81208…4544` | Binance Deposit: 0x30D81208F42C7Ba484131f3C840bfd5cdAE04544 | $1,158,468 | 3 |
| `0x5679651f…b786` | ByBit Deposit: 0x5679651F97154FAa98b35CCA77F335aCc3a0b786 | $1,010,882 | 50 |
| `0xe80eeac1…3b71` | Binance Deposit: 0xE80eEAC197B778ABDa21Ae2e2A89CE4396cE3B71 | $924,429 | 10 |
| `0xa55f225a…0014` | Binance Deposit: 0xA55F225AAd1Bf05A1f743FC4c92a21F5fA140014 | $895,194 | 178 |
| `0xaad60b66…4e7f` | Binance Deposit: 0xaaD60b6615b9eB13a9B0212af7b298F26dD74e7f | $833,817 | 142 |
| `0x96288545…2146` | Binance Deposit: 0x962885450708f2500840905B8c13316F73222146 | $693,648 | 7 |
| `0x93803d62…18b9` | Binance Deposit: 0x93803D62C26e523fC534a1c1457B27BC6dC018b9 | $680,161 | 7 |
| `0x63146eaa…2a93` | Binance Deposit: 0x63146EaA57d2DBD614Ec1D70d4c225Aa171e2a93 | $621,875 | 14 |
| `0x41d6a1ce…31db` | ByBit Deposit: 0x41d6A1Ce50A1EC1365efeb98241B4892d10331Db | $610,768 | 30 |
| `0x10787b6e…6435` | ByBit Deposit: 0x10787b6E8A7d320Af75b9795e76855C607726435 | $607,060 | 10 |
| `0xe208463f…6f6c` | Binance Deposit: 0xe208463FEBE08caD4baFD6BEadA7567149476F6c | $572,947 | 65 |
| `0x74799664…c81d` | Binance Deposit: 0x7479966448e516848bd8174c839FC3E3591Dc81D | $549,892 | 20 |
| `0x0f43b6e6…20f1` | Binance Deposit: 0x0F43b6e67694E5AF3Af04Ecc66668024B6C820F1 | $545,758 | 57 |
| `0xf6ab6a6c…807f` | Binance Deposit: 0xf6aB6A6c39Fc60cCF61A0A2c64D523E7E7BB807f | $543,307 | 64 |
| `0x6b001531…0c70` | Binance Deposit: 0x6B001531717E17f945382E9Ee04E3e73F1950C70 | $518,590 | 56 |
| `0x57be1317…a340` | Gate Deposit: 0x57be1317d96617e2d28d9bf271a8fcb359eda340 | $514,013 | 11 |
| `0xf653df3f…3bb3` | Binance Deposit: 0xf653DF3fa6Dae9D489cCcdA5A5983e9Be0493Bb3 | $506,737 | 4 |
| `0x2521145a…a0f5` | ByBit Deposit: 0x2521145a7b957E268d0D1587aB98059f8C66a0F5 | $480,532 | 3 |
| `0x11e74c54…eade` | Binance Deposit: 0x11E74c54580C96ADc818FA2327806e571fB9eAdE | $475,544 | 29 |
| `0xa538340e…8546` | Binance Deposit: 0xA538340eEf0E0AbEc7C4758Fc3CbD617E4E58546 | $467,040 | 67 |
| `0xc00b08d9…167f` | Bitkub Deposit: 0xC00b08D9D40c8a73a5850009913d454d1899167F | $444,366 | 14 |
| `0x7c957795…80b4` | Binance Deposit: 0x7c9577959E9B60117B9b9a9d6878A8B0b3c080b4 | $421,948 | 5 |
| `0xd8ad068f…b23d` | Binance Deposit: 0xd8Ad068Fabede7f25Bcf138F86848295C22Eb23d | $411,511 | 79 |

</details>

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

<details><summary>Show 8 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x4976a4a02f38326660d17bf34b431dc6e2eb2327` | Binance 20 | $0 | $14 | 0 / 2 |
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $0 | $5 | 0 / 1 |
| `0xf977814e90da44bfa03b6295a0616a897441acec` | Binance 8 | $0 | $0 | 1 / 0 |
| `0x09c30cdcdd971423cb3ba757a47d56c35d06d818` | Revolut 6 | $0 | $0 | 0 / 1 |
| `0x75e89d5979e4f6fba9f97c104c2f0afb3f1dcb88` | MEXC 1 | $0 | $0 | 1 / 0 |
| `0xf16e9b0d03470827a95cdfd0cb8a8a3b46969b91` | KuCoin 9 | $0 | $0 | 2 / 0 |
| `0x4c9df57276dc17dee5635ded208c07b0be32afd0` | Crypto.com 30 | $0 | $0 | 2 / 0 |
| `0x5754284f345afc66a98fbb0a0afe71e0f007b949` | Bitfinex Tether Treasury | $0 | $0 | 1 / 0 |

</details>

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0xae2d4617…673f` | Kraken 10 | $400,154 | 1 |

### External counterparties — confirmed via BlockSec MetaSleuth

BlockSec MetaSleuth's address-label API v3 carries attributions for two of the largest formerly-unattributed Zonda 5 counterparties. Both are Kraken customer-deposit addresses (single-customer accounts that aggregate Zonda customer withdrawals before forwarding to Kraken's hot-wallet infrastructure). Receipt: [`../../sources/blocksec/labels-2026-05-18.json`](../../sources/blocksec/labels-2026-05-18.json).

| Counterparty | Tag (BlockSec) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xf9793f37…a72d` | Kraken: Deposit Address | $0 | $48,243,283 | 0 / 337 |
| `0x8d73769a…696c` | Kraken: Deposit Address | $0 | $8,630,387 | 0 / 298 |

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 156,716 of the 158,211 external counterparties in the full enumeration carry no public name tag on Etherscan as of 2026-05-18 and do not appear in this inventory's roster. The unidentified rows aggregate **$513,077,072 outbound** and **$659,604,569 inbound** across `no-public-tag` + `below-cutoff` rows. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06` | $43,668,293 | $0 | 213 / 0 | 2022-08-31 → 2026-03-26 |
| 2 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $0 | $43,003,709 | 0 / 124 | 2024-03-28 → 2026-01-13 |
| 3 | `0xa370d3a30a125bb025501bf256eb6eab23d54c98` | $42,591,639 | $0 | 919 / 0 | 2022-12-15 → 2026-03-30 |
| 4 | `0xaad6825c2e63363adebbb79203d45b4ed0ac1862` | $27,273,920 | $0 | 720 / 0 | 2022-12-07 → 2026-02-23 |
| 5 | `0x73bfc8b17296cb284b7b116e519c7b84df4e4020` | $24,181,500 | $0 | 2,511 / 0 | 2021-04-15 → 2026-04-02 |
| 6 | `0x70a9ffd5ccd90efd82b56e55ff7dc5511c809852` | $24,135,233 | $0 | 157 / 0 | 2022-05-10 → 2026-03-26 |
| 7 | `0xd3b1ca9dfbb4acf1669c60bd8587122144295b73` | $19,563,746 | $0 | 524 / 0 | 2021-11-14 → 2026-03-30 |
| 8 | `0xb7777ac291408554b0e3fedbe79d7675ac962af8` | $19,473,351 | $0 | 502 / 0 | 2025-12-18 → 2026-04-10 |
| 9 | `0x47ef949598e02b90ae2a38624f07b77c18fabb8b` | $16,968,056 | $28 | 2,838 / 1 | 2021-04-13 → 2026-04-03 |
| 10 | `0x7dd88a0f2f1599b89c560d9e6e5a77d342687d64` | $0 | $16,928,923 | 0 / 13 | 2025-07-25 → 2025-07-27 |

<details><summary>Show 40 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0xcbc537685c04659d5bddb3d6e2c4149d0e5e4680` | $0 | $16,081,410 | 0 / 66 | 2025-05-29 → 2026-04-07 |
| 12 | `0x1990abd6e49218ab403f01aefeb9d22d07244181` | $0 | $14,754,327 | 0 / 104 | 2025-11-28 → 2026-04-01 |
| 13 | `0x896088463f9660410f10c52e002ac1e274920b0d` | $14,609,119 | $2 | 255 / 1 | 2023-12-08 → 2026-04-10 |
| 14 | `0x25c2f0e18f8945f5395aa971c99e95f808e79dea` | $14,328,650 | $0 | 21 / 0 | 2022-03-30 → 2024-10-28 |
| 15 | `0xf910450ee0d86bd4e3ee4425de0b435edd8543a7` | $13,267,535 | $0 | 411 / 0 | 2022-09-15 → 2026-03-26 |
| 16 | `0xcee4dfde1ce0260afb87f8c917726ab0502fd457` | $12,448,868 | $59 | 327 / 1 | 2021-04-23 → 2025-11-20 |
| 17 | `0x413f54b9308f35e1ae954a111acd059b9083d6b8` | $11,295,199 | $0 | 186 / 0 | 2022-11-02 → 2026-03-26 |
| 18 | `0x097511b9af934c6acb44ba110c24783f57fb4cbb` | $10,926,549 | $0 | 33 / 0 | 2021-06-29 → 2022-01-07 |
| 19 | `0xaabbe35b7dfc5c1f669b4f6558ba7d998c11039b` | $0 | $10,662,176 | 0 / 156 | 2022-10-31 → 2024-12-02 |
| 20 | `0x42b6de749dc4bf0e9f9a0e13a94986587d42498b` | $0 | $10,221,309 | 0 / 9 | 2024-08-28 → 2025-07-25 |
| 21 | `0xeed3b5bb18c81d0dcbc9404b60b016c77e61b555` | $10,180,750 | $0 | 291 / 0 | 2022-03-30 → 2026-04-06 |
| 22 | `0x5ee84d30c7ee57f63f71c92247ff31f95e26916b` | $9,893,084 | $0 | 16 / 0 | 2025-09-22 → 2025-12-15 |
| 23 | `0xda4793ecb8f785837a61864e0b454063d94bfe60` | $9,517,244 | $0 | 40 / 0 | 2025-08-05 → 2025-12-16 |
| 24 | `0x19f0d946c85ed649cf82250f5a07140323e71cc7` | $0 | $9,497,053 | 0 / 16 | 2023-02-15 → 2024-03-07 |
| 25 | `0x43b603d4cdaed3dfa30855c9e354e300094a0a2d` | $0 | $9,197,023 | 0 / 888 | 2023-08-18 → 2026-03-16 |
| 26 | `0xf9d6b16bbf23cedc08846482d8cc5901b6b5d50c` | $9,091,008 | $0 | 1,742 / 0 | 2021-04-13 → 2026-04-03 |
| 27 | `0x8c55e56cf813ce34b50dfbcc86762d0fc909aa51` | $1,789,983 | $7,276,007 | 4 / 23 | 2024-08-13 → 2025-11-25 |
| 28 | `0x05ec9b5421ec93df501054c0a15152da5bb12708` | $8,620,748 | $19 | 80 / 1 | 2022-04-26 → 2025-11-20 |
| 29 | `0x8e96a3e70530f013f4d92f0076d833fdcaa47df4` | $0 | $7,161,653 | 0 / 266 | 2022-09-08 → 2025-11-27 |
| 30 | `0x65c349fa4e1c64115c30e731e5e1c29b7c822690` | $0 | $6,969,419 | 0 / 70 | 2022-01-09 → 2023-12-28 |
| 31 | `0x3372e8c4222c7165c1007fd5d8aefdb720e0a7a1` | $0 | $6,912,875 | 0 / 7 | 2024-03-08 → 2024-08-29 |
| 32 | `0x057d2890018e5cb7efdde1c9c6c042d19b67a4f4` | $6,586,809 | $0 | 80 / 0 | 2022-09-13 → 2026-03-26 |
| 33 | `0x308f672cd0e6111e738262fb65fdf20b811f8b01` | $6,309,144 | $0 | 20 / 0 | 2023-12-13 → 2026-03-30 |
| 34 | `0xf27dc973a47555612d55f0aa5ab021778be7244b` | $0 | $5,984,883 | 0 / 11 | 2024-03-01 → 2024-11-04 |
| 35 | `0xd5e6ad0fce9d6a2fd945284f3bf1cc3a0c78c632` | $5,836,589 | $0 | 20 / 0 | 2025-03-20 → 2026-03-30 |
| 36 | `0x827417b3f50a9927a6055b97a71f36ad3fc23713` | $0 | $5,742,913 | 0 / 192 | 2023-01-12 → 2023-10-17 |
| 37 | `0xec019b1130b869f728f9b496f145bc0e76d8a6cb` | $4,904,960 | $0 | 3 / 0 | 2024-02-18 → 2026-03-26 |
| 38 | `0x36f217d70c84c7362b82d8ef866cc8ffbd020fd1` | $4,825,094 | $0 | 639 / 0 | 2022-02-16 → 2026-03-30 |
| 39 | `0x4b039efd60f4aa2106c6fe4e718b346111ac5cd4` | $4,497,385 | $70 | 458 / 1 | 2021-04-13 → 2026-03-30 |
| 40 | `0x7b464929a7c7c9f59335211a0f699667322b4f14` | $4,393,196 | $17 | 164 / 1 | 2022-04-11 → 2026-03-30 |
| 41 | `0x30ccc62fd085d3dbe11d9fb716dc76ecd67f0ef5` | $0 | $4,311,005 | 0 / 5 | 2022-04-01 → 2022-10-03 |
| 42 | `0x0036934a937dff8fbee41bbed50ed1829067e34e` | $4,306,664 | $0 | 170 / 0 | 2022-08-29 → 2026-03-30 |
| 43 | `0x5fc9611bf4ae9b44201c80f0b27df43e55a57b55` | $3,711,416 | $0 | 10 / 0 | 2024-10-07 → 2026-03-30 |
| 44 | `0x4fc05911251b5bc1dbddb4788c92c19ccf67c8d2` | $3,680,128 | $0 | 596 / 0 | 2021-09-11 → 2026-03-30 |
| 45 | `0x69736878bcc150b58d683bf875cf67485f72a9b2` | $0 | $3,573,814 | 0 / 39 | 2024-10-18 → 2025-09-30 |
| 46 | `0xa7588d1e0b12a41c1750dde919605e51a9443b23` | $0 | $3,561,208 | 0 / 28 | 2024-11-18 → 2025-08-14 |
| 47 | `0x03a283e9293c399ec55239db794a12297529382f` | $0 | $3,385,103 | 0 / 25 | 2022-05-10 → 2022-10-27 |
| 48 | `0x34a34dcf0c3f127737937ad607f70a34c61ef0f2` | $3,375,973 | $0 | 74 / 0 | 2022-08-22 → 2026-03-26 |
| 49 | `0xcf68022ebfd4f565a9e8cacfec4ecf93524b0fd6` | $3,374,216 | $0 | 33 / 0 | 2023-11-15 → 2026-03-26 |
| 50 | `0x533671f6a2e1c20e77af941691790bad3cd3fb9c` | $0 | $3,359,388 | 0 / 9 | 2025-05-06 → 2025-12-03 |

</details>
## Multichain footprint — probed-and-empty chains (2026-05-13)

Beyond Ethereum and Polygon (both ACTIVE — see flow profiles in this file), Zonda 5's multichain footprint has been independently probed and found empty on every other EVM chain it carries an attribution claim on. The same EVM key (`0x6edf968d…5048`) is empty on:

| Chain | Result | Method | Receipt |
|--|--|--|--|
| Optimism | EMPTY (0 events in the most recent 100,000 blocks scanned) | Archive RPC `eth_getLogs` over rolling 100k-block window | working archive |
| Base | EMPTY (0 events in the most recent 100,000 blocks scanned) | Archive RPC `eth_getLogs` | working archive |
| Avalanche C-chain | EMPTY (0 events in 100,000 blocks) | Archive RPC `eth_getLogs` | working archive |
| BSC | EMPTY (0 events / 10×10k chunks) | Archive RPC `eth_getLogs` | working archive |
| zkSync Era | UNPROBED for this key (only the F-005 institutional address was zkSync-probed; deferred) | — | — |
| Tron (native + TRX_EVM_RPC) | EMPTY (zero balance + zero txs) | Tronscan API + TRX_EVM_RPC | working archive |

Receipt JSONs from the `eth_getLogs` probes are retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility). Each probe is reproducible from the address alone against any archive RPC endpoint for the named chain.

The "BSC / Optimism / Base" annotation that appears on this page above for Zonda 5 reflects same-key cross-chain availability of the EOA, not active flow on those chains: the most-recent-window probes return zero events. Historical pre-2024 BSC activity has not been ruled in or out by these recent-window probes; a deeper backward chunked scan is queued in the case's `queue.md` but has not been run.

**Confidence:** CONFIRMED-empty on the recent-window probes shown above. The longer-history BSC question remains UNPROBED.

## Flow profile (Polygon, Dune-aggregated 2026-05-13)

Full-history aggregation built from Dune `tokens_polygon.transfers` (≥$1,000 USD-equivalent per event). See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $133,447,101 |
| Gross OUT (USD-equivalent at tx time) | $131,913,325 |
| Total throughput | $265,360,426 |
| Net direction | +$1,533,776 |
| Total events ≥$1k | 8,021 |
| Distinct external counterparties (≥$1k cumulative) | 1,677 |
| Identified counterparties in this section | 5 internal + 230 external (PolygonScan-tagged via cross-chain ETH closure-pass + PolygonScan probe 2026-05-14) + 15 external (hildobby-tagged) |
| Counterparties without a public name tag | **16,838 (full enumeration), aggregating ~$29,373,207 outbound and ~$102,656,866 inbound across `no-public-tag` + `below-cutoff` rows** |
| Active period | 2023-11-22 → 2026-04-09 |

**Confidence:** CONFIRMED on totals. CONFIRMED on Internal and External-tagged rows below (each PolygonScan tag verified by fresh HTML fetch on 2026-05-13 + 2026-05-14 PolygonScan closure pass; HTML retained in the working archive; see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 6 `0xd388009f…8046` | $13,614,690 | $57,282,318 | 159 |
| Zonda 2 `0x781229c7…57fc` | $10,812,322 | $11,723,827 | 49 |
| BitBay 879882 `0x879882c5…b54f` | $6,914,650 | $0 | 544 |

### External destinations — confirmed via PolygonScan public name tags

Listed by descending outbound USD. Top 50 of 230 PolygonScan-tagged rows shown; full enumeration in CSV.

| Counterparty | Tag (PolygonScan) | Outbound USD | Events |
|--|--|--:|--:|
| `0x7ff423f8…4c76` | Binance Deposit: 0x7fF423F83622434edC4Eb3eA8212394a115e4C76 | $7,976,049 | 158 |
| `0xfae79cff…a9ae` | Binance Deposit: 0xfAe79cFFdFF6893e772940ec4e0CAF36c037a9Ae | $6,684,605 | 98 |
| `0x48e77e08…296b` | Binance Deposit: 0x48e77E0892972e420034e928060293288B32296b | $5,169,243 | 188 |
| `0x61620b28…d24f` | Binance Deposit: 0x61620b28C86ae7D3C9A1b39b38c4147FAA9FD24f | $3,217,586 | 192 |
| `0x1936d385…f057` | Binance Deposit: 0x1936d3853c9b7BCf4c3a4105B59D9eFb7984F057 | $2,268,165 | 179 |
| `0x71959d55…dcc0` | Binance Deposit: 0x71959d556b7a50287bb669990791f1EB09a4DCc0 | $1,995,365 | 337 |
| `0xe8dca932…da41` | ByBit Deposit: 0xE8dcA93289304044682d100F570ddD8eD80DDa41 | $1,295,439 | 80 |
| `0x558b6d62…07c9` | Binance Deposit: 0x558b6d6258462E78907F14EA7402f52f1CD807C9 | $819,579 | 8 |
| `0x41d6a1ce…31db` | ByBit Deposit: 0x41d6A1Ce50A1EC1365efeb98241B4892d10331Db | $579,927 | 23 |
| `0xe70a98cb…44df` | Binance Deposit: 0xe70A98cbfD42125e4c940cDf328E67032d6044DF | $481,187 | 11 |

<details><summary>Show 40 more rows</summary>

| Counterparty | Tag (PolygonScan) | Outbound USD | Events |
|--|--|--:|--:|
| `0x57a484ea…0cb5` | Gate Deposit: 0x57a484ea925a1c4ccffd35d433bfa03985410cb5 | $261,888 | 213 |
| `0x213000a6…8bec` | Binance Deposit: 0x213000A65dA8b1b64E31C63Ba39B9a8809f28beC | $201,899 | 2 |
| `0xeba8cbae…68f1` | Gate Deposit: 0xeba8cbae20d25fbe1f992f45a90a5719df0d68f1 | $172,289 | 8 |
| `0x93803d62…18b9` | Binance Deposit: 0x93803D62C26e523fC534a1c1457B27BC6dC018b9 | $166,695 | 3 |
| `0x95c9c3b6…9632` | Binance Deposit: 0x95C9c3b62fFeaA9E8645c2BEE7C1709a6A469632 | $165,605 | 5 |
| `0x2521145a…a0f5` | ByBit Deposit: 0x2521145a7b957E268d0D1587aB98059f8C66a0F5 | $150,079 | 1 |
| `0xaedfffd8…4d80` | Binance Deposit: 0xaEdFFfd82aE5df02812b035099Bb3e58FaEd4d80 | $148,801 | 6 |
| `0x97a38f2b…27a4` | Binance Deposit: 0x97a38F2b58Cb7D8771020aBCB15e54F983C627a4 | $126,957 | 24 |
| `0xb6df501f…92b8` | ByBit Deposit: 0xb6Df501F9a4De5B1DCb09f3a14b934CD4d6B92b8 | $124,903 | 8 |
| `0xaec2abe3…532b` | ByBit Deposit: 0xaEC2aBe3B54a9F7d28b8938217A3dF45645d532B | $105,509 | 2 |
| `0x4e29b73f…0569` | Binance Deposit: 0x4e29B73FEAABdf2b04134386BdA62FaA164C0569 | $100,550 | 26 |
| `0x68cd627d…5fea` | Binance Deposit: 0x68cd627D3A077aF46bE4CcCE3249dce0d5F65FEA | $89,464 | 4 |
| `0xb92addb2…d83c` | Coinbase Deposit: 0xb92adDB207C35Af1DFf0eC8d08B95a60DC50d83c | $82,872 | 11 |
| `0x34d6d815…fbfe` | Binance Deposit: 0x34d6d815Ff27Ddf5C5293Eed305a6c4A1f7aFbFe | $77,063 | 6 |
| `0x1b04aab3…9c05` | ByBit Deposit: 0x1b04aAB39cDCe6EDFbcD6eb03dfc5f585e449C05 | $74,025 | 15 |
| `0x91104530…bc88` | Binance Deposit: 0x91104530A337764aAF7cD1073F4410BB5aa8bc88 | $70,054 | 2 |
| `0x88815de5…6417` | ByBit Deposit: 0x88815De595AdDB6FdD58D07e050a97dc4B186417 | $68,905 | 16 |
| `0x1e607bed…e41e` | ByBit Deposit: 0x1e607Bed795A42459A2c197DB1844C97d42Ae41E | $64,950 | 14 |
| `0x47c25685…06d3` | Gate Deposit: 0x47c25685687d181add0527f122696bbbbcda06d3 | $59,077 | 9 |
| `0x1af42345…eb22` | Binance Deposit: 0x1aF42345EAe13d1B97dfe8b4482027aD405DEb22 | $58,833 | 9 |
| `0xd32cea17…0108` | Binance Deposit: 0xd32cea173bC2752C05B48b2A2f578CCB4dC60108 | $56,802 | 3 |
| `0x8690fac5…f0b2` | Binance Deposit: 0x8690fAc51C751EA3485246E0Cab0d38A0E47F0b2 | $55,291 | 2 |
| `0xde807374…24ac` | Gate Deposit: 0xde8073743a00b498016c05e5df9a245ffa3a24ac | $53,371 | 7 |
| `0x4936166c…6754` | Gate Deposit: 0x4936166c9129fee5f4cf1ffa4500ba3a3f846754 | $53,032 | 1 |
| `0xf569f8b6…7aac` | Binance Deposit: 0xF569F8B6cef334459Aa83d9Cfea777962A8D7AaC | $51,116 | 4 |
| `0x6055626d…82e3` | Binance Deposit: 0x6055626da6D21De5e49Cdd9029D6b1e5781082e3 | $50,706 | 34 |
| `0x9e5172dd…7417` | Binance Deposit: 0x9e5172DDf01Cb57Fc17D6bE66Ca0520c94FD7417 | $49,777 | 4 |
| `0x5ff911cc…5f8c` | Binance Deposit: 0x5fF911cC502e6972aF0c5F418ff15ed6d2FF5f8C | $47,276 | 11 |
| `0xcda897d1…3075` | ByBit Deposit: 0xcdA897d11B3d12Ac7401384beae0475BF1F53075 | $44,538 | 5 |
| `0x4fc256ff…9201` | Binance Deposit: 0x4Fc256ff34514A964225585E56BA4a997b879201 | $44,234 | 179 |
| `0xc3d44a80…9867` | Binance Deposit: 0xc3d44A80989c49FDb5F75edF32F65105a4309867 | $43,729 | 2 |
| `0x7ec6642b…1f8f` | ByBit Deposit: 0x7Ec6642B7e80f72aF1b2a79105Dc07B57B0C1f8F | $40,935 | 2 |
| `0x39ac8257…75c7` | ByBit Deposit: 0x39aC8257Fce2270f7740Ded8CfF1EcfCF78e75C7 | $39,623 | 5 |
| `0x8efbf936…21f2` | Gate Deposit: 0x8efbf936d8966309b999d967018b0ace51c121f2 | $38,271 | 2 |
| `0x4c99e609…da12` | ByBit Deposit: 0x4C99e609d49b870c13aFe69b861189fc7Ec7DA12 | $37,358 | 4 |
| `0x6bb5860b…9233` | Binance Deposit: 0x6bb5860B935f7774A3d71f1Ff15560373F159233 | $34,905 | 29 |
| `0xa0de8817…237e` | ByBit Deposit: 0xA0dE8817Fa3806EFF3EA69F1601d1AC73C1d237E | $31,429 | 11 |
| `0x0cf5b6f9…71e9` | Binance Deposit: 0x0cf5B6f9DD42fbb106312E520B95c3787B9C71E9 | $31,344 | 7 |
| `0x413d6880…09ac` | Binance Deposit: 0x413D68800E09214fe897C56e14B6c6D3b56409Ac | $29,673 | 3 |
| `0x1b604ece…0605` | Binance Deposit: 0x1b604ecEE329CfB99699c53E43a6dA73D2c50605 | $27,962 | 4 |

</details>

### External counterparties — confirmed via hildobby CEX Dune query 3237025

15 hildobby-tagged Polygon counterparties — mostly poisoning-seed entries ($0 USD) where the seed transfer used a known CEX hot-wallet as the spoofed source. Real value flow only on Gate.io 1 ($168k inbound).

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--:|--:|--:|
| `0x0d070796…92fe` | Gate.io 1 | $168,037 | $0 | 3 / 0 |
| `0xf89d7b9c…aa40` | Bybit 5 | $0 | $0 | 10 / 0 |
| `0xe7804c37…e245` | Binance 48 | $0 | $0 | 151 / 0 |
| `0x77134cbc…35ec` | Bitfinex Hot Wallet | $0 | $0 | 6 / 0 |
| `0xc9aaa6ca…f299` | Coinbase 37 | $0 | $0 | 8 / 0 |
| `0x082489a6…08da` | Binance 53 | $0 | $0 | 6 / 0 |
| `0xf977814e…acec` | Binance 8 | $0 | $0 | 4 / 0 |
| `0x51e3d441…75e0` | MEXC 8 | $0 | $0 | 1 / 0 |
| `0x290275e3…cb88` | Binance 68 | $0 | $0 | 1 / 0 |
| `0x20fe51a9…3b7a` | Coinbase 21 | $0 | $0 | 1 / 0 |

<details><summary>Show 5 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--:|--:|--:|
| `0x631fc1ea…a161` | Binance 44 | $0 | $0 | 1 / 0 |
| `0xfe9e8709…51c8` | Binance 5 | $0 | $0 | 1 / 0 |
| `0xd7025073…7e42` | HTX 48 | $0 | $0 | 1 / 0 |
| `0x51528181…a621` | WhiteBIT 5 | $0 | $0 | 1 / 0 |
| `0x3727cfcb…6be8` | Bitbank 2 | $0 | $0 | 1 / 0 |

</details>

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** 16,838 of the 17,083 Polygon external counterparties in the full enumeration carry no PolygonScan public name tag as of 2026-05-14 and do not appear in this inventory's roster. The unidentified rows aggregate **$29,373,207 outbound** and **$102,656,866 inbound** across `no-public-tag` + `below-cutoff` rows. Entity-attribution work on these counterparties is ongoing.

**Receipts**: `../../sources/dune/polygon-per-wallet-2026-05-13.json` (query 7491823) + `../../sources/dune/polygon-totals-2026-05-13.json` (query 7491829) (PolygonScan public-name-tag HTML batch retained in the working archive; see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)).

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-5-counterparties.csv`](zonda-5-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

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
