# Zonda (BitBay) (0xc7f05e…9305)

**Address:** `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth.

**Confidence:** PARTIAL.

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`.[^1] The entity description in the response links the operator at `zondacrypto.com`. No matching public name tag on Etherscan as of 2026-05-14; no row in hildobby's Dune compilation (query 3237025). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

## Activity (Ethereum, probed 2026-05-14)

- Native txs: first 2019-05-01 (block 7676630); most recent 2026-03-18 (block 24684058); 2,029 events (within a single 10,000-event Etherscan page — full count, not truncated).
- ERC-20 events: first ≈2019 (block range covered by `tokentx` paginated sweep); most recent 2020-11-07; 8 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile

This wallet was added to the inventory on 2026-05-14 after the BlockSec attribution above. Its full counterparty enumeration (a per-counterparty CSV in the style applied to the other wallets in this inventory) is not yet generated and is scheduled for the next counterparty-enumeration sweep across the inventory.

From the prior Dune-aggregated counterparty enumeration already run across the wallet inventory (Dune query `7482290`, execution `01KRGWD3EXCCWS6W63YM5M4B8R`, 2026-05-13), this address appears as a counterparty of three other ZondaCrypto wallets in this inventory — [Zonda 2](zonda-2.md), [Zonda 1](zonda-1.md), and [Zonda 3](zonda-3.md) — with cumulative **$57M flowed and 151 events** across that union. The earliest observed transfer with any of those three is 2020-09; the most recent is 2024-12.

## Block-explorer link

https://etherscan.io/address/0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-14 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, name_tag `"Zonda (BitBay): Deposit Address"`. Receipt at [`sources/blocksec/labels-2026-05-14.json`](../../sources/blocksec/labels-2026-05-14.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
