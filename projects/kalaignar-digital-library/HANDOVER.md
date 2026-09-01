# Kalaignar Digital Library / Reading Room — Master Handover

**Last updated:** 2026-09-01

---

## ⚠️ CURRENT STATE — read this before anything below

**The Phase 1–9 narrative in this document stops at Phase 7 (2026-08-21) and is now HISTORICAL.**
Several phases have shipped since it was written, and its work counts, shelf counts and
"last production application-code checkpoint" are stale. It is kept as history and has **not** been
retro-edited. Where it disagrees with this section or with live GitHub, **live GitHub wins**.

### Verified live state — 2026-09-01 ✅ CURRENT

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

**Measured now**, not copied from the previous checkpoint: the SHA and open-PR count from live
GitHub; the work/shelf census from `data/library.ts` at that SHA; the page count from a production
build of it; and the sitemap count from the deployed site. `https://nenjukkuneethi.org/read`,
`/speeches/kalaivanar-nsk-memorial-day` and `/speeches/kalaivanar-nsk-memorial-day/source` all
return 200 in production.

Shipped since the 2026-08-30 checkpoint:

- **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs** — implementation and publication are **live**
  in Cinema Writing, which is why that shelf is now 4 rather than 3. Its **separate formal
  control-document close-out remains pending** and is deliberately not performed here.
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
  and the catalogue to 26. Implementation live; **formal control close-out still pending**.
- **Speech Benchmark #4 — the first audio-sourced speech**, taking Speeches to 14 and the catalogue
  to 27. **Closed by this document.**

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
10. **Film Songs formal control close-out — still pending.**

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

> ⚠️ **SUPERSEDED (2026-09-01) — kept as the status snapshot it was.** Two lines below are no longer
> current: **Phase 3 is ACTIVE, not paused** (the owner-directed pause was lifted), and **Speech
> Benchmark #4 is COMPLETE and CLOSED**, not "NOT STARTED and NOT SELECTED". See the CURRENT STATE
> checkpoint and the Speech Benchmark #4 close-out near the top of this document. Everything else in
> this snapshot stands as written.
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
>   `Socrates` have **no controlling Tamil source** and remain blocked.
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

**Phase 3 is ACTIVE and NOT complete.** Three benchmarks are done — one assembly speech and two
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

When it is reactivated, the guidance stands: integrate additional released speeches one at a time
under the same **Speeches** shelf (both Legislative Assembly and Public speeches are subtypes of it,
not separate shelves), reusing this reader/importer pattern. Prefer machine-readable indexes where
present, but verify every reader-facing work against source-repository release state.

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
at live `main` `2230a8d` it holds a **second**, `poems/anaiya-vilakku-anna`. `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**.
At the pinned state,
and the repository README states that a *next* poem must begin again from its own
startup/source-inspection workflow. Poetry remains an **open** Digital Library form; it is neither
complete nor cancelled.

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

## Phase 7 — Drama / Stage Plays — 🚧 ACTIVE (benchmark 1 COMPLETE / MERGED / PRODUCTION-VERIFIED)

**Read this qualifier before quoting the status.** Benchmark #1 is complete, merged and
production-verified. The PHASE remains **ACTIVE**: Drama Benchmark #2 is NOT STARTED and NOT
SELECTED, and the remaining stage plays have no controlling Tamil source.

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

**Drama Benchmark #2: NOT STARTED and NOT SELECTED.** `Anarkali`, `Cheran Senguttuvan` and
`Socrates` remain registry stubs with **no controlling Tamil source**; only a published English
secondary witness exists for them, and it must never be reverse-translated into canonical Tamil.

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

> ⚠️ **SUPERSEDED IN PART (2026-09-01).** The paragraph below was written at the Drama Benchmark #1
> synchronization. Two of its statements are no longer current: **Phase 3 is ACTIVE, not paused**,
> and **Speech Benchmark #4 is COMPLETE and CLOSED** rather than not started. The current
> immediate-next-activity position is: **Speech Benchmark #4 is closed; no next benchmark is started,
> selected or authorized; the Kalaignar Film Songs formal control close-out remains pending
> housekeeping; and `kalaivanar-nsk-memorial-day-audio-06` is a SEPARATE source archive that is NOT
> selected.** Owner authorization is required before any new implementation.

**Phase 1 and Phase 2 are COMPLETE. Phase-3 Speech Benchmarks #1–#3 are complete, merged and
production-verified, and Phase 3 is PAUSED by owner direction. Phase-4 Poetry Benchmark #1,
Phase-5 Essays & Articles Benchmark #1, Phase-6 Fiction Benchmark #1 and Phase-7 Drama Benchmark #1
are complete, merged and production-verified. Do NOT start any completed phase or benchmark again.**
_(This section once instructed a fresh chat to begin Phase 1, and later Phase-3 Benchmark #4
candidate selection. Both are stale and superseded; the Phase-1 principles are preserved as history
in §10 → Phase 1, and the paused Phase-3 guidance in §10 → Phase 3.)_

**Phase-7 Drama Benchmark #1 (சிலப்பதிகாரம் நாடகக் காப்பியம்) is merged and production-verified, and
this documentation synchronization records it. No next implementation benchmark has been started, and
no next candidate or category has been selected.**

Current standing state:

- **Speech Benchmark #4:** ⚠️ **SUPERSEDED** — previously "NOT STARTED / NOT SELECTED / **PAUSED** by
  owner direction". Now **COMPLETE / MERGED / PRODUCTION-VERIFIED and CLOSED**: the first
  audio-sourced speech, A1 PR #62 squash `492b26ddd5681f085726ac802681c3fcbc7162f0`, A2 PR #63 squash
  `56ca0c978e34afddde52595f2ce825872bd6aeef`.
- **Speech Benchmark #5:** NOT STARTED / NOT SELECTED / NOT AUTHORIZED.
- **Poetry Benchmark #2:** NOT STARTED / NOT SELECTED / **NOT APPROVED FOR IMPLEMENTATION** — a
  second work now exists at live `kalaignar-poems` `2230a8d`, but `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**.
