# Cross-wallet CEX off-ramp summary (Ethereum, Dune-aggregated 2026-05-13)

Sum of outbound USD-equivalent value (at transaction time) from each ZondaCrypto inventory wallet to Etherscan-tagged centralised-exchange addresses. The classification rule is mechanical: any external counterparty whose Etherscan Public Name Tag begins with a CEX brand (Binance, Kraken, KuCoin, Gate, Bitstamp, Bitfinex, Bybit, MEXC, HTX, Bidesk, Kanga, etc.) is bucketed under that brand. The CEX name tag was verified by a fresh HTML fetch on 2026-05-13 for every address listed; receipts at `case/sources/etherscan-name-tags-2026-05-13/<addr>.html`.

**Scope.** Etherscan-tagged CEX deposit / hot-wallet addresses only. Heuristic operator-network counterparties, OTC desks, or aggregator addresses not carrying a public name tag are out of scope of this summary by design — they belong in each wallet's Unidentified-counterparty row and remain unattributed under the inventory's primary-citation standard until cleared individually.

**Confidence.** CONFIRMED on totals: every cell is a Dune-aggregation sum filtered to addresses with a fresh-verified Etherscan public name tag. PARTIAL on rows where the source-wallet attribution itself is at PARTIAL tier (the BitBay-era wallets — flagged below).

## Per-CEX × per-source-wallet outbound (USD)

| CEX brand (Etherscan tag prefix) | Source Zonda wallet | Outbound USD | Events | Distinct tagged addresses |
|--|--|--|--|--|
| Binance | Zonda 5 `0x6edf968d…5048` | $121,971,089 | 4,222 | 12 |
| Binance | Zonda 1 `0xf646cbe3…b95e` | $49,659,754 | 1,991 | 6 |
| Binance | Zonda 4 `0x2b645268…763a` | $31,433,084 | 697 | 4 |
| Binance | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source)** | $8,399 | 1 | 1 |
| Binance | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source)** | $1,099 | 1 | 1 |
| Bybit | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source)** | $3,096 | 3 | 1 |
| Gate | Zonda 5 `0x6edf968d…5048` | $8,049,973 | 85 | 1 |
| Gate | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source)** | $350,968 | 11 | 1 |

## Per-CEX totals (across all source wallets)

| CEX brand | Total outbound USD | Total events | Distinct tagged deposit addresses | Source wallets |
|--|--|--|--|--|
| **Binance** | $203,073,425 | 6,912 | 16 | 5 |
| **Gate** | $8,400,941 | 96 | 2 | 2 |
| **Bybit** | $3,096 | 3 | 1 | 1 |
| **All CEX brands combined** | **$211,477,461** | — | — | — |

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
| Kanga | (multiple, 1 addr) | BitBay 879882 `0x879882c5…b54f`  **(PARTIAL source-wallet attribution)** | $13,053 | 2 |
| Kraken | (multiple, 8 addr) | BitBay 56d943 `0x56d943ae…4778`  **(PARTIAL source-wallet attribution)** | $3,600,757 | 655 |
| Kraken | (multiple, 1 addr) | Zonda 5 `0x6edf968d…5048` | $400,154 | 1 |
| Kraken | (multiple, 3 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $34,869 | 15 |
| KuCoin | (multiple, 2 addr) | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source-wallet attribution)** | $189,365 | 7 |
| KuCoin | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $1,742 | 1 |
| MEXC | (multiple, 1 addr) | BitBay 3f1eea `0x3f1eea8d…0539`  **(PARTIAL source-wallet attribution)** | $30,016 | 3 |
| MEXC | (multiple, 1 addr) | Zonda Deposit Wallet `0x82c82923…900c` | $19,095 | 3 |

## Methodology cross-link

Per-wallet flow profiles cited above sit in the same directory tree:

- [Zonda 5](../scouting/wallets/ethereum/zonda-5.md)
- [Zonda 1](../scouting/wallets/ethereum/zonda-1.md)
- [Zonda 4](../scouting/wallets/ethereum/zonda-4.md)
- [BitBay 3f1eea](../scouting/wallets/ethereum/bitbay-3f1eea.md)
- [BitBay 56d943](../scouting/wallets/ethereum/bitbay-56d943.md)

**Receipts.** Same Dune executions and Etherscan HTML fetches used by the per-wallet flow profiles: `case/sources/dune/stage1-L1-per-wallet-2026-05-13.json` (query 7482290) and `case/sources/etherscan-name-tags-2026-05-13/`.
