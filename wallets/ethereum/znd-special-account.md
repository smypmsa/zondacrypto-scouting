# ZND `s_specialAccount`

**Address:** `0x41c31f690873ec5a642dd374e2f2dd1528d05730`

**Chain:** Ethereum.

**Role:** Privileged operator account recorded in the `s_specialAccount` state variable of the ZNDStaking contract.

**Confidence:** CONFIRMED.

## Attribution

Reading `s_specialAccount` on the ZNDStaking contract returns this address.[^1] ZNDStaking is the contract that owns the ZND token (see [`znd-staking.md`](znd-staking.md)); the role of `s_specialAccount` is defined in its verified source.[^2] The on-chain chain from ZondaCrypto: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address is also among the top-100 holders of the ZND token.

## Block-explorer link

https://etherscan.io/address/0x41c31f690873ec5a642dd374e2f2dd1528d05730

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x7ef6e8bd` (`s_specialAccount()`) returns `0x000000000000000000000000` + `41c31f690873ec5a642dd374e2f2dd1528d05730`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
