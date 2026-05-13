# Zonda Deposit Funder 1

**Address:** `0x5bff49eec8f76c066f979a818187b9732ac69503`

**Chain:** Ethereum.

**Role:** ZondaCrypto deposit-funder / gas-supplier wallet. Exchanges typically maintain a small set of EOAs that pre-fund user-deposit addresses with the ETH needed to pay forwarding gas. This is one of them.

**Confidence:** CONFIRMED.

## Attribution

Etherscan carries the public name tag "Zonda: Deposit Funder 1" on this address.[^1] The label is sourced from the hildobby compilation of known EVM centralised-exchange addresses on Dune Analytics (entry added 2024-10-06 as "Zonda Gas Supplier 1").[^2] The receipt of the Dune query result is preserved at [`sources/dune/hildobby-3237025-zonda-rows.json`](../../sources/dune/hildobby-3237025-zonda-rows.json).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2023-10-31 (block 18468877); most recent 2026-04-27 (block 24972323); ≥ 10,000 events.
- ERC-20 events: first 2023-10-31 (block 18469076); most recent 2026-04-26 (block 24964245); 1,255 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Block-explorer link

https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503

[^1]: Etherscan, public name tag "Zonda: Deposit Funder 1". https://etherscan.io/address/0x5bff49eec8f76c066f979a818187b9732ac69503
[^2]: hildobby, "All Known EVM CEX Addresses", Dune query 3237025. Row: `cex_name="Zonda"`, `distinct_name="Zonda Gas Supplier 1"`, `added_date="2024-10-06"`. https://dune.com/queries/3237025
