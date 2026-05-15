# TMPL token (TeamPL Token)

> **Plain-language summary.** An ERC-20 token (`TeamPL Token`, symbol `TMPL`) that ZondaCrypto uses to pay the Polish Olympic Committee and Polish Olympic Team sponsorship in a 50/50 split with Polish złoty. Attributed by Etherscan source verification, ZondaCrypto's own announcement, and the CoinGecko listing for the same contract. The second-largest TMPL holder (13.96% of supply) is Zonda 5.

**Address:** `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07`

**Chain:** Ethereum.

**Role:** ERC-20 token used by ZondaCrypto to pay the Polish Olympic Committee (PKOl) and Polish Olympic Team sponsorship in 50/50 split with Polish złoty.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

The contract is an OpenZeppelin-based ERC-20 with permit (Solidity 0.8.28), source-verified on Etherscan with `name() = "TeamPL Token"` and `symbol() = "TMPL"`.[^1] ZondaCrypto's official news post announcing the PKOl sponsorship names TMPL as the payment token alongside PLN cash.[^2] CoinGecko's listing identifies the same contract as the TeamPL Token issued for the ZondaCrypto–PKOl partnership.[^3] The whitepaper is hosted at `assets.znd.co/tmpl-token/en/whitepaper.pdf`, the same `znd.co` domain that hosts the ZND token whitepaper.

The Zonda link is also visible on-chain: the second-largest holder of TMPL is the Etherscan-tagged Zonda 5 exchange wallet ([`zonda-5.md`](zonda-5.md)), which holds 139,637,857 TMPL — 13.96% of the total supply. The largest holder is the contract that deployed TMPL — the `TMPLPools` vesting contract at `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4` ([`tmpl-pools.md`](tmpl-pools.md)) — which holds 860,325,400 TMPL (86.03%).

## On-chain facts

- Deployment transaction: `0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f`
- Deployment block: 24,326,010
- Deployment timestamp: 2026-01-27 11:56:11 UTC
- Constructor mint: 1,000,000,000 TMPL (one billion, 18 decimals)
- Current supply: 999,972,733 TMPL (≈27,267 TMPL burned since launch)
- Holder count (Ethplorer): 12
- The vesting factory `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4` deployed TMPL inside its constructor; its source is verified on Etherscan
- TMPL is not listed on any visible DEX pool; the token trades on the ZondaCrypto centralised exchange (TMPL/PLN pair) per the sponsorship announcement

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2026-01-29 (block 24340677); most recent 2026-05-10 (block 25063625); 126 events.
- ERC-20 events: first 2026-04-05 (block 24813609); most recent 2026-04-05 (block 24813609); 1 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)

This wallet moves ZND / TMPL tokens for which Dune `tokens_ethereum.transfers` has no liquid USD-equivalent price. The full counterparty enumeration is therefore native-denominated: USD columns in the CSV are 0/blank by design (no price oracle), and the inventory information lies in the `native_amounts` column (`SYMBOL:amount;...`) and the `n_events_in` / `n_events_out` counts.

| Metric | Value |
|---|---|
| Total distinct counterparties (no threshold) | 1 |
| Total events (IN / OUT) | 1 / 0 |
| Active period | 2026-04-05 → 2026-04-05 |

Counterparty classification follows the same `internal` / `hildobby` / `etherscan` / `below-cutoff` / `deferred-above-cutoff` precedence as the USD-denominated profiles. The full CSV lives at [`tmpl-token-counterparties.csv`](tmpl-token-counterparties.csv).

**Confidence:** CONFIRMED on the row-level event counts and native-token sums (direct on-chain reads via Dune). PARTIAL on per-counterparty entity attribution — the same fetch / label-source precedence is applied as elsewhere in the inventory.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x6357d3843d715496257e338a878ab0b72040a918` | $0 | $0 | 1 / 0 | 2026-04-05 → 2026-04-05 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`tmpl-token-counterparties.csv`](tmpl-token-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/token/0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07

## Disambiguation

At least four unrelated tokens share the TMPL ticker (an unverified TeamPL duplicate at `0x499Fe986…a8b5D9AD7`, a presale at `0xB4C8d29E…F967ADBA7`, the ampleforth fork TruAmpl at `0xFCB755B046ea9B9bC4586db4018b49c5A02e3d1c`, and a separate TMPL contract at `0x52132a43d7cae69b23abe77b226fa1a5bc66b839`). Only the contract documented on this page is held in volume by a Zonda-tagged wallet and referenced by ZondaCrypto's own announcement.

[^1]: Etherscan, verified source and token tag "TeamPL Token (TMPL)". https://etherscan.io/token/0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07
[^2]: ZondaCrypto news, "zondacrypto General Sponsor of PKOl and the Polish Olympic Team". https://zondacrypto.com/en/news/zondacrypto-general-sponsor-of-pkol-and-polish-olympic-team
[^3]: CoinGecko, "TeamPL Token (TMPL)" coin page. https://www.coingecko.com/en/coins/teampl-token
