# Zonda (BitBay) 0x56d943…4778 disbursement contract (`0xb6be264…2f19`)

> **Plain-language summary.** A native-ETH-only disbursement smart contract deployed and operated by the ZondaCrypto / BitBay-attributed wallet `0x56d943ae…4778` (see [`zonda-bitbay-56d943.md`](zonda-bitbay-56d943.md)). The deployer is the contract's sole caller across every recorded transaction; the contract fans each payment out to a wide set of recipient addresses via a single `multisendEther` method. Over a ~9-week active window (2025-08-04 → 2025-10-08) it disbursed 39.10 ETH across 805 deployer-funded calls into 1,701 native-ETH transfers to 594 distinct recipients, with custody net-zero (every wei in is paid out in the same window). Attribution is at PARTIAL tier — the deployer-of-contract relation to a single-primary-source-attributed wallet is the only primary citation, and the deployer itself sits at PARTIAL.

**Address:** `0xb6be26445f21e41bc69197fe68f697fc1a862f19`

**Chain:** Ethereum.

**Role:** Native-ETH disbursement smart contract operated by Zonda (BitBay) `0x56d943…4778`. Behavioural shape (deployer-only IN, wide-fanout small-amount OUT, no ERC-20 footprint) matches customer-withdrawal disbursement infrastructure.

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Etherscan records `0x56d943aea92b099228b31f01cd12bd4aa39b4778` as the Contract Creator of this address at deployment transaction `0xb3ccd233…374fc` (block 23066530, 2025-08-04).[^1] The deployer is in turn attributed to ZondaCrypto / BitBay by Bubblemaps (`entity_id = "zonda"`, `is_cex = true`) — see the deployer wallet page [`zonda-bitbay-56d943.md`](zonda-bitbay-56d943.md) for that primary-source receipt.

