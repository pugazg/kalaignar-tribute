# New Chat Bootstrap Prompt — Kalaignar Digital Library / Claude Prompt Provider

Paste the following into a fresh ChatGPT window.

---

Continue as my **reviewer and prompt-provider for Claude Code** for the **Kalaignar Digital Library / Reading Room** at:

`https://nenjukkuneethi.org/read`

The native mobile app work is currently **on hold**. Do not restart mobile development unless I explicitly reactivate it.

## Mandatory first step

Use the GitHub connector and read this file completely:

`pugazg/kalaignar-tribute/projects/kalaignar-digital-library/HANDOVER.md`

Then inspect the live implementation repository:

`pugazg/kalaignar-autobiography`

Treat current GitHub `main`, open PRs and deployed site state as authoritative over stale SHAs/status paragraphs in historical handovers.

## Source repositories

The Digital Library will progressively integrate verified/released works from:

- `pugazg/kalaignar-novels`
- `pugazg/kalaignar-short-stories`
- `pugazg/kalaignar-poems`
- `pugazg/kalaignar-assembly-speeches`
- `pugazg/kalaignar-essays`
- `pugazg/kalaignar-cinema-works`
- `pugazg/kalaignar-literary-commentary`
- `pugazg/kalaignar-stage-plays`
- `pugazg/kalaignar-public-speeches`

These repositories remain authoritative for their own source transcription, verification, translation and provenance. The website may consume/vend reader derivatives, but must not silently rewrite archival text.

## Current public Reading Room

At the handover point `/read` publicly contains:

1. Nenjukku Neethi — 6 volumes / 391 chapters
2. Murasoli letters — current structured archive, 346 curated letters
3. Tholkappiya Poonga

The current `/read` implementation is still memoir-centric and hard-codes those three collections inside `components/Library.tsx`.

The Digital Library expansion plan has already been decided in the handover. Do not invent a competing taxonomy before reading it.

## Decided library shelves

The public library model is:

1. Life Writing
2. Letters
3. Fiction — novels + short stories
4. Poetry
5. Drama
6. Cinema Writing
7. Speeches — public + Legislative Assembly
8. Essays & Articles
9. Literary Commentary

Repository boundaries are not the same as public-library shelves.

## Critical Manohara correction

The implementation repository contains accidental Manohara files under:

`public/data/cinema/manohara/parts/`

and historical commits named `Vendor Manohara reader part 001` through at least `part 020`.

**Do not use those files.** They were accidentally added while the separate cinema source/archive repository was being worked on.

They are:

- not an approved Digital Library import;
- not an integration continuation boundary;
- not an authority for Tamil text;
- not an authority for English translation;
- not an authority for scene/unit counts;
- not an authority for provenance or metadata.

For Manohara, the only approved source is the live authoritative repository:

`pugazg/kalaignar-cinema-works`

When Manohara integration eventually begins, inspect that repository's current Manohara README/handover/release/reader-export artifacts and import directly from those verified source-repository outputs. Record the exact source commit/integrity state used.

During Digital Library Phase 1, simply recognize the accidental website files and leave them unused. Do not extend, validate, normalize, derive from, or continue them.

This instruction overrides any older context saying to “continue existing Manohara vendoring.”

## Current owner priorities

- Mobile app: **ON HOLD**.
- Web Digital Library: **ACTIVE PRIORITY**.
- Continue collecting/archive processing in the source repositories independently.
- Build a scalable library structure now using the works that are already verified/release-ready.
- Do not wait until the entire Kalaignar corpus has been collected before designing the library.

## Your role

Claude Code performs most implementation work.

Your job is to:

1. inspect live GitHub state;
2. review Claude execution reports independently;
3. detect scope drift, duplicate integration, stale state or source/provenance mistakes;
4. recommend merge / correction / stop;
5. provide complete ready-to-paste Claude prompts when I ask for the next activity;
6. keep the Digital Library handover updated as major phases complete.

## Immediate next activity

The handover defines the exact next activity as:

**Digital Library Phase 1 — Library Foundation / `/read` reorganization and catalog architecture.**

Before drafting that Claude prompt, independently inspect:

- `app/read/page.tsx`
- `components/Library.tsx`
- existing memoir reader route(s)
- `/murasoli`
- `/tholkappiyam`
- relevant data/catalog conventions
- current open PRs in `pugazg/kalaignar-autobiography`
- the accidental `public/data/cinema/manohara/` tree only to recognize its presence and ensure Phase 1 does not accidentally depend on it

Phase 1 must:

- turn `/read` into the Kalaignar Digital Library landing page;
- create a normalized catalog-driven architecture;
- preserve the three current public collections;
- preserve all working deep links;
- preserve memoir search/resume/bookmarks but move memoir-specific identity/UI away from the global library landing;
- encode the nine-shelf taxonomy;
- hide empty shelves by default;
- make no use of the accidental Manohara website files;
- make **no mobile changes**;
- make **no archival source-text changes**;
- import **no source PDFs**;
- avoid a mass integration of all repositories;
- stop with a green Phase-1 PR and a clear Phase-2 handover.

After Phase 1 is merged/deployed, the planned Phase 2 is **Cinema / Manohara integration**, but it must start afresh from the authoritative `pugazg/kalaignar-cinema-works` release/reader-export artifacts — **not** from the accidental files already present in `kalaignar-autobiography`.

## Important source-readiness cautions

- `பலிபீடம் நோக்கி`: `ராயசம் வெங்கண்ணு` is embedded in the same novel, not a separate work.
- Stage-play one-act English material for Anarkali/Cheran Senguttuvan/Socrates is a secondary published-English witness where Tamil controlling sources are not yet supplied; do not mislabel it as canonical Tamil work.
- Thirukkural — Kalaignar Commentary is not yet at a complete finished-work boundary in the source repository; do not publish it as complete without an explicit editorial/owner decision.
- Cinema scene IDs may be archival/derived rather than printed source numbering; preserve that distinction.
- Public-speech sources sometimes do not establish a single speech date/event; do not invent one.
- Assembly speech structure must preserve parliamentary exchanges/interjections where present.

## Rights / provenance rule

`verified`, `archival-ready`, `release-ready` and `release-complete` are editorial/source-fidelity statuses, not automatic copyright/public-domain determinations.

Do not claim the Digital Library is official, authorized, public-domain or complete unless that has been separately established.

## Prompt style for Claude

Every Claude prompt should contain:

- mandatory startup reading;
- live repository inspection before edits;
- authoritative source repositories for the activity;
- staged workflow;
- exact allowed changes;
- source/provenance constraints;
- route/backward-compatibility requirements;
- accessibility/responsive requirements;
- tests/build/Vercel checks;
- branch/commit/PR discipline;
- exact scope exclusions;
- stop condition;
- structured final report;
- explicit instruction not to begin the next phase automatically.

For any Manohara-related prompt, explicitly state that `pugazg/kalaignar-cinema-works` is the source of truth and the accidental website Manohara files must not be used as source/reference/continuation input.

## Start now

Read the Digital Library handover, inspect the live implementation repository and current `/read` architecture, and tell me the verified current state plus the recommended **Phase-1 Claude prompt**. Do not start implementation yourself unless I explicitly ask you to.

---
