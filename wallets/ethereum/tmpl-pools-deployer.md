# TMPLPools deployer

> **Plain-language summary.** The externally-owned account (EOA) that deployed the TMPLPools contract on 2026-01-27. TMPLPools is itself the smart contract that deployed the TMPL token and that holds 86.03% of TMPL supply across 17 vesting pools (see [tmpl-pools.md](tmpl-pools.md)). Attribution rests on a single primary source — the contract-creation transaction itself — so this address is recorded at PARTIAL tier. Five-transaction lifetime; no other operational activity observed.

**Address:** `0xd3d11158cb21a852bffdabc5f2887bd06144ed71`

**Chain:** Ethereum.

**Role:** Externally-owned account that deployed the TMPLPools contract (`0x80140b93…f4`) on 2026-01-27. TMPLPools is the deployer of and supermajority holder of the TMPL token (`0xc2FdA18D…07`); see [tmpl-pools.md](tmpl-pools.md) and [tmpl-token.md](tmpl-token.md).

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan v2 `account/txlist` records this address as the `from` of transaction `0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f` (block 24326010, 2026-01-27), in which it deployed the TMPLPools contract at `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4`.[^1] The TMPLPools contract's constructor in the same transaction then deployed the TMPL token at `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07`.[^1]

Per [methodology § Evidence types](../../methodology.md#evidence-types), the deployer-of-an-already-attributed-contract relation is a **smart-contract relation** primary citation. It is the only primary citation currently recorded for this EOA: no public name tag is displayed on Etherscan as of 2026-05-21, and no second independent label set names this address against ZondaCrypto. Recorded as **PARTIAL** pending a second independent labelling.

The address has only five lifetime transactions on Ethereum at the time of recording — consistent with a single-purpose deployer key, the same operational shape as `znd-deployer` (`0x43a8a5b1…99b`, see [znd-deployer.md](znd-deployer.md)) which deployed the ZND token suite under the same single-purpose pattern.

### Sources checked and what came back

To make the PARTIAL tier concrete, this address has been probed against every free attribution source this inventory uses. Negative results are recorded so the gap is machine-discoverable.

| Source | Result | Date |
|---|---|---|
| Etherscan public name tag | No public name tag displayed on the address page | 2026-05-21 |
| hildobby's Dune query 3237025 ("All Known EVM CEX Addresses") | Not present | 2026-05-21 |
| OFAC SDN ETH-address list | Not present | 2026-05-21 |
| BlockSec MetaSleuth API v3 | Not yet probed (no slot allocated; address surfaced 2026-05-21) | — |

## Activity (Ethereum, probed 2026-05-21)

- Native txs: 5 events. Single-day activity profile consistent with a single-purpose deployer EOA.
- ERC-20 events: none.
- Contract creation: TMPLPools (`0x80140b93…f4`) at block 24326010, 2026-01-27. The constructor of TMPLPools in the same transaction created TMPL (`0xc2FdA18D…07`).

Source: Etherscan v2 `account/txlist` + `account/txlistinternal` (chainid 1). The address returns "No transactions found" on Polygon and Arbitrum at the time of probing. Free-tier coverage on Base / Optimism / zkSync / BSC / Avalanche-C was not available; those chains are not assessed here.

## Scope and negative space

This page records the contract-creation relation between this EOA and TMPLPools. It does not document:

- Who controls the EOA off-chain — that question is outside the public primary-citation gate.
- Whether the EOA holds any token balances beyond the gas-token (native ETH) it spent — Etherscan's token-holdings view at the time of recording shows no token positions.
- Any onward authority chain over TMPL — TMPLPools is itself a smart contract; the natural-person beneficiaries of its vesting pools are documented in the contract's verified source and are not enumerated here.

## Block-explorer link

https://etherscan.io/address/0xd3d11158cb21a852bffdabc5f2887bd06144ed71

## Citations

[^1]: Etherscan v2 `account/txlist` and `account/txlistinternal` for `0xd3d11158cb21a852bffdabc5f2887bd06144ed71`, fetched 2026-05-21. Records `to = null` / `contractAddress = 0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4` for transaction `0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f` at block 24326010 (timestamp 1769514971). The same transaction's internal-trace record shows TMPLPools (`from = 0x80140b93…f4`) then creating TMPL at `0xc2fda18d62c8688902741da1e3c5be65c86bab07`. Receipt mirrored at [`../../sources/eth-archive/e6-token-creators-2026-05-21.json`](../../sources/eth-archive/e6-token-creators-2026-05-21.json). https://etherscan.io/address/0xd3d11158cb21a852bffdabc5f2887bd06144ed71 · https://etherscan.io/tx/0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f
