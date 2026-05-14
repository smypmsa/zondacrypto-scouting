# ZND deployer

**Address:** `0x43a8a5b11b2f82866ad7dcef2c0a18e78e77399b`

**Chain:** Ethereum.

**Role:** Externally-owned account that deployed the ZND token contract on 2024-10-18.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "ZND: Deployer" on this address.[^1] The contract-creation transaction `0xa200bfe88a341e69cd12744da545ffb2f0da9b1808c6a536d897a039efe88e30`, in which this account deployed the ZND token contract at `0x2d8eA194902Bc55431420BD26Be92b0782dCe91D` (see [znd-token.md](znd-token.md)), records the relation on chain.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-18 (block 20992003); most recent 2024-10-18 (block 20993351); 5 events.
- ERC-20 events: none

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 1 |
| Total events (IN / OUT) | 2 / 1 |
| Active period | 2024-10-18 → 2024-10-18 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`znd-deployer-counterparties.csv`](znd-deployer-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`znd-deployer-counterparties.csv`](znd-deployer-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x43a8a5b11b2f82866ad7dcef2c0a18e78e77399b

[^1]: Etherscan, public name tag on ZND: Deployer. https://etherscan.io/address/0x43a8a5b11b2f82866ad7dcef2c0a18e78e77399b
