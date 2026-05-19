# Zonda (BitBay) (0x3ef6683f…2eda)

> **Plain-language summary.** An Ethereum deposit-address attributed to ZondaCrypto / BitBay by BlockSec MetaSleuth (`name_tag = "Zonda (BitBay): Deposit Address"`). Single primary source — recorded as PARTIAL tier pending a second independent labelling. Operates as a deposit-receipt hop: 100% of outbound flow ($120.1 million, 793 events) lands on Zonda 5 alone, while the inbound side is dominated by 17 hildobby-tagged centralised-exchange hot wallets across 9 exchanges.

**Address:** `0x3ef6683f2553af861f91194d23bdf8522d1f2eda`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth. Acts as a deposit-receipt hop that funnels customer flow from 17+ centralised-exchange hot wallets to Zonda 5 (`0x6edf968d…5048`, the operator's multichain MM wallet). The same operational shape as `0xced004…2f06` (the other BlockSec-attributed Zonda Deposit Address in this inventory) at roughly 2.8× the throughput.

**Confidence:** PARTIAL.

> *CONFIRMED = two independent primary sources. PARTIAL = single primary source. HEURISTIC = on-chain pattern only, working hypothesis. See [glossary](../../glossary.md).*

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, and `name_tag = "Zonda (BitBay): Deposit Address"`.[^1] No matching public name tag on Etherscan as of 2026-05-18; no row in hildobby's Dune compilation (query 3237025). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

Structural corroboration: 100% of outbound flow ($120.1M / 793 events) goes to Zonda 5 alone, with no other recipient. Inbound side is dominated by 17 hildobby-tagged CEX hot wallets across 9 exchanges (full table below). The deposit-address operational signature is unambiguous.

## Activity (Ethereum, probed 2026-05-18)

- First event: 2023-05-31.
- Most recent event: 2026-03-29.
- Total events: 2,465 (1,322 IN + 1,143 OUT).
- Distinct counterparties: 75.

Source: Dune `tokens_ethereum.transfers` full-history aggregation, no truncation, $0 USD floor. Reproducible via query `7500518` execution `01KRZA9HZVRW70Y2QDTA2V4FFR`.

## Flow profile (Ethereum, Dune-aggregated 2026-05-18)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if hildobby's CEX-address Dune compilation carries an attribution or Etherscan carries a Public Name Tag, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profiles) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $119,999,069 |
| Gross OUT (USD-equivalent at tx time) | $120,140,272 |
| Total throughput (gross in + out) | $240,139,341 |
| Net direction | -$141,203 |
| Distinct counterparties (no threshold) | 75 |
| Identified counterparties in this section | 2 internal + 17 external (hildobby-tagged) + 1 external (Etherscan-tagged) |
| Counterparties without a public name tag | **55, of which 15 are above the $10k cumulative cutoff and 40 are below** |
| Active period | 2023-05-31 → 2026-03-29 |

**Confidence:** CONFIRMED on totals. CONFIRMED on per-counterparty Internal + hildobby-tagged + Etherscan-tagged rows. PARTIAL on the Unattributed rows — entity attribution work is ongoing in the case's internal working notes.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $0 | $120,140,272 | 0 / 793 |
| Zonda Deposit Funder 1 `0x5bff49ee…9503` | $659 | $0 | 327 / 0 |

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags. Listed by descending inbound USD.

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x267be1c1…ffdc0` | Kraken 4 | $20,875,482 | 62 |
| `0x89e51fa8…7c40` | Kraken 7 | $10,699,969 | 80 |
| `0x0d070796…92fe` | Gate.io 1 | $4,120,529 | 19 |
| `0x9642b23e…5d4e` | MEXC 21 | $3,907,548 | 13 |
| `0xae2d4617…c673f` | Kraken 10 | $2,726,471 | 11 |
| `0x16b2b042…c415` | Kraken 43 | $2,520,738 | 71 |
| `0xc6bed363…63da` | Kraken 8 | $2,135,824 | 65 |
| `0xd91efec7…0747` | KuCoin 26 | $1,995,062 | 6 |
| `0x58edf782…6a51` | KuCoin 32 | $1,353,765 | 7 |
| `0x56eddb7a…b17f` | Binance 17 | $1,025,050 | 2 |

<details><summary>Show 7 more rows</summary>

| Counterparty | Tag (hildobby) | Inbound USD | Events |
|---|---|---:|---:|
| `0x6d0cf1f6…3d26` | Kraken 55 | $888,292 | 92 |
| `0x28c6c062…1d60` | Binance 14 | $343,782 | 19 |
| `0xfbb1b73c…bb98` | Bittrex 1 | $282,791 | 14 |
| `0xdfd5293d…963d` | Binance 16 | $238,365 | 20 |
| `0x7f604d59…b752` | Bitstamp 60 | $236,299 | 6 |
| `0x21a31ee1…5549` | Binance 15 | $197,465 | 16 |
| `0x2982bb64…7d67` | BitMart 18 | $47 | 1 |

</details>

(Aggregate hildobby-tagged IN: $51.6M / 17 distinct CEXes-of-record across 9 exchanges — Kraken, Binance, Gate.io, MEXC, KuCoin, Bitstamp, Bittrex, BitMart, plus the Etherscan-tagged Binance Hot Wallet 34 row below; ~43% of total inbound USD.)

### External counterparties — confirmed via Etherscan public name tag

| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|---|---|---:|---:|
| `0xee7ae85f…4055` | Binance: Hot Wallet 34 | $6,559 | 1 |

### Unattributed counterparties

**This section is a known incomplete part of the analysis.** Of the 75 distinct counterparties in the full enumeration, 55 carry no public name tag in any free attribution source as of 2026-05-18. The unattributed rows aggregate **$0 outbound** (all outbound is internal-to-Zonda-5) and **$66,444,373 inbound**, of which **$43,170,335 (131 events, 36% of total inbound) comes from `0xead65957…ae880d`** — the largest unattributed inflow source. The next-largest is `0x42b6de74…498b` at **$18,264,458 (7 events)**. These two together account for ~92% of the unattributed inbound. The remaining 13 unattributed-but-above-$10k counterparties aggregate $5.0M; below-$10k counterparties aggregate ~$0.005M. Entity-attribution work on these counterparties is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-3ef668-counterparties.csv](zonda-bitbay-3ef668-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv).

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: `../../sources/dune/zonda-bitbay-3ef668-2026-05-18.json` (query 7500518, execution `01KRZA9HZVRW70Y2QDTA2V4FFR`).
- BlockSec MetaSleuth API v3 response: `../../sources/blocksec/labels-2026-05-18.json` (key `0x3ef6683f2553af861f91194d23bdf8522d1f2eda`).

## Block-explorer link

https://etherscan.io/address/0x3ef6683f2553af861f91194d23bdf8522d1f2eda

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-18 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`. Receipt at `../../sources/blocksec/labels-2026-05-18.json`. Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
