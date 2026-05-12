# Zonda Deposit Wallet (0x82c829…900c)

**Address:** `0x82c829237159287dac6fc62eb139e6a89195900c`

**Chain:** Ethereum.

**Role:** Deposit-side ZondaCrypto wallet.

**Confidence:** CONFIRMED.

## Attribution

Two independent primary label sources point to this address as a ZondaCrypto wallet:

1. **Bubblemaps** — the `addresses/token-top-holders` API for the ZND token returns this address with `address_details.label = "Zonda Deposit Wallet"` and `entity_id = "zonda"`.[^1]
2. **BlockSec MetaSleuth** — the `address-label/api/v3/labels` endpoint returns `main_entity = "Zonda (BitBay)"` under the `EXCHANGE` category.[^2] The receipt of the BlockSec response is preserved at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json).

In addition, Etherscan's address page shows this wallet transacts directly with `Zonda: Deposit Funder 1` (see [`zonda-deposit-funder-1.md`](zonda-deposit-funder-1.md)), consistent with the deposit-wallet role.

The address is currently a top-100 ZND holder (≈0.046% of supply).

## Block-explorer link

https://etherscan.io/address/0x82c829237159287dac6fc62eb139e6a89195900c

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
[^2]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`. Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
