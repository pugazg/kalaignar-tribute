# New Chat Bootstrap Prompt — Kalaignar Digital Library / after Wave-6 Batch-6 P1–P3 + P4 (Batches 1–6) closure

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub is authoritative. Do not trust copied SHAs, PR bodies or this
bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely** (its highest-precedence CURRENT
   checkpoint is the 2026-09-15 **Wave-6 Batch-6 P1–P3 + P4 Batches 1–6 MERGED / CLOSED** state).
3. Inspect all open control PRs.
4. Fetch live `pugazg/kalaignar-autobiography` `main` and inspect all open implementation PRs.
5. Treat live GitHub as authoritative — any newer legitimate live state supersedes this bootstrap; update
   the reasoning accordingly.

## CURRENT state — Wave-6 P1–P3 merged through Batch 6; P4 for Batches 1–6 MERGED / CLOSED

- **Live GitHub is authoritative.**
- **Wave 5: COMPLETE / CLOSED.**
- **Wave 6 P0: COMPLETE / FROZEN.**
- **Wave-6 P1 → P2 → P3: merged through Batch 6** (Cinema, Drama, Speeches, Poetry, Novels, Essays & Articles).
- **22 / 125 READY works merged** through P3.
- **Cumulative Wave-6 direct routes: 321.**
- **Wave-6 P4 for Batches 1–6: MERGED / CLOSED** (PR #85).
- Implementation `main` is anchored by the P4 squash-merge commit
  **`2ca4d19830755864acec153f99f2659f413802cb`**, tree **`837c92893ab248f6185a36dc3b13f353495f5c9d`**,
  unless live `main` has legitimately advanced since this docs sync — in which case live wins.

Wave-6 merged progress: Batch 1 Cinema +65 (65) · Batch 2 Drama +83 (148) · Batch 3 Speeches +6 (154) ·
Batch 4 Poetry +30 (184) · Batch 5 Novels +63 (247) · **Batch 6 Essays & Articles MERGED / CLOSED +74 (321)**.

## Public inventory after P4 (durable)

- Catalogue works: **100** (was 78).
- Public collections: **1** (unchanged).
- `/read` discovery entries: **64** (was 42); initially visible with cap 6: **39** (was 34).
- Sitemap URLs: **3672** (was 3351); **0 duplicates**; Wave-6 exposed route set = the existing **321**
  P3 routes, set-equal to `data/internal/wave6/p3-routes.json.cumulativeRoutes` (missing 0 / extra 0 /
  duplicate 0).
- Build boundary: **3681 prerender routes / 3676 HTML** = frozen baseline 3360 / 3355 + 321. **P4 created
  ZERO new reader routes.**
- Catalogue shelf census (9 shelves, total 100): Life Writing 1 · Letters 1 · Fiction 41 · Poetry 14 ·
  Drama 8 · Cinema Writing 7 · Speeches 17 · Essays & Articles 9 · Literary Commentary 2.
- Post-merge integrity: `post-merge main tree == approved PR-head tree` (`837c9289…`) — **PASS**.

## Batch-6 durable facts (for continuity)

- Implementation PR **#84** merged Batch 6 (Essays & Articles). Prior implementation `main` / merge
  commit `d6621b71256ae99b1c89b4f2091513dcc5f96626`; merged tree `55823ff9742969e6868741312740aec06ebfd4ff`.
- Works: `ina-muzhakkam` (6) · `kolaikkalam` (6) · `kudumbaththin-nalvilakku` (1) · `sinthanaiyum-seyalum`
  (50) · `vedhanai-ch-siraiyinindrum-viduthalai-pera` (1 government message / `செய்தி`). Totals:
  **5 works · 64 articles · 74 direct routes**.
- Source anchor (immutable for Batch 6): `pugazg/kalaignar-essays` commit
  `564add708b8bd942fa9d5f505b083955248873d0`, tree `14a4a6cd81dbd13145f289734812583cac9b1403`; target
  subtree pins — `ina-muzhakkam` `4e6a28cb93a1eb2b8f376a1abebc938a1d7f8ef9`, `kolaikkalam`
  `e1eff4df14bd56e37575f15651e400f87b332ff0`, `kudumbaththin-nalvilakku`
  `1d1001992ff376056da5cba8d54f7dd79901566b`, `sinthanaiyum-seyalum`
  `488cd61fa8df5aafa5a9a505001ce417b2892e90`, `vedhanai-ch-siraiyinindrum-viduthalai-pera`
  `f3c43511240df098b175b9d39cdcc6f4318f2230`.
- Semantic restraint: `kudumbaththin-nalvilakku` — no established edition, no invented year,
  `controllingIsFirstEdition: null`, `editionStatus: "not-established"`, printed pages remain 2–9;
  `vedhanai-…` — government `செய்தி` / message, **NOT a speech**, no fabricated date/venue, edition
  not-established; `sinthanaiyum-seyalum` — exactly 50 articles, 2010 third edition, five transfer PDFs.

## P4 durable facts (for continuity)

- Implementation PR **#85** (`Wave 6 P4 — Publish completed Batches 1–6 to catalogue, discovery and
  sitemap`) is **MERGED / CLOSED**; approved head `c65070845e75337ea65989bc83f792739983f795` / tree
  `837c92893ab248f6185a36dc3b13f353495f5c9d`; squash merge commit `2ca4d198…`; post-merge `main` tree
  **equals** the approved PR-head tree (integrity gate **PASS**). Exact-head CI run `34964450981` — all
  gates SUCCESS.
- P4 semantic restraint (independently corrected before merge): `oruthalaik-kathal` remains one
  **verse-novel / poetry publication of 11 source sections — NOT 11 independent poems**. Public metadata
  is data-driven from `readingUnitKind` / `workForm`: landing says **11 source sections**, child says
  **section N of 11**; normal poetry publications keep poem/poems wording. **Do not regress to "11 poems."**
- Other P4 restraints hold: Ammaiyappan segments not source-numbered scenes; Kagithapoo no invented
  Scenes 22/23; Thiruvalar no invented act/scene system; Namathu Nilai no fabricated date; Idhaya /
  Palli no invented date/venue; 1975 Kaviyaranga ordinals 01/02/04 (03 absent); Periya = 7 archive
  reading sections (never 18); Pudhaiyal = 52 literary units / 54 total direct routes; Kudumbaththin no
  invented edition/year; Vedhanai is a government message, not a speech.
- Durable record `data/internal/wave6/p4-integration.json` exists; the historical
  `data/internal/wave6/p3-routes.json` was intentionally **not rewritten** (its `discoverable=false` /
  `sitemapExposed=false` values are P3-phase history, not current public state).

## Next execution activity — await explicit owner direction

**Wave-6 P5 is NOT authorized. Wave-6 P6 is NOT authorized. Batch 7 has NOT started. No new source
ingestion is authorized.** Do **not** imply that P5 automatically follows P4. The next chat must first
fetch live GitHub state and then **await explicit owner direction** for the next execution activity — do
not begin the next batch, P5, P6, or any ingestion on the strength of this bootstrap alone.

## Workflow contract

- **Claude Code performs GitHub writes, branches, commits, PR corrections and merges.**
- **ChatGPT independently reviews exact live state and supplies prompts.**
- **Live GitHub and production beat copied prompts/reports.**

**STOP after Wave-6 Batch-6 P1–P3 + P4 (Batches 1–6) closure. P5 / P6 remain NOT authorized. Batch 7 is
NOT started and requires explicit owner authorization.**
