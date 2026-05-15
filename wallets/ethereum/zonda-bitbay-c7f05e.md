# Zonda (BitBay) (0xc7f05e…9305)

**Address:** `0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305`

**Chain:** Ethereum.

**Role:** ZondaCrypto / BitBay-attributed deposit address per BlockSec MetaSleuth.

**Confidence:** PARTIAL.

## Attribution

BlockSec MetaSleuth's address-label API v3 returns this address with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE` (code 3011), attribute `DEPOSIT ADDRESS` (code 4007), and `name_tag = "Zonda (BitBay): Deposit Address"`.[^1] The entity description in the response links the operator at `zondacrypto.com`. No matching public name tag on Etherscan as of 2026-05-14; no row in hildobby's Dune compilation (query 3237025). BlockSec is the sole primary source at this time; recorded as PARTIAL pending a second independent labelling.

## Activity (Ethereum, probed 2026-05-14)

- Native txs: first 2019-05-01 (block 7676630); most recent 2026-03-18 (block 24684058); 2,029 events (within a single 10,000-event Etherscan page — full count, not truncated).
- ERC-20 events: first ≈2019 (block range covered by `tokentx` paginated sweep); most recent 2020-11-07; 8 events.

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 1), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Flow profile (Ethereum, Dune-aggregated 2026-05-14)

Full-history aggregation of native ETH and ERC-20 token transfers where this wallet appears as `from` or `to`, USD-valued at transaction time using Dune `tokens_ethereum.transfers`. Counterparties are flagged **Internal** if they appear in this inventory's roster, **External-tagged** if Etherscan / hildobby carries a verified public attribution, or **Unattributed** otherwise. See [methodology](../../methodology.md#flow-profile) for the SQL. Reproducible from Dune query `7482290` execution `01KRJWX2C88JW62MM144PAS1E5`.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $53,742,378 |
| Gross OUT (USD-equivalent at tx time) | $51,148,033 |
| Total throughput (gross in + out) | $104,890,411 |
| Net direction | +$2,594,345 |
| Distinct counterparties (no threshold) | 32 |
| Identified counterparties in this section | 4 internal + 17 external (Etherscan-tagged) |
| Counterparties without a public name tag | **11, of which 9 are above the $10k cumulative cutoff and 2 are confirmed no-tag from a fresh Etherscan fetch** |
| Active period | 2019-05-02 → 2026-03-24 |

**Confidence:** CONFIRMED on totals (Gross IN/OUT, throughput, distinct-counterparty count). CONFIRMED on per-counterparty Internal + Etherscan-tagged rows below.

### Counterparties also in this inventory

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| [Zonda 3](zonda-3.md) | $0 | $51,116,423 | 88 |
| [Zonda 1](zonda-1.md) | $0 | $24,250 | 1 |
| [Zonda 2](zonda-2.md) | $0 | $7,358 | 1 |
| [ZNDStaking](znd-staking.md) | $0 | $1 | 1 |

This wallet is the inflow side of a sweep relationship: it receives from many external CEX-deposit-address counterparties and forwards (sweeps) to Zonda 3 in periodic large batches.

### External destinations / sources — confirmed via Etherscan public name tags

All 17 Etherscan-tagged external counterparties are on the **inbound** side. The outbound side concentrates almost entirely on Zonda 3 (above). Listed by descending inbound USD.

| Counterparty | Tag (Etherscan) | Inbound USD | Events |
|--|--|--|--|
| `0x0681d8db…edbbf` | Binance 4 | $9,453,912 | 390 |
| `0xd551234a…92ff` | Binance 2 | $7,994,610 | 389 |
| `0x564286...3aaced` | Binance 3 | $7,907,700 | 364 |
| `0x3f5ce5fb…f0be` | Binance | $7,135,621 | 382 |
| `0x708396f1…b82f` | Binance 11 | $4,060,279 | 74 |
| `0x85b931a3…d69b` | Binance 10 | $3,226,491 | 64 |
| `0x56eddb7a…b17f` | Binance 17 | $3,121,956 | 37 |
| `0x28c6c062…1d60` | Binance 14 | $2,377,956 | 27 |
| `0xdfd5293d…963d` | Binance 16 | $2,252,322 | 26 |
| `0x21a31ee1…5549` | Binance 15 | $2,173,279 | 28 |
| `0x9696f59e…6976` | Binance 18 | $2,032,880 | 26 |
| `0x4976a4a0…2327` | Binance 20 | $1,798,927 | 22 |
| `0x8f22f206…0c8f` | Binance 13 | $800,967 | 10 |
| `0x832f1667…15d6` | BTC Turk: Main Wallet | $235,782 | 2 |
| `0xc55edda…e7fa` | BTC Markets 2 | $219,083 | 2 |
| `0xdf4b6fb7…145b` | Liquid 2 | $27,336 | 2 |
| `0x0d070796…92fe` | Gate Deposit | $11,376 | 1 |

The flow shape: customer accounts at Binance (predominantly), BTC Turk (Turkey), BTC Markets (Australia), Liquid (Liquid Group / formerly Quoine, FTX-acquired 2022), and Gate.io withdrew to this address; this address swept the accumulated balance to Zonda 3 in periodic batches. The earliest inflow is 2019-05; the most recent is 2026-03.

### Unattributed counterparties

11 counterparties carry no public name tag on Etherscan as of 2026-05-14 and are not in this inventory's roster:
- 9 sit above the $10,000 cumulative cutoff (range $11k–$92k each)
- 2 were fetched and confirmed to have no Public Name Tag on Etherscan

These addresses are listed in the CSV at `label_source ∈ {deferred-above-cutoff, no-public-tag}`. Entity-attribution work on these 11 addresses is ongoing.

## Counterparty enumeration (full)

A complete enumeration of every counterparty in this wallet's full transaction history is available as a CSV at [zonda-bitbay-c7f05e-counterparties.csv](zonda-bitbay-c7f05e-counterparties.csv). Columns documented in [methodology.md § Inventory profile CSV](../../methodology.md#inventory-profile-csv). Loadable into Jupyter / spreadsheet for any reader.

**Receipts (for reproduction)**:
- Dune full-history per-counterparty aggregation: `../../sources/dune/a20-counterparties-2026-05-14.json` (query 7482290, execution `01KRJWX2C88JW62MM144PAS1E5`).
- Etherscan HTML name-tag fetches (2026-05-14 closure pass, browser-style User-Agent, ~0.85s pacing) retained in the working archive — see [methodology § Receipts](../../methodology.md#receipts-and-reproducibility).

## Block-explorer link

https://etherscan.io/address/0xc7f05e700f3f1fb6dc62428e2d0e4280110c9305

[^1]: BlockSec MetaSleuth, address-label API v3. Response captured 2026-05-14 with `main_entity = "Zonda (BitBay)"`, category `EXCHANGE`, attribute `DEPOSIT ADDRESS`, name_tag `"Zonda (BitBay): Deposit Address"`. Receipt at [`sources/blocksec/labels-2026-05-14.json`](../../sources/blocksec/labels-2026-05-14.json). Endpoint: https://aml.blocksec.com/address-label/api/v3/labels
