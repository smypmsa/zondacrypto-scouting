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

## Wintermute — three institutional-MM bilateral addresses with the MM/OTC hub two hops downstream of Zonda 1

The MM/OTC hub `0x5ee84d30c7ee57f63f71c92247ff31f95e26916b` (the same hub that holds the MakerDAO RWA-007 bilateral above; it sits two hops downstream of [Zonda 1](../wallets/ethereum/zonda-1.md) via the unattributed relay `0x1990abd6e49218ab403f01aefeb9d22d07244181`) has three counterparty addresses that BlockSec MetaSleuth attributes to Wintermute on 2026-05-24. Combined lifetime bilateral magnitude: **~$994 million** across the three addresses.

| Field | Hot Wallet (inbound to MM/OTC hub) | Hot Wallet (inbound to MM/OTC hub) | Trading wallet (outbound from MM/OTC hub) |
|---|---|---|---|
| Counterparty address | `0xdbf5e9c5206d0db70a90108bf936da60221dc080` | `0xf8191d98ae98d2f7abdfb63a9b0b812b93c873aa` | `0xdbefb887662ca19cd485381f3386fe5f8537b910` |
| BlockSec `name_tag` | `Wintermute: Hot Wallet` | `Wintermute: Hot Wallet` | `Wintermute trading:b910(related_level_1)` |
| BlockSec `main_entity` | `Wintermute` | `Wintermute` | `Wintermute` |
| BlockSec category | `ASSET MANAGEMENT` (code 3001) | `ASSET MANAGEMENT` (code 3001) | `ASSET MANAGEMENT` (code 3001) |
| BlockSec attribute | `HOT WALLET` (code 4009) | `HOT WALLET` (code 4009) | (none) |
| Capture date | 2026-05-24, chain_id=1 | 2026-05-24, chain_id=1 | 2026-05-24, chain_id=1 |
| Receipt | [`../sources/blocksec/labels-2026-05-24.json`](../sources/blocksec/labels-2026-05-24.json) | [`../sources/blocksec/labels-2026-05-24.json`](../sources/blocksec/labels-2026-05-24.json) | [`../sources/blocksec/labels-2026-05-24.json`](../sources/blocksec/labels-2026-05-24.json) |
| Nearest inventory wallet | [Zonda 1](../wallets/ethereum/zonda-1.md) `0xf646cbe3…b95e` | [Zonda 1](../wallets/ethereum/zonda-1.md) `0xf646cbe3…b95e` | [Zonda 1](../wallets/ethereum/zonda-1.md) `0xf646cbe3…b95e` |
| Hops from inventory | Two (Zonda 1 → relay `0x1990abd6…244181` → MM/OTC hub `0x5ee84d30…6916b` → this Wintermute address) | Two (same path) | Two (same path) |
| Bilateral with MM/OTC hub | $590 million IN to the hub across 476 events (lifetime) | $206 million IN to the hub across 262 events (lifetime) | $198 million OUT from the hub across 42 events (lifetime) |
| Source receipt for bilateral magnitude | [`../sources/dune/d9-f005-institutional-10k-reprofile-2026-05-21.json`](../sources/dune/d9-f005-institutional-10k-reprofile-2026-05-21.json) | (same Dune receipt) | (same Dune receipt) |

**Plain-language reading.** Wintermute is a global institutional crypto market maker and OTC desk (Wintermute Trading, headquartered in London with offices in Amsterdam). BlockSec resolves three distinct Wintermute-controlled Ethereum addresses on direct bilateral paths with the MM/OTC hub two hops downstream of Zonda 1: two `Hot Wallet`-class addresses that send capital to the hub (~$796M combined lifetime) and one `trading` class address that receives capital from the hub (~$198M lifetime). The third address's BlockSec name tag includes the suffix `(related_level_1)`, which is BlockSec's marker for an address attributed by on-chain proximity to a labelled core Wintermute trading wallet (one degree of separation in BlockSec's clustering graph) rather than by direct labelling — still a Wintermute-controlled address for the purposes of this entity attribution, but the clustering-relationship origin is noted in the receipt. BlockSec assigns category `ASSET MANAGEMENT` (code 3001) to all three Wintermute addresses, which is BlockSec's taxonomy for the algorithmic-market-maker / OTC-desk class — the on-chain entity attribution is Wintermute regardless of how the category is named in BlockSec's internal classification.

The two-hop structural path is identical to the MakerDAO RWA-007 row above (Zonda 1 → relay → MM/OTC hub → external address). The on-chain graph establishes that the MM/OTC hub one degree downstream of Zonda's institutional-side relay has very large bilateral magnitudes with both MakerDAO's RWA-007 settlement address and Wintermute's hot + trading wallets. As with the MakerDAO row, the path does not establish that any specific Zonda customer dollar reached Wintermute — the relay and the hub are not themselves carrying a BlockSec primary attribution at the 2026-05-24 capture date and may serve other counterparties as well.

**Both the relay and the MM/OTC hub remain BlockSec-unattributed.** A direct probe of the relay address `0x1990abd6e49218ab403f01aefeb9d22d07244181` on 2026-05-24 returned no BlockSec `main_entity`. The MM/OTC hub address `0x5ee84d30c7ee57f63f71c92247ff31f95e26916b` was probed on 2026-05-13 and also returned no BlockSec `main_entity` (the hub remains BlockSec-unattributed at that capture date; receipt mirrored at [`../sources/blocksec/labels-2026-05-13.json`](../sources/blocksec/labels-2026-05-13.json)). Two readings are consistent with the on-chain pattern: (a) the relay and the hub are crypto-native MM/OTC routing wallets not yet indexed in BlockSec's institutional-entity database; (b) one or both is an internal routing wallet of some entity that doesn't merit a public label even when its counterparties (Wintermute, MakerDAO, Circle, FalconX, Coinbase Custody) are public. The on-chain primary citation surface terminates at these two unattributed intermediate addresses; the underlying entities are left to investigator handoff.

**Out of scope for this page.** Which specific Wintermute desk (institutional OTC, on-chain MM, principal trading book) corresponds to each of the three observed addresses, and what contractual or settlement arrangement underlies the ~$994M bilateral. Those are real-world-entity attribution questions that go beyond what the BlockSec primary attributions themselves state.

## Methodology cross-link

See [`../methodology.md`](../methodology.md) for the confidence-tier definitions and the receipts-mirroring policy. The BlockSec MetaSleuth API v3 endpoint and the response-field semantics (`main_entity`, `attributes`, `name_tag`) are documented there. Aggregations against `tokens_ethereum.transfers` follow the same Dune-aggregation policy used by the per-wallet flow profiles.
