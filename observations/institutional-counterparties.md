# Institutional counterparties (non-CEX, BlockSec-resolved)

A roster of non-CEX institutional counterparties that BlockSec MetaSleuth's address-label API resolves on counterparty addresses sitting downstream of ZondaCrypto-inventoried Ethereum wallets. CEX-side resolutions live in [`cex-off-ramp-summary.md`](cex-off-ramp-summary.md); this page covers everything else — RWA vault settlement addresses, lending protocols, custodied institutional infrastructure, and similar non-exchange entities — where BlockSec returns a `main_entity` that is not a centralised exchange brand. Each row is reproducible against the mirrored BlockSec receipt for the cited capture date.

**Scope.** Counterparty addresses that (a) have an on-chain bilateral path to a ZondaCrypto-inventoried Ethereum wallet, and (b) carry a non-CEX `main_entity` in BlockSec MetaSleuth at the cited capture date. Multi-hop paths are reported in the "Hops from inventory" column so the on-chain distance from a Zonda-tagged address is explicit.

**Confidence.** CONFIRMED on the BlockSec attribution itself (single primary source per row; receipt mirrored). The on-chain bilateral magnitudes are CONFIRMED from indexed `tokens_ethereum.transfers` aggregations. The structural reading of what each attribution means for ZondaCrypto's institutional-flow architecture is HEURISTIC per row and is annotated in the row's notes.

## MakerDAO RWA-007 — Coinbase Custody settlement address

| Field | Value |
|---|---|
| Counterparty address | `0xc3acf3b96e46aa35dbd2aa3bd12d23c11295e774` |
| BlockSec `name_tag` | `Maker: Rwa007 A Coinbase Custody` |
| BlockSec `main_entity` | `Maker` |
| BlockSec categories | `STABLE COIN` (code 3024) + `RWA` (code 3045) |
| Capture date | 2026-05-22, chain_id=1 |
| Receipt | [`../sources/blocksec/labels-2026-05-22.json`](../sources/blocksec/labels-2026-05-22.json) |
| Nearest inventory wallet | [Zonda 1](../wallets/ethereum/zonda-1.md) `0xf646cbe3…b95e` |
| Hops from inventory | Two (Zonda 1 → relay `0x1990abd6…244181` → MM/OTC hub `0x5ee84d30…6916b` → MakerDAO RWA-007 Coinbase Custody). The relay and the hub do not themselves carry a BlockSec primary attribution at the 2026-05-22 index date; they sit in the Zonda 1 wallet page's `Unattributed counterparties` section. |
| Bilateral magnitude | $552M lifetime USDC OUT from the MM/OTC hub to this address across 12 events. Lifetime aggregation; full history. |
| Source receipt for the bilateral magnitude | [`../sources/dune/d9-f005-institutional-10k-reprofile-2026-05-21.json`](../sources/dune/d9-f005-institutional-10k-reprofile-2026-05-21.json) — Dune query 7500518, execution `01KS5C46T4MP643ZHDKH886SPY`, lifetime aggregation of `tokens_ethereum.transfers` at $10k/event threshold |

**Plain-language reading.** RWA-007 was a MakerDAO collateral type backed by securitised real-world-asset exposure; the Coinbase Custody address is the settlement endpoint where USDC moves into and out of the vault. The on-chain flow shows that the largest single USDC OUT counterparty of the MM/OTC hub sitting two hops downstream of Zonda 1 is this MakerDAO RWA-007 settlement address. The on-chain graph establishes the path but does not establish that any specific Zonda customer USDC dollar reached the MakerDAO vault — the path is multi-hop and the intermediate hub is not exclusively used for Zonda flow. The reading is at the structural level: ZondaCrypto's USDC OUT side has on-chain exposure to the institutional venue that handles MakerDAO's RWA-007 collateral.

**Out of scope for this page.** Which RWA originator managed RWA-007 at the cited capture date, what governance arrangement was in force, and which specific RWA-007 vault operations correspond to the 12 observed events. Those are real-world-entity attribution questions that go beyond what the BlockSec primary attribution itself states. Public MakerDAO governance forum threads (forum.makerdao.com) carry historical RWA-007 origination context for readers who want to pursue it.

## Methodology cross-link

See [`../methodology.md`](../methodology.md) for the confidence-tier definitions and the receipts-mirroring policy. The BlockSec MetaSleuth API v3 endpoint and the response-field semantics (`main_entity`, `attributes`, `name_tag`) are documented there. Aggregations against `tokens_ethereum.transfers` follow the same Dune-aggregation policy used by the per-wallet flow profiles.
