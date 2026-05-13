# Zonda 2

**Address:** `0x781229c7a798c33ec788520a6bbe12a79ed657fc`

**Chain:** Ethereum, Polygon.

**Role:** ZondaCrypto exchange wallet.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda 2 (Exchange)" on this address.[^1] Polygonscan carries the same "Zonda 2" name tag on the same address (key reused unchanged across chains).[^4] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses maintained on Dune Analytics.[^2] BlockSec's MetaSleuth address-label database independently attributes this address to the entity "BitBay" (the legacy brand of the same operator) under the EXCHANGE category.[^3]

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2021-09-01 (block 13140703); most recent 2026-04-13 (block 24869201); ≥ 10,000 events.
- ERC-20 events: first 2021-07-27 (block 12907119); most recent 2026-04-17 (block 24898630); 4,493 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Activity (Polygon, probed 2026-05-13)

- Native txs: first 2024-05-01; most recent 2026-03-24; 43 events.
- ERC-20 events (raw, including fake-token poisoning seeds): first 2021-09-10; most recent 2026-03-29; 426 events. Filtered to the canonical Polygon Tether contract (`0xc2132d05…58e8f`, current symbol `USDT0`), real-USDT activity is 64 events spanning 2024-02-06 → 2025-12-06.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each.

## Block-explorer links

- Ethereum: https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
- Polygon: https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc

[^1]: Etherscan, public name tag on Zonda 2. https://etherscan.io/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. https://dune.com/queries/3237025
[^3]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "BitBay"`, category `EXCHANGE`. Receipt at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
[^4]: Polygonscan, public name tag on Zonda 2. Verified by HTML fetch 2026-05-13. https://polygonscan.com/address/0x781229c7a798c33ec788520a6bbe12a79ed657fc
