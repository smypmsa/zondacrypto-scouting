# TMPLPools (TMPL deployer / vesting pool)

> **Plain-language summary.** The smart contract that deployed the TMPL (TeamPL Token) ERC-20 and that holds 86.03% of TMPL supply across 17 allocation pools with cliff periods and vesting schedules. Source-verified on Etherscan as `TMPLPools`. Attribution is at PARTIAL tier — the deployer-of-TMPL relation is the only primary citation; no public name tag on Etherscan, no second independent label set.

**Address:** `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4`

**Chain:** Ethereum.

**Role:** Smart contract that deployed the TMPL token and manages its vesting / pool allocations. Holds the supermajority of TMPL supply.

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan shows this address as the **Contract Creator** of the TMPL token contract `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07` (see [`tmpl-token.md`](tmpl-token.md)).[^1] The contract's source is verified on Etherscan with the name `TMPLPools`; it implements 17 allocation pools with cliff periods and per-pool vesting schedules. Etherscan's `tokenholdings` view records this contract as the **largest holder of TMPL** at 860,325,400 TMPL (86.03% of total supply).[^1]

Per [methodology § Evidence types](../../methodology.md#evidence-types), the deployer-of-an-already-attributed-contract relation is a **smart-contract relation** primary citation. It is the only primary citation recorded for this address; no public name tag is displayed on Etherscan as of 2026-05-15, and no second independent label set names this address against ZondaCrypto. Recorded as **PARTIAL** pending a second independent labelling.

### Sources checked and what came back

To make the PARTIAL tier concrete, this address has been probed against every free attribution source this inventory uses. Negative results recorded so the gap is machine-discoverable and the reader does not have to re-run them:

| Source | Result | Date |
|---|---|---|
| Etherscan public name tag | No public name tag displayed on the address page | 2026-05-15 |
| hildobby's Dune query 3237025 ("All Known EVM CEX Addresses") | Not present (8 Zonda-tagged rows checked; no match) | 2026-05-11 |
| Bubblemaps v2 `tokens/details` + `/holders` | `404 — No transfer data` / `404 — No holder found`; no `entity_id = "zonda"` label returned | 2026-05-12 |
| OFAC SDN ETH-address list | Not present (88 sanctioned ETH addresses on list) | 2026-05-14 |
| BlockSec MetaSleuth API v3 | Pending a clean re-query (the 2026-05-12 local probe row returned an empty response but its `address` field does not match this query — log integrity is being re-verified on the next quota cycle) | 2026-05-16 (queued) |

## Activity (Ethereum, probed 2026-05-15)

- This is a smart contract, not an externally-owned account.
- Deployed approximately 107 days before 2026-05-15 — consistent with the TMPL token's debut window (TMPL first ERC-20 event 2026-01-29 per [`tmpl-token.md`](tmpl-token.md)).
- Holdings: 860,325,400 TMPL (86.03% of supply) + 1 HEX (dust). Source: Etherscan token-holdings view, fetched 2026-05-15.

A full per-counterparty flow profile is not built for this entry: the contract holds tokens with no liquid USD-equivalent price on Dune (TMPL is unpriced in `tokens_ethereum.transfers`), so the USD-denominated flow-profile method used elsewhere in this inventory does not apply. Activity is reproducible from the address alone via Etherscan v2 `account/tokentx`.

## Scope and negative space

This page records the contract's role as deployer + dominant holder of the TMPL token. It does not document:

- The individual allocation pools or their beneficiary addresses — those are readable directly from the contract's verified source and from the token-holders list of TMPL, but are not enumerated here.
- The natural-person or corporate-entity identities behind those allocation pools — that is investigator-handoff territory beyond the public primary-citation gate.
- Whether the contract is upgradeable / proxy-controlled — `TMPLPools` is documented as a fixed-source vesting contract; no proxy / admin address has been identified at the time of recording.

## Block-explorer link

https://etherscan.io/address/0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4

## Citations

[^1]: Etherscan address page for `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4`, fetched 2026-05-15. Records the address as a smart contract named `TMPLPools`, the Contract Creator of TMPL token `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07`, and the largest holder of TMPL at 860,325,400 TMPL. No public name tag displayed. https://etherscan.io/address/0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4
