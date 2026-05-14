# Zonda `0xd388…8046` family (Polygon)

A cluster of three Polygon Bitcoin-style cross-EVM addresses that share the vanity pattern `0xd388…8046` — including the previously-attributed Zonda 6 address (`0xd388009f…8046`) — and that exchange traffic almost exclusively with Zonda 5 on Polygon.

## Cluster members

| Address | Role on Polygon |
|---|---|
| `0xd388009f01bbe5e6d2cb6ba8525ca50b56308046` | Same as Ethereum **Zonda 6** ([→](../ethereum/zonda-6.md)). EVM addresses are chain-agnostic; the same key controls this address across chains. |
| `0xd388d1d810bf188f3456d8757e2b5949b44f8046` | Polygon-side sibling. Receives **67% of Zonda 5's real-token outbound** on Polygon (1,258 events sampled). |
| `0xd388c824b0684e7d1b04ad1e416e18ce562f8046` | Polygon-side sibling. 42 outbound events from Zonda 5. |

## Why the attribution holds

Two evidence types combined, per [methodology.md](../../methodology.md):

1. **Transaction relation.** All three addresses receive material ETH-equivalent token flow directly from the confirmed Zonda 5 multichain key (`0x6edf968d…`) on Polygon. The two sibling addresses sit at the very top of Zonda 5's outbound counterparty distribution on Polygon (#1 and ranked) — a position only a same-operator address could plausibly occupy.
2. **Cluster heuristic — vanity suffix.** All three share the constructed pattern `0xd388…8046`: identical first-2 bytes `d388` *and* identical last-2 bytes `8046`. Such a 4-byte vanity overlap is computationally non-trivial to generate and statistically distinctive in the address space; it is the canonical "operator-generated address family" signal documented across institutional crypto operations (compare F-007's `…b472` / `…7f73` family on the F-005 institutional MM/OTC desk).

Together — transaction relation tied to a confirmed Zonda wallet *plus* a non-coincidental vanity-suffix cluster *plus* (as a check) one cluster member already independently confirmed as Zonda 6 via Etherscan name tag — supports a **CONFIRMED** attribution for the two new members.

## Confidence

**CONFIRMED.** Inclusion criteria per [methodology.md](../../methodology.md) (transaction relation + cluster heuristic combined, with one cluster member already independently confirmed) are satisfied. Cross-citation from a name-tag source on the new members is still pending; a future name-tag hit would upgrade the entry from "CONFIRMED via composite primary citation" to "CONFIRMED with two independent primary citations". A name-tag hit naming a different entity would reopen this attribution.

## Activity (Polygon, probed 2026-05-13)

| Address | Native txs (first → most-recent) | ERC-20 events (first → most-recent) |
|---|---|---|
| `0xd388009f…8046` (Zonda 6, same-key) | 2023-10-30 → 2026-03-25 (575) | 2023-10-31 → 2026-01-14 (3,123) |
| `0xd388d1d8…8046` | 2025-08-05 → 2025-10-02 (310) | 2025-05-16 → 2025-10-04 (3,499) |
| `0xd388c824…8046` | 2025-04-01 → 2026-01-07 (12) | 2025-04-01 → 2026-01-07 (965) |

Source: Etherscan v2 `account/txlist` + `account/tokentx` (chainid 137), 10,000-event page each, sort=asc for first / sort=desc for most-recent.

## Sources

- WalletExplorer-style cluster reasoning + Polygon Etherscan v2 `tokentx` (chainid 137) sampled 2026-05-12. Source: `https://api.etherscan.io/v2/api?chainid=137&module=account&action=tokentx&address=0x6edf968d…` (the 10,000 most-recent events).
- Zonda 6 Etherscan name tag (separate primary attribution): see [zonda-6](../ethereum/zonda-6.md).
- Investigation flow context: case-internal F-008.

## Flow profile (Polygon, Dune-aggregated 2026-05-13)

**Scope note.** The d388 vanity-suffix sibling addresses (`0xd388d1d8…8046`, `0xd388c824…8046`) moved tokens for which Dune `tokens_polygon.transfers` has no liquid USD-equivalent price (predominantly ZND / TMPL). Both addresses return zero rows from the canonical ≥$1k Dune aggregation and so do not appear in the tables below. The flow profile here therefore covers only the Zonda 6 multichain address `0xd388009f…8046` on Polygon.

Full-history aggregation built from Dune `tokens_polygon.transfers` (≥$1,000 USD-equivalent per event). See [methodology](../methodology.md#flow-profile) for the SQL.

| Metric | Value |
|--|--|
| Gross IN (USD-equivalent at tx time) | $68,487,666 |
| Gross OUT (USD-equivalent at tx time) | $70,681,314 |
| Total throughput | $139,168,980 |
| Net direction | −$2,193,648 |
| Total events ≥$1k | 473 |
| Distinct external counterparties (≥$1k cumulative) | 4 |
| Identified counterparties in this section | 1 internal + 3 external (PolygonScan-tagged) |
| Counterparties without a public name tag | **1, aggregating ~$152,571 outbound and ~$0 inbound across captured rows** |
| Active period | 2023-11-22 → 2026-01-14 |

**Confidence:** CONFIRMED on totals. CONFIRMED on Internal and External-tagged rows below (each PolygonScan tag verified by fresh HTML fetch on 2026-05-13 saved to `case/sources/polygonscan-name-tags-2026-05-13/`). PARTIAL on the Unidentified counterparties row — entity attribution work is ongoing.

### Counterparties also in this inventory   [internal flows]

| Counterparty | Inbound USD | Outbound USD | Events |
|--|--|--|--|
| Zonda 5 `0x6edf968d…5048` | $57,282,318 | $13,614,690 | 159 |

### External destinations — confirmed via PolygonScan public name tags

| Counterparty | Tag (PolygonScan) | Outbound USD | Events |
|--|--|--|--|
| `0x10f7835f…d2ec` | Circle: Token Minter | $43,050,218 | 198 |
| `0x00000000…0000` | Null: 0x000…000 | $13,474,833 | 113 |
| `0x00000000…1010` | Polygon: POL Token | $389,002 | 2 |

### Unidentified counterparties

**This section is a known incomplete part of the analysis.** 1 of the 5 Polygon counterparties with ≥$1k cumulative flow carry no PolygonScan public name tag as of 2026-05-13 and do not appear in this inventory's roster. The unidentified rows captured here aggregate **$152,571 outbound** and **$0 inbound**. Entity-attribution work on these counterparties is ongoing.

**Receipts**: `case/sources/dune/polygon-per-wallet-2026-05-13.json` (query 7491823) + `case/sources/dune/polygon-totals-2026-05-13.json` (query 7491829) + `case/sources/polygonscan-name-tags-2026-05-13/<addr>.html`.

### External counterparties — confirmed via hildobby CEX Dune query 3237025

Each row here is sourced from [hildobby's Dune query 3237025](https://dune.com/queries/3237025), "All Known EVM CEX Addresses". The hildobby label set is treated as primary alongside Etherscan public name tags.

| Counterparty | Tag (hildobby) | Inbound USD | Outbound USD | Events (IN / OUT) |
|---|---|---:|---:|---:|
| `0xf89d7b9c864f589bbf53a82105107622b35eaa40` | Bybit 5 | $0 | $0 | 4 / 0 |
| `0xf977814e90da44bfa03b6295a0616a897441acec` | Binance 8 | $0 | $0 | 1 / 0 |
| `0xe84f75fc9caa49876d0ba18d309da4231d44e94d` | Kraken 24 | $0 | $0 | 1 / 0 |
| `0x082489a616ab4d46d1947ee3f912e080815b08da` | Binance 53 | $0 | $0 | 1 / 0 |
| `0x3727cfcbd85390bb11b3ff421878123adb866be8` | Bitbank 2 | $0 | $0 | 1 / 0 |
| `0xe7804c37c13166ff0b37f5ae0bb07a3aebb6e245` | Binance 48 | $0 | $0 | 45 / 0 |


### Top 50 unattributed counterparties by gross USD

These are the largest counterparties (full enumeration, no truncation) that carry no public name tag on the chain's primary block explorer, are not in this inventory's roster, and are not in hildobby's CEX-address Dune query. They sit at `label_source ∈ {below-cutoff, deferred-above-cutoff}` in the CSV.

| # | Counterparty | Inbound USD | Outbound USD | Events (IN / OUT) | First → last seen |
|---|---|---:|---:|---:|---|
| 1 | `0x10f7835f827d6cf035115e10c50a853d7fb2d2ec` | $0 | $43,052,918 | 0 / 207 | 2025-04-01 → 2026-01-14 |
| 2 | `0x0000000000000000000000000000000000001010` | $0 | $389,388 | 3 / 3 | 2024-07-17 → 2024-09-26 |
| 3 | `0xa25b76424b676cbb48e1189926c1c8d8fc083f42` | $0 | $152,571 | 0 / 1 | 2023-11-22 → 2023-11-22 |
| 4 | `0x58a91fce89b5a4b2771c83a96078bc4854006c03` | $4 | $0 | 1 / 0 | 2024-04-13 → 2024-04-13 |
| 5 | `0x6edffd3c53ce226b0b16fbe960e2d69af31c5048` | $0 | $0 | 20 / 13 | 2024-04-25 → 2025-03-03 |
| 6 | `0x0000c72f94112a0ef4f6386bcba7d5f849360000` | $0 | $0 | 1 / 0 | 2024-10-06 → 2024-10-06 |
| 7 | `0x00009ba1459586753ddcc5373d716c8e85d00000` | $0 | $0 | 1 / 0 | 2024-10-06 → 2024-10-06 |
| 8 | `0x0000d124ae5df5c35edffad0f5c74528ae3c0000` | $0 | $0 | 1 / 0 | 2024-10-06 → 2024-10-06 |
| 9 | `0x0000f9b4e1b0336a65dcd0b8daef34ec2c6b0000` | $0 | $0 | 1 / 0 | 2024-10-06 → 2024-10-06 |
| 10 | `0x000082fba4d7e96dc528fccda74d036995ca0000` | $0 | $0 | 1 / 0 | 2024-10-06 → 2024-10-06 |
| 11 | `0x00007ea6a03504487a53b740e0cfe5ea8ef70000` | $0 | $0 | 1 / 0 | 2024-10-11 → 2024-10-11 |
| 12 | `0xfa395a3cb794a5307b3de49cf9bc15f441f4ebce` | $0 | $0 | 1 / 0 | 2024-04-14 → 2024-04-14 |
| 13 | `0x3c499c542cef5e3811e1192ce70d8cc03d5c3359` | $0 | $0 | 7 / 0 | 2024-08-02 → 2025-06-26 |
| 14 | `0xdf2140dee6b07ae495382bc1cd446f7b328f63e3` | $0 | $0 | 34 / 0 | 2025-02-07 → 2025-11-18 |
| 15 | `0x000024d1899b81cef4764aa4bdf34e08a0030000` | $0 | $0 | 4 / 4 | 2024-12-18 → 2024-12-18 |
| 16 | `0xca86706c7a6a29e96288d030eb0f4027dd183da2` | $0 | $0 | 1 / 0 | 2024-07-04 → 2024-07-04 |
| 17 | `0x9c8cc7d9dd29ccb00e9a3895194e1e9dcac96373` | $0 | $0 | 1 / 0 | 2025-04-01 → 2025-04-01 |
| 18 | `0x6edf0a4128a781e6f81e1becb9d6f528434e5048` | $0 | $0 | 7 / 1094 | 2025-08-05 → 2025-11-09 |
| 19 | `0x6edf2527128b94b0c93ec23123772dd4fcf95048` | $0 | $0 | 0 / 1088 | 2025-05-13 → 2025-09-30 |
| 20 | `0x82e88a0a7719e717a6a97268b8343061033d8be1` | $0 | $0 | 2 / 0 | 2025-12-09 → 2025-12-09 |
| 21 | `0x337827814155ecbf24d20231fca4444f530c0555` | $0 | $0 | 1 / 0 | 2025-01-22 → 2025-01-22 |
| 22 | `0x6985884c4392d348587b19cb9eaaf157f13271cd` | $0 | $0 | 1 / 0 | 2024-07-12 → 2024-07-12 |
| 23 | `0x03b54a6e9a984069379fae1a4fc4dbae93b3bccd` | $0 | $0 | 2 / 0 | 2025-03-28 → 2025-04-17 |
| 24 | `0xc3c7d422809852031b44ab29eec9f1eff2a58756` | $0 | $0 | 1 / 0 | 2025-01-15 → 2025-01-15 |
| 25 | `0xec7be89e9d109e7e3fec59c222cf297125fefda2` | $0 | $0 | 1 / 0 | 2025-02-02 → 2025-02-02 |
| 26 | `0x0000143d63bd6e233d71a27c4c2c84c404f00000` | $0 | $0 | 0 / 2 | 2024-11-08 → 2024-11-08 |
| 27 | `0x3a58a54c066fdc0f2d55fc9c89f0415c92ebf3c4` | $0 | $0 | 4 / 0 | 2024-07-02 → 2024-10-01 |
| 28 | `0x6edf9240c7a2186946ef2892b6081602c4cd5048` | $0 | $0 | 9 / 11 | 2024-12-20 → 2025-03-03 |
| 29 | `0x00d5b8c2afd0588e59632b6eb29f65bd4d0a6041` | $0 | $0 | 1 / 0 | 2024-09-06 → 2024-09-06 |
| 30 | `0x2791bca1f2de4661ed88a30c99a7a9449aa84174` | $0 | $0 | 1 / 0 | 2025-01-22 → 2025-01-22 |
| 31 | `0x6edfaf539ed1e2bad5eecf204bc605bbdc725048` | $0 | $0 | 0 / 28 | 2024-12-20 → 2025-08-06 |
| 32 | `0xf329e36c7bf6e5e86ce2150875a84ce77f477375` | $0 | $0 | 1 / 0 | 2024-07-17 → 2024-07-17 |
| 33 | `0x67366782805870060151383f4bbff9dab53e5cd6` | $0 | $0 | 2 / 0 | 2025-02-07 → 2025-05-13 |
| 34 | `0x8f3cf7ad23cd3cadbd9735aff958023239c6a063` | $0 | $0 | 1 / 0 | 2025-01-27 → 2025-01-27 |
| 35 | `0x53075c1cd19d6b9fe5cb702c6a3fd2480e24bbad` | $0 | $0 | 0 / 72 | 2025-03-25 → 2025-04-07 |
| 36 | `0x9c2c5fd7b07e95ee044ddeba0e97a665f142394f` | $0 | $0 | 1 / 0 | 2024-07-17 → 2024-07-17 |
| 37 | `0xb0897686c545045afc77cf20ec7a532e3120e0f1` | $0 | $0 | 1 / 0 | 2024-07-29 → 2024-07-29 |
| 38 | `0x05b27f3a054adf50e21fb873ea1cfda1911c5048` | $0 | $0 | 0 / 24 | 2024-12-27 → 2025-03-03 |
| 39 | `0x6edf100444a66aa6adfb222ca9f5e6563b025048` | $0 | $0 | 0 / 6 | 2025-05-13 → 2025-05-16 |
| 40 | `0x6f2fc630811183235be6949361f3f8f380c3ce73` | $0 | $0 | 1 / 0 | 2024-04-16 → 2024-04-16 |
| 41 | `0x00003984c7ad2c9e2d9a77e467f007d7d0ea0000` | $0 | $0 | 0 / 2 | 2024-10-19 → 2024-10-19 |
| 42 | `0x0000b9687ff92199ffa1a4fbdbc7006717840000` | $0 | $0 | 0 / 2 | 2024-10-11 → 2024-10-11 |
| 43 | `0xc2132d05d31c914a87c6611c10748aeb04b58e8f` | $0 | $0 | 18 / 0 | 2024-09-01 → 2025-06-05 |
| 44 | `0x0000e844b052bf8f225ceca958f8fdb68e9d0000` | $0 | $0 | 0 / 2 | 2024-11-04 → 2024-11-04 |
| 45 | `0x71c7656ec7ab88b098defb751b7401b5f6d8976f` | $0 | $0 | 1 / 0 | 2025-07-11 → 2025-07-11 |
| 46 | `0x3a0b42ce6166abb05d30ddf12e726c95a83d7a16` | $0 | $0 | 1 / 0 | 2024-07-18 → 2024-07-18 |
| 47 | `0x239b9c1f24f3423062b0d364796e07ee905e9fce` | $0 | $0 | 7 / 0 | 2025-04-17 → 2026-01-01 |
| 48 | `0xf328b73b6c685831f238c30a23fc19140cb4d8fc` | $0 | $0 | 1 / 0 | 2024-04-15 → 2024-04-15 |
| 49 | `0x7ceb23fd6bc0add59e62ac25578270cff1b9f619` | $0 | $0 | 5 / 0 | 2024-08-07 → 2025-03-14 |
| 50 | `0x6edf591193ebb235b35344f1b82829dd2b055048` | $0 | $0 | 0 / 8 | 2024-04-15 → 2024-07-17 |

## Counterparty enumeration (full)

Full per-counterparty enumeration with no truncation and a $0 USD floor is published as a CSV alongside this page: [`zonda-d388-family-polygon-counterparties.csv`](zonda-d388-family-polygon-counterparties.csv). The CSV covers every distinct counterparty that ever transferred to or from this wallet across its full history on Polygon; rows are sorted by gross USD flow descending. Schema and label-source precedence are documented in [`methodology.md`](../methodology.md#inventory-profile-csv).

