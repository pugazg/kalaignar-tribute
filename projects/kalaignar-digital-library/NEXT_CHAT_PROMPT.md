# New Chat Bootstrap Prompt — Kalaignar Digital Library / Wave 6 COMPLETE · CLOSED · FROZEN at P5

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub and production are authoritative. Do not trust copied SHAs, PR
bodies or this bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely** (highest-precedence CURRENT
   checkpoint is **2026-09-17 — Batch-7 P2–P4 merged (PR #87) + P5 production acceptance PASS + Wave 6 COMPLETE / CLOSED / FROZEN at P5**).
3. Read `projects/kalaignar-digital-library/WAVE6_P5_PRODUCTION_ACCEPTANCE.md` (the durable acceptance
   record), plus the top banners of `WAVE6_COMPLETED_WORKS_CENSUS.md` and `WAVE6_BATCH7_SHORT_STORIES.md`.
4. Inspect all open control PRs.
5. Fetch live `pugazg/kalaignar-autobiography` `main` and inspect all open implementation PRs.
6. Treat live GitHub and production as authoritative — any newer legitimate live state supersedes this bootstrap.

## CURRENT state

- **Live GitHub / production are authoritative.**
- **Wave 5: COMPLETE / CLOSED.** **Wave 6: COMPLETE / CLOSED / FROZEN at P5** — the established lifecycle is P0 → P1 → P2 → P3 → P4 → P5; P0–P5 are frozen; **there is no Wave-6 P6.**
- **Wave 6 P1–P5 (the full lifecycle) are merged/accepted:**
  - Batches 1–6 (22 works) merged (P1–P3 + P4 for Batches 1–6).
  - Batch 7 (116 short stories) merged: **P1 via PR #86**, **P2–P4 via PR #87**.
  - **P5 production acceptance = PASS** (2026-09-17); implementation delta = 0, source delta = 0.
- **Accepted implementation boundary:**
  - implementation `main`: `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e`
  - implementation tree: `06c7ae8646ba85e61c973fecb5945ffbec256c39`
  - approved-head-tree == merged-main-tree PASS (approved head `b34e05dcc27ba809e8f7c3743d2f4570614457eb`).
- **Realized public surface:**
  - catalogue **216** · Fiction **157** · non-empty shelves **9**
  - public collections **6** (1977 + 2008/40, 2004/34, 1987/25, 1982/6, 2009/16)
  - `STORY_SLUGS` **154** unique
  - `/read` discovery **77** / visible **40** (Fiction discovery **18**, over-cap → disclosure)
  - sitemap **3909 / 0 dup** · build **3918 / 3913**.
- **All 138 Wave-6 selected works are implemented** (22 + 116).
- **No implementation or source change occurred in P5** (control-only close-out).

## Wave-6 route arithmetic (durable)

```
Batches 1–6 = 321 ; Batch-7 stories = 232 ; Batch-7 collections = 5 ; total = 558
3360 + 558 = 3918 (prerender) ; 3355 + 558 = 3913 (html) ; 3351 + 558 = 3909 (sitemap)
```

## Frozen source (unchanged)

- Batch-7 source `pugazg/kalaignar-short-stories` `main` `7205a10892d0b208df2617766844f480b6a2c798`,
  tree `1be34cc368fbc96ff72933a004a074ef840168ee`. P5 repinned nothing.

## Durable semantic facts (do not regress)

- Plural membership is live: `jaadi-kutti-poduma` (one work; 2008 + 1987, 1987 ordinal 2),
  `kuruvi-rameswaram` (one work; 2004 + 1987, 1987 ordinal 11), and the eleven 1977 canonicals reprinted
  in 2009 (1977 + 2009) — each a single canonical work; the 2009 collection-local page/scan extents do not
  overwrite 1977 provenance.
- Eight Batch-7 works are non-collection standalone Fiction discovery entries: `seerazhitha-sirippu`,
  `madurai-selavu`, `kondru-varuga`, `naattiya-kalarani`, `maanam`, `neruppu`, `vilaiyal-vangalaiyo`, `nanbana`.
- `நந்தியூர் நரியப்பன்` and `நரியூர் நந்தியப்பன்` are distinct works. `தேனலைகள்` and `நடுத்தெரு நாராயணி` remain excluded.
- P2 corrections durable (nine stories apparatus-clean; `madurai-selavu` excludes the scan-25
  `intervening-non-story` interleaf, English scan-25 continuation preserved).

## No P6 — Wave 6 is closed at P5

- **Wave 6 is COMPLETE / CLOSED / FROZEN at P5. There is no pending P6.**
- **P6 is not part of the Wave-6 lifecycle** and is not defined by any historical programme material (Wave 5
  likewise ran P0–P5 and closed at P5). The owner reviewed the read-only P6 definition audit and accepted
  the determination that no P6 is required. **Do not invent a P6, and do not read the historical
  `P6 NOT STARTED / NOT AUTHORIZED` guard (retained inside superseded checkpoints) as pending Wave-6 work.**
- Do **not** automatically start Wave 7, **do not** automatically run a fresh census, and **do not** ingest
  new source material.
- The next activity requires **explicit owner authorization** for either (a) a **new wave**, or (b) a
  **specifically scoped maintenance/repair activity** on already-published works — never framed as "P6".

## Workflow contract

- **Claude Code performs GitHub writes, branches, commits, PR corrections and merges.**
- **The reviewer independently reviews exact live state and supplies prompts.**
- **Live GitHub and production beat copied prompts/reports.**
- P5 was closed by control-only PR **#33** (`Wave 6 P5 — production acceptance and durable control
  close-out`). Wave-6 final closure at P5 is recorded by control-only PR **#34** (`Wave 6 — declare
  final closure at P5`). Both are control-only; **no** implementation change belongs to this closure.
  Live GitHub remains authoritative for current PR state.

**STOP. Wave 6 is COMPLETE / CLOSED / FROZEN at P5; there is no pending P6. Fetch live GitHub and await explicit owner authorization for a new wave or a specifically scoped maintenance/repair activity before any further execution.**
