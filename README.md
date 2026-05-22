# Zondacrypto scouting

[Zondacrypto](https://zondacrypto.com), formerly BitBay, is a Polish cryptocurrency exchange. In April 2026, after [months of withdrawal failures](https://x.com/przemyslaw_kral/status/2041229323382804500), [its CEO publicly acknowledged](https://x.com/przemyslaw_kral/status/2044763900541854094) that the company's largest claimed bitcoin reserve was not under company control. [Polish prosecutors opened a criminal case](https://www.coindesk.com/business/2026/04/18/zondacrypto-under-fire-as-poland-s-prime-minister-links-exchange-to-legislative-interference) with damages estimated at no less than 350 million złoty. This repository collects publicly verifiable facts about the case and follows the money on-chain.

## What this repository contains and does not contain

It contains an **inventory** of on-chain addresses attributable to ZondaCrypto / BitBay by a primary public source, the **on-chain math** derived directly from those addresses (balances, transfers, counterparties, totals), and the **citations and receipts** that back each row. Every claim is reproducible from the wallet address alone against the named data source.

It does not contain interpretations, accusations, named-person commentary beyond what a primary record itself states, or attribution that exceeds what the cited source says.

## Headline figures

A small set of inventory-wide numbers a journalist or auditor can quote. Each is reproducible from the linked artefact alone.

- **34 inventoried wallets and clusters** across Bitcoin, Ethereum, and Polygon. See [`wallets/README.md`](wallets/README.md) for the per-row index.
- **4,503.26 BTC** standing balance on the address ZondaCrypto's CEO disclosed as the company's largest claimed Bitcoin reserve, in its lifetime never spent. First funded 2016-03-06, last received deposit 2026-05-08. See [`wallets/bitcoin/16aEn4p6-cold-reserve.md`](wallets/bitcoin/16aEn4p6-cold-reserve.md).
- **26,014 addresses, 321,245 transactions** in the WalletExplorer-named `BitBay.net` cluster, the post-2019 operational hot-wallet cluster. Active 2019-05-13 → 2025-08-24. See [`wallets/bitcoin/bitbay-net-cluster.md`](wallets/bitcoin/bitbay-net-cluster.md).
- **$211.5 million** in cumulative outbound flow from ZondaCrypto-inventoried Ethereum wallets to Etherscan-tagged centralised-exchange deposit addresses (Binance $203.1M, Gate $8.4M, Bybit $3k), plus an additional **~$61.1 million** resolved by BlockSec MetaSleuth on 2026-05-21 and 2026-05-22 (Z4 sub-network C → `WhiteBIT: Hot Wallet` $10.4M; Z5 → three Binance customer-aggregator deposit addresses $34.7M; Z5 → two Kraken customer-aggregator deposit addresses $16.0M) — combined CEX-attributable outbound **~$272.5 million**. See [`observations/cex-off-ramp-summary.md`](observations/cex-off-ramp-summary.md) for the per-CEX × per-source-wallet breakdown and the inbound side.
- **≈98% decline** in Ethereum inventory outbound USD-equivalent volume from $19.86M (January 2026) to $0.31M (May 2026, partial through May 21), monotone across five consecutive months with no recovery month. See [`observations/inventory-outbound-volume-collapse.md`](observations/inventory-outbound-volume-collapse.md) for the per-month table and historical context.

## Repository layout

A reading order, not an alphabetical map. Start at the top and descend as needed.

1. **[`wallets/README.md`](wallets/README.md)** — the inventory index, one row per address or cluster, grouped by chain and role.
2. **[`wallets/<chain>/<slug>.md`](wallets/)** — the per-wallet page: a plain-language summary, attribution with citations, activity, full-history flow profile, counterparty tables, and a "Scope and negative space" section declaring what the page does not cover. Each page links a companion CSV with the un-truncated, no-threshold view of the same on-chain data.
3. **[`observations/`](observations/)** — cross-wallet math summaries: the [CEX off-ramp summary](observations/cex-off-ramp-summary.md) and the [inventory outbound-volume collapse](observations/inventory-outbound-volume-collapse.md).
4. **[`methodology.md`](methodology.md)** — confidence tiers, evidence types, the exact SQL behind every flow profile, the counterparty-CSV schema, and the receipts-mirroring policy.
5. **[`glossary.md`](glossary.md)** — plain-language definitions of every term used across the repository.

Two supporting files for contributors and reviewers, not part of the reading order:

- **[`templates.md`](templates.md)** — canonical structure for wallet, cluster, and observation files (heading vocabulary is frozen here).
- **[`sources/`](sources/)** — mirrored primary receipts cited by wallet pages (BlockSec label JSONs, Dune execution JSONs, WalletExplorer cluster HTML). Bulk HTML name-tag receipts are held in the working archive instead of the repo; see [methodology § Receipts](methodology.md#receipts-and-reproducibility).

## Contributions

Contributions are welcome from anyone who can supply data verifiable against primary records or against public blockchain state. Submit pull requests with the source link, the retrieval date, and the exact query or document that backs the claim. News commentary and paraphrase are not used as evidence.

## Disclaimer

Nothing here is legal advice and nothing here is an accusation against any named individual or entity. The repository describes addresses, balances, transfers, and the public documents that link them, and leaves interpretation to the reader.
