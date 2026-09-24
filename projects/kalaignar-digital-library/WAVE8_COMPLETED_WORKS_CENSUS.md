# Wave 8 P0 — Owner-Selected Scope & Digital-Library Readiness

**WAVE 8 P0 — COMPLETE / REVIEW-READY, NOT YET FROZEN BY MERGE.**
**WAVE 8 P1 — NOT STARTED / NOT AUTHORIZED.**

**Created:** 2026-09-24 · **Control documentation only.** Implementation delta = **0**, source delta = **0**,
production delta = **0**. Live GitHub is authoritative; every SHA, tree and count below was fetched or
re-derived live for this record.

> **Accounting rule — read first.** Wave 8 has **8 source publication inputs** but only **2 new canonical
> LibraryWorks**. Six of the inputs are **volume-level expansions of 1 existing LibraryWork**
> (`murasoli-letters`). Wave 8 must **never** be summarized as "8 new works".

Wave 6 and Wave 7 remain **COMPLETE / CLOSED / FROZEN at P5**; neither is reopened by this record.

---

## 1. Authoritative accepted baseline (Wave 7 closed)

| Repo | main | tree |
|---|---|---|
| control `pugazg/kalaignar-tribute` | `732213dcb868d66e57ce01c2739b293bb3d25f6b` | `4ffcb8e71c374b21d48d911d1b73d372276ed4be` |
| implementation `pugazg/kalaignar-autobiography` | `cf769d06c1bdb4abc58b5ef2c26e609a777b4923` | `35d64fb97f7bed1e26c3bb09fea5649db9d1e348` |

Open PRs at P0: control **0**, implementation **0**, and **0** in each of the three Wave-8 source repositories.
No drift from the owner prompt's witnessed SHAs was found.

Accepted public baseline (from [`WAVE7_P5_PRODUCTION_ACCEPTANCE.md`](./WAVE7_P5_PRODUCTION_ACCEPTANCE.md), re-checked
on live `main`): catalogue **333** — Life Writing 1 · Letters 1 · Poetry 14 · Cinema Writing 10 · Drama 10 ·
Fiction 162 · Essays & Articles 15 · Speeches 117 · Literary Commentary 3; collections **9**; `/read` 96 / 41;
production sitemap **4779** (re-fetched: 4779 unique).

## 2. Owner authorization and fixed scope

The owner authorized **Wave 8 at P0 only**, with an owner-selected, closed scope of exactly three segments:

| Segment | Source repository | Path(s) |
|---|---|---|
| B1 — Murasoli Letters expansion | `pugazg/kalaignar-murasoli-letters` | `volumes/volume-42/` … `volumes/volume-47/` |
| B2 — Drama / ஒரே முத்தம் | `pugazg/kalaignar-stage-plays` | `works/ore-mutham/` |
| B3 — Literary Commentary / சங்கத் தமிழ் | `pugazg/kalaignar-literary-commentary` | `works/sangatamil/` |

P0 authorizes **no** implementation, payload, catalogue, discovery, route, sitemap, reader, source or production
change.

## 3. Live source pins (frozen at P0)

| Source repository | live `main` (pinned) | repo tree |
|---|---|---|
| `pugazg/kalaignar-murasoli-letters` | `bd0bb7904c85bdbfe05aa4970ac098d701a6967f` | `ff604c584ab05d0d769abe4a0c685b79a7a79e5b` |
| `pugazg/kalaignar-stage-plays` | `521fe5452e3e9ed54baa81e672325ce6ba501c5e` | `cea50efb13baf27390b794b39b76b039a9ccaead` |
| `pugazg/kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` | `2302d1fc6cbe9386a8010b344a9caba2f4913fa4` |

Per-input subtree pins (the import boundary; a later source commit that leaves these trees unchanged is **not**
drift and must not trigger an arbitrary repin):

