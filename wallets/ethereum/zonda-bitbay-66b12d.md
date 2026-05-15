# Zonda (BitBay) (0x66b12d…1327)

**Address:** `0x66b12dcff9f466f2a771e264b6d145bdd00e1327`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed wallet per Bubblemaps.

**Confidence:** PARTIAL.

## Attribution

Bubblemaps' `addresses/expand/magic` endpoint, queried while exploring the neighbourhood of the ZND token's top holders, returns this address with `label = "Zonda (BitBay) (0x66…1327)"` and `entity_id = "zonda"`.[^1] No matching row in hildobby's Dune compilation; no public name tag on Etherscan. Bubblemaps is the sole primary source at this time.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2025-02-21 (block 21893924); most recent 2026-02-03 (block 24374048); 11 events.
- ERC-20 events: first 2025-02-21 (block 21893923); most recent 2026-02-08 (block 24410592); 21 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

No material flow above the $1,000 USD-equivalent threshold on Ethereum. This address moves tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price (ZND / TMPL), or its on-chain activity is below the $1k-per-event threshold used elsewhere in this inventory. On-chain activity is non-zero but USD-equivalent unmeasurable at the same threshold used for the other wallets in this inventory. Receipt: `../../sources/dune/inventory-per-wallet-totals-2026-05-13.json`.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0xead6595703fa97174e67d86998ecab7994ae880d` | $0 | $270 | 0 / 2 | 2026-01-30 → 2026-01-30 |
| 2 | `0x075bb12865d9470f0d0613a9fbe9e7b78ece8a73` | $0 | $0 | 0 / 4 | 2025-09-02 → 2025-09-02 |
| 3 | `0x075bac49cbf9390313367be1a199002566ff8a73` | $0 | $0 | 0 / 4 | 2025-09-02 → 2025-09-02 |
| 4 | `0xead6fd0a8ea83d26dc840ea565b4099b0926880d` | $0 | $0 | 1 / 0 | 2026-02-03 → 2026-02-03 |
| 5 | `0x075b798122a0c0030d992d3d76fe357a9e058a73` | $0 | $0 | 0 / 2 | 2025-09-01 → 2025-09-01 |
| 6 | `0xead68368448f60d9d97f18dd7c742e6b2e42880d` | $0 | $0 | 1 / 0 | 2026-01-30 → 2026-01-30 |
| 7 | `0xead6cd56c337bea5493cde72a3540b6ae476880d` | $0 | $0 | 0 / 1 | 2026-02-08 → 2026-02-08 |
| 8 | `0x6d7a3bfdc702d9d3ec0dce728d6796e0b44cb106` | $0 | $0 | 0 / 4 | 2025-02-21 → 2025-06-30 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-bitbay-66b12d-counterparties.csv`](zonda-bitbay-66b12d-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x66b12dcff9f466f2a771e264b6d145bdd00e1327

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x0d0707963952f2fba59dd06f2b425ace40b492fe` | Gate.io 1 | $0 | $0 | 1 / 0 |

