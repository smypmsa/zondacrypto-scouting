# Methodology

How attributions in this repository are established and what each confidence tier means.

## Confidence tiers

**CONFIRMED.** Two or more independent primary sources point to the attribution. Examples: a public name tag on a major block explorer plus a deterministic on-chain link to another already-confirmed address; a self-attestation plus an auditor reference; two public-label sets that do not derive from each other.

**PARTIAL.** A single primary source. Recorded but should not be cited without that caveat.

**HEURISTIC.** No primary source. Derived from on-chain pattern, clustering, or behavioural fingerprint. Useful as a working hypothesis only.

## Evidence types

**Self-attestation.** The entity itself pointed at the address — a tweet, video, signed message, or page on its own domain.

**Public name tag.** A label maintained by a major block explorer (Etherscan, PolygonScan, OP Etherscan, BscScan, BaseScan, Solscan, Tronscan), or an aggregated label set such as the hildobby Dune query.

**Smart-contract relation.** The address is the deployer of, deployed by, or owner of an already-attributed contract.

**Transaction relation.** The address received from or sent to an already-attributed address in a specific transaction whose hash is quoted.

**Cluster heuristic.** Bitcoin co-spend or change-output adjacency, or EVM common-deployer-EOA clustering. By itself, HEURISTIC; combined with another evidence type, can support CONFIRMED.

**Behavioural fingerprint.** Holdings shape, transaction-volume pattern, or other indirect evidence. Weakest tier.

## Verification

Every factual claim in this repository carries a citation. Block-explorer URLs are considered durable; for other external sources we prefer mirroring to an `archive.today` or `web.archive.org` snapshot so the citation keeps resolving after the live URL dies.

## Natural persons

Natural persons are referenced by role where possible. Where naming is unavoidable because the person's name is part of the primary record itself (for example a tweet posted from their own handle), the URL is given as-is and no further commentary is added.