| Input | Path | Tree | Tamil subtree | English subtree |
|---|---|---|---|---|
| Murasoli Vol 42 | `volumes/volume-42` | `0bb4cfe677badd63fb0fbf5b66ea0fae9897339d` | `chapters` `c6d327db39aa36edf2e4e152d691a32658a99e14` | `translations/en` `5b860ecdac07a452e552f9ffcffe97e7ce39fc58` |
| Murasoli Vol 43 | `volumes/volume-43` | `35162a6263ed7e9eb7aba872008f86d1d185ee2c` | `chapters` `29cf8f47c3e3fd225893dcbbe5676789e481abb7` | `translations/en` `699448f7b14ecee4e71654a720ba2e832b7db1ae` |
| Murasoli Vol 44 | `volumes/volume-44` | `b9142e10a44df2e58d365066de098ffa4a9c351d` | `chapters` `41292fadf352278577c1f6d29da71ca40c55c10d` | `translations/en` `9c4ab4f0c95e7ca06d18381a2991fb7735e8520d` |
| Murasoli Vol 45 | `volumes/volume-45` | `9efc967a226b519888fa3cf9af4eca6b8c70a5c7` | `chapters` `91b48c0bd772ad20d1ce1d5c974527232eec235a` | `translations/en` `7fbfae929696e1e2678eaf17d63dba087b5377d9` |
| Murasoli Vol 46 | `volumes/volume-46` | `f111d393681b384aed7c288353a16931ca083fb0` | `chapters` `9df82ac77011835c99d8fb7b84f104d9c1b0334d` | `translations/en` `fed573e35a6d30f78d8d08011df780ed35f7529b` |
| Murasoli Vol 47 | `volumes/volume-47` | `71998ba7bcc3aa0d800a44bcd89d9d61c09c7a7f` | `chapters` `278d3c53c54afd8014ec8cf57f4d3938ba2d2ab6` | `translations/en` `844d5d03aa28b4cec97b831b8b99259b1498ec07` |
| ஒரே முத்தம் | `works/ore-mutham` | `0839c6efc7bfd41fd11d30db3a46b0a2b3c901e6` | `scenes` `7b751021c53b7d7fcb4aecdad3416b3cd92e8688` | `translations/en` `4fca6de80a4163619cb77c09357d7f44f227979d` |
| சங்கத் தமிழ் | `works/sangatamil` | `25231d62c62e22228a248fd2976e0ee9c43939c1` | `pages` `fa1f5b8e239bd3f3cba57de771ed6959088fec2c` | `translations/en` `87e3e497764691425f13227fa90cd150da769894` |

Controlling sources (as recorded by each archive; PDFs are not committed to any source repository):

