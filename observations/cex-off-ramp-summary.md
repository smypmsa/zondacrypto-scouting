# Cross-wallet CEX off-ramp summary (Ethereum, Dune-aggregated 2026-05-13; BlockSec extension 2026-05-21)

Sum of outbound USD-equivalent value (at transaction time) from each ZondaCrypto inventory wallet to centralised-exchange addresses carrying a primary public attribution. Two attribution sources are used in this summary: (1) Etherscan Public Name Tags verified by fresh HTML fetch on 2026-05-13 for every row in the Etherscan-tagged tables below; and (2) BlockSec MetaSleuth address-label API v3 responses captured 2026-05-21 for one further address that carries no Etherscan public name tag (`0xde7adbb3…0add` = `WhiteBIT: Hot Wallet`). Each row remains directly re-checkable: the Etherscan-tagged rows against the live block-explorer page, the BlockSec-resolved row against the mirrored JSON receipt.

Across the union of both attribution sources, **$211,477,461 in Etherscan-tagged outbound** plus **$10,400,000 in additional BlockSec-resolved outbound** (WhiteBIT only) is now CEX-attributable from the inventoried Ethereum wallets — a combined **~$221,877,461** of outbound flow lands on addresses with a primary CEX attribution.

**Scope.** Outbound from ZondaCrypto-inventoried Ethereum wallets to addresses with one of the two primary CEX attributions named above. Operator-network counterparties, OTC desks, or aggregator addresses that carry neither an Etherscan public name tag nor a BlockSec entity label remain out of scope of this summary by design — they belong in each wallet's Unattributed-counterparty row and remain unattributed under the inventory's primary-citation standard until cleared individually.

**Confidence.** CONFIRMED on totals: every cell is a Dune-aggregation sum filtered to addresses with a primary CEX attribution (Etherscan public name tag verified by fresh HTML fetch 2026-05-13, or BlockSec MetaSleuth `main_entity` returned 2026-05-21). PARTIAL on rows where the source-wallet attribution itself is at PARTIAL tier (the BitBay-era wallets — flagged below).

## Per-CEX × per-source-wallet outbound (USD)

Rows tagged **(BlockSec 2026-05-21)** are attributed by BlockSec MetaSleuth API v3 against an address that carries no Etherscan public name tag; receipt mirrored at [`../sources/blocksec/labels-2026-05-21.json`](../sources/blocksec/labels-2026-05-21.json). All other rows are Etherscan-tagged (HTML fetch 2026-05-13).

| CEX brand | Attribution source | Source Zonda wallet | Counterparty address | Outbound USD | Events | Distinct addresses |
|--|--|--|--|--|--|--|
| Binance | Etherscan public name tag | Zonda 5 `0x6edf968d…5048` | (12 addresses) | $121,971,089 | 4,222 | 12 |
| Binance | Etherscan public name tag | Zonda 1 `0xf646cbe3…b95e` | (6 addresses) | $49,659,754 | 1,991 | 6 |
| Binance | Etherscan public name tag | Zonda 4 `0x2b645268…763a` | (4 addresses) | $31,433,084 | 697 | 4 |
| Binance | Etherscan public name tag | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source)** | (1 address) | $8,399 | 1 | 1 |
| Binance | Etherscan public name tag | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source)** | (1 address) | $1,099 | 1 | 1 |
| Bybit | Etherscan public name tag | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source)** | (1 address) | $3,096 | 3 | 1 |
| Gate | Etherscan public name tag | Zonda 5 `0x6edf968d…5048` | (1 address) | $8,049,973 | 85 | 1 |
| Gate | Etherscan public name tag | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source)** | (1 address) | $350,968 | 11 | 1 |
| **WhiteBIT** | **BlockSec MetaSleuth 2026-05-21** | **Zonda 4 `0x2b645268…763a`** (via sub-network C forwarder `0x29606f60…e0ab`) | **`0xde7adbb3…0add`** (`WhiteBIT: Hot Wallet`) | **$10,400,000** | **128** | **1** |

