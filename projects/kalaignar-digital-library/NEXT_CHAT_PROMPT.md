# New Chat Bootstrap Prompt — Kalaignar Digital Library / after Wave-6 Batch-5 closure

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub is authoritative. Do not trust copied SHAs, PR bodies or this
bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely** (its highest-precedence CURRENT
   checkpoint is the 2026-09-10 Wave-6 Batch-5 **MERGED / CLOSED** state).
3. Inspect all open control PRs.
4. Fetch live `pugazg/kalaignar-autobiography` `main` and inspect all open implementation PRs.
5. Re-fetch live `pugazg/kalaignar-novels` `main` and resolve the two Batch-5 target subtrees.
6. Treat any newer legitimate live state as authoritative and update the reasoning accordingly.

## CURRENT state — Wave-6 P1–P3 merged through Batch 5

- **Live GitHub is authoritative.**
- **Wave 5: COMPLETE / CLOSED.**
- **Wave 6 P0: COMPLETE / FROZEN.**
- **Wave-6 P1 → P2 → P3: merged through Batch 5** (Cinema, Drama, Speeches, Poetry, Novels).
- Implementation `main` is anchored by the Batch-5 merge commit
  **`bb0beaa0a18f97336b52319c1e7b15e62d81d1ed`**, tree **`2fdc92b40d66c60caf4042b327babed97e53ae94`**,
  unless live `main` has legitimately advanced since this docs sync — in which case live wins.
- **17 / 125 READY works merged** through P3.
- **Cumulative Wave-6 direct routes: 247.**
- **Wave-6 P4 is NOT AUTHORIZED.**
- **Batch 6 has NOT started.**

Wave-6 merged progress: Batch 1 Cinema +65 (65) · Batch 2 Drama +83 (148) · Batch 3 Speeches +6 (154) ·
Batch 4 Poetry +30 (184) · **Batch 5 Novels MERGED / CLOSED +63 (247)**.

## Batch-5 durable facts (for continuity)

- Implementation PR **#83** is **MERGED / CLOSED**; approved head `5226f10e265bff981692b9b70f834230de94a200`
  / tree `2fdc92b40d66c60caf4042b327babed97e53ae94`; merge commit `bb0beaa0…`; post-merge
  `main` tree **equals** the approved PR-head tree (integrity gate **PASS**).
- Source anchor (adjudicated, immutable for Batch 5): `pugazg/kalaignar-novels`
  commit `d6679e46051ab93de8da6361413c39e7db468cfe`, tree `e4ea40ffd495fe084221541f9ca5fd48742dee3e`;
  target subtrees `works/periya-idathup-pen` `47168b63142012ade56ec832e8977c494d0027a6`,
  `works/pudhaiyal` `450d7da31a0f2eed5c12d43e4082edb758134618`; literary freeze retained in the
  byte-stable `novel.json` payloads `a99f135467dd38e294faff31088a937994790a47`.
- Literary/routing model: `periya-idathup-pen` = one continuous work, **7** canonical archive reading
  sections → **9 direct routes**; `pudhaiyal` = **52 literary units** (`00-arimugam`/`00-introduction`
  + Chapters 01–51) → **54 direct routes**. Never say Periya has 18 sections; never say Pudhaiyal has 54
  literary sections (it has **52 literary units / 54 total direct routes**).

## P4 freeze — must remain unchanged

Confirm catalogue **78** · public collections **1** · sitemap **3351 / 0 duplicates** · Poetry discovery
**6** · Fiction discovery **3** · zero Batch-5 sitemap/catalogue/discovery exposure · `/read` does not
expose the Wave-6 P1–P3 works. **Wave-6 P4 is NOT AUTHORIZED.**

## Next execution activity — await explicit owner direction

Batch 5 P1–P3 is closed. **Do NOT automatically begin Batch 6, and do not authorize Batch 6 merely
because the broader Wave-6 programme exists.** The next chat must first fetch live state and then **await
explicit owner direction** for the next execution activity (e.g. the next READY-works batch, or any other
task the owner names). Only the owner authorizes starting the next batch or Wave-6 P4.

## Workflow contract

- **Claude Code performs GitHub writes, branches, commits, PR corrections and merges.**
- **ChatGPT independently reviews exact live state and supplies prompts.**
- **Live GitHub and production beat copied prompts/reports.**

**STOP after Batch 5. Wave-6 P4 remains NOT AUTHORIZED. Batch 6 is NOT started and requires explicit
owner authorization.**