| Input | Controlling file | SHA-256 (as recorded) | Physical extent | Canonical manifest / release authority |
|---|---|---|---|---|
| Vol 42 | `TVA_BOK_0065826_கலைஞரின்_கடிதங்கள்_தொகுதி_42.pdf` | `43f9b51fd3765144f707cce535cc9ed39892f911a126c3c3c005173a1efc1676` | 402 PDF pp. (400 printed) | `metadata.yml`; `translations/en/RELEASE_REPORT.md` |
| Vol 43 | `TVA_BOK_0065828_கலைஞரின்_கடிதங்கள்_தொகுதி_43.pdf` | `53607130844a56b7b65b7dc5451031a33690c867e81c5ffab6e9b70958fdaf35` | 402 PDF pp. | `metadata.yml`; `translations/en/RELEASE_REPORT.md` |
| Vol 44 | `TVA_BOK_0065830_கலைஞரின்_கடிதங்கள்_தொகுதி_44.pdf` | `573d65d7b7d3a8e3cc158b7f91af3a9382ac90ea1eaa37e8c0022b5a64dc747d` | 400 PDF pp. | `metadata.yml`; `translations/en/RELEASE_REPORT.md` |
| Vol 45 | `TVA_BOK_0065831_கலைஞரின்_கடிதங்கள்_தொகுதி_45.pdf` | **not recorded by the archive** (see §8) | 402 PDF pp. | `metadata.yml` (nested schema); `README.md`; `translations/en/RELEASE_REPORT.md` |
| Vol 46 | `Vol46.pdf` | `ff88d5a78a5ef4d96888ec2f5a0a3653a4f34b1bfbcb0317b5191242cc72cff9` | 402 PDF pp. | `metadata.yml`; `translations/en/RELEASE_REPORT.md` |
| Vol 47 | `Vol47.pdf` | `4c151357a822a8855e553de080b311d35934e9d844c81aff168b811cd8fd8558` | 401 PDF pp. | `metadata.yml`; `README.md`; `translations/en/FINAL_RELEASE_REPORT.md` |
| ஒரே முத்தம் | `TVA_BOK_0064325_ஒரே_முத்தம்.pdf` | `60780e340e6b0c6d6f3956af8beeb69692fab3f20e843c6ed4275b9962aae220` | 131 scans (224,884,964 bytes) | `README.md`; `TERMINAL_SOURCE_CONDITION_HOLDS.md`; `TAMIL_CLOSURE_REVIEW.md`; `translations/en/TRANSLATION_REVIEW.md` |
| சங்கத் தமிழ் | `TVA_BOK_0042551_சங்கத்_தமிழ்.pdf` | `b58517d046eb68010c3c0cfcc5e2702a080a1f1856a56c445fb6fc43480f83ed` (imported-byte, `metadata/source.md`) | 497 scans | `README.md` + `GATE_I_FINAL_CLOSURE.md` (2026-09-20 current checkpoint); `translations/en/reviews/WHOLE_VOLUME_ENGLISH_RELEASE_REPORT.md` |

## 4. Source readiness evidence (re-derived from the pinned trees)

### B1 — Murasoli Volumes 42–47

Counted independently from `chapters/*.md` (Tamil records) and `translations/en/letters/*.md` (English records):

| Vol | Tamil records | Printed number span | Date span | English records | Tamil gates | English | Source-incomplete |
|---:|---:|---|---|---:|---|---|---|
| 42 | **64** | 3364–3376, **3154**, 3378–3427 | 2009-01-31 → 2009-10-30 | 64 | structural audit PASS; 2nd visual/textual-fidelity PASS 402/402 | final release PASS 64/64 | 0 |
| 43 | **56** | 3428–3483 | 2009-11-01 → 2010-07-17 | 56 | structural PASS; 2nd visual PASS 402/402 | final release PASS 56/56 | 0 |
| 44 | **53** | 3484–3536 | 2010-07-18 → 2011-03-11 | 53 | structural PASS; 2nd visual PASS 400/400 | final release PASS 53/53 | 0 |
| 45 | **55** | 3537–3591 | 2011-03-12 → 2011-09-27 (first/last letters) | 55 | structural PASS; 2nd visual PASS 402/402 | final release PASS 55/55 | 0 |
| 46 | **55** | 3592–3649 with gaps (see §8) | 2011-10-05 → 2012-08-15 | 55 | full-volume audit complete; 2nd visual complete 1–402 | released 55/55 | 0 |
| 47 | **59** | 3647–3705 | 2012-08-19 → 2013-02-19 | 59 | full-volume audit complete; 2nd visual complete 1–401 | release-ready-with-source-exception 59/59 | **1 — Letter 3681** |
| **Total** | **342** | | | **342** | | | **1** |

`64 + 56 + 53 + 55 + 55 + 59 = 342` new source records, matching the owner prompt.

### B2 — ஒரே முத்தம்

- Archive status (README): **COMPLETE / VERIFIED / CLOSED**.
- **131 / 131** page records carry `status: verified` (each page record read directly); terminal `blocked` **0 / 131**;
  ordinary `needs-review` **0**. `TERMINAL_SOURCE_CONDITION_HOLDS.md`: *"CLOSED — 0 CURRENT-SOURCE-CONDITION HOLDS;
  131 / 131 SCANS VERIFIED"*; it is retained only as a historical ledger. The final 13 formerly-held scans
  (72–74, 77, 79, 88, 90, 94–95, 98–100, 112) were closed on 2026-09-19 against the page images, using a
  user-supplied transcription **only as a word-level cross-witness** (punctuation/structure source-controlled).
