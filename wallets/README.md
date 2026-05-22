# Known wallets

Wallets attributed to ZondaCrypto, BitBay, or the ZND token by a primary reference. One file per wallet, except where a single primary source attributes a cluster of operational hot-wallet / per-user-deposit addresses to the operator — in that case the cluster is documented as a single inventory item.

The **Activity** column is a compact summary of on-chain activity per chain. Probed 2026-05-13 via Etherscan v2 (`account/txlist` + `account/tokentx`) for EVM chains, mempool.space for the Bitcoin cold reserve, and WalletExplorer for the BitBay.net cluster. The `≥10k` markers indicate the wallet has more events than a single 10,000-event Etherscan page can return — i.e. the true count is at least that, and any aggregation must paginate or use an indexed-DB query (Dune, BigQuery) for completeness. See each per-wallet file for the full date+block-height detail.

## Bitcoin

The two Bitcoin-side inventory items. The cold reserve is a single address; the BitBay.net cluster is a 26,014-address cluster recorded as one inventory item.

| Address | What it is | Activity | Detail |
|---|---|---|---|
| `16aEn4p6hK4FMpLtJGpoQZMZ946sDg1Z6n` | Disclosed BTC cold reserve | 2016-03-06 → 2026-05-08, 39 tx, all UTXOs unspent (4,503.26 BTC balance) | [→](bitcoin/16aEn4p6-cold-reserve.md) |
| WalletExplorer cluster `BitBay.net` (26,014 addresses) | Post-2019 operational hot-wallet cluster | 2019-05-13 → 2025-08-24, 321,245 tx (cluster total) | [→](bitcoin/bitbay-net-cluster.md) |

## Ethereum — Zonda core exchange wallets

The seven `Zonda <N>` wallets that carry an Etherscan public name tag in the `Zonda <N> (Exchange)` family. Zonda 5 is a single key in use across five EVM chains; the per-wallet file documents the multichain activity.

| Address | Chains | What it is | Activity | Detail |
|---|---|---|---|---|
| `0xf646cbe3b030fb6c2569215f0117dba58badb95e` | Ethereum | Zonda 1 | ETH: 2017-12-11 → 2026-04-04, ≥10k native / 176 ERC-20 | [→](ethereum/zonda-1.md) |
| `0x781229c7a798c33ec788520a6bbe12a79ed657fc` | Ethereum, Polygon | Zonda 2 | ETH: 2021-07-27 → 2026-04-17, ≥10k native / 4,493 ERC-20. POL: 2021-09-10 → 2026-03-29, 43 native / 426 ERC-20 (incl. poisoning seeds). | [→](ethereum/zonda-2.md) |
| `0x0ff24158220a14398f047a80a513617ddc4f5289` | Ethereum | Zonda 3 | ETH: 2016-04-02 → 2026-02-21, ≥10k native / 378 ERC-20 | [→](ethereum/zonda-3.md) |
| `0x2b645268e2fbb384b423e50089657395f749763a` | Ethereum | Zonda 4 | ETH: 2020-08-12 → 2026-04-16, ≥10k native / 21 ERC-20 | [→](ethereum/zonda-4.md) |
| `0x6edf968da408a9640b8865826429a977a11c5048` | Ethereum, Polygon, Optimism, BSC, Base | Zonda 5 (same key on five EVM chains) | ETH: 2021-04-09 → 2026-05-12, ≥10k / ≥10k. POL: 2021-08-08 → 2026-04-12, ≥10k / ≥10k. Recent-window archive-RPC probes on Optimism / Base / BSC returned 0 events for this key — see the per-wallet file. | [→](ethereum/zonda-5.md) |
| `0xd388009f01bbe5e6d2cb6ba8525ca50b56308046` | Ethereum, Polygon | Zonda 6 | ETH: 2023-10-25 → 2026-03-29, 830 native / 1,217 ERC-20. POL: 2023-10-30 → 2026-03-25, 575 native / 3,123 ERC-20. | [→](ethereum/zonda-6.md) |

## Ethereum — deposit infrastructure

Operational EOAs and addresses that pre-fund user-deposit addresses (gas suppliers) and the deposit-side wallet itself.

