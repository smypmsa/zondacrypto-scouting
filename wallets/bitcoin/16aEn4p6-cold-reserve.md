# Disclosed BTC cold reserve

**Address:** `16aEn4p6hK4FMpLtJGpoQZMZ946sDg1Z6n`

**Chain:** Bitcoin.

**Role:** Cold-storage bitcoin reserve, publicly disclosed by the ZondaCrypto CEO on 2026-04-16.

**Confidence:** PARTIAL.

## Attribution

A video posted on the X account of the ZondaCrypto CEO on 2026-04-16 displayed this Bitcoin address on screen and described it as the company's cold reserve.[^1] The CEO subsequently stated that the private key is held by the company's missing former CEO and that the address is not currently under company control.

This is the only Bitcoin address that ZondaCrypto has self-attested. No other primary source links this address to the company.

## Activity (Bitcoin, probed 2026-05-13)

- First on-chain tx: 2016-03-06 (block 401,390).
- Most recent on-chain tx: 2026-05-08 (block 948,382).
- Tx count: 39. Funded UTXOs: 40. Spent UTXOs: 0. Current balance: 4,503.26 BTC — every input ever received is still unspent.
- Source: mempool.space `/api/address/<addr>` + paginated `/api/address/<addr>/txs/chain`.

## WalletExplorer cluster context (probed 2026-05-13)

WalletExplorer's co-spend clustering assigns the 69 distinct foundational input addresses across this wallet's full transaction history to two unnamed clusters:

- **65 inputs → cluster `[033a676d6f50f05c]`** — a short-lived 2016-Q1 aggregator (129 transactions, 116 distinct counterparty wallets, lifespan 2016-01-15 → 2016-03-06 08:03:46, terminating at the second-precision timestamp of this address's first incoming transaction).
- **4 inputs → cluster `[89547e98ce46121f]`** — a separate unnamed cluster active 2015-09 → 2016-09. Its full transaction history (582 tx, 312 counterparty wallets) touches WalletExplorer-named clusters `BTC-e.com` (3), `Huobi.com-2` (2), `Xapo.com` (1), and `BitcoinWallet.com` (1).
- **0 inputs → WalletExplorer-named `BitBay.net` cluster** (the post-2019 operational hot-wallet cluster documented at `bitbay-net-cluster.md`).

Neither funding cluster's full transaction history contains any wallet that WalletExplorer attributes to a BitBay-named cluster. The 2016 funding sources visible in WalletExplorer point to the 2015–16 OTC ecosystem rather than to BitBay operational infrastructure. This is a behavioural-heuristic observation from a single tool (WalletExplorer's co-spend clustering) and does not by itself confirm or deny the wallet's role as a corporate cold reserve — the company's own public statement remains the only primary attribution.

Receipts: per-address WalletExplorer HTML probes archived under `case/sources/walletexplorer-2026-05-13/` (not in this public inventory).

## Flow profile (Bitcoin, mempool.space-aggregated 2026-05-13)

Full-history aggregation built from the mempool.space `address/<addr>` summary and the paginated `address/<addr>/txs/chain` endpoint. Dune Analytics has no Bitcoin coverage; the BTC flow profile is built directly from a self-hostable mempool.space-style indexer over the address's UTXO set. See [methodology](../methodology.md#flow-profile-bitcoin) for the data sources.

| Metric | Value |
|--|--|
| Gross IN (BTC) | 4,503.25949830 BTC |
| Gross OUT (BTC) | 0 BTC |
| Current balance | 4,503.25949830 BTC (every UTXO ever received is still unspent) |
| Total transactions | 39 |
| Funded UTXOs | 40 |
| Spent UTXOs | 0 |
| Distinct funding addresses (inputs to txs that funded this address) | 116 |
| Distinct spending destinations | 0 (no outgoing spends — all UTXOs unspent) |
| Active period | 2016-03-06 → 2026-05-08 |

**Confidence:** CONFIRMED on totals (balance, tx count, UTXO state, active period). The "no outgoing spends" claim is reproducible from `mempool.space/api/address/<addr>` returning `spent_txo_count: 0` and `spent_txo_sum: 0` simultaneously, both today and historically. PARTIAL on per-funding-address classification — none of the 116 funding addresses has a Bitcoin-side public name tag on a major block explorer, and the WalletExplorer cluster-context observation in the section above is heuristic.

### Counterparties — inflow side

The 116 distinct funding addresses lie in two unnamed WalletExplorer co-spend clusters as documented in the section above. **No funding address carries a public name tag on mempool.space or a comparable Bitcoin block explorer as of 2026-05-13.** All 116 are classified Unidentified under the inventory's primary-citation standard.

### Counterparties — outflow side

None. Zero on-chain spends since the wallet's first deposit in 2016-03. Every UTXO ever received to this address is still UTXO-unspent as of 2026-05-08.

### Unidentified counterparties

**This section is a known incomplete part of the analysis.** All 116 of 116 funding addresses are unattributed under the inventory's primary-citation standard. The WalletExplorer cluster context above is a heuristic observation from a single tool and does not establish primary attribution on any individual funding address. Entity-attribution work on these counterparties is ongoing in the case's internal working notes.

**Receipts (for reproduction)**:
- mempool.space summary + paginated tx history: `case/sources/btc-16aEn4-2026-05-13/summary.json` + `txs-page-*.json` + combined `all-txs.json`.
- Reproduce: `curl -s "https://mempool.space/api/address/16aEn4p6hK4FMpLtJGpoQZMZ946sDg1Z6n"` for the summary, then iterate `…/txs/chain[/<last_txid>]` for full tx history.

## Block-explorer link

https://mempool.space/address/16aEn4p6hK4FMpLtJGpoQZMZ946sDg1Z6n

[^1]: Video by the ZondaCrypto CEO on X, 2026-04-16. https://x.com/przemyslaw_kral/status/2044763900541854094
