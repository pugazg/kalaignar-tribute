# New Chat Bootstrap Prompt — Kalaignar Digital Library / after Wave-6 short-story census refresh (combined Batch 7)

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub is authoritative. Do not trust copied SHAs, PR bodies or this
bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely** (highest-precedence CURRENT
   checkpoint is the 2026-09-16 short-story census refresh; the 2026-09-15 checkpoint carries the still-current
   implementation boundary).
3. Read `projects/kalaignar-digital-library/WAVE6_COMPLETED_WORKS_CENSUS.md` (top refresh banner) and
   `projects/kalaignar-digital-library/WAVE6_BATCH7_SHORT_STORIES.md` (the deterministic Batch-7 manifest).
4. Inspect all open control PRs.
5. Fetch live `pugazg/kalaignar-autobiography` `main` and inspect all open implementation PRs.
6. Treat live GitHub as authoritative — any newer legitimate live state supersedes this bootstrap.

## CURRENT state

- **Live GitHub is authoritative.**
- **Wave 5: COMPLETE / CLOSED.** **Wave 6 P0: COMPLETE / FROZEN.**
- **Implementation is closed through Batches 1–6** (Wave-6 P1–P3 through Batch 6 + P4 for Batches 1–6,
  MERGED / CLOSED). This is unchanged by the census refresh:
  - implementation `main`: `2ca4d19830755864acec153f99f2659f413802cb`
  - implementation tree: `837c92893ab248f6185a36dc3b13f353495f5c9d`
  - catalogue **100** · collections **1** · `/read` discovery **64** / visible **39** · sitemap **3672 / 0 dup** · build **3681 / 3676**.
- **Short-story census refreshed (2026-09-16) from live `pugazg/kalaignar-short-stories`**
  (`main` `7205a10892d0b208df2617766844f480b6a2c798`, tree `1be34cc368fbc96ff72933a004a074ef840168ee`).

## Refreshed Wave-6 completed population = 138

- **22** already-implemented non-short-story Wave-6 works (Batches 1–6).
- **116** completed canonical short stories = **combined future Batch 7**.
- `22 + 116 = 138` (old total was 125 = 22 + 103; **+13** short stories completed since the old census).

## Batch 7 — all completed short stories (single implementation batch)

- **116 canonical short-story works**, enumerated deterministically in `WAVE6_BATCH7_SHORT_STORIES.md`.
- Internal source/provenance groups are **validation partitions only**, NOT separate implementation
  batches: `2008 40 + 2004 34 + 1987 23 + 2009 5 + 1982 6 + periodical 3 + 1976 2 + 1969 1 + 1953-thappivittargal 1 + 1997 1 = 116`.
  The old conceptual B7–B11 split is **superseded** — Batch 7 is one combined batch.
- Derivation cross-check: `154 stories/ dirs − 37 (1977 anthology members) − 1 (kizhavan-kanavu, already implemented) = 116`.
- **1982 is a 6-story anthology** (`நந்தியூர் நரியப்பன்` and `நரியூர் நந்தியப்பன்` are separate canonical stories — never collapse).
- **Witness-only** source entries (1950, 1953-naadum, 1956, 1979, and the per-collection witnesses of
  1976/1997/1969/1953/1987/2009/periodical) do **not** become new LibraryWorks.

## Intentional exclusions — NOT automatic future short-story work

- **`தேனலைகள்` (1958):** already represented in the essays / கட்டுரைகள் workstream under `மீசை முளைத்த வயதில்`
  (cross-repository overlap). Its 12 mapped headings are **NOT** Batch-7 short-story candidates. Do not silently reopen.
- **`நடுத்தெரு நாராயணி`:** intentionally excluded from the short-story programme because it is handled
  through the separate `அரும்பு` / short-novel source path. Not in Batch 7.

## Collection model — Batch-7 P1 decisions (not decided yet)

Do not auto-create a public collection per source. Candidates: 2008 / 2004 / 1987 / 1982. **Open owner
question:** for the 2009 source, whether collection membership should include its 11 existing-canonical
witnesses via the plural collection-membership model. 1997 / 1969 / periodical / single-new-canonical
containers are not public collections on their own. See the manifest's collection-model audit.

## Projections (future state only — nothing implemented)

If Batch 7 later onboards all 116: catalogue `100 + 116 = 216`; Fiction shelf `41 + 116 = 157`.

## Next execution activity — await explicit owner direction

**Batch-7 P1 has NOT started. Wave-6 P5 is NOT authorized. Wave-6 P6 is NOT authorized. No new source
ingestion is authorized.** Do not begin Batch-7 implementation, generate payloads, create routes, or
modify catalogue/discovery/sitemap on the strength of this bootstrap. The next chat must fetch live
GitHub state and await explicit owner authorization.

## Workflow contract

- **Claude Code performs GitHub writes, branches, commits, PR corrections and merges.**
- **ChatGPT independently reviews exact live state and supplies prompts.**
- **Live GitHub and production beat copied prompts/reports.**

**STOP. Batch-7 P1 is NOT started; P5 / P6 remain NOT authorized. The census refresh changed control
documents only — no implementation, public, or source state changed.**