- Scenes: `scenes/main-01` … `main-30` (**30**) + `scenes/nagai-suvai-01` … `-03` (**3**) = **33**; main play scans
  8–118 / pp. 6–116; separate `நகைச் சுவைப் பகுதி.` scans 119–130 / pp. 117–128, **source-numbered காட்சி 1–3**;
  scan 131 = back-cover advertisement.
- Tamil closure review: PASS. English: 33 / 33 scene files; `BATCH_01`–`BATCH_07` **PASS / LOCKED**; final
  `TRANSLATION_REVIEW.md` **PASS / COMPLETE — 33 / 33 reviewed; 0 Tamil source holds remain**.
- Identity: `ore-mutham` · ஒரே முத்தம் · கலைஞர் மு. கருணாநிதி · தென்றல் நூற்பதிப்புக் கழகம் · ஐந்தாம் பதிப்பு, 1964.

### B3 — சங்கத் தமிழ்

- Current authoritative checkpoint (2026-09-20, supersedes the 2026-09-16 Gate-I status table and pre-WFV
  "not word-for-word verified" wording in section READMEs): Gates A–I complete; fresh physical-source WFV
  **497 / 497**; WFV-001 REJECTED (canonical retained); **WFV-002…WFV-056 = 55 / 55 user-adjudicated / closed**;
  pending WFV rows 0.
- Tamil, from the 497 page records read directly: **496 `verified` + 1 `partial` (scan 8,
  `0008-munnurai-handwritten-facsimile.md`)**; 0 needs-review; 0 blocked. Visual fidelity: 496 verified + 1
  needs-review (the same scan 8).
- Maintained English, from the 497 English page records read directly: **496 `release-ready` + 1
  `source-limited` (scan 8)**; 0 blocked; whole-volume English release **PASS / APPROVED / CLOSED**; canonical
  Tamil changes from English work 0.
- Archive states: *"None required. Sangatamil Tamil WFV and maintained-English release are COMPLETE / CLOSED."*

## 5. Digital-Library de-duplication check (live implementation `cf769d06…` + production)

- `ore-mutham`: absent from `data/`, `app/`, `lib/`, `components/`, `public/data/plays/`, the production sitemap;
  `/plays/ore-mutham` and `/plays/ore-mutham/source` → **404**.
- `sangatamil`: absent from the same locations and the sitemap; `/sangatamil`, `/sangath-tamil`,
  `/literary-commentary/sangatamil` → **404**. (Sitemap substring hits for "sanga" are unrelated speech/poem/essay
  slugs; `tp-m42…m47` hits are Tholkappiya Poonga units.)
- Murasoli: the website carries **Volumes 48–54 only** — `public/data/murasoli/index.json` `volumeCount 7`
  (48–54); `letters-index.json` **346** letters (48: 58 · 49: 53 · 50: 50 · 51: 49 · 52: 50 · 53: 50 · 54: 36),
  346 unique ids; production sitemap `/murasoli/*` = **687** (letters of 48–53 + Vol 54's 36 letters and 341 page
  routes). No `m42`–`m47` id exists; `/murasoli/m42-l3364`, `/murasoli/m47-l3681` → **404**.
- No Wave-8 identity duplicates an existing LibraryWork; Volumes 42–47 are not integrated under any other path.

## 6. Existing-work vs new-work identity decision

| Input | Identity decision | Catalogue effect |
|---|---|---|
| Murasoli Vols 42–47 | **Coverage expansion of the existing LibraryWork `murasoli-letters`** (shelf Letters, `readerStructure: "letter"`, href `/murasoli`) | **0** — no new card, no Letters-shelf increment |
| `ore-mutham` | **One new canonical LibraryWork** (Drama) | **+1** |
| `sangatamil` | **One new canonical LibraryWork** (Literary Commentary) | **+1** |

