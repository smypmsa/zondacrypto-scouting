# ZND `s_withdrawalAccount`

**Address:** `0x36ac695293d35bd90586b5353471c2004407ef6e`

**Chain:** Ethereum.

**Role:** Withdrawal-recipient account recorded in the `s_withdrawalAccount` state variable of the ZNDStaking contract.

**Confidence:** CONFIRMED.

## Attribution

Reading `s_withdrawalAccount` on the ZNDStaking contract returns this address.[^1] The role is defined in the contract's verified source.[^2] The on-chain chain from ZondaCrypto: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address has a zero outbound nonce at the time of recording — it has never sent a transaction itself.

## Block-explorer link

https://etherscan.io/address/0x36ac695293d35bd90586b5353471c2004407ef6e

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x4ec1b858` (`s_withdrawalAccount()`) returns `0x000000000000000000000000` + `36ac695293d35bd90586b5353471c2004407ef6e`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
