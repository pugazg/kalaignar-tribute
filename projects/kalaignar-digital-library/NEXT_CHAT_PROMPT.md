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

## ⚠️ CURRENT STATE — 2026-09-02, post-Wave-3 (supersedes the phase list below)

**The "Where the project actually stands" list below stops at Phase 7 and is HISTORICAL.** Its work
and shelf counts are stale. It is kept for completed-phase detail and has not been retro-edited.
**Live GitHub wins over anything in it.**

Measured at the Wave-3 production boundary: implementation `main`
**`c4660c49edb20895d11751e4454942e46e8b0951`**, **0 open implementation PRs**, **71 published works**,
**Essays & Articles 4**, **9 non-empty shelves**, **3128 Next build static-route count**, **3116 sitemap
URLs**. The continuity-only prerendered `.html` figure is **3120** and is not the static-route count.

Shelf census: Life Writing 1 · Letters 1 · Fiction 39 · Poetry 1 · Drama 5 · Cinema Writing 4 ·
Speeches 14 · **Essays & Articles 4** · Literary Commentary 2. Total **71**.

### Bulk Onboarding Wave 3 — Essays & Articles — ✅ COMPLETE; control closure proposed

Exactly three publications were onboarded together:

- `கயிற்றில் தொங்கிய கணபதி` — 1 article;
- `உணர்ச்சிமாலை` — 10 articles;
- `திராவிட சம்பத்து` — 2 articles, damaged/out-of-order source.

Implementation PR **#66**. First reviewed head `d50aefae5cc5a665230a4185aab43d16c7dfeb81`
was **NOT APPROVED** despite green CI because `/source` route metadata still leaked the reference work's
14-article/reprint/rights claims. Repaired exact head
**`c4f40f7f77a115700915f17e65c2a2a1ddf54bbd`** was independently reviewed and APPROVED FOR MERGE.
Squash `c4660c49edb20895d11751e4454942e46e8b0951`; merged tree
`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`; post-merge CI **33607016982 success**; Vercel production
success. Approved-head and merged trees are identical.

Frozen source: `pugazg/kalaignar-essays` @
**`6814e979fd3c2cefa14cbeb17eeec28164ce28f5`** with per-work trees:
`ca1c92591b9389e60d44b9683af849e3a682e528` ·
`f49d77a0733ca75f7a96fb6a1cf4631e375b05d0` ·
`fe0f6ea0482ac2cd0e8c4558edd3b452e249dbdd`. At control-close-out preparation the live source had
advanced to `8d3b3e6792f6b3a7783ff3621f4d5c8e3e9be4d4` for `இன முழக்கம்`; all three Wave-3 work trees were
rechecked and remained exactly frozen. Do not repin Wave 3 to moving source `main`.

Wave 3 added **+19 public URLs** and moved 68 → 71 works, Essays 1 → 4, static routes 3109 → 3128,
`.html` 3101 → 3120 and sitemap 3097 → 3116. All 19 new routes and all 16 reference-work routes were
production-verified 200. Final batch validator: **510 assertions / 7 groups / 0 failed**, **23/23
negative tests proven**. Reference validator: **188 assertions / 0 failed**.

`திராவிட சம்பத்து` must retain article scan runs `5–6, 13–16` and `12, 3`, reconstructed reading
order `1 → 2 → 9 → 10 → 5 → 6 → 13 → 14 → 15 → 16 → 7 → 8 → 11 → 12 → 3 → 4`, no invented printed
pagination and no reconstruction of torn text. Its visible `/source` page summarizes those provenance
facts; the exact sequence/policy is available in deployed provenance rather than fully rendered as
visible rows.

**This control-only PR proposes the durable Wave-3 close-out. The control record becomes closed only
when this PR is independently exact-head reviewed and merged.**

### NEXT ACTIVITY AFTER THIS CONTROL CLOSE-OUT

**Wave 4 is NOT SELECTED, NOT AUTHORIZED, and no Wave-4 readiness census has started.** Do not select,
rank, census or implement a next wave merely because Wave 3 is closing. Wait for explicit owner
authorization for the next activity.

Standing exclusions/status remain unchanged: Film Songs formal control close-out is separate and still
pending; validator migration is **PAUSED**; native mobile is **ON HOLD**; Manimagudam is never
auto-selected and requires its own readiness gate + owner authorization; `kalaivanar-nsk-memorial-day-audio-06`
is a separate source-active archive and is never auto-selected.

## ⚠️ CURRENT STATE — 2026-09-02, post-Wave-2 ⚠️ SUPERSEDED (kept as history)