Murasoli remains exactly **one** LibraryWork. Wave 8 does not redesign its canonical identity. No new
LibraryCollection is implied by this scope.

## 7. Murasoli volume-coverage delta

- Live today: Volumes **48–54** (7 volumes, 346 letters; Vol 48 begins at Letter 3706).
- Wave-8 source adds Volumes **42–47** (342 records; Vol 47 ends at Letter 3705) — **contiguous** with Vol 48.
- If later published: Volumes **42–54 = 13 volumes**, **688** letter records (346 + 342), subject to every
  source-specific qualification in §8.

## 8. Qualification and source-condition records

**Murasoli Vol 47 — READY WITH QUALIFICATION.** Letter **3681** («இருள் தொலைந்திட வா! விரைந்து வா! வா!», dated
15-12-2012 from the printed contents) is **source-incomplete**: PDF 249–252 / printed 248–251 survive; printed page
**252 is absent from the only source PDF**; `status: source-incomplete`, `missing_printed_pages: [252]`, signature
"மூல PDF-இல் கிடைக்கவில்லை". The archive's final English release report records it as the *sole source-incomplete
record* and states the missing continuation, closing and date are **not reconstructed**. Every later Wave-8 layer
must carry this transparently on the public provenance/source surface; nothing may be inferred or filled.

**Murasoli source-numbering anomalies (preserved, not errors to correct):**
- Vol 42: contents and PDF 092 heading both print **3154** between 3376 and 3378; **no Letter 3377 exists** —
  never invent it.
- Vol 46: **two distinct letters are both printed 3637** — «“இன்றே செல்க! இனிதே வெல்க!” என வாழ்த்தி வழியனுப்புகிறேன்!»
  (3-7-2012, from PDF 336) and «என் உயிரினுமேலான அன்பு உடன்பிறப்புக்களே!» (05-07-2012, from PDF 343); **no 3636**;
  **no 3644–3646**.
- Vol 46 / Vol 47: printed numbers **3647–3649 occur in both volumes as different letters** (Vol 46: 02/05/15-8-2012;
  Vol 47: 19/25/30-8-2012).
