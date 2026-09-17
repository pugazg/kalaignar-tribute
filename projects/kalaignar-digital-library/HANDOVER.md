# Kalaignar Digital Library / Reading Room — Master Handover

**Last updated:** 2026-09-17

---

## ⚠️ CURRENT STATE — read this before anything below

**The Phase 1–9 narrative in this document stops at Phase 7 (2026-08-21) and is now HISTORICAL.**
Several phases have shipped since it was written, and its work counts, shelf counts and
"last production application-code checkpoint" are stale. It is kept as history and has **not** been
retro-edited. Where it disagrees with this section or with live GitHub, **live GitHub wins**.

### Verified live state — 2026-09-17, Wave-6 Batch 7 P2–P4 MERGED (PR #87) + P5 PRODUCTION ACCEPTANCE PASS — WAVE 6 COMPLETE / CLOSED / FROZEN at P5 ✅ CURRENT

**This checkpoint has highest precedence over every lower `CURRENT`/`SUPERSEDED` label retained as history. Live GitHub and production win. This is a CONTROL-ONLY close-out — P5 made no implementation, payload, route, catalogue, discovery, sitemap, or source change (implementation delta = 0, source delta = 0).**

Wave 5 remains **COMPLETE / CLOSED**. Wave 6 P0 remains **COMPLETE / FROZEN**. **Batch 7 is now fully implemented and published:** Batch-7 **P1 merged (PR #86)**, and **P2–P4 merged (PR #87)** — the 116 canonical short stories are published as independent Fiction works and grouped into 5 new public collections. **Wave-6 P5 production acceptance = PASS, and Wave 6 is now COMPLETE / CLOSED / FROZEN at P5.**

The old projection "onboarding all 116 later would give catalogue 216 / Fiction 157" (2026-09-16 checkpoint) is now **realized live state**, not a projection.

#### Merged + accepted implementation boundary (authoritative)

| Item | Durable state |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| Implementation `main` (P2–P4 squash merge of PR #87) | `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e` |
| Implementation `main` tree | `06c7ae8646ba85e61c973fecb5945ffbec256c39` |
| PR #87 | MERGED / CLOSED, `mergedAt` `2026-09-17T01:28:47Z`; approved head `b34e05dcc27ba809e8f7c3743d2f4570614457eb`; approved head tree == merged main tree (`06c7ae86…`) PASS; single squash parent `171d7b37…` |
| PR #86 (Batch-7 P1) | MERGED / CLOSED |
| Batch-7 source (frozen, unchanged) | `pugazg/kalaignar-short-stories` `main` `7205a10892d0b208df2617766844f480b6a2c798`, tree `1be34cc368fbc96ff72933a004a074ef840168ee` |
| Wave-6 implemented works | **138** = 22 (Batches 1–6) + 116 (Batch 7) |
| Catalogue | **216** works (Fiction **157**) |
| Public collections | **6** (1977 + 2008/40, 2004/34, 1987/25, 1982/6, 2009/16) |
| `STORY_SLUGS` | **154** unique |
| `/read` discovery | **77** entries / **40** visible (Fiction discovery **18**, over-cap) |
| Sitemap | **3909** URLs / **0** dup |
| Build | **3918** prerender / **3913** `.html` |
| Wave-6 route delta | **558** = 321 (Batches 1–6) + 232 (Batch-7 stories) + 5 (Batch-7 collections); `3360+558=3918`, `3355+558=3913`, `3351+558=3909` |

- **Plural membership is live production data:** `jaadi-kutti-poduma` (one work; 2008 + 1987, 1987 ordinal 2) and `kuruvi-rameswaram` (one work; 2004 + 1987, 1987 ordinal 11); the eleven 1977 canonicals reprinted in 2009 are members of 1977 + 2009 while remaining single works textually controlled by their 1977 payload (the 2009 collection-local page/scan extents do not overwrite 1977 provenance). Plural membership inflated neither catalogue works (216) nor discovery entries (77).
- **Eight Batch-7 works are non-collection standalone Fiction** discovery entries: `seerazhitha-sirippu`, `madurai-selavu`, `kondru-varuga`, `naattiya-kalarani`, `maanam`, `neruppu`, `vilaiyal-vangalaiyo`, `nanbana`.
- **P2 corrections durable:** the nine corrected stories render apparatus-clean; `madurai-selavu` Tamil excludes the scan-25 `intervening-non-story` interleaf with its English scan-25 continuation preserved; `நந்தியூர் நரியப்பன்` / `நரியூர் நந்தியப்பன்` remain distinct; `தேனலைகள்` and `நடுத்தெரு நாராயணி` remain excluded.
- **P5 production acceptance (2026-09-17) against `https://nenjukkuneethi.org`:** 558/558 Wave-6 routes HTTP 200; representative invalid routes 404 (fail-closed); `/read`, all 6 collection pages, plural membership, apparatus/interleaf and semantic-restraint checks accepted; sitemap 3909/0 with Batch-7 set 237/237 present; full merged-main regression green; exact-head CI `35170239750` SUCCESS; Vercel + Preview Comments SUCCESS. Full evidence: [`WAVE6_P5_PRODUCTION_ACCEPTANCE.md`](./WAVE6_P5_PRODUCTION_ACCEPTANCE.md).
- **Wave-6 lifecycle & final closure (owner-approved 2026-09-17):** the established programme lifecycle is **P0 (census/selection) → P1 (hidden data foundation) → P2 (fidelity/reader validation) → P3 (direct routes while hidden) → P4 (publication: catalogue/discovery/sitemap/collections) → P5 (independent production acceptance + durable control close-out)**. **Wave 6 is COMPLETE / CLOSED / FROZEN at P5.** **There is no Wave-6 P6** — no historical programme definition of P6 exists (Wave 5 likewise ran P0–P5 and closed at P5), and the read-only P6 definition audit determined none is required. P0–P5 are frozen historical stages; the accepted implementation boundary above is immutable. The earlier `P6 NOT STARTED / NOT AUTHORIZED` wording was a guard against inventing work before the lifecycle was reviewed — that review is complete and P6 is **not part of the Wave-6 lifecycle** (any historical `P6 NOT STARTED / NOT AUTHORIZED` text retained in the SUPERSEDED checkpoints below is thereby historical). Any subsequent onboarding or programme expansion requires **separately authorized new-wave scope**; maintenance of already-published works requires an **explicitly authorized maintenance/repair activity** — never P6, and never an automatic Wave 7 or fresh census.

### Verified live state — 2026-09-16, Wave-6 short-story census refreshed → combined Batch 7 (116 works) ⚠️ SUPERSEDED as current state (kept as history)

**Superseded by the 2026-09-17 P5 checkpoint above: Batch 7 has since been implemented and published (PR #86 P1, PR #87 P2–P4) and production-accepted, so this checkpoint's "Batch-7 P1 has NOT started" / "catalogue 100 / collections 1" / "216 & 157 are projections" statements are now historical. Retained as the census-refresh evidence. Live GitHub wins.** This was a CONTROL-ONLY census refresh — no implementation, payload, route, catalogue, discovery, sitemap, or source change was made by it.

Wave 5 remains **COMPLETE / CLOSED**. Wave 6 P0 remains **COMPLETE / FROZEN**. Implementation remains closed through **Batches 1–6 (Wave-6 P1–P3 through Batch 6 + P4 for Batches 1–6, MERGED / CLOSED)** — unchanged: implementation `main` `2ca4d19830755864acec153f99f2659f413802cb`, tree `837c92893ab248f6185a36dc3b13f353495f5c9d`; catalogue **100**, collections **1**, `/read` **64 / 39 visible**, sitemap **3672 / 0 dup**, build **3681 / 3676**; post-merge tree equality PASS (see the 2026-09-15 checkpoint below).

The short-story programme was **re-verified from live `pugazg/kalaignar-short-stories`** (`main` `7205a10892d0b208df2617766844f480b6a2c798`, tree `1be34cc368fbc96ff72933a004a074ef840168ee`). The old census figure of **103** short stories is superseded: all currently completed canonical short stories are consolidated into **one combined future Batch 7 = 116 canonical works**. Internal source/provenance groups are **validation partitions only** (the old B7–B11 split is superseded — Batch 7 is a single implementation batch).

- **Batch 7 = 116 canonical short stories.** Deterministic enumeration, source pins, witness/cross-repository exclusions and the collection-model audit are in [`WAVE6_BATCH7_SHORT_STORIES.md`](./WAVE6_BATCH7_SHORT_STORIES.md); the master census carries the refresh banner.
- Derivation: `2008 40 + 2004 34 + 1987 23 + 2009 5 + 1982 6 + periodical 3 + 1976 2 + 1969 1 + 1953-thappivittargal 1 + 1997 1 = 116` (and `154 stories/ dirs − 37 1977-anthology members − 1 kizhavan-kanavu = 116`). **+13 since the old 103** = 1982 (6), 1976 (2), periodical (3), 1969 (1), 1953 `தப்பிவிட்டார்கள்` (1). **1982 is a 6-story anthology, not 5** (`நந்தியூர் நரியப்பன்` and `நரியூர் நந்தியப்பன்` are separate canonical stories).
- **Refreshed Wave-6 completed/READY population = 138** = 22 already-implemented non-short-story Wave-6 works + 116 Batch-7 short stories (old total was 125 = 22 + 103).
- **Intentional exclusions (not short-story backlog):** `தேனலைகள்` (1958) — already represented in the essays / கட்டுரைகள் workstream under `மீசை முளைத்த வயதில்` (cross-repository overlap; its 12 mapped headings are NOT Batch-7 candidates; do not silently reopen); `நடுத்தெரு நாராயணி` — intentionally excluded, handled via the separate `அரும்பு` / short-novel source path.
- Witness-only source entries (1950, 1953-naadum, 1956, 1979, and the per-collection witnesses of 1976/1997/1969/1953/1987/2009/periodical) do **not** become duplicate LibraryWorks.
- **Projections (future state only — nothing implemented):** onboarding all 116 later would give catalogue `100 + 116 = 216`, Fiction shelf `41 + 116 = 157`.
- **Batch-7 P1 has NOT started. Wave-6 P5 / P6 have NOT started.** No implementation/public/source/control-programme change; await explicit owner authorization.

### Verified live state — 2026-09-15, Wave-6 Batch-6 P1–P3 + P4 Batches 1–6 MERGED / CLOSED ⚠️ SUPERSEDED (kept as history)

**Superseded by the 2026-09-16 census-refresh checkpoint above (which changed control docs only; this checkpoint's implementation boundary remains current). Live GitHub wins.**

Wave 5 remains **COMPLETE / CLOSED**. Wave 6 P0 remains **COMPLETE / FROZEN**. Since the Batch-5 checkpoint below, **Wave-6 Batch 6 (Essays & Articles) P1–P3 merged (PR #84)** and **Wave-6 P4 for the completed Batches 1–6 merged (PR #85)**. **Wave-6 P5 is NOT authorized. Wave-6 P6 is NOT authorized. Batch 7 has NOT started.** No new source ingestion is authorized. Live GitHub is authoritative.

#### Merged implementation boundary (authoritative)

| Item | Durable merged state |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| Implementation `main` (post-P4 squash merge) | `2ca4d19830755864acec153f99f2659f413802cb` |
| Implementation `main` tree | `837c92893ab248f6185a36dc3b13f353495f5c9d` |
| READY works merged through P3 | **22 / 125** |
| Cumulative Wave-6 direct routes | **321** |
| Prerender routes | **3681** = frozen 3360 baseline + 321 |
| Prerendered `.html` | **3676** = frozen 3355 baseline + 321 |

Wave-6 batch progress on merged `main` (P1–P3 direct-reader routes):

| Batch | Family | Works | State | Route delta | Cumulative |
|---:|---|---:|---|---:|---:|
| 1 | Cinema / `ammaiyappan` | 1 | MERGED | +65 | 65 |
| 2 | Drama / `kagithapoo`, `manimagudam`, `thiruvalar-desiyampillai` | 3 | MERGED | +83 | 148 |
| 3 | Speeches / `namathu-nilai`, `idhaya-perikai`, `palli-vazhkkai` | 3 | MERGED | +6 | 154 |
| 4 | Poetry / 8 READY works | 8 | MERGED | +30 | 184 |
| 5 | Novels / `periya-idathup-pen`, `pudhaiyal` | 2 | MERGED | +63 | 247 |
| 6 | Essays & Articles / 5 READY works | 5 | **MERGED / CLOSED** | +74 | **321** |

#### Wave-6 Batch 6 — Essays & Articles P1–P3 MERGED / CLOSED (PR #84)

Implementation PR **#84** merged Batch 6. Merge commit / prior implementation `main`:
`d6621b71256ae99b1c89b4f2091513dcc5f96626`; merged tree `55823ff9742969e6868741312740aec06ebfd4ff`.

| Work | Literary articles |
|---|---:|
| `ina-muzhakkam` | 6 |
| `kolaikkalam` | 6 |
| `kudumbaththin-nalvilakku` | 1 |
| `sinthanaiyum-seyalum` | 50 |
| `vedhanai-ch-siraiyinindrum-viduthalai-pera` | 1 (government message / `செய்தி`) |

Batch-6 totals: **5 works · 64 literary articles · 74 direct routes**; cumulative Wave-6 P3 **247 → 321**.

Batch-6 source boundary (durable):
- source repo: `pugazg/kalaignar-essays`;
- frozen source anchor: commit `564add708b8bd942fa9d5f505b083955248873d0`, tree `14a4a6cd81dbd13145f289734812583cac9b1403`;
- target subtree pins:
  - `ina-muzhakkam` `4e6a28cb93a1eb2b8f376a1abebc938a1d7f8ef9`
  - `kolaikkalam` `e1eff4df14bd56e37575f15651e400f87b332ff0`
  - `kudumbaththin-nalvilakku` `1d1001992ff376056da5cba8d54f7dd79901566b`
  - `sinthanaiyum-seyalum` `488cd61fa8df5aafa5a9a505001ce417b2892e90`
  - `vedhanai-ch-siraiyinindrum-viduthalai-pera` `f3c43511240df098b175b9d39cdcc6f4318f2230`

Batch-6 durable semantic restraints:
- `kudumbaththin-nalvilakku`: no established edition; no invented publication year; `controllingIsFirstEdition: null`; `editionStatus: "not-established"`; printed-page evidence remains **2–9** (do not invent printed pages 1 or 10).
- `vedhanai-ch-siraiyinindrum-viduthalai-pera`: a government `செய்தி` / message, **NOT a speech**; no fabricated date or venue; no established edition; `controllingIsFirstEdition: null`; `editionStatus: "not-established"`.
- `sinthanaiyum-seyalum`: exactly **50 articles**; 2010 third edition; five transfer PDFs.

#### Wave-6 P4 for Batches 1–6 — MERGED / CLOSED (PR #85)

Implementation PR **#85**, `Wave 6 P4 — Publish completed Batches 1–6 to catalogue, discovery and sitemap`, is **MERGED / CLOSED**:
- reviewed/final head: `c65070845e75337ea65989bc83f792739983f795`;
- approved head tree: `837c92893ab248f6185a36dc3b13f353495f5c9d`;
- squash merge commit / current implementation `main`: `2ca4d19830755864acec153f99f2659f413802cb`;
- merged `main` tree: `837c92893ab248f6185a36dc3b13f353495f5c9d`.

**Critical post-merge integrity result: `post-merge main tree == approved PR-head tree` — PASS.** This exact tree equality is the durable Wave-6 P4 close evidence.

Exact-head Library CI before merge — run `34964450981`: `typecheck • build` SUCCESS · `archival validators` SUCCESS · Vercel SUCCESS.

P4 covered **Batches 1–6 only (22 works)** and created **ZERO new reader routes** — it exposed exactly the existing cumulative **321** P3 direct routes.

Public inventory after P4 (this supersedes the Batch-5 boundary of catalogue 78 / sitemap 3351 / 247 routes below):

| Surface | Before (P3) | After (P4) |
|---|---:|---:|
| Catalogue works | 78 | **100** |
| Public collections | 1 | **1** |
| `/read` discovery entries | 42 | **64** |
| Initially visible (cap 6) | 34 | **39** |
| Sitemap URLs | 3351 | **3672** |
| Sitemap duplicates | 0 | **0** |
| Prerender routes | 3681 | **3681** |
| Prerendered `.html` | 3676 | **3676** |

Exact catalogue shelf census (9 non-empty shelves, total **100**): Life Writing 1 · Letters 1 · **Fiction 41** · **Poetry 14** · **Drama 8** · **Cinema Writing 7** · **Speeches 17** · **Essays & Articles 9** · Literary Commentary 2.

Per-shelf `/read` discovery (total **64**): Life Writing 1 · Letters 1 · **Fiction 5** · **Poetry 14** · **Drama 8** · **Cinema Writing 7** · **Speeches 17** · **Essays & Articles 9** · Literary Commentary 2. Over-cap shelves (each rendering one disclosure): Poetry, Drama, Cinema Writing, Speeches, Essays & Articles. **Fiction discovery remains 5 despite 41 Fiction works** because the existing 1977 short-story anthology collection collapses its 37 members into one discovery entry.

Sitemap: the exposed Wave-6 route set is exactly set-equal to `data/internal/wave6/p3-routes.json.cumulativeRoutes` (**missing 0 · extra 0 · duplicate 0**); the Wave-6 sitemap delta is **321**.

Build boundary derivation: frozen baseline 3360 / 3355 + Wave-6 existing P3 routes 321 = **3681 / 3676**. P4 created no routes.

Durable P4 record: implementation contains `data/internal/wave6/p4-integration.json`. The historical P3 manifest `data/internal/wave6/p3-routes.json` was intentionally **not rewritten** — its `discoverable=false` / `sitemapExposed=false` values are retained as **P3-phase historical evidence**, not current P4 public state.

#### P4 semantic restraint (independently corrected before merge)

P4 passed an independent semantic correction before merge. `oruthalaik-kathal` remains one **verse-novel / poetry publication** of **11 source sections — NOT 11 independent poems**. Final public metadata is **data-driven from `readingUnitKind` / `workForm`**: the landing says **11 source sections**, the child route says **section N of 11**, and normal poetry publications retain poem/poems wording. **Do not regress this into "11 poems."**

Other durable P4 restraints:
- Ammaiyappan archival segments are not claimed as source-numbered scenes.
- Kagithapoo has no invented Scenes 22/23.
- Thiruvalar has no invented numbered scene/act system and retains its source-condition qualification.
- Namathu Nilai has no fabricated single date.
- Idhaya Perikai / Palli Vazhkkai have no invented date or venue.
- 1975 Kaviyaranga publication keeps item ordinals 01 / 02 / 04; excluded ordinal 03 remains absent.
- Periya Idathup Pen = **7 archive reading sections**, never 18.
- Pudhaiyal = **52 literary units / 54 total direct routes**, never "54 literary sections."
- Kudumbaththin has no invented edition/year.
- Vedhanai remains a government message, not a speech.

**Next action:** none authorized by this checkpoint. Wave-6 Batch-6 P1–P3 and Wave-6 P4 for Batches 1–6 are MERGED / CLOSED. **P5 is NOT authorized. P6 is NOT authorized. Batch 7 has NOT started. No new source ingestion is authorized.** A fresh chat must first fetch live GitHub state (authoritative) and await explicit owner direction before any next execution activity. Do not imply P5 automatically follows P4.

### Verified live state — 2026-09-10, Wave-6 Batch-5 Novels MERGED / CLOSED ⚠️ SUPERSEDED (kept as history)

**Superseded by the 2026-09-15 checkpoint above; retained as history. Live GitHub wins.**

Wave 5 remains **COMPLETE / CLOSED**. Wave 6 P0 remains **COMPLETE / FROZEN**. The owner authorized
**Wave-6 P1 → P2 → P3 for all 125 READY works** using the established **11 deterministic batches**.
**Wave-6 P4 remains NOT AUTHORIZED.** **Batch 6 has NOT started.**

### Merged implementation boundary through Batch 5

| Item | Durable merged state |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| Implementation `main` (Batch-5 merge commit) | `bb0beaa0a18f97336b52319c1e7b15e62d81d1ed` |
| Implementation `main` tree | `2fdc92b40d66c60caf4042b327babed97e53ae94` |
| READY works merged through P3 | **17 / 125** |
| Cumulative Wave-6 direct routes | **247** |
| Prerender routes | **3607** = frozen 3360 baseline + 247 |
| Prerendered `.html` | **3602** = frozen 3355 baseline + 247 |

Wave-6 batch progress on merged `main`:

| Batch | Family | Works | State | Route delta | Cumulative |
|---:|---|---:|---|---:|---:|
| 1 | Cinema / `ammaiyappan` | 1 | MERGED | +65 | 65 |
| 2 | Drama / `kagithapoo`, `manimagudam`, `thiruvalar-desiyampillai` | 3 | MERGED | +83 | 148 |
| 3 | Speeches / `namathu-nilai`, `idhaya-perikai`, `palli-vazhkkai` | 3 | MERGED | +6 | 154 |
| 4 | Poetry / 8 READY works | 8 | MERGED | +30 | 184 |
| 5 | Novels / `periya-idathup-pen`, `pudhaiyal` | 2 | **MERGED / CLOSED** | +63 | **247** |

The public P4 boundary is unchanged: **catalogue 78 · public collections 1 · sitemap 3351 / 0
duplicates · Poetry discovery 6 · Fiction discovery 3 · `/read` does not expose the Wave-6 P1–P3
works.** Batch-5 catalogue / discovery / sitemap exposure is **0**. Do not infer public exposure from
direct-reader route availability.

### Batch 5 — PR #83 MERGED (source drift adjudicated, corrected, independently reviewed, merged)

Implementation PR **#83**, `Wave 6 P1–P3 — Novels batch: Periya Idathup Pen and Pudhaiyal`, is
**MERGED / CLOSED**. The Batch-5 Periya source-freeze drift was **independently adjudicated as
literary-harmless but provenance-material**: the Periya subtree moved only because
`works/periya-idathup-pen/metadata/source.md` was updated and
`works/periya-idathup-pen/metadata/witness-arumbu-1978.md` was added (an additional, **non-controlling**
1978 `அரும்பு` witness); the assembled reading layer stayed byte-identical. A **revised source anchor**
was established, a narrow provenance-only correction was made on the **same PR #83** (the two
`novel.json` literary payloads stayed byte-identical; only `provenance.json` changed), the corrected
exact head passed a **fresh immutable-head independent review**, and it was merged and independently
post-merge verified:

- base: `5c6b5ef8901044660e607d4649238d7c66cb648d`;
- approved PR head: `5226f10e265bff981692b9b70f834230de94a200`;
- approved PR-head tree: `2fdc92b40d66c60caf4042b327babed97e53ae94`;
- merge commit / current implementation `main`: `bb0beaa0a18f97336b52319c1e7b15e62d81d1ed`;
- post-merge implementation `main` tree: `2fdc92b40d66c60caf4042b327babed97e53ae94`.

**Critical post-merge integrity result: `post-merge main tree == approved PR-head tree` — PASS.** This
exact tree equality is the durable Batch-5 close evidence.

Durable literary / routing model (do **not** revive the disproved Periya 18-section assumption):

- `periya-idathup-pen` — one continuous work; **7** canonical archive reading sections; landing +
  `/source` + 7 literary sections = **9 direct routes**.
- `pudhaiyal` — exactly **52 literary `[section]` units**: `00-arimugam` / `00-introduction` plus
  Chapters 01–51. `front-matter.md`, `99-printer-colophon.md`, `sections/checkpoints/**`, and English
  release/audit/workflow files are provenance/paratext, **not** literary `[section]` routes. Landing +
  `/source` + 52 sections = **54 direct routes**.
- Batch-5 arithmetic = **9 + 54 = 63 direct routes**; cumulative Wave-6 routes = **184 → 247** (merged).

### Batch-5 source boundary — durable

- source repo: `pugazg/kalaignar-novels`;
- reviewed/adjudicated active provenance anchor: commit `d6679e46051ab93de8da6361413c39e7db468cfe`,
  tree `e4ea40ffd495fe084221541f9ca5fd48742dee3e`;
- target subtree pins: `works/periya-idathup-pen` `47168b63142012ade56ec832e8977c494d0027a6`,
  `works/pudhaiyal` `450d7da31a0f2eed5c12d43e4082edb758134618`;
- literary snapshot/freeze retained inside the byte-stable `novel.json` payloads:
  `a99f135467dd38e294faff31088a937994790a47`.

At this control-sync check, novels live `main` was `14167ec9e23f7c8e93eb899746196461dcc303d2` / tree
`700c78475da4e081290d49bd22b7e259e3f4ffd0`, and **both target subtrees still equal the reviewed pins
above**. Live novels `main` may advance for unrelated works; that volatile SHA/tree is context only —
the immutable Batch-5 provenance anchor remains `d6679e46…`. Do not treat unrelated source-main
movement as Batch-5 drift while the two target subtree pins remain equal.

**Next action:** none authorized by this checkpoint. Batch 5 P1–P3 is MERGED / CLOSED. A fresh chat must
first fetch live state and await explicit owner direction for the next execution activity. **Do not
start Batch 6. Do not start or authorize Wave-6 P4.**

### Verified live state — 2026-09-08, post-Wave-6-P0 (P0 census COMPLETE; P1 NOT AUTHORIZED — implementation/production boundary unchanged from Wave-5-P5) ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `632476baa40ebbe94083ec41a6c8f4a26dfec77c` |
| Implementation `main` tree | `6a4b2cd6bdcdada399cdb27247e485527813a7b2` |
| Open PRs (implementation) | 0 |
| Published **works** | **78** |
| **Cinema Writing works** (public) | **6** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **42** |
| **Initially visible discovery entries** | **34** |
| **Prerender-manifest routes** | **3360** |
| Prerendered `.html` files | 3355 |
| **Sitemap URLs** | **3351** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** ·
Drama 5 · **Cinema Writing 6** · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **78**.

**Bulk Onboarding Wave 5 — Cinema Writing (Manthiri Kumari + Raja Rani) is COMPLETE and CLOSED.** The
implementation boundary is unchanged from the P4 close — `632476baa40ebbe94083ec41a6c8f4a26dfec77c`
(tree `6a4b2cd6bdcdada399cdb27247e485527813a7b2`), the exact P4 approved tree — because **Wave 5 P5 is
production acceptance + durable control closure and produced NO implementation delta.** P5 independently
re-verified the final production boundary and every P1–P4 guarantee, found no regression, and closed the
wave. Every public inventory/route metric above is identical to the P3/P4 boundary. P5 production
acceptance (measured on `https://nenjukkuneethi.org`): `/read` shows the six Cinema cards in onboarding
order (Manohara · Parasakthi · Tirumbippaar · Kalaignar Film Songs · Manthiri Kumari · Raja Rani), Cinema
is exactly at the six-entry cap with **no** disclosure control and Speeches remains the **sole** over-cap
shelf; all representative Manthiri/Raja routes return **200** and invalid children (`performance-16/99`,
`scene-000/059`, `song-12`) **404**; the production sitemap holds **3351** URLs / **0** duplicates with
**346** Cinema URLs and the exact per-family split **59/48/95/55/18/71** (Wave-5 **89 = 18 + 71**); Manthiri
keeps its source-backed story/dialogue credit and is not a screenplay; Raja stays neutral (no role credit,
archive segments not numbered scenes, 6 songs unresolved, segment-58↔song-11 review-level, deleted T055
ids and the PDF-74 ownership stamp absent). From current `main`: P4 integrity **475/0**, P4 UI **33/0**,
P2 **443/0**, P3 **66/0**, collections **258/0**, poetry-architecture **118/0**, shelf-disclosure **60/0**,
Manthiri P1 **90/0**, Raja P1 **75/0**, `npm run validate` exit 0, typecheck clean, clean production build
(prerender **3360** / `.html` **3355**), `git diff --check` clean. Source freeze `75b22046…` and the four
P1 payload hashes are unchanged. **Wave 5 must not be reopened from stale prompts; P0–P5 are frozen
historical stages unless a newly discovered source-backed regression requires repair.** See the Wave-5
section below.

### Wave 6 — P0 completed-works census ✅ COMPLETE — HISTORICAL / SUPERSEDED (assessment-only checkpoint)

Owner-authorized **Wave 6 P0 only** — a read-only global census of completed archival works and their
Digital-Library readiness. **No onboarding is authorized; no implementation/source/route/catalogue/
sitemap/production change was made.** Full findings: `projects/kalaignar-digital-library/WAVE6_COMPLETED_WORKS_CENSUS.md`.

Result (counts derived from unique canonical work identities): **125 READY works** not yet onboarded —
1 Cinema (`ammaiyappan`, Reading Room payload QA PASS); 3 Drama (`kagithapoo`, `manimagudam`,
`thiruvalar-desiyampillai` with documented physical-loss qualification); 8 Poetry (release-cleared);
2 Novels (`periya-idathup-pen`, `pudhaiyal`); 5 Essays (frozen Publications 1–9, English release
verified); 3 Speeches (`namathu-nilai`, `idhaya-perikai`, `palli-vazhkkai`); and **103 unique short-story
works** across the 2008 (40), 2004 (34), 1987 (**23 distinct**, +2 witness relations), 2009 (5 new) and
1997 (`நண்பனா?`, 1) sources. **HOLD:** stage-play `ore-mutham` (`SOURCE_VERIFICATION` — ~21% terminal
documented physical-source loss, owner decision) and the `chinna-chinna-malargal` quote collection
(`PUBLICATION_MODEL` — no Quotes shelf/reader model yet). **NOT COMPLETE (12 candidate works):** naam, vellikkizhamai,
meesai-mulaiththa-vayathil, நடுத்தெரு நாராயணி (counted once), sangatamil, kuraloviyam, iratha-kanneer,
and the **five separate 1982 முடியாத தொடர்கதை stories** (the anthology is a source container, not one
work). Total not-yet-onboarded candidate works = 125 READY + 2 HOLD + 12 NOT COMPLETE = **139**. Onboarding all READY would take the catalogue **78 → 203 works** (Fiction 39 → 144),
collections **1 → 5** (`நண்பனா?` standalone; 1997 is not a public collection). Feasibility recommendation:
**B — one Wave-6 governance programme implemented as deterministic per-shelf/family batches** (the
103-story fiction partition and its duplicate-identity clearance are the main risk). **Wave 6 P1 is NOT
authorized and has NOT started** — P0 is assessment only.

### Verified live state — 2026-09-04, post-Wave-5-P3 (cinema catalogue/discovery/sitemap exposure) ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `c6ac8b6cde867c865c5358e252828fbf0b4f8524` |
| Implementation `main` tree | `270d66492ec70fbd7c24a9e05f044a454b533b9a` |
| Open PRs (implementation) | 0 |
| Published **works** | **78** |
| **Cinema Writing works** (public) | **6** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **42** |
| **Initially visible discovery entries** | **34** |
| **Prerender-manifest routes** | **3360** |
| Prerendered `.html` files | 3355 |
| **Sitemap URLs** | **3351** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** ·
Drama 5 · **Cinema Writing 6** · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **78**.

Implementation `main` advanced from the Wave-5 P2 close `cf6a952c…` to
`c6ac8b6cde867c865c5358e252828fbf0b4f8524` (tree `270d66492ec70fbd7c24a9e05f044a454b533b9a`) by
**Wave 5 P3** — implementation PR #77, which turned the two already-live P2 cinema readers into normal
Reading Room **catalogue / discovery / sitemap** members. Two new `LibraryWork` records land on the
Cinema Writing shelf in onboarding order (Manohara · Parasakthi · Tirumbippaar · Kalaignar Film Songs ·
Manthiri Kumari · Raja Rani), taking works **76 → 78**, Cinema Writing **4 → 6**, discovery **40 → 42**,
initially-visible **32 → 34**, and the sitemap **3262 → 3351** (**+89**: Manthiri **18** + Raja **71**,
enumerated from the frozen reader registries via `lib/cinema-wave5-routes.ts`, **0** duplicates). **P3
added NO page route** — the +89 routes were already live from P2 — so the prerender-manifest (**3360**)
and `.html` (**3355**) counts are unchanged from P2. Cinema Writing now sits exactly at the six-entry
disclosure cap, so all six cards are initially visible with **no** disclosure control; **Speeches (14
discovery entries) remains the sole over-cap shelf**, and Fiction still renders 3 discovery entries
despite 39 works. The independently approved PR-head tree and the squash-merged `main` tree are the
**same tree SHA** `270d66492ec70fbd7c24a9e05f044a454b533b9a` — no drift. Production-verified: `/read`
shows all six Cinema cards in order, both new works link correctly, all representative Manthiri/Raja
routes (landing, story-summary, performance-11/13, scene-001/058, song-11, `/source`) return **200**,
invalid children (`performance-16/99`, `scene-059/000`, `song-12`) **404**, and the production sitemap
holds exactly **3351** URLs / **0** duplicates with the exact **18 + 71 = 89** Wave-5 set (no missing, no
extra). Semantic restraint held: Manthiri keeps its source-backed story/dialogue credit
(`கதை, வசனம் : மு. கருணாநிதி`); Raja's catalogue card is **neutral** (`வசன நூல்: …` / "Dialogue
screenplay publication: …") with no role-specific credit. Measured at the current production boundary
from a build of `c6ac8b6c…`. **Wave 5 is NOT closed** — P0/P1/P2/P3 are complete; **P4
(regression/integrity hardening) is the planned next stage, is NOT authorized, and has NOT started.**
See the Wave-5 section below. **This checkpoint is superseded by the post-Wave-5-P4 checkpoint above**
(P4 added the test/CI cross-work integrity hardening at merge `632476ba…`, tree unchanged in effect —
the public inventory/route metrics are identical) and is retained only as history.

### Verified live state — 2026-09-04, post-Wave-5-P2 (cinema public readers; catalogue still deferred) ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `cf6a952ca9f0edea254d9c72b48ef333523bfd51` |
| Implementation `main` tree | `9bf711784a86458f95a333c6f4c1768cbe65f690` |
| Open PRs (implementation) | 0 |
| Published **works** | **76** |
| **Cinema Writing works** (public) | **4** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **40** |
| **Initially visible discovery entries** | **32** |
| **Prerender-manifest routes** | **3360** |
| Prerendered `.html` files | 3355 |
| **Sitemap URLs** | **3262** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** ·
Drama 5 · **Cinema Writing 4** · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **76**.

Implementation `main` advanced from the Wave-5 P1 close `7cc0546f…` to
`cf6a952ca9f0edea254d9c72b48ef333523bfd51` (tree `9bf711784a86458f95a333c6f4c1768cbe65f690`) by
**Wave 5 P2** — implementation PR #76, the Manthiri Kumari + Raja Rani **public readers, direct routes
and `/source` pages**. **P2 makes the two works directly readable but keeps them OUT of the Reading Room
catalogue until P3:** neither is in `data/library.ts`, neither is in `/read` discovery, and neither is
in the sitemap. So the catalogue/discovery/sitemap metrics are unchanged from the Wave-4 baseline
(works **76** · Cinema Writing **4** · Poetry 6 · collections 1 · shelves 9 · discovery **40** · visible
**32** · sitemap **3262** / 0 dup · `/poems/` 147). The only metric that moved is the build route count:
prerender-manifest **3271 → 3360** and `.html` **3266 → 3355**, a delta of exactly **+89** — the intended
P2 direct-route set (Manthiri **18** = landing + story-summary + 15 performances + source; Raja Rani
**71** = landing + 58 archival scene segments + 11 numbered songs + source). Production-verified: all
representative direct routes return **200**, invalid children (`performance-16/99`, `scene-059/000`,
`song-12`) **404** (fail-closed), and `/read` still does not discover either work. Measured at the
current production boundary from a build of `cf6a952c…`. **Wave 5 is NOT closed** — P0/P1/P2 are
complete, P3–P5 remain; the public catalogue stays 76 works / Cinema Writing 4 until P3. See the Wave-5
section below. **This checkpoint is superseded by the post-Wave-5-P3 checkpoint above** (P3 added the two
works to the catalogue/discovery/sitemap, works 76 → 78 · Cinema Writing 4 → 6 · sitemap 3262 → 3351)
and is retained only as history.

### Verified live state — 2026-09-04, post-Wave-5-P1 (cinema data foundation, hidden) ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `7cc0546fc311aabae2a67ef3d7f8c5fd2390b7d5` |
| Implementation `main` tree | `41fb1a5431195d6796e7d8bd4181ffa883bb29b0` |
| Open PRs (implementation) | 0 |
| Published **works** | **76** |
| **Cinema Writing works** (public) | **4** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **40** |
| **Initially visible discovery entries** | **32** |
| **Prerender-manifest routes** | **3271** |
| Prerendered `.html` files | 3266 |
| **Sitemap URLs** | **3262** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

**This checkpoint is superseded by the post-Wave-5-P2 checkpoint above** (P2 added the +89 public direct
routes while catalogue/discovery/sitemap stayed unchanged) and is retained only as history.

Implementation `main` advanced from the post-Wave-4-repair close `946dc8a5…` to
`7cc0546fc311aabae2a67ef3d7f8c5fd2390b7d5` (tree `41fb1a54…`) by **Wave 5 P1** — implementation PR #75,
the Manthiri Kumari + Raja Rani cinema **source freeze and deterministic data foundation**. **P1 is a
HIDDEN data foundation: it adds NO public route, no catalogue entry, no `/source` page and no sitemap
URL.** Every public inventory and route metric is therefore unchanged from the Wave-4 baseline (works
**76** · Cinema Writing **4** · Poetry 6 · collections 1 · shelves 9 · discovery 40 · visible 32 ·
prerender-manifest **3271** · `.html` **3266** · sitemap **3262** / 0 dup · `/poems/` 147); the merge
added only generated data under `public/data/cinema/{manthiri-kumari,raja-rani}/`, two importers, two
validators, two type modules, and CI/validate wiring. Neither work is in `data/library.ts`; production
`/cinema/manthiri-kumari` and `/cinema/raja-rani` return **404** (correctly not exposed). Measured at the
current production boundary: implementation `main`/tree and open PRs from live GitHub; the census and
route metrics from a production build of `7cc0546f…` (zero delta vs the previous checkpoint). **Wave 5 is
NOT closed** — only P0 and P1 are complete; the public site stays 76 works / Cinema Writing 4 until P3.
See the Wave-5 section below.

### Verified live state — 2026-09-04, post-Poetry-landing-copy-regression-repair ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `946dc8a510ef5f836eab2af15d3b2d69ee9360c2` |
| Implementation `main` tree | `3ccdeb53f69db8fdcdbaf61a6c80bc4622d2e1b9` |
| Open PRs (implementation) | 0 |
| Published **works** | **76** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **40** |
| **Initially visible discovery entries** | **32** |
| **Prerender-manifest routes** | **3271** |
| Prerendered `.html` files | 3266 |
| **Sitemap URLs** | **3262** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** ·
Drama 5 · Cinema Writing 4 · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **76**.
**This checkpoint is superseded by the post-Wave-5-P1 checkpoint above** (same public metrics; the
implementation `main` has since advanced by the hidden Wave-5 P1 data foundation) and is retained only
as history.

Implementation `main` advanced from the post-Wave-4 close `ad998113…` to `946dc8a510ef5f836eab2af15d3b2d69ee9360c2`
(tree `3ccdeb53…`) by a single **post-Wave-4 production regression repair** — implementation PR #74, a
publication-landing copy fix. **This is NOT Wave 5 and NOT a reopening of Wave 4**, which remains
COMPLETE and CLOSED. Every public inventory and route metric is unchanged from the Wave-4 close (works
76 · Poetry 6 · collections 1 · shelves 9 · discovery 40 · visible 32 · prerender-manifest 3271 · `.html`
3266 · sitemap 3262 / 0 dup · `/poems/` 147); the repair changed only the shared landing description
copy, a new focused regression test, and its CI wiring — no data, payload, witness, route, or catalogue
change. Measured at the current production boundary: implementation `main`/tree and open PRs from live
GitHub; work/shelf/discovery census from the merged implementation; the prerender-manifest, `.html` and
sitemap figures from a production build of `946dc8a5…`; the sitemap duplicate check from deployed
production. The implementation backlog is back to **0**. See the post-Wave-4 repair section below.

### Verified live state — 2026-09-04, post-Wave-4-Poetry ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `ad998113c365f48aabf944b29d4b19b8679a14fc` |
| Implementation `main` tree | `e6a8c2920bc90f8cca73ea7de4049f32ac38d712` |
| Open PRs (implementation) | 0 |
| Published **works** | **76** |
| **Poetry works** (top-level) | **6** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **40** |
| **Initially visible discovery entries** | **32** |
| **Prerender-manifest routes** | **3271** |
| Prerendered `.html` files | 3266 |
| **Sitemap URLs** | **3262** |
| Sitemap duplicates | **0** |
| `/poems/` URLs | **147** |

**This checkpoint is superseded by the post-repair checkpoint above** (same public metrics; implementation
`main` has since advanced by the PR #74 landing-copy repair) and is retained only as history.

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** ·
Drama 5 · Cinema Writing 4 · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **76**.

Wave 4 Poetry onboarding took Poetry from **1 → 6** and the catalogue from **71 → 76**. Wave 4 left
Poetry with **six** top-level works: four standalone poems and two publications. Idhayathai was the
pre-existing Poetry work, so the **five** net additions were Anaiya, Marathi, Thennan, காலப் பேழை and
கலைஞரின் கவிதைகள். The two Poetry publications carry **135** internal reading units between them
(58 + 77); those units are **not** LibraryWorks and **not** collection members, so the collection count
stays **1**. Measured at the current production boundary: implementation `main`/tree and open PRs from
live GitHub; work/shelf/discovery census from the merged implementation; the prerender-manifest, `.html`
and sitemap figures from a production build of `ad998113…` with all pinned source clones present; the
sitemap duplicate check from deployed production. Wave 4 P0–P4 are merged; P5 is the control close-out
that records this state and adds no implementation change.

#### ⚠️ WORKS are not DISCOVERY ENTRIES — and publication UNITS are neither

Five distinct measurements describe this state and must never be conflated:

| measurement | value | what it counts |
|---|---:|---|
| **published works** | **76** | the archival catalogue — what the library holds (Poetry contributes 6) |
| **discovery entries** | **40** | what `/read` renders fully expanded; one collection entry stands in for 37 Fiction works |
| initially visible entries | 32 | of those 40, before any disclosure is opened |
| **prerender-manifest routes** | **3271** | the routes represented by the build's prerender manifest (`.html` subset **3266**) |
| **sitemap URLs** | **3262** | what the deployed sitemap lists, **0** duplicates |

**Fiction holds 39 works and renders 3 discovery entries** — never write "Fiction 3" as a work count.
**Poetry is now 6 works and 6 discovery entries.** The two Poetry publications together hold **135
internal reading units** (58 + 77); a reading unit is **not** a LibraryWork and **not** a collection
member. The two publications are **publications, not Reading Room collections** — collections remain
**1** (the 1977 short-story anthology).

Shipped / closed since the post-Film-Songs checkpoint:

- **Bulk Onboarding Wave 4 — Poetry** — the six-workspace Poetry onboarding: standalone Anaiya, Marathi
  and Thennan beside the pre-existing Idhayathai, plus the two publications காலப் பேழையும் கவிதைச்
  சாவியும் (58 units) and கலைஞரின் கவிதைகள் (77 units), and exactly two cross-witness relations linking
  the same canonical poem across a standalone witness and a publication-item witness. Implementation
  PRs #69–#73 all merged under the exact-head gate; production-verified; the durable P4 close is
  `ad998113…`. **If this text is being read from the unmerged P5 close-out branch, live control `main`
  remains authoritative and closure is only proposed. Once this control PR is on `main`, Wave 4 Poetry
  is durably COMPLETE and CLOSED.** See the dedicated Wave-4 section below.

### Verified live state — 2026-09-03, post-Film-Songs-control-close-out ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `1c6dcd81f0aa143a8e9b3162976c74dd18791058` |
| Open PRs (implementation) | 0 |
| Published **works** | **71** |
| **Collections** | **1** |
| Non-empty shelves | **9** |
| **Fully-expanded `/read` discovery entries** | **35** |
| **Initially visible discovery entries** | **27** |
| **Next build static-route count** | **3129** |
| **Sitemap URLs** | **3117** |

Shelf census, unchanged by that control-only close-out: Life Writing 1 · Letters 1 · **Fiction 39** · Poetry 1 ·
Drama 5 · Cinema Writing 4 · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **71**.
**This checkpoint is superseded by the post-Wave-4 checkpoint above** and is retained only as history;
its counts predate the five Wave-4 Poetry works.

#### ⚠️ WORKS are not DISCOVERY ENTRIES

This checkpoint retains the four measurements established by Reading Room Wayfinding. They must never
be conflated merely because this close-out changes no implementation count.

| measurement | value | what it counts |
|---|---:|---|
| **published works** | **71** | the archival catalogue — what the library holds |
| **discovery entries** | **35** | what `/read` renders when every shelf is expanded; one collection entry stands in for 37 works |
| initially visible entries | 27 | of those 35, what renders before any disclosure is opened |
| **Next build static-route count** | **3129** | every route the build prerenders |
| prerendered `.html` | 3121 | the subset written as HTML pages — an explanatory continuity metric, **not** the static-route count |
| **sitemap URLs** | **3117** | what the deployed sitemap lists, 0 duplicates |

**Fiction is the whole point of the distinction:** it holds **39 works** and renders **3 discovery
entries**. Writing "Fiction 3" as a work count, or "35 works", would erase 36 published works on
paper. The 37 anthology stories remain 37 independent works with their own routes.

**Measured at the current production boundary**, not copied forward: implementation `main`, tree and
open PRs from live GitHub; works, collections, shelves and discovery counts from the merged
implementation; the static-route and `.html` counts from the verified Wayfinding production build;
the sitemap count and duplicate check from deployed production. Film Songs close-out is control-only
and changes none of those implementation measurements.

Shipped / closed since the post-Wave-3 checkpoint:

- **Reading Room Wayfinding — Phase 0 + Phase 1** — the shelf disclosure that stopped `/read` from
  being an endless scroll, and the first collection layer, benchmarked on the 1977 short-story
  anthology. No content was onboarded: the catalogue is the same 71 works it was before. Closed by
  control PR #21; see the Wayfinding section below.
- **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs — formal control close-out.** The E1–E4
  implementation was already live and production-verified; this control-only activity records its
  source freeze, authorship/display contract, public/internal provenance boundary and staged PR chain.
  **If this text is being read from the unmerged close-out branch, live control `main` remains
  authoritative and closure is only proposed. Once this control PR is on `main`, Film Songs is durably
  COMPLETE and CLOSED.** See the dedicated section below.

### Verified live state — 2026-09-02, post-Wave-3 ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `c4660c49edb20895d11751e4454942e46e8b0951` |
| Open PRs (implementation) | 0 |
| Published works | **71** |
| Essays & Articles works | **4** |
| Non-empty shelves | **9** |
| **Next build static-route count** | **3128** |
| **Sitemap URLs** | **3116** |

Shelf census: Life Writing 1 · Letters 1 · Fiction 39 · Poetry 1 · Drama 5 ·
Cinema Writing 4 · Speeches 14 · **Essays & Articles 4** · Literary Commentary 2. Total **71**.

**This checkpoint is superseded by the current checkpoint above** and is retained only as history;
its route and sitemap counts predate the collection route. Measured at that boundary: implementation
`main` and open PRs from live GitHub; the catalogue census from the merged implementation;
static-route count from the merged production build; sitemap count from deployed production. The older prerendered `.html`
measurement is **3120** and remains an explanatory continuity metric only — it is not the Next static-route
count. Wave 3 contributes **+19 public URLs**: கயிற்றில் தொங்கிய கணபதி 3 · உணர்ச்சிமாலை 12 ·
திராவிட சம்பத்து 4. All **19/19** Wave-3 routes returned 200 in production, and all **16**
சக்கரவர்த்தியின் திருமகன் regression routes remained 200.

Shipped since the post-Wave-2 checkpoint:

- **Bulk Onboarding Wave 3 — Essays & Articles / three-publication batch** — கயிற்றில் தொங்கிய கணபதி,
  உணர்ச்சிமாலை and திராவிட சம்பத்து published together from one frozen historical source pin with
  three independently guarded work trees, taking Essays & Articles from 1 to 4 and the catalogue from
  68 to 71. Implementation PR #66 followed the exact-head gate, including one rejected green-CI head,
  a focused repair, a second exact-head review, approved squash merge and production verification.
  Closed by its merged control close-out; see the Wave-3 section immediately below.

### Verified live state — 2026-09-02, post-Wave-2 ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `4fd45a92663abbe70ff0c0a605168314cd36e44c` |
| Open PRs (implementation) | 0 |
| Published works | **68** |
| Fiction works | **39** |
| Non-empty shelves | **9** |
| **Next build static-route count** | **3109** |
| **Sitemap URLs** | **3097** |

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · Poetry 1 · Drama 5 ·
Cinema Writing 4 · Speeches 14 · Essays & Articles 1 · Literary Commentary 2. Total **68**.

**Measured now**, not copied forward: the SHA and open-PR count from live GitHub; the work/shelf
census from `data/library.ts` at that SHA; the static-route count from a production build of it; the
sitemap count from the deployed site. All 74 Wave-2 URLs return 200 in production.

Shipped since the post-Wave-1 checkpoint:

- **Bulk Onboarding Wave 2 — Fiction / 1977 short-story anthology** — the 37 stories of
  கலைஞர் கருணாநிதியின் சிறுகதைகள் published together from one frozen source release, taking Fiction
  from 2 to 39 and the catalogue from 31 to 68. **The second bulk-onboarding activity, and the first
  to run the exact-head sequence correctly end to end.** **Closed by this document**; see its section
  below.

### Verified live state — 2026-09-01, post-Wave-1 ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `0dc92fa0fd832b5932b8df75606ef049c9f261ea` |
| Open PRs (implementation) | 0 |
| Published works | **31** |
| Drama works | **5** |
| Non-empty shelves | **9** |
| Next build static-route count | **3035** |
| Sitemap URLs | **3023** |

Shelf census: Life Writing 1 · Letters 1 · Fiction 2 · Poetry 1 · **Drama 5** ·
**Cinema Writing 4** · **Speeches 14** · Essays & Articles 1 · Literary Commentary 2. Total **31**.

**This line is superseded by the post-Wave-2 checkpoint above** and is retained only as history.
Measured at that checkpoint: the SHA and open-PR count from live GitHub; the work/shelf census from
`data/library.ts` at that SHA; the page and static-route counts from a production build of it; the
sitemap count from the deployed site. All 22 Wave-1 URLs returned 200 in production.

#### ⚠️ Site-wide TOTALS vs a wave's DELTA — never mix them

Two independent mistakes are possible here, and earlier checkpoints made both.

**First: a total is not a delta.** Wave 2's public contribution is **+74 URLs** (37 reader routes +
37 `/source` routes). The build's static-route count (**3109**) is a *site-wide total* covering every
prerendered route in the whole Digital Library — 391 memoir chapters, 1330 Kurals, every speech, every
play, every story. The 74 is a *change*; 3109 is a *census*. They answer different questions and must
never be presented as the same kind of number.

**Second: the totals themselves are three different measurements**, nested rather than equal, as
measured at the Wave-2 merge boundary:

| measurement | value | what it counts |
|---|---|---|
| **Next build static-route count** | **3109** | every route the build prerenders, including route outputs that are not HTML pages |
| Prerendered `.html` files | 3101 | the subset written as actual HTML pages |
| **Sitemap URLs** | **3097** | the public, indexable subset — the 4 HTML pages excluded are `/_not-found`, `/about`, `/privacy` and `/support` |

**The two metrics this document uses going forward are the Next build static-route count and the
sitemap URL count:**

| metric | pre-Wave-2 | post-Wave-2 | delta |
|---|---|---|---|
| **Next build static-route count** | 3035 | **3109** | **+74** |
| **Sitemap URLs** | 3023 | **3097** | **+74** |

For the wave before it, the same two metrics moved 3013 → 3035 and 3001 → 3023, both **+22**.

⚠️ **The `.html` file count is NOT the Next static-route count and must never be quoted as one.**
`3101` is the post-Wave-2 `.html` figure and `3109` is the static-route count; likewise `3027` and
`3035` at the Wave-1 boundary. The `.html` count is the older "Prerendered pages" convention used by
checkpoints up to and including the pre-Wave-1 one. That convention was re-measured for continuity —
rebuilding pre-Wave-1 `main` (`56ca0c978e34afddde52595f2ce825872bd6aeef`) and counting prerendered
`.html` files returns exactly **3005**, so the historical rows are honest — but it is **not** the
build's route count, and it is **deliberately not carried in the CURRENT STATE table**. It is retained
here, in the explanatory table above, only for continuity. Historical checkpoints keep their own
`3005` / `3001` rows unchanged.

All three totals happen to move **+74** for Wave 2 because the same 74 URLs are involved. That is a
consequence, not evidence that they measure the same thing.

The Wave-1 boundary shipped:

- **Bulk Onboarding Wave 1 — Drama / கலைஞரின் நான்மணி மாலை four-play batch** — பரதாயணம், அனார்கலி,
  சாக்ரடீஸ் and சேரன் செங்குட்டுவன் published together from one frozen source release, taking Drama
  from 1 to 5 and the catalogue from 27 to 31. **The first bulk-onboarding activity**, and the reason
  bulk onboarding is now the standing default. **Closed by this document**; see its section below.

### Verified live state — 2026-09-01, pre-Wave-1 ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `56ca0c978e34afddde52595f2ce825872bd6aeef` |
| Open PRs (implementation) | 0 |
| Published works | **27** |
| Non-empty shelves | **9** |
| Prerendered pages | **3005** |
| Sitemap URLs | **3001** |

Shelf census: Life Writing 1 · Letters 1 · Fiction 2 · Poetry 1 · Drama 1 ·
**Cinema Writing 4** · **Speeches 14** · Essays & Articles 1 · Literary Commentary 2. Total **27**.

**This line is superseded by the post-Wave-1 checkpoint above** and is retained only as history.

Measured at that checkpoint, not copied from the one before it: the SHA and open-PR count from live
GitHub; the work/shelf census from `data/library.ts` at that SHA; the page count from a production
build of it; and the sitemap count from the deployed site. `https://nenjukkuneethi.org/read`,
`/speeches/kalaivanar-nsk-memorial-day` and `/speeches/kalaivanar-nsk-memorial-day/source` all
returned 200 in production.

Shipped between the 2026-08-30 checkpoint and that one:

- **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs** — implementation and publication are **live**
  in Cinema Writing, which is why that shelf is now 4 rather than 3. At this historical checkpoint its
  separate formal control-document close-out was still pending; that status is superseded by the
  CURRENT close-out section below.
- **Speech Benchmark #4 — கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** — the first
  audio-sourced speech, taking Speeches to 14 and the catalogue to 27. **Closed by this document**;
  see its section below.

### Verified live state — 2026-08-30 ⚠️ SUPERSEDED (kept as history)

| | |
|---|---|
| Implementation `main` | `766d68680cecca549d4d752e32561834f7dde0f5` |
| Open PRs | 0 |
| Published works | **25** |
| Non-empty shelves | **9** |
| Prerendered pages | **2948** |
| Sitemap URLs | **2944** |

Shelf census: Life Writing 1 · Letters 1 · Fiction 2 · Poetry 1 · Drama 1 ·
**Cinema Writing 3** · Speeches 13 · Essays & Articles 1 · Literary Commentary 2.

Verified against live production on 2026-08-30, not carried over from the previous checkpoint. The
previous 2026-08-26 line — `15405c7f…`, 24 works, 2853 pages, 2849 sitemap URLs, Cinema Writing 2 —
was the pre-Tirumbippaar state and is superseded. **This 2026-08-30 line is itself now superseded by
the 2026-09-01 checkpoint above** and is retained only as history.

### Phases shipped after this document's Phase-7 narrative

These are recorded here as completed fact. Their detail lives in the implementation repository's
merged PRs, not in this file:

- **Thirukkural — கலைஞர் உரை** (Literary Commentary), including the Daily Kural surface.
- **Assembly-speech anthology** — the remaining 10 dated sittings, taking Speeches to 13.
- **Phase B — கிழவன் கனவு** (Fiction short story), taking Fiction to 2.
- **Phase C — பராசக்தி** (Cinema Writing), taking Cinema Writing to 2.
- **Phase D — திரும்பிப்பார்** (Cinema Writing), taking Cinema Writing to 3 and the catalogue to 25.
- **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs** (Cinema Writing), taking Cinema Writing to 4
  and the catalogue to 26. Implementation live; its later formal control close-out is recorded in the
  dedicated CURRENT section below.
- **Speech Benchmark #4 — the first audio-sourced speech**, taking Speeches to 14 and the catalogue
  to 27. **Closed by this document.**
- **Bulk Onboarding Wave 1 — Drama**, taking Drama to 5 and the catalogue to 31. The first
  bulk-onboarding activity. **Closed by this document.**
- **Bulk Onboarding Wave 2 — Fiction / the 1977 short-story anthology**, taking Fiction to 39 and the
  catalogue to 68. **Closed by this document.**
- **Bulk Onboarding Wave 3 — Essays & Articles / three-publication batch**, taking Essays & Articles
  to 4 and the catalogue to 71. Exact-head implementation review included one rejected head and a
  repaired approved head; production verification passed. **Closed by its merged control close-out.**

---

## Bulk Onboarding Wave 5 — Cinema Writing / Manthiri Kumari + Raja Rani — ✅ COMPLETE and CLOSED (P0 ✅ · P1 ✅ · P2 ✅ · P3 ✅ · P4 ✅ · P5 ✅)

**The fifth bulk-onboarding wave, and the first Cinema Writing wave.** Owner-authorized; the selected
batch is **மந்திரி குமாரி / Manthiri Kumari** and **ராஜா ராணி / Raja Rani**, both from
`pugazg/kalaignar-cinema-works`, on the Cinema Writing shelf. **Wave 5 is COMPLETE and CLOSED** — P0
(census), P1 (source freeze + data foundation), P2 (public readers/routes), P3 (catalogue/discovery/
sitemap exposure), P4 (cross-work regression/integrity hardening) and P5 (production acceptance + durable
control closure) are all complete. The public site is **78 works / Cinema Writing 6**. Manthiri Kumari +
Raja Rani onboarding is fully complete. **Since this close, Wave 6 P0 (completed-works census) is COMPLETE
(assessment only — see the Wave-6 P0 subsection in the CURRENT block above); Wave 6 P1 is NOT authorized
and has NOT started.**

Staging, all complete: **P0** census ✅ · **P1** source freeze + deterministic data foundation ✅ · **P2**
public readers/routes/`/source` pages ✅ · **P3** catalogue/discovery/sitemap exposure ✅ · **P4**
cross-work regression/integrity hardening ✅ · **P5** production acceptance + Wave-5 control close-out ✅.
**P0–P5 are frozen historical stages; Wave 5 must not be reopened from stale prompts** unless a newly
discovered, source-backed regression requires a separately authorized bounded repair.

### P0 — source-readiness census ✅ COMPLETE

A read-only census across all source repositories selected the two release-complete Cinema Writing
works as the strongest coherent, source-ready batch (one repo, one shelf, Tamil + English + bilingual
QA closed). Runners-up recorded but not selected: `kudumbaththin-nalvilakku` (Essays, fully frozen,
single work) and `pudhaiyal` (novel, release-ready with two physical-loss `needs-review` scans).
`kolaikkalam` was NEAR (English mid-translation); `ina-muzhakkam` / `kuraloviyam` / `sangatamil` /
short-stories 38+ NOT ready. Manimagudam and `kalaivanar-nsk-memorial-day-audio-06` remain excluded.

### P1 — source freeze + deterministic data foundation ✅ COMPLETE

Implementation PR **#75** merged. This is a hidden data foundation; it published nothing.

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#75` |
| First reviewed head — NOT APPROVED | `2bef0a7c686d164c5aeee57800d7c3477c195753` (validator-trust finding) |
| Exact approved head | **`b1f67597ddb3519c46cf5f41aabb6c078e6619f5`** |
| Approved head tree | **`41fb1a5431195d6796e7d8bd4181ffa883bb29b0`** |
| Squash merge / implementation `main` | **`7cc0546fc311aabae2a67ef3d7f8c5fd2390b7d5`** |
| Merged tree | **`41fb1a5431195d6796e7d8bd4181ffa883bb29b0`** (== approved head tree) |
| Base | `946dc8a510ef5f836eab2af15d3b2d69ee9360c2` |
| Library CI | archival validators + typecheck·build green (named steps Manthiri Kumari / Raja Rani Wave 5 P1) |
| Production | Vercel success; `/cinema/manthiri-kumari` and `/cinema/raja-rani` return 404 (not exposed) |

The approved PR-head tree and the squash-merged `main` tree are the **same tree SHA** — no drift.

**Source freeze.** `pugazg/kalaignar-cinema-works` @ **`75b22046490f92df3bbf641a69a59fcad7b91bde`**
(repo tree `43d28d85587294279e4d7fe901b143f5ec469194`). Per-work tree pins (mandatory — this repo holds
many unrelated works): Manthiri Kumari **`225662fc8f93d91daff0005b348948da6372840b`** · Raja Rani
**`abbc5cb8890e67ad2b18e0ab50e5af6f678bbd06`**. Source `main` has since advanced for unrelated work
(e.g. `388517aa…`), but **both selected work trees are unchanged, so the historical freeze remains
valid and no repin was required.** No source PDFs are vendored (identity = filename + SHA-256 + pages:
Manthiri `TVA_BOK_0026144` `a64ac0b5…` 14pp; Raja Rani `TVA_BOK_0017188` `26ecc026…` 80pp / 79 canonical).

**Generated frozen artifacts (P1 checkpoint bytes).**

| artifact | SHA-256 |
|---|---|
| `public/data/cinema/manthiri-kumari/reader.json` | `ebdbf54fde3031a5027eb0bd61874c2c606a4c765676d2b2f2802082c965bffe` |
| `public/data/cinema/manthiri-kumari/provenance.json` | `1355625046f020110e815c12b5aa16e006afa9dd9deb375aea44838c646a67b2` |
| `public/data/cinema/raja-rani/reader.json` | `f1c28efe2a3be14a7a4e379ac7f7ebd41d080ebd59566074854fffe12e7c4acf` |
| `public/data/cinema/raja-rani/provenance.json` | `2dbcbd4786672dfcce6b9d97a9c0ca90bf3b990fbafe4a08d8e1bdc37097ec1b` |

**Importer / validator architecture.** Deterministic importers (`scripts/import-<slug>.mjs`) consume
the pinned QA-PASS `integrations/reading-room/reading-room.json` payloads plus referenced records and
emit the artifacts above (byte-identical reruns). Validators (`scripts/validate-<slug>.mjs`) use an
INDEPENDENT evidence path — the raw layer indexes (`scenes/index.json`, `dialogues/index.json`,
`songs/index.json`, `metadata.yaml`, `editions/en/manifest.json`) — and, after the review, pin the
approved freeze as **independent constants** (source commit, repo/work trees, PDF SHA, reading-room SHA,
reader SHA, provenance SHA) proving *constant → provenance* AND *constant → artifact* separately, so a
coordinated `reader.json + provenance.json` mutation cannot redefine the expected truth. Registered in
`npm run validate` and the CI archival job. Final results: **Manthiri Kumari 90 / 0**, **Raja Rani
75 / 0**. Fourteen adversarial mutations (7 per work) each fail — the coordinated hash mutations on the
independent hash pin, every semantic mutation on its specific assertion.

**Durable source semantics — must survive P2+.**

- **Manthiri Kumari** — a *film story-song booklet, NOT a screenplay*: 1 story summary (13 logical
  units, 1 cross-page) + **15 performance blocks** (52 sections, **234/234** Tamil/English line-cues,
  7 cross-page). Performance ordinals 1–15 are **archival source-order navigation, not printed
  numbering**; **0 source-numbered scenes**. Item-level lyricists **0 verified / 15 unresolved** — the
  cover's story/dialogue credit is not a lyric credit, and later anthology text must not repair the
  booklet. **Block 11 alone** is a confirmed existing-anthology witness of **`kalaignar-song-001`**; the
  other 14 are source-only. **Performance 13** keeps its printed heading `பார்த்திபன்—மந்திரிகுமாரி`
  distinct from its internal turn labels `பார்த்திபன்` / `அமுதவல்லி` — never collapse them.
- **Raja Rani** — a dialogue screenplay with numbered songs: **58 archival/editorial scene segments**
  that are **NOT source-printed scene numbers** (songs 1–11 ARE genuine source numbering). **1,236**
  English screenplay units (1,090 dialogue / 137 stage-direction / 4 performance-cue / 5 written-text),
  **1,071** immutable dialogue links, **19** source-unlabelled spoken units. Songs: 67 sections,
  **181/181** line-cues, authorship **5 anthology-attributed / 6 unresolved** (never upgraded). The sole
  review-level relation is **`raja-rani-song-011` ↔ scene 58** (occurrence `raja-rani-song-perf-004`);
  the three verified relations are songs 003@4 / 005@16 / 008@40. Deleted duplicate ids
  `s055-d026`–`s055-d030` must never return; the PDF-74 `K. N. சங்கரன்` ownership stamp stays excluded
  from canonical text.

Authorship certainty stays separate from display eligibility; no rights/year/edition inferred (all
null). No cross-witness UI/relation is created in P1.

### P2 — public readers / direct routes / `/source` pages ✅ COMPLETE

Implementation PR **#76** merged. P2 makes both works directly readable through public routes while
keeping them out of the Reading Room catalogue/discovery/sitemap until P3.

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#76` |
| First reviewed head — NOT APPROVED | `5cf02d73…` (source-page semantics finding) |
| Exact approved head | **`7eedf14c9de0cd680356445c6dfa930d3d4f0734`** |
| Approved head tree | **`9bf711784a86458f95a333c6f4c1768cbe65f690`** |
| Squash merge / implementation `main` | **`cf6a952ca9f0edea254d9c72b48ef333523bfd51`** |
| Merged tree | **`9bf711784a86458f95a333c6f4c1768cbe65f690`** (== approved head tree) |
| Base | `7cc0546fc311aabae2a67ef3d7f8c5fd2390b7d5` |
| Library CI | archival validators + typecheck·build green (named steps Manthiri/Raja P1 + **Cinema readers — Manthiri Kumari + Raja Rani (Wave 5 P2)**) |
| Production | Vercel success; all direct routes 200, invalid children 404, `/read` still excludes both works |

**Route contract — +89 direct public routes (registry-driven, fail-closed with `dynamicParams = false`).**

- **Manthiri Kumari — 18 routes**: landing · story-summary surface (13 units) · 15 performance surfaces
  · `/source`. A booklet, **not a screenplay**: performance ordinals 1–15 are labelled **archive
  navigation** (`களஞ்சிய வரிசை N`), never printed source numbers; **0 source-numbered scenes**. Every
  performance shows an **unresolved-lyricist** note (15/15) and no blanket Kalaignar lyric claim. **Block
  11 alone** is the confirmed anthology witness of `kalaignar-song-001` — the source page describes it as
  **`களஞ்சிய வரிசை 11`**. **Performance 13** keeps its printed compound heading
  `பார்த்திபன்—மந்திரிகுமாரி` distinct from the internal turn labels `பார்த்திபன்` / `அமுதவல்லி`. Source
  page: archive id **`TVA_BOK_0026144`**; Tamil stated as the **controlling** text (`மூல தமிழே ஆளும் உரை`),
  not "official".
- **Raja Rani — 71 routes**: landing · **58 archival scene-segment surfaces** · **11 numbered-song
  surfaces** · `/source`. The 58 segments are **archival/editorial navigation** (`களஞ்சியப் பகுதி N`),
  **0 source-numbered scenes**; the **11 song numbers are source-backed** (`பாட்டு 1–11`). Authorship
  frozen at **5 anthology-attributed / 6 unresolved** (never flattened). The **segment-58 ↔ song-11**
  relation (occurrence `raja-rani-song-perf-004`) stays **review-level**. The deleted T055 duplicate ids
  and the PDF-74 ownership stamp are absent from all rendered output. Source page: archive id
  **`TVA_BOK_0017188`**; relation copy uses **`களஞ்சியப் பகுதி 58`** and the deletion note
  **`களஞ்சியப் பகுதி 55`** — no plain `காட்சி 58/55`.

Bilingual per the existing cinema convention (Tamil default + in-page toggle; Tamil authoritative;
English project-created, exact printed Tamil speaker labels never expanded). No PDF page/hash/commit
appears in any reader — all provenance is on `/source`. P1 reader/provenance bytes are unchanged
(`ebdbf54f…` / `f1c28efe…`); P1 validators still 90/0 and 75/0; the P2 UI test is **443/0**.

**Catalogue/discovery/sitemap stay deferred to P3.** After P2: works **76**, Cinema Writing **4**,
Poetry 6, collections 1, shelves 9, discovery **40**, visible **32**, sitemap **3262** / 0 dup — all
unchanged. Only the build route count moved: prerender-manifest **3271 → 3360**, `.html` **3266 → 3355**
(**+89**). Neither work is in `data/library.ts` or the sitemap; both are directly addressable but
undiscoverable from `/read`.

### P3 — catalogue / discovery / sitemap exposure ✅ COMPLETE

Implementation PR **#77** merged. P3 turned the two already-live P2 cinema readers into normal Reading
Room catalogue/discovery/sitemap members **without adding any new page route** — the +89 routes were
already live from P2.

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#77` |
| First reviewed head — NOT APPROVED | `fba5e30b…` (false Set-equality proof; over-cap shelf mislabelled Fiction; Manthiri comment; Raja over-claimed a role credit) |
| Second reviewed head — corrections | `7b0846ca…` (exact-set proof, over-cap identity, Raja neutralised) |
| Exact approved head | **`6aa7a25cc9c8da7a709b2de24222b08d64359401`** (final provenance-comment correction: PDF 1 vs PDF 2) |
| Approved head tree | **`270d66492ec70fbd7c24a9e05f044a454b533b9a`** |
| Squash merge / implementation `main` | **`c6ac8b6cde867c865c5358e252828fbf0b4f8524`** |
| Merged tree | **`270d66492ec70fbd7c24a9e05f044a454b533b9a`** (== approved head tree) |
| Base | `cf6a952ca9f0edea254d9c72b48ef333523bfd51` |
| Library CI | archival validators + typecheck·build green (named step **Cinema catalogue/discovery/sitemap (Wave 5 P3)** — 66/0) |
| Production | Vercel success; `/read` shows six Cinema cards in order; all routes 200, invalid children 404; sitemap 3351 / 0 dup |

**The approved PR-head tree and the squash-merged `main` tree are the same tree SHA
`270d66492ec70fbd7c24a9e05f044a454b533b9a` — no drift.**

**Catalogue / discovery / sitemap contract.** Two new `LibraryWork` records on the Cinema Writing shelf
in onboarding order — **Manohara · Parasakthi · Tirumbippaar · Kalaignar Film Songs · Manthiri Kumari ·
Raja Rani**. Works **76 → 78**, Cinema Writing **4 → 6**, discovery entries **40 → 42**, initially
visible **32 → 34**, collections **1**, shelves **9**. Cinema Writing sits **exactly at the six-entry
cap**, so all six cards are initially visible with **no** disclosure control. **Speeches (14 discovery
entries) remains the sole over-cap shelf**; **Fiction has 3 discovery entries despite 39 works** (below
the cap — its 37-story anthology is one collection entry). Prerender-manifest **3360** and `.html`
**3355** are unchanged from P2 (no new page route).

**Sitemap — exactly the +89 already-live P2 route set, registry-derived.** Sitemap **3262 → 3351**,
**0** duplicates. Manthiri **18** (landing + `/source` + story-summary + 15 performances); Raja Rani
**71** (landing + `/source` + 58 archival scene segments + 11 source-numbered songs). Both sets are
enumerated from the frozen reader registries through **`lib/cinema-wave5-routes.ts`** — the single slug
authority shared by the `[item]`/`[section]` `generateStaticParams` and the sitemap, so the two cannot
drift. **No numeric reconstruction.** The corrected P3 test proves **true exact-set membership** (sorted
arrays + bidirectional set-difference — the earlier draft used `eq(new Set(a), expSet)`, which false-passes
because `JSON.stringify(new Set(...)) === "{}"`), and rejects both missing and extra URLs. Production
sitemap re-verified at close: the 18 + 71 = 89 Wave-5 URLs match the registry exactly, no missing, no
extra.

**Semantic safeguards (durable — must survive P4+).**

- **Manthiri Kumari** — a **film booklet, not a screenplay**; keeps its **source-backed** story/dialogue
  credit `கலைஞரின் கதை–வசனம்` / "Kalaignar's story and dialogue" (the booklet prints
  `கதை, வசனம் : மு. கருணாநிதி`); 15 performance blocks in source order; **no source scene-numbering
  system**; 15 item-level lyricists **unresolved**; no blanket song-authorship claim; no inferred
  year/edition/rights.
- **Raja Rani** — **neutral** catalogue description `வசன நூல்: 58 களஞ்சியப் பகுதிகளும் மூல எண்ணிடப்பட்ட
  11 பாடல்களும்` / "Dialogue screenplay publication: 58 archive segments and 11 source-numbered songs",
  with **no role-specific credit** (Raja's source carries no equivalent explicit role line, so
  `கலைஞரின் கதை–வசனம்` / "Kalaignar's story and dialogue" must NOT be introduced for Raja); **58 archive
  segments, 0 source-numbered screenplay scenes**; 11 source-numbered songs; **5 anthology-attributed /
  6 unresolved**; the segment-58 ↔ song-11 relation stays **review-level**; no inferred
  year/edition/rights. The internal `data/library.ts` provenance comment distinguishing **PDF 1** (cover:
  `மு. கருணாநிதி` with `முழு வசனம்` / `பாடல்கள்`) from **PDF 2** (`முழுவசனம், கதை` / `பூராப்பாடல்கள்`) is
  accepted and must remain — it does not elevate either layout into a public role or song-authorship
  claim.

P1 reader/provenance bytes are unchanged (`ebdbf54f…` / `1355625046…` / `f1c28efe…` / `2dbcbd47…`); P1
validators still **90/0** and **75/0**; P2 UI **443/0**; P3 catalogue/discovery/sitemap **66/0**;
collections **258/0**; poetry-architecture **118/0**; shelf-disclosure **60/0** (34 visible / 1
disclosure); `npm run validate` exit 0; typecheck clean; production build ✓.

### P4 — cross-work regression / integrity hardening ✅ COMPLETE

Implementation PR **#78** merged. P4 is a **test/CI/package-only** hardening layer — a durable
higher-level regression contract over the completed P1/P2/P3 Cinema Writing implementation. **It changes
no product behaviour, catalogue, route, sitemap, reader data or source.**

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#78` |
| First reviewed head — NOT APPROVED | `1b2d5349…` (A4 protected the four legacy Cinema families by count only) |
| Exact approved head | **`92367e2e8cbb1110711970ef25d95166545b9212`** |
| Approved head tree | **`6a4b2cd6bdcdada399cdb27247e485527813a7b2`** |
| Squash merge / implementation `main` | **`632476baa40ebbe94083ec41a6c8f4a26dfec77c`** |
| Merged tree | **`6a4b2cd6bdcdada399cdb27247e485527813a7b2`** (== approved head tree) |
| Base | `c6ac8b6cde867c865c5358e252828fbf0b4f8524` |
| Library CI | archival validators + typecheck·build green (named steps **Cinema cross-work integrity (Wave 5 P4)** 475/0 and **Cinema cross-work UI regression (Wave 5 P4)** 33/0) |
| Production | merged-main Library CI success; `/read` six Cinema cards in order; sitemap 3351/0, 346 Cinema URLs |

**The independently approved PR-head tree and the squash-merged `main` tree are the same tree SHA
`6a4b2cd6bdcdada399cdb27247e485527813a7b2` — no drift.**

**Changed files (4, all hardening surface).** `scripts/validate-wave5-p4-cinema-integrity.ts` (new,
no source clone), `scripts/test-wave5-p4-cinema-ui.ts` (new, renders `LibraryHome` EN+TA),
`package.json` (`test:wave5-p4-cinema-integrity`, `test:wave5-p4-cinema-ui`), `.github/workflows/library-ci.yml`
(two named steps in `typecheck • build`, after Build and after the P2/P3 steps).

**Integrity gate — 475 / 0.** A1 the four Wave-5 payloads byte-pinned (exact SHA-256, unchanged:
`ebdbf54f…` / `1355625046…` / `f1c28efe…` / `2dbcbd47…`). A2 six-work census/identity + onboarding
order (no 7th). A3 each work's distinct source semantics as positive assertions (Manohara archival
segments + nationalisation rights; Parasakthi 46 printed scenes; Tirumbippaar 93 scenes + 1953 edition;
Film Songs 54 corpus; Manthiri film-booklet + source-backed credit + 15 unresolved + block-11 sole
witness + perf-13 heading; Raja neutral, 58 archive / 0 source-numbered, 5 attributed / 6 unresolved,
song-11↔scene-58 **review**, verified 3@4/5@16/8@40). **A4 — exact registry-derived membership for ALL
SIX Cinema families** (not count-only, not only Wave-5): each expected set derived independently from
that work's released registry (legacy four from the generated `index.json` `segments`/`scenes`/`songs`,
never a numeric range; Wave-5 two from the frozen `reader.json` via `lib/cinema-wave5-routes`), proven by
length, registry-size == pinned count, sorted-array equality, bidirectional set-difference, and no
in-family duplicate; the six families exactly **partition** the **346** Cinema URLs with no cross-family
collision; Wave-5 **89 = 18 + 71**; no `JSON.stringify(Set)`. A5 global invariants (78 works, census,
42/34 discovery, Cinema at cap, Speeches sole over-cap, Fiction 39 works / 3 entries). A6 sitemap 3351/0.
**A7 build-output boundary** from the real `.next`: prerender **3360**, `.html` **3355**, and the
**complete production-build Cinema route set == the sitemap Cinema route set as exact sets (== 346, no
build-only, no sitemap-only)** — closing the same-size build/sitemap drift gap.

**UI gate — 33 / 0.** Six Cinema cards in onboarding order; per-work rendered semantics distinct;
Manthiri keeps its credit / Raja stays neutral; no year/edition/rights on the Wave-5 cards; Cinema renders
no disclosure; Speeches carries the sole one.

**Route-family exact memberships (all six):** Manohara **59** · Parasakthi **48** · Tirumbippaar **95** ·
Film Songs **55** · Manthiri Kumari **18** · Raja Rani **71** = **346**. Wave-5 subset **89 = 18 + 71**.

**Adversarial proof.** The original eight mutations each still fail for their intended reason. The new
**legacy-family same-count substitution** — replacing one registered Manohara sitemap child with an
unregistered same-family slug, family count held at **59** and Cinema total held at **346** — fails on the
Manohara **exact-membership** and the **A7 build/sitemap set** assertions, **not** on any count assertion.
All mutations restored; the committed tree holds only the P4 patch.

**Regression + boundary.** P2 443/0 · P3 66/0 · collections 258/0 · poetry-architecture 118/0 ·
shelf-disclosure 60/0 · Manthiri P1 90/0 · Raja P1 75/0 · `npm run validate` exit 0 · typecheck clean ·
clean production build ✓ · `git diff --check` clean. **Source freeze `75b22046…` unchanged** (both target
work trees `225662fc…` / `abbc5cb8…` unchanged even at live source `main`, which advanced only for
unrelated Naam work); **four P1 payload hashes unchanged**. Every public count identical to the P3 close.

### P5 — production acceptance + Wave-5 control close-out ✅ COMPLETE

P5 is the final Wave-5 stage: an independent production acceptance of the merged P1–P4 boundary and the
durable control closure. **P5 produced NO implementation delta** — no implementation PR was opened; the
accepted boundary is the P4 merge `632476baa40ebbe94083ec41a6c8f4a26dfec77c` (tree
`6a4b2cd6bdcdada399cdb27247e485527813a7b2`), unchanged. This control close-out is the only P5 artifact.

**Production acceptance (measured on `https://nenjukkuneethi.org`).**
- `/read`: the six Cinema Writing cards render in onboarding order — Manohara · Parasakthi · Tirumbippaar ·
  Kalaignar Film Songs · Manthiri Kumari · Raja Rani; Cinema is exactly at the six-entry cap with **no**
  disclosure control; Speeches is the **sole** over-cap shelf (one `<details>` on the page).
- Manthiri Kumari: landing, `story-summary`, `performance-01/11/13/15`, `source` all **200**;
  `performance-16` / `performance-99` **404**. Booklet not screenplay; source-backed story/dialogue credit
  present; perf-13 heading distinct; no scene-numbering; block-11 sole witness; 15 lyricists unresolved;
  no year/edition/rights.
- Raja Rani: landing, `scene-001`, `scene-058`, `song-01`, `song-11`, `source` all **200**; `scene-000` /
  `scene-059` / `song-12` **404**. 58 archive segments (not source-numbered scenes); 11 source-numbered
  songs; catalogue neutral (no Manthiri role credit); 6 songs unresolved and "unresolved ≠ not Kalaignar's"
  note present; segment-58↔song-11 relation **review-level** (not verified); deleted T055 ids and the
  PDF-74 ownership stamp absent from served text; no year/edition/rights.
- Production sitemap: **3351** URLs / **0** duplicates; **346** Cinema URLs; per-family **59/48/95/55/18/71**;
  Wave-5 subset **89 = 18 + 71**; `/poems/` **147**.

**Acceptance from current `main` (clean production build).** P4 integrity **475/0** (incl. exact
registry-derived membership for all six families and the build-vs-sitemap exact-set equality — the full
production-build Cinema route set == the sitemap Cinema route set == 346, no missing/extra/duplicate/
same-count substitution) · P4 UI **33/0** · P2 **443/0** · P3 **66/0** · collections **258/0** ·
poetry-architecture **118/0** · shelf-disclosure **60/0** · Manthiri P1 **90/0** · Raja P1 **75/0** ·
`npm run validate` exit 0 · typecheck clean · clean production build (prerender **3360** / `.html` **3355**)
· `git diff --check` clean. Global boundary: works **78** · Cinema **6** · Poetry **6** · collections **1**
· shelves **9** · discovery **42** / visible **34**. Source freeze `75b22046…` and target work trees
`225662fc…` / `abbc5cb8…` unchanged even at live cinema source `main`; the four P1 payload hashes
(`ebdbf54f…` / `1355625046…` / `f1c28efe…` / `2dbcbd47…`) unchanged. No production/runtime/data/route/
semantic regression was found.

### Standing state after Wave 5 (CLOSED)

P0, P1, P2, P3, P4 and P5 are COMPLETE; **Wave 5 is COMPLETE and CLOSED.** Manthiri Kumari + Raja Rani
onboarding is fully complete and needs no further control action. **Do not reopen Wave 5 from stale
prompts** — P0–P5 are frozen historical stages unless a newly discovered, source-backed regression requires
a separately authorized bounded repair (which would not be P5 and would not reopen the closed stages). Both
cinema works are normal catalogue members (works **78**, Cinema Writing **6**); do not add further Cinema
Writing works, change those counts, alter the Manthiri/Raja catalogue cards or their neutral/attributed
wording, modify the +89 sitemap set, weaken the P4 gates, or repin the Wave-5 freeze `75b22046…`. **No
Wave 6 has been authorized and no automatic next onboarding wave is selected — await explicit owner
direction.** Validator-contract migration remains PAUSED; native mobile ON HOLD; Reading Room Phase 2
unauthorized; Wave 4 and the Poetry regression repair remain closed.

---

## Post-Wave-4 Poetry publication landing copy regression repair — ✅ COMPLETE and CLOSED

**A single post-Wave-4 production regression repair — NOT Wave 5, NOT a reopening of Wave 4.** Wave 4
Poetry remains COMPLETE and CLOSED; this repair only corrected one shared UI copy defect discovered in
production after the Wave-4 close.

**Defect.** The shared `components/PublicationLanding.tsx` description paragraph hard-coded "58 poems …
numbered first part" (`…முதல் பாகத்தில் உள்ள 58 கவிதைகள்`). That is source-true for
**காலப் பேழையும் கவிதைச் சாவியும்** (58 poems, the book's numbered first part, no groups) but wrong for
**கலைஞரின் கவிதைகள்** (77 poems across 5 source-established groups): its landing rendered a contradictory
**58** and a false "numbered first part" structure, even though its badge and `<meta>` description
already used `pub.itemCount` (77).

**Repair.** The description is now derived from each publication's own already-approved structure via
`describePublication(pub, ta)` — the count is always `pub.itemCount`, and a publication with
source-established groups (>1) reports its section count while a flat publication does not. No mechanical
58→77 substitution (that would have preserved the false "numbered first part" claim for the grouped
anthology), no per-title hard-coding, and **no new data field or payload edit** — the twelve pinned
Wave-4 payloads are untouched. Final rendered copy:

- காலப் பேழை… (flat): TA `இந்த நூலில் உள்ள 58 கவிதைகள். …` · EN "The 58 poems of this book. …"
- கலைஞரின் கவிதைகள் (grouped): TA `…5 பிரிவுகளாக அமைந்த 77 கவிதைகள். …` · EN "The 77 poems of this
  book, arranged in its 5 source-established sections. …"

**Regression coverage.** New `scripts/test-publication-landing-copy.ts` (19 positive checks) proves
Kaalap 58 and கலைஞரின் கவிதைகள் 77 in **both** Tamil and English, proves the grouped "sections"/
"பிரிவுகள்" wording renders for the grouped publication only, and proves neither publication inherits the
other's count or structural wording. It fails against the old hard-coded copy and passes with the fix.
Registered as an npm script and a named CI step.

**Implementation identity.**

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#74` |
| Base | `ad998113c365f48aabf944b29d4b19b8679a14fc` |
| Independently approved head | **`afd4c1c3c039505b67f259826a8e21556d896f40`** |
| Approved head tree | **`3ccdeb53f69db8fdcdbaf61a6c80bc4622d2e1b9`** |
| Squash merge / implementation `main` | **`946dc8a510ef5f836eab2af15d3b2d69ee9360c2`** |
| Merged tree | **`3ccdeb53f69db8fdcdbaf61a6c80bc4622d2e1b9`** (== approved head tree) |
| Changed files | **4** — `components/PublicationLanding.tsx`, `scripts/test-publication-landing-copy.ts`, `package.json`, `.github/workflows/library-ci.yml` |
| Library CI | archival validators + typecheck·build green (incl. the new named landing-copy step) |
| Production | Vercel success for `946dc8a5…` |

**Production verification (all four combinations, live):** காலப் பேழை… TA **58** / EN **58** (flat, no
grouped-section wording); கலைஞரின் கவிதைகள் TA **77 + 5 பிரிவுகள்** / EN **77 + 5 source-established
sections** — with the incorrect **58** and any "numbered first part" / `முதல் பாக…` wording absent from
the 77-poem publication in both languages. Item lists still render, கலைஞரின் கவிதைகள் keeps its group
dividers, காலப் பேழை stays flat, and both `/source` links work.

**Scope.** Zero route/sitemap delta (prerender-manifest 3271 · `.html` 3266 · sitemap 3262 / 0 dup ·
`/poems/` 147); inventory unchanged (76 · Poetry 6 · collections 1 · shelves 9 · discovery 40 / visible
32 · 58 + 77 = 135 internal units · exactly two witness relations); twelve P4 payload pins green; no
source repo, payload, witness, route, or catalogue change. **Implementation backlog: 0.** No new
onboarding wave is authorized; Reading Room Phase 2 is not authorized; validator-contract migration
remains PAUSED; native mobile remains ON HOLD; no further Poetry onboarding is authorized.

---

## Bulk Onboarding Wave 4 — Poetry / six-workspace onboarding + cross-witness model — ✅ COMPLETE and CLOSED

**The fourth bulk-onboarding activity, and the first to ship a cross-witness relation model.** All six
frozen Poetry source workspaces are now publicly represented, taking the Poetry shelf from 1 to 6 and
the catalogue from 71 to 76. Implementation is merged and production-verified across five staged PRs
(#69–#73); this section is the durable merged control closure. P5 is documentation-only and changes no
implementation code, content, route, relation, catalogue entry or payload.

### Implementation identity and durable checkpoint chain

Wave 4 shipped as five exact-head-gated phases. Each phase opened one bounded PR from verified live
`main`, was independently reviewed at its exact head, squash-merged only at the approved SHA, and
production-verified. The durable merged checkpoints are the important history; rejected/replaced review
heads are not preserved here.

| phase | PR | purpose | squash merge / durable `main` |
|---|---:|---|---|
| P0 | #69 | Poetry **publication architecture** foundation | `69aa7653bccd9ca8cec75ace9c0f2ead3903a919` |
| P1 | #70 | standalone onboarding — Anaiya, Marathi, Thennan (beside existing Idhayathai) | `f9cd1ccd58c2df40927f20f153a95eafab8d69fa` |
| P2 | #71 | **காலப் பேழையும் கவிதைச் சாவியும்** — 58 internal units | `b480d53f8ba1bb3658cdad8efd8ca1152bc58fa6` |
| P3 | #72 | **கலைஞரின் கவிதைகள்** — 77 internal units + exactly two witness relations | `364d64d16d2c6bbe1f130a17935c5f3a3a73c3a1` |
| P4 | #73 | cross-witness **regression / public-semantics hardening** | **`ad998113c365f48aabf944b29d4b19b8679a14fc`** |

The durable Wave-4 implementation close is P4 squash-merge
**`ad998113c365f48aabf944b29d4b19b8679a14fc`**, tree
**`e6a8c2920bc90f8cca73ea7de4049f32ac38d712`**. The independently approved P4 PR-head tree and the
squash-merged `main` tree are the **same tree SHA** — the squash introduced no drift. Post-merge Library
CI run **`33838803531`** succeeded (both jobs), production Vercel succeeded for the merge commit, and a
four-direction witness production smoke-check passed.

### Source freeze — final record

| | |
|---|---|
| Source repository | `pugazg/kalaignar-poems` (READ ONLY) |
| **Frozen Wave-4 source pin** | **`969823195ea8943a67fad4286ab1bc7f1c876d56`** |
| **Frozen source tree** | **`e382ee02c8f333da9ddfd61f3c9858b97c65cf3b`** |

All six frozen top-level Poetry work trees (subtrees under `poems/` at the frozen pin), re-verified at
close-out:

| work | source work tree |
|---|---|
| `anaiya-vilakku-anna` | `bddc54f0493dbc38e53f9ec9fe5162e0c4e49464` |
| `idhayathai-thanthidu-anna` | `a92fb5ff742aa1c5ae11039fc55a9ffa4bdafc63` |
| `kaalap-pezhaiyum-kavithai-saaviyum` | `07a2d3cba65a1eb10b887dac3c83ce993f94a710` |
| `kalaignarin-kavithaigal` | `6489ab3d4fdf21a1442aa46d7a7aa1a08071be7e` |
| `marathi` | `fda18674b928f7934f66c695ba494208344a6814` |
| `thennan-kathai` | `a63a171ffee75d12e6ef612c41b36262e5562a78` |

**All six source workspaces are now publicly represented. Source processing is not reopened** by
unrelated future movement of the poems source repository. No source PDFs are vendored; source identity
is filename + SHA-256 + size + scan count, held in the deterministic importer's provenance.

### Public ontology — the durable Poetry shape

Exactly **6** top-level Poetry LibraryWorks:

1. `idhayathai-thanthidu-anna` — standalone poem
2. `anaiya-vilakku-anna` — standalone poem
3. `marathi` — standalone poem
4. `thennan-kathai` — standalone poem
5. `kaalap-pezhaiyum-kavithai-saaviyum` — poetry **publication**, **58** internal reading units
6. `kalaignarin-kavithaigal` — poetry **publication**, **77** internal reading units

Four are standalone poems; two are poetry publications. Total internal Poetry publication units:
**135** (58 + 77). **These 135 units are NOT LibraryWorks and NOT collection members.** Collections
remain **1**; shelves remain **9**. **Do not describe the two Poetry publications as Reading Room
collections** — a publication is a single work whose reader exposes internal item routes; a collection
is a discovery layer over independent works (only the 1977 anthology is a collection).

### Route contract — durable

- Standalone poem: `/poems/<standalone-slug>` and `/poems/<standalone-slug>/source`.
- Publication: `/poems/<publication-slug>` and `/poems/<publication-slug>/source`.
- Direct publication item: `/poems/<publication-slug>/<item-slug>` — **not** `/items/<item-slug>`.
- Unknown publication children **fail closed** (404). No numeric aliases, no ordinal routes, no
  title-derived runtime slugging — item slugs come from the released registry.

### Cross-witness contract — durable

Exactly **TWO** witness relations exist. A witness relation states only that *another source
witness/version of the same canonical poem is available*; it is symmetric and endpoint-identity-driven.

| relation id | endpoints |
|---|---|
| `idhayathai-thanthidu-anna--kalaignarin-kavithaigal--item-01` | `/poems/idhayathai-thanthidu-anna` ↔ `/poems/kalaignarin-kavithaigal/give-me-your-heart-anna` |
| `thennan-kathai--kalaignarin-kavithaigal--item-02` | `/poems/thennan-kathai` ↔ `/poems/kalaignarin-kavithaigal/the-tale-of-the-southerner` |

The durable semantic rule is:

> **canonical poem identity != source-witness identity != publication membership.**

Neither relation claims identical text, byte equality, supersession, a corrected version, an
original/derivative hierarchy, or a preferred witness. Approved public wording, unchanged:

- **English:** `Another source witness of this same poem is available.`
- **Tamil:** `இதே கவிதையின் மற்றொரு மூல ஆதாரப் பதிப்பும் கிடைக்கிறது.`

The **Thennan** standalone witness retains its owner-directed, witness-local scan-151 editorial
exception (one omitted source term, recorded as **not reproduced**). **The anthology witness does NOT
inherit it**, and the omitted source word is never reproduced anywhere in code, tests, comments or
these control documents.

### P3 source-provenance state — கலைஞரின் கவிதைகள் Gate-3 title-witness accounting

Durable Gate-3 accounting, exposed on the publication `/source` page:

- **81** total title/group/item witnesses inventoried;
- **51** exact;
- **30** source-valid variants;
- **0** unresolved;
- **29** item-level variants + **1** group-only variant (group 1 counted once, not double-counted).

The one group-only variant is group 4: contents witness **கண்ணீர்க் கவிதை** vs canonical group title
**கண்ணீர்த் துளிகள்** — both witnesses retained. The five source-established anthology groups remain
provenance/structure, **not** five separate works. The eight pure structural scans remain
**32, 33, 70, 71, 372, 373, 392, 393**; group 1 retains shared scans **18–19** inside item 01.

### P4 payload regression contract — twelve exact SHA-256 pins

P4 froze every already-approved Poetry payload against accidental content or cross-witness mutation.
The P4 integrity validator hard-pins the SHA-256 of all **12** approved artifacts with exact equality
(not presence/length). These are the durable pins; **P5 does not rewrite these payloads**:

| artifact | SHA-256 |
|---|---|
| `anaiya-vilakku-anna/poem.json` | `22b26e59323a7ea1b6ca78b866178da76246e4ea3fc00423224ef9fa04f47fee` |
| `anaiya-vilakku-anna/provenance.json` | `8501373910610499fac48822c922e8e941461403863b7dd6444eedf8f50299e7` |
| `idhayathai-thanthidu-anna/poem.json` | `6833738340243833b712479e017f25294bb0e45b701d66d060a77f634c3e64f7` |
| `idhayathai-thanthidu-anna/provenance.json` | `d06a664052178762372d42727c95620a3c3a88159f85b56e43a095e8a401e930` |
| `marathi/poem.json` | `bd2f1f48e76b4a419dd0d86859b2c6dd8e43bb0ba3949242817d206b3eb3c0ed` |
| `marathi/provenance.json` | `e18bdbda5919bf8839581a0216cf6fafb797565f48ec769ac83e7777522eb3a7` |
| `thennan-kathai/poem.json` | `9d26512203004d794d9a859fc22905601714b6f84094d763294054c4dd8fb53b` |
| `thennan-kathai/provenance.json` | `2add1819a2309bbdb7a482f3ff8cff0150978e9e9ce11bdf58409edb34b13bf7` |
| `kaalap-pezhaiyum-kavithai-saaviyum/publication.json` | `d013e047922d9840a226eb1f2d08c7898758dea811bb9f9cac2f314fa3fb0b78` |
| `kaalap-pezhaiyum-kavithai-saaviyum/provenance.json` | `6a655ee198269d27ffcb90f0c4d9784d4d4180bf61a64569643dd7bbc821710c` |
| `kalaignarin-kavithaigal/publication.json` | `5b2a8fba7cd80e9082f51fd78459a8008dcb18232ddd4046435d1ffa74e95418` |
| `kalaignarin-kavithaigal/provenance.json` | `3321205441bdd2d6b5a86ffda2409dd5b74bc54ac14bea4fc7cd33f386a33dfa` |

The P4 layer is registered in Library CI as the named steps **Poetry witness relations — integrity
(Wave 4 P4)** and **Poetry witness relations — UI regression (Wave 4 P4)**, and the P4 **integrity**
validator is the final validator in the canonical `npm run validate` chain. Final P4 validator:
**131 assertions / 0 failed**; P4 witness UI regression: **60 checks / 0 failed**.

### Production boundary

Wave 4 moved the public census as follows:

| metric | pre-Wave-4 (Film-Songs close) | post-Wave-4 | delta |
|---|---:|---:|---:|
| Published works | 71 | **76** | +5 |
| Poetry works | 1 | **6** | +5 |
| Non-empty shelves | 9 | **9** | 0 |
| Collections | 1 | **1** | 0 |
| Fully-expanded discovery entries | 35 | **40** | +5 |
| Initially visible discovery entries | 27 | **32** | +5 |
| **Prerender-manifest routes** | 3126 | **3271** | +145 |
| Prerendered `.html` files | 3121 | **3266** | +145 |
| **Sitemap URLs** | 3117 | **3262** | +145 |
| `/poems/` URLs | — | **147** | — |

The prerender-manifest baseline is the independently measured **P1-before-Wave-4** count **3126**; the
coherent Wave-4 lineage is **3126 → 3132 → 3192 → 3271** across P1/P2/P3 (**+6 / +60 / +79 = +145**),
matching the public route additions **6 + 60 + 79 = 145** and the identical `.html` and sitemap deltas.
This is a different metric from the SUPERSEDED Film-Songs-era "Next build static-route count" (**3129**),
which stays recorded, unchanged, in its own historical checkpoint. Sitemap duplicates: **0**. The
`.html`, prerender-manifest and sitemap figures are three distinct measurements. All six top-level
Poetry works, both publication landing and `/source` pages, and
spot-checked items (a Kaalap item, an ordinary கலைஞரின் கவிதைகள் item, and both witness items 01/02)
returned 200 in production; two nonexistent publication children returned 404 (fail-closed); all four
witness-link directions resolved with the approved EN/TA note and no Kaalap relation; the Thennan
editorial exception is served on the standalone only and absent from the anthology item.

### Standing state after Wave 4

Wave 4 Poetry onboarding is **COMPLETE and CLOSED**. All six frozen Poetry workspaces are publicly
represented; the Wave-4 implementation backlog is **0**. Do not reopen the six Wave-4 Poetry works, add
Poetry works, alter Poetry content, change the witness relations or routes, or rewrite the 12 pinned
payloads without a newly discovered, source-backed regression. Validator-contract migration remains
**PAUSED**; native mobile remains **ON HOLD**; Reading Room Phase 2 is not authorized; no further
Poetry onboarding is authorized. The next major activity requires a new explicit owner authorization.

---

## Reading Room Wayfinding — Phase 0 + Phase 1 — ✅ COMPLETE and CLOSED

**The first architectural activity that onboarded no content.** Every number in the catalogue is the
same before and after: 71 works, 9 shelves, 39 Fiction works. What changed is how `/read` presents
them, and — in Phase 1 — that the archive can now say that thirty-seven of those works were published
together in one book.

### The problem

`/read` rendered every published work as its own card. At 71 works that was already a long scroll, and
the shape of the problem was worse than the size: **37 of the 39 Fiction cards were the 1977 anthology's
stories**, sitting as siblings of the standalone works with no way to see that they belonged to one
publication. The catalogue had no concept of a collection, so it had no way to say so.

Two phases, deliberately separated: relief first, architecture second.

---

### Phase 0 — shelf progressive disclosure

**Purpose:** immediate scroll relief with **no change to the archive ontology**. No model change, no
route, no data claim — a presentation cap only, and revertible in one commit.

| | |
|---|---|
| PR | **#67** `feat(reading-room): add shelf progressive disclosure` |
| Approved exact head | `13f313b04e4dcc89eb8130427d34b299b57d3be0` |
| Approved tree | `dc35249b6413b5fd6cf98521e11a54c2f62df8ff` |
| Squash merge | `1bc1123ecfcbdd181221cf34f558d3f7129d17e0` |
| Merged tree | `dc35249b6413b5fd6cf98521e11a54c2f62df8ff` — identical to the approved tree |
| Merged | 2026-09-02T15:14:40Z |
| Post-merge CI | `33647284338` — success |
| Production | deployment success, verified live |

**What it does.** Each shelf shows its first six entries; the rest move behind a native
`<details>`/`<summary>`. The shelf heading states the shelf's **full work count**, not the visible
count. Declaration order is preserved across the split.

**Native disclosure, deliberately.** `<details>` works with JavaScript unavailable, carries its own
keyboard and expanded-state semantics without a hand-written `aria-expanded` to fall out of sync, and
— unlike a `hidden` div — keeps the closed cards out of the tab order for free. A `hidden` attribute
would have stayed hidden without JavaScript, which is the opposite of progressive enhancement.

**Print.** A closed `<details>` would have dropped 41 of 71 works from a printed catalogue, which reads
as a shorter archive rather than a collapsed control. A narrow print rule keeps the whole catalogue on
paper and drops only the summary control, using both the modern `::details-content` mechanism and the
older slotted-children one so it does not depend on which the engine uses.

**Measured effect at that boundary:** initially visible cards **71 → 30**; works **71 → 71**;
fully-expanded cards **71 → 71**. Only Fiction and Speeches were over the cap.

#### The exact-head repair sequence — a durable lesson

Two heads were rejected before approval, and both rejections were correct:

| head | outcome |
|---|---|
| `6e1a626d3d69149c5f8cb5a51620797739790379` | **NOT approved** — the new 12px dark disclosure text measured ~**4.00:1**, under the 4.5:1 AA floor |
| `dfc0491da405b62c9f55cbc2a84ee858e5e10a54` | **NOT approved** — text fixed, but the authored dark focus ring still measured ~**2.5:1**, under the 3:1 WCAG 1.4.11 asks of a non-text indicator |
| `13f313b04e4dcc89eb8130427d34b299b57d3be0` | **APPROVED** — local accessible dark text and focus-ring treatments |

Both defects came from the control reusing tokens that are correct elsewhere in the app on other
backgrounds. The rule this establishes:

> **A pre-existing shared token does not exempt a NEW interactive control from accessibility review.**
> The control is new; where it sits is new; the measurement has to be taken there.

Both repairs were **local to the new control**. The shared `.focus-ring` utility, the Tailwind tokens
and every existing control were left untouched. This is a rule about new controls, **not** a claim that
the Reading Room as a whole is WCAG-clean — see the deferred issues below.

---

### Phase 1 — the 1977 anthology collection

**Purpose:** introduce the collection layer **without demoting member stories from independent works**.

```text
Collection / Publication
        │
        ├── Work        ← keeps its own id, route, provenance, citation identity, searchability
        ├── Work
        └── Work
              └── reading units, if that work has any
```

and emphatically **not**:

```text
one Work
  └── 37 reading units
```

The 37 stories remain **37 independent `LibraryWork` records** with their own `/stories/<slug>` and
`/stories/<slug>/source` routes. Belonging to a collection changes discovery density and nothing else.

| | |
|---|---|
| PR | **#68** `feat(reading-room): add 1977 anthology collection` |
| Final approved exact head | `ca217592cd2f8bd8c1eda51ef42524c8d16e3ea5` |
| Approved tree | `9d78706d263e5375638dd5e353f8fbc783a82020` |
| Squash merge | `1c6dcd81f0aa143a8e9b3162976c74dd18791058` |
| Merged tree | `9d78706d263e5375638dd5e353f8fbc783a82020` — identical to the approved tree |
| Merged | 2026-09-03T02:15:54Z |
| Post-merge CI | `33706978869` — success |
| Production | deployment success, verified live |

#### The benchmark collection

| | |
|---|---|
| id | `1977-kalaignar-karunanidhiyin-sirukathaigal` |
| Tamil title | `கலைஞர் கருணாநிதியின் சிறுகதைகள்` |
| kind | `anthology` — the only kind the model admits |
| shelf | Fiction |
| members | **37**, ordinals **1–37** |
| edition | `முதல் பதிப்பு: 1977` |
| publisher | `தமிழ்க்கனி பதிப்பகம், சென்னை-28` |
| route | `/collections/1977-kalaignar-karunanidhiyin-sirukathaigal` |

The collection page is an **archival navigation surface, not another story reader**: it duplicates no
story text and every row links to the member's own existing route.

**Route family.** `/collections/<id>`, statically enumerated from the declarations, unknown id 404s.
Deliberately **not** `/read/<collection>`: `/read/[id]` is the memoir's 391-chapter namespace, and a
collection segment would have shared it.

#### Source freeze

| | |
|---|---|
| source repository | `pugazg/kalaignar-short-stories` |
| frozen commit | `76135e1b5d504128c15be6bf59937716e5517d78` |
| collection tree | `d45434d46b1e779a880fff3d774d0fcb5833e477` |
| scan SHA-256 | `853032661482eaccb26c083a38d7aa75c081362d33c963c63e37d088bf20acb3` |

The commit alone is a weak guard — that repository advances for unrelated stories — so the
per-collection tree carries the freeze, the same way the Wave-3 essays' per-work trees do. **No repin.**

The archive registers the collection itself, in `collections/<id>/metadata/source.md` and
`indexes/story-inventory.md`: identity, edition, publisher, size, and a printed contents table giving
each story's ordinal, printed-page range and directory. Membership is validated from that structured
registration and is **never inferred** from `descEn`, `descTa`, title patterns, slug prefixes or shared
scan names.

#### Architectural rules established

**A. Membership is canonical in one place.** It lives in `LibraryCollection.members`. No `collectionId`
is added to `LibraryWork`: two stores of one fact can disagree, and the failure would be silent.

**B. Reverse membership is PLURAL.** The helper is `collectionsForWork(workId)` and returns a list —
**not** the stale singular `collectionForWork()`. A `Map<string, Collection>` would encode "at most one
collection per work", which the archive does not promise: a canonical work later found in another
publication is registered there as a further witness rather than duplicated, and a singular map would
silently drop one relationship. One collection exists today; the shape simply cannot lose data tomorrow.

**C. `memberCount` is not `unitCount`.** `memberCount` counts independent works in a collection;
`unitCount` counts reading units inside a single work (14 articles, 1,330 குறள், 391 chapters).
**37 stories are not 37 units of one work**, and no member gained a `unitCount` by joining.

**D. Member resolution fails closed.** `collectionMemberWorks()` does not filter unresolved members
away — it throws, naming the collection and the work id. Silent filtering would turn a declaration of
37 works into a clean-looking 36-row page, which is the worst kind of wrong because nothing on screen
says anything is missing.

#### The collection validator

`scripts/validate-collections.mjs` — **71 assertions, 8 groups, 0 failures**.

It is **distinct from** `scripts/validate-1977-short-stories.mjs`. That validator proves the 37 released
stories are faithful to the frozen source. This one proves what it cannot: that the **catalogue-facing
collection declaration equals the collection the source archive registers**. It re-derives its
expectation from the source's own registration and never reads `data/collections.ts` for it — a
validator and a declaration that read the same file would agree about a lie.

Negative-test history, recorded as it actually happened rather than as a combined total: the initial
collection validator had **15 mutations proven**; the review repairs added guards for reverse-membership
plurality and fail-closed resolution, and the implementation tests added accessibility and interaction
guards, each negative-tested when introduced.

**Validator contract after Phase 1: 3 registered · 13 pending · 16 total.** Migration remains
**PAUSED** — the new pending validator is not a resumption of it.

#### Exact-head review history — the second durable lesson

| head | outcome |
|---|---|
| `b48213de65b987bf8202f858969bbf07862f98d4` | **NOT approved.** Architecture and source declaration accepted in principle; six defects found: dark focus indicators below the non-text floor; inaccessible new dark hover text; newly introduced normal-text contrast failures; singular reverse membership encoding one collection per work; member resolution silently filtering unresolved works; and a printed collection page losing its own identity because the global print rule hid `<header>`. |
| `36720ce81b3de8675c9e3f76f20ab7fbe0a0bcf2` | **NOT approved.** All six repaired, but the new title hover kept `group-hover:text-marina` with no dark counterpart. That class is not light-mode-only — it applies in dark too, so Marina still won there. |
| `ca217592cd2f8bd8c1eda51ef42524c8d16e3ea5` | **APPROVED FOR MERGE.** Both titles state `group-hover:text-marina dark:group-hover:text-night-text`. |

The second rejection is the one worth keeping:

> **Where state or theme variants coexist, proving a bad class is ABSENT is not enough.** The first
> repair removed `dark:group-hover:text-marina-light` and the guard passed — while an unqualified
> `group-hover:text-marina` quietly took its place in dark mode. Where correctness depends on an
> override, the test must positively prove the required good state is **PRESENT**.

#### Print and no-JS

The collection's identity header is archival content, not chrome, so it is exempted from the generic
rule that hides page headers — placed after that rule and more specific. Printing the collection page
keeps the title, edition, publisher, count and all 37 member rows; the Back link is hidden through the
existing `data-print="hide"` convention. The 37-row inventory is server-delivered and depends on no
search or filter JavaScript.

#### Production verification

`/read`: works **71** · shelves **9** · collections **1** · fully-expanded entries **35** · initially
visible **27**. Fiction: **39 works**, **3 discovery entries** (1 collection + 2 standalone works), no
disclosure — the disclosure disappears because 3 < 6, not because anything tests for the Fiction shelf.
The three entries are `கலைஞர் கருணாநிதியின் சிறுகதைகள்`, `பலிபீடம் நோக்கி`, `கிழவன் கனவு`. Speeches keeps
its Phase-0 disclosure: 14 entries, 6 visible, 8 deferred.

Collection page: 37 unique members, ordinals 1–37 in source order, first `புகழேந்தி`, last
`நுனிக்கரும்பு`, `கிழவன் கனவு` correctly excluded, 37 printed-page ranges, no duplicated story body,
unknown collection id 404.

Story identity, proved as a full inventory rather than by sampling: `STORY_SLUGS` **38** · story sitemap
URLs **76** · **37/37** anthology reader routes 200 · **37/37** anthology `/source` routes 200.

### Standing state after Reading Room Wayfinding — superseded where noted

- **Wave 4 readiness census / selection is now AUTHORIZED BY OWNER but NOT STARTED.** This supersedes
  the earlier “Wave 4 NOT AUTHORIZED” status. **Wave 4 implementation is NOT YET AUTHORIZED**; the
  census/selection must report its chosen coherent batch before any implementation begins.
- **Phase 2 discovery search is NOT started and NOT authorized.** Phase 1 deliberately left the
  registries clean enough for it; that is preparation, not permission.
- **Chronology, Tamil-first sorting and `/read/browse` remain unstarted and unauthorized.**
- **No second collection is authorized.** Drama's Naanmani Maalai is explicitly *not* modelled: its four
  plays share a scan SHA-256 and a prose note and nothing structural, which is not enough to declare
  membership under the source-first rule. Essays publications are not collections either — an Essays
  publication is one work whose articles are reading units. Murasoli's volume hierarchy has not had its
  design pass.
- **Film Songs formal control close-out is recorded by the dedicated section below.** If this file is
  read from the unmerged close-out branch, live control `main` still wins; once this PR is on `main`,
  Film Songs is durably COMPLETE and CLOSED.
- **Validator migration remains PAUSED.**
- **Native mobile remains ON HOLD.**
- **Manimagudam** and **`kalaivanar-nsk-memorial-day-audio-06`** are never auto-selected.

### Known follow-up debt — recorded, not fixed here

Two pre-existing issues were found while measuring Wayfinding. Neither is a Wayfinding defect and
neither is fixed by it.

- **Digital Library theme bootstrap.** `/read` and `/collections` carry dark-mode classes, but a direct
  load of a Digital Library route does not mount the component that activates the site's `.dark` class —
  that component is mounted on `/` alone. Phase-1 dark states were verified by forcing the project's
  actual dark class. Pre-existing and site-level.
- **Pre-existing work-card contrast.** The existing work cards' secondary text still carries older
  low-contrast tokens. The Phase-1 collection card and page were fixed locally; **no claim is made that
  the existing Reading Room is WCAG-clean**, and no work-card restyle is authorized.

---

## Kalaignar Film Songs — E1–E4 — ✅ COMPLETE and CLOSED

**கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs.** The implementation was intentionally staged
through deterministic data, CI, reader, catalogue and sitemap work before this separate formal
control closure. No implementation change is part of this section.

**Control-merge boundary.** This section describes the durable state this control PR establishes. If
read from the unmerged branch, closure is still proposed and live control `main` remains authoritative.
Once this exact documentation tree is merged to control `main`, Film Songs is formally COMPLETE and
CLOSED and needs no further close-out activity.

### Source freeze and integrity

| | |
|---|---|
| Source repository | `pugazg/kalaignar-cinema-works` |
| Source path | `works/kalaignar-thirai-isai-paadalgal` |
| Frozen source commit | **`d6f3128381235e80891cc6647d19464b838f4103`** |
| Controlling source | `TVA_BOK_0065867` |
| Controlling scan SHA-256 | **`f0beac14c33ffc73c0231bd54ca57ec4093eef6e85072bd68ce48f7b5e258b05`** |
| Earlier witness | `TVA_BOK_0065773` |
| Earlier-witness SHA-256 | **`56d414a65a61a73b990632eadc17a3b1efdc764d47f64b851060c161a3f98e3b`** |
| Reading Room payload SHA-256 | **`8ec0e25f7fc1f1a9750d370ccbef5dd07caa66629a3dfacb8425bbeebd08fcce`** |
| Evidence-register SHA-256 | **`9aa03e32f2bf2a2fa491f6995ed6d455f36d74aa1294cf4fc5763d4afb2f27de`** |
| Source-input aggregate | **`9d499beb2c54c692cf972e5fe269c7e7f21d3bafa07a5d4c76d2bf9acb027935`** — 4 files |

At close-out preparation, live `pugazg/kalaignar-cinema-works/main` itself still resolves to the exact
frozen implementation pin. **No repin occurred.** The earlier 1989 witness is authorship evidence only
and contributes **no lyric text**.

### Final corpus

**23 films · 54 numbered lyrics · 1105 paired Tamil/English line-cues · 8 cross-page songs.**

Cross-page song numbers: **9, 19, 23, 24, 36, 37, 51, 52**. Songs **001–054** exist exactly once.
The front-matter incipit `ஆளப்பிறந்தவன் தமிழன் அவனிதனிலே` is named editorially but has no numbered
lyric body in the corpus; it is **not** a 55th song and must never become one.

### Authorship certainty is not display eligibility

This is the central Film Songs contract:

| fact | count |
|---|---:|
| public/displayable numbered lyrics | **54** |
| established Kalaignar authorship | **48** |
| unresolved individual authorship | **6** |
| notice-required | **6** |

The unresolved records are exactly songs **013–018** in **அம்மையப்பன்**. They remain publicly
displayable because they are part of the controlling source's numbered corpus, but they carry **no
positive Kalaignar-authorship claim**. `unresolved` means the source does not establish authorship in
either direction — it never means “not Kalaignar's”, “established other”, or rejected attribution.

The source-controlled notice group is **`ammayappan-unresolved`**, covering exactly songs 013–018.
Its Tamil and English text is imported from the source contract. A notice-required song may not render
without its notice; resolution fails closed. Song **012** is separately established from the earlier
witness and correctly receives **no** unresolved notice.

### E1–E4 implementation history

| stage | implementation PR | final reviewed head | squash merge | durable purpose |
|---|---:|---|---|---|
| **E1** | #57 | `912dcc759d4a8951c0899e5378d8a4181a304a42` | `c5fae2abac15d3b1e4f07d22862c4e865596d870` | deterministic source-pinned data import + validator |
| **CI gate** | #58 | `494a833bb51a7962713ae5aa319838a5621dd222` | `1cd8c66344660d0d8e70b9f057ad577dc6a76cc7` | wire Film Songs into explicit Library archival-validator CI |
| **E2** | #59 | `82c1198632a77659d1c5d6ad4a608324e4edd660` | `5580fe5c26f76828ff8f6f1351197381a4577ea0` | public film→lyric reader |
| **E3** | #60 | `502f31a1f617510883209d4548179463d0aaff23` | `780d1e28e9cacd073a5d44073243b87642c7b06d` | Reading Room catalogue exposure |
| **E4** | #61 | `a97fd4c8fed7fedf8946a514e3d40e8a2a300d7f` | `2712080873d51e7cfb020295e20d4c32da803a7c` | sitemap exposure |

#### E1 — deterministic data + public/internal boundary

E1 established the source-pinned registry and lyric files and a source-linked validator. Its first
reviewed design put archival `provenance.json` under Next.js `public/` and merely described it as
“build-time only”. Independent review correctly rejected that: **everything under `public/` is a
served asset regardless of what a comment calls it.**

The accepted repair moved archival provenance to:

`data/internal/thirai-isai-paadalgal/provenance.json`

and removed scan/page-level per-song provenance from the served lyric records. Nothing archival was
lost: the internal record retains source repo/path/commit, both witness hashes, evidence-register and
source-input hashes, all source paths, page mappings, contents-title variants, printed music/voice
credits, archival attribution and verification states. The public tree carries reader-needed data only.

> **Durable rule: filesystem placement is the real public/private boundary.** A label cannot make a
> file private if the framework serves the directory it occupies.

Final Film Songs validator: **155 assertions / 0 failed**.

#### CI gate — explicit validation really runs

`npm run validate` already knew the work, but the Library CI `archival validators` job invoked works
through explicit per-work steps and initially had no Film Songs step. PR #58 closed that gap without
changing product behaviour. Film Songs uses its own source-checkout directory because Manohara,
Tirumbippaar and Film Songs pin the same source repository at different historical commits; one
checkout cannot satisfy all three, and the same-directory/same-pin guard was not weakened.

The named current CI step remains **Kalaignar Film Songs**. Validator-contract migration remains
**PAUSED**; the Film Songs validator is not migrated merely because it is active in CI.

#### E2 — film → lyric reader

Public routes:

- `/cinema/thirai-isai-paadalgal` — one landing grouping **23 films**;
- `/cinema/thirai-isai-paadalgal/song-001` … `/song-054` — **54 lyric pages**.

Total public Film Songs reader routes: **55**. There are **no per-film routes**, **no `/source` route**,
and no `song-055`. Films are grouping anchors on the landing, not pages.

No byline is rendered per lyric. The six unresolved lyrics render the source-controlled notice in the
same active language as the lyric body; the other 48 do not. Previous/next navigation stays within the
current film.

Independent review also tightened the server→client payload: neighbour props became only
`{ slug, titleTa }`, and notice props only `{ noticeTa, noticeEn }`. That was **payload minimisation and
surface discipline**, not a secrecy finding; many of the removed summary values already exist in the
public registry.

#### E3 — catalogue

The final catalogue entry is one **Cinema Writing** work:

| field | final value |
|---|---|
| id | `kalaignar-thirai-isai-paadalgal` |
| slug | `thirai-isai-paadalgal` |
| title | `கலைஞர் திரை இசைப் பாடல்கள்` / `Kalaignar Film Songs` |
| subtype | `film-song-collection` |
| reader structure | `film-song` |
| href | `/cinema/thirai-isai-paadalgal` |
| Tamil | complete |
| English | complete |
| English kind | `project-created` |
| `unitCount` | **54 songs** |

**The 54 is a corpus count, not an authorship count.** It must never be paraphrased as “54 songs
written by Kalaignar”.

Catalogue `rights` is deliberately absent. Applying the nationalisation status across this 54-song
collection would silently treat the six unresolved songs as Kalaignar-authored for rights purposes —
resolving an authorship question through a rights field. **Display eligibility, authorship certainty and
rights are three separate facts.**

`provenanceHref`, public `sourceRepo`, `sourcePath`, `sourceCommit` and `edition` are absent by design;
there is no public Film Songs source page. The internal provenance record remains the deterministic
validation boundary.

#### E4 — sitemap

E4 adds exactly **55** Film Songs sitemap URLs: the landing plus 54 lyric routes. It advertises no
`/source`, per-film page, fragment URL or Song 55. Slugs come from the same released registry that
drives `generateStaticParams`, not a numeric reconstruction.

The first E4 comment made a wrong argument for a correct design: it claimed a 001–054 numeric loop
would invent the unnumbered editorial incipit. It would not. The comment was repaired without changing
behaviour.

> **Correct durable reason:** the registry is the authority for the routes that actually exist. A
> future numbering gap, renumbering or other route-set change must not leave the sitemap describing
> pages the router no longer generates.

### English provenance

The English layer is **complete** and **project-created** from the verified Tamil derivative. It is
not an official translation, not a historical published translation and not a source witness. Tamil
remains the authoritative lyric-text layer; the earlier 1989 witness serves only the stated authorship
evidence role.

### Current regression state

At the current post-Wayfinding implementation boundary, Film Songs remains one of **4 Cinema Writing
works** and all global metrics remain **71 works / 1 collection / 9 shelves / 35 fully-expanded
entries / 27 initially visible / 3129 static routes / 3121 `.html` / 3117 sitemap URLs / 0 duplicates**.
This formal close-out changes documentation only.

The live validator remains `scripts/validate-thirai-isai-paadalgal.mjs`, **155 assertions**, invoked by
both `npm run validate` and Library CI. The validator contract remains **3 registered / 13 pending /
16 total**, migration **PAUSED**.

### Standing state after Film Songs formal close-out

- **Film Songs E1–E4 implementation: COMPLETE, published and production-verified.**
- **Film Songs formal control close-out: COMPLETE and CLOSED once this control PR is merged.**
- **Wave 4 readiness census / selection: AUTHORIZED BY OWNER, NOT STARTED.** This is now the next
  bounded activity.
- **Wave 4 implementation: NOT YET AUTHORIZED.** Census/selection must report the chosen coherent batch
  first; implementation requires a later explicit authorization.
- Phase 2 Reading Room search, chronology, Tamil-first sorting, `/read/browse` and a second collection
  remain unauthorized.
- Validator migration remains **PAUSED**; native mobile remains **ON HOLD**.
- Manimagudam and `kalaivanar-nsk-memorial-day-audio-06` remain never-auto-selected special cases.
- Existing theme-bootstrap and WorkCard-contrast debt remains recorded, not authorized by this closure.

---

## Bulk Onboarding Wave 3 — Essays & Articles / three-publication batch — ✅ COMPLETE and CLOSED

**The third bulk-onboarding activity.** Three release-complete publications from `pugazg/kalaignar-essays`
were published together on the existing Essays & Articles shelf:

1. **கயிற்றில் தொங்கிய கணபதி** / *Ganapathi Who Hung from the Rope* — 1 article, 17 scans;
2. **உணர்ச்சிமாலை** / *Garland of Emotion* — 10 articles, 50 scans;
3. **திராவிட சம்பத்து** / *Dravidian Wealth* — 2 articles, 16 scans, damaged/out-of-order source.

Implementation is merged and production-verified. This section is the durable merged control closure.

### Implementation identity and exact-head gate

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#66` |
| First reviewed head — **REJECTED** | `d50aefae5cc5a665230a4185aab43d16c7dfeb81` |
| Exact independently approved head | **`c4f40f7f77a115700915f17e65c2a2a1ddf54bbd`** |
| Squash merge / implementation `main` | **`c4660c49edb20895d11751e4454942e46e8b0951`** |
| Merged tree | **`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`** |
| Parent/base | `4fd45a92663abbe70ff0c0a605168314cd36e44c` |
| Merged | 2026-09-02T08:07:00Z |
| Changed files | **23** — 15 implementation/CI and 8 generated |
| Diff size | **+13057 / -166** |
| Post-merge Library CI | run **`33607016982`** — success |
| Production deployment | Vercel — **success** for `c4660c49…` at 2026-09-02T08:09:30Z |

The approved PR-head tree and the squash-merged `main` tree are **exactly the same tree SHA**:
`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`. The squash introduced no implementation drift.

#### Exact-head lesson — green CI is not an approval substitute

The first candidate head `d50aefae…` had green CI but **was not approved**. Independent exact-head
review found that `app/essays/[slug]/source/page.tsx` still emitted a hard-coded source-page metadata
string inherited from சக்கரவர்த்தியின் திருமகன், falsely telling every Wave-3 publication that it had
a first-edition/reprint distinction, a 14-article map and rights. The visible source component had been
generalized, but the route metadata had not.

The repair made `/source` metadata data-derived from each publication's own provenance, added validator
coverage for that exact defect class, and raised the Wave-3 validator from 472 assertions / 6 groups /
20 negative tests to **510 assertions / 7 groups / 23 negative tests**, all passing. The repaired head
`c4f40f7f…` was independently reviewed and **APPROVED FOR MERGE**; only that SHA was merged.

**Standing rule strengthened by Wave 3:** successful build/CI does not replace exact-head review, and
route metadata is part of source-form correctness. If a reviewed head changes, approval is void.

### Source freeze

| | |
|---|---|
| Source repository | `pugazg/kalaignar-essays` |
| **Frozen implementation pin** | **`6814e979fd3c2cefa14cbeb17eeec28164ce28f5`** |
| `publications/kayittril-thongiya-kanapathi` | **`ca1c92591b9389e60d44b9683af849e3a682e528`** |
| `publications/unarchchimaalai` | **`f49d77a0733ca75f7a96fb6a1cf4631e375b05d0`** |
| `publications/thiraavida-sampaththu` | **`fe0f6ea0482ac2cd0e8c4558edd3b452e249dbdd`** |

Source identities at the frozen release:

| work | controlling PDF | SHA-256 | scans |
|---|---|---|---:|
| கயிற்றில் தொங்கிய கணபதி | `TVA_BOK_0064013_கயிற்றில்_தொங்கிய_கணபதி.pdf` | `927d05fb27a2545d6732acd9bf8bde04dba2d22546d171b502703a773b40f45a` | 17 |
| உணர்ச்சிமாலை | `TVA_BOK_0063821_உணர்ச்சிமாலை.pdf` | `d2d45de049505218fd612bf71949135e34ecb317ffb5d003dfe59a3a0608461d` | 50 |
| திராவிட சம்பத்து | `TVA_BOK_0064196_திராவிட_சம்பத்து.pdf` | `09d567abb30a0beacc1efd1e1fb757f01da93968f5582c9b1b8859b87dac2165` | 16 |

The source repository is intentionally fast-moving because **`publications/ina-muzhakkam/` is active**.
At control-close-out preparation time its live `main` was
`8d3b3e6792f6b3a7783ff3621f4d5c8e3e9be4d4` (`Advance Ina Muzhakkam P5 frontier through scans 43-44`).
The three Wave-3 work trees at that newer live head were re-computed and remained **exactly** the frozen
values above. Therefore unrelated future source-`main` movement does not repin or reopen Wave 3.

**`இன முழக்கம்` was explicitly excluded** from Wave 3 because it was source-active. It is not the
fourth work in this batch and is not automatically selected for any later wave.

A second source-status lesson is retained for **கயிற்றில் தொங்கிய கணபதி**: its older
`PUBLICATION_COMPLETION_REVIEW.md` ends with historical wording that English work may begin, but the
later authoritative `translations/en/RELEASE_REPORT.md` records **E7 PASSED / English release gate
closed**. A stale earlier status paragraph must never override a later release authority.

### Source-form architecture shipped

The existing Essays implementation was still partly a one-publication model. Wave 3 generalized only
what the three sources required:

- source-page and page-transition printed numerals are nullable — absence stays absence;
- article coverage is ordered `scanRuns[]`, not a single `{from,to}` range;
- printed pagination is a discriminated `range | partial | none` witness;
- article numbering distinguishes printed contents numbers from archive reading ordinals;
- first-edition, controlling-edition and publication-wide printed-page facts are optional/source-led;
- `projectRights` is optional — no rights block was invented for the three Wave-3 pamphlets;
- damaged/out-of-order sources can carry explicit `readingOrder` and `physicalCondition` provenance;
- landing, article, source UI and all three route metadata families are source-form-aware through
  `lib/essay-source-facts.ts`.

The importer is deterministic and pinned: one shared Wave-3 Essays parser/core plus explicit work
declarations, historical source commit + per-work tree guards, no source PDFs vendored and byte-identical
reruns from clean state.

### திராவிட சம்பத்து — source order must remain non-normalized

This publication is the structural stress case and must not be simplified later:

- article 1 **திராவிட சம்பத்து**: ordered scan runs **`5–6, 13–16`**;
- article 2 **ஐயர் அறிவிக்கிறார்!**: ordered scan runs **`12, 3`** — the descending order is deliberate;
- reconstructed physical reading order:
  **`1 → 2 → 9 → 10 → 5 → 6 → 13 → 14 → 15 → 16 → 7 → 8 → 11 → 12 → 3 → 4`**;
- no visible printed pagination is invented;
- torn/missing source text is **not reconstructed**.

Production preserves these facts. The visible `/source` body summarizes the damage/reading-order
provenance; the exact reconstruction policy and literal arrow sequence are carried in the deployed
provenance record rather than rendered as full visible rows. Record this distinction precisely — the
facts are **available**, but not every datum is printed in the visible source-page body.

### Production boundary

Wave 3 moved the public census as follows:

| metric | pre-Wave-3 | post-Wave-3 | delta |
|---|---:|---:|---:|
| Published works | 68 | **71** | +3 |
| Essays & Articles works | 1 | **4** | +3 |
| Non-empty shelves | 9 | **9** | 0 |
| **Next build static-route count** | 3109 | **3128** | **+19** |
| Prerendered `.html` files | 3101 | **3120** | **+19** |
| **Sitemap URLs** | 3097 | **3116** | **+19** |

The `.html`, static-route and sitemap figures are **three distinct measurements** even though each
happened to move by +19. Sitemap duplicates: **0**. The Essays route family contains **35** URLs after
Wave 3: 19 from the new batch plus 16 from சக்கரவர்த்தியின் திருமகன்.

Production verification checked **all 19/19** new Wave-3 routes individually and all returned 200.
The existing 16 சக்கரவர்த்தியின் திருமகன் routes also remained 200.

The previously rejected metadata defect was verified absent in production:

- கயிற்றில் தொங்கிய கணபதி `/source`: single article; no 14-article, reprint, 2018 or rights claim;
- உணர்ச்சிமாலை `/source`: 10-article map; no 14-article, reprint or rights claim;
- திராவிட சம்பத்து `/source`: 2-article map + damage + reconstructed-reading-order metadata; no
  14-article, reprint or rights claim;
- சக்கரவர்த்தியின் திருமகன் `/source`: its real 14-article map, first-edition/reprint distinction and
  established rights record remain intact.

Other production fidelity checks: உணர்ச்சிமாலை has 10 article navigation entries and excludes scan 50's
மணமகள் advertisement; கயிற்றில் தொங்கிய கணபதி publishes one article and excludes advertisement scans
16–17. No source absence was normalized into an invented publication fact.

### Validator and reference regression

Final Wave-3 batch validator: **510 assertions · 7 groups · 0 failed**. **23/23 negative tests proven**,
including wrong pin/tree drift, missing/duplicate article, quotation/voice corruption, imported
advertisements, invented pagination/reprint/rights, rejection of the intentionally frozen
`strict-reviewed` vocabulary, flattening `5–6, 13–16` to `5–16`, sorting `12, 3` to `3, 12`, replacing
the reconstructed reading order with numeric scan order, accidental Ina Muzhakkam inclusion, reference
regression and restoration of the rejected hard-coded source metadata.

**சக்கரவர்த்தியின் திருமகன் is the regression benchmark.** Its generated JSON changed shape because
the shared types generalized, so byte identity was not claimed. Semantic equivalence was proved:
14 articles; identical Tamil and English reading blocks; same slugs/order/titles/contents witnesses and
page transitions; 1956 first edition; 2018 controlling reprint; printed page count 80; established
rights record; mixed-voice behavior intact. Its validator passed **188 assertions, 0 failed** and its
16 production routes remained healthy.

### Standing state after Wave 3 — historical at this point

At the Wave-3 close-out, Wave 4 was not yet authorized and Film Songs formal closure was still pending.
Those two statuses are now superseded by the CURRENT Film Songs section above. The durable historical
facts remain: validator migration was **PAUSED**, native mobile **ON HOLD**, Manimagudam required its
own readiness gate, and `kalaivanar-nsk-memorial-day-audio-06` was a separate source-active archive.

**Do not reopen Wave 3** merely because the Essays source repository continues to advance for other
publications.

---

## Bulk Onboarding Wave 2 — Fiction / 1977 short-story anthology — ✅ COMPLETE and CLOSED

**The second bulk-onboarding activity, and the first to run the exact-head sequence correctly from
end to end.** 37 short stories published together on the Fiction shelf from one frozen source release.
Implementation PR [#65](https://github.com/pugazg/kalaignar-autobiography/pull/65), squash merge
**`4fd45a92663abbe70ff0c0a605168314cd36e44c`**, merged tree
**`0a5029273e018482176502791ab440563e52e6a2`**, merged **2026-09-02T03:28:20Z**, 83 files. Verified in
production on 2026-09-02.

**Do NOT reopen this wave** merely because source `main` later moves.

### The batch

37 stories from **கலைஞர் கருணாநிதியின் சிறுகதைகள்** (1977) — shelf **Fiction**, reader family
**story**.

The batch is coherent because all 37 share **one anthology, one source release, one shelf, one reader
family, and the same completed upstream release state.**

**கிழவன் கனவு was explicitly excluded**: it is a separate, earlier source, it was already published,
and it is this wave's regression benchmark. **It is not the 38th anthology story** and must never be
described as one.

### Implementation identity

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#65` |
| Exact independently reviewed head | **`2ba1ee3aaa5078ddc60463e45cb00bca36ae4f8d`** |
| Squash merge | **`4fd45a92663abbe70ff0c0a605168314cd36e44c`** |
| Merged tree | **`0a5029273e018482176502791ab440563e52e6a2`** |
| Merged | 2026-09-02T03:28:20Z |
| Changed files | **83** — 74 generated (37 × `story.json` + 37 × `provenance.json`) and 9 implementation/CI files |
| Post-merge Library CI | run **`33587162687`** — success |

**Wave 2 followed the intended exact-head sequence in full:** the implementation PR was opened → the
exact current head was independently reviewed → ChatGPT gave APPROVED FOR MERGE for `2ba1ee3a…` → the
head did not change → merge → production verification → and only then this control close-out. The
merged tree was confirmed byte-identical to the approved head's tree.

**This is the standing process, and it is the deliberate contrast with Wave 1's historical process
defect**, where a PR was merged before its final repaired head had been approved. See the Wave-1
process-lesson section below; that remains recorded, and remains not a precedent.

### Source freeze

| | |
|---|---|
| Source repository | `pugazg/kalaignar-short-stories` |
| **Frozen pin** | **`76135e1b5d504128c15be6bf59937716e5517d78`** |
| Controlling source | `TVA_BOK_0064142_கலைஞர்_கருணாநிதியின்_சிறுகதைகள்.pdf` |
| SHA-256 | `853032661482eaccb26c083a38d7aa75c081362d33c963c63e37d088bf20acb3` |
| Physical scans | **260** |
| Story block | scans **10–259**, printed story pages **1–250** |
| Scan **260** | **back cover — excluded from story text** |
| Collection tree | **`d45434d46b1e779a880fff3d774d0fcb5833e477`** |

**All 37 work trees were frozen and guarded individually.** A shared repository pin does not collapse
37 works into one provenance identity: each tree was checked on its own, by both the importer and the
validator, and per-work drift guards are enforced on every run.

| # | slug | title | English | printed | scans | frozen tree |
|---:|---|---|---|---:|---:|---|
| 1 | `pugazhendhi` | புகழேந்தி | Pugazhendhi | 1–6 | 10–15 | `7489e5ddb8b35d8a2ef41600bccfc9b291332845` |
| 2 | `nalayini` | நளாயினி | Nalayini | 7–14 | 16–23 | `784d833f69f2ff741d9874ae864555366ccb3e21` |
| 3 | `sabalam` | சபலம் | Sabalam | 15–21 | 24–30 | `fc02d6b8c288bbdd5f03fe3fe51622a383228a60` |
| 4 | `aattakkavadi` | ஆட்டக்காவடி | Aattakkavadi | 22–29 | 31–38 | `f54a7197c661ad91b631ec0cba52d8b8747a9ba1` |
| 5 | `kuppai-thotti` | குப்பைத்தொட்டி | Kuppai Thotti | 30–37 | 39–46 | `e8d5cf43fb200e95b85a637a4d49bd263f2ef5cc` |
| 6 | `santhana-kinnam` | சந்தனக்கிண்ணம் | Santhana Kinnam | 38–47 | 47–56 | `d154416ac269678f5984ff665dc2e97b106abb69` |
| 7 | `sangilichami` | சங்கிலிச்சாமி | Sangilichami | 48–59 | 57–68 | `3b2f3c02d19757d956649e4eedf75ca33cd76f6f` |
| 8 | `gangaiyin-kadhal` | கங்கையின் காதல் | Gangaiyin Kadhal | 60–63 | 69–72 | `c25e85fcfff59e93e911a34ac1817fd24e7f81c3` |
| 9 | `thaaymai` | தாய்மை | Thaaymai | 64–74 | 73–83 | `bcd5bf6b06c9b564864abe25e75c70599fe0e9e6` |
| 10 | `thappivittargal` | தப்பிவிட்டார்கள் | Thappivittargal | 75–82 | 84–91 | `bd0b1c983be714c5997894f0b53a5a9c895e07ee` |
| 11 | `thappavillai` | தப்பவில்லை | Thappavillai | 83–92 | 92–101 | `ce80ac8bb1e8fe89d09952a2dbe7d20f43abf371` |
| 12 | `aatharikkirar` | ஆதரிக்கிறார் | Aatharikkirar | 93–98 | 102–107 | `fe4fabd9ca0a76a84ca9724cd162b136e1017c84` |
| 13 | `iragasiyam` | இரகசியம்! | Iragasiyam! | 99–102 | 108–111 | `0baab51100f49e438e5d6a3464328b626a34f6f7` |
| 14 | `munnuru-rupai` | முந்நூறு ரூபாய் | Munnuru Rupai | 103–105 | 112–114 | `64d6d69ca597efca0a60bd60d1bfc8254b717042` |
| 15 | `ezhai` | ஏழை | Ezhai | 106–109 | 115–118 | `35e0f00154c5536cf60bc561d77b298d993ab1da` |
| 16 | `originalil-ullapadi` | ஒரிஜினலில் உள்ளபடி | Originalil Ullapadi | 110–116 | 119–125 | `6596ce8d2c660d04f1f1d9b771399efc0be7c60a` |
| 17 | `panangulai` | பனங்குலை | Panangulai | 117–121 | 126–130 | `38335b1d9f11a1191f0864e84c19ab20d4564481` |
| 18 | `seththaval-kathai` | செத்தவள் கதை | Seththaval Kathai | 122–130 | 131–139 | `9a70ee7fe99326260a5bc775b02c351c4fd5744f` |
| 19 | `pretha-visaranai` | பிரேத விசாரணை | Pretha Visaranai | 131–136 | 140–145 | `d1bbb45d3462de55047f9f26e1e705cafc32693b` |
| 20 | `kandathum-kadhal-ozhiga` | கண்டதும் காதல் ஒழிக! | Kandathum Kadhal Ozhiga! | 137–141 | 146–150 | `1903720fecd0b53c009da637f023a7914d76b5a9` |
| 21 | `aalamarathup-puraakkal` | ஆலமரத்துப் புறாக்கள் | Aalamarathup Puraakkal | 142–146 | 151–155 | `d09e93781afa679d35349e93555a4c110664fbe7` |
| 22 | `thothukkili` | தொத்துக்கிளி | Thothukkili | 147–151 | 156–160 | `71f04f3621f4c40e8b6ca8216dd9910b07d1fddd` |
| 23 | `kadhal-kaditham` | காதல் கடிதம் | Kadhal Kaditham | 152–156 | 161–165 | `0beca693da89e23a456f11cfd1f2a7e21e0e8b45` |
| 24 | `kannadakkam` | கண்ணடக்கம் | Kannadakkam | 157–163 | 166–172 | `e14d7afb2675cffe463f834eae616667894701de` |
| 25 | `vazha-mudiyathavargal` | வாழ முடியாதவர்கள் | Vazha Mudiyathavargal | 164–171 | 173–180 | `b03f83a712a6fcbfb98451ecc73afd23cf402bb9` |
| 26 | `abagya-chinthamani` | அபாக்ய சிந்தாமணி | Abagya Chinthamani | 172–179 | 181–188 | `ba2ac25f5e45629ac02d43e13625e51b50353de2` |
| 27 | `palaivana-roja` | பாலைவன ரோஜா | Palaivana Roja | 180–184 | 189–193 | `82be76bbc27a860681597b440f3f0d33581a6001` |
| 28 | `puratchip-padam` | புரட்சிப் படம் | Puratchip Padam | 185–189 | 194–198 | `78fcda9d34ca9a36fd280e7a65d7c31aa3f903da` |
| 29 | `thidukkidum-kathai` | திடுக்கிடும் கதை | Thidukkidum Kathai | 190–195 | 199–204 | `e6eea7e253f33f029f1c64958ea184dbd07423e0` |
| 30 | `kadaisi-kattam` | கடைசிக் கட்டம் | Kadaisi Kattam | 196–201 | 205–210 | `4176f3cc1e2797938a4a26d8acb11cc816105261` |
| 31 | `ayyo-raja` | அய்யோ ராஜா! | Ayyo Raja! | 202–208 | 211–217 | `9bdc09d0a9f09ffddad6e651d6846ca5014690c9` |
| 32 | `visham-inidhu` | விஷம் இனிது | Visham Inidhu | 209–215 | 218–224 | `1e0a876ad13c6fb48c91ff7f14d51be9318bafb9` |
| 33 | `veniyin-kadhalan` | வேணியின் காதலன் | Veniyin Kadhalan | 216–221 | 225–230 | `49ea97a0025eca96ae6895764df86188480933e0` |
| 34 | `amirthamathi` | அமிர்தமதி | Amirthamathi | 222–229 | 231–238 | `6392d447a9fbd0822452f5040f6a524d48128222` |
| 35 | `sumanthaval` | சுமந்தவள் | Sumanthaval | 230–240 | 239–249 | `e84057745986e7e6712e4342f12a149c7d113c77` |
| 36 | `siddharthan-silai` | சித்தார்த்தன் சிலை | Siddharthan Silai | 241–243 | 250–252 | `c82f565ccdae0a7882e5b3942ba28bae38ac8792` |
| 37 | `nunikkarumbu` | நுனிக்கரும்பு | Nunikkarumbu | 244–250 | 253–259 | `5a20d7cfcdef25999ca74d17e110679176d76ef7` |

Story 29's tree is the **corrected** one, `e6eea7e253f33f029f1c64958ea184dbd07423e0` — see below.

### ⚠️ The Story-29 source defect — stop, repair upstream, re-freeze

**The most important lesson of Wave 2.**

The initial Wave-2 source candidate was **`a9b333f12128686785ee981f97313a64af12e29b`**. During
implementation preparation the fail-closed importer found a genuine **source-provenance defect** in
`stories/thidukkidum-kathai`: the English translation's **prose was complete**, but its source-page
markers were **shifted by one page from scan 200 onward**, leaving scan 204's marker section empty.
Tamil scan 200's opening (`"அன்புள்ள நண்பர்களே!"` → *"Dear friends!"*) sat inside the English
**scan-199** section.

The implementation activity **stopped and reported it**. It did **not** silently repair the
translation downstream, did **not** drop the affected story, and did **not** weaken the validator to
get past it. An earlier revision of the importer had carried a re-attribution workaround; that
workaround was **deliberately removed** once the source was fixed, so an empty English marker section
now fails closed.

The archive was corrected first, and the batch was then re-frozen against the corrected release:

| | |
|---|---|
| Corrected pin | **`76135e1b5d504128c15be6bf59937716e5517d78`** — `Fix Thidukkidum Kathai English scan anchoring` |
| Story 29 — old tree | `a0f871a59b90782de7ff6dd7fc3f07c9c62ff830` |
| Story 29 — corrected tree | **`e6eea7e253f33f029f1c64958ea184dbd07423e0`** |
| Other 36 target trees | **unchanged** |
| Collection tree | **unchanged** |
| English prose | **unchanged** |
| Tamil | **unchanged** |

Only provenance / page-marker anchoring changed. The whole 37-tree freeze was **recomputed**, not
patched by substituting one SHA.

**Standing lessons:**

> A source release gate is not permission to work around a source defect downstream. If ingestion
> reveals a genuine source defect, **stop, repair and re-verify upstream, then establish a new source
> freeze.**

> **Marker presence and order alone do not prove source-page attribution.** Provenance anchors must
> correspond to actual content boundaries.

The second lesson generalises: a future source needs boundary evidence, not Story-29-specific
machinery.

### Source-format heterogeneity — normalise ingestion, not the source

All 37 workspaces were complete, but their **assembled Tamil files did not share one scan-marker
convention.** Observed across the batch: leading markers, trailing markers, incomplete marker
coverage, and **some works with no assembly markers at all.**

The importer therefore used the **uniform verified `pages/` records as the page-level source
authority**, rather than assuming assembly-comment syntax was canonical. Three further apparatus
findings:

- **`# அச்சு உரை`** appears as archival Markdown apparatus in some page records and is **not** printed
  story text — the archive's own visual-fidelity pass documents it as not occurring in the source;
- **`## Source review note` / `## Source-review note`** are archival apparatus;
- the genuine printed sub-headings inside **திடுக்கிடும் கதை** (`## காதல் கதை`, `## வீரக்கதை`) **are**
  story text and had to survive.

> **Bulk onboarding must normalise ingestion mechanics, not normalise away real source
> heterogeneity.** Choose the strongest uniform source layer, and explicitly exclude archival
> apparatus from reader text.

### Story model generalization — optionality as honest absence

The pre-Wave-2 `Story` model carried fields derived from the standalone `கிழவன் கனவு` booklet as
**required**. The anthology prints none of them. Wave 2 introduced source-form and provenance
distinctions — `StorySourceForm`, `StoryAnthologyPlacement`, `StoryAnthologyProvenance`,
`StoryTitleWitness`, `StoryVisualFidelity` — and made the booklet-specific fields optional:
`formLabel`, `printedAuthorshipLineTa`, `physicalPublication`, `printedPageUncertainty`, `errata`.

> A model generalization may make a previously required field **optional** when that field was
> actually **source-form-specific**. Optionality must represent **honest absence**, not weakened
> validation.

The validator proves each absence rather than merely tolerating it. **`கிழவன் கனவு` remained
byte-equivalent** in its generated reading and provenance data and retained every booklet-specific
fact.

### Title witnesses

| story | contents witness | opening witness |
|---|---|---|
| 28 | `புரட்சிப்படம்` | `புரட்சிப் படம்` |
| 36 | `சித்தார்த்தன்` | `சித்தார்த்தன் சிலை` |

The public canonical title follows the **story-opening** witness; provenance preserves **both**.

> Conflicting source title witnesses should be **represented, not silently normalized** into one
> invented form.

### English / Tamil authority

**Tamil remains authoritative.** All 37 English layers are **project-created** translations carried
from the source archive: 37/37 story-local translation reviews **PASS**, and the anthology-wide
English structural/control QA is **PASS**. **No retranslation occurred** during Digital Library
onboarding, and no external published English witness was used.

### Rights / edition — deliberate absences

No anthology story received an invented standalone `edition`, standalone publication claim, catalogue
`unitCount`, rights block, `WorkAttribution`, form label, individual printed authorship line,
publisher errata or printed-page uncertainty.

**`முதல் பதிப்பு: 1977` is a property of the anthology**, recorded on each provenance page. It was
**not** promoted into a fictional standalone first edition for 37 separate stories.

### Importer and validator

One deterministic batch importer, `scripts/import-1977-short-stories.mjs`, and one **independent**
source-linked validator, `scripts/validate-1977-short-stories.mjs`.

**Final validator: 2522 assertions · 42 groups · 0 failures · `BATCH RESULT: ALL PASS`.**

**Negative tests: 17 / 17 proven**, each failing through the intended contract rather than crashing —
source pin mismatch · per-work tree drift · missing/empty Tamil · missing/empty English · incomplete
review state · page-range errors · scan 260 entering story text · collapsed title witnesses · invented
booklet fields · the obsolete source pin appearing in output · and **a reconstruction of the original
Story-29 shifted page anchoring**.

Carried forward from Wave 1 and re-proved here:

- **one story failure fails the whole batch**, while the report still names the story;
- importer and validator **do not share extraction logic** in a way that would let one defect certify
  itself;
- **presence → structure → equality** remains mandatory; `empty == empty` may never certify;
- **failure paths report rather than crash** — three negative tests initially crashed on undefined
  data and the validator was made defensive;
- **`process.exitCode`** preserves the full report through a CI pipe;
- the importer **reruns byte-identical** from a clean state, with no clock values.

### CI

The anthology source is checked out at the **corrected historical pin** in a **dedicated CI
directory**, which preserves the same-repository/different-pin safety rule — `கிழவன் கனவு` uses its
own older pin.

Two CI mistakes occurred while the PR was still under development and were corrected **before**
exact-head approval: an apostrophe inside a bash single-quoted `node -e` block broke parsing, and the
new validator step initially lacked the per-step source-directory environment and fetch-success guard
its siblings carry. **Neither was a source defect.** The durable engineering lesson:

> **CI wiring is part of the review surface.** Validate embedded shell quoting, and require every
> archival-validator step to carry the same explicit source-directory environment and fetch-success
> guard.

**Validator-contract migration remains PAUSED.** Wave 2 did **not** resume it; the batch validator is
deliberately unregistered and counted as pending.

### Catalogue and public footprint

| | before | after |
|---|---|---|
| Published works | 31 | **68** |
| Fiction | 2 | **39** |
| Non-empty shelves | 9 | **9** |

**Wave-2 public contribution: 37 reader routes + 37 `/source` routes = +74 public URLs.** Contributed
through the existing `STORY_SLUGS`-driven route family; no slug is hard-coded into the sitemap.

| metric | pre-Wave-2 | post-Wave-2 | delta |
|---|---|---|---|
| **Next build static-route count** | 3035 | **3109** | **+74** |
| **Sitemap URLs** | 3023 | **3097** | **+74** |
| Prerendered `.html` files *(older, non-equivalent metric)* | 3027 | 3101 | +74 |

0 duplicate sitemap URLs. All three move +74 because the same 74 URLs are involved — **not** because
they measure the same thing. **3109 is the static-route count; 3101 is the `.html` file count; 3097 is
the sitemap URL count**, and none of those numbers may be substituted for another.

### Production verification — 2026-09-02

Post-merge **production** verification against `https://nenjukkuneethi.org` — not a preview.

Catalogue: **68** published works, **Fiction 39**, **9** non-empty shelves, no duplicate ids or slug
collisions, all 37 new cards rendering on `/read`. **All 74 Wave-2 routes returned 200**, sitemap
served 3097 URLs with 0 duplicates, and `/plays/`, `/speeches/`, `/cinema/` and `/read` were
undisturbed.

Representative checks: `pugazhendhi` · `thidukkidum-kathai` · `puratchip-padam` · `siddharthan-silai`
· `nunikkarumbu`, plus the `kizhavan-kanavu` regression — reader and `/source` 200 for each.

**Story 29 in production:** corrected pin visible, obsolete pin absent, the repaired boundary consumed
correctly (scan-199's tail precedes scan-200's opening, so the English is not shifted), the scan-204
ending present, the printed sub-headings retained, and archival apparatus absent from reader text.

**Title witnesses in production:** story 28 displays `புரட்சிப் படம்` with both witnesses in
provenance; story 36 displays `சித்தார்த்தன் சிலை` with both witnesses in provenance.

**Kizhavan regression PASS:** form label, printed authorship line, standalone physical-publication
section, printed-page uncertainty and the separate erratum witness all retained; its own historical
pin shown and the anthology pin absent; no anthology placement or title-witness section attached.

### Lessons for future bulk waves

1. **A source release gate is not permission to work around a source defect.** Stop, fix upstream,
   re-freeze — and recompute the whole freeze rather than substituting one SHA.
2. **Provenance anchors must match content boundaries**, not merely exist in the right order.
3. **Normalise ingestion mechanics, not the source.** Pick the strongest uniform source layer.
4. **Archival apparatus is not reader text** — and genuine printed headings are.
5. **Optionality must mean honest absence**, proved by the validator, never weakened validation.
6. **CI wiring is part of the review surface.**
7. **The exact-head sequence works.** Wave 2 ran it end to end and is the reference for how a wave
   should be shipped.

---

## Bulk Onboarding Wave 1 — Drama / கலைஞரின் நான்மணி மாலை four-play batch — ✅ COMPLETE and CLOSED

**The first bulk-onboarding activity in the Digital Library.** Four stage plays published together
from one frozen composite source release. Implementation PR
[#64](https://github.com/pugazg/kalaignar-autobiography/pull/64), squash merge
**`0dc92fa0fd832b5932b8df75606ef049c9f261ea`**, reviewed head
`74c7f6dc692571a8a3abcee77d929b76084ab9db`, 24 files. Verified in production on 2026-09-01.

**Do NOT reopen this wave.**

### Batch selection and rationale

The four works share **one controlling scan, one source release pin and one public shelf**, and each
had reached the same verified state upstream. That coherence — not convenience — is what made them a
batch. They were onboarded through **one importer, one validator and one review gate** rather than
four benchmark lifecycles, because nothing about them needed four separate architectural decisions.

**மணிமகுடம் / Manimagudam was excluded**, deliberately and explicitly: its source processing was
still active upstream at the freeze. See its subsection below.

### Source freeze

| | |
|---|---|
| Source repository | `pugazg/kalaignar-stage-plays` |
| Release pin | **`145e52e88dbd009286f749a7f0e3520386e63244`** |
| Controlling scan | `TVA_BOK_0065576_நான்மணி_மாலை.pdf` |
| SHA-256 | `18d2b1405544b03507e9f92067d287cb28f5a92eaf02bed7054e6e78e5e38c89` |
| Size | 146,754,449 bytes |
| Physical scans | 54 |
| Coverage audit | PASS / COMPLETE — 0 gaps, 0 overlaps |

Per-work target trees, guarded at every check including this close-out:

| work | source path | tree SHA | scans |
|---|---|---|---|
| பரதாயணம் / Bharathayanam | `works/bharathayanam` | `9923484dc94c7913581c0a87f99c8b017dddd2e7` | 6–17 |
| அனார்கலி / Anarkali | `works/anarkali` | `a1bc47bdda1abf9ba77cf04190f5b493d1443290` | 18–26 |
| சாக்ரடீஸ் / Socrates | `works/socrates` | `b09ab882ad7421b2cba4d61abbd0ae7185572552` | 27–43 |
| சேரன் செங்குட்டுவன் / Cheran Senguttuvan | `works/cheran-senguttuvan` | `d5a88f1288fb0e902e2dee6077399aa651a8db16` | 44–53 |

**Scans 1–5 are the composite's shared front matter and scan 54 its shared back matter.** Neither
belongs to any individual work, and neither may be attributed to one.

The pin is a **historical immutable release state**, not source `main`. Source `main` has advanced
since — entirely for `works/manimagudam/` — and all four target trees were re-confirmed byte-identical
at this close-out. **A released work stays pinned to the state that was reviewed; source `main` moving
is not drift.**

### Architectural generalization — structure kind vs reading unit

The public shelf and type are **unchanged**: `shelf: Drama`, `subtype: stage-play`,
`readerStructure: stage-play`. What Wave 1 added is a **source-structure** distinction inside the play
model:

- `structureKind: "scene-sequence" | "continuous-play"`
- reading-unit `kind: "scene" | "closing-tableau" | "continuous-body"`

**There is no `continuous-play` catalogue subtype and none may be created.** A play printed as one
continuous text is not a different *kind of work*; it is the same kind of work with a different
printed structure. Splitting the public category along that axis would be the wrong cut — the same
principle Speech Benchmark #4 established for source form.

### Bharathayanam — the continuous-play rule

| | |
|---|---|
| Source structure | `continuous-play` |
| Source scenes | **0** |
| Public reading body | one continuous reading unit |
| Editorial route slug | `continuous-play` |
| Catalogue `unitCount` | **ABSENT** |

The edition prints no scene division. **Do NOT describe it as "Scene 1", a "one-scene play", or
"1 of 1 scenes".** The route slug `continuous-play` is **navigation only** and is not a scene name;
the importer and validator both refuse a scene-shaped slug or a fabricated scene count. The catalogue
carries no unit badge because the source establishes no unit to count.

### The opening-note model

Printed pre-dramatic material is carried as a `PlayOpeningNote`: it is **source text, but never a
scene, never routed and never counted**. It attaches to the reading unit it precedes. Three of the
four works carry one — Bharathayanam (2 units, scan 6), Socrates (13 units, scans 27–28) and Cheran
Senguttuvan (5 units, scan 44). Anarkali prints none, and none was invented for it.

**Cheran Senguttuvan's pre-scene framing is explicitly NOT a scene**: its 5 units attach to reading
unit `01`, and its `sceneCount` stays **4**. The same holds for Socrates' 13-unit note against
`sceneCount` 5, and Bharathayanam's 2-unit note against a work with **no scenes at all**.

#### Page-record fidelity — a BOUNDED precedent

Socrates' Tamil introductory note had **verified page records but no source-repository assembled Tamil
intro file**. The integration therefore carried the page-record text **with its physical print
lineation intact**, and did **not** join print-line splits such as `கருத்` / `துக்கள்`.

**The bounded precedent:** where the source archive deliberately holds only verified page records and
no authorized assembly, the Digital Library **may preserve page-record fidelity rather than silently
perform its own textual assembly**. Assembly is the archive's decision to make.

**Do NOT turn this into a universal rule for every source without review.**

### Socrates — the source-fidelity repair

**This is the most important lesson of Wave 1 and is recorded in full because it nearly shipped.**

At the first PR head, Socrates published:

```
openingNote.tamil.units = []
```

while source scans 27–28 demonstrably contain verified Tamil introductory material, and the English
side carried 13 units. Independent review caught it.

**Root cause.** Both the importer and the validator bounded a page record's `## Printed text` section
with a pattern equivalent to:

```
/^## Printed text\n([\s\S]*?)(?=^## |\s*$)/m
```

Under the `m` flag the `\s*$` alternative matches at the **blank line directly beneath the heading**,
so the reluctant capture terminated there and returned an empty section. Because importer and
validator **shared the same defect**, the validator's "verbatim" check reduced to `[] === []` and
certified as complete a section the source fills. The assertion was **vacuous, not wrong-answered** —
the most dangerous failure mode a validator has.

**The repair** replaced both with H2-boundary extraction — from the heading to the next `^## ` or EOF
— gave the validator an **independent** implementation, and made an empty extraction an error rather
than an answer:

| | |
|---|---|
| source scan 27 | **7** introductory paragraphs |
| source scan 28 | **6** |
| combined source intro | **13** |
| generated Tamil intro | **13** — 11 prose/unlabelled · 1 square-bracket stage direction · 1 final ornament `*` |
| provenance `tamilUnits` | 108 → **121** (stage directions 24 → 25, ornaments 9 → 10) |
| English | unchanged — 13 intro units, 120 total |
| scene count | remains **5** |
| intro route | **none** |

Printed line structure is preserved exactly: **no print-line wrap is joined**, because that assembly
decision belongs to the source archive, not to a downstream integration.

**Protected Tamil readings — carried verbatim, never normalized:**

```
மார்க்சும், எஞ்சல்சும்
ஹெகல்
‘ஜாடை’ காட்டினான்
தூசு நிகர் காரணங்களைக்கொண்டு
‘சோக்ரதர்’
ஆஸ்திகப்பழமாக்கியிருக்கிறார்
நானோ
சபைன்
```

The intro opens with `ஃ சாக்ரடீஸ் கிரேக்கம் தந்த தத்துவாசிரியன்`, carries the bracketed scan-28
`முதற்காட்சி` setup as one square stage-direction, and ends with the printed `*`.

### The validator-output repair

A second, independent defect: after the source repair the validator was **correct but unreadable in
CI**. Its assertions all ran and all passed, yet the CI log stopped 64 lines in, so the new Socrates
gates could not be seen. Two causes, both of which destroy the report while leaving the exit code
looking right:

1. **`process.exit()` discards buffered stdout when stdout is a pipe** — which is exactly what GitHub
   Actions provides. Reproduced: **411 lines to a file, 59 to a pipe, exit 0 both times.**
2. **Direct array indexing in failure-only spot checks** threw a `TypeError` before the final report,
   so an induced failure exited 1 for the wrong reason and printed no summary.

The repair uses `process.exitCode` for the normal final exit, keeps the deliberate fail-closed early
exits, and makes failure-sensitive assertions read defensively. Verified through a pipe:

| path | result |
|---|---|
| success | exit **0**, complete report, empty stderr |
| induced failure | exit **1**, all 385 assertions still run, **17** clean failures, empty stderr, complete report |
| source-pin mismatch | exit **2**, prints `BATCH RESULT: CANNOT VALIDATE` |

### Deterministic importer

One importer, `scripts/import-naanmani-malai-plays.mjs`, pinned to the release commit and fail-closed
on source-HEAD mismatch, on an empty printed-text extraction, on a missing protected reading, and on
a missing bracketed setup or ornament. Two clean runs at the pin produced **byte-identical** output,
identical to the committed data, with **no clock or timestamp values** in any generated file. Generated
JSON is never hand-patched.

### Batch validator

One source-linked validator, `scripts/validate-naanmani-malai-plays.mjs`, re-deriving expectations
from the pinned source tree and reporting **per work**:

| group | assertions |
|---|---|
| BATCH PRECONDITIONS | 17 |
| BHARATHAYANAM | 82 |
| ANARKALI | 81 |
| SOCRATES | 109 |
| CHERAN SENGUTTUVAN | 83 |
| BATCH OPENING NOTES | 10 |
| BATCH ROUTE CONTRACT | 3 |
| **total** | **385 · 0 failed · BATCH RESULT: ALL PASS** |

**The final validator contract is 385 assertions.** The pre-repair figure of 355 is **historical
only** and must never be quoted as the contract.

### English authority

All four English layers are **project-created** and source-linked to the verified Tamil. Tamil remains
the authoritative layer.

For **Anarkali, Socrates and Cheran Senguttuvan**, M. D. Jayabalan's separately copyrighted **2009
published English translation is SECONDARY COMPARISON EVIDENCE ONLY**. It is **not** the public
English reading layer, **not** Tamil authority and **not** translation authority, and it is never
imported or reverse-translated.

For **Bharathayanam there is no corresponding 2009 witness** — the 2009 collection contains no
Bharathayanam. That is **NOT APPLICABLE**, not pending.

### Rights

Nationalisation applies to **Kalaignar's underlying Tamil dramatic works**. It does **NOT** extend to:

- the project-created English;
- the third-party 2009 published English witness;
- publisher / imprint matter;
- the printed price;
- cover artwork or design;
- library, accession or other copy-specific markings on the physical volume.

GO number and formal issue date remain `null` and **must not be invented**; `2024-12-22` is the public
handover date only. A scoped **`WorkAttribution`** model remains future work and was **not** created.

### Edition / year

**`edition` is absent on all four**, deliberately. The source establishes publisher, place and price
but **no defensible standalone publication year or edition statement** for the individual works.
**Do NOT promote 2009 into a Tamil edition year** — 2009 belongs only to the third-party English
witness.

### Catalogue and public footprint

| | before | after |
|---|---|---|
| Published works | 27 | **31** |
| Drama shelf | 1 | **5** |
| Non-empty shelves | 9 | **9** |

Catalogue order on the Drama shelf: `silappathikaram-nataka-kappiyam` → `bharathayanam` → `anarkali`
→ `socrates` → `cheran-senguttuvan`, following the composite's own printed order.

Unit badges: Bharathayanam **absent** · Anarkali **4 scenes** · Socrates **5 scenes** ·
Cheran Senguttuvan **4 scenes**. All four carry the exact pin and **no `edition`**.

### Route and sitemap deltas — Wave-1 facts, not to be rewritten later

**22 public URLs**, contributed through `PLAY_SLUGS` and the generated `readingUnits` — the four works
are **not** hard-coded into the sitemap:

| work | routes | breakdown |
|---|---|---|
| Bharathayanam | 3 | landing + `continuous-play` + source |
| Anarkali | 6 | landing + 4 scenes + source |
| Socrates | 7 | landing + 5 scenes + source |
| Cheran Senguttuvan | 6 | landing + 4 scenes + source |

| metric | before | after | delta |
|---|---|---|---|
| **Next build static-route count** *(site-wide total)* | 3013 | **3035** | **+22** |
| **Sitemap URLs** *(site-wide total)* | 3001 | **3023** | **+22** |

**Wave-1 public URL contribution: +22**, broken down as **4 landings + 4 source pages + 14 reading
routes**. The 14 reading routes are Bharathayanam 1 (`continuous-play`) + Anarkali 4 + Socrates 5 +
Cheran Senguttuvan 4.

The **+22 is a delta**; the 3035 and 3023 figures are **site-wide totals** at the Wave-1 boundary. The
older "Prerendered pages" convention (3005 → 3027) is **not** carried here — see the metric note in
the CURRENT STATE section.

0 duplicate sitemap URLs. These are the deltas **at this wave's boundary**; if the site advances later
for unrelated reasons, refresh the CURRENT STATE checkpoint — **do not rewrite these figures**.

### Silappathikaram regression

The existing Drama benchmark was carried through the shared model generalization **without any
textual or source change**. The rename `PlayScene` → `PlayReadingUnit` and `isClosingTableau` → `kind`
is a **model rename, not a content change**:

- **38** source-numbered scenes, unchanged;
- the closing tableau remains **separate and is NOT Scene 39** — it carries `order: null`, slug
  `closing-tableau` and no scene number;
- reading text **byte-equivalent across the migration** — 2409 units on both sides;
- catalogue entry **unchanged**;
- public behaviour and routes **unchanged**;
- validator **157 assertions, ALL PASS**.

### CI and production verification — 2026-09-01

Merged-main Library CI run **`33537622127`** on `0dc92fa0…`:

| job / step | result |
|---|---|
| typecheck • build | **SUCCESS** |
| archival validators | **SUCCESS** |
| Naanmani Malai Plays — 4-work Drama batch | **SUCCESS** — 385 assertions, 0 failed across 7 groups, `BATCH RESULT: ALL PASS` |
| Silappathikaram Nataka Kappiyam | **SUCCESS** — 157 assertions passed, 0 failed |
| Validator contract | **SUCCESS** — **3 registered / 10 pending** |
| Vercel | **SUCCESS** |

**Validator-contract migration remains PAUSED.** The batch validator is deliberately **not**
registered. Do not resume the migration.

Production, measured against `https://nenjukkuneethi.org`: **all 22 Wave-1 public URLs return 200** —
that is the complete Wave-1 set, already inclusive of the four `/source` routes; it is not 22 plus
anything. The **Silappathikaram route family was regression-checked separately** and is not part of
the Wave-1 22. `/plays/socrates/01` renders the verified Tamil
introductory note **before** Scene 1, labelled `அச்சிடப்பட்ட முன்னுரைக் குறிப்பு`, with every
protected reading, the bracketed setup and the closing `*` present, still reading "Scene 1 of 5" and
**never** presented as a sixth scene. `/plays/socrates/00-introduction`, `/plays/socrates/06`,
`/plays/anarkali/05`, `/plays/cheran-senguttuvan/05`, `/plays/bharathayanam/scene-01` and
`/plays/manimagudam` all return **404**.

### மணிமகுடம் / Manimagudam — excluded, and still excluded

Manimagudam was excluded from Wave 1 because **its source processing was incomplete at the Wave-1
freeze**. Its source directory has advanced substantially since and continues to move independently.

That movement does **NOT**:

- retroactively add it to Wave 1;
- repin Wave 1;
- make it automatically eligible for Wave 2;
- authorize its publication.

**Do not inspect or adjudicate Manimagudam** beyond the source-separation check Wave 1 requires, and
**do not treat it as the next candidate.**

**It is not permanently ineligible.** Manimagudam remains **source-active** upstream and may become a
legitimate candidate later, once it passes **its own release/readiness gate** and the owner authorizes
a wave that includes it. What is excluded is *automatic* selection: eligibility, whenever it arrives,
is still not authorization.

### ⚠️ Process lesson — the exact-head review gate

**Recorded because it must not become the pattern.**

Wave 1's implementation PR **#64** was **merged before its final repaired head received independent
ChatGPT exact-head approval**. The final repaired head was
`74c7f6dc692571a8a3abcee77d929b76084ab9db`; the squash merge is
`0dc92fa0fd832b5932b8df75606ef049c9f261ea`. Independent ChatGPT subsequently performed a read-only
**post-merge** review of the exact merged implementation and **accepted** it.

**That acceptance settles Wave 1. It does not make post-merge review an acceptable substitute for the
review gate, and it is not a precedent.**

**Standing rule for every future bulk implementation PR:**

1. Claude Code opens the bulk implementation PR;
2. ChatGPT reviews the **EXACT current PR head**;
3. ChatGPT gives **APPROVED FOR MERGE** for that exact head;
4. **only then** may Claude Code merge;
5. **if the PR head changes after approval — for any reason, including a repair — STOP and re-review
   before merging.**

Bulk onboarding does **not** relax this gate. A batch concentrates more work behind one review, which
makes the exact-head discipline more important, not less.

### Lessons for future bulk waves

1. **Coherence, not convenience, defines a batch** — one source release, one shelf, one comparable
   verified state.
2. **Batching must not flatten source differences.** Wave 1's four works kept different structures,
   different opening notes and different witness situations; the shared importer accommodated that
   rather than normalizing it.
3. **A validator must never be able to certify `[] === []`.** Prove presence, then structure, then
   equality — see the standing rule recorded below.
4. **Importer and validator may share a contract but must not share an implementation defect.** The
   validator's extraction is now independent by design.
5. **Validator success is not enough if the evidence cannot be read** — see the CI-output rule below.
6. **A route slug is not a structural claim.** `continuous-play` is navigation; it never became a
   scene name or a unit count.
7. **Printed pre-dramatic material is source text without being a scene** — carry it, attach it, and
   neither route nor count it.
8. **Absent metadata stays absent.** No `edition`, no year, no unit badge where the source establishes
   none.
9. **A secondary published translation stays secondary** in a batch exactly as it does for one work,
   and "no witness exists" is *not applicable*, never *pending*.
10. **One review gate for a coherent batch is sufficient** — four separate benchmark lifecycles would
    have added ceremony, not assurance. **But it must still be an exact-head gate before merge.**
11. **One coherent source batch may share one historical source pin**, while **per-work provenance
    stays distinct** — each work keeps its own scan extent, counters and provenance page.
12. **Source-tree drift guards remain per work**, not per repository: the batch is only frozen if each
    work's tree SHA is checked individually.
13. **One failure must fail the whole batch.** The batch validator reports per work, but any group's
    failure fails the run — a batch result may never average away one work's defect.
14. **A batch may justify a small reusable model generalization** (`structureKind`, `readingUnits`,
    `openingNote`), but **source structure must never be flattened just to make the batch uniform.**
15. **`readingUnits` is more source-honest than assuming every public unit is a scene** — it is what
    let a continuous play, a scene sequence and a closing tableau share one model without any of them
    lying about its source.
16. **Scan-provenance granularity must not claim precision the archive does not publish** — where the
    archive records per-unit-group scans, the generated data says so and does not invent per-unit
    precision.
17. **Dedicated CI source checkouts are necessary when one source repository is pinned at multiple
    historical commits.** Silappathikaram and the Naanmani Malai batch both come from
    `pugazg/kalaignar-stage-plays` at *different* pins, so they use separate checkout directories and
    the workflow's same-directory/same-pin guard keeps its meaning.

---

## Bulk onboarding is the STANDING DEFAULT workflow

**Owner decision, recorded 2026-09-01 after Bulk Onboarding Wave 1 — Drama.** This supersedes the
older one-work-per-benchmark default and the "no bulk import, no mass ingestion" constraint that
appears in the historical per-benchmark constraint lists below. Those lists are kept as the record of
how earlier benchmarks were run; **they are no longer the default for new work.**

### The default procedure

1. **identify a coherent batch** by source release / source repository / public shelf;
2. **perform a readiness census over the whole candidate set** before selecting anything;
3. **explicitly exclude incomplete or blocked works**, and record why;
4. **freeze each included work** by source commit and tree identity;
5. use **one coherent deterministic importer** where appropriate;
6. use **one coherent source-linked batch validator**;
7. the validator **reports and fails per work** — a batch result may never hide a single work's
   failure;
8. **preserve per-work provenance, rights and structural distinctions**;
9. publish the coherent batch in **one implementation PR** where the architecture allows;
10. use **one independent ChatGPT review gate** for the batch;
11. **ChatGPT reviews the EXACT current PR head and gives APPROVED FOR MERGE; merge only after that
    approval; if the head changes, STOP and re-review**;
12. **after merge, perform production verification, then perform one batch control close-out**;
13. **do not flatten source differences merely because the work is batched.**

Steps 11 and 12 are ordering commitments, not formalities: **approval precedes merge, merge precedes
production verification, and production verification precedes the control close-out.** This sequence
is identical in `NEXT_CHAT_PROMPT.md`, and the two documents must never disagree about it.

### Bulk is the default, not permission to mix

**Bulk does not mean "publish whatever is nearby".** It is not a claim that every future work must be
bulked regardless of source state, and it never authorizes mixing incompatible or incomplete sources.
A work that is not source-ready is excluded from the batch and said so explicitly — exactly as
மணிமகுடம் was in Wave 1.

### One-work benchmark cycles are now the EXCEPTION

Use single-work treatment only where a work introduces a genuinely new:

- **source form** (as the first audio speech did);
- **reader architecture**;
- **unresolved rights or attribution boundary**;
- **unusual structure**;
- **source-fidelity blocker**;
- **implementation risk that should not be coupled to a batch.**

Eligibility for a batch is **not** authorization to start one. **Owner authorization is still required
before any wave begins.**

### Standing rule — batch validation must avoid SHARED FALSE POSITIVES

An importer and a validator may implement the same source contract, but they **must not share a defect
that makes both derive the same empty or wrong expected value.** Wave 1 shipped a work whose verified
Tamil introductory note was missing precisely because both sides computed `[]` and the equality check
then "passed".

For any source section known to exist, a validator **MUST explicitly assert NON-EMPTY source
extraction before asserting equality.**

The general rule:

> **prove presence → then prove structure → then prove equality.**

**Never allow `empty == empty` to certify completeness.** Where practical, give the validator an
implementation of the source contract that is independent of the importer's, and negative-test both
gates to confirm they actually bite.

### Standing rule — validator success is not enough if the evidence cannot be read

A green check with an unreadable log is not evidence. For verbose validators running in CI:

- **avoid a final `process.exit()`** when stdout may still be buffered — Node discards buffered stdout
  writes when `process.exit()` is called while stdout is a pipe, which is what CI provides;
- **prefer `process.exitCode`** for normal completion, and let the process end on its own;
- keep deliberate fail-closed early exits where they are intentional;
- **ensure failure paths report their assertions rather than crash** — an assertion that throws while
  dereferencing missing data exits non-zero for the wrong reason and destroys the report;
- **test validators through a pipe as well as direct stdout** wherever log completeness matters.

This is a reusable validator-engineering rule, not a Socrates-specific note.

---

## Speech Benchmark #4 — கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை — ✅ COMPLETE and CLOSED

**Kalaivanar N. S. Krishnan Memorial-Day Speech.** Slug `kalaivanar-nsk-memorial-day`. Merged and
verified in two independently reviewed stages, A1 and A2. Final benchmark implementation boundary:
**`56ca0c978e34afddde52595f2ce825872bd6aeef`**. Verified in production on 2026-09-01.

**Do NOT reopen this benchmark.**

### Selection / architectural purpose

This work was selected because it was the first opportunity to prove that the existing **Speech
reader could support a second controlling-source form** — an audio recording rather than a printed
booklet or scan — **without** creating a separate public `audio-speech` subtype and **without**
building a generalized media framework.

The architectural result: **`public-speech` remains the content subtype**, and **`sourceForm`
distinguishes print from audio only where the reader and provenance layer actually need it**. Source
form is orthogonal to content subtype; splitting the public speech category along the media axis
would have been the wrong cut.

This is the result *for this work*. It is a precedent to weigh, not a rule: **do not assume every
future audio work must use exactly this model without its own review.**

### Source boundary

| | |
|---|---|
| Source repository | `pugazg/kalaignar-public-speeches` |
| Source path | `speeches/kalaivanar-nsk-memorial-day` |
| Release pin | `1ef73a709a343390befe55dcdfb029427f527bf4` |
| Target tree SHA | `256cbe2adc8dbc9c245be57196652ed79da48eeb` |

The pin is a **historical immutable release state**, not source `main`. Live public-speeches `main`
has advanced repeatedly since the pin, and the target archive's tree SHA was re-confirmed identical
at every check, including immediately before this close-out. **A released work stays pinned to the
state that was reviewed; source `main` moving is not drift.**

Controlling source — an audio recording, **not** a publication:

| | |
|---|---|
| Filename | `05.Kalaivanar N.S.Krishnan Ninnaivu Naal Vizha vil Kalaigar Speech.mp3` |
| SHA-256 | `7457004d3c3ee87722edfe6814e830d3521b834dcf29b4de45bb7174a2278148` |
| Size | 7,087,106 bytes |
| Decoded duration | 443.559 s — `00:07:23.559` |

Archive-recorded verification state, carried from the source archive and not re-adjudicated here:

- Tamil transcription **verified-complete**
- strict direct-listening audit **12 / 12 segments passed**
- open Tamil uncertainties **0**
- **recording NOT truncated** — an earlier incomplete reading of the ending was withdrawn upstream
  after a direct tail re-audit restored the closing passage through `07:23.559`
- English translation **verified-complete** (E2 fidelity review and E3 final verification passed)
- **12 timestamp markers**

### A1 — audio-source model, data, reader, provenance, routes, CI

Implementation PR **#62**, squash **`492b26ddd5681f085726ac802681c3fcbc7162f0`** (11 files).

A1 delivered the first audio-sourced Digital Library speech by extending the existing `speech`
reader architecture by **source form**:

- work remains `public-speech`; **no `audio-speech` subtype was created**;
- `sourceForm: "audio"` in the speech data — absent means print, so **no released print speech was
  rewritten**;
- deterministic importer, fail-closed on source-HEAD mismatch, on timestamp divergence, and on any
  source layer the archive had not released; it **never opens, probes or fetches the MP3**;
- deterministic source-linked validator;
- audio-specific reader copy; audio-specific provenance/source page;
- reader route and source route;
- automatic sitemap exposure through the existing `SPEECH_SLUGS` registry;
- Library CI integration under the named step **Kalaivanar NSK Memorial Speech**;
- **no audio binary, no audio player, no runtime media fetch**;
- **no catalogue card at the A1 boundary** — `/read` discovery was deliberately deferred to A2.

A1 also fixed a latent metadata-grammar defect that this candidate was the first released speech to
expose: a speech with a venue and no date produced `Kalaignar M. Karunanidhi's at <venue>`, because
the date clause was what supplied the noun. Zero description drift for every already-released speech.

### A2 — Reading Room catalogue onboarding

Implementation PR **#63**, squash **`56ca0c978e34afddde52595f2ce825872bd6aeef`** (2 files).

A2 delivered exactly one `LibraryWork`, appended as the **14th Speech catalogue work** after
`2006-08-23-industries-debate`, giving the already-live reader its `/read` discovery. It retained the
historical source pin and added **no `edition`, no `unitCount`, and no catalogue-level `sourceForm`**.

**A2 added no routes and no sitemap URLs.** Both speech URLs were already live from A1 through
`SPEECH_SLUGS`.

A2 also carried one authorized validator change: **assertion 64 was transitioned** from the temporary
A1 statement *"the catalogue is absent"* — which A2 deliberately makes false — to a **durable
catalogue-present contract** that isolates this one `LibraryWork` and proves its identity, historical
pin, coverage, provenance route, rights scope and the three deliberate absences. The validator
**remains 102 assertions**; assertions 1–63 were untouched and no source-fidelity check was removed
or weakened.

### Public footprint

| | |
|---|---|
| Reader | `/speeches/kalaivanar-nsk-memorial-day` |
| Source / provenance | `/speeches/kalaivanar-nsk-memorial-day/source` |
| Catalogue | one Reading Room card on the **Speeches** shelf |
| Sitemap contribution | **2 URLs** |

Those 2 sitemap URLs were introduced **in A1** through `SPEECH_SLUGS`. **Do not double-count them
against A2**, whose sitemap delta and route delta were both **0**.

### Stage deltas — benchmark-stage facts, not to be rewritten later

**A1:** Speech registry 13 → 14 · application pages 3003 → 3005 · sitemap 2999 → 3001 · catalogue
**unchanged** at the A1 boundary.

**A2:** published works 26 → 27 · Speech catalogue works 13 → 14 · `/read` card 0 → 1 ·
application pages 3005 → **3005** · sitemap 3001 → **3001**.

These are the deltas **at each stage**. If the live site advances later for unrelated reasons, refresh
the CURRENT STATE checkpoint — **do not rewrite these historical stage figures**.

### Date / venue / event boundary

- **Exact speech date: NOT ESTABLISHED.** The recording states none, so `date` is `null`.
- **Year: NOT INFERRED.** `year` is `null`.
- **Venue:** `கலைவாணர் அரங்கம், சென்னை`
- **Event:** `கலைவாணர் நினைவு நாள் விழா`

Venue and event are carried exactly as the source archive establishes them from direct listening,
with no expansion from outside historical knowledge. The archive separately records secondary
chronology as context and expressly forbids substituting it for the speech date; that reasoning is
**deliberately not imported** into public data, and neither are the file's embedded timestamps.
**Secondary chronology is not the controlling source for the date. Do not introduce 1974 — or any
other historical date — as the speech date.**

### Audio-source model

- The **12 timestamps are APPROXIMATE NAVIGATION MARKERS**. They are **not** source-authored
  chapters, sections, speech units, or exact word-level timing. They are imported as their own block
  kind and rendered as subdued navigation separators — never as headings — and the Tamil list, the
  English list and the archive's own time map must be identical in order or the import fails closed.
- **No fabricated page provenance.** A recording is not paginated: there is no `edition`, no scan
  filename, no scan or printed page range, no front/back matter, no source-page mapping and no
  page-boundary adjudication. Every occurrence of "printed", "scan" or "page" on the provenance page
  is a negation.
- **No media redistribution.** The MP3 is not committed upstream and is not vendored, streamed,
  proxied or played here. Its identity travels as URL + filename + SHA-256 + size + decoded duration
  + stream properties. The original URL appears on the provenance page as an ordinary external link
  only.
- **No audio player was necessary to publish the verified transcript.**
- English is a **project-created** layer made from the frozen verified Tamil — not translated
  independently from the recording. Tamil remains the authoritative transcription layer, and the
  recording remains the controlling witness for the spoken Tamil.

### Rights boundary

The project's nationalisation position applies to **Kalaignar's underlying authored Tamil speech**.

It does **NOT** establish rights over:

- the **source audio recording**;
- the **recording master**;
- **third-party recording production**;
- the **project-created English translation**.

The catalogue entry and the provenance page both carry that exclusion explicitly, so a nationalisation
badge on an audio-sourced work can never be read as a claim over the media file. **Do not say the MP3
is nationalised. Do not say the recording is Government of Tamil Nadu property.** GO number and formal
issue date remain `null`; `2024-12-22` is the public handover date only.

**No new rights model was created.** A scoped **`WorkAttribution`** model remains future work.

### Validator / CI

- Work-specific validator: `scripts/validate-kalaivanar-nsk-memorial-day.mjs`
- Final assertion count: **102**
- Main-branch result: **102 passed / 0 failed**
- Source checkout: `1ef73a709a343390befe55dcdfb029427f527bf4`
- Named CI step: **Kalaivanar NSK Memorial Speech**
- A1 main-branch CI run: **33491297938** (`492b26dd…`) — both `typecheck • build` and
  `archival validators` success
- A2 main-branch CI run: **33506276740** (`56ca0c97…`) — both success

Regression evidence at both merges: **Poonthottam PASS**, **Arappor PASS**.

The validator shares the public-speeches CI checkout with Poonthottam and Arappor — all three pin the
same commit, so the workflow's same-directory/same-pin guard keeps its meaning.

**Validator-contract migration remains PAUSED**, recorded at the A2 merge as **3 registered /
9 pending**. This validator is deliberately **not** registered in the migrated contract. Do not resume
the migration.

### Production verification — 2026-09-01

Measured against `https://nenjukkuneethi.org`:

- `/speeches/kalaivanar-nsk-memorial-day` → **200**; public-speech label, audio-source indicator,
  **12** navigation markers, **no date chip**, no printed-source claim, no `<audio>` element
- `/speeches/kalaivanar-nsk-memorial-day/source` → **200**; audio-specific source facts with the
  exact SHA-256 and `00:07:23.559`, a 12-entry time map, the recording-rights exclusion, and **no
  rendered print/scan provenance section**
- `/read` → **200**; **exactly one** catalogue card, linking to the reader route, with **no inferred
  date, no year and no unit-count badge** in either Tamil or English

### Lessons / future reuse

1. **Source form is orthogonal to content subtype.** Add a discriminator where the render layer needs
   it; do not split the public category along the media axis.
2. **An audio speech has no printed-page provenance** — do not fabricate PDF/scan/page apparatus for
   a source that has none.
3. **Timestamp markers are navigation aids, not source-authored structure**, and must never become a
   catalogue unit count.
4. **An exact speech date must stay `null`** when the recording does not establish one.
5. **Technical recording provenance can be preserved without redistributing the binary.**
6. **No audio player was necessary** to publish the verified transcript.
7. **Underlying authored-work rights and recording rights are separate questions.**
8. **English remains a project-created layer** derived from the frozen verified Tamil.
9. **A source repository's `main` may advance while a released work remains pinned** to a historical
   immutable release state.
10. **Sibling source archives with similar names must never be conflated** — see the warning below.

### ⚠️ `kalaivanar-nsk-memorial-day-audio-06` is a SEPARATE archive

`pugazg/kalaignar-public-speeches` also contains a sibling archive
`speeches/kalaivanar-nsk-memorial-day-audio-06/`, which is a **different recording** and a **separate
source work**. It is under active upstream development and accounts for essentially all
public-speeches `main` movement since this benchmark's pin.

It is **NOT**:

- a revision of the published Benchmark #4 archive;
- a new pin for Benchmark #4;
- automatically selected for the Digital Library;
- automatically ready for publication.

Changes under that directory are **not** benchmark drift. Do not inspect or adjudicate Audio 06
beyond establishing that it is separate, and **do not treat it as the next candidate**.

### Standing follow-ups — separate future work, NOT Benchmark #4 blockers

None of these were fixed in A1 or A2, and none may be folded into another change automatically:

1. the generic print-centric top-level comment in `data/speeches.ts`;
2. the nearby `SpeechReader` internal comment that still describes block streams in print terms;
3. **validator-contract migration — PAUSED**;
4. **mobile — ON HOLD**;
5. **Manohara source-drift audit** — future;
6. **`WorkAttribution`** — future scoped rights model for composite works;
7. Film Songs nullable-label type mismatch;
8. stale `/read` metadata description;
9. Film Songs E3 catalogue-comment wording precision;
10. **Film Songs formal control close-out — historical pending item, now superseded by the dedicated
    COMPLETE and CLOSED section above.**

---

## Phase C — பராசக்தி / Parasakthi — ✅ COMPLETE and CLOSED

Cinema Writing benchmark #2. Verified in production 2026-08-26.

**Final implementation `main` after C5: `15405c7ff252ad98250a2ad50b4d718598300ded`.**

Stages, all merged:

| Stage | PR | Squash |
|---|---|---|
| C1 source/readiness audit | — | (audit only, no PR) |
| C2 deterministic data import | #48 | `1b46dbe` |
| C2.1 attribution provenance correction | #50 | `fd5ffe5` |
| C3 reader + source/provenance routes | #49 | `5349f1d` |
| C4 catalogue | #51 | `017f0b5` |
| C5 sitemap | #52 | `15405c7` |
| C6 final production audit | — | (audit only, no defects, no PR) |

**Source pin:** `pugazg/kalaignar-cinema-works` @ `789b003b6c0dfcf0bc38b906037f92953fd8146f` —
work-specific, not source `main`. It supersedes `a593db5079e76887abeb41d9c2abfd978a7fe9a5`, which
predates the archive's song-attribution correction.

**Public footprint:** 48 Parasakthi sitemap URLs — 1 landing, 1 source page, 46 scenes.

### The three source facts Phase C exists to protect

1. **The booklet prints its own scene headings**, unlike Manohara's archive-created navigation
   segments. Parasakthi's 46 are the booklet's; Manohara's 57 are not. That distinction is encoded in
   `unitCount` labels and must not be collapsed if a third cinema work arrives.
2. **Headings 23 and 34 are never printed.** No scene file, no route, no sitemap URL, no placeholder.
   The absence is recorded as absence.
3. **The songs are not all Kalaignar's.** The booklet credits six poets collectively and pairs none
   with a song. Item-level attribution rests on three tiers — 11 `external-source`,
   2 `anthology-attributed`, 1 `canonical-context-explicit` — and exactly **two** of the fourteen
   occurrences are his, both on **anthology** evidence, which is **not** an original-film credit. The
   superseded பாரதிதாசன் tracklist witness for scene 4 is preserved, not deleted or called wrong.

**No blanket rights block.** Parasakthi is a composite publication; the nationalisation model that
applies to Manohara cannot be applied to a booklet containing five other poets' work. A scoped
`WorkAttribution` model remains future work.

**Do NOT reopen Parasakthi.**

---

## Phase D1 — திரும்பிப்பார் / Tirumbippaar readiness audit — COMPLETE

Audited at `pugazg/kalaignar-cinema-works` @ `ca7431f3de8f8b2367a65206b8a9739d87788413`; re-confirmed
unchanged at `03c89cd2bb3019c5f75c2bfbca14077a8d1f643b` (intervening commits are Raja Rani only).

### The original premise was wrong: the crop is NON-BLOCKING

Tirumbippaar was carried as partial/blocked over "an unresolved crop". The crop is real but sits in
**front matter**, not reading text:

- location: PDF **2**, lower printer/imprint line
- visible partial: `சிட்டி பிரஸ், மதுரை ரோ…`
- canonical screenplay begins at PDF **9** — seven pages later
- canonical range: PDF **9–112** / printed pp. **1–104**, **104/104 verified**, 0 draft, 0 review
- `additional_main_text_crop_or_duplicate_findings: []`; zero crop/illegible markers in any of the
  five canonical transcription parts

It is a printer's imprint — a bibliographic detail, not a word of the screenplay. It stays **partial
and unreconstructed** (no `மதுரை ரோடு`, no address or printer-name continuation), and is classified
**documented / unresolved / front matter / non-blocking**.

### Measured census at D1 — ⚠️ PRE-CORRECTION, SUPERSEDED

These were the figures at the D1 audit pin, **before** the user's textual-correction pass. They are
recorded for history only. **Do not reuse them** — the current verified census is in the D1.1 section
below (1042 dialogue records, 1330 translation units).

104 canonical pages (0 missing, 0 duplicate, `printed = pdf − 8` with 0 violations) · 93 scenes ·
~~1,040 dialogue records · 1,321 English units~~ · 39 entities / 45 labels.

Songs: 8 occurrences — **3 verified, 5 unresolved, 0 attributed to Kalaignar**. The three verified are
`external-source` only (பாரதிதாசன் ×1, கண்ணதாசன் ×2). No anthology tier, no full lyric body printed,
no Tamil song derivative invented from absent text. Work authorship is a direct printed cover credit:
`கதை - வசனம் — கலைஞர் மு. கருணாநிதி`. Rights: `உரிமையுடையது.` and `விலை ரூ. 0-10-0` are recorded as
printed 1953 statements, not a present-day determination — no blanket rights block.

---

## Phase D1.1 — canonical/derivative reconciliation — CONTENT PASS

The earlier D1.1 framing — "one remaining PDF-59 punctuation blocker" — is **superseded and no longer
the state**. That question was overtaken by a full textual-correction pass the user ran against the
controlling scan, which corrected the canonical Tamil across the work.

### Source authority

The controlling scan decides every reading. Readings are **not** judged by grammar, gender agreement,
expected syntax, character identity or modern usage. As-printed forms that look unusual are preserved
— `அறிமுகமானான்`, `விளையாடுகிறான்`, `மாடிக்குப் போகிறாள்`, `பெருமூச்ச`, `பரந்தாமான்`.

**`ஊஹும்` was verified directly by the user against the controlling PDF.** That reading is settled,
is preserved in every reading layer, and is not to be reopened or reverted to `ஊஹூம்`.

### What source PR #2 does

The correction pass updated canonical but did not consistently re-derive the dependent layers, so
`pugazg/kalaignar-cinema-works` **PR #2** reconciles them:

- 16 scene lines brought into line with corrected canonical (scenes 6, 7, 8, 16, 28, 41);
- one **canonical omission restored from the scan** — `கருடன் : இல்லை பரந்தாமன்.` is the first line of
  printed page 6 / PDF 14; canonical had dropped it and `scene-05` had it in the PDF 13 block. It is
  now in canonical once at the head of the PDF 14 block, in `scene-05` after the `pdf=14` anchor, not
  duplicated, and carried by dialogue record `tirumbippaar-s005-d007`;
- two dialogue records (`tirumbippaar-s006-d012`, `tirumbippaar-s028-d011`) whose live `text` still
  held the superseded `ஊஹூம்` corrected to `ஊஹும்`. No reading layer now contains `ஊஹூம்`.

### Validation — two distinct gates, reported separately

Earlier wording conflated these and wrongly called a normalized result "exact reconstruction".

**A. Strict textual equality** (exact trimmed-line identity; punctuation, ellipses, spacing, quote
glyphs all significant): **1173 of 1342 exact, 169 mismatches** (base was 1156 / 186).

**B. Normalized word-level alignment** (Tamil letters only): **1342 of 1342 aligned, 0 unaligned**
(base was 1325 / 17). This is *alignment*, not exact reconstruction.

Every Tamil-letter reading now matches canonical. The 169 strict mismatches are presentation-layer
only — 140 whitespace, 11 quote/dash glyph, 18 other punctuation (bracket type, ellipsis count). The
previously reported "29" is the whitespace-folded subset (11 + 18) and **still exists**; it is
deliberately untouched, since changing punctuation is outside a reading reconciliation.

### Census — recomputed, not carried over

The old **1040 dialogue / 1321 English unit** baselines are **obsolete and must not be reused**.

| | |
|---|---|
| canonical pages | **104** (PDF 9–112) — 83 `verified` + 21 `verified-reconciled`, 0 draft, 0 review |
| scenes | **93** |
| dialogue records | **1042** |
| translation units | **1330**, all verified |
| dialogue links | **1042 exactly once, 0 duplicates, 0 orphans, 0 unlinked** |
| character entities / labels | 39 / 45 |
| song occurrences | 8 — 3 verified, 5 unresolved, **0 attributed to Kalaignar** |

The **PDF-2 printer-imprint crop remains partial, documented and NON-BLOCKING** — it is front matter,
seven pages before canonical text begins, and is never reconstructed.

Ten `புண்ணகோடி` occurrences remain, all correction-history quotations or audit records and none in
live reading text; they are preserved as evidence. The entity ID `tirumbippaar-char-punnakodi` is
**not renamed** — an internal identifier referenced only within `characters/`, whose display label
already carries the corrected `புண்யகோடி`.

### Status

**D1.1 CONTENT RECONCILIATION: PASS — and source PR #2 is now MERGED**, squash
`d4b394a7b4582935792df4cf2840fbd466dd41c5` (the source `main` at that time; **now superseded by the
D1.2 merge `505b1ea7`**); branch deleted. Post-merge verification on that main: `ஊஹும்` 5/5/5 in transcription, scenes and
dialogues with **zero `ஊஹூம்` anywhere in the work**; the restored `கருடன் : இல்லை பரந்தாமன்.` is
canonical exactly once at the head of the PDF 14 block, in `scene-05` after the `pdf=14` anchor, not
duplicated, and carried by `tirumbippaar-s005-d007`; census 104 pages / 93 scenes / 1042 dialogue
records / 1330 translation units / 1042 links exactly once, 0 duplicates, 0 orphans, 0 unlinked.

## Phase D1.2 — strict derivative-fidelity audit — CONTENT PASS on PR #3 head

**Source PR #2 is merged** at `d4b394a7b4582935792df4cf2840fbd466dd41c5` — the source `main` at that
time, **now superseded by the D1.2 merge `505b1ea7`**. D1.1 is complete.

**D1.2 lives on source PR #3** (`fix/tirumbippaar-strict-derivative-fidelity`), validated on the clean
committed head **`49e1b2c4387190e4fe0aea822f8e68b338dccb9d`**.

The method finding stands: canonical could not serve as the punctuation authority, because it carried
OCR artifacts the scene layer did not, while elsewhere the scene was the faulty layer. Only the
controlling scan decided.

### Closure round

**Scene 45.** The user verified the PDF directly: the source prints `பாண்டியன் : தொழிலாளர்கள்` with no
full stop after the speaker name. Canonical and scene both carried `பாண்டியன். :`; both corrected. The
dialogue record `tirumbippaar-s045-d013` already held `பாண்டியன்` and is unchanged — it was correct and
the defect was above it. **No `பாண்டியன்.` variant created; the inventory stays at 45 exact labels.**

**Heading markers fully closed.** 18 location-opening markers (previous round) and now **22 of 22
scene-number closing markers**, each inspected individually on the scan: 19 that printed `)` and 3 that
had no glyph at all, all corrected to `]`. **0 unresolved.** Source anomalies preserved: scene 5
`காட்சி 5[`, scene 36 with no closing glyph, scene 43 `காட்சி 43].`.

### Gates on `49e1b2c4`

| gate | result |
|---|---|
| canonical↔scene source-visible | **0 mismatches** (1348/1348 exact text and page) |
| page attribution | **0** |
| scene↔dialogue text | **0 unexplained** (2 documented scene-72 records) |
| scene↔dialogue provenance | **0** |
| dialogue↔translation provenance | **0** |
| dialogue links | 1042 exactly once, 0 duplicate, 0 orphan, 0 unlinked |
| character source labels | **45** |
| translation/reader preflight | PASS |
| heading markers | **0 unresolved** |

Census: **104** canonical pages (0 draft, 0 review) · **93** scenes · **1042** dialogue records ·
**1330** translation units. `ஊஹும்` is user-verified and preserved at 5/5/5 with **0 `ஊஹூம்` in live
reading layers**. The **PDF-2 printer-imprint crop remains partial, documented and NON-BLOCKING**.

Reader and EPUB artifacts are **not** committed — CI regenerates them on push to `main`.

### Source PR #3 — MERGED · CI-fix PR #4 — MERGED · publication package COMPLETE

| stage | SHA |
|---|---|
| D1.2 source fidelity, PR #3 reviewed head | `49e1b2c4387190e4fe0aea822f8e68b338dccb9d` |
| PR #3 squash merge | `505b1ea7382bacb39c82d9f314668a67a38219bd` |
| CI-fix PR #4 reviewed head | `9bd4b1f370c7f6602648e5e3e1e7cfced4edd34e` |
| PR #4 squash merge | `b4ab599d8726f45780a72e5d4531d52583b7f220` |
| **CI publication commit — authoritative source pin** | **`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`** |

Both branches deleted; 0 open source PRs. **The authoritative Tirumbippaar source pin is
`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`.**

### Official publication CI — PASSED

`Tirumbippaar English reader QA`, run **`33247433975`** (#288) on `b4ab599d`, event `push`:
**completed / success**, all 11 steps of `qa-and-build` succeeded with **nothing skipped**. The
previously failing migration step now reports *"Reader gates already index-authoritative; nothing to
migrate."* and continues.

| step | result |
|---|---|
| reader preflight | **PASS** |
| whole-work QA | **PASS** — 93 scenes · 1330 units · 1042 dialogue links · 12 cross-page |
| deterministic EPUB 3 package | **PASS** — 93 scenes · 1330 units |
| metadata synchronization | **PASS** |
| generated-package commit | **PASS** — pushed `6a8c59c4`, 8 files |

**Official EPUB:** `works/tirumbippaar/editions/en/tirumbippaar-en.epub`, **370,204 bytes**, SHA-256
**`955ce8adffe318ccbb5f77cb65afebb6951b7c7ac3091343adf2fd3dcb996ae0`** — recomputed from final main and
identical to the CI-reported value, confirming the build is genuinely deterministic. `QA_REPORT.md`
**PASS** (1,330 verified / 0 review / 0 draft); `EPUB_QA_REPORT.md` **PASS**; `manifest.json` and
`package-manifest.json` both `complete-verified`, pinning `source_scan_sha256`
`973b9c3f7b84d6a1902a4a472af8799c783bf1ec2d6cd015796fc1df1ce59682` — the controlling scan.

### Final validation on `6a8c59c4`

| gate | result |
|---|---|
| canonical↔scene | **1348/1348 exact text; 1348/1348 exact text + page; 0 mismatches** |
| page attribution | **0** |
| scene↔dialogue text | **0 unexplained** (2 documented scene-72 structural records) |
| scene↔dialogue provenance | **0** |
| dialogue↔translation provenance | **0** |
| dialogue links | **1042 exactly once**, 0 duplicate, 0 orphan, 0 unlinked |
| translation QA / reader preflight | **PASS** |
| heading surfaces | 18 opening + 22 closing · **0 unresolved** |

Census: **104** canonical pages (83 `verified` + 21 `verified-reconciled`, **0 draft, 0 review**,
`printed = pdf − 8` with 0 violations) · **93** scenes · **1042** dialogue records · **1330**
translation units · **39** character entities / **45** exact source labels · **8** song occurrences
(3 verified, 5 unresolved, **0 attributed to Kalaignar**).

`ஊஹும்` is user-confirmed and preserved at **5/5/5** with **0 `ஊஹூம்` in live reading layers**.
Scene 45 reads **`பாண்டியன் : தொழிலாளர்கள்`** in canonical and scene; `tirumbippaar-s045-d013` holds
`speaker_label` `பாண்டியன்`, text `தொழிலாளர்கள்`, provenance PDF 59 / printed 51, and **no
`பாண்டியன்.` source-label variant exists**. Heading anomalies retained exactly as printed:
**`காட்சி 5[`**, **`காட்சி 36`** (no closing glyph), **`காட்சி 43].`**. The **PDF-2 printer-imprint
crop remains partial, front matter, documented, NON-BLOCKING and never reconstructed**.

### Status

**D1.1 COMPLETE · D1.2 COMPLETE · PUBLICATION PACKAGE COMPLETE.**

**Tirumbippaar source main was released for D2** at
`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`, and that pin is now the published provenance authority
(see Phase D2 below).

*(Historical note, superseded: the earlier publication-CI failure on `505b1ea7` — run `33246879335` —
was a non-idempotent workflow migration step, not a source-content defect. It is fixed and resolved.)*

---

## Phase D2 — திரும்பிப்பார் / Tirumbippaar Digital Library integration — ✅ COMPLETE and CLOSED

**TIRUMBIPPAAR PHASE D COMPLETE.** D1.1 COMPLETE · D1.2 COMPLETE · SOURCE PUBLICATION PACKAGE
COMPLETE · D2.1 COMPLETE · D2.2 COMPLETE · D2.3 COMPLETE · D2.4 COMPLETE · D2.5 COMPLETE.

*(This section previously carried a not-yet-started note for D2. That note was accurate when written
on 2026-08-26, is now superseded, and has been removed rather than left to be misread as current.)*

| | |
|---|---|
| Source pin | `6a8c59c445890e568dfe65cc36c2900dd2a8a0b3` |
| Implementation `main` after D2.4 | `766d68680cecca549d4d752e32561834f7dde0f5` |
| Post-merge Library CI | `33292800096` — success |
| Production deployment | GitHub deployment `6163236518`, environment **Production**, state `success`, for that exact SHA |

**PR chain.** #53 — D2.1 deterministic importer and generated data · #54 — D2.2 reader, scene and
source routes · #55 — D2.3 catalogue entry · #56 — D2.4 sitemap publication.

### Final public state — verified live on 2026-08-30

⚠️ The **site-wide** totals in this paragraph are the 2026-08-30 state and are **superseded** — see
the CURRENT STATE checkpoint at the top. The **Tirumbippaar-specific** figures below remain the
durable record of this benchmark.

25 catalogue works · 3 Cinema Writing works (`manohara → parasakthi → tirumbippaar`, onboarding
order, not year) · 2944 sitemap URLs · **95** of them Tirumbippaar · 2948 clean-build pages.

Route family: `/cinema/tirumbippaar`, `/cinema/tirumbippaar/<93 registry scene slugs>`,
`/cinema/tirumbippaar/source`. All **95** published URLs returned 200 in production; the live sitemap
scene set equals the generated registry exactly — 0 missing, 0 extra, 0 duplicates — and off-registry
slugs (`scene-94`, `scene-00`, `scene-1`, `94`, `caatci-5`) are absent from the sitemap and 404 live.

### Source census — as recorded by the archive at the pin

104 canonical pages · 93 scenes · 1042 dialogue records · 1330 English units · 39 character entities ·
45 exact printed labels · 8 song/performance occurrences (**3 verified to other people, 5 unresolved,
0 attributed to Kalaignar**).

Stored Tamil reading layer: 1320 blocks — 923 dialogue, 273 stage-direction, 30 prose, 94 separator;
1226 non-separator literary blocks. English layer: 1330 units — 1049 dialogue, 262 stage-direction,
7 song-reference, 2 chant, 10 written-text, **0 full song** — with 12 cross-page units.

**The 923 speaker-labelled Tamil blocks and the 1042 immutable dialogue records are deliberately
different granularities, not a mismatch:** ten scenes print one speech across several paragraphs.

### Rights posture — deliberately unset

Catalogue-level present-day rights for the whole publication are **deliberately unset**, following
Parasakthi rather than Manohara. Tirumbippaar is a **composite cinema publication**: Kalaignar's story
and dialogue alongside song/performance material with mixed or unresolved authorship — three
occurrences attributed to others, five unresolved, none attributed to Kalaignar. Asserting
`nationalised-by-tamil-nadu-government` over the whole booklet would claim other people's work as his.
The schema documents absence as equivalent to `unclassified`, so omission is an honest value.

The printed 1953 notice **`உரிமையுடையது.`** is preserved on `/cinema/tirumbippaar/source` as printed
source evidence only, labelled `அச்சிட்ட உரிமை அறிவிப்பு`, and is **not** a present-day determination.
A scoped `WorkAttribution` model for composite works remains separate future project-level work.

Attribution is role-scoped to the printed cover credit **`கதை - வசனம்`** — story and dialogue. The
catalogue card says "Kalaignar's story and dialogue", never that he wrote the songs; the
`LibraryWork` schema has no generic `author` field.

### Settled source-fidelity decisions — do not reopen

- **`ஊஹும்`** — 5 in live production; **`ஊஹூம்`** — 0. The latter is superseded, not an alternative.
- Scene 45 reads **`பாண்டியன் : தொழிலாளர்கள்`**. No `பாண்டியன்.` **source-label** variant exists for
  scene 45. (Stated precisely: the settled finding is about the source-label inventory, which stays at
  45 exact labels — not a broader claim that the string never appeared anywhere in the derivative
  layers. A `பாண்டியன். :` form did occur in canonical and scene text and was corrected upstream in
  D1.2.)
- Headings retained exactly as printed: **`காட்சி 5[`**, **`காட்சி 36`** (no closing glyph),
  **`காட்சி 43].`**.
- The PDF-2 printer-imprint crop stays partial, front matter, documented and never reconstructed.

**Source-visible irregularity is not inferred to be error** merely because expected Tamil spelling,
grammar, gender agreement or punctuation convention would suggest another form. The source page
labels these `அச்சிடப்பட்ட தலைப்பு வேறுபாடுகள்` — differences, not `வழுக்கள்`.

### Reader principles as shipped

Tamil is the default. English **replaces** Tamil on toggle — never two full reading streams at once —
and is labelled a project-created, source-linked reading translation with the Tamil left
authoritative. Speaker labels stay in exact printed Tamil in both modes. Stored Tamil `block.text` is
rendered verbatim and never rebuilt from `speakerLabel + text`. Separators are structural ornament,
`aria-hidden`, never prose, and the archive kind name `separator` never reaches the reading body.
Static params and previous/next come from the generated registry, never numeric arithmetic.

### D2.5 production verification — 2026-08-30

Live `/read` shows Tirumbippaar exactly once, on Cinema Writing, third, linking `/cinema/tirumbippaar`.
The Tamil card description renders by default; switching the global library language (the Navbar
control, persisted as `nn-lang`) renders the English `descEn` in its place — both descriptions have a
real display surface. Landing, scenes 01/05/36/43/45/93 and `/source` all 200; `scene-94` 404. The
Tamil→English→Tamil toggle behaves correctly on scene 45 with 7 Tamil speaker labels retained in
English mode. Separator renders as an `aria-hidden` ★. The source page carries the identifier
`TVA_BOK_0014652`, the pin, the scan SHA-256
`973b9c3f7b84d6a1902a4a472af8799c783bf1ec2d6cd015796fc1df1ce59682`, the edition
`முதல் பதிப்பு: 1953`, the full census and the historical rights notice, with no stale D2.1
route-status note, no universal "stored in no archive" claim, no `உரிமம்`, and no blanket present-day
rights determination. No horizontal overflow at 375px on landing, Tamil scene, English scene or source
page; the scan hash wraps in full rather than truncating. Print emits exactly one reading stream per
mode with navigation and controls hidden.

QA language throughout is **archive-recorded**, **automated QA** and **scan-adjudicated upstream**.
**No human, editorial or expert review of the text is claimed**, because the project has no such layer.

### Outstanding items — separate future work, NOT Tirumbippaar blockers

1. **Manohara source-drift audit** — future work, not started.
2. **Validator migration** — **PAUSED** after the Manohara migration; resume only on explicit owner
   instruction.
3. **`components/ManoharaReader.tsx`** carries the phrase "Kalaignar's original Tamil text". This
   was surfaced during Tirumbippaar review as a separate wording **question**, and was deliberately
   **not adjudicated** there. It is **not** established that it is wrong: `data/library.ts` records
   Manohara's booklet as Kalaignar's work throughout — which is exactly why the nationalisation
   rights model applies to Manohara and not to Parasakthi or Tirumbippaar — so the phrase may well be
   correct for that work. Tirumbippaar needed different wording because Tirumbippaar is composite,
   not because Manohara was found to be. Do not change it without re-checking Manohara's own
   source/attribution model, preferably during the future Manohara source-drift audit. Not a
   Tirumbippaar blocker.
4. **`components/StorySource.tsx`** carries a universal "stored in no archive" scan-storage claim —
   the same wording narrowed for Tirumbippaar in D2.2. Separate question.
5. **Tirumbippaar internal catalogue comment** in `data/library.ts` says song/performance material
   "is not his" while five occurrences are unresolved. Strictly, unresolved authorship does not
   establish that those five are someone else's. Safer future wording: *"song/performance material
   with mixed or unresolved authorship — three attributed to others, five unresolved, none attributed
   to Kalaignar."* Reviewed as **NON-BLOCKING**; it did not trigger an implementation change in D2.5
   and should be folded into a future PR that legitimately edits that comment.
6. **Scoped `WorkAttribution`** rights model for composite works — future project-level issue.

**Do NOT reopen Tirumbippaar** absent an explicit new issue or a new source release.

---

> ⚠️ **SUPERSEDED (2026-09-01) — kept as the status snapshot it was.** Three lines below are no longer
> current: **Phase 3 is ACTIVE, not paused** (the owner-directed pause was lifted); **Speech
> Benchmark #4 is COMPLETE and CLOSED**, not "NOT STARTED and NOT SELECTED"; and **the three blocked
> stage plays have since been published by Bulk Onboarding Wave 1**, taking Drama to 5. See the
> CURRENT STATE checkpoint, the Wave-1 close-out and the Speech Benchmark #4 close-out near the top of
> this document. Everything else in this snapshot stands as written.
>
> **Status:** **Phase 1 COMPLETE** · **Phase 2 (Cinema / Manohara) COMPLETE** · **Phase 3 — Speeches
> is ACTIVE but PAUSED by owner direction (not complete)** · **Phase 4 — Poetry is ACTIVE** ·
> **Phase 5 — Essays & Articles is ACTIVE** · **Phase 6 — Fiction COMPLETE** · **Phase 7 — Drama /
> Stage Plays is ACTIVE (benchmark 1 COMPLETE / MERGED / PRODUCTION-VERIFIED)**.
>
> **Phase 8 — Consolidation & Provenance Parity has NOT started.** No consolidation work, validator,
> CI or component extraction exists yet.
>
> **Owner direction.** The owner explicitly asked for the next Digital Library work to come from a
> category **other than speeches** ("I want from another category other than speech"). That produced
> **Phase 4 — Poetry**. Speech expansion must **not** resume unless the owner explicitly reactivates it.
>
> **Phase 3 — Speeches (ACTIVE but PAUSED):**
>
> - **Benchmark #1 — உதயக் கதிர் / Udhaya Kathir** (assembly speech): **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED** — PR #18, squash `13ddf04f01b6a75024985b6df172deace9d26e80`, verified live
>   2026-08-18.
> - **Benchmark #2 — பூந்தோட்டம் / Poonthottam** (the first **public** speech): **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED** — PR #20, reviewed head `0906919e21066ab9e917985d51f60086823ad8ce`, squash
>   `2777064490910c02f5aa6938b9b6872b15e21e7c`, verified live 2026-08-19. A follow-up
>   presentation/provenance hotfix (PR #21, squash `acb9721127de72c7575c035ccccf877deeb6421e`) is part
>   of that history but is **no longer** the latest application-code checkpoint.
> - **Benchmark #3 — அறப்போர் / Arappor** (`public-speech`): **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED** — PR #23, final reviewed head
>   `06b42db399e1e97762ff9a9d522b63a83995bc03`, squash
>   `ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (2026-08-19T11:51:46Z), production Vercel **success**
>   on that exact squash SHA.
> - **Speech Benchmark #4: NOT STARTED** and **NOT SELECTED**. — ⚠️ **SUPERSEDED (2026-09-01):**
>   Benchmark #4 is now **COMPLETE and CLOSED** (A1 PR #62 `492b26dd…`, A2 PR #63 `56ca0c97…`).
>   **Benchmark #5** is what is now NOT STARTED / NOT SELECTED / NOT AUTHORIZED.
>
> **Phase 4 — Poetry (ACTIVE):**
>
> - **Benchmark #1 — இதயத்தைத் தந்திடு அண்ணா / Lend Me Your Heart, Anna:** **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED** — PR #25, final reviewed head
>   `3653023db60cb51ee1df4d970d621494c095791c`, squash
>   `c2d1c46d1c2d4e1f11722360848226208867789f` (2026-08-20T01:58:07Z), production Vercel **success**
>   on that exact merge SHA (deployment `92kdGyRiKucdUPSywP2XqnZMx1g9`).
> - **Poetry Benchmark #2: NOT STARTED, NOT SELECTED and NOT APPROVED FOR IMPLEMENTATION.** A second
>   work now EXISTS in the source repository — this is a change from the earlier record, which said no
>   second work was available. At live `pugazg/kalaignar-poems` `2230a8d`, `poems/` holds
>   `idhayathai-thanthidu-anna` (released) **and** `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா).
>   `anaiya-vilakku-anna` is **NOT READY**: of 19 source pages only **1** page record exists, Tamil
>   assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and
>   no byte size** — so it does not yet meet the repository's own source-identity step. A candidate
>   source therefore exists, but it is **not approved for implementation**. Phase 4 is **not**
>   complete, and **live source state always wins**.
>
> **Phase 5 — Essays & Articles (ACTIVE):**
>
> - **Benchmark #1 — சக்கரவர்த்தியின் திருமகன் / Chakravarthi's Son:** **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED**. PR #27, final reviewed head
>   `929bb545e5358056ea0e0a671d157d7f97bede6a`, squash merge
>   `bcb11396b2215bc2cc1e81873c0ce278ef98598a` (2026-08-20T10:15:15Z), production Vercel **success**
>   on that exact merge SHA (deployment `AwU8uyXYHxthgez8ZGQWP1rTS3PF`). Source pin
>   `pugazg/kalaignar-essays @ bff35320b668cb5beeaafc5faa58260c4f4473f8`.
> - **Phase-5 Benchmark #2: NOT STARTED and NOT SELECTED.**
>
> **Phase 6 — Fiction (COMPLETE):**
>
> - **Benchmark #1 — பலிபீடம் நோக்கி / Towards the Sacrificial Altar:** **COMPLETE / MERGED /
>   PRODUCTION-VERIFIED** — PR #28, squash `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a`. Source pin
>   `pugazg/kalaignar-novels @ 9e80c567d4a2165178c5374a02210240140685bf`. ONE novel in three assembled
>   sections; `ராயசம் வெங்கண்ணா` is an internal sequence of that novel, never a separate work.
> - **Phase-6 Benchmark #2: NOT STARTED and NOT SELECTED.**
>
> **Phase 7 — Drama / Stage Plays (ACTIVE):**
>
> - **Benchmark #1 — சிலப்பதிகாரம் நாடகக் காப்பியம்:** **COMPLETE / MERGED / PRODUCTION-VERIFIED** —
>   PR #29, squash `9aade1d441bb314b5ab62f97b87b373d33db08c5` (2026-08-21T01:09:13Z), production
>   verified 2026-08-21. Source pin
>   `pugazg/kalaignar-stage-plays @ a66e62bbecaf63825b3db09a1d421401e1ab2e8e`. 38 numbered scenes plus
>   a separate **unnumbered** closing tableau, which is never Scene 39.
> - **Phase-7 Benchmark #2: NOT STARTED and NOT SELECTED.** `Anarkali`, `Cheran Senguttuvan` and
>   `Socrates` have **no controlling Tamil source** and remain blocked. — ⚠️ **SUPERSEDED
>   (2026-09-01):** controlling Tamil sources were released, and those three plus `Bharathayanam`
>   were published by **Bulk Onboarding Wave 1**. Drama is now **5**.
>
> **Last production application-code checkpoint:
> `9aade1d441bb314b5ab62f97b87b373d33db08c5`** (the Phase-7 Drama Benchmark #1 / PR #29 squash merge,
> production-verified 2026-08-21). It **supersedes**
> `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (Phase 6),
> `bcb11396b2215bc2cc1e81873c0ce278ef98598a` (Phase 5),
> `c2d1c46d1c2d4e1f11722360848226208867789f` (Phase 4) and
> `ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (Phase 3), all of which remain important **historical**
> checkpoints but are no longer current.
>
> `/read` publishes **11 works across 9 non-empty shelves** — every shelf is now non-empty. The
> published works are: Nenjukku Neethi · Murasoli Letters · Tholkappiya Poonga · Manohara ·
> Udhaya Kathir · Poonthottam · Arappor · Idhayathai Thanthidu Anna · Sakkaravarththiyin Thirumagan ·
> Balipeedam Nokki · Silappathikaram Nadaka Kappiyam. **புனைவு / Fiction**, **நாடகங்கள் / Drama**,
> **கட்டுரைகள் / Essays & Articles** and **கவிதைகள் / Poetry** each hold **exactly one** work; the
> single **Speeches** shelf holds **3** (Udhaya Kathir · Poonthottam · Arappor). No `/essays`,
> `/novels`, `/plays` or other collection landing exists. **Verify this live rather than trusting the
> numbers.**
>
>
> _(Historical: `c2d1c46d1c2d4e1f11722360848226208867789f` was the application-code checkpoint at the
> close of Phase-4 Poetry Benchmark #1, superseding the Phase-3 checkpoint
> `ecf73cc8146cd9a9578c4aeaf73518b122ce569c`. Both are historical; the current checkpoint is stated
> above.)_
>
> **Current repository `main` must always be read live from GitHub.** Documentation-only closeout
> commits — including the handover PRs that accompany this update — may move repository `main` beyond
> the application-code checkpoint **without changing deployed application behaviour**, so treat
> `9aade1d4…` as the production application-code state, not as the newest commit on `main`, and never
> record a docs-only SHA as a newer application-code checkpoint.
>
> _(At the close of Phase 4 the library published 8 works across 6 shelves.)_ No separate Public
> Speeches shelf exists, and no `/speeches`, `/poems` or `/essays` collection landing was added. See
> **§10 → Phase 3**, **§10 → Phase 4**, **§10 → Phase 5**, **§10 → Phase 6** and **§10 → Phase 7**
> for the full records.
>
> Mobile remains **ON HOLD** (Activity 6 / PR #15 merged for preservation — see §4).

This is the durable cross-chat handover for the **web Reading Room / Kalaignar Digital Library** at `https://nenjukkuneethi.org/read`.

The native mobile app work is **on hold by owner decision** while this web-library expansion is prioritised. Mobile history remains preserved separately under `projects/kalaignar-autobiography/`.

---

## 1. Canonical repositories and roles

### Web implementation / production site

- **Implementation repository:** `pugazg/kalaignar-autobiography`
- **Production site:** `https://nenjukkuneethi.org`
- **Current Reading Room:** `https://nenjukkuneethi.org/read`

The implementation repository remains authoritative for the deployed Next.js site and intentionally imported reader data.

### Cross-chat control repository

- **Tracking / handover repository:** `pugazg/kalaignar-tribute`
- This file is the authoritative high-level plan and continuation state for the Digital Library expansion.

### Source/archive repositories to integrate

The source repositories remain authoritative for their own archival Tamil, translations, verification state and provenance. The website must consume or vendor **released/verified derivatives from those source repositories**; it must never silently rewrite archival source text.

1. `pugazg/kalaignar-novels`
2. `pugazg/kalaignar-short-stories`
3. `pugazg/kalaignar-poems`
4. `pugazg/kalaignar-assembly-speeches`
5. `pugazg/kalaignar-essays`
6. `pugazg/kalaignar-cinema-works`
7. `pugazg/kalaignar-literary-commentary`
8. `pugazg/kalaignar-stage-plays`
9. `pugazg/kalaignar-public-speeches`

Future Kalaignar source repositories may be added without redesigning the library taxonomy.

---

## 2. Current public Reading Room baseline

> **Superseded by Phase 1 (see §10):** `/read` is no longer memoir-centric — it is now the
> catalog-driven Digital Library landing, and the memoir's own library/search UI moved to
> `/read/nenjukku-neethi`. The description below is the pre-Phase-1 baseline, kept for history.

Before Phase 1, the public Reading Room presented three peer collections _(historical)_:

1. **நெஞ்சுக்கு நீதி / Nenjukku Neethi**
   - 6 volumes
   - 391 chapters
2. **முரசொலி கடிதங்கள் / Murasoli Letters**
   - current structured archive covers letters from the 2013–2016 period represented by volumes 48–54
   - 346 curated letters in the current implementation data
3. **தொல்காப்பியப் பூங்கா / Tholkappiya Poonga**

Before Phase 1, the `/read` page was still structurally memoir-centric _(historical)_:

- `app/read/page.tsx` renders `components/Library.tsx`;
- page metadata still describes the six-volume memoir specifically;
- `components/Library.tsx` hard-codes the three current collection cards;
- memoir title/full-text search, volume filters, resume/read/bookmark features all live directly on this page.

This architecture was appropriate when `/read` was primarily the memoir reader, but it will not scale to a complete Kalaignar library.

### Existing routes must be preserved

Do not break working deep links merely to make URLs aesthetically uniform.

In particular preserve current working reader URLs while the library shell evolves, including:

- existing memoir chapter routes under `/read/[id]`;
- existing Murasoli routes under `/murasoli`;
- existing Tholkappiya Poonga routes under `/tholkappiyam`.

New catalog/navigation layers may link to these existing destinations first. Route normalization can be a later, explicit migration with redirects.

---

## 3. Critical correction — accidental Manohara files in the website repository are NOT an integration source

The implementation repository currently contains files under:

`public/data/cinema/manohara/parts/`

and live history includes commits titled `Vendor Manohara reader part 001` through at least `Vendor Manohara reader part 020`.

**Owner correction:** these files were accidentally added while work was being carried out in the separate `pugazg/kalaignar-cinema-works` source/archive repository. They are **not an approved Digital Library integration, not a continuation boundary, and not a source of truth for Manohara**.

For every future Manohara Reading Room activity:

- **ignore those website-repository Manohara files as input/reference;**
- do not continue from them;
- do not compare source-repository output against them as though they were an accepted prior import;
- do not derive counts, scene text, translations, provenance, metadata or reader structure from them;
- do not use their commit sequence to decide where integration should resume;
- obtain Manohara only from the live authoritative `pugazg/kalaignar-cinema-works` repository, after inspecting its current release/reader-export state;
- record the exact source-repository commit/integrity state used for the real Digital Library import.

During Phase 1, the accidental files may simply remain untouched because cinema integration is out of scope. Their later deletion/replacement/cleanup must be deliberate and must not be mistaken for archival-source editing.

This correction overrides all older notes saying to “protect”, “continue”, or “resume from” the website's Manohara vendor boundary.

---

## 4. Owner decision — mobile app paused

The owner has explicitly chosen to **put mobile app development on hold** for now and concentrate on the web Reading Room / Digital Library.

Do not start new mobile production-readiness work unless the owner reactivates it.

Mobile **Activity 6 / PR #15** (`mobile/offline-network-readiness`) has now been **merged into
implementation `main` for durable preservation** (squash merge SHA
`36d1325e9dc04084ed84cb50a2d0c3f6a665b795`, 2026-08-18) — offline/network status, launch/cache
reliability, and retry on all content-failure surfaces, with **no privacy-model change**. This was
a preservation merge only: **mobile development remains ON HOLD**, no new mobile activity is active,
and the active next workstream is the **Phase 3 web Digital Library** work. Do not treat PR #15 as
open/unmerged after this point, and do not start new mobile features unless the owner reactivates
mobile development.

---

# 5. Product direction

The Reading Room must evolve from a three-item memoir-oriented page into a **scalable Kalaignar Digital Library** capable of housing his works by literary/public form while preserving each source archive's structure.

The goal is not to force every work into one generic text shape.

The goal is:

> **one coherent library, multiple source-faithful reader types.**

The library shell should feel unified, while a poem remains a poem, a stage play remains scene/dialogue-based, an Assembly speech preserves exchanges/interjections, and a commentary work preserves its own unit structure.

---

# 6. Decided information architecture

## 6.1 Library home

`/read` becomes the **Kalaignar Digital Library landing page** rather than the memoir's internal library/search page.

Recommended public heading:

- Tamil: **கலைஞர் மின்னூலகம்**
- English: **Kalaignar Digital Library**

"Reading Room" may remain as a secondary experience label/subtitle, but the page should communicate that it is a multi-genre digital library.

The current memoir-specific text such as page counts / OCR wording belongs on the Nenjukku Neethi work/collection surface, not in the global library introduction.

## 6.2 Top-level shelves

Use these stable conceptual shelves:

1. **வாழ்க்கை எழுத்து / Life Writing**
   - Nenjukku Neethi / autobiography / memoir
2. **கடிதங்கள் / Letters**
   - Murasoli letters
3. **புனைகதை / Fiction**
   - Novels
   - Short stories
4. **கவிதைகள் / Poetry**
5. **நாடகங்கள் / Drama**
   - Stage plays / dramatic works
6. **திரை எழுத்து / Cinema Writing**
   - Screenplay, dialogue, cinema writing
7. **உரைகள் / Speeches**
   - Public speeches
   - Legislative Assembly speeches
8. **கட்டுரைகள் / Essays & Articles**
9. **இலக்கிய உரை / Literary Commentary**
   - Tholkappiya Poonga
   - Thirukkural — Kalaignar Commentary
   - future Sangatamil, Kuraloviyam and related works

This nine-shelf model is intentionally broader than repository names. Repository boundaries are archival/engineering boundaries; the public library should use reader-friendly literary forms.

## 6.3 Empty shelves

The architecture may support all shelves immediately, but the public site should **not render misleading empty categories or invented "coming soon" promises by default**.

Only publish a shelf/card when it contains at least one intentionally exposed catalog item, unless the owner explicitly asks for a public roadmap display.

---

# 7. Catalog-first architecture

The current three collection cards are hard-coded in `Library.tsx`. That must be replaced by a catalog-driven model before mass integration.

Create one normalized library catalog in the implementation repository. Exact file names may be chosen after inspecting current conventions, but conceptually each work entry should support:

- stable `id` / `slug`;
- Tamil title;
- English title where appropriate;
- shelf/category;
- subtype (`novel`, `short-story`, `poem`, `stage-play`, `cinema`, `public-speech`, `assembly-speech`, etc.);
- source repository;
- source work path;
- source/release commit or integrity identifier where practical;
- publication/edition metadata when established;
- Tamil availability/status;
- English availability/status and translation type where relevant;
- reader structure (`volume-chapter`, `letter`, `scene`, `article`, `speech`, `poem`, `story`, `commentary-unit`, etc.);
- unit counts where source-supported;
- public reader href;
- provenance/source-note href;
- publication state (`published`, `ready-to-integrate`, `archival-in-progress`, etc.) for internal control.

Public UI must be driven by **published** entries, not by repository existence alone.

---

# 8. Source-of-truth and integration contract

## 8.1 Source repositories remain canonical

Do not edit a typo, translation, speaker label, scene boundary, poem lineation or source note in the website merely because it looks awkward.

Corrections belong in the authoritative source repository first, through that repository's archival workflow.

For Manohara specifically, `pugazg/kalaignar-cinema-works` is the only approved archival/reader-export source. Accidental files already present in `kalaignar-autobiography/public/data/cinema/manohara/` have no source-authority status.

## 8.2 Website uses derived/vendored reader artifacts

Preferred model:

1. source repository reaches an explicit reader/release gate;
2. website integration identifies the exact source repository path + commit/integrity state;
3. deterministic/importable reader data is vendored or generated into `kalaignar-autobiography`;
4. public catalog entry records provenance;
5. site build validates the imported structure.

Do **not** make the production site depend on live GitHub API calls at reader runtime.

Do **not** treat previously accidental website files as a substitute for step 1 or step 2.

## 8.3 No single forced schema for prose content

Use a shared catalog envelope but allow reader adapters by form.

Examples:

- memoir → volume/chapter reader;
- letters → letter reader;
- novels / short stories → work/section reader;
- poems → line/stanza-preserving reader;
- essays → publication/article reader;
- public speeches → source/speech-section reader;
- Assembly speeches → dated legislative speech reader preserving interjections/exchanges;
- stage plays → scene/speaker/stage-direction reader;
- cinema → scene/dialogue/stage-direction reader;
- literary commentary → work-specific commentary unit reader.

---

# 9. Current source-repository readiness inventory

This inventory is a planning snapshot. **Always inspect live `main` before integration.**

## 9.1 Novels — `pugazg/kalaignar-novels`

Current completed reference work:

- **பலிபீடம் நோக்கி** — **INTEGRATED** as Phase-6 Fiction Benchmark #1 (see §10 → Phase 6)
- Tamil 34/34 verified
- assembled Tamil passed
- English verified
- repository status: archival package **RELEASE-READY**
- integrated source pin: `9e80c567d4a2165178c5374a02210240140685bf`

Important structural rule: `ராயசம் வெங்கண்ணா` is an embedded sequence inside the same work, not a
separate novel/work.

**Spelling — source-backed correction.** The name of that embedded sequence is
**`ராயசம் வெங்கண்ணா` / Rayasam Venganna**. The reading was taken from the **controlling scanned
source edition** — the printed title card and the body text of the 1947 first edition — and the
archive was corrected at `pugazg/kalaignar-novels` `9e80c56` before the work was integrated. The
earlier form `ராயசம் வெங்கண்ணு` / Rayasam Vengannu is **superseded**; it is recorded here only so
older notes can be recognised, and it is **not** an alternative reading.

## 9.2 Short stories — `pugazg/kalaignar-short-stories`

Current completed work:

- **கிழவன் கனவு**
- story body 16/16 verified
- English complete / source-complete / release-ready

Non-story front matter may have separate unresolved physical-copy records, but the story body is closed.

## 9.3 Poetry — `pugazg/kalaignar-poems`

Current completed work:

- **இதயத்தைத் தந்திடு அண்ணா**
- Tamil source complete
- English translation release-complete
- lineation/cadence/voice must be preserved
- **INTEGRATED** as Phase-4 Poetry Benchmark #1 at pin
  `42c156d7242fa799ea80adbb0c5f2b9eba078fe9` — see **§10 → Phase 4**. Live `main` has since moved to
  `2230a8d`, which adds a SECOND work directory, `poems/anaiya-vilakku-anna`. `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**.
  A Benchmark #2 candidate must be
  chosen from **live** repository state, not from this snapshot.

## 9.4 Assembly speeches — `pugazg/kalaignar-assembly-speeches`

The 2007 industrial-speeches anthology contributes 10 fully released dated speeches with verified Tamil + English, and the repository also contains the separately archived 1970 no-confidence-motion speech.

Machine-readable index exists at `data/speeches.json`.

This repository is one of the strongest candidates for catalog-driven integration because its speech units are explicitly dated and structured.

## 9.5 Essays — `pugazg/kalaignar-essays`

Current completed publication:

- **சக்கரவர்த்தியின் திருமகன்**
- 14 Tamil articles
- Tamil source/fidelity complete and frozen
- English translation/release complete

Contents-heading variants and other source-witness distinctions must remain preserved.

**INTEGRATED** as Phase-5 Essays & Articles Benchmark #1 at pin
`bff35320b668cb5beeaafc5faa58260c4f4473f8` — see **§10 → Phase 5**. Any further Essays work must be
chosen from **live** repository state, not from this snapshot.

## 9.6 Cinema — `pugazg/kalaignar-cinema-works`

This repository explicitly identifies the Reading Room as the preferred public destination and already has reader/export-ready material.

Current major completed works include:

- **மனோகரா / Manohara** — 57 archival scenes; Tamil verified; English reader/export package verified;
- **பராசக்தி / Parasakthi** — verified Tamil scene/dialogue derivatives and complete verified English reader/export;
- **திரும்பிப்பார்! / Tirumbippaar!** — 93 scenes; verified Tamil derivatives; complete verified English reader/export.

Cinema should normally be read **by scene**, preserving speaker labels, stage directions and provenance. Scene IDs derived by the archive must not be misrepresented as printed source scene numbers when the source has none.

**Manohara remains the recommended first new Cinema integration because the authoritative cinema source repository has mature verified reader/export output — not because of the accidental files already present in the website repository.**

When Manohara integration begins, start from the live `pugazg/kalaignar-cinema-works` release/reader-export artifacts and their exact commit/integrity state. Do not continue from `kalaignar-autobiography/public/data/cinema/manohara/parts/`.

## 9.7 Literary commentary — `pugazg/kalaignar-literary-commentary`

Existing site already includes **Tholkappiya Poonga** from the implementation repository's current data.

Separate repository current state includes:

- **திருக்குறள் — கலைஞர் உரை** Tamil archival-ready through Kural 1325;
- project English released through Kural 1225;
- Part 014 English draft exists but still has a source-check gate;
- final Part 015 Tamil work has not yet been created on `main` at the snapshot time.

Therefore do **not** present Thirukkural commentary as a complete finished library work until the actual source repository reaches the intended publication boundary. Partial publication would require an explicit owner/editorial decision.

Future planned works in this category include Sangatamil and Kuraloviyam when their sources are archived.

## 9.8 Stage plays — `pugazg/kalaignar-stage-plays`

Current canonical Tamil work ready for future integration:

- **சிலப்பதிகாரம் — நாடகக் காப்பியம்**
- Tamil archive complete/pass
- 38 scenes + closing tableau
- independent English translation complete/ready

The 2009 English one-act-play material for Anarkali / Cheran Senguttuvan / Socrates is a **secondary witness**, not a substitute for missing Tamil controlling sources. Do not publish it as though canonical Tamil archival work exists.

## 9.9 Public speeches — `pugazg/kalaignar-public-speeches`

Completed verified Tamil + English public-speech/source units currently include:

- **அறப்போர்**
- **இதய பேரிகை**
- **பூந்தோட்டம்**
- **பள்ளி வாழ்க்கை**
- **கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** (audio-derived archive)

The source repositories deliberately distinguish a true dated speech from compilations/booklets whose source does not establish one single event. The website must preserve that distinction.

---

# 10. Decided implementation sequence

Do not attempt to integrate all repositories in one giant PR.

## Phase 0 — planning / state protection — COMPLETE by this handover

- Mobile development put on hold.
- Digital Library becomes active priority.
- Source repository inventory established.
- Public taxonomy decided.
- Accidental website-repository Manohara files identified as **non-authoritative and excluded from future integration inputs**.

## Phase 1 — Library Foundation — ✅ COMPLETE

**Merged and live in production, verified 2026-08-17.**

- **Implementation repository:** `pugazg/kalaignar-autobiography`
- **Phase-1 PR:** #16 — _Digital Library Phase 1 — library foundation and catalog architecture_
  (squash-merged; feature branch `digital-library/phase-1-foundation` deleted)
- **Merged implementation `main` SHA:** `645cbbe67e6efa2fcd8870140f03267b1a56cfeb`
- **Production verification date:** 2026-08-17 (checked on `https://nenjukkuneethi.org`, not a
  PR preview)
- **Implementation-repo Phase-1 handover:** `docs/digital-library/PHASE1_HANDOVER.md`

What shipped:

- **`/read` = the global Kalaignar Digital Library landing** (கலைஞர் மின்னூலகம்), catalog-driven,
  no memoir-specific global identity.
- **`/read/nenjukku-neethi` = the memoir collection surface** — the relocated memoir library:
  title + full-text search, volume filters, progress / continue / bookmarks.
- **`/read/[id]` memoir chapter deep links preserved** (e.g. `/read/v1-ch01`), along with `nn-*`
  localStorage state, `?find=` deep links, share/citation URLs. Memoir "Contents" backlinks now
  target `/read/nenjukku-neethi`.
- **`/murasoli` and `/tholkappiyam` (and their readers/deep links) preserved unchanged.**
- **Nine-shelf taxonomy encoded** in `data/library.ts` (`SHELVES`); **only non-empty shelves
  render** (`visibleShelves()`), so the live landing shows exactly Life Writing, Letters, and
  Literary Commentary. No "coming soon" placeholders.
- **Three currently-published works:** Nenjukku Neethi (Life Writing), Murasoli — The Letters
  (Letters), Tholkappiya Poonga (Literary Commentary). Rendered from catalog data, not a
  hard-coded array. Public rendering is driven only by `state: "published"`; there is **no
  filesystem auto-discovery**.
- **Murasoli coverage correction:** Murasoli Tamil availability is **`partial`** at the intended
  collection boundary (only volumes 48–54 of the full letters collection are integrated) — it is
  no longer falsely `complete`.
- **English coverage vs English provenance modeled separately:** `Availability`
  (`complete|partial|none`) for coverage, and a distinct optional `EnglishKind`
  (`project-created | separately-published | published-source-witness`) for provenance/kind
  (left unset for all three legacy works — not guessed).
- **Manohara:** no catalog entry, no Cinema Writing shelf, no dependency on the accidental
  `public/data/cinema/manohara/parts/` files (left untouched and non-authoritative).
- **No mobile changes** (mobile PR #15 untouched) and **no archival/source-text or PDF changes**.

Phase 1 was an information-architecture/refactor activity, not a mass content import.

## Phase 2 — Cinema / Manohara — ✅ COMPLETE

**Merged and live in production, verified 2026-08-18.** First **Cinema Writing** work onboarded;
`/read` now shows four works across four shelves.

- **Implementation repository:** `pugazg/kalaignar-autobiography`
- **Phase-2 PR:** #17 — _Digital Library Phase 2 — Manohara cinema reader_ (squash-merged)
- **Final pre-merge PR head:** `ea0b01399cbb1df9c9fe932b54c9f039cbc04602`
- **Implementation `main` merge SHA:** `ae2f2a6d5c2f8293a0f9a2b2c4fc0c0124f44119`
- **Production deployment verification date:** 2026-08-18 (Vercel Production deployment for the
  merge SHA = success; checked on `https://nenjukkuneethi.org`, not a PR preview)
- **Implementation-repo Phase-2 handover:** `docs/digital-library/PHASE2_MANOHARA_HANDOVER.md`

**Source (authoritative, unmodified):**

- Source repo/path: `pugazg/kalaignar-cinema-works` @ `works/manohara`
- Source commit: `4b5f3238bd1e5983e995ddd85cd8a81ae27de21d`
- Source scan SHA-256: `87518fd8c290d7880aa2ddd9f2b5999c9d421d48fe1f02d61cf8e254393236a9`
- No source-repository modification was part of this phase.

**Segmentation:**

- **57 archive-created navigation segments.** The 1954 booklet **prints no numbered scenes**
  (`sourceSceneNumber = null`, `sourceSceneNumbering: none-printed`). These are never described
  publicly as source/printed scenes — the reader and source page say "archive segment N of 57".

**Tamil:** complete-verified source derivative — no normalization / modernization / rewriting.

**English:** complete-verified, **project-created** source-linked derivative — 1190 units; exact
speaker labels; **null speakers preserved**; per-unit source record / occurrence / page provenance
preserved, including **17 exact cross-page English-page-segment records**; no invented song lyrics.
(Counts kept distinct: **27** source-unlabelled **spoken** units, vs the broader null-speaker /
non-dialogue provenance population — the latter is *not* labelled "source-unlabelled spoken units".)

**Accidental data:** the old `public/data/cinema/manohara/parts/` tree was removed as
non-authoritative implementation cleanup — **never** used as source, reference, baseline, or
validation.

**Rights (nationalisation model established):**

- Kalaignar-authored underlying work: **nationalised by the Government of Tamil Nadu** (Tamil:
  **நாட்டுடைமை / நாட்டுடைமையாக்கப்பட்டது**).
- Announcement: **2024-08-22** (without royalty).
- Government Order **public handover to Rajathi Ammal: 2024-12-22** — recorded strictly as the
  handover date, **not** the GO issue date.
- GO **number: null / unverified**; GO **formal issue date: null / unverified** — awaiting direct
  verification from the order itself; never inferred.
- The historical **1954 printed rights notice** (`உரிமை : ஆசிரியருக்கே.`) remains a **separate
  source witness**, not the present status.
- The **project-created English translation** has separate provenance; **third-party material** is
  treated separately.
- A reusable `WorkRights` catalog model was introduced. **A dedicated future rights audit** should
  bring the other existing Kalaignar Digital Library works onto this same model and record the GO
  number/issue date once verified. **No rights migration of existing works was performed here.**

**Scope:** web-only. **No mobile changes** (Phase 2 did not touch mobile; mobile PR #15 was
separate and has since been merged on its own — see §4) and **no archival/source-repo or PDF
changes**. No generalized ingestion framework.

**Not started (deliberately out of scope for this phase):** Parasakthi, Tirumbippaar, or any other
cinema work — each future cinema work is integrated one at a time from its source-repository
release output, on the same source-faithful terms.

## Phase 3 — Speeches — 🚧 ACTIVE (benchmarks 1, 2, 3 and 4 COMPLETE / MERGED / PRODUCTION-VERIFIED)

**Phase 3 is ACTIVE and NOT complete.** Four benchmarks are done — one assembly speech and three
public speeches — and the shared speech architecture is proven end-to-end across **both**
`assembly-speech` and `public-speech`, on one shelf, one reader and one provenance page, now
including a source that establishes **no** date, venue or event. Many more released speeches remain.

> ⚠️ **SUPERSEDED (2026-09-01).** This paragraph previously read *"Benchmark #4 has NOT been started
> and is NOT selected by this handover"*, and the phase was carried as **PAUSED by owner direction**.
> Both statements are **historical**. **Speech Benchmark #4 is COMPLETE and CLOSED** — see
> _Speech Benchmark #4 — கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை_ near the top of
> this document. The pause was lifted before that benchmark ran. **No Benchmark #5 is started,
> selected or authorized**, and no further speech work may begin without explicit owner
> authorization.

Implementation began from the post-mobile-merge `main`
(`36d1325e9dc04084ed84cb50a2d0c3f6a665b795`) and was merged back on **2026-08-18**.

- **Phase-3 branch:** `digital-library/phase-3-speeches`
- **Phase-3 PR:** #18 — _Digital Library Phase 3 — Speeches: Udhaya Kathir_ (**squash-merged**)
  - **Final pre-merge head:** `a3f6c43d28ecccebf250d8596e35767c7be782f9`
  - **Squash-merge SHA (implementation `main`):** `13ddf04f01b6a75024985b6df172deace9d26e80`
  - **Production-verified:** 2026-08-18 at `https://nenjukkuneethi.org` on the exact merge SHA
    (Vercel production deployment succeeded; reader + source pages confirmed live).
- **Implementation-repo Phase-3 handover:** `docs/digital-library/PHASE3_SPEECHES_HANDOVER.md`
- **First benchmark:** `udhaya-kathir` — உதயக் கதிர் / Udhaya Kathir (Tamil Nadu Legislative
  Assembly, 1970-09-09; reply to the no-confidence-motion debate). Chosen on **source readiness** as
  the strongest fully-released assembly speech (standalone 1970 booklet `TVA_BOK_0065650`; verified
  Tamil + verified faithful English; 29 printed section headings; speech pp. 5–46 of 48).
- **Source (pinned, unmodified):** `pugazg/kalaignar-assembly-speeches`
  @ `b1b82402642d8f2cf36927d4752c8e7d28142fdd` (still the current Udhaya pin). Both speech repos were
  inspected during this activity (`kalaignar-assembly-speeches` @ `b1b8240`,
  `kalaignar-public-speeches` @ `c8abf95` — the latter is a **HISTORICAL Benchmark-#1 inspection
  snapshot only**; the current public-speeches pin is `1ef73a709a343390befe55dcdfb029427f527bf4`, see
  Benchmark #2 below); both hold fully-released verified works. Deterministic importer, fail-closed on source-HEAD mismatch; no PDF
  vendoring; no runtime GitHub access. **Assembly inventory is now 11 indexed speeches** (10
  industrial-anthology + the separately archived Udhaya Kathir).
- **Public model:** the single **Speeches** shelf (`உரைகள்`); `assembly` / `public` are **subtypes**
  (`subtype: "assembly-speech"` / `"public-speech"`), **not** separate public shelves. Routes are
  flat `/speeches/<slug>` (+ `/source`); repository names are not exposed as route taxonomy. New
  `readerStructure: "speech"` reader (long-form prose with printed headings — not scene
  segmentation); source provenance preserved in the vendored data; nationalisation rights model
  reused (GO number/issue date still unverified).
- **Honest boundary model (proven here):** page boundaries are audited explicitly, never inferred
  from punctuation. Tamil carries a full **41-transition** boundary audit (relation + lexical join
  per page break); English classifies all **42** `Source page N` anchors. The audited Tamil result is
  **41 transitions = 31 source-established same-paragraph continuations + 3 source-established
  paragraph boundaries + 7 unresolved printed-paragraph relationships** (0 heading boundaries), with
  lexical joins **none 10 / space 16 / unknown 5**. ("Speaker turn" is the per-transition *evidence*
  for those three boundaries — not the generic meaning of the `paragraphBoundary` field, which counts
  source-established paragraph boundaries for any subtype.) Two classes of source
  fact remain **unresolved and are shown as unresolved, not guessed**:
  - **7 unresolved printed-paragraph relationships** — grouped as `unresolved-break` (`role="group"`),
    not asserted as clean logical paragraphs;
  - **5 unresolved lexical joins** (sandhi cross-page) — encoded `joinToNext: "unknown"`, both
    verbatim source fragments preserved with a neutral inline source-page marker (neither space nor
    concatenation asserted).
  Both classes are **source-evidence limitations**, not implementation defects. **Durable rule:**
  resolving either requires an **upstream source-archive visual review** of the controlling scan
  (`TVA_BOK_0065650`) that explicitly records the missing printed fact — the paragraph relation, or
  the exact joined-vs-spaced form. The source PDF is not vendored, and **this Digital Library does not
  establish those typographic facts independently**; rendering stays neutral until the archive settles
  them, **without changing source authority**. Both remain visible at
  `/speeches/udhaya-kathir/source` and in `provenance.json`. _(Earlier revisions framed this as whether
  the scan was reachable in the integration environment; that was a temporary workflow observation, not
  durable provenance, and was corrected by implementation PR #21.)_
- **Done in the Benchmark-#1 activity _(historical record of that activity)_:** readiness inventory
  across both repos; benchmark selected; Phase-3 data/reader/importer architecture; ONE benchmark
  integrated, validated, published, **squash-merged and production-verified** on the Speeches shelf;
  its source/provenance page with both blocker classes. **Not done in that activity (deliberate):** any
  second speech, bulk assembly/public import, a `/speeches` collection landing, Essays/Fiction/Poetry,
  another cinema work, mobile features, a generalized ingestion framework, or the project-wide
  existing-works rights audit. _(The "no second speech" line describes that activity only — Benchmark #2
  has since been completed; see below.)_

### Benchmark #2 — பூந்தோட்டம் / Poonthottam (public speech) — ✅ COMPLETE

The **first public-speech subtype**, proving the shared architecture carries both subtypes without a
second reader and without losing their distinct source metadata.

- **Implementation PR:** #20 — reviewed head `0906919e21066ab9e917985d51f60086823ad8ce`, squash merge
  **`2777064490910c02f5aa6938b9b6872b15e21e7c`** (2026-08-19T09:40:26Z), **production-verified
  2026-08-19** on the exact merge SHA.
- **Source (pinned, unmodified):** `pugazg/kalaignar-public-speeches` @
  **`1ef73a709a343390befe55dcdfb029427f527bf4`** — the current authoritative public-speeches pin,
  being the squash merge of source-correction **PR #1** in that archive (closed/merged; both layers
  `verified-complete`). Controlling scan `TVA_BOK_0065784` (SHA-256 `2a8bf5f6…`, 18 PDF pages).
- **Same Speeches shelf** — `subtype: "public-speech"`, routes `/speeches/poonthottam` (+ `/source`).
  No separate Public Speeches shelf, no new taxonomy.
- **Corrected canonical text:** Tamil **`மாடப்புறா`** (the superseded `மாட்டுப்புறா` is absent);
  English **`humanity`** and **`dove`** (no `mattuppura`, no untranslated `மானிடம்`); **five**
  translator notes.
- **Source-established metadata only:** speech date **1951-12-06**, venue
  **சென்னை கிண்டி இன்ஜினியரிங் கல்லூரி** — **no invented event/occasion/audience**. Scan pages **6–17**,
  printed pages **5–16**, **12** speech pages.
- **Boundary model: 11 transitions = 3 source-established same-paragraph continuations + 8 unresolved
  printed-paragraph relationships + 0 source-established clean paragraph boundaries**; lexical joins
  **none 0 / space 3 / unknown 0**. The **0** is the **source archive's silence**, not a single-speaker
  inference; no punctuation or speaker-count heuristic is used. **Unresolved relations stay
  unresolved** and render neutrally.

### Post-production provenance hotfix — implementation PR #21 — ✅ COMPLETE

Production verification of PR #20 surfaced a **presentation/provenance defect only — no canonical
content change**.

- **PR #21** — reviewed head `4135c29ed3a2ad1322397a68d1f4d4b09c840d45`, squash merge
  **`acb9721127de72c7575c035ccccf877deeb6421e`** (**superseded** as the application-code checkpoint by
  Benchmark #3 / PR #23 — see below), **production-verified 2026-08-19**.
- Durable blocker **`resolution`** is now actually **rendered** (it existed but was never shown);
  temporary **environment-availability wording** is gone from the Tamil presentation; the generic label
  is now **"Source-established paragraph boundaries" / "மூலத்தால் உறுதிசெய்யப்பட்ட பத்தி எல்லைகள்"**
  instead of "speaker turn"; Udhaya's generated blocker resolutions were cleaned to the durable
  upstream-review wording; both validators hardened against regression.
- **Both `speech.json` files stayed byte-identical.** Verified live afterwards: **Poonthottam
  source-established paragraph boundaries = 0**; **Udhaya = 3**, with its blocker classes **7 + 5**
  intact.

### Benchmark #3 — அறப்போர் / Arappor (public speech) — ✅ COMPLETE

The third benchmark, and the first whose examined source establishes **no speech date, no venue and
no event** — proving the model can represent source absence honestly.

- **Implementation PR:** #23 — final reviewed head `06b42db399e1e97762ff9a9d522b63a83995bc03`, squash
  merge **`ecf73cc8146cd9a9578c4aeaf73518b122ce569c`** (2026-08-19T11:51:46Z), **production-verified
  2026-08-19** with Vercel success on that exact squash SHA. This is now the **last production
  application-code checkpoint**.
- **Source (pinned, unmodified):** `pugazg/kalaignar-public-speeches` @
  **`1ef73a709a343390befe55dcdfb029427f527bf4`**, `speeches/arappor`. Controlling scan
  `TVA_BOK_0064122_அறப்போர்.pdf`, SHA-256
  `8172cf4f04e804ebbcfe1b1e236c9d41bda2e07377952c162be4e4bb098ce01c`, 31,769,752 bytes, 22 PDF pages.
  Body **PDF 4–20 / printed 3–19 (17 pages)**; front matter PDF 1–3; advertisements/back matter PDF
  21–22. Edition: **second edition, April 1949, அறிவுப்பண்ணை** — **publication/edition context, NOT the
  speech date**.
- **Source-absence contract (source facts, not defects):** the examined source states no **date**, no
  **venue**, no **event**. The model now supports `date: null`, `year: null` and an optional
  public-speech `venue`, with the discriminated union preserved. Reader, SEO and provenance omit or
  explicitly document the absences without fabricating substitutes; nothing is described as
  "the 1949 speech".
- **Tamil: 17 pages, 16 transitions = 5 source-established same-paragraph continuations + 0
  source-established clean paragraph boundaries + 11 unresolved printed-paragraph relationships**;
  lexical joins **none 0 / space 5 / unknown 0**; **64** paragraphs and runs (42 resolved + 22
  unresolved-group) over **69** segments; **5** cross-page paragraphs.
  - The five continuations rest on the archive's documented cross-page word splits — `மௌனம்`,
    `நடராஜன்`, `அதற்காக`, `சுப்பராயன்`, `கடைசியாக`. **Reviewer-approved correction preserved:** the
    original brief expected these downstream joins to be `none`; that was rejected because the source
    archive had **already consolidated** each split word into the preceding page. Printed p.4 ends
    with the complete `மௌனம்` and p.5 begins `சாதித்தனர்`, so the surviving boundary is an ordinary
    word boundary — **`join: "space"`**. `none` would have produced `மௌனம்சாதித்தனர்`.
- **English: 17 anchors = 15 same-paragraph continuations + 1 clean page-transition paragraph
  boundary (printed p.10 → p.11) + 1 heading boundary (printed p.3)**; **54** paragraphs over **69**
  segments; **15** cross-page paragraphs. A page anchor is provenance — never a paragraph boundary in
  itself. _(First independent review defect: the first revision treated nearly every anchor as a
  paragraph boundary; the explicit `EN_BOUNDARY` audit now drives paragraph assembly.)_
- **Hard-line-break source fidelity** _(second independent review defect)_: both source layers contain
  exactly **one** Markdown hard-break group — the printed **p.9** language-policy quotation, **8 lines
  / 7 intentional breaks** in each language. It is generated as **ONE paragraph with one same-page
  segment preserving all 7 breaks**, rendered with a narrowly scoped `whitespace-pre-line` — never as
  eight semantic paragraphs. **Lesson:** trailing whitespace must be inspected *before* trimming,
  because Markdown's "two spaces + newline" carries source structure. Also established: body-section
  preamble before the first page marker is excluded from speech prose, and cross-page paragraphs mean
  **more than one DISTINCT source page**, not merely `segments.length > 1`.
- **Blockers:** exactly **one** class — the **11** unresolved Tamil printed-paragraph relationships,
  rendered neutrally. **Durable rule:** resolution requires an **upstream source-archive visual
  review** of the controlling scan that explicitly records the missing printed paragraph relationship;
  this Digital Library does not establish those typographic facts independently. The absent
  date/venue/event are **not** blockers.
- **Validation:** Arappor validator **ALL PASS (68 assertions)**; deterministic second import **no
  diff**; wrong-source-HEAD **fails closed, no writes**; Udhaya and Poonthottam validators **ALL PASS**
  with their `speech.json` **and** `provenance.json` byte-identical across the benchmark; `tsc` clean;
  build success (**1262** static pages); `git diff --check` clean.

**Remaining Phase-3 direction.** Phase 3 is still not complete — many released speeches remain.

> ⚠️ **SUPERSEDED (2026-09-01).** This paragraph previously read: *"Remaining Phase-3 direction —
> PAUSED. … **Speech Benchmark #4 is NOT STARTED and NOT SELECTED**, and speech expansion must not
> resume unless the owner explicitly reactivates it."* That is **historical**: the owner-directed
> pause (which produced Phase 4 — Poetry) was lifted, and **Benchmark #4 has since been completed and
> closed** — the first audio-sourced speech. **Nothing here authorizes a Benchmark #5.** No further
> speech work is started, selected or authorized; each new work still requires explicit owner
> authorization.

For any future owner-authorized speech expansion, the guidance stands: integrate additional released
speeches one at a time under the same **Speeches** shelf (both Legislative Assembly and Public
speeches are subtypes of it, not separate shelves), reusing this reader/importer pattern. Prefer
machine-readable indexes where present, but verify every reader-facing work against
source-repository release state.

Do not collapse public speeches and Assembly proceedings into one reader model if that loses parliamentary structure.

## Phase 4 — Poetry — 🚧 ACTIVE (benchmark 1 COMPLETE / MERGED / PRODUCTION-VERIFIED)

**Owner-directed move away from speeches.** The owner asked for the next Digital Library work to come
from a category **other than speeches**; Phase 4 opened the **Poetry / கவிதைகள்** shelf with exactly
one work. Implementation-level detail lives in
`pugazg/kalaignar-autobiography/docs/digital-library/PHASE4_POETRY_HANDOVER.md`.

### Benchmark #1 — இதயத்தைத் தந்திடு அண்ணா / Lend Me Your Heart, Anna — ✅ COMPLETE

- **Implementation PR:** #25 — final reviewed head `3653023db60cb51ee1df4d970d621494c095791c`, squash
  merge **`c2d1c46d1c2d4e1f11722360848226208867789f`** (2026-08-20T01:58:07Z), **production-verified
  2026-08-20** with Vercel success on that exact merge SHA (deployment
  `92kdGyRiKucdUPSywP2XqnZMx1g9`). This is now the **last production application-code checkpoint**,
  superseding the historical Phase-3 checkpoint `ecf73cc8…`.
- **Library:** 7 works / 5 non-empty shelves → **8 works / 6 non-empty shelves**. **Poetry / கவிதைகள்**
  is live with exactly **1** work; **Speeches** remains exactly **3** on ONE shelf. Routes
  `/poems/idhayathai-thanthidu-anna` and `…/source`; **no `/poems` collection landing**. Build: 1264
  static pages.
- **Source (pinned, unmodified):** `pugazg/kalaignar-poems` @
  **`42c156d7242fa799ea80adbb0c5f2b9eba078fe9`**, `poems/idhayathai-thanthidu-anna`. Controlling scan
  `TVA_BOK_0064132_இதயத்தைத்_தந்திடு_அண்ணா.pdf`, SHA-256
  `152cfb251a2049662102a2296487220f6f227f243657c9456df34105520676fe`, 26,816,066 bytes, **28 scans,
  28/28 verified**; poem body **scans 13–26, 14/14 verified**; printed pages 11–23 on scans 13–25;
  **scan 26 carries no visible printed page number and is never labelled 24**. The source PDF is
  **not vendored**.
- **Source context, not verse:** the note above the poem establishes **9.2.1969**, **சென்னை வானொலி /
  Chennai Radio**, **கலைஞர் மு. கருணாநிதி**, a **கண்ணீர்க் கவிதாஞ்சலி** to **பேரறிஞர் அண்ணா**. It is
  metadata; not one word enters the poem body.
- **Publication absence:** the scan establishes **no publication year and no edition statement**, so
  both stay null. The **15.9.2008** foreword date is a **foreword/internal source date only** and is
  never promoted to "publication year 2008", "edition year 2008" or a "2008 poem"; the work is
  likewise never described as "published in 1969".
- **Reader architecture:** a poem is **not** speech prose — the authoritative reading unit is the
  **source line**, with ordered boundary events distinguishing **in-page source-established stanza
  breaks** from **physical page transitions**. Cross-page relations carry **two independent
  dimensions** — textual/rhetorical and typographic stanza — and neither may be inferred from the
  other. Page-spanning derived groups are called **verse runs**, never stanzas.
- **Final counts** — Tamil: **339** source lines, **58** indented, **23** in-page stanza breaks,
  **37** verse runs, **11** source-established complete stanzas. English: **345** / **47** / **20** /
  **34** / **8**.
- **Cross-page provenance (13 physical transitions):** typographic stanza relation **0 same-stanza /
  0 stanza-boundary / 13 unresolved**; textual relation **10 source-established continuations / 1
  explicit non-continuation / 2 not specifically recorded**. The explicit non-continuation is scan
  **25→26**, where the source records the text continues *"thematically, but not textually"* — that is
  **textual evidence only** and gives **zero** typographic stanza evidence.
- **Blocker:** one class — **`cross-page-stanza-relationship`, count 13**. Durable resolution requires
  an **upstream source-archive visual/source review** of the controlling scan; the Digital Library must
  not resolve that typographic fact independently.
- **Two independent reviewer corrections (do not regress):**
  1. **Structural** — the initial implementation conflated textual/rhetorical continuity with
     typographic stanza continuity and asserted all 13 transitions were same-stanza; the initial
     English validator also stripped blank lines, so it could not prove stanza structure. Corrected:
     dimensions separated, only explicit source typographic evidence may resolve a stanza relation,
     validator derives evidence independently, and the 24/21-stanza and 13/13 same-stanza claims were
     **withdrawn**.
  2. **Print fidelity** — the neutral unresolved marker carried `data-print="hide"`, so Print → Save as
     PDF deleted it and silently presented the lines as continuous. Corrected: the marker is
     provenance, not chrome; it survives screen **and** print, with border-drawn hairlines and an
     explicit language-correct label.
- **Screen + print provenance contract:** source-established stanza gap **28 px**; unresolved page
  transition an **8 px** restrained marker asserting neither same-stanza nor a new stanza. **13/13
  markers retained per language on screen and in Print → Save as PDF** — printed English `source scan
  14 · stanza relation unresolved`, Tamil `மூல ஸ்கேன் 14 · அச்சுப் பத்தித் தொடர்பு
  தீர்மானிக்கப்படவில்லை`. The print marker is not verse and must never again be hidden as chrome.
- **English release:** *Lend Me Your Heart, Anna* — **project-created**, **RELEASE-COMPLETE**, 345
  lines, 0 omissions / 0 duplications, Markdown emphasis retained verbatim in data and rendered as
  `<em>`. Tamil remains authoritative; do not retranslate downstream.
- **Validation:** Poetry validator **310 assertions ALL PASS** (exact Tamil and English line
  reconstruction, in-page stanza structure checked, cross-page evidence independently derived, unknown
  relations cannot silently resolve, same-stanza negative test fails multiple checks, print-regression
  guard); deterministic importer **second run NO DIFF**; **wrong source HEAD fails closed with no
  writes**; Udhaya Kathir, Poonthottam and Arappor validators **ALL PASS**.
- **Rights unchanged:** the existing nationalisation model, with GO number and formal issue date still
  **null**, not broadened to third-party foreword, photographs, publisher/donor matter, printer
  imprint, design or the project-created English translation.
- **No source repository, mobile or PDF changes.**

**Poetry Benchmark #2: NOT STARTED / NOT SELECTED / NOT APPROVED FOR IMPLEMENTATION.** At the pinned
source state above, `poems/` held **exactly one** work directory (`poems/idhayathai-thanthidu-anna`);
at the historical snapshot `2230a8d` it held a **second**, `poems/anaiya-vilakku-anna`. That snapshot
recorded `anaiya-vilakku-anna` as NOT READY. **Wave 4 census authorization now requires re-checking live
source state rather than carrying that old readiness judgment forward.**

**Phase 4 records the Poetry work that actually happened.** It does **not** mean every subsequent
non-speech integration must remain under Poetry, and Essays/Fiction/Drama are not to be forced into
it. Category and phase naming for the next benchmark is decided when that benchmark is selected.

## Phase 5 — Essays & Articles — 🚧 ACTIVE (benchmark 1 COMPLETE / MERGED / PRODUCTION-VERIFIED)

Opened the **கட்டுரைகள் / Essays & Articles** shelf, selected by a live non-speech source-readiness
review. Implementation-level detail lives in
`pugazg/kalaignar-autobiography/docs/digital-library/PHASE5_ESSAYS_HANDOVER.md` when it is written;
until then this section plus PR #27 is the durable record.

### Benchmark #1 — சக்கரவர்த்தியின் திருமகன் / Chakravarthi's Son — ✅ COMPLETE

- **Implementation PR:** #27 — final reviewed head `929bb545e5358056ea0e0a671d157d7f97bede6a`,
  squash merge **`bcb11396b2215bc2cc1e81873c0ce278ef98598a`** (2026-08-20T10:15:15Z),
  **production-verified 2026-08-20** with Vercel success on that exact merge SHA (deployment
  `AwU8uyXYHxthgez8ZGQWP1rTS3PF`). This is now the **last production application-code checkpoint**.
- **Source (pinned, unmodified):** `pugazg/kalaignar-essays` @
  **`bff35320b668cb5beeaafc5faa58260c4f4473f8`**, `publications/sakkaravarththiyin-thirumagan`.
  Controlling scan `TVA_BOK_0065662_சக்கரவர்த்தியின்_திருமகன்.pdf`, SHA-256
  `5d7f8404a53c0766df896ddedf9978a3fd31f97b8e98625b70a93366412eb90d`, 201,858,823 bytes, **83
  scans — 83/83 verified and 83/83 strict visual-text-fidelity PASS**, 80 printed pages. The source
  PDF is **not vendored**.
- **Edition distinction:** first published **மே 1956 (வேலூர் திராவிடன் பதிப்பகம்)**; the CONTROLLING
  source integrated here is the **2018 reprint** (title-page line `திராவிடர் கழக (இயக்க) வெளியீடு`).
  The scan is never described as a 1956 scan, and the 1956 history is never erased.
- **Scope:** ONE catalog publication holding **14 source-numbered articles** — never 14 catalog
  works. Numbers 1–14 come from the printed contents page with every boundary verified against its
  heading page. Tamil **14/14** assemblies frozen with **0** unresolved fidelity items; English
  **14/14** verified, **E6 PASS**, **E7 PASS**, release gate **CLOSED**, 0 unresolved questions,
  0 blockers, `englishKind: project-created`.
- **Library:** 8 works / 6 shelves → **9 works / 7 non-empty shelves**. Poetry stays **1**; the
  single Speeches shelf stays **3**. Routes `/essays/<slug>`, 14 `/essays/<slug>/articles/<article>`
  and `/essays/<slug>/source`; **no `/essays` collection landing**. Build: 1280 static pages.

**Final archival model — two independent dimensions.** An article is neither speech prose, verse nor
a scene, so Essays has its own reader and its own narrow model:

```
ArticleBlock
 ├── kind        paragraph | subheading | attribution      (SOURCE structure)
 ├── segments    [ authored-text | quoted-text ]           (VOICE inside the block)
 └── sourcePages [ { scan, printed } … ]                   (block-level provenance)
```

A source paragraph regularly closes a quotation and then continues in Kalaignar's own voice, so
**only an all-quoted paragraph may render as a full quotation**; a mixed paragraph stays a paragraph
with its quoted runs marked inline. Kalaignar's framing is never attributed to the person he quotes.
Source quotation punctuation is preserved and never repaired — the archive's source-irregular
unclosed quotations simply leave a block ending in quoted voice.

**Final counts** — Tamil **349** blocks: **213** authored-only · **54** quotation-only · **74**
mixed. English **358** blocks: **208** authored-only · **61** quotation-only · **81** mixed. Plus 1
attribution and 7 source-printed subheadings per layer, **14** translator notes held outside the
authored body, and **90** page-spanning blocks.

**Cross-page evidence model — positive evidence only.**

```
positive continuation evidence → same-block
positive boundary evidence     → block-boundary
absence of evidence            → unknown
```

**60** in-article page transitions: **45 same-block · 0 block-boundary · 15 unknown**. A relation is
never inferred from blank lines, marker formatting, marker removal, punctuation, semantic flow or
the absence of a note. The 15 unresolved edges are never joined and never shown as a clean paragraph
break: a restrained prose marker states the relation is unresolved, is weaker than a paragraph gap,
and **survives Print → Save as PDF** with a border-drawn rule and a language-correct label. One
blocker class, `cross-page-block-relationship` (15), resolvable only by an upstream source-archive
review.

**Two independent reviewer corrections (do not regress):**

1. **Mixed voice.** The initial model gave a whole source paragraph one semantic kind, decided
   largely by whether it opened with a quotation mark, so Kalaignar's post-quotation framing rendered
   inside `<blockquote>`. Corrected by separating block structure from voice segments; explicit
   Tamil **and** English Article-1 regression tests now guard it.
2. **Cross-page evidence.** The initial 45 / 15 / 0 taxonomy treated the absence of a continuation
   note as positive block-boundary evidence. Corrected to the positive-evidence model above; the
   result is 45 / 0 / 15.

**Validation:** Essays validator **185 assertions ALL PASS** (both layers reconstructed exactly,
voice re-segmented independently, cross-page relations re-derived independently of the importer);
deterministic importer **second run NO DIFF**; **wrong source HEAD fails closed with no writes**;
Udhaya Kathir, Poonthottam, Arappor and Idhayathai Thanthidu Anna validators **ALL PASS** with their
generated data byte-identical; `tsc` clean; `git diff --check` clean.

**Rights unchanged:** the existing nationalisation model, GO number and formal issue date still
**null**, not broadened to publisher matter, cover/design, advertisements, library marks, the
project-created translation, or the third-party texts quoted inside the essays.

**Preserved source distinctions:** heading-page vs contents-page title witnesses kept separate for
articles **5** and **14** (never normalized); article 10's differing body phrase never promoted to a
title; scan-82 material below the printed article-ending ornament and the whole scan-83 back cover
excluded, so the promotional Article-12 excerpt never extends canonical body; `Achariyar` /
`Rajaji` (article 7) / `the Achariyars` (article 11) carried exactly as released.

**Phase-5 Benchmark #2: NOT STARTED and NOT SELECTED.**

## Phase 6 — Fiction — ✅ COMPLETE (benchmark 1 COMPLETE / MERGED / PRODUCTION-VERIFIED)

**Read this qualifier before quoting the status.** "COMPLETE" here means **Phase-6 Benchmark #1** is
complete, merged and production-verified. It does **NOT** mean the Fiction shelf is finished:
**Fiction Benchmark #2 is NOT STARTED and NOT SELECTED**, and the remaining novels and short stories
listed under *Remaining Fiction roadmap* below are still **future** items.

_Historical planning context: this grouping was once written as "Phase 4 — Essays + Fiction +
Poetry", and was then carried as "Future non-speech categories — Fiction (planning only)". **Poetry**
became the actual, owner-directed **Phase 4** and **Essays & Articles** became **Phase 5**; Fiction
has now shipped its first benchmark as **Phase 6**. Completed Phase 1–5 history is not renumbered._

### Benchmark #1 — பலிபீடம் நோக்கி / Towards the Sacrificial Altar (novel) — ✅ COMPLETE

- **Source repository:** `pugazg/kalaignar-novels`
- **Source merge / pin:** `9e80c567d4a2165178c5374a02210240140685bf`
- **Application repository:** `pugazg/kalaignar-autobiography`
- **Application merge:** `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (PR #28 squash merge)
- **Edition:** முதற்பதிப்பு ஏப்ரல் 1947 — எரிமலைப் பதிப்பகம், துறையூர்
- **Shape:** ONE novel in THREE assembled reading sections; Fiction becomes the eighth non-empty
  shelf and the catalog reaches ten published works.
- **Routes (live):** `/novels/balipeedam-nokki`, its three section routes and
  `/novels/balipeedam-nokki/source`.

Decisions worth carrying forward:

- **Embedded-sequence rule.** `ராயசம் வெங்கண்ணா — தஞ்சை சரித்திரக் கதை` is **section 2 of this
  novel**, never a separate work: no catalog entry, route, work-level metadata, translation project
  or release identity of its own. The importer refuses to run if the source stops saying so.
- **Section titles are the archive's labels, not printed headings.** A heading enters the reading
  body only where an audited page record prints it verbatim (scan 4; scan 8), cited to the scan that
  prints it. Section 3's label is printed nowhere, so it stays out of the body and claims **no** page
  provenance; the reader says so where a reader meets it.
- **Join evidence is classified by kind.** Six joins carry page-edge fragments; the scans 12→13
  dying-speech quotation is a **narrative continuity** the audit established by reading. A semantic
  continuity is never displayed as printed paragraph structure.
- **Uncertainty preserved.** Printed page numbers are carried only where the scan shows one; the
  Government Order's number and issue date remain `null`.
- **Spelling correction.** The `ராயசம் வெங்கண்ணா` / Rayasam Venganna reading was derived from the
  **controlling scanned source edition**, corrected in the archive first and then re-pinned here —
  see **§9.1**. The earlier `வெங்கண்ணு` / Vengannu form is **superseded**, not an alternative.

**Fiction Benchmark #2: NOT STARTED and NOT SELECTED.**

### Remaining Fiction roadmap (planning only — NOT started, NOT selected)

- **Novels:** works in `pugazg/kalaignar-novels` other than the integrated `பலிபீடம் நோக்கி`, subject
  to live source readiness at selection time.
- **Short Stories:** `Kizhavan Kanavu` was recorded as a planning candidate only — not selected, not
  started, and not privileged over a live readiness inspection.

_(Essays: `Sakkaravarththiyin Thirumagan` was the planning candidate and is now **integrated** as
Phase-5 Benchmark #1 — see **§10 → Phase 5**.)_

After one work of each form is proven, extract reusable adapters rather than prematurely inventing abstraction.

## Phase 7 — Drama / Stage Plays — 🚧 ACTIVE (benchmark 1 COMPLETE · Bulk Wave 1 COMPLETE)

**Read this qualifier before quoting the status.** Benchmark #1 (சிலப்பதிகாரம்) is complete, merged
and production-verified, and **Bulk Onboarding Wave 1 has since published four more plays**, taking
the Drama shelf to **5**. The PHASE remains **ACTIVE**: no further Drama work is started, selected or
authorized.

> ⚠️ **SUPERSEDED (2026-09-01).** This section previously said Drama Benchmark #2 was blocked because
> `Anarkali`, `Cheran Senguttuvan` and `Socrates` had **no controlling Tamil source**. That is no
> longer true: controlling Tamil sources were released in `pugazg/kalaignar-stage-plays` at
> `145e52e88dbd009286f749a7f0e3520386e63244`, and all three — with பரதாயணம் — were published by
> **Bulk Onboarding Wave 1**. See the Wave-1 close-out near the top of this document. **மணிமகுடம் /
> Manimagudam remains unpublished and excluded.**

### Benchmark #1 — சிலப்பதிகாரம் நாடகக் காப்பியம் — ✅ COMPLETE

- **Source repository:** `pugazg/kalaignar-stage-plays`
- **Source pin:** `a66e62bbecaf63825b3db09a1d421401e1ab2e8e`
- **Application PR:** [#29](https://github.com/pugazg/kalaignar-autobiography/pull/29) — **MERGED** 2026-08-21
- **Application merge SHA:** `9aade1d441bb314b5ab62f97b87b373d33db08c5` (squash)
- **Application base:** `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a`
- **Production verified:** 2026-08-21 — all six routes 200; `/plays`, `/drama` and `…/39` 404; Drama
  shelf populated and the other eight shelves unchanged; the scan-88 obstruction marker present in
  both layers with no reconstruction and **surviving print** (no print rule hides it or any
  ancestor); printed speaker abbreviations and both printed separators (`" : "` and `": "`)
  rendered as set; unlabelled two-column continuations rendered with no injected label; scene 06's
  unmatched-bracket direction intact with the following speech not swallowed; no 2009 witness
  wording in any reader content; provenance page showing the identity-basis disclaimer, the
  49,459,844-byte size, no publication year, and G.O. number/date as not verified.
- **Edition:** அஞ்சுகம் வெளியீடு, சென்னை-6 — **no publication year is printed**, and none is inferred
- **Shape:** 38 numbered scenes **plus a separate unnumbered closing tableau**

Decisions carried by this benchmark:

- **A stage-play reader model, not the cinema one.** `readerStructure: "stage-play"`; Manohara's
  `"scene"` screenplay model is untouched and unreused. Dialogue, stage directions (both printed
  delimiters), quoted verse and ornaments are never reclassified into one another.
- **The closing tableau is NOT Scene 39.** `கண்ணகி சிலை நாட்டு விழா` is printed after காட்சி-38
  without a number; it is excluded from the scene count (38, never 39) and the importer refuses to
  run if a Scene 39 appears.
- **Two-column continuations stay unattributed.** The edition does not re-label a speech resuming
  after the column break, so those units carry `speakerAsPrinted: null` rather than an invented
  attribution.
- **Speaker labels are printed authority.** The edition's inconsistent abbreviations and its varying
  separator are carried verbatim — never expanded, unified or regularised.
- **The scan-88 obstruction is evidence.** The library-stamp marker is carried into both layers,
  rendered visibly and never hidden from print; the covered characters are not reconstructed.
- **The 2009 published English witness is evidence only** — a third party's separately copyrighted
  translation, never imported and never reader content.

### Bulk Onboarding Wave 1 — ✅ COMPLETE

`Anarkali`, `Cheran Senguttuvan`, `Socrates` and `Bharathayanam` are **published**, from the frozen
source pin `145e52e88dbd009286f749a7f0e3520386e63244` — PR #64, squash
`0dc92fa0fd832b5932b8df75606ef049c9f261ea`. Full detail is in the Wave-1 close-out section near the
top of this document.

*(Historical: this paragraph previously recorded those three as registry stubs with no controlling
Tamil source. Controlling Tamil sources have since been released. The **2009 published English
witness remains secondary comparison evidence only** and must never be reverse-translated into
canonical Tamil — that constraint is unchanged and was honoured by Wave 1.)*

**No further Drama work is started, selected or authorized.** மணிமகுடம் / Manimagudam is **not**
published and is **not** automatically a Wave-2 candidate.

## Future — broader Literary Commentary (planning only)

_Historical planning context: this section was once numbered "Phase 5". That number is now taken by
the shipped **Phase 5 — Essays & Articles** (above). Stage plays and broader literary commentary
remain **future** categories; nothing here has been started. Completed Phase 1–5 history is not
renumbered, and the phase name for the next benchmark is decided when that benchmark is selected._

- Silappathikaram — Nadaga Kappiyam
- further literary commentary only when source work has reached its publication gate
- Thirukkural commentary waits for an explicit complete/partial-publication decision based on live archival state

## Phase 8 — Cross-library discovery

_Historical planning context: this section was numbered "Phase 6", then "Phase 7". Those numbers are
now taken by the shipped **Phase 6 — Fiction** and the active **Phase 7 — Drama / Stage Plays**
(above). Nothing here has been started, and completed phase history is not renumbered._

Only after several shelves contain real public works:

- global search across published library units;
- filters by shelf/form/language/date where source metadata supports them;
- recently added;
- continue reading across work types;
- unified bookmarks/shelf if desired;
- citation/provenance affordances.

Do not label the existing memoir-only full-text search as a global library search.

## Phase 9 — ingestion automation

_Historical planning context: this section was numbered "Phase 7", then "Phase 8". Nothing here has
been started._

Once multiple integration adapters are proven:

- define a reusable Digital Library export contract;
- optionally add per-source-repo deterministic `library-export` builders/manifests;
- central website vendor script records source repo + commit + integrity metadata;
- CI validates that imported artifacts and catalog entries agree.

Do this after real integrations establish what the contract actually needs.

---

# 11. Reader UX principles

## Unified library chrome

Across works, aim for consistent:

- Tamil-first presentation;
- Tamil/English switch only where English exists;
- readable measure and typography;
- light/dark/reading-theme behavior where current site supports it;
- next/previous unit navigation;
- work table of contents;
- provenance/source note;
- citation/deep-linkable units;
- responsive desktop/mobile layout;
- accessibility semantics.

## Preserve form-specific structure

Never flatten:

- poem lineation;
- dialogue/speaker structure;
- stage directions;
- Assembly interjections;
- article boundaries;
- scene boundaries;
- source-page provenance;
- commentary unit boundaries.

## Translation labels

Distinguish where necessary:

- published English source/witness;
- project-created translation;
- Tamil-only work;
- English incomplete/unreleased.

Do not imply every English layer is an official published translation.

---

# 12. Public-library provenance and rights language

Repository status such as `RELEASE-READY`, `RELEASE-COMPLETE`, `archival-ready` or `verified` is an **editorial/source-fidelity status**, not by itself a copyright/republication-rights determination.

Do not add claims such as:

- public domain;
- officially authorized;
- complete works;
- official DMK/Kalaignar-family archive;

unless independently established and explicitly approved.

Every public work should have enough provenance to explain which archived source/edition it represents without exposing source PDFs contrary to repository policy.

---

# 13. Architecture anti-patterns to avoid

Do not:

- turn the nine source repositories into nine unrelated mini-sites;
- hard-code every new work directly into `Library.tsx`;
- create one giant JSON blob containing every literary form;
- fetch GitHub dynamically from the browser for production reading;
- overwrite verified source text in the website;
- merge source repos into the website repository;
- import source PDFs;
- expose unfinished/uncertain work as complete;
- fabricate dates, genres, speaker identities, source numbering or translation status;
- break legacy URLs merely to create a cleaner route taxonomy;
- integrate all works in one PR;
- use accidental website-repository Manohara files as archival evidence, import authority, translation authority, provenance authority or an integration resume point.

---

# 14. Claude Code / prompt-provider operating model

A fresh ChatGPT window should act primarily as **reviewer + prompt-provider for Claude Code**.

Before every implementation prompt:

1. read this handover;
2. inspect live `pugazg/kalaignar-autobiography` main and open PRs;
3. inspect the relevant source repository main/readme/handover/release reports;
4. identify already-started integration work and continue it rather than duplicating it **except for explicitly documented accidental/non-authoritative artifacts such as the existing website Manohara parts, which must be ignored as integration inputs**;
5. write an explicit staged Claude prompt;
6. require source/release/provenance validation;
7. require build/typecheck and live-route checks;
8. require a clean branch/PR and stop after the requested activity.

**Bulk onboarding is the standing default** for selecting and shipping new work — see the
standing-policy section near the top of this document. A batch still needs a readiness census, an
explicit exclusion list, per-work freezing, per-work validator reporting and one independent review
gate; and it still needs **owner authorization** before it starts.

When Claude returns a report, independently verify:

- actual PR head/base;
- changed filenames;
- commits;
- CI/Vercel;
- source-repo commit/integrity reference;
- counts and availability claims;
- no silent source edits;
- no mobile scope drift;
- for Manohara, evidence that all imported reader content came from `pugazg/kalaignar-cinema-works`, not the accidental website files.

---

# 15. Immediate next activity

> ⚠️ **CURRENT OVERRIDE (2026-09-04).** Older Wave-4/census planning language below is historical.
> **Bulk Onboarding Wave 5 — Cinema Writing is IN PROGRESS and owner-authorized**: batch Manthiri Kumari
> + Raja Rani. **P0 (census), P1 (source freeze / hidden data foundation, PR #75 squash `7cc0546f…`) and
> P2 (public readers/routes/`/source` pages, PR #76 squash `cf6a952c…`) are COMPLETE**; P3–P5 have not
> started. **Wave 5 P3 is the planned next stage but requires a separate explicit owner authorization and
> has NOT started.** Wave 4 — Poetry and its post-Wave-4 landing-copy regression repair remain COMPLETE
> and CLOSED. The two cinema works are directly readable at `/cinema/manthiri-kumari` and
> `/cinema/raja-rani` but the public **catalogue** stays at **76 works / Cinema Writing 4** until P3
> (P3 makes it 78 / 6). No implementation activity beyond the completed P2 is authorized; the next stage
> or any new wave requires a **new explicit owner authorization** and must not be started implicitly.

Historical completed state remains:

- **Bulk Onboarding Wave 1 — Drama is COMPLETE and CLOSED** (PR #64, squash `0dc92fa0…`).
- **Bulk Onboarding Wave 2 — Fiction is COMPLETE and CLOSED** (PR #65, reviewed head `2ba1ee3a…`,
  squash `4fd45a92663abbe70ff0c0a605168314cd36e44c`).
- **Bulk Onboarding Wave 3 — Essays & Articles is COMPLETE and CLOSED** (PR #66, approved head
  `c4f40f7f…`, squash `c4660c49…`).
- **Reading Room Wayfinding Phase 0 + Phase 1 is COMPLETE and CLOSED** (PRs #67/#68; control PR #21).
- **Film Songs implementation E1–E4 is COMPLETE and CLOSED** (control close-out merged).
- **Bulk Onboarding Wave 4 — Poetry is COMPLETE and CLOSED** (PRs #69–#73; durable close `ad998113…`,
  tree `e6a8c29…`). Six Poetry workspaces represented; two publications (58 + 77 = 135 internal units);
  exactly two cross-witness relations; 12 payload SHA-256 pins; collections still 1.
- **Bulk onboarding remains the STANDING DEFAULT workflow** for any *future, separately authorized* wave.
- **மணிமகுடம் / Manimagudam is never automatically selected**; it requires its own current readiness
  gate and must be judged live during a census if considered at all.
- `kalaivanar-nsk-memorial-day-audio-06` remains a **SEPARATE** source archive and is never
  auto-selected.
- **Validator-contract migration remains PAUSED** and **native mobile remains ON HOLD.**

**Bulk Onboarding Wave 5 — Cinema Writing is IN PROGRESS and owner-authorized.** P0 (census), P1 (source
freeze / hidden data foundation, PR #75 squash `7cc0546f…`) and P2 (public readers/routes/`/source`
pages, PR #76 squash `cf6a952c…`) are **COMPLETE**. **Wave 5 P3 is the planned next stage but requires a
separate explicit owner authorization and has NOT started.** When authorized, P3 adds Manthiri Kumari and
Raja Rani to `data/library.ts`, exposes them in `/read` discovery (works **76 → 78**, Cinema Writing
**4 → 6**) and the sitemap, with the related catalogue/discovery tests. Until then do not add either work
to `data/library.ts`, expose them in `/read`, change those counts, or modify the sitemap for them. The
prior Wave-4 items remain closed: do not reopen the six Wave-4 Poetry works or rewrite the 12 pinned
payloads without a newly discovered, source-backed regression. A future *new* wave, if authorized, must
run its own read-only source census before any implementation PR.

Last production application-code checkpoint at this handover:
**`cf6a952ca9f0edea254d9c72b48ef333523bfd51`** (Wave 5 P2 / PR #76 squash merge), tree
**`9bf711784a86458f95a333c6f4c1768cbe65f690`**. It advanced application code from the Wave-5 P1 close
`7cc0546f…` by the cinema **public readers, direct routes and `/source` pages** — **+89 direct public
routes** (Manthiri 18 + Raja Rani 71). The build route count moved (prerender **3271 → 3360**, `.html`
**3266 → 3355**) but the **catalogue/discovery/sitemap are unchanged** (works 76 · Cinema Writing 4 ·
discovery 40 · visible 32 · sitemap 3262 / 0 dup · `/poems/` 147). Neither work is in `data/library.ts`
or the sitemap; both resolve directly but are undiscoverable from `/read` until P3.