**The "Where the project actually stands" list below stops at Phase 7 and is HISTORICAL.** Its work
and shelf counts are stale. It is kept for the completed-phase detail it records, and has not been
retro-edited. **Live GitHub wins over anything in it.**

Measured live 2026-09-02: implementation `main` **`4fd45a92663abbe70ff0c0a605168314cd36e44c`**,
**0 open PRs**, **68 published works**, **39 Fiction works**, **9 non-empty shelves**,
**3109 Next build static-route count**, **3097 sitemap URLs**.

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · Poetry 1 · Drama 5 · Cinema Writing 4 ·
Speeches 14 · Essays & Articles 1 · Literary Commentary 2. Total **68**.

These were measured now — SHA and open PRs from live GitHub, the census from `data/library.ts` at
that SHA, static routes from a production build, sitemap from the deployed site — not copied
forward.

### ⚠️ Three different page metrics — never use them interchangeably

**A site-wide TOTAL is not a wave's DELTA.** Wave 2's public contribution is **+74 URLs**
(37 reader routes + 37 `/source` routes). The build's static-route count is a *site-wide census* of
every prerendered route in the whole library. Never present the two as the same kind of number.

| metric | how it is measured | pre-Wave-2 | post-Wave-2 | delta |
|---|---|---|---|---|
| **Next build static-route count** | the `Generating static pages (N/N)` figure | 3035 | **3109** | **+74** |
| **Sitemap URLs** | `<loc>` entries in the deployed `sitemap.xml` | 3023 | **3097** | **+74** |

The two differ because the build count includes non-HTML route outputs and four non-indexed pages
(`/_not-found`, `/about`, `/privacy`, `/support`).

⚠️ **The prerendered `.html` file count is NOT the Next static-route count** and must never be quoted
as one. Post-Wave-2 those are **3101** and **3109** respectively; at the Wave-1 boundary they were
3027 and 3035. The `.html` count is the older "Prerendered pages" convention, re-measured for
continuity (a pre-Wave-1 rebuild returns exactly 3005) but measuring a different thing, and it is
**deliberately not carried as a current metric**.

*(The previous **2026-09-01 post-Wave-1** line — `0dc92fa0…`, 31 works, Fiction 2, Drama 5, 3035
static routes, 3023 sitemap URLs — is **superseded** and kept only as history, as is the pre-Wave-1
line before it: `56ca0c97…`, 27 works, 3005 prerendered pages, 3001 sitemap URLs, Drama 1.)*

### Bulk Onboarding Wave 2 — Fiction — ✅ COMPLETE and CLOSED

**The 37 short stories of the 1977 anthology கலைஞர் கருணாநிதியின் சிறுகதைகள்**, published together on
the Fiction shelf. PR **#65**, exact reviewed head **`2ba1ee3aaa5078ddc60463e45cb00bca36ae4f8d`**,
squash **`4fd45a92663abbe70ff0c0a605168314cd36e44c`**, merged tree `0a502927…`, 83 files, merged
2026-09-02T03:28:20Z; post-merge Library CI run `33587162687` success. Source pin
`pugazg/kalaignar-short-stories` @ **`76135e1b5d504128c15be6bf59937716e5517d78`**, collection tree
`d45434d46b1e779a880fff3d774d0fcb5833e477`, all 37 work trees frozen and guarded individually.

**`கிழவன் கனவு` was excluded** — a separate, earlier source, already published, and the short-story
regression benchmark. **It is not the 38th anthology story.**

**Wave 2 ran the exact-head sequence correctly end to end**: PR opened → exact head reviewed →
APPROVED FOR MERGE for `2ba1ee3a…` → head unchanged → merge → production verification → control
close-out. That is the standing process.

**The Story-29 lesson:** the first candidate pin `a9b333f1…` carried a real source defect — Story 29's
English page markers were shifted from scan 200 onward with scan 204 empty. Implementation **stopped
and reported it** rather than repairing downstream or dropping the story; the archive was corrected,
and the whole 37-tree freeze was recomputed against `76135e1b…` (only Story 29's tree changed, to
`e6eea7e2…`). **A source release gate is not permission to work around a source defect.**

Validator: **2522 assertions, 42 groups, 0 failures**; **17/17 negative tests proven**, including a
reconstruction of the old shifted anchoring. `கிழவன் கனவு` regression byte-equivalent. Full detail is
in `HANDOVER.md`.

### Bulk Onboarding Wave 1 — Drama — ✅ COMPLETE and CLOSED

