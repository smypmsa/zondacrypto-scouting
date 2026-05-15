# BitBay.net cluster (WalletExplorer)

> **Plain-language summary.** A WalletExplorer-named cluster of 26,014 Bitcoin addresses attributed to the BitBay.net brand — the predecessor identity of ZondaCrypto. Active 2019-05-13 → 2025-08-24 across 321,245 cluster-level transactions. Recorded as a single inventory item for the cluster as a whole. Attribution is at PARTIAL tier because WalletExplorer is the only public label set naming this cluster.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

A clustered set of operational Bitcoin addresses that WalletExplorer attributes — under a single named cluster — to the BitBay.net brand. This entry is a single inventory item for the cluster as a whole. The cluster's canonical address list lives upstream; this file documents the cluster's identity, the basis for attribution, representative addresses, and what the cluster does *not* cover.

## Cluster identity

- Cluster name (verbatim): **`BitBay.net`**
- Source: [walletexplorer.com/wallet/BitBay.net](https://www.walletexplorer.com/wallet/BitBay.net)
- Size: **26,014** addresses
- Transactions: **321,245**
- Earliest observed transaction: **2019-05-13**
- Most recent observed transaction: **2025-08-24**
- Confidence tier: **PARTIAL** — single primary source (WalletExplorer's named clustering). No second public label set has been located that names the same address group. The cluster name itself is a public attribution by WalletExplorer to the BitBay.net domain, which is the predecessor branding of zondacrypto (formal rebrand 2021-11-08; the `BitBay.net` domain belongs to the same operator).

## Why a single cluster file rather than 26,014 wallet files

The cluster is internally coherent (WalletExplorer's co-spend / common-input heuristic), uniformly low-balance (the 20 largest addresses by current balance all hold sub-0.004 BTC), and operationally homogeneous (hot-wallet / per-user-deposit churn). The investigative value is in the cluster's *flow*, not in any individual address. Aggregating into one entry follows the same convention OSINT investigations (Bellingcat, OCCRP, Chainalysis published reports) use for exchange clusters: document the cluster as the inventory item, link to its canonical source, list a representative sample. The full 26,014-address list is enumerable via the WalletExplorer cluster page's pagination or its "CSV Export: all pages" affordance.

## Representative addresses

Top 20 by current balance, snapshot 2026-05-12 (source: `/wallet/BitBay.net/addresses` page 1, sorted balance descending):

| Address | Balance (BTC) | Txs | Inferred role |
|---|---|---|---|
| `1MSaQRPCQkXrUBKKQGssBrVmbfU8J8UUXa` | 0.00393560 | 25 | Hot wallet |
| `18jCVedwoMfofT7GAhdwLmw9phfmmqnn1v` | 0.00221857 | 145 | Hot wallet, high reuse |
| `1GfeHpKDWEKJBZC9XeRpssT7yupqYSg7o2` | 0.00200131 | 26 | Hot wallet |
| `145n9frEnr297eL3EFcf1Ha9K1bkQXVRXk` | 0.00200080 | 14 | Hot wallet |
| `1Gh2L9sRcLpvaa94Mxsp3gsYTtJj4DhNEW` | 0.00198224 | 11 | Hot wallet |
| `19zhuuxTS8phiqdtRGss5qHYJe5Em18aML` | 0.00177806 | 11 | Hot wallet |
| `1JWF2VKnHZiynREXi1RmXa4VT8i4g6VRBX` | 0.00174644 | 2 | Likely deposit address |
| `1J1EzH4LEfrxAaNwqhdkmkfixZq7tWZEjG` | 0.00161000 | 20 | Hot wallet |
| `1PzCYzPkBhXUwcnqQf9vqgbJjzc1DghBe7` | 0.00130997 | 13 | Hot wallet |
| `1GAqEKYmR8XxE9bgcCeMwdFBm19TV57Pz3` | 0.00113700 | 8 | Hot wallet |
| `16vzY8McaCbLfyCTpK7GtUA4aZ5KEhi9cw` | 0.00113138 | 19 | Hot wallet |
| `19YF2rm3LnvM6HtyQvZWC5wwaT3HzJ9WzT` | 0.00105430 | 4 | Likely deposit address |
| `1G7eupKrc4wXZSY13iVY6PZv9qwnNFZfyu` | 0.00101245 | 4 | Likely deposit address |
| `1HHbci56DgHpWN9KZmiVmSw7zvBDC8cUt6` | 0.00098828 | 100 | Hot wallet, high reuse |
| `1GLyEWcHgJEMcnrNB19AmE7QsDgw719Xff` | 0.00098306 | 3 | Likely deposit address |
| `16BmxaxzMteokySxnWp9fcaakpWVxxzDRw` | 0.00098071 | 60 | Hot wallet, high reuse |
| `18TmkHYdpAvzt2UiQYncYtis84f2DdPYqB` | 0.00097954 | 6 | Hot wallet |
| `1LXHAzj9RjZuZeLHJwHp21ZFHAeJKG5ea`  | 0.00097935 | 12 | Hot wallet |
| `18NTq51gShpDRvnPx6DXE23qjnexrnZ5DW` | 0.00097801 | 3 | Likely deposit address |
| `1BK996rZ9oBBNEA71jKTAXeyD9cEMiPh98` | 0.00097201 | 15 | Hot wallet |

These addresses are the most useful entry points for flow analysis that lands on this cluster — checking whether a Bitcoin counterparty in some other investigation is BitBay-related is a question of whether the counterparty's address (or any co-spend partner) sits inside the WalletExplorer `BitBay.net` cluster, not whether it matches one of the 20 representatives above. The 20 are *examples*, not *the inventory*.

## Scope and negative space

- **2019+ operational addresses only.** The cluster begins on **2019-05-13**, three years after the cold reserve `16aEn4p6hK4FMpLtJGpoQZMZ946sDg1Z6n` (see `bitcoin/16aEn4p6-cold-reserve.md`) was funded in 2016-03. WalletExplorer's `BitBay.net` name therefore does *not* retroactively cover the 2016-era infrastructure.
- **The cold reserve is NOT in this cluster.** `16aEn4p6…` sits in WalletExplorer's unnamed cluster `[c66f0fa5dd193b1c]` (the cluster that contains the receiving cold-reserve address and its dust).
- **The 2016-era cold-reserve funders are NOT in this cluster.** They sit in unnamed WalletExplorer clusters `[033a676d6f50f05c]` (67 of 69 distinct 2016-03-06 inputs to the cold reserve, per byte-clean per-address WE probes archived on 2026-05-13) and `[89547e98ce46121f]` (2 of 69 inputs; the cluster's full transaction history touches BTC-e.com, Xapo.com, Huobi.com counterparties). These two unnamed clusters are *not* attributed publicly to BitBay and are not part of this inventory.

## Flow profile (cluster-level)

The cluster is too large to enumerate per-address as an inventory deliverable. **26,014 addresses** in the cluster (point-in-time snapshot 2026-05-12). **321,245 transactions** at the cluster level. Active period **2019-05-13 → 2025-08-24**. WalletExplorer reports these aggregates on the cluster page directly.

**Scope note — structural stats only.** Cluster-level BTC volume and per-counterparty named-cluster touches are deferred from this inventory entry. Reproducing them requires either WalletExplorer's CSV-export-all-pages affordance (which paginates over 26,014 addresses across many transaction-history pages) or a full local co-spend re-cluster against a Bitcoin full node. Both reproduction paths are documented in the [methodology](../../methodology.md#inventory-profile-csv) under "Bitcoin cluster scope". Readers needing aggregate cluster flow numbers should consult the WalletExplorer cluster page directly: [walletexplorer.com/wallet/BitBay.net](https://www.walletexplorer.com/wallet/BitBay.net).

Per-address enumeration of this cluster is out of scope for this inventory under the cluster-as-inventory-item convention documented in the "Why a single cluster file rather than 26,014 wallet files" section above.

## Verification

The cluster is verifiable at any time by visiting the cited WalletExplorer URL — it shows the cluster's size, transaction count, time bounds, and per-address breakdown. Replication: any reader can compare WalletExplorer's clustering against an independent run (e.g. via [Bitcoinwhoswho](https://www.bitcoinwhoswho.com/) or a fresh local co-spend-graph cluster) on a sample of the 20 addresses above. WalletExplorer is industry-standard but not infallible; this entry is recorded as PARTIAL until a second independent labelling source corroborates the same cluster identity.

## Footnotes

- Cluster fetched and snapshotted on 2026-05-12. Source HTML preserved in the local case at `../../sources/walletexplorer/bitbay-cluster-2026-05-12.html`.
- WalletExplorer applies clustering retroactively as new on-chain data accrues; the cluster size and address roster will grow with operational usage and may, on rare occasions, shrink if a clustering correction is applied. The figures above are point-in-time.