Per [methodology § Evidence types](../../methodology.md#evidence-types), the deployer-of-an-already-attributed-contract relation is a **smart-contract relation** primary citation. Because the deployer itself is at PARTIAL tier, this contract inherits PARTIAL and does not become CONFIRMED via the deployment relation alone. Recorded as **PARTIAL** pending a second independent labelling (a public name tag on Etherscan or a BlockSec MetaSleuth label on either this contract or its deployer would resolve it to CONFIRMED).

Structural corroboration on-chain: across the contract's entire recorded life, 805 of 805 normal IN transactions (100%) originate from the deployer, no other caller is ever observed, the only function selector seen is `multisendEther(address[],uint256[])` (`0xab883d28`), and the contract holds zero balance at the time of probing — i.e. every wei the deployer sends in is paid out internally in the same window.[^2]

### Sources checked and what came back

| Source | Result | Date |
|---|---|---|
| Etherscan public name tag | No public name tag displayed on the address page | 2026-05-21 |
| Etherscan source-code verification | Source not verified; bytecode-only | 2026-05-21 |
| hildobby's Dune query 3237025 ("All Known EVM CEX Addresses") | Not present | 2026-05-21 |
| BlockSec MetaSleuth API v3 | Not yet probed (smart contracts are not the primary target of the BlockSec address-label index; queue prioritises EOAs) | n/a |
| Bubblemaps v2 entity index | Not present (Bubblemaps indexes EOAs against `entity_id = "zonda"`; the deployer is in that index, this contract is not) | 2026-05-21 |

## Activity (Ethereum, probed 2026-05-21)

- This is a smart contract, not an externally-owned account.
- Deployed 2025-08-04 (block 23066530) by `0x56d943ae…4778`.
- First post-deployment call: 2025-08-04. Most recent call: 2025-10-08. Active window: ~9 weeks (65 days).
- Native-ETH transactions: 806 normal (1 deployment + 805 deployer-funded calls) + 1,701 internal value-transfers.
- ERC-20 / ERC-721 transfers: 0 / 0. Token-mix is native ETH only.
- Balance at probe time: 0 wei.
- Distinct counterparties (combined IN + OUT side): 595 (1 deployer + 594 internal-tx recipients).

Source: Etherscan v2 (`account.txlist` + `account.txlistinternal` + `account.tokentx` + `account.tokennfttx` + `contract.getsourcecode` + `account.balance`), chainid=1. Receipt: [`../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json`](../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json).

## Flow profile (Ethereum, Etherscan v2 full-history aggregation, probed 2026-05-21)

Native-ETH-only flow. No ERC-20 transfers; no Dune USD-pricing layer applied. The "USD" column is omitted because every value here is denominated in native ETH and no conversion is asserted by this page.

| Metric | Value |
|---|---|
| Gross IN (native ETH, normal txs) | 39.10332519 ETH from 1 distinct counterparty (the deployer) across 805 events |
| Gross OUT (native ETH, internal txs) | 39.10332519 ETH to 594 distinct counterparties across 1,701 events |
| Net balance change over lifetime | 0 ETH (every wei in is paid out internally) |
| Token-mix | Native ETH only (0 ERC-20 / 0 ERC-721 transfers) |
| Active window | 2025-08-04 → 2025-10-08 (~9 weeks) |
| Access pattern | Deployer-only normal-tx caller (805/805) |
| Method-selector observed | `multisendEther(address[] _contributors, uint256[] _balances)` (`0xab883d28`) |

**Confidence:** CONFIRMED on totals, active window, deployer-only access pattern, and zero-ERC-20 footprint — each is reproducible from Etherscan v2 against the contract address alone. PARTIAL on the operator attribution itself (inherited from the deployer's PARTIAL tier).

### Counterparties also in this inventory

| Counterparty | Inbound ETH | Outbound ETH | Events (IN / OUT) |
|---|---|---|---|
| Zonda (BitBay) 0x56d943…4778 (deployer) `0x56d943ae…4778` | 39.10332519 | 0 | 805 / 0 |

The deployer is the contract's sole funder; no other inventory wallet appears on either side of the flow profile.

### External counterparties — confirmed via public name tag

None. No recipient address in the 594-counterparty OUT set carries an Etherscan public name tag verified by fresh HTML fetch on 2026-05-21, and none appears in hildobby's Dune query 3237025 attribution set.

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** All 594 internal-tx recipient addresses are unattributed in any free public attribution source as of 2026-05-21 (no Etherscan public name tag, not in hildobby's CEX-address Dune query, not in Bubblemaps' `entity_id` index). The OUT side aggregates 39.10332519 ETH across 1,701 events to these 594 addresses; the highest single-recipient event count is 66 (`0x49016964…0de1c`), and the top-10 recipients by event-count receive between 20 and 66 transfers each — long-tail wide-fanout pattern, not a small high-frequency operator set.

The behavioural signature (deployer-only IN, wide-fanout small-amount OUT to a long tail of one-time-ish addresses, native-ETH-only token mix) is consistent with customer-withdrawal disbursement infrastructure: a payout contract that the operator funds from its own wallet and that distributes those funds in batched calls to many customer recipients. This page records that signature; it does not attempt to identify the natural-person or corporate-entity beneficiaries behind the 594 recipient addresses.

## Scope and negative space

This page records the contract's role as a deployer-only-funded, native-ETH disbursement contract operated by a ZondaCrypto / BitBay-attributed wallet. It does not document:

- The natural-person or corporate-entity identities behind the 594 internal-tx recipient addresses — that is investigator-handoff territory beyond the public primary-citation gate.
- A USD-denominated flow profile — the contract is native-ETH-only and this page does not assert an ETH→USD conversion; price-time series can be applied externally against the per-tx blockheights in the receipt.
- A second independent attribution of the contract or its deployer — the deployer rests on a single primary source (Bubblemaps `entity_id = "zonda"`), and resolving this contract's tier to CONFIRMED requires that second source to land on either side of the deployment relation.
- Whether the contract is upgradeable / proxy-controlled — the bytecode is unverified on Etherscan; the inferred behaviour rests on the observed method selector `0xab883d28` and the absence of any other selector across 805 calls.

## Block-explorer link

https://etherscan.io/address/0xb6be26445f21e41bc69197fe68f697fc1a862f19

## Citations

[^1]: Etherscan address page for `0xb6be26445f21e41bc69197fe68f697fc1a862f19`, fetched 2026-05-21. Records the address as a smart contract created by `0x56d943aea92b099228b31f01cd12bd4aa39b4778` at deployment transaction `0xb3ccd233d44ddd880a3362af2da630c98c56d5d2600cd145391ec461224374fc` in block 23066530. Receipt at [`../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json`](../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json) (`deployment_tx`). https://etherscan.io/address/0xb6be26445f21e41bc69197fe68f697fc1a862f19

[^2]: Etherscan v2 `account.txlist` + `account.txlistinternal` + `account.tokentx` + `account.tokennfttx` + `contract.getsourcecode` + `account.balance` against chainid=1, probed 2026-05-21T14:16:59Z. Totals: 806 normal txs, 1,701 internal txs, 0 ERC-20, 0 ERC-721; deployer-only normal-tx caller (805/805); only observed function selector `0xab883d28` = `multisendEther(address[] _contributors, uint256[] _balances)`; balance 0 wei. Receipt at [`../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json`](../../sources/eth-archive/0xb6be2644-profile-2026-05-21.json).