**கலைஞரின் நான்மணி மாலை four-play batch** — பரதாயணம் / Bharathayanam · அனார்கலி / Anarkali ·
சாக்ரடீஸ் / Socrates · சேரன் செங்குட்டுவன் / Cheran Senguttuvan. **The first bulk-onboarding activity
in the Digital Library.** PR **#64**, squash **`0dc92fa0fd832b5932b8df75606ef049c9f261ea`**, reviewed
head `74c7f6dc…`, 24 files. Source pin `pugazg/kalaignar-stage-plays` @
**`145e52e88dbd009286f749a7f0e3520386e63244`** — one composite scan
(`TVA_BOK_0065576_நான்மணி_மாலை.pdf`, 54 scans), four frozen work trees, re-confirmed unchanged at
close-out while source `main` advances for **மணிமகுடம் only**.

Drama **1 → 5**, catalogue **27 → 31**, **+22 public URLs** (Bharathayanam 3 · Anarkali 6 ·
Socrates 7 · Cheran 6).

The architecture: `structureKind` (`scene-sequence` / `continuous-play`) and reading-unit `kind`
(`scene` / `closing-tableau` / `continuous-body`) are **source-structure** distinctions. The public
shelf and type are unchanged, and **there is no `continuous-play` catalogue subtype**.
**Bharathayanam prints no scenes** — one continuous reading unit, route slug `continuous-play`
(navigation only), catalogue `unitCount` **absent**, and it is never "Scene 1" or a "one-scene play".
**Socrates** publishes **13** verified Tamil introductory units from scans **27–28** before its **5**
source scenes — the intro is not a scene, has **no route**, and `/plays/socrates/00-introduction` is
**404**. Anarkali and Cheran hold **4** scenes each. Silappathikaram was carried through the model
rename with **byte-equivalent reading text** and its closing tableau is still **not Scene 39**.

Two durable engineering lessons came out of it — the **`empty == empty` validation trap** and the
**buffered CI-output trap**. Both are recorded in `HANDOVER.md` and both are now standing rules.
Final batch validator: **385 assertions, 7 groups, 0 failed, BATCH RESULT: ALL PASS** *(the pre-repair
355 is historical only)*.

**மணிமகுடம் / Manimagudam was excluded** because its source processing was incomplete at the freeze.
Its upstream movement does **not** add it to Wave 1, repin Wave 1, make it *automatically* eligible
for Wave 3, or authorize publication. **It is not permanently ineligible** — it remains source-active
and may become a legitimate candidate once it passes its own release/readiness gate and the owner
authorizes a wave including it.

Full detail is in `HANDOVER.md`.

### ⚠️ Exact-head review is MANDATORY before any merge

Wave 1's PR #64 was **merged before its final repaired head received independent ChatGPT exact-head
approval**; ChatGPT then performed an independent read-only **post-merge** review of the exact
merged implementation and accepted it. **That is not the
workflow and is not a precedent.**

**The standing rule:** Claude opens the PR → ChatGPT reviews the **exact current head** → ChatGPT
gives **APPROVED FOR MERGE** → only then does Claude merge. **If the head changes after approval, STOP
and re-review.** Bulk onboarding does not relax this gate.

### ⚙️ Bulk onboarding is the STANDING DEFAULT workflow

**Owner decision, recorded 2026-09-01.** This supersedes the older one-work-per-benchmark default and
the "no bulk import, no mass ingestion" constraint repeated in the historical lists further down.

1. identify a coherent batch by source release / source repository / public shelf;
2. perform a readiness census over the whole candidate set;
3. exclude incomplete or blocked works explicitly;
4. freeze each included work against source commit/tree identity;
5. use one coherent deterministic importer where appropriate;
6. use one coherent source-linked batch validator;
7. the validator **MUST still report and fail per work**;
8. preserve per-work provenance, rights and structural distinctions;
9. publish the coherent batch in one implementation PR where architecture allows;
10. use one independent ChatGPT review gate for the batch;
11. **ChatGPT reviews the EXACT current PR head and gives APPROVED FOR MERGE; merge only after that
    approval; if the head changes, STOP and re-review**;
12. **after merge, production verification, then one batch control close-out** — in that order;
13. **do not flatten source differences merely because the work is batched.**

Approval precedes merge, merge precedes production verification, and production verification precedes
the control close-out. `HANDOVER.md` carries this identical sequence.

**A batch validator must report per work and fail the whole batch on any one work's failure.**
Source-tree drift guards are **per work**, and a source repository pinned at multiple historical
commits needs **separate CI checkout directories**.

**Bulk is the default, not permission to mix.** It never authorizes combining incompatible or
incomplete sources, and it is not a claim that every future work must be bulked regardless of source
state. A work that is not source-ready is excluded explicitly.

