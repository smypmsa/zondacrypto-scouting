# Glossary

Plain-language definitions for terms used across this repository. Linked from `README.md` and from the legend block in every wallet file.

## Confidence tiers

- **CONFIRMED** — Two or more independent primary sources point to the same attribution. The strongest tier used in this repository.
- **PARTIAL** — A single primary source supports the attribution. Recorded, but not cited without that caveat.
- **HEURISTIC** — No primary source. Derived from on-chain pattern, clustering, or behavioural fingerprint. A working hypothesis only.

A wallet's confidence tier is for the **attribution** of the wallet to ZondaCrypto / BitBay. The flow-profile numbers themselves are always direct on-chain reads.

## Source / receipt terms

- **Primary source** — A document or dataset published by, or directly bearing the mark of, the entity the claim is about: a self-attestation on the entity's own domain or social account; a public name tag maintained by a major block explorer; a label set published by an established attribution provider.
- **Public name tag** — A label maintained by a major block-explorer page for an address (Etherscan, PolygonScan, BscScan, OP Etherscan, BaseScan, Solscan, Tronscan). Visible to anyone who loads the address's page.
- **Receipt** — The saved response from a primary source at the moment it was queried: an API JSON response, the HTML rendered at a given block-explorer URL, a snapshot of a dataset row. Lets a reader re-check a claim even if the live source later changes. See [methodology § Receipts](methodology.md#receipts-and-reproducibility).
- **Working archive** — Bulk receipts (e.g. tens of thousands of HTML name-tag fetches per closure pass) retained outside this public repository because of size. The corresponding upstream URL + retrieval date is the canonical public-verifiable artefact.

## Attribution sources

- **hildobby** — A public Dune Analytics query (`query_3237025`, "All Known EVM CEX Addresses") maintained by the `hildobby` Dune user. Compiles centralised-exchange addresses across EVM chains from multiple sources. Treated as primary alongside Etherscan public name tags.
- **BlockSec MetaSleuth** — A commercial address-label database. Its v3 address-label API returns `main_entity`, category, and `name_tag` strings for a queried address. Used as a primary source where it carries a label.

## On-chain clustering terms

- **Co-spend clustering** — Two Bitcoin addresses that appear as inputs to the same transaction are presumed to share a private-key holder (the input-cospend heuristic). Repeating the rule transitively builds a *cluster*. WalletExplorer applies this rule across the Bitcoin chain history.
- **Vanity-suffix cluster (EVM)** — A set of EVM addresses sharing a memorable suffix (e.g. all ending in `…8046`), normally produced by an address-mining tool with a shared seed. Implies a single deployer at the time of mining; does not by itself prove a shared current operator.
- **EOA / external owned account** — An Ethereum address controlled by a private key (as opposed to a smart-contract address controlled by code).

## Flow-analysis terms

- **Flow profile** — A per-wallet section reporting Gross IN, Gross OUT, throughput, net direction, distinct counterparties, and active period, computed directly from on-chain transfer events for a single address. Reproducible from the address alone.
- **Deposit-receipt hop** — An intermediate address that receives deposits from one or more centralised-exchange hot wallets and forwards them to a single onward destination. Operational signature: most or all of the outbound flow lands on one onward address, while inbound comes from many CEX-tagged sources.
- **MM / OTC wallet** — Market-maker or over-the-counter wallet. An address whose transaction pattern (high event count, large gross USD, counterparty mix dominated by trading-firm or large-block transfers) matches an institutional trading rather than a retail-deposit role.

## CSV label-source values

These appear in the `label_source` column of the counterparty enumeration CSVs.

- **`internal`** — The counterparty appears in this inventory's own roster of labelled wallets.
- **`hildobby`** — The counterparty is listed in hildobby's Dune query 3237025.
- **`etherscan`** — The counterparty's block-explorer page carries a Public Name Tag, verified by a fresh HTML fetch at the cited date.
- **`no-public-tag`** — A fresh HTML fetch was completed; the saved HTML contains no `Public Name Tag` string. Different from `below-cutoff` (intentionally not fetched) and `deferred-above-cutoff` (fetch outstanding).
- **`below-cutoff`** — Cumulative gross USD flow across the inventory is below the $10,000 cutoff for fetching name tags; no fetch is attempted.
- **`deferred-above-cutoff`** — Cumulative gross USD flow is at or above the $10,000 cutoff but no name-tag fetch has been completed in the most recent pass. A known, machine-discoverable gap.
