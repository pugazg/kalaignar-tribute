# Kalaignar Digital Library / Reading Room — Master Handover

**Last updated:** 2026-08-18

> **Status:** **Phase 3 — Speeches is ACTIVE** (first benchmark speech — Udhaya Kathir — in
> reviewer-gated PR #18, **not merged**), building on the **COMPLETE** Phase 1 foundation and
> **COMPLETE** Phase 2 (Cinema / Manohara, merged + live in production, verified 2026-08-18).
> `/read` is the Kalaignar Digital Library landing; on `main` it shows four works across four
> shelves (Life Writing, Letters, Cinema Writing, Literary Commentary), and PR #18 adds a fifth
> (Speeches). See **§10 → Phase 3** for the active record and **§10 → Phase 2** for the completion
> record. Mobile remains **ON HOLD** (Activity 6 / PR #15 merged for preservation — see §4).

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

At the time of this handover, the public Reading Room presents three peer collections:

1. **நெஞ்சுக்கு நீதி / Nenjukku Neethi**
   - 6 volumes
   - 391 chapters
2. **முரசொலி கடிதங்கள் / Murasoli Letters**
   - current structured archive covers letters from the 2013–2016 period represented by volumes 48–54
   - 346 curated letters in the current implementation data
3. **தொல்காப்பியப் பூங்கா / Tholkappiya Poonga**

The current `/read` page is still structurally memoir-centric:

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

- **பலிபீடம் நோக்கி**
- Tamil 34/34 verified
- assembled Tamil passed
- English verified
- repository status: archival package **RELEASE-READY**

Important structural rule: `ராயசம் வெங்கண்ணு` is an embedded sequence inside the same work, not a separate novel/work.

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

## Phase 3 — Speeches — 🚧 ACTIVE (first benchmark in review)

**Implementation has begun** from the post-mobile-merge `main`
(`36d1325e9dc04084ed84cb50a2d0c3f6a665b795`). The first benchmark speech is integrated and open
for review; **it is not merged, and Phase 3 is not complete.**

- **Phase-3 branch:** `digital-library/phase-3-speeches`
- **Phase-3 PR:** #18 — _Digital Library Phase 3 — Speeches: Udhaya Kathir_ (**open, reviewer-gated,
  not merged**)
- **Implementation-repo Phase-3 handover:** `docs/digital-library/PHASE3_SPEECHES_HANDOVER.md`
- **First benchmark:** `udhaya-kathir` — உதயக் கதிர் / Udhaya Kathir (Tamil Nadu Legislative
  Assembly, 1970-09-09; reply to the no-confidence-motion debate). Chosen on **source readiness** as
  the strongest fully-released assembly speech (standalone 1970 booklet `TVA_BOK_0065650`; verified
  Tamil + verified faithful English; 29 printed section headings; speech pp. 5–46).
- **Source (pinned, unmodified):** `pugazg/kalaignar-assembly-speeches`
  @ `b1b82402642d8f2cf36927d4752c8e7d28142fdd`. Both speech repos were inspected
  (`kalaignar-assembly-speeches` @ `b1b8240`, `kalaignar-public-speeches` @ `c8abf95`); both hold
  fully-released verified works. Deterministic importer, fail-closed on source-HEAD mismatch.
- **Public model:** the single **Speeches** shelf (`உரைகள்`); `assembly` / `public` are **subtypes**
  (`subtype: "assembly-speech"` / `"public-speech"`), **not** separate public shelves. Routes are
  flat `/speeches/<slug>` (+ `/source`); repository names are not exposed as route taxonomy. New
  `readerStructure: "speech"` reader (long-form prose with printed headings — not scene
  segmentation); source provenance preserved in the vendored data; nationalisation rights model
  reused (GO number/issue date still unverified).
- **Done in this activity:** readiness inventory across both repos; benchmark selected; Phase-3
  data/reader/importer architecture; ONE benchmark integrated + published on the Speeches shelf; its
  source/provenance page; validation; PR opened. **Not done (deliberate):** any second speech, bulk
  assembly/public import, a `/speeches` collection landing, Essays/Fiction/Poetry, another cinema
  work, mobile features, a generalized ingestion framework, or the project-wide existing-works rights
  audit.

**Remaining Phase-3 direction** — integrate additional released speeches one at a time under the
same **Speeches** shelf (both Legislative Assembly and Public speeches are subtypes of it, not
separate shelves), reusing this reader/importer pattern. Prefer machine-readable indexes where
present, but verify every reader-facing work against source-repository release state.

Do not collapse public speeches and Assembly proceedings into one reader model if that loses parliamentary structure.

## Phase 4 — Essays + Fiction + Poetry

Integrate one released work per activity:

- Essays: Sakkaravarththiyin Thirumagan
- Novels: Balipeedam Nokki
- Short Stories: Kizhavan Kanavu
- Poetry: Idhayathai Thanthidu Anna

After one work of each form is proven, extract reusable adapters rather than prematurely inventing abstraction.

## Phase 5 — Stage Plays + broader Literary Commentary

- Silappathikaram — Nadaga Kappiyam
- further literary commentary only when source work has reached its publication gate
- Thirukkural commentary waits for an explicit complete/partial-publication decision based on live archival state

## Phase 6 — Cross-library discovery

Only after several shelves contain real public works:

- global search across published library units;
- filters by shelf/form/language/date where source metadata supports them;
- recently added;
- continue reading across work types;
- unified bookmarks/shelf if desired;
- citation/provenance affordances.

Do not label the existing memoir-only full-text search as a global library search.

## Phase 7 — ingestion automation

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

The next Claude implementation prompt should be:

**Digital Library Phase 1 — Library Foundation / `/read` reorganization and catalog architecture.**

It should **not** integrate all nine repositories yet.

Mandatory Phase-1 principles:

- preserve current three public collections and working URLs;
- preserve memoir reader/search behavior, but move memoir-specific UI out of the global library identity;
- create catalog-driven shelves/work cards;
- build the nine-shelf taxonomy in data/model form;
- hide empty shelves by default;
- recognize that accidental Manohara files exist under the website repository but **do not use, extend, validate, normalize or derive from them**;
- do not integrate Manohara or any other new source work during Phase 1;
- no mobile changes;
- no source text changes;
- no source PDFs;
- no mass import;
- stop with a green PR and a Phase-2 handover.

After Phase 1 is merged and deployed, **Phase 2 begins with Cinema / Manohara imported afresh from the authoritative `pugazg/kalaignar-cinema-works` release/reader-export artifacts. The accidental website-repository Manohara parts are not a continuation boundary and must not be used.**
