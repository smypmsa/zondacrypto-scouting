# ZND token

> **Plain-language summary.** The ERC-20 token contract issued by ZondaCrypto on 2024-10-18. Attributed by the Etherscan public token tag plus ZondaCrypto's own announcement post. The contract was deployed by the EOA documented at [`znd-deployer.md`](znd-deployer.md) and is owned on-chain by the ZNDStaking contract.

**Address:** `0x2d8eA194902Bc55431420BD26Be92b0782dCe91D`

**Chain:** Ethereum.

**Role:** ERC-20 token contract issued by ZondaCrypto.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan carries the public token tag "ZND: ZND Token" on this contract.[^1] ZondaCrypto's own announcement of the token's debut references this contract address.[^2] The contract was deployed on 2024-10-18 in transaction `0xa200bfe88a341e69cd12744da545ffb2f0da9b1808c6a536d897a039efe88e30` by the EOA documented at [znd-deployer.md](znd-deployer.md).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-21 (block 21012460); most recent 2026-05-13 (block 25085168); ≥ 10,000 events.
- ERC-20 events: first 2024-10-29 (block 21069997); most recent 2026-04-02 (block 24791147); 19 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 12 |
| Total events (IN / OUT) | 19 / 0 |
| Active period | 2024-10-29 → 2026-04-02 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`znd-token-counterparties.csv`](znd-token-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xdd6c83663007f7fb6b1966cd08cd2d0889f4802e` | $29 | $0 | 1 / 0 | 2025-01-07 → 2025-01-07 |
| 2 | `0x00e2b6d170740c15bf9fb01d0b6e77c0d4510e32` | $0 | $0 | 1 / 0 | 2026-02-27 → 2026-02-27 |
| 3 | `0x110956c46f3419fba8707cd8dd00593792bfc0ff` | $0 | $0 | 1 / 0 | 2024-10-30 → 2024-10-30 |
| 4 | `0x3339a8704d934b141e45fc78f215dff82d598fb2` | $0 | $0 | 1 / 0 | 2024-10-29 → 2024-10-29 |
| 5 | `0x5e3699948fad1e7b2cac3926958e817ee826f265` | $0 | $0 | 1 / 0 | 2025-01-11 → 2025-01-11 |
| 6 | `0x6357d3843d715496257e338a878ab0b72040a918` | $0 | $0 | 1 / 0 | 2026-04-02 → 2026-04-02 |
| 7 | `0x7444590c145f0084eaa1b9270c4eccc8c2c9fe2c` | $0 | $0 | 1 / 0 | 2025-01-26 → 2025-01-26 |
| 8 | `0xc4596ab731991aa3b96272f24a9ec3f325a1a6ef` | $0 | $0 | 1 / 0 | 2025-01-11 → 2025-01-11 |
| 9 | `0xc97dfc795b046653df9d06f022e7676190b5f406` | $0 | $0 | 1 / 0 | 2025-01-28 → 2025-01-28 |
| 10 | `0xdf87866b9ff81d590d2f1cb2670c1af0f974be05` | $0 | $0 | 1 / 0 | 2024-10-29 → 2024-10-29 |
| 11 | `0xf70fdf0b14d8d9b4bac7ff549f0cabc987c1e01c` | $0 | $0 | 1 / 0 | 2025-03-12 → 2025-03-12 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`znd-token-counterparties.csv`](znd-token-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/token/0x2d8eA194902Bc55431420BD26Be92b0782dCe91D

[^1]: Etherscan, token tag "ZND: ZND Token". https://etherscan.io/token/0x2d8eA194902Bc55431420BD26Be92b0782dCe91D
[^2]: ZondaCrypto news, "Discover the ZND Token". https://zondacrypto.com/en/news/discover-the-znd-token
