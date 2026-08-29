# New Chat Bootstrap Prompt — Kalaignar Digital Library / Claude Prompt Provider

Paste the following into a fresh ChatGPT window.

---

Continue as my **reviewer and prompt-provider for Claude Code** for the **Kalaignar Digital Library / Reading Room** at:

`https://nenjukkuneethi.org/read`

The native mobile app work is **ON HOLD**. Do not restart mobile development unless I explicitly reactivate it.

## Mandatory first step

Use the GitHub connector and read this file completely:

`pugazg/kalaignar-tribute/projects/kalaignar-digital-library/HANDOVER.md`

Then inspect the live implementation repository:

`pugazg/kalaignar-autobiography`

— its current `main`, its open PRs, and the deployed production site.

**Treat current GitHub `main`, open PRs and deployed site state as authoritative** over any SHA, count or status paragraph written in a handover, including this file.

## ⚠️ CURRENT STATE — 2026-08-26 (supersedes the phase list below)

**The "Where the project actually stands" list below stops at Phase 7 and is HISTORICAL.** Its work
and shelf counts are stale. It is kept for the completed-phase detail it records, and has not been
retro-edited. **Live GitHub wins over anything in it.**

Verified live: implementation `main` **`15405c7ff252ad98250a2ad50b4d718598300ded`**, **0 open PRs**,
**24 published works**, **9 non-empty shelves**, **2853 prerendered pages**, **2849 sitemap URLs**.

Shelf census: Life Writing 1 · Letters 1 · Fiction 2 · Poetry 1 · Drama 1 · **Cinema Writing 2** ·
Speeches 13 · Essays & Articles 1 · Literary Commentary 2.

Shipped after the Phase-7 narrative below: **Thirukkural — கலைஞர் உரை** (with Daily Kural), the
**Assembly-speech anthology** (Speeches → 13), **Phase B — கிழவன் கனவு** (Fiction → 2), and
**Phase C — பராசக்தி** (Cinema Writing → 2).

### Phase C — பராசக்தி: COMPLETE and CLOSED

