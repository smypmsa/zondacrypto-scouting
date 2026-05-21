# TMPLPools owner

> **Plain-language summary.** The externally-owned account (EOA) recorded as the initial owner of the TMPLPools contract at deployment. TMPLPools is the smart contract that deployed the TMPL token and that holds 86.03% of TMPL supply across 17 vesting pools (see [tmpl-pools.md](tmpl-pools.md)). The owner has the privileged-action authority that the TMPLPools contract's `Ownable` pattern exposes. Attribution is recorded at PARTIAL tier — the on-chain ownership-event log is the only primary citation; no public name tag and no second independent label set name this address against ZondaCrypto.

**Address:** `0xefa67cbf1378f174c8c49b645433561103488a43`

**Chain:** Ethereum.

**Role:** Externally-owned account recorded by TMPLPools' `OwnershipTransferred` event as the contract's owner from deployment block 24326010 (2026-01-27). No subsequent `OwnershipTransferred` event has been observed on TMPLPools at the time of recording, so this address is the current owner as of 2026-05-21.

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

The TMPLPools contract's deployment transaction (`0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f`, block 24326010, 2026-01-27) emits an `OwnershipTransferred(previousOwner = 0x0000…0000, newOwner = 0xefa67cbf1378f174c8c49b645433561103488a43)` event from the TMPLPools contract.[^1] No later `OwnershipTransferred` event from TMPLPools is recorded against this address at the time of recording.

Per [methodology § Evidence types](../../methodology.md#evidence-types), the owner-of-an-already-attributed-contract relation is a **smart-contract relation** primary citation. It is the only primary citation currently recorded for this EOA; no public name tag is displayed on Etherscan as of 2026-05-21, and no second independent label set names this address against ZondaCrypto. Recorded as **PARTIAL** pending a second independent labelling.

### Sources checked and what came back

| Source | Result | Date |
|---|---|---|
| Etherscan public name tag | No public name tag displayed on the address page | 2026-05-21 |
| hildobby's Dune query 3237025 ("All Known EVM CEX Addresses") | Not present | 2026-05-21 |
| OFAC SDN ETH-address list | Not present | 2026-05-21 |
| BlockSec MetaSleuth API v3 | Not yet probed (no slot allocated; address surfaced 2026-05-21) | — |

## Activity (Ethereum, probed 2026-05-21)

The owner relation was established by the TMPLPools deployment transaction at block 24326010 (2026-01-27). A per-counterparty flow profile is not built for this entry: this wallet's role in the inventory is the smart-contract-authority relation, not an operational settlement flow. Activity is reproducible from the address alone via Etherscan v2 `account/txlist` and `account/tokentx`.

## Scope and negative space

This page records the on-chain owner relation between this EOA and the TMPLPools contract. It does not document:

- Who controls the EOA off-chain — that question is outside the public primary-citation gate.
- Whether the TMPLPools contract exposes any privileged-action functions beyond the `Ownable` pattern's standard set — the contract's verified source on Etherscan is the canonical reference for the action surface.
- Whether the owner has exercised any privileged actions on TMPLPools since deployment — that would require a per-action trace of the contract's event log and is not covered here.
- The natural-person identities behind the TMPLPools vesting pools — those are readable from the contract's verified source but are outside the scope of this page.

## Block-explorer link

https://etherscan.io/address/0xefa67cbf1378f174c8c49b645433561103488a43

## Citations

[^1]: Dune `tokens_ethereum.transfers` + `ethereum.logs` combined query recording `OwnershipTransferred` and contract-creation events on the ZND-token-suite contract set (ZND, ZNDStaking, TMPL, TMPLPools), executed 2026-05-21 as Dune query `7500518` execution `01KS5BTVNXMD3G7SR9EZ3QRFVN`. The TMPLPools contract (`0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4`) emits `OwnershipTransferred(0x0000…0000 → 0xefa67cbf1378f174c8c49b645433561103488a43)` in transaction `0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f` at block 24326010 (block_time 2026-01-27 11:56:11 UTC). Receipt mirrored at [`../../sources/dune/d7-znd-token-suite-operator-2026-05-21.json`](../../sources/dune/d7-znd-token-suite-operator-2026-05-21.json). https://etherscan.io/tx/0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f · https://etherscan.io/address/0xefa67cbf1378f174c8c49b645433561103488a43
