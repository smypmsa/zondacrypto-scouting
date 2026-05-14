# ZND `s_zndPlatform`

**Address:** `0xae4f32dfa85b9e8c424a9604e7bf1d8128859943`

**Chain:** Ethereum.

**Role:** Platform-side operator recorded in the `s_zndPlatform` state variable of the ZNDStaking contract.

**Confidence:** CONFIRMED.

## Attribution

Reading `s_zndPlatform` on the ZNDStaking contract returns this address.[^1] The role is defined in the contract's verified source.[^2] The on-chain chain from ZondaCrypto: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address has a substantial outbound nonce at the time of recording — consistent with operational, recurring use rather than a single-purpose admin key. It is also among the top-100 holders of the ZND token.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-18 (block 20992782); most recent 2026-03-20 (block 24699606); 206 events.
- ERC-20 events: first 2024-10-24 (block 21035110); most recent 2026-03-28 (block 24752665); 193 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 100 |
| Total events (IN / OUT) | 137 / 151 |
| Active period | 2024-10-18 → 2026-03-28 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`znd-platform-counterparties.csv`](znd-platform-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x0262202acd9539f9f7c7b6096c6cd3e66efa1b98` | $140 | $317 | 1 / 3 | 2024-10-28 → 2026-01-22 |
| 2 | `0x3ce0935e2f28339d6f9f1068356a90bf6d3173e3` | $8 | $121 | 1 / 3 | 2024-10-21 → 2025-08-14 |
| 3 | `0x4c5e31774b09cf489c482a472bb78ae8c024c701` | $8 | $121 | 1 / 3 | 2024-10-21 → 2025-08-14 |
| 4 | `0x719d74be74980f94b2b9ee670f94f540661f9f66` | $8 | $121 | 1 / 3 | 2024-10-21 → 2025-08-14 |
| 5 | `0x552002ec9504f3931019d63a8d992c98fcdf1eb7` | $8 | $109 | 1 / 3 | 2024-10-21 → 2025-08-14 |
| 6 | `0x36fdb8800968fb8b38d53ebce3c86f909c796372` | $12 | $104 | 1 / 2 | 2024-10-24 → 2025-08-14 |
| 7 | `0x344b16fe768582f69205897d240e2971b3ac0c09` | $8 | $62 | 6 / 5 | 2024-10-21 → 2025-05-21 |
| 8 | `0xca4bde17f2a29fd041665cee2d206bc5c2ae507f` | $9 | $47 | 1 / 3 | 2024-10-21 → 2025-01-08 |
| 9 | `0xc5d2d690d683c6f7bb654e91fed293caec2a26b5` | $9 | $47 | 2 / 3 | 2024-10-21 → 2025-06-17 |
| 10 | `0xfdf5b0d1cd40223ef91027ce014cb4a31ac4ecf2` | $10 | $45 | 2 / 3 | 2024-10-21 → 2025-07-16 |
| 11 | `0x9ff1299f5abea9ff1789c86e1c972ac1b3a8d38d` | $8 | $30 | 1 / 2 | 2024-10-21 → 2025-01-08 |
| 12 | `0x53423085f352a12f0b4c51e00c512e130ae02b38` | $9 | $26 | 2 / 3 | 2024-10-21 → 2024-10-30 |
| 13 | `0xae0a2dbdfdc0b9d1132b52796d5fcc9a19bd5dc3` | $11 | $13 | 3 / 2 | 2024-10-21 → 2024-10-30 |
| 14 | `0xaf3bf534d2b026b9c72cb6fb30a5f7f879a6f4f1` | $10 | $13 | 1 / 1 | 2024-10-21 → 2024-10-24 |
| 15 | `0x18bf7f1cf41f840a7cb21618d5d1c1af7ca3e908` | $0 | $18 | 0 / 1 | 2024-11-30 → 2024-11-30 |
| 16 | `0x6fbb2804e362c1e879c0930705f6f196bca5b069` | $0 | $9 | 2 / 4 | 2025-04-30 → 2025-11-20 |
| 17 | `0xe26eb18ef05b25606a384d57117fb65c2ec6af92` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 18 | `0x5e81ef911f825ee2116f0bb6fe1576735638da49` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 19 | `0x18aa4786ec27330106f78bae7bc1e582f79710d0` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 20 | `0x468fc8bf5986919fc805528b4eb71ff72c705cb7` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 21 | `0x4698d2ed7b040f45e519949c24aaca4d65303a1c` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 22 | `0x5a48e5f7ac2cabe9e2eecb70fc23a6e17ad90c18` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 23 | `0x69a5fb54e4abe160b7fa26b4516a9c8473f9fa89` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 24 | `0x7fb47d214897c35564a6a9c3126982ac5a4133e0` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 25 | `0x80a1866f12e24e15e9226730a49647f10046e29e` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 26 | `0x82b8033ad2e2408b961971cd195f0dfcbd940d7d` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 27 | `0xaa881b4e43b2c5edebde7f4758dc34a74b6bbae0` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 28 | `0xbac0cf7b44a4bda7231b78c9d2fa498f4b68d0dd` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 29 | `0xbda21e5cf4b3e482545f06dcc396813c1e1d5553` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 30 | `0xcbd467c3e8d88e22d30eb8f345d30d2fdd8a5c81` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 31 | `0xd61003d766f39b5f5348cf3da17a9dbc690f0971` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 32 | `0xdbfa67114961754d0be14caaaf7c6156ec44a47c` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 33 | `0xed9886088eb88c984ea067ecdb1108351eca60a2` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 34 | `0xefa67cbf1378f174c8c49b645433561103488a43` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 35 | `0xfba0831b8ee2faa338b51eadff8f458e7eb412a9` | $0 | $3 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 36 | `0x000c41e9ed80bb9cde40c68147fa99ac800d0000` | $0 | $0 | 0 / 1 | 2025-12-16 → 2025-12-16 |
| 37 | `0x026155a4cb4bc5a184c502fe21ee16d96389eb98` | $0 | $0 | 0 / 1 | 2026-01-22 → 2026-01-22 |
| 38 | `0x0262dc53a81a5298c6fe615d379c141b09731b98` | $0 | $0 | 1 / 0 | 2026-01-22 → 2026-01-22 |
| 39 | `0x026cc36d526958eb7bd1edd5fcc0ebdf0a4a1b98` | $0 | $0 | 1 / 0 | 2026-01-22 → 2026-01-22 |
| 40 | `0x026d0ed38c3e860a156aab21644a1e2344fa1b98` | $0 | $0 | 0 / 1 | 2026-01-22 → 2026-01-22 |
| 41 | `0x18a25521354c80ca995174147a5c589b4f7110d0` | $0 | $0 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 42 | `0x26ca7aefbc73cb20364df9bba4fdf642c52a60e4` | $0 | $0 | 1 / 0 | 2025-10-08 → 2025-10-08 |
| 43 | `0x344b17ce45436fc8e6193529644ff19d16771c09` | $0 | $0 | 0 / 1 | 2025-05-24 → 2025-05-24 |
| 44 | `0x468742cf68962c953bac2b9a6368a10cfa2e6cb7` | $0 | $0 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 45 | `0x4692ce4ef4b4360320757c7ffb39251e1562ba1c` | $0 | $0 | 0 / 1 | 2026-01-29 → 2026-01-29 |
| 46 | `0x46983b85dc028026e4aff356155452ddc4503a1c` | $0 | $0 | 1 / 0 | 2026-01-29 → 2026-01-29 |
| 47 | `0x469876a11a9e4c23987e097100b173f6b4623a1c` | $0 | $0 | 1 / 0 | 2026-02-03 → 2026-02-03 |
| 48 | `0x469882eee4dc292402b8c89deb46d5d7bab23a1c` | $0 | $0 | 0 / 1 | 2026-02-08 → 2026-02-08 |
| 49 | `0x51bd024dc19be14c56b622106e10c475cfd9164e` | $0 | $0 | 0 / 1 | 2025-04-28 → 2025-04-28 |
| 50 | `0x51bdd01f32f203bf3f8d5b3efaab992feda6764e` | $0 | $0 | 0 / 1 | 2025-04-28 → 2025-04-28 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`znd-platform-counterparties.csv`](znd-platform-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0xae4f32dfa85b9e8c424a9604e7bf1d8128859943

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x20dd50df` (`s_zndPlatform()`) returns `0x000000000000000000000000` + `ae4f32dfa85b9e8c424a9604e7bf1d8128859943`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
