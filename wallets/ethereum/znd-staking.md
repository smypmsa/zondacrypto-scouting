# ZNDStaking

**Address:** `0xcb3d2be5386a13c87944f9384214ead9a6dba792`

**Chain:** Ethereum.

**Role:** Smart contract that manages ZondaCrypto's ZND-token staking and reward distribution. It is also the on-chain owner of the ZND token contract — supply control sits inside this contract, not in an EOA. Holds 74.27% of total ZND supply.

**Confidence:** CONFIRMED.

## Attribution

The contract was deployed by the ZND deployer (see [`znd-deployer.md`](znd-deployer.md)) in the same transaction sequence as the ZND token. Its source is verified on Etherscan as `ZNDStaking`.[^1] An on-chain reading of the ZND token's `owner()` returns this address, so ZND supply authority lives in this contract.[^2]

ZNDStaking exposes four address-typed state variables that record the operator-side accounts allowed to interact with the contract:

| State variable | Returned address | Role per the verified source |
|---|---|---|
| `owner()` | [`0x08d807a320d5986eb7c4f086bbab974c8db210da`](zndstaking-owner.md) | Ownable2Step owner — controls the contract |
| `s_specialAccount` | [`0x41c31f690873ec5a642dd374e2f2dd1528d05730`](znd-special-account.md) | Privileged operator account |
| `s_withdrawalAccount` | [`0x36ac695293d35bd90586b5353471c2004407ef6e`](znd-withdrawal-account.md) | Withdrawal-recipient account |
| `s_zndPlatform` | [`0xae4f32dfa85b9e8c424a9604e7bf1d8128859943`](znd-platform.md) | Platform-side operator |

Reading any of these is a single `eth_call` against the contract; the deterministic result is what links each EOA to the ZondaCrypto operator on chain.

## Block-explorer link

https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792

[^1]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
[^2]: `eth_call` to ZND token at `0x2d8eA194902Bc55431420BD26Be92b0782dCe91D` with selector `0x8da5cb5b` (`owner()`) returns `0xcb3d2be5386a13c87944f9384214ead9a6dba792`. Reproducible against any Ethereum archive RPC.
