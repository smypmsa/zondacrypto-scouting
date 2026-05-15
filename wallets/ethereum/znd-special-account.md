# ZND `s_specialAccount`

> **Plain-language summary.** The privileged operator account recorded in the `s_specialAccount` state variable of the ZNDStaking contract. Attribution is on-chain: reading the contract returns this address. Among the top-100 holders of the ZND token.

**Address:** `0x41c31f690873ec5a642dd374e2f2dd1528d05730`

**Chain:** Ethereum.

**Role:** Privileged operator account recorded in the `s_specialAccount` state variable of the ZNDStaking contract.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Reading `s_specialAccount` on the ZNDStaking contract returns this address.[^1] ZNDStaking is the contract that owns the ZND token (see [`znd-staking.md`](znd-staking.md)); the role of `s_specialAccount` is defined in its verified source.[^2] The on-chain chain from ZondaCrypto: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address is also among the top-100 holders of the ZND token.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-12-17 (block 21421223); most recent 2026-02-13 (block 24448611); 14 events.
- ERC-20 events: first 2024-12-17 (block 21421238); most recent 2026-01-12 (block 24218958); 12 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 6 |
| Total events (IN / OUT) | 9 / 4 |
| Active period | 2024-12-17 → 2026-01-12 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`znd-special-account-counterparties.csv`](znd-special-account-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x51c9a7324ced2d8c783c44eecafb00c1518ad849` | $0 | $0 | 1 / 0 | 2026-01-12 → 2026-01-12 |
| 2 | `0x9a9fb1d7b263939ef7de83d5f69956b111f9a706` | $0 | $0 | 1 / 0 | 2026-01-03 → 2026-01-03 |
| 3 | `0xc5d2d690d683c6f7bb654e91fed293caec2a26b5` | $0 | $0 | 1 / 0 | 2024-12-18 → 2024-12-18 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`znd-special-account-counterparties.csv`](znd-special-account-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x41c31f690873ec5a642dd374e2f2dd1528d05730

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x7ef6e8bd` (`s_specialAccount()`) returns `0x000000000000000000000000` + `41c31f690873ec5a642dd374e2f2dd1528d05730`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