**One-work benchmark cycles are now the EXCEPTION**, appropriate only where a work introduces a
genuinely new source form, reader architecture, unresolved rights/attribution boundary, unusual
structure, source-fidelity blocker, or implementation risk that should not be coupled to a batch.

**Two standing validator rules from Wave 1:**

- **Never let `empty == empty` certify completeness.** An importer and a validator may share a
  contract but must not share a defect that makes both derive the same empty value. For a source
  section known to exist, assert **NON-EMPTY source extraction before equality**:
  **prove presence → then prove structure → then prove equality.**
- **Validator success is not enough if the evidence cannot be read.** Avoid a final `process.exit()`
  when stdout may be buffered (Node discards buffered stdout on a pipe, which is what CI provides);
  prefer `process.exitCode`; keep deliberate fail-closed early exits; ensure failure paths report
  assertions rather than crash; test through a pipe as well as direct stdout.

### Speech Benchmark #4 — ✅ COMPLETE and CLOSED

**கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** / *Kalaivanar N. S. Krishnan
Memorial-Day Speech* (`kalaivanar-nsk-memorial-day`) — the **first audio-sourced speech** in the
Digital Library. Both stages are merged and independently verified:

- **A1** (audio-source model, import, validator, reader, provenance page, routes, sitemap, CI):
  PR **#62**, squash **`492b26ddd5681f085726ac802681c3fcbc7162f0`**
- **A2** (Reading Room catalogue onboarding): PR **#63**, squash
  **`56ca0c978e34afddde52595f2ce825872bd6aeef`**

Source pin `pugazg/kalaignar-public-speeches` @ **`1ef73a709a343390befe55dcdfb029427f527bf4`**, path
`speeches/kalaivanar-nsk-memorial-day`, tree **`256cbe2adc8dbc9c245be57196652ed79da48eeb`** — a
historical release state, re-confirmed unchanged even though source `main` keeps advancing.

The architecture: **an audio recording is a SOURCE FORM for an existing `public-speech`, not a new
public subtype.** No `audio-speech` subtype, no printed-page provenance, no media binary, no player,
no runtime media fetch. The **exact speech date is NOT established and no year is inferred**. The 12
timestamps are **approximate navigation markers**, never source-authored sections or catalogue units.
Nationalisation is scoped to Kalaignar's underlying Tamil speech and **excludes the source recording,
the recording master, third-party recording production and the project-created English**. The
source-linked validator is **102/102**.

⚠️ **`speeches/kalaivanar-nsk-memorial-day-audio-06/` is a SEPARATE archive** — a different
recording, under active upstream development, and the reason public-speeches `main` keeps moving. It
is **not** a revision of this benchmark, **not** a new pin, and **not** selected for publication.
Never conflate the two.

Full detail, including the durable lessons and the rights boundary, is in `HANDOVER.md`.

*(The previous **2026-08-30** line — `766d6868…`, 25 works, 2948 pages, 2944 sitemap URLs, Cinema
Writing 3, Speeches 13 — is **superseded** and kept only as history, as is the 2026-08-26 line before
it: `15405c7f…`, 24 works, 2853 pages, 2849 sitemap URLs, Cinema Writing 2.)*

Shipped after the Phase-7 narrative below: **Thirukkural — கலைஞர் உரை** (with Daily Kural), the
**Assembly-speech anthology** (Speeches → 13), **Phase B — கிழவன் கனவு** (Fiction → 2),
**Phase C — பராசக்தி** (Cinema Writing → 2), **Phase D — திரும்பிப்பார்**
(Cinema Writing → 3, catalogue → 25), **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs**
(Cinema Writing → 4, catalogue → 26) and **Speech Benchmark #4** (Speeches → 14, catalogue → 27).

**Film Songs:** implementation and publication are **live** — that is why Cinema Writing is 4 — but
its **separate formal control-document close-out is still pending** and was deliberately not
performed by the Speech Benchmark #4 close-out. Treat it as pending housekeeping, **not** as
authorized execution.

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
`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`, now the published provenance authority.

*(Historical note, superseded: the earlier publication-CI failure on `505b1ea7` — run `33246879335` —
was a non-idempotent workflow migration step, not a source-content defect. It is fixed and resolved.)*

## Phase D2 — திரும்பிப்பார் / Tirumbippaar integration — ✅ COMPLETE and CLOSED

**TIRUMBIPPAAR PHASE D COMPLETE** — D1.1 · D1.2 · SOURCE PUBLICATION PACKAGE · D2.1 · D2.2 · D2.3 ·
D2.4 · D2.5 all COMPLETE. *(The not-yet-started note previously here is superseded and removed.)*