| Address | What it is | Activity | Detail |
|---|---|---|---|
| `0x5bff49eec8f76c066f979a818187b9732ac69503` | Zonda Deposit Funder 1 | 2023-10-31 → 2026-04-27, ≥10k native / 1,255 ERC-20 | [→](ethereum/zonda-deposit-funder-1.md) |
| `0x818ab3c61f66e975b8e6290c20999d6749f60d8d` | Zonda Deposit Funder 2 | 2021-04-12 → 2023-11-06, ≥10k native / 15 ERC-20 (dormant after 2023-11) | [→](ethereum/zonda-deposit-funder-2.md) |
| `0x82c829237159287dac6fc62eb139e6a89195900c` | Zonda Deposit Wallet | 2022-11-28 → 2026-04-03, 262 native / 351 ERC-20 | [→](ethereum/zonda-deposit-wallet-82c829.md) |

## Ethereum — ZND token suite

The ZND token contract, its deployer EOA, the ZNDStaking contract that owns the token, the EOA that owns ZNDStaking, and the three operator-side accounts ZNDStaking exposes as state variables. Plus the TMPL token, an Olympic-sponsorship ERC-20 issued by ZondaCrypto.

| Address | What it is | Activity | Detail |
|---|---|---|---|
| `0x2d8eA194902Bc55431420BD26Be92b0782dCe91D` | ZND token contract | 2024-10-21 → 2026-05-13, ≥10k native / 19 ERC-20 | [→](ethereum/znd-token.md) |
| `0x43a8a5b11b2f82866ad7dcef2c0a18e78e77399b` | ZND deployer | 2024-10-18 (single day), 5 native / 0 ERC-20 | [→](ethereum/znd-deployer.md) |
| `0xcb3d2be5386a13c87944f9384214ead9a6dba792` | ZNDStaking contract (owner of ZND token) | 2024-10-18 → 2026-04-05, 430 native / 369 ERC-20 | [→](ethereum/znd-staking.md) |
| `0x08d807a320d5986eb7c4f086bbab974c8db210da` | ZNDStaking owner EOA | 2024-10-18 (single day), 4 native / 0 ERC-20 | [→](ethereum/zndstaking-owner.md) |
| `0x41c31f690873ec5a642dd374e2f2dd1528d05730` | ZNDStaking `s_specialAccount` | 2024-12-17 → 2026-02-13, 14 native / 12 ERC-20 | [→](ethereum/znd-special-account.md) |
| `0x36ac695293d35bd90586b5353471c2004407ef6e` | ZNDStaking `s_withdrawalAccount` | no on-chain activity (never sent or received a transaction at the time of probing) | [→](ethereum/znd-withdrawal-account.md) |
| `0xae4f32dfa85b9e8c424a9604e7bf1d8128859943` | ZNDStaking `s_zndPlatform` | 2024-10-18 → 2026-03-28, 206 native / 193 ERC-20 | [→](ethereum/znd-platform.md) |
| `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07` | TMPL token contract (PKOl sponsorship vehicle) | 2026-01-29 → 2026-05-10, 126 native / 1 ERC-20 | [→](ethereum/tmpl-token.md) |
| `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4` | TMPLPools — deployer of TMPL; holds 86.03% of TMPL supply across 17 vesting pools (PARTIAL) | smart contract; deployed ~2026-01-28; 860,325,400 TMPL held | [→](ethereum/tmpl-pools.md) |
| `0xd3d11158cb21a852bffdabc5f2887bd06144ed71` | TMPLPools deployer EOA (PARTIAL) | 2026-01-27 (single day), 5 native / 0 ERC-20 | [→](ethereum/tmpl-pools-deployer.md) |
| `0xefa67cbf1378f174c8c49b645433561103488a43` | TMPLPools owner EOA (PARTIAL) | initial owner per `OwnershipTransferred` at deployment block 24326010 (2026-01-27); no subsequent ownership transfer observed | [→](ethereum/tmpl-pools-owner.md) |

## Ethereum — BitBay-era wallets

Wallets attributed to ZondaCrypto / BitBay by one or more primary sources (Bubblemaps `entity_id = "zonda"`; BlockSec MetaSleuth label). Rows attributed by a single primary source are PARTIAL tier; the BB-879882 row carries two independent primary sources (BlockSec MetaSleuth 2026-05-22 + Bubblemaps) and is CONFIRMED. Underlying transfers are CONFIRMED from on-chain data; their attribution to ZondaCrypto operations inherits the wallet's tier.