- Consequence for P1: a letter's printed number is **not** a unique identity. The live id scheme
  `m{volume}-l{number}` handles the cross-volume overlap but **collides on Vol 46's duplicate 3637**; P1 must adopt a
  source-faithful disambiguation (e.g. the source's own file stem) without renumbering anything.

**Murasoli Vol 45 source identity.** The archive records filename + 402 PDF pages but **no controlling-scan
SHA-256**. P1 must record the hash only if it is established from the archive; otherwise identity is carried as
filename + extent, never an invented hash. (Vols 46–47 use the archive's `Vol46.pdf` / `Vol47.pdf` filenames with
recorded SHA-256s.)

**ஒரே முத்தம்.** No qualification: 0 blocked / 0 needs-review. The former Wave-7 `HOLD / OWNER_DECISION` (28
terminal holds at P0 of Wave 7) is **historical and superseded** by the live closed source state. Structural rule:
the separate `நகைச் சுவைப் பகுதி.` scenes stay source-numbered **1–3**, never main scenes 31–33.

**சங்கத் தமிழ் — READY WITH QUALIFICATION.** Scan **8** (the handwritten `முன்னுரை` facsimile) is a **permanent
source-limited partial**, description-only by explicit user direction — Tamil `partial`, English `source-limited`.
It is a source condition, not pending work. Never invent or reconstruct its text, never promote it to verified,
never describe the work as 497/497 textually complete without this qualification.

## 9. Reader / publication-model assessment (recorded; decisions finalize in P1)

**B1 Murasoli (existing `letter` reader).** Live `/murasoli` + `/murasoli/[id]` (letters and Vol 54 page ids),
data-driven from `index.json` / `letters-index.json` (+ `letters/`, `letters-en/`, `text/`); the sitemap enumerates
letter ids and Vol 54 page ids. The live data already mixes two payload shapes (Vols 48–53 letter pages as printed
numbers; Vol 54 page ids). The implementation has **no Murasoli importer, validator, `provenance.json` or `/source`
page**, and its catalogue comments assert "only volumes 48–54". The Wave-8 source is a newer archival format with
**two header dialects** (YAML front matter in Vols 42, 43, 46, 47; Markdown bullet headers in Vols 44–45) and
per-volume English layouts. **P1 needs a new source-pinned import/translation adapter** (per-volume provenance,
qualification carriage, id disambiguation, data-derived volume/letter statistics) — not a reuse of the older
payload assumptions. Tamil/English coverage flags must be re-derived from data, not hand-edited.

**B2 ஒரே முத்தம் (existing `stage-play` reader).** Reusable: landing `/plays/[slug]`, unit routes
`/plays/[slug]/[scene]`, `/plays/[slug]/source` (PR #95 allowlisted public projection), Tamil/English toggle,
speaker/stage-direction units, registry-driven sitemap. **Gap:** `PlayReadingUnit` has no notion of a second,
separately titled **part** with its own scene numbering; supplementary scenes 1–3 would collide with main scenes
1–3 on `order`. P1 must add a minimal, source-faithful part attribute (main play vs `நகைச் சுவைப் பகுதி.`) and use
the source's own stems (`main-NN`, `nagai-suvai-NN`) for slugs — additive to the model, not a new reader, and never
a renumbering to 31–33.

**B3 சங்கத் தமிழ் (Literary Commentary).** Source hierarchy: volume → **104** source-order sections (front matter +
titled pieces; sequence numbers are navigation only; no numbered `மலர்` scheme) → **115** formal provenance units
(+4 source-note-only) → anchor pages. Page types: 374 text · 97 illustration · 9 poetry · front/back matter. Section
bodies are Kalaignar's verse retellings with hard lineation, right-aligned carry-over fragments and illustration
pages; each piece closes with a printed citation of its Sangam source (e.g. `புறநானூறு — பாடல் : 192 — கணியன்
பூங்குன்றன்`). **Not `kural-commentary`** (no பால் → இயல் → அதிகாரம் → குறள் hierarchy and no couplet+commentary pairing).
**Candidate: the `commentary-unit` family** (as Tholkappiya Poonga / Kuraloviyam: free-standing ordered units with
front/back matter; Kuraloviyam already carries per-page source-limited handling), at section granularity — provided
P1 proves it can preserve verse lineation, carry-over fragments, illustration records and the printed source
citation as a distinct element that is not Kalaignar's text. A new reader structure is justified only if that proof
fails. Decision and evidence to be recorded before implementation.

## 10. Projected catalogue / shelf counts (P0 projection — NOT current state)

| Shelf | Current | If all Wave-8 scope later publishes |
|---|---:|---:|
| Life Writing | 1 | 1 |
| Letters | 1 | **1** (Murasoli volumes 48–54 → 42–54) |
| Poetry | 14 | 14 |
| Cinema Writing | 10 | 10 |
| Drama | 10 | **11** |
| Fiction | 162 | 162 |
| Essays & Articles | 15 | 15 |
| Speeches | 117 | 117 |
| Literary Commentary | 3 | **4** |
| **Total** | **333** | **335** (+2) |

Collections remain **9**. These are projections only and must not be written into current/public state.

## 11. P0 classification

| Segment | Item | Classification | Catalogue effect |
|---|---|---|---|
| B1 | Murasoli Vol 42 | READY | existing-work expansion |
| B1 | Murasoli Vol 43 | READY | existing-work expansion |
| B1 | Murasoli Vol 44 | READY | existing-work expansion |
| B1 | Murasoli Vol 45 | READY | existing-work expansion |
| B1 | Murasoli Vol 46 | READY | existing-work expansion |
| B1 | Murasoli Vol 47 | **READY WITH QUALIFICATION** (Letter 3681 / printed p. 252 absent) | existing-work expansion |
| B2 | `ore-mutham` | READY | **+1 LibraryWork** (Drama) |
| B3 | `sangatamil` | **READY WITH QUALIFICATION** (scan 8 permanent source-limited) | **+1 LibraryWork** (Literary Commentary) |

Live evidence supports every expected classification; no row was forced.

## 12. Explicit exclusions (closed scope)

Not in Wave 8: `chinna-chinna-malargal` and any Quotes architecture; Murasoli Volume 1 (complete but outside the
owner-selected scope); Murasoli Volume 41 (active / incomplete); Murasoli Volumes 48–54 (already live — regression
only); any other Murasoli volume; additional public or assembly speeches; financial-statement Speech 16+; in-progress
novels; short stories; essays; cinema; poetry; anything else discovered during inspection.

Out-of-scope observations only (no action): the Murasoli repository holds both `volumes/volume-01` and
`volumes/volume-1` directories, and source directories for Vols 48–53 (the live Vols 48–54 payloads predate this
archival format; the repository has no `volume-54` directory).

## 13. Recommended P1+ segmentation (NOT authorized)

- **B1 — Murasoli 42–47 (existing-work expansion):** source-pinned import adapter for both header dialects; Tamil
  letter payloads + reviewed English; per-volume provenance; Vol 47 Letter 3681 qualification carried end to end;
  source-faithful id disambiguation for duplicate printed numbers; volumes 42–47 added to the existing navigation
  with 48–54 byte-unchanged; one `murasoli-letters` work; verified 42–54 ordering; volume/letter statistics derived
  from data.
- **B2 — ஒரே முத்தம் (new Drama work):** hidden data foundation; 33-unit stage-play reader preserving the 30-main +
  3-supplementary distinction; Tamil/English; allowlisted provenance/source page; direct routes; later
  catalogue/discovery/sitemap publication.
- **B3 — சங்கத் தமிழ் (new Literary Commentary work):** hidden data foundation; reader-structure decision per §9;
  Tamil/English; scan-8 permanent limitation preserved; provenance/source page; direct routes; later publication.

Lifecycle: P0 census/freeze → P1 hidden data foundation → P2 fidelity/readers → P3 direct routes while hidden → P4
publication → P5 independent production acceptance and durable close-out. There is no P6.

## 14. Validation performed for this P0

- No duplicate Wave-8 LibraryWork identity; Vols 42–47 not integrated under any path; `ore-mutham` and `sangatamil`
  absent from catalogue, payloads, routes and sitemap (404 probes above).
- Live website Murasoli set = Volumes 48–54 (346 letters).
- Readiness counts re-derived from the pinned trees (342 Tamil + 342 English Murasoli records; 131/131 ஒரே முத்தம்
  pages verified, 33 scenes, 33 English scenes; சங்கத் தமிழ் 496 + 1 Tamil and 496 + 1 English page records).
- Vol 47 and scan-8 qualifications represented from the archives' own records.
- Projected arithmetic: 333 + 2 = 335; Letters 1 → 1; Drama 10 → 11; Literary Commentary 3 → 4.
- Implementation delta **0**, source delta **0** (read-only clones only), production delta **0** (read-only
  requests only).

## 15. Conclusion

**WAVE 8 P0 — COMPLETE / REVIEW-READY, NOT YET FROZEN BY MERGE.**

- **B1** — Murasoli Volumes 42–47: six-volume expansion of the existing `murasoli-letters` LibraryWork; Volumes
  42–46 READY, Volume 47 READY WITH QUALIFICATION.
- **B2** — `ore-mutham`: READY, one new Drama LibraryWork.
- **B3** — `sangatamil`: READY WITH QUALIFICATION, one new Literary Commentary LibraryWork.

Canonical new-work delta if later published: **+2**. Projected catalogue after eventual Wave-8 publication: **335**.
Murasoli remains **one** catalogue work.

**P1 is NOT STARTED / NOT AUTHORIZED by this P0.**