Source pin `6a8c59c445890e568dfe65cc36c2900dd2a8a0b3` · implementation `main` after D2.4
`766d68680cecca549d4d752e32561834f7dde0f5` · post-merge Library CI `33292800096` success · GitHub
Production deployment `6163236518` success for that SHA.

PR chain: **#53** D2.1 data · **#54** D2.2 reader/source routes · **#55** D2.3 catalogue ·
**#56** D2.4 sitemap.

Measured at the D2.5 boundary on **2026-08-30** — ⚠️ **site-wide totals since superseded**, see the
CURRENT STATE section above: 25 catalogue works · Cinema Writing 3
(`manohara → parasakthi → tirumbippaar`) · 2944 sitemap URLs with **95** Tirumbippaar (1 landing +
93 registry scenes + 1 source) · 2948 build pages. All 95 production URLs 200; sitemap scene set
equals the registry exactly; off-registry slugs 404. *(The **95 Tirumbippaar URLs** and the route
family are the durable Tirumbippaar facts; the catalogue/sitemap/page totals around them have moved
on.)*

Census at the pin: 104 pages · 93 scenes · 1042 dialogue records · 1330 English units · 39 entities ·
45 labels · 8 song/performance occurrences (3 verified to others, 5 unresolved, **0 Kalaignar**).

**Rights deliberately unset** for the whole publication — composite work, same posture as Parasakthi.
The 1953 `உரிமையுடையது.` notice is printed source evidence only. Credit is role-scoped to the printed
`கதை - வசனம்`.

**Settled, do not reopen:** `ஊஹும்` (5 live) not `ஊஹூம்` (0) · scene 45 `பாண்டியன் : தொழிலாளர்கள்` ·
headings `காட்சி 5[`, `காட்சி 36`, `காட்சி 43].`. Source-visible irregularity is **not** inferred to be
error from expected Tamil or punctuation convention.

**Do NOT reopen Tirumbippaar** absent an explicit new issue or a new source release.

---

## Where the project actually stands (completed — do NOT redo)

