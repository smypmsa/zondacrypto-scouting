# Inventory outbound-volume collapse (Ethereum, Dune-aggregated 2026-05-21)

> **Plain-language summary.** Monthly outbound USD-equivalent volume from the inventoried Ethereum wallets (USDT + USDC + native ETH, excluding inv-to-inv self-rotation) drops from **$19.86M in January 2026** to **$0.31M in May 2026 (partial, through May 21)** — a **98.4% decline across five consecutive months, monotone with no recovery month**. The Feb–May 2026 monthly average ($6.05M) is about 31% of the 2025 monthly median ($19.57M), or 69% below.

**Scope.** Outbound transfers from the 29 inventoried Ethereum wallets active in the W3 sender set (Z1–Z6 + early operator + BB-879882 + others), in three token classes (USDT, USDC, native ETH at $2,500 reference). Inv-to-inv transfers are excluded so the figure reflects net outbound volume rather than internal rotation. Polygon, Bitcoin, and Ethereum L2 chains (Arbitrum, Optimism, Base, etc.) are out of scope of this observation; a multichain re-run is a follow-up.

**Confidence.** CONFIRMED on the per-month arithmetic. Every row is a Dune-aggregation sum on `erc20_ethereum.evt_transfer` + `ethereum.transactions` from a single execution receipt mirrored below. The on-chain figure is what it is; this page does not interpret the cause.

## Per-month outbound volume (Ethereum, all inventoried senders)

| Month | Outbound USD | Δ vs Jan 2026 | Δ vs prior month |
|--|--|--|--|
| 2026-01 | $19,858,887 | baseline | — |
| 2026-02 | $11,274,064 | −43.2% | −43.2% |
| 2026-03 | $8,247,167 | −58.5% | −26.8% |
| 2026-04 | $4,353,551 | −78.1% | −47.2% |
| 2026-05 (partial, through May 21) | $310,425 | −98.4% | −92.9% |

**Feb–May 2026 monthly average:** $6,046,302. **2025 monthly median (twelve months Jan–Dec):** $19,571,192. The Feb–May 2026 monthly average is ≈31% of the 2025 monthly median, i.e. roughly 69% below the 2025 monthly run rate.

## Historical Q1 context (reproducible from the same receipt)

The 2026 Q1 monthly average is on par with prior pre-2024 Q1 averages, but the trajectory across the quarter is different: in 2022 and 2023, Q1 months sat near the year's running average; in 2026, the Jan figure is itself near the 2025 monthly median and each successive month drops monotonically.

| Year | Q1 monthly average (USD, Ethereum inv outbound) |
|--|--|
| 2021 | $58.4M (DeFi-summer aftermath; Z1 + Z4 high-throughput period) |
| 2022 | $12.8M |
| 2023 | $12.6M |
| 2024 | $23.3M |
| 2025 | $14.5M |
| 2026 | $13.1M (Jan–Mar; April collapses to $4.4M and May to $0.3M) |

The 2026 anomaly is not visible at the Q1-average level; it is visible in the **month-on-month monotone decline** that begins in February and continues through May without a recovery month.

## Methodology

Per (month, sender, bucket, entity) grouping of inventory-OUT transfers, restricted to Ethereum mainnet and to the three token classes USDT, USDC, and native ETH. ETH valued at a $2,500 flat reference; stables at face value. Inv-to-inv self-rotation is filtered out. The per-month figure in the table above is the sum across all senders and all (`cex_attributed` + `hildobby_cex` + `unattributed`) buckets for the calendar month.

## Reproducibility

- Dune query: `7500518`, execution `01KS62AM2BRH8PQPH2V4Q7CPMA` (submitted 2026-05-21).
- Receipt: [`../sources/dune/w3-zonda-out-monthly-binned-2026-05-21.json`](../sources/dune/w3-zonda-out-monthly-binned-2026-05-21.json) (334 rows; full execution payload mirrored).
- Per-month figures above are the grand-total `usd_total` summed across all rows in the receipt grouped by `month` (first 7 characters of the `month` field).

## Methodology cross-link

- Per-wallet flow profiles for the dominant 2026 senders: [Zonda 5](../wallets/ethereum/zonda-5.md) (the largest single contributor to the 2026 monthly volume), [Zonda 1](../wallets/ethereum/zonda-1.md), [Zonda 4](../wallets/ethereum/zonda-4.md).
- The cross-wallet [CEX off-ramp summary](cex-off-ramp-summary.md) reports the lifetime CEX-attributed slice of the same outbound volume.
- See [methodology](../methodology.md) for confidence tiers and the receipts-mirroring policy.

## Scope and negative space

- **Ethereum mainnet only.** This observation does not cover Polygon, Bitcoin, or Ethereum L2 chains. The "volume shifted to L2 / other chain" alternative reading is not tested here.
- **Outbound side only.** This is not a balance-of-funds claim and not a customer-side activity figure. Customer wallets are jurisdictionally diffuse and not part of this inventory.
- **No interpretation.** The on-chain figure is what it is. The case-level connection to publicly-reported withdrawal events is the reader's to draw; this page reports the math, not the cause.
- **Sender set fixed at the 2026-05-21 inventory snapshot.** A withdrawal-side address that is not yet in the inventory and absorbs the missing volume would not appear here; the 8 unattributed candidates aggregate to ~$31M lifetime IN-from-inventory, materially below the missing monthly volume even if all were Zonda-controlled.
