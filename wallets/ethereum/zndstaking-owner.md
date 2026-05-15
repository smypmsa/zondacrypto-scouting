# ZNDStaking owner

> **Plain-language summary.** The EOA at the top of ZondaCrypto's on-chain authority chain over the ZND token. ZNDStaking's `owner()` returns this address, and ZNDStaking in turn owns the ZND token contract. Low outbound nonce (3 transactions) — consistent with a purpose-built admin key rather than an operational hot wallet.

**Address:** `0x08d807a320d5986eb7c4f086bbab974c8db210da`

**Chain:** Ethereum.

**Role:** Externally-owned account that is the Ownable2Step owner of the ZNDStaking contract. Because ZNDStaking is in turn the owner of the ZND token contract, this EOA holds the top of ZondaCrypto's on-chain authority chain over the ZND token system.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Reading `owner()` on the ZNDStaking contract returns this address.[^1] ZNDStaking's source code is verified on Etherscan and inherits OpenZeppelin's `Ownable2Step`, where `owner()` is the contract's privileged-action authority.[^2] The on-chain link from ZondaCrypto runs: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address has a low outbound nonce (3 transactions) at the time of recording — consistent with a purpose-built admin key rather than an operational hot wallet.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-18 (block 20993348); most recent 2024-10-18 (block 20993396); 4 events.
- ERC-20 events: none

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 2 |
| Total events (IN / OUT) | 1 / 2 |
| Active period | 2024-10-18 → 2024-10-18 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`zndstaking-owner-counterparties.csv`](zndstaking-owner-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x36fdb8800968fb8b38d53ebce3c86f909c796372` | $0 | $22 | 0 / 2 | 2024-10-18 → 2024-10-18 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zndstaking-owner-counterparties.csv`](zndstaking-owner-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x08d807a320d5986eb7c4f086bbab974c8db210da

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x8da5cb5b` (`owner()`) returns `0x000000000000000000000000` + `08d807a320d5986eb7c4f086bbab974c8db210da`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
