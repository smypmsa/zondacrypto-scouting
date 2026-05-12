# ZND `s_zndPlatform`

**Address:** `0xae4f32dfa85b9e8c424a9604e7bf1d8128859943`

**Chain:** Ethereum.

**Role:** Platform-side operator recorded in the `s_zndPlatform` state variable of the ZNDStaking contract.

**Confidence:** CONFIRMED.

## Attribution

Reading `s_zndPlatform` on the ZNDStaking contract returns this address.[^1] The role is defined in the contract's verified source.[^2] The on-chain chain from ZondaCrypto: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address has a substantial outbound nonce at the time of recording — consistent with operational, recurring use rather than a single-purpose admin key. It is also among the top-100 holders of the ZND token.

## Block-explorer link

https://etherscan.io/address/0xae4f32dfa85b9e8c424a9604e7bf1d8128859943

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x20dd50df` (`s_zndPlatform()`) returns `0x000000000000000000000000` + `ae4f32dfa85b9e8c424a9604e7bf1d8128859943`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