- **Phase-5 Benchmark #2 (a second Essays work):** NOT STARTED / NOT SELECTED.
- **Phase-6 Benchmark #2 (a second Fiction work):** NOT STARTED / NOT SELECTED. Fiction shipping its
  first benchmark does **not** privilege Fiction in the next selection.
- **Phase-7 Drama Benchmark #1 (சிலப்பதிகாரம் நாடகக் காப்பியம்):** **COMPLETE / MERGED /
  PRODUCTION-VERIFIED** — PR [#29](https://github.com/pugazg/kalaignar-autobiography/pull/29),
  squash `9aade1d441bb314b5ab62f97b87b373d33db08c5`, production-verified 2026-08-21.
- **Phase-7 Drama Benchmark #2:** NOT STARTED / NOT SELECTED — `Anarkali`, `Cheran Senguttuvan` and
  `Socrates` have no controlling Tamil source.

If the owner simply says **"Proceed with next activity"**, the reviewer performs:

**NEXT NON-SPEECH CATEGORY CANDIDATE SELECTION.**

**No next work or category has been selected.** In particular, **Poetry Benchmark #2 is NOT the
automatic default**: at live `pugazg/kalaignar-poems` `2230a8d` a second work directory
(`poems/anaiya-vilakku-anna`) now exists, but `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**. Poetry Benchmark #2 therefore cannot be
selected today.

The reviewer must inspect **live** source readiness across the relevant **non-speech** repositories
and recommend **exactly ONE** next work. At minimum consider live state from repositories such as:

- `pugazg/kalaignar-poems`
- `pugazg/kalaignar-essays`
- `pugazg/kalaignar-novels`
- `pugazg/kalaignar-short-stories`
- `pugazg/kalaignar-stage-plays`
- `pugazg/kalaignar-cinema-works`
- `pugazg/kalaignar-literary-commentary`

**Do not assume every repository above has an eligible work.** Inspect live source/release state, and
**do not preselect from historical planning candidate names** anywhere in this handover.

Select the single strongest next benchmark on:

- released/verified source readiness;
- released English where bilingual publication is intended;
- provenance completeness;
- architectural value as the next Digital Library **form** benchmark;
- source authority.

**Speech repositories are excluded from the default selection** because Phase 3 is paused by owner
direction. If the owner explicitly asks to resume speeches, that overrides the pause. If the owner
explicitly names a non-speech category, follow that category instead of running broad selection. If by
then another source-ready poem has appeared in `kalaignar-poems`, Poetry Benchmark #2 may legitimately
compete in this selection — but **Poetry is not privileged merely because Benchmark #1 was Poetry**.

Constraints for whichever work is selected:

- integrate **exactly one** work;
- reviewer-gated PR; **no bulk import**, no mass ingestion;
- deterministic, **commit-pinned** importer that **fails closed** on a source-HEAD mismatch;
- build **no** generalized ingestion framework, and add no collection landing without separate
  justification and approval;
- preserve a form-specific reader model **only where that work's source actually supports it** — **do
  not assume** இதயத்தைத் தந்திடு அண்ணா's unresolved cross-page pattern generalizes;
- unresolved source facts stay **unresolved** — no punctuation, indentation, semantic or grammatical
  inference;
- absent source metadata is represented honestly and never fabricated;
- **no** source-archive edits, **no** PDF vendoring, **no** runtime GitHub;
- **no** mobile work (mobile remains ON HOLD);
- **stop after that one benchmark.**

Last production application-code checkpoint at this handover:
**`9aade1d441bb314b5ab62f97b87b373d33db08c5`** (the Phase-7 Drama Benchmark #1 / PR #29 squash merge) — live GitHub `main` is authoritative and overrides this SHA if it later moves;
documentation-only commits may advance `main` past it without changing the deployed application, and
such a docs-only SHA must never be recorded as a newer application-code checkpoint. The earlier
`992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (Phase 6), `bcb11396b2215bc2cc1e81873c0ce278ef98598a`
(Phase 5), `c2d1c46d1c2d4e1f11722360848226208867789f` (Phase 4) and
`ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (Phase 3) are **historical** checkpoints only.

Current novels source pin: `pugazg/kalaignar-novels` `9e80c567d4a2165178c5374a02210240140685bf`.