- **Phase 1 — Library Foundation:** COMPLETE, merged, production-verified.
- **Phase 2 — Cinema / Manohara:** COMPLETE, merged, production-verified.
- **Phase 3 — Speeches: ACTIVE, NOT complete.** Four benchmarks are done. *(Historical context: I asked at the time for the next work to come from a category **other than speeches**, which produced Phase 4 — Poetry. That pause is **historical and superseded**; Benchmark #4 has since run and closed. No FURTHER speech work is authorized.)*
  - **Benchmark #1 — உதயக் கதிர் / Udhaya Kathir** (assembly speech): COMPLETE, merged, production-verified (PR #18).
  - **Benchmark #2 — பூந்தோட்டம் / Poonthottam** (public speech): COMPLETE, merged, production-verified (PR #20), plus the PR #21 presentation/provenance hotfix.
  - **Benchmark #3 — அறப்போர் / Arappor** (public speech): COMPLETE, merged, production-verified (PR #23).
  - **Benchmark #4 — கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** (public speech, **audio source**): **COMPLETE, merged, production-verified** — A1 PR #62 squash `492b26dd…`, A2 PR #63 squash `56ca0c97…`. Source pin `pugazg/kalaignar-public-speeches @ 1ef73a709a343390befe55dcdfb029427f527bf4`, tree `256cbe2a…`. First audio-sourced speech; `public-speech` retained, audio carried as source form. *(This line replaces the earlier "Speech Benchmark #4: NOT STARTED and NOT SELECTED", which is historical.)*
  - **Speech Benchmark #5: NOT STARTED / NOT SELECTED / NOT AUTHORIZED.**
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
  - **Bulk Onboarding Wave 1 — Drama:** ✅ **COMPLETE, merged, production-verified and CLOSED** — பரதாயணம், அனார்கலி, சாக்ரடீஸ் and சேரன் செங்குட்டுவன், PR #64, squash `0dc92fa0…`, source pin `pugazg/kalaignar-stage-plays @ 145e52e88dbd009286f749a7f0e3520386e63244`. Drama 1 → **5**. *(This line replaces the earlier "Drama Benchmark #2: NOT STARTED / NOT SELECTED — `Anarkali`, `Cheran Senguttuvan` and `Socrates` have no controlling Tamil source", which is **historical**: controlling Tamil sources were released and those works are published. The 2009 published English witness remains **secondary comparison evidence only** and must never be reverse-translated into Tamil — that constraint is unchanged.)*
  - **Any further Drama work / a future Drama batch: NOT STARTED / NOT SELECTED / NOT AUTHORIZED.** **மணிமகுடம் / Manimagudam is NOT published** and is **not** automatically eligible.

**Last production application-code checkpoint at this handover:**

`9aade1d441bb314b5ab62f97b87b373d33db08c5`

That is the Phase-7 Drama Benchmark #1 / PR #29 squash merge, and it identifies the last **production application-code** state. It supersedes `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (Phase 6), `bcb11396b2215bc2cc1e81873c0ce278ef98598a` (Phase 5), `c2d1c46d1c2d4e1f11722360848226208867789f` (Phase 4) and `ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (Phase 3), which are now **historical** checkpoints only. Repository `main` may contain later **documentation-only** commits that do not change deployed application behaviour, and such a docs-only SHA is **never** a newer application-code checkpoint. If live `main` has moved past that SHA, **live state wins** — inspect it and reconcile before advising anything.

⚠️ **SUPERSEDED COUNTS (2026-09-01) — the per-shelf structural facts below still stand, the totals
do not.** The current census is **27 works across 9 non-empty shelves** with **Speeches 14** and
**Cinema Writing 4** (see CURRENT STATE at the top). The paragraph below is the Phase-7-era snapshot,
kept for the per-work structure it records.

`/read` currently publishes **11 works across 9 non-empty shelves** (Life Writing, Letters, **Poetry**, Cinema Writing, Speeches, **Essays & Articles**, Literary Commentary, **Fiction**, **Drama**). **நாடகங்கள் / Drama** holds exactly **1** work (`சிலப்பதிகாரம் நாடகக் காப்பியம்`, 38 scenes plus a separate closing tableau). **புனைவு / Fiction** holds exactly **1** work (`பலிபீடம் நோக்கி`, three sections); **கட்டுரைகள் / Essays & Articles** holds exactly **1** publication (14 articles inside it); **Poetry / கவிதைகள்** holds exactly **1** work; the **single** Speeches / உரைகள் shelf holds exactly **3** — Udhaya Kathir, Poonthottam and Arappor. Verify this live rather than trusting the numbers.

**Do NOT restart:** Phase 1, Phase 2 / Manohara, Speech Benchmarks #1–#3, **Speech Benchmark #4
(கலைவாணர் memorial-day audio speech — CLOSED)**, the PR #21 hotfix, Poetry Benchmark #1 (Idhayathai Thanthidu Anna), Phase-5 Essays Benchmark #1 (Sakkaravarththiyin Thirumagan), Phase-6 Fiction Benchmark #1 (Balipeedam Nokki), Phase-7 Drama Benchmark #1 (Silappathikaram Nataka Kappiyam), or mobile.

## Current poetry source pin

- **இதயத்தைத் தந்திடு அண்ணா:** `pugazg/kalaignar-poems` @ `42c156d7242fa799ea80adbb0c5f2b9eba078fe9`

At that source state, `poems/` contains **exactly one** work directory — `idhayathai-thanthidu-anna` — and the repository README says a *next* poem must begin again from its own startup/source-inspection workflow. **Do not pretend another released Poetry candidate is currently available.** Re-check live source state before advising.

## Current essays source pin

- **சக்கரவர்த்தியின் திருமகன்:** `pugazg/kalaignar-essays` @ `bff35320b668cb5beeaafc5faa58260c4f4473f8`

## Current speech source pins

- **Udhaya Kathir:** `pugazg/kalaignar-assembly-speeches` @ `b1b82402642d8f2cf36927d4752c8e7d28142fdd`
- **Poonthottam:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`
- **Arappor:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`
- **Kalaivanar N. S. Krishnan Memorial-Day Speech:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4` (path `speeches/kalaivanar-nsk-memorial-day`, tree `256cbe2adc8dbc9c245be57196652ed79da48eeb`). Source `main` has advanced well past this pin for the **separate** `kalaivanar-nsk-memorial-day-audio-06` archive; the released work stays pinned here.

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

**You are the reviewer and prompt provider. Claude Code performs every repository write.** You do not
commit and you do not merge — you review, you recommend, and you supply prompts. **Live GitHub state
wins over any SHA, count or status paragraph copied into a handover, including this file.** **Owner
authorization is required before a new benchmark starts**; being eligible for consideration is not
authorization.

Your job is to:

1. inspect live GitHub state;
2. review Claude execution reports independently and sceptically;
3. detect scope drift, duplicate integration, stale state, or source/provenance mistakes;
4. recommend merge / correction / stop;
5. provide complete ready-to-paste Claude prompts when I ask for the next activity;
6. keep the Digital Library handover updated as major milestones complete.

## Immediate next activity

**Bulk Onboarding Wave 1 — Drama is COMPLETE and CLOSED** (PR #64 / `0dc92fa0…`; control close-out
recorded in `HANDOVER.md`), and **Speech Benchmark #4 is CLOSED** (A1 #62 / `492b26dd…`,
A2 #63 / `56ca0c97…`). **No next implementation activity has been started, and no next work, batch or
category has been selected.**

**Bulk onboarding is now the default workflow. Before starting Wave 3, fetch live state and perform a
read-only readiness census for a coherent candidate batch. Eligibility is not authorization. Do not
begin implementation until the owner authorizes the selected Wave 3 batch.**

**Wave 3 is NOT SELECTED, NOT AUTHORIZED and has had no readiness census.** Closing Wave 2 selects
nothing. Do not automatically choose மணிமகுடம் / Manimagudam,
`kalaivanar-nsk-memorial-day-audio-06`, the Film Songs close-out, any speech batch or any poem batch.

Before any new implementation, fetch live state and **obtain owner authorization for the next bounded
activity**. Legitimate possibilities include any still-pending control close-out the owner explicitly
authorizes, or a new candidate readiness/selection activity. **Eligibility is not authorization.**

**Pending housekeeping — not authorized execution:** the **Kalaignar Film Songs formal control
close-out** has not been performed. Its implementation is live (Cinema Writing = 4), but its
control-document close-out section does not exist yet. Mention it if the owner asks what is
outstanding; do not perform it unprompted.

**Do NOT** select `kalaivanar-nsk-memorial-day-audio-06` as the next candidate. It is a **separate
recording and a separate source work**, still under upstream development — not a revision of the
closed Benchmark #4, not a new pin for it, and not established as ready for publication.

**Do not continue Tirumbippaar D2 work.** It is complete and production-verified. **Do not reopen
Speech Benchmark #4.**

Before proposing anything, the next chat must: fetch live control and implementation state, read
`HANDOVER.md` completely, and **confirm owner authorization** for the next roadmap work. Do not select
or begin a work automatically.

**Known roadmap candidates after Tirumbippaar — none selected, none authorized:**

- printed public-speech booklets;
- audio / public speeches — *(the first audio speech has since shipped as Benchmark #4; further audio
  speeches remain candidates, none selected)*;
- the cinema song-lyrics taxonomy decision — *(Film Songs has since shipped; its formal control
  close-out remains pending)*;
- **Mandhiri Kumari — NOT ready**;
- **Anaiyaa Vilakku Anna — NOT ready**;
- blocked stage-play stubs.

**Standing paused / held work — do not fold any of these into the next benchmark automatically:**

- **Validator migration remains PAUSED** after the Manohara migration, unless the owner explicitly
  resumes it.
- **Mobile remains ON HOLD.**
- **Manohara source-drift audit remains separate future work.**
- `ManoharaReader` "Kalaignar's original Tamil text" wording and `StorySource` universal
  scan-storage wording are **separate pre-existing questions**, to be reviewed only if/when those
  components are next touched.
- **Tirumbippaar internal catalogue comment** in `data/library.ts` says song/performance material
  "is not his" while five occurrences are unresolved — strictly, unresolved authorship does not
  establish that those five are someone else's. Safer future wording: *"song/performance material with
  mixed or unresolved authorship — three attributed to others, five unresolved, none attributed to
  Kalaignar."* Reviewed as **NON-BLOCKING**; fold it into a future PR that legitimately edits that
  comment, and do **not** open an implementation change for it on its own.
- A scoped **`WorkAttribution`** rights model for composite works remains a separate future issue.
- **Speech-model comment debt (from Speech Benchmark #4):** the top-level comment in
  `data/speeches.ts` and a nearby `SpeechReader` internal comment still describe the block stream in
  print-only terms ("printed section headings", "source-page boundaries"). Non-runtime, non-public
  explanatory debt. Fold into a future PR that legitimately edits those comments; do **not** open a
  change for it on its own.
- **Film Songs follow-ups:** the nullable section-label type mismatch, and the E3 catalogue-comment
  wording precision — both separate future work.
- **Stale `/read` metadata description** — the page-level description still names only the memoir,
  the letters and the commentary. Separate future work.
- **Film Songs formal control close-out** — still pending; see the Immediate-next-activity note.

- **Poetry Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-5 Essays Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Fiction Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-7 Drama Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Benchmark #2 (a second Fiction work):** NOT STARTED / NOT SELECTED.
- **Poetry Benchmark #2:** NOT STARTED / NOT SELECTED / **NOT APPROVED FOR IMPLEMENTATION** — at live `kalaignar-poems` `2230a8d` a second work `anaiya-vilakku-anna` exists, but `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**.
- **Phase-5 Benchmark #2 (a second Essays work):** NOT STARTED / NOT SELECTED.
- **Speech Benchmark #4:** ✅ **COMPLETE / MERGED / PRODUCTION-VERIFIED** — the first audio-sourced
  speech (A1 #62 `492b26dd…`, A2 #63 `56ca0c97…`). Closed; do not reopen. *(This line previously read
  "NOT STARTED / NOT SELECTED / NOT AUTHORIZED"; that is now historical.)*
- **Speech Benchmark #5:** NOT STARTED / NOT SELECTED / NOT AUTHORIZED. A fifth speech is eligible to
  be compared, but **`kalaivanar-nsk-memorial-day-audio-06` is not selected** and is not established
  as ready.

### Default for "Proceed with next activity"

**Category-neutral, and superseding the older non-speech-only default.** Fetch live control,
implementation and relevant source state, and read `HANDOVER.md` completely. Inspect the currently
recorded roadmap candidates **without excluding a category because of an older historical rule** —
printed public-speech booklets and audio/public speeches are eligible for consideration again, and so
are non-speech categories. Being eligible for consideration is **not** authorization.

**Do NOT implement or select a new benchmark unless the owner has explicitly authorized that roadmap
step.** Do not automatically resume any held or paused stream. If the owner asks for a
recommendation, compare live source-ready candidates and return one recommended category, one
recommended work, why it is the strongest next source-ready/form/provenance benchmark, and a complete
ready-to-paste Claude Code prompt. Do **not** implement it yourself.

At minimum consider live state from repositories such as `pugazg/kalaignar-poems`, `pugazg/kalaignar-essays`, `pugazg/kalaignar-novels`, `pugazg/kalaignar-short-stories`, `pugazg/kalaignar-stage-plays`, `pugazg/kalaignar-cinema-works` and `pugazg/kalaignar-literary-commentary`. **Do not assume every one of them has an eligible work**, and do not preselect from historical planning candidate names.

Judge candidates on released/verified source readiness, released English where bilingual publication is intended, provenance completeness, architectural value as the next Digital Library **form** benchmark, and source authority.

Return:

- the selected **category**;
- the selected **single work**;
- **why** it is the strongest next form/provenance benchmark, from live source state;
- a complete ready-to-paste Claude Code prompt.

**If, by that future date, another source-ready poem has appeared in `kalaignar-poems`, Poetry Benchmark #2 may legitimately compete in this selection — but do not privilege Poetry merely because Benchmark #1 was Poetry.**

*(Superseded: this default previously excluded speech repositories because Phase 3 was paused. After
Tirumbippaar, no category is excluded by that historical rule — speech and non-speech candidates may
be compared when I ask. Nothing about that makes any speech work authorized.)* If I explicitly name a
category, follow that category instead of running broad selection.

Whichever work or batch is selected, the activity must — ⚠️ **the first two bullets are HISTORICAL
(2026-09-01):** bulk onboarding is now the standing default, so "exactly one work" and "no bulk
import" no longer describe it. Everything below them still applies, and applies **per work** inside a
batch:

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
- Stage-play one-act English material for Anarkali / Cheran Senguttuvan / Socrates is a **secondary published-English witness** and must never be mislabelled as canonical Tamil work or reverse-translated. ⚠️ **Updated 2026-09-01:** controlling Tamil sources **have since been supplied** and all three are published by Bulk Onboarding Wave 1 — the "not yet supplied" half of this caution is historical. **The secondary-witness rule itself still stands**, and for **Bharathayanam no 2009 witness exists at all** — that is *not applicable*, not pending.
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

Read the current Digital Library handover completely, inspect the live implementation repository (current `main`, open PRs, production `/read`, and the Drama route family `/plays/socrates`, `/plays/socrates/01`, `/plays/bharathayanam/continuous-play` and a `/source` route), and verify the post-Wave-1 checkpoint above. Then tell me the verified current state.

**Do not resume Tirumbippaar** — Phase D is closed through D2.5.

When I ask for it, inspect the **live source repositories** and perform a read-only readiness census for a **coherent candidate batch** — naming the source release, the shelf, the works that qualify and the works that must be excluded and why — together with a complete ready-to-paste Claude prompt. Bulk onboarding is the default; recommend a single work only where it meets the one-work exception. **Do not select or begin Wave 3 yourself.** Do not implement the work yourself and do not assume a category: speech and non-speech candidates are both eligible for comparison, and none is authorized until I say so. Validator migration stays **PAUSED** and mobile stays **ON HOLD** unless I explicitly resume them.

---