| Address | What it is | Tier | Activity | Detail |
|---|---|---|---|---|
| `0x56d943aea92b099228b31f01cd12bd4aa39b4778` | Zonda (BitBay) 0x56d943…4778 | PARTIAL | 2025-08-04 → 2026-05-13, ≥10k native / ≥10k ERC-20 | [→](ethereum/zonda-bitbay-56d943.md) |
| `0xb6be26445f21e41bc69197fe68f697fc1a862f19` | Zonda (BitBay) 0x56d943…4778 disbursement contract — native-ETH-only payout contract deployed and operated by `0x56d943…4778` | PARTIAL | 2025-08-04 → 2025-10-08, 806 normal / 1,701 internal / 0 ERC-20; deployer-only IN, fans out to 594 distinct recipients | [→](ethereum/zonda-bitbay-56d943-disbursement.md) |
| `0x879882c59d9cc548d6c0e7d0238e8aa40858b54f` | Zonda (BitBay) 0x879882…b54f — multichain deposit address (ETH + POL + ARB + OP via EVM-key-reuse propagation from the 2026-05-22 BlockSec attribution) | CONFIRMED | 2021-03-31 → 2026-04-02, 1,259 native / 2,112 ERC-20 | [→](ethereum/zonda-bitbay-879882.md) |
| `0x66b12dcff9f466f2a771e264b6d145bdd00e1327` | Zonda (BitBay) 0x66b12d…1327 | PARTIAL | 2025-02-21 → 2026-02-08, 11 native / 21 ERC-20 | [→](ethereum/zonda-bitbay-66b12d.md) |
| `0x3f1eea8dcda2b5620643aca1987d4780cae80539` | Zonda (BitBay) 0x3f1eea…0539 | PARTIAL | 2024-12-17 → 2026-03-29, 168 native / 3,329 ERC-20 | [→](ethereum/zonda-bitbay-3f1eea.md) |
| `0x4ff97a1bd55f7edb7f0da364d5a8ea2148ab0e4b` | Zonda (BitBay) 0x4ff97a…0e4b | PARTIAL | 2025-08-14 → 2026-01-30, 29 native / 72 ERC-20 | [→](ethereum/zonda-bitbay-4ff97a.md) |
| `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305` | Zonda (BitBay) 0xc7f05e…9305 | PARTIAL | 2019-05-01 → 2026-03-18, 2,029 native / 8 ERC-20 | [→](ethereum/zonda-bitbay-c7f05e.md) |
| `0xced004645e40f1bd5d11e6562e8fdbe9f4862f06` | Zonda (BitBay) 0xced004…2f06 | PARTIAL | 2022-08-31 → 2026-03-29, 472 events (227 IN / 245 OUT); deposit-receipt hop — 18 hildobby-tagged CEXes feed in, 100% of outbound to Zonda 5 | [→](ethereum/zonda-bitbay-ced004.md) |
| `0x3ef6683f2553af861f91194d23bdf8522d1f2eda` | Zonda (BitBay) 0x3ef668…2eda | PARTIAL | 2023-05-31 → 2026-03-29, 2,465 events (1,322 IN / 1,143 OUT); deposit-receipt hop — 17 hildobby-tagged CEXes feed in, 100% of outbound to Zonda 5 (~2.8× the throughput of the ced004 instance) | [→](ethereum/zonda-bitbay-3ef668.md) |

## Polygon — Zonda vanity-suffix cluster

A cluster of three Polygon addresses sharing a 4-byte vanity pattern, including the previously-attributed Zonda 6 address. Recorded as a single inventory item.

| Address | What it is | Activity | Detail |
|---|---|---|---|
| `0xd388…8046` family (3 addresses incl. Zonda 6) | Zonda Polygon-side vanity-suffix cluster | per-address activity in the cluster file (table) | [→](polygon/zonda-d388-family-polygon.md) |

A wallet's inclusion in this inventory does **not** depend on having recent activity — every primary-citation labelled wallet is listed regardless of whether it is currently active, dormant, or has never moved. Empty wallets are tagged as such (e.g. ZNDStaking `s_withdrawalAccount`) so downstream aggregation work doesn't silently skip them.

See [methodology.md](../methodology.md) for how attributions are established and what each confidence tier means.
