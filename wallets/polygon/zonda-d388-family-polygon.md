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