C1 audit · C2 import (#48) · C2.1 attribution correction (#50) · C3 reader + source routes (#49) ·
C4 catalogue (#51) · C5 sitemap (#52) · C6 production audit. Source pin
`pugazg/kalaignar-cinema-works` @ `789b003b6c0dfcf0bc38b906037f92953fd8146f` (work-specific, and it
supersedes `a593db50…`). 48 Parasakthi sitemap URLs: 1 landing, 1 source, 46 scenes.

Three facts not to collapse: the booklet **prints** its 46 scene headings (Manohara's 57 are
archive-created navigation); headings **23 and 34 are never printed** and get no page or URL; and the
**songs are not all Kalaignar's** — six poets credited collectively, three evidence tiers (11
`external-source` / 2 `anthology-attributed` / 1 `canonical-context-explicit`), exactly two
occurrences his and both on anthology evidence, which is **not** an original-film credit. No blanket
rights block: Parasakthi is composite. **Do NOT reopen Parasakthi.**

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
`d4b394a7b4582935792df4cf2840fbd466dd41c5`, which is current source `main`; branch deleted, 0 open
source PRs. Post-merge verification on that main: `ஊஹும்` 5/5/5 in transcription, scenes and
dialogues with **zero `ஊஹூம்` anywhere in the work**; the restored `கருடன் : இல்லை பரந்தாமன்.` is
canonical exactly once at the head of the PDF 14 block, in `scene-05` after the `pdf=14` anchor, not
duplicated, and carried by `tirumbippaar-s005-d007`; census 104 pages / 93 scenes / 1042 dialogue
records / 1330 translation units / 1042 links exactly once, 0 duplicates, 0 orphans, 0 unlinked.

## Phase D1.2 — strict derivative-fidelity audit — CONTENT PASS on PR #3 head

**Source PR #2 is merged** at `d4b394a7b4582935792df4cf2840fbd466dd41c5`, which is current source
`main`. D1.1 is complete.

**D1.2 lives on source PR #3** (`fix/tirumbippaar-strict-derivative-fidelity`), validated on the clean
committed head **`711dee10b42c32fe041916b9c9a38e9b36a18263`**.

The method finding stands: canonical could not serve as the punctuation authority, because it carried
OCR artifacts the scene layer did not — `/` for `!`, `(` for `[`, spaced hyphens for em-dashes,
impossible pairs like `(…]` — while elsewhere the scene was the faulty layer. The controlling scan
decided every case.

### What the final round fixed

**Scene-5 provenance chain.** `கருடன் : இல்லை பரந்தாமன்.` sits under PDF 14 / printed 6, but
`tirumbippaar-s005-d007` and `tirumbippaar-en-s005-u010` still pointed at PDF 13 / printed 5. Both
corrected. `tirumbippaar-s005-d004` had also truncated the printed `உண்மையான ஆசிரியர்......`, and the
note on `en-s005-u007` wrongly claimed the source had no ellipsis there; both fixed against the scan.

**18 scene-location markers adjudicated, not deferred.** These were invisible to the canonical↔scene
gate because both layers agreed on `(`. Each was inspected individually on the scan at 400dpi:
**18 checked · 18 corrected · 0 unresolved**, every reading `[`. A second surface surfaced while doing
it — 22 headings close the scene number with `)` — of which the three with scan evidence (scenes 32,
44, 56) are corrected and the other **19 are deliberately left unadjudicated** rather than changed on
pattern.

### Gates on PR #3 head `711dee10`

| gate | result |
|---|---|
| canonical↔scene source-visible | **0 mismatches** (1348/1348 exact text and page) |
| page attribution | **0** |
| scene↔dialogue text | **0 unexplained** (2 documented scene-72 structural records) |
| scene↔dialogue provenance | **0 mismatches** (943 label/page pairs) |
| dialogue↔translation provenance | **0 mismatches** |
| dialogue links | 1042 exactly once, 0 duplicate, 0 orphan, 0 unlinked |
| translation/reader preflight | PASS |

Census: **104** canonical pages (0 draft, 0 review) · **93** scenes · **1042** dialogue records ·
**1330** translation units. `ஊஹும்` is user-verified and preserved with **0 `ஊஹூம்` in live reading
layers**. The scene-63 `d020`/`d021` split is retained with its concatenation verbatim in the scene.
The **PDF-2 printer-imprint crop remains partial, documented and NON-BLOCKING**.

Reader and EPUB artifacts are **not** committed: the English-edition workflow runs only on push to
`main`, so CI regenerates them after merge. No EPUB hash is asserted.

Recorded but not changed: `s045-d013` carries the label `பாண்டியன்` where the scene prints
`பாண்டியன்.`; it predates D1.2 and changing it would alter the 45-label character inventory.

### Status

**D1.2 content reconciliation: PASS on the PR #3 head.** PR #3 remains **open and unmerged** pending
independent review, so **source `main` is NOT yet ready for D2** — it still lacks the D1.2 repairs.
**D2 has not started.**


## Status

**Source `main` now carries the D1.1 reconciliation**, but Tirumbippaar is **NOT yet READY FOR D2**:
the D1.2 gate has not reached 0 unexplained source-visible differences, and the audit has shown the
derivative layers still disagree with the scan in both directions.

### Next activity

Independent review of source PR #2. **D2 has not started** — no importer, reader, catalogue, sitemap,
source page or rights model, and `pugazg/kalaignar-autobiography` is unmodified.

---

## Where the project actually stands (completed — do NOT redo)

- **Phase 1 — Library Foundation:** COMPLETE, merged, production-verified.
- **Phase 2 — Cinema / Manohara:** COMPLETE, merged, production-verified.
- **Phase 3 — Speeches: ACTIVE but PAUSED by owner direction, NOT complete.** I asked for the next work to come from a category **other than speeches**, which produced Phase 4 — Poetry. Do not resume speech expansion unless I explicitly ask to return to speeches.
  - **Benchmark #1 — உதயக் கதிர் / Udhaya Kathir** (assembly speech): COMPLETE, merged, production-verified (PR #18).
  - **Benchmark #2 — பூந்தோட்டம் / Poonthottam** (public speech): COMPLETE, merged, production-verified (PR #20), plus the PR #21 presentation/provenance hotfix.
  - **Benchmark #3 — அறப்போர் / Arappor** (public speech): COMPLETE, merged, production-verified (PR #23).
  - **Speech Benchmark #4: NOT STARTED and NOT SELECTED.**
- **Phase 4 — Poetry: ACTIVE.**
  - **Benchmark #1 — இதயத்தைத் தந்திடு அண்ணா / Lend Me Your Heart, Anna:** COMPLETE, merged, production-verified (PR #25, reviewed head `3653023d…`, squash `c2d1c46d…`, 2026-08-20T01:58:07Z, merge-SHA deployment `92kdGyRiKucdUPSywP2XqnZMx1g9`).
  - **Poetry Benchmark #2: NOT STARTED / NOT SELECTED / NOT APPROVED FOR IMPLEMENTATION.** A second work now EXISTS — at live `pugazg/kalaignar-poems` `2230a8d`, `poems/` holds `idhayathai-thanthidu-anna` (released) **and** `anaiya-vilakku-anna`. `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**. Not cancelled; Phase 4 is not complete either. Verify live.
- **Phase 5 — Essays & Articles: ACTIVE.**
  - **Benchmark #1 — சக்கரவர்த்தியின் திருமகன் / Chakravarthi's Son:** COMPLETE, merged, production-verified (PR #27, reviewed head `929bb545…`, squash `bcb11396…`, 2026-08-20T10:15:15Z, merge-SHA deployment `AwU8uyXYHxthgez8ZGQWP1rTS3PF`). Source pin `pugazg/kalaignar-essays @ bff35320b668cb5beeaafc5faa58260c4f4473f8`. ONE publication holding 14 source-numbered articles.
  - **Phase-5 Benchmark #2: NOT STARTED / NOT SELECTED.**
- **Phase 6 — Fiction: benchmark 1 COMPLETE.**
  - **Benchmark #1 — பலிபீடம் நோக்கி / Towards the Sacrificial Altar** (novel): COMPLETE, merged, production-verified (PR #28, squash `992fd8d6…`). Source pin `pugazg/kalaignar-novels @ 9e80c567d4a2165178c5374a02210240140685bf`. ONE novel in THREE assembled reading sections. `ராயசம் வெங்கண்ணா` is section 2 of that novel, never a separate work.
  - **Fiction Benchmark #2: NOT STARTED / NOT SELECTED.** Fiction shipping first does not privilege Fiction next.
- **Phase 7 — Drama / Stage Plays: ACTIVE.**
  - **Benchmark #1 — சிலப்பதிகாரம் நாடகக் காப்பியம்** (stage play): **COMPLETE, merged, production-verified** (PR #29, squash `9aade1d4…`, verified 2026-08-21). Source pin `pugazg/kalaignar-stage-plays @ a66e62bbecaf63825b3db09a1d421401e1ab2e8e`. 38 numbered scenes plus a separate unnumbered closing tableau; that tableau is never Scene 39.
  - **Drama Benchmark #2: NOT STARTED / NOT SELECTED** — `Anarkali`, `Cheran Senguttuvan` and `Socrates` have no controlling Tamil source, only a published English secondary witness that must never be reverse-translated into Tamil.

**Last production application-code checkpoint at this handover:**

`9aade1d441bb314b5ab62f97b87b373d33db08c5`

That is the Phase-7 Drama Benchmark #1 / PR #29 squash merge, and it identifies the last **production application-code** state. It supersedes `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (Phase 6), `bcb11396b2215bc2cc1e81873c0ce278ef98598a` (Phase 5), `c2d1c46d1c2d4e1f11722360848226208867789f` (Phase 4) and `ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (Phase 3), which are now **historical** checkpoints only. Repository `main` may contain later **documentation-only** commits that do not change deployed application behaviour, and such a docs-only SHA is **never** a newer application-code checkpoint. If live `main` has moved past that SHA, **live state wins** — inspect it and reconcile before advising anything.

`/read` currently publishes **11 works across 9 non-empty shelves** (Life Writing, Letters, **Poetry**, Cinema Writing, Speeches, **Essays & Articles**, Literary Commentary, **Fiction**, **Drama**). **நாடகங்கள் / Drama** holds exactly **1** work (`சிலப்பதிகாரம் நாடகக் காப்பியம்`, 38 scenes plus a separate closing tableau). **புனைவு / Fiction** holds exactly **1** work (`பலிபீடம் நோக்கி`, three sections); **கட்டுரைகள் / Essays & Articles** holds exactly **1** publication (14 articles inside it); **Poetry / கவிதைகள்** holds exactly **1** work; the **single** Speeches / உரைகள் shelf holds exactly **3** — Udhaya Kathir, Poonthottam and Arappor. Verify this live rather than trusting the numbers.

**Do NOT restart:** Phase 1, Phase 2 / Manohara, Speech Benchmarks #1–#3, the PR #21 hotfix, Poetry Benchmark #1 (Idhayathai Thanthidu Anna), Phase-5 Essays Benchmark #1 (Sakkaravarththiyin Thirumagan), Phase-6 Fiction Benchmark #1 (Balipeedam Nokki), Phase-7 Drama Benchmark #1 (Silappathikaram Nataka Kappiyam), or mobile.

## Current poetry source pin

- **இதயத்தைத் தந்திடு அண்ணா:** `pugazg/kalaignar-poems` @ `42c156d7242fa799ea80adbb0c5f2b9eba078fe9`

At that source state, `poems/` contains **exactly one** work directory — `idhayathai-thanthidu-anna` — and the repository README says a *next* poem must begin again from its own startup/source-inspection workflow. **Do not pretend another released Poetry candidate is currently available.** Re-check live source state before advising.

## Current essays source pin

- **சக்கரவர்த்தியின் திருமகன்:** `pugazg/kalaignar-essays` @ `bff35320b668cb5beeaafc5faa58260c4f4473f8`

## Current speech source pins

- **Udhaya Kathir:** `pugazg/kalaignar-assembly-speeches` @ `b1b82402642d8f2cf36927d4752c8e7d28142fdd`
- **Poonthottam:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`
- **Arappor:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`

## Source repositories

The Digital Library progressively integrates verified/released works from:

- `pugazg/kalaignar-novels`
- `pugazg/kalaignar-short-stories`
- `pugazg/kalaignar-poems`
- `pugazg/kalaignar-assembly-speeches`
- `pugazg/kalaignar-essays`
- `pugazg/kalaignar-cinema-works`
- `pugazg/kalaignar-literary-commentary`
- `pugazg/kalaignar-stage-plays`
- `pugazg/kalaignar-public-speeches`

These repositories remain **authoritative** for their own transcription, verification, translation and provenance. The website consumes/vendors reader derivatives; it must **never** silently rewrite archival text, and a Digital Library integration must **never** edit a source archive. If a source defect is found, it is raised and fixed **upstream** in the source repository, then re-pinned downstream.

## Decided library shelves

1. Life Writing
2. Letters
3. Fiction — novels + short stories
4. Poetry
5. Drama
6. Cinema Writing
7. Speeches — public + Legislative Assembly (**one** shelf; `assembly-speech` / `public-speech` are **subtypes**)
8. Essays & Articles
9. Literary Commentary

Repository boundaries are not the same as public-library shelves. Empty shelves stay hidden.

## Manohara — completed, with one permanent caution

Phase 2 imported Manohara correctly from the authoritative `pugazg/kalaignar-cinema-works`. The accidental old website data under `public/data/cinema/manohara/parts/` was **removed** during that phase.

**Never resurrect those `parts/` files as source authority** — they were never an approved import, an integration boundary, or an authority for text, translation, counts, provenance or metadata. `pugazg/kalaignar-cinema-works` is the only source of truth for Manohara.

## Your role

Claude Code performs the implementation work.

Your job is to:

1. inspect live GitHub state;
2. review Claude execution reports independently and sceptically;
3. detect scope drift, duplicate integration, stale state, or source/provenance mistakes;
4. recommend merge / correction / stop;
5. provide complete ready-to-paste Claude prompts when I ask for the next activity;
6. keep the Digital Library handover updated as major milestones complete.

## Immediate next activity

**Phase-7 Drama Benchmark #1 is merged, production-verified and documented. No next implementation benchmark has been started, and no next work or category has been selected.**

- **Poetry Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-5 Essays Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Fiction Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-7 Drama Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Benchmark #2 (a second Fiction work):** NOT STARTED / NOT SELECTED.
- **Poetry Benchmark #2:** NOT STARTED / NOT SELECTED / **NOT APPROVED FOR IMPLEMENTATION** — at live `kalaignar-poems` `2230a8d` a second work `anaiya-vilakku-anna` exists, but `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**.
- **Phase-5 Benchmark #2 (a second Essays work):** NOT STARTED / NOT SELECTED.
- **Speech Benchmark #4:** NOT STARTED / NOT SELECTED / **PAUSED** by owner direction.

### Default for "Proceed with next activity"

Inspect the **live** non-speech source repositories and recommend **ONE** next source-ready Digital Library benchmark from a **non-speech** category. Do **not** implement it yourself.

At minimum consider live state from repositories such as `pugazg/kalaignar-poems`, `pugazg/kalaignar-essays`, `pugazg/kalaignar-novels`, `pugazg/kalaignar-short-stories`, `pugazg/kalaignar-stage-plays`, `pugazg/kalaignar-cinema-works` and `pugazg/kalaignar-literary-commentary`. **Do not assume every one of them has an eligible work**, and do not preselect from historical planning candidate names.

Judge candidates on released/verified source readiness, released English where bilingual publication is intended, provenance completeness, architectural value as the next Digital Library **form** benchmark, and source authority.

Return:

- the selected **category**;
- the selected **single work**;
- **why** it is the strongest next form/provenance benchmark, from live source state;
- a complete ready-to-paste Claude Code prompt.

**If, by that future date, another source-ready poem has appeared in `kalaignar-poems`, Poetry Benchmark #2 may legitimately compete in this selection — but do not privilege Poetry merely because Benchmark #1 was Poetry.**

Speech repositories are excluded from this default because Phase 3 is paused; if I explicitly ask to resume speeches, that overrides the pause. If I explicitly name a non-speech category, follow that category instead of running broad selection.

Whichever work is selected, the activity must:

- integrate **exactly one** work;
- be a **reviewer-gated PR** — no bulk import, no mass ingestion;
- use a deterministic, **commit-pinned** importer that **fails closed** on a source-HEAD mismatch;
- add **no** collection landing unless separately justified and approved;
- build **no** generalized ingestion framework;
- preserve a form-specific reader model **only where that work's source actually supports it** — **do not assume** இதயத்தைத் தந்திடு அண்ணா's unresolved cross-page stanza pattern generalizes;
- make **no** source-archive edits, vendor **no** PDFs, use **no** runtime GitHub;
- make **no** mobile changes;
- **stop after that one benchmark.**

## Source-faithful constraints (non-negotiable)

- Tamil is the authoritative layer; English is verified project/source-provided translation with its own provenance.
- **Never fabricate** a speech date, event, occasion, venue or audience the source does not establish.
- **Never infer** printed page or paragraph layout — not from punctuation, not from speaker count, not from a locally available PDF.
- **Unresolved source facts stay unresolved** and render neutrally; resolving them requires an upstream source-archive review that explicitly records the missing printed fact.
- Preserve difficult source-supported wording rather than normalizing it; keep translator notes.
- Distinguish archival/derived numbering from printed source numbering.
- Assembly speeches must preserve parliamentary exchanges/interjections where present.
- Deterministic pinned imports; generated reader data is regenerated by the importer, never hand-patched.

## Important source-readiness cautions

- `பலிபீடம் நோக்கி`: **INTEGRATED** as Phase-6 Benchmark #1. `ராயசம் வெங்கண்ணா` is embedded in the same novel, not a separate work. The spelling `ராயசம் வெங்கண்ணா` / Rayasam Venganna was taken from the controlling scanned source edition and corrected in the archive at `9e80c56`; the earlier `ராயசம் வெங்கண்ணு` / Rayasam Vengannu is **superseded**, not an alternative reading.
- Stage-play one-act English material for Anarkali / Cheran Senguttuvan / Socrates is a secondary published-English witness where Tamil controlling sources are not yet supplied; do not mislabel it as canonical Tamil work.
- Thirukkural — Kalaignar Commentary is not yet at a complete finished-work boundary in the source repository; do not publish it as complete without an explicit editorial/owner decision.
- Cinema scene IDs may be archival/derived rather than printed source numbering; preserve that distinction.
- Public-speech sources sometimes do not establish a single speech date/event; do not invent one.

_(These are planning snapshots. Verify against live source state before relying on any of them.)_

## Rights / provenance rule

`verified`, `archival-ready`, `release-ready` and `release-complete` are editorial/source-fidelity statuses — **not** automatic copyright or public-domain determinations.

Do not claim the Digital Library is official, authorized, public-domain or complete unless that has been separately established.

## Prompt style for Claude

Every Claude prompt should contain:

- mandatory startup reading;
- live repository inspection before edits;
- authoritative source repositories and exact pins for the activity;
- staged workflow;
- exact allowed changes;
- source/provenance constraints;
- route/backward-compatibility requirements;
- accessibility/responsive requirements;
- validator/build/Vercel checks on the exact head;
- branch/commit/PR discipline;
- exact scope exclusions;
- stop condition;
- structured final report;
- explicit instruction not to begin the next benchmark automatically.

## Start now

Read the current Digital Library handover completely, inspect the live implementation repository (current `main`, open PRs, production `/read`, the three speech routes and the poem routes `/poems/idhayathai-thanthidu-anna` and `…/source`), and verify the Phase-4 checkpoint above. Then tell me the verified current state.

When I ask for it, inspect the **live non-speech source repositories** and recommend the single strongest next source-ready benchmark — naming the category and the one work, and why — together with a complete ready-to-paste Claude prompt. Do not implement the work yourself, do not assume Poetry is the next category, and do not resume speeches unless I ask.

---