The WhiteBIT Z4 row aggregates 128 forwarding events that pass through the sub-network C connector `0x29606f60…e0ab` and sink at the WhiteBIT hot wallet; the connector itself remains unattributed under the primary-citation standard and is recorded in the Z4 Unattributed-counterparties section.

## Per-CEX totals (across all source wallets)

| CEX brand | Etherscan-tagged outbound USD | BlockSec-resolved outbound USD (2026-05-21) | Combined outbound USD |
|--|--|--|--|
| Binance | $203,073,425 | — | $203,073,425 |
| Gate | $8,400,941 | — | $8,400,941 |
| Bybit | $3,096 | — | $3,096 |
| WhiteBIT | — | $10,400,000 | $10,400,000 |
| **All CEX brands combined** | **$211,477,461** | **$10,400,000** | **$221,877,461** |

## Inbound side (CEX → Zonda wallet)

| CEX brand | Source CEX address | Destination Zonda wallet | Inbound USD | Events |
|--|--|--|--|--|
| Bidesk | (multiple, 1 addr) | BitBay 879882 `0x879882c5…b54f`  **(PARTIAL source-wallet attribution)** | $3,976 | 1 |
| Binance | (multiple, 10 addr) | BitBay 879882 `0x879882c5…b54f`  **(PARTIAL source-wallet attribution)** | $4,817,532 | 539 |
| Binance | (multiple, 5 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $152,001 | 28 |
| Bitfinex | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $15,696 | 11 |
| Bitstamp | (multiple, 2 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $20,634 | 10 |
| Bybit | (multiple, 2 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $42,402 | 7 |
| Gate | (multiple, 1 addr) | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source-wallet attribution)** | $1,036,407 | 19 |
| Gate | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $158,566 | 34 |
| Gate | (multiple, 1 addr) | BitBay 879882 `0x879882c5…b54f`  **(PARTIAL source-wallet attribution)** | $7,483 | 1 |
| HTX | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $10,932 | 7 |

<details><summary>Show 8 more rows</summary>

| CEX brand | Source CEX address | Destination Zonda wallet | Inbound USD | Events |
|--|--|--|--|--|
| Kanga | (multiple, 1 addr) | BitBay 879882 `0x879882c5…b54f`  **(PARTIAL source-wallet attribution)** | $13,053 | 2 |
| Kraken | (multiple, 8 addr) | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source-wallet attribution)** | $3,600,757 | 655 |
| Kraken | (multiple, 1 addr) | Zonda 5 `0x6edf968d…5048` | $400,154 | 1 |
| Kraken | (multiple, 3 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $34,869 | 15 |
| KuCoin | (multiple, 2 addr) | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source-wallet attribution)** | $189,365 | 7 |
| KuCoin | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $1,742 | 1 |
| MEXC | (multiple, 1 addr) | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source-wallet attribution)** | $30,016 | 3 |
| MEXC | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $19,095 | 3 |

</details>

## Methodology cross-link

Per-wallet flow profiles cited above sit in the same directory tree:

- [Zonda 5](../wallets/ethereum/zonda-5.md)
- [Zonda 1](../wallets/ethereum/zonda-1.md)
- [Zonda 4](../wallets/ethereum/zonda-4.md)
- [Zonda BitBay 3f1eea](../wallets/ethereum/zonda-bitbay-3f1eea.md)
- [Zonda BitBay 56d943](../wallets/ethereum/zonda-bitbay-56d943.md)

**Receipts.** Same Dune executions and Etherscan HTML fetches used by the per-wallet flow profiles: [`../sources/dune/inventory-L1-per-wallet-2026-05-13.json`](../sources/dune/inventory-L1-per-wallet-2026-05-13.json) (query 7482290). The Etherscan public-name-tag HTML batch is retained in the working archive; the live Etherscan page for each address is the canonical primary source. BlockSec MetaSleuth API v3 receipts for the two 2026-05-21 attributions are mirrored at [`../sources/blocksec/labels-2026-05-21.json`](../sources/blocksec/labels-2026-05-21.json).
