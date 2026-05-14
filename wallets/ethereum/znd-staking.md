# ZNDStaking

**Address:** `0xcb3d2be5386a13c87944f9384214ead9a6dba792`

**Chain:** Ethereum.

**Role:** Smart contract that manages ZondaCrypto's ZND-token staking and reward distribution. It is also the on-chain owner of the ZND token contract — supply control sits inside this contract, not in an EOA. Holds 74.27% of total ZND supply.

**Confidence:** CONFIRMED.

## Attribution

The contract was deployed by the ZND deployer (see [`znd-deployer.md`](znd-deployer.md)) in the same transaction sequence as the ZND token. Its source is verified on Etherscan as `ZNDStaking`.[^1] An on-chain reading of the ZND token's `owner()` returns this address, so ZND supply authority lives in this contract.[^2]

ZNDStaking exposes four address-typed state variables that record the operator-side accounts allowed to interact with the contract:

| State variable | Returned address | Role per the verified source |
|---|---|---|
| `owner()` | [`0x08d807a320d5986eb7c4f086bbab974c8db210da`](zndstaking-owner.md) | Ownable2Step owner — controls the contract |
| `s_specialAccount` | [`0x41c31f690873ec5a642dd374e2f2dd1528d05730`](znd-special-account.md) | Privileged operator account |
| `s_withdrawalAccount` | [`0x36ac695293d35bd90586b5353471c2004407ef6e`](znd-withdrawal-account.md) | Withdrawal-recipient account |
| `s_zndPlatform` | [`0xae4f32dfa85b9e8c424a9604e7bf1d8128859943`](znd-platform.md) | Platform-side operator |

Reading any of these is a single `eth_call` against the contract; the deterministic result is what links each EOA to the ZondaCrypto operator on chain.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-18 (block 20993307); most recent 2026-03-31 (block 24779368); 430 events.
- ERC-20 events: first 2024-10-18 (block 20993307); most recent 2026-04-05 (block 24813277); 369 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 21 |
| Total events (IN / OUT) | 34 / 335 |
| Active period | 2024-10-18 → 2026-04-05 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`znd-staking-counterparties.csv`](znd-staking-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x18bf7f1cf41f840a7cb21618d5d1c1af7ca3e908` | $0 | $0 | 0 / 7 | 2024-11-30 → 2026-03-31 |
| 2 | `0x344b16fe768582f69205897d240e2971b3ac0c09` | $0 | $0 | 0 / 12 | 2024-10-21 → 2025-04-28 |
| 3 | `0x36fdb8800968fb8b38d53ebce3c86f909c796372` | $0 | $0 | 0 / 26 | 2024-10-18 → 2026-03-31 |
| 4 | `0x3ce0935e2f28339d6f9f1068356a90bf6d3173e3` | $0 | $0 | 0 / 24 | 2024-10-21 → 2025-08-14 |
| 5 | `0x4c5e31774b09cf489c482a472bb78ae8c024c701` | $0 | $0 | 0 / 24 | 2024-10-21 → 2025-08-14 |
| 6 | `0x51c9a7324ced2d8c783c44eecafb00c1518ad849` | $0 | $0 | 1 / 0 | 2026-01-12 → 2026-01-12 |
| 7 | `0x53423085f352a12f0b4c51e00c512e130ae02b38` | $0 | $0 | 0 / 18 | 2024-10-21 → 2026-03-31 |
| 8 | `0x552002ec9504f3931019d63a8d992c98fcdf1eb7` | $0 | $0 | 0 / 30 | 2024-10-21 → 2026-02-20 |
| 9 | `0x6357d3843d715496257e338a878ab0b72040a918` | $0 | $0 | 1 / 0 | 2026-04-05 → 2026-04-05 |
| 10 | `0x719d74be74980f94b2b9ee670f94f540661f9f66` | $0 | $0 | 0 / 33 | 2024-10-21 → 2025-11-13 |
| 11 | `0x9a9fb1d7b263939ef7de83d5f69956b111f9a706` | $0 | $0 | 1 / 0 | 2026-01-03 → 2026-01-03 |
| 12 | `0x9ff1299f5abea9ff1789c86e1c972ac1b3a8d38d` | $0 | $0 | 0 / 20 | 2024-10-21 → 2025-06-16 |
| 13 | `0xae0a2dbdfdc0b9d1132b52796d5fcc9a19bd5dc3` | $0 | $0 | 0 / 1 | 2024-10-21 → 2024-10-21 |
| 14 | `0xaf3bf534d2b026b9c72cb6fb30a5f7f879a6f4f1` | $0 | $0 | 0 / 1 | 2024-10-21 → 2024-10-21 |
| 15 | `0xc5d2d690d683c6f7bb654e91fed293caec2a26b5` | $0 | $0 | 0 / 31 | 2024-10-21 → 2026-03-31 |
| 16 | `0xca4bde17f2a29fd041665cee2d206bc5c2ae507f` | $0 | $0 | 0 / 16 | 2024-10-21 → 2025-04-22 |
| 17 | `0xf70fdf0b14d8d9b4bac7ff549f0cabc987c1e01c` | $0 | $0 | 1 / 0 | 2025-03-12 → 2025-03-12 |
| 18 | `0xfdf5b0d1cd40223ef91027ce014cb4a31ac4ecf2` | $0 | $0 | 0 / 28 | 2024-10-21 → 2026-03-31 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`znd-staking-counterparties.csv`](znd-staking-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792

[^1]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
[^2]: `eth_call` to ZND token at `0x2d8eA194902Bc55431420BD26Be92b0782dCe91D` with selector `0x8da5cb5b` (`owner()`) returns `0xcb3d2be5386a13c87944f9384214ead9a6dba792`. Reproducible against any Ethereum archive RPC.
