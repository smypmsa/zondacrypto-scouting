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

No material flow above the $1,000 USD-equivalent threshold on Ethereum. This address moves tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price (ZND / TMPL), or its on-chain activity is below the $1k-per-event threshold used elsewhere in this inventory. On-chain activity is non-zero but USD-equivalent unmeasurable at the same threshold used for the other Stage-1 wallets. Receipt: `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json`.

## Block-explorer link

https://etherscan.io/address/0x66b12dcff9f466f2a771e264b6d145bdd00e1327

[^1]: Bubblemaps token-graph expansion API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
