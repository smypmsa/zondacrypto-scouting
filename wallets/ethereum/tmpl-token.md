# TMPL token (TeamPL Token)

**Address:** `0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07`

**Chain:** Ethereum.

**Role:** ERC-20 token used by ZondaCrypto to pay the Polish Olympic Committee (PKOl) and Polish Olympic Team sponsorship in 50/50 split with Polish złoty.

**Confidence:** CONFIRMED.

## Attribution

The contract is an OpenZeppelin-based ERC-20 with permit (Solidity 0.8.28), source-verified on Etherscan with `name() = "TeamPL Token"` and `symbol() = "TMPL"`.[^1] ZondaCrypto's official news post announcing the PKOl sponsorship names TMPL as the payment token alongside PLN cash.[^2] CoinGecko's listing identifies the same contract as the TeamPL Token issued for the ZondaCrypto–PKOl partnership.[^3] The whitepaper is hosted at `assets.znd.co/tmpl-token/en/whitepaper.pdf`, the same `znd.co` domain that hosts the ZND token whitepaper.

The Zonda link is also visible on-chain: the second-largest holder of TMPL is the Etherscan-tagged Zonda 5 exchange wallet ([`zonda-5.md`](zonda-5.md)), which holds 139,637,857 TMPL — 13.96% of the total supply. The largest holder is the contract that deployed TMPL, a vesting factory at `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4`, which holds 860,325,400 TMPL (86.03%).

## On-chain facts

- Deployment transaction: `0x29e73bb21485bd659ad9bf3c8bfdcefbec8b84d5fb6a4f272ee37d249fe0157f`
- Deployment block: 24,326,010
- Deployment timestamp: 2026-01-27 11:56:11 UTC
- Constructor mint: 1,000,000,000 TMPL (one billion, 18 decimals)
- Current supply: 999,972,733 TMPL (≈27,267 TMPL burned since launch)
- Holder count (Ethplorer): 12
- The vesting factory `0x80140b93f81d9e4e519b8168a15289bcfc0f3bf4` deployed TMPL inside its constructor; its source is verified on Etherscan
- TMPL is not listed on any visible DEX pool; the token trades on the ZondaCrypto centralised exchange (TMPL/PLN pair) per the sponsorship announcement

## Block-explorer link

https://etherscan.io/token/0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07

## Disambiguation

At least four unrelated tokens share the TMPL ticker (an unverified TeamPL duplicate at `0x499Fe986…a8b5D9AD7`, a presale at `0xB4C8d29E…F967ADBA7`, the ampleforth fork TruAmpl at `0xFCB755B046ea9B9bC4586db4018b49c5A02e3d1c`, and a separate TMPL contract at `0x52132a43d7cae69b23abe77b226fa1a5bc66b839`). Only the contract documented on this page is held in volume by a Zonda-tagged wallet and referenced by ZondaCrypto's own announcement.

[^1]: Etherscan, verified source and token tag "TeamPL Token (TMPL)". https://etherscan.io/token/0xc2FdA18D62C8688902741Da1e3c5BE65C86BAB07
[^2]: ZondaCrypto news, "zondacrypto General Sponsor of PKOl and the Polish Olympic Team". https://zondacrypto.com/en/news/zondacrypto-general-sponsor-of-pkol-and-polish-olympic-team
[^3]: CoinGecko, "TeamPL Token (TMPL)" coin page. https://www.coingecko.com/en/coins/teampl-token
