# Zonda Deposit Wallet (0x82c829…900c)

> **Plain-language summary.** A deposit-side ZondaCrypto wallet on Ethereum, attributed by two independent primary label sources (Bubblemaps' `entity_id = "zonda"` plus BlockSec MetaSleuth `main_entity = "Zonda (BitBay)"`). Also transacts directly with Zonda Deposit Funder 1, consistent with the deposit-wallet role. Active since November 2022; current top-100 ZND holder.

**Address:** `0x82c829237159287dac6fc62eb139e6a89195900c`

**Chain:** Ethereum.

**Role:** Deposit-side ZondaCrypto wallet.

**Confidence:** CONFIRMED.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

Two independent primary label sources point to this address as a ZondaCrypto wallet:

1. **Bubblemaps** — the `addresses/token-top-holders` API for the ZND token returns this address with `address_details.label = "Zonda Deposit Wallet"` and `entity_id = "zonda"`.[^1]
2. **BlockSec MetaSleuth** — the `address-label/api/v3/labels` endpoint returns `main_entity = "Zonda (BitBay)"` under the `EXCHANGE` category.[^2] The receipt of the BlockSec response is preserved at [`sources/blocksec/labels-zonda-2026-05-12.json`](../../sources/blocksec/labels-zonda-2026-05-12.json).

In addition, Etherscan's address page shows this wallet transacts directly with `Zonda: Deposit Funder 1` (see [`zonda-deposit-funder-1.md`](zonda-deposit-funder-1.md)), consistent with the deposit-wallet role.

The address is currently a top-100 ZND holder (≈0.046% of supply).

## Activity (Ethereum, probed 2026-05-13)

- Native txs: first 2022-11-28 (block 16068080); most recent 2026-04-03 (block 24796973); 262 events.
- ERC-20 events: first 2022-12-02 (block 16100080); most recent 2026-04-03 (block 24796973); 351 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-13)
Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan carries a Public Name Tag verified by fresh HTML fetch on 2026-05-13, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.
| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $460,941 |
| Gross OUT (USD-equivalent at tx time) | $467,870 |
| Total throughput (gross in + out) | $928,811 |
| Net direction | −$6,928 |
| Total events ≥$1k | 228 |
| Distinct external counterparties (≥$1k cumulative) | 18 |
| Identified counterparties in this section | 1 internal + 17 external (Etherscan-tagged) |
| Counterparties without a public name tag | **1, aggregating ~$0 outbound and ~$5,004 inbound across the top-500 captured here** |
| Active period (≥$1k events) | 2022-12-02 → 2026-01-21 |

**Confidence:** CONFIRMED on totals (Gross IN, Gross OUT, throughput, active period, distinct-counterparty count). CONFIRMED on per-counterparty classification for the Internal and External-tagged rows below (each Etherscan tag was verified by a fresh HTML fetch on 2026-05-13; the HTML is retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility)). PARTIAL on the Unattributed counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory
| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $467,870 | 111 |

### External sources — confirmed via Etherscan public name tags
| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0d070796…92fe` | Gate Deposit: 0x0d0707963952f2fba59dd06f2b425ace40b492fe | $158,566 | 34 |
| `0xdfd5293d…963d` | Binance 16 | $67,228 | 11 |
| `0x21a31ee1…5549` | Binance 15 | $42,526 | 9 |
| `0x28c6c062…1d60` | Binance 14 | $33,758 | 6 |
| `0xf89d7b9c…aa40` | Bybit: Hot Wallet | $25,347 | 5 |
| `0x9642b23e…5d4e` | MEXC 16 | $19,095 | 3 |
| `0x260b364f…4cea` | Bybit: Opensea User | $17,055 | 2 |
| `0x77134cbc…35ec` | Bitfinex: Hot Wallet | $15,696 | 11 |
| `0x48ec5560…6b0c` | Bitstamp: Wallet | $13,674 | 6 |
| `0xae2d4617…673f` | Kraken 10 | $12,585 | 5 |

<details><summary>Show 7 more rows</summary>

| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x05ff6964…f381` | Kraken: Hot Wallet 4 | $12,169 | 5 |
| `0xa03400e0…7687` | HTX 48 | $10,932 | 7 |
| `0xe7178ad7…d5c6` | Kraken 47 | $10,115 | 5 |
| `0x7f604d59…b752` | Bitstamp 61 | $6,960 | 4 |
| `0xee7ae85f…4055` | Binance: Hot Wallet 34 | $6,772 | 1 |
| `0xd91efec7…0747` | KuCoin: ERC-20 Batch Transfer | $1,742 | 1 |
| `0x56eddb7a…b17f` | Binance 17 | $1,716 | 1 |

</details>

### Unattributed counterparties
**This section is a known incomplete part of the analysis.** 1 of the 19 counterparties with ≥$1k cumulative flow carry no public name tag on Etherscan as of 2026-05-13 and do not appear in this inventory's roster. Within the top-500-by-USD slice captured here, the unidentified rows aggregate **$0 outbound** and **$5,004 inbound**. These addresses remain unattributed in this public inventory until each clears the same primary-citation standard used for the inventory itself (Etherscan/PolygonScan name tag, BlockSec MetaSleuth label, hildobby CEX-address Dune compilation, or an equivalent independent primary source). Entity-attribution work on these counterparties is ongoing in the case's internal working notes and will be added back to this section as individual addresses clear the primary-citation gate.

### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x6de037ef9ad2725eb40118bb1702ebb27e4aeb24` | $0 | $0 | 1 / 0 | 2024-01-25 → 2024-01-25 |
| 2 | `0xe065ecde5341eed30741d97a02e4377c7f6d9e8b` | $0 | $0 | 1 / 0 | 2024-07-06 → 2024-07-06 |
| 3 | `0x6ed0746b0d206ab919374ee51c59da5878bc5048` | $0 | $0 | 0 / 2 | 2022-12-20 → 2022-12-20 |
| 4 | `0x6ed24f302e7d20174fab25020b1d4fd4ed2c5048` | $0 | $0 | 0 / 1 | 2022-12-21 → 2022-12-21 |
| 5 | `0xe1bfb3d11890f9b11c046cdec9f7e7cd7d472238` | $0 | $0 | 3 / 0 | 2024-08-30 → 2024-11-02 |
| 6 | `0x39c0e0c8b0ea7b92b926b5f2057e46ec4bb0e130` | $0 | $0 | 1 / 0 | 2024-09-07 → 2024-09-07 |
| 7 | `0xf70fdf0b14d8d9b4bac7ff549f0cabc987c1e01c` | $0 | $0 | 1 / 0 | 2025-03-12 → 2025-03-12 |
| 8 | `0x6ee9951bf99f25540caef3e2bc0c3f9ebe1c5048` | $0 | $0 | 2 / 0 | 2022-12-03 → 2022-12-03 |
| 9 | `0xabc029ff1649b5e764dd28a9e48b1cf716ef225f` | $0 | $0 | 1 / 0 | 2024-06-29 → 2024-06-29 |
| 10 | `0x6eb9ee74064f8e7b36f6f941c0b57a74a36c5048` | $0 | $0 | 0 / 2 | 2022-12-03 → 2022-12-03 |

<details><summary>Show 1 more rows</summary>

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 11 | `0xb7e27d218b687e5d9234d6e31fe1ac8d0cf329f6` | $0 | $0 | 1 / 0 | 2024-07-06 → 2024-07-06 |

</details>
## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-deposit-wallet-82c829-counterparties.csv`](zonda-deposit-wallet-82c829-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Ethereum; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../../methodology.md#inventory-profile-csv).

## Block-explorer link

https://etherscan.io/address/0x82c829237159287dac6fc62eb139e6a89195900c

[^1]: Bubblemaps token-holders API for ZND. Captured 2026-05-11. https://v2.bubblemaps.io/map?address=0x2d8eA194902Bc55431420BD26Be92b0782dCe91D&chain=eth
[^2]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-12 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`. Endpoint: https://aml.blocksec.com/address-label/api/v3/labels

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0x0d0707963952f2fba59dd06f2b425ace40b492fe` | Gate.io 1 | $164,316 | $0 | 51 / 0 |
| `0xdfd5293d8e347dfe59e90efd55b2956a1343963d` | Binance 16 | $67,306 | $0 | 14 / 0 |
| `0x21a31ee1afc51d94c2efccaa2092ad1028285549` | Binance 15 | $43,041 | $0 | 13 / 0 |
| `0x28c6c06298d514db089934071355e5743bf21d60` | Binance 14 | $34,295 | $0 | 10 / 0 |
| `0xf89d7b9c864f589bbf53a82105107622b35eaa40` | Bybit 5 | $25,347 | $0 | 5 / 0 |
| `0x9642b23ed1e01df1092b92641051881a322f5d4e` | MEXC 21 | $20,023 | $0 | 9 / 0 |
| `0x77134cbc06cb00b66f4c7e623d5fdbf6777635ec` | Bitfinex Hot Wallet | $17,964 | $0 | 15 / 0 |
| `0x260b364fe0d3d37e6fd3cda0fa50926a06c54cea` | Bybit 40 | $17,055 | $0 | 2 / 0 |
| `0xa03400e098f4421b34a3a44a1b4e571419517687` | HTX 52 | $15,905 | $0 | 15 / 0 |
| `0x48ec5560bfd59b95859965cce48cc244cfdf6b0c` | Bitstamp 8 | $15,612 | $0 | 9 / 0 |

<details><summary>Show 8 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xae2d4617c862309a3d75a0ffb358c7a5009c673f` | Kraken 10 | $12,585 | $0 | 5 / 0 |
| `0xe7178ad747f2c12ab1f8332e61cf6e756815d5c6` | Kraken 28 | $10,423 | $0 | 7 / 0 |
| `0x7f604d597c15b2e2f60dc645844f68b1d781b752` | Bitstamp 60 | $9,837 | $0 | 8 / 0 |
| `0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43` | Coinbase 10 | $5,004 | $0 | 1 / 0 |
| `0x56eddb7aa87536c09ccc2793473599fd21a8b17f` | Binance 17 | $2,477 | $0 | 2 / 0 |
| `0xd91efec7e42f80156d1d9f660a69847188950747` | KuCoin 26 | $1,742 | $0 | 1 / 0 |
| `0xccfa6f3b01c7bf07b033a9d496fdf22f0cdf5293` | CoinDCX 16 | $0 | $0 | 1 / 0 |
| `0x58edf78281334335effa23101bbe3371b6a36a51` | KuCoin 32 | $0 | $0 | 8 / 0 |

</details>

