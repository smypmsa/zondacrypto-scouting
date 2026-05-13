# ZNDStaking owner

**Address:** `0x08d807a320d5986eb7c4f086bbab974c8db210da`

**Chain:** Ethereum.

**Role:** Externally-owned account that is the Ownable2Step owner of the ZNDStaking contract. Because ZNDStaking is in turn the owner of the ZND token contract, this EOA holds the top of ZondaCrypto's on-chain authority chain over the ZND token system.

**Confidence:** CONFIRMED.

## Attribution

Reading `owner()` on the ZNDStaking contract returns this address.[^1] ZNDStaking's source code is verified on Etherscan and inherits OpenZeppelin's `Ownable2Step`, where `owner()` is the contract's privileged-action authority.[^2] The on-chain link from ZondaCrypto runs: Zonda 5 → ZND deployer → ZNDStaking → this address.

The address has a low outbound nonce (3 transactions) at the time of recording — consistent with a purpose-built admin key rather than an operational hot wallet.

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2024-10-18 (block 20993348); most recent 2024-10-18 (block 20993396); 4 events.
- ERC-20 events: none

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

No material flow above the $1,000 USD-equivalent threshold on Ethereum. This address moves tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price (ZND / TMPL), or its on-chain activity is below the $1k-per-event threshold used elsewhere in this inventory. On-chain activity is non-zero but USD-equivalent unmeasurable at the same threshold used for the other Stage-1 wallets. Receipt: `case/sources/dune/stage1-per-wallet-totals-2026-05-13.json`.

## Block-explorer link

https://etherscan.io/address/0x08d807a320d5986eb7c4f086bbab974c8db210da

[^1]: `eth_call` to `0xcb3d2be5386a13c87944f9384214ead9a6dba792` with selector `0x8da5cb5b` (`owner()`) returns `0x000000000000000000000000` + `08d807a320d5986eb7c4f086bbab974c8db210da`. Reproducible against any Ethereum archive RPC.
[^2]: Etherscan, verified source for `ZNDStaking`. https://etherscan.io/address/0xcb3d2be5386a13c87944f9384214ead9a6dba792#code
