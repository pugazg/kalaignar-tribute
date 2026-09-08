# Wave 6 P0 — Global Completed-Works Census

**Wave 6 P0 COMPLETE — census only. P1 NOT STARTED / NOT AUTHORIZED.**

This is a read-only assessment of which completed archival works across the `pugazg` Kalaignar
source repositories are ready for Digital Library onboarding. It authorizes **no** onboarding, no
implementation change, and no source-repository change. Classifications are **READY / HOLD /
ALREADY ONBOARDED / NOT COMPLETE**. "Complete" in a source repo does not automatically mean
Digital-Library-ready.

## Live boundary at census time (2026-09-08)

| | |
|---|---|
| Control `main` | `c0e56199b8fe608148e7a5ac39a8be82bed83ad4` (tree `9bd264b121477e2cbf1512c5ccb22f581f8776dc`) |
| Implementation `main` | `632476baa40ebbe94083ec41a6c8f4a26dfec77c` (tree `6a4b2cd6bdcdada399cdb27247e485527813a7b2`) |
| Open PRs (control / implementation) | 0 / 0 |
| Wave 5 | COMPLETE / CLOSED (P0–P5) |
| Current public catalogue | **78 works**, 9 shelves, 1 collection |

Live GitHub state was authoritative; nothing was reopened from stale prompts.

## Repositories inspected

Kalaignar archival source repositories under `pugazg` (13 relevant):
`kalaignar-autobiography` (implementation), `nenjukku-needhi-archive`, `kalaignar-murasoli-letters`,
`kalaignar-poems`, `kalaignar-stage-plays`, `kalaignar-cinema-works`, `kalaignar-short-stories`,
`kalaignar-novels`, `kalaignar-essays`, `kalaignar-literary-commentary`, `tolkappiyap-poonga`,
`kalaignar-assembly-speeches`, `kalaignar-public-speeches`, `kalaignar-quotes`.

Excluded as not Kalaignar-authored publishable works: `DMK`, `DMK-achievements-2021-2026`,
`Dravidian-Method`, `Kalaignar-Legacy` (legacy docs), `Minequest`, `Silpathikaram`, `ab-2`,
`anna-corpus` (Annadurai), `aytham`, `classical-tamil`, `kalaignar-bio-documentary` (video),
`manimekalai-cinematic-adaptation` (scholarly adaptation, not a Kalaignar-authored work),
`multimodal-fact-verification`, `nannul` (grammar), `sangam-literature-corpus`,
`tolk-ppiyam-english-translation` (a Tolkappiyam translation, not Kalaignar's authored work),
`tolkappiyam-arivagam`.

## Authoritative already-onboarded set (from implementation `main`)

78 published `LibraryWork` records:

| Shelf | Count | Onboarded slugs / source |
|---|---:|---|
| Life Writing | 1 | `nenjukku-neethi` (memoir; source `nenjukku-needhi-archive`) |
| Letters | 1 | `murasoli` (முரசொலி கடிதங்கள்; source `kalaignar-murasoli-letters`) |
| Literary Commentary | 2 | `tholkappiyam` (source `tolkappiyap-poonga`), `thirukkural` (source `kalaignar-literary-commentary`) |
| Cinema Writing | 6 | manohara, parasakthi, tirumbippaar, thirai-isai-paadalgal, manthiri-kumari, raja-rani |
| Drama | 5 | silappathikaram-nataka-kappiyam, bharathayanam, anarkali, socrates, cheran-senguttuvan |
| Essays & Articles | 4 | sakkaravarththiyin-thirumagan, kayittril-thongiya-kanapathi, unarchchimaalai, thiraavida-sampaththu |
| Fiction | 39 | 1 novel `balipeedam-nokki` + 38 short stories (37-story 1977 anthology + `kizhavan-kanavu`) |
| Poetry | 6 | idhayathai-thanthidu-anna, anaiya-vilakku-anna, marathi, thennan-kathai, kaalap-pezhaiyum-kavithai-saaviyum, kalaignarin-kavithaigal |
| Speeches | 14 | udhaya-kathir + 10 industries-debate (assembly) + poonthottam, arappor, kalaivanar-nsk-memorial-day (public) |

Murasoli letters, the memoir, Tholkappiya Poonga and Thirukkural are **existing catalogue works**;
completed additions inside them (e.g. Murasoli Volume 43 FINAL RELEASE COMPLETE) are **existing-work
maintenance**, not new Wave-6 works, and are out of scope for a "new completed-works" wave.

---

## MASTER CENSUS — candidate (not-yet-onboarded) works

Fields: source repo · work path · Tamil title · type · proposed shelf · archival status · provenance ·
structure · Tamil · English · classification · blocker · notes.

### Cinema Writing — `kalaignar-cinema-works`

| Work | Tamil title | Archival status | Tamil | English | Class | Notes |
|---|---|---|---|---|---|---|
| `works/ammaiyappan` | அம்மையப்பன் | closed canonical Tamil + structured derivatives + whole-work English reconciliation PASS; reader/export QA PASS; **Reading Room payload complete-verified QA PASS** (SHA `f00efb81…`) | 105/105 dual-gate, 63 archival scenes, 1,009 dialogue + 16 supplement = 1,025 units | complete-verified 63/63 scenes, 1,210 units | **READY** | Distinct full screenplay/dialogue booklet (source `TVA_BOK_0064230`), NOT the Film Songs anthology's 6 unresolved *Ammayappan* songs. Safeguard: archive scenes are navigation, not printed scene numbers; 5 retained song occurrences stay source-visible, no standalone lyric files, no authorship upgrade; do not cross-contaminate with the Film Songs anthology. |
| `works/naam` | நாம் | active source; first-pass 67/67 but dual-gate verified only 13/67; PDF 5 & 10 physical-damage holds; derivatives/English blocked | in progress | blocked | **NOT COMPLETE** | Verification and English incomplete. |

### Poetry — `kalaignar-poems`

All eight below are Phase-4 **RELEASE-CLEARED** (Tamil FINAL-CLEARED + reviewed/released English) per
`README.md` "Preserved completed work". Proposed shelf: Poetry.

| Work | Tamil title | Class | Notes |
|---|---|---|---|
| `poems/thalaikettan-thambi` | தலைகேட்டான் தம்பி (1966) | **READY** | CLOSED 2026-09-08; 0 unresolved. |
| `poems/aanthaiyum-arasanum` | ஆந்தையும் அரசனும்! (1965) | **READY** | Phase 1–4 complete. |
| `poems/poomudi` | பூமுடி (1965) | **READY** | Phase 1–4 complete. |
| `poems/anna-kaviyarangam` | அண்ணா கவியரங்கம் | **READY** | Release-cleared; confirm standalone-vs-collection reader shape at P1. |
| `poems/gunanayagar-nehru` | குணநாயகர் நேரு | **READY** | Release-cleared. |
| `poems/oruthalaik-kathal` | ஒருதலைக் காதல் | **READY** | Release-cleared. |
| `poems/kalaignarin-kaviyaranga-kavithaigal-1975` | கலைஞரின் கவியரங்கக் கவிதைகள் 1975 | **READY** | Release-cleared; likely a multi-item publication — confirm publication vs standalone model at P1. |
| `poems/kanchithan-annan` | காஞ்சித்தான் அண்ணன் | **READY** | Release-cleared. |

A secondary-witness comparison lane (Bharathiar University 2009 English translations) is active but is
**report-only** and does not affect release-cleared Tamil/English; not an onboarding blocker.

### Novels — `kalaignar-novels`

| Work | Tamil title | Class | Notes |
|---|---|---|---|
| `works/periya-idathup-pen` | பெரிய இடத்துப் பெண் | **READY** | Source audit complete; assembled Tamil PASSED; English VERIFIED; "release-ready with qualification" — confirm the exact qualification at P1. Reader model = novel sections (like `balipeedam-nokki`). |
| `works/pudhaiyal` | புதையல் | **READY** | 448 canonical / **446 complete / 2 physical-loss `needs-review`**; English VERIFIED; "release-ready with qualification". The 2 physical-loss pages are a documented, non-blocking source-damage qualification (cf. Tirumbippaar's front-matter crop) — preserve as documented, never reconstruct. |
| `works/vellikkizhamai` | வெள்ளிக்கிழமை | **NOT COMPLETE** | Canonical 118/179; assembled Tamil & English not started/blocked. (Blocks short-stories `நடுத்தெரு நாராயணி`.) |

### Essays & Articles — `kalaignar-essays`

Publications **1–9 are RELEASE COMPLETE / FROZEN**; Publication 10 is in progress. 4 of the 9 are
onboarded. Proposed shelf: Essays & Articles.

| Work | Tamil title | Class | Notes |
|---|---|---|---|
| `publications/ina-muzhakkam` | இன முழக்கம் | **READY** | In the frozen 1–9 set. (An earlier Wave-5 census listed it "not ready"; live essays `main` now records it RELEASE COMPLETE — live state governs.) Confirm English release at P1. |
| `publications/kolaikkalam` | கொலைக்களம் | **READY** | In the frozen 1–9 set. (Earlier "English mid-translation"; live `main` now RELEASE COMPLETE.) Confirm English release at P1. |
| `publications/kudumbaththin-nalvilakku` | குடும்பத்தின் நல்விளக்கு | **READY** | In the frozen 1–9 set; a Wave-5 census runner-up ("fully frozen"). Confirm English release at P1. |
| `publications/sinthanaiyum-seyalum` | சிந்தனையும் செயலும் | **READY** | In the frozen 1–9 set. Confirm English release at P1. |
| `publications/vedhanai-ch-siraiyinindrum-viduthalai-pera` | வேதனைச் சிறையினின்றும் விடுதலை பெற | **READY** | In the frozen 1–9 set. Confirm English release at P1. |
| `publications/meesai-mulaiththa-vayathil` | மீசை முளைத்த வயதில் | **NOT COMPLETE** | Publication 10; P2 in progress (30/146 verified); English blocked until Tamil P5 freeze. |

Readiness caveat for the 5 READY essays: essays onboard bilingually. "RELEASE COMPLETE" in this repo
historically includes the English E-phases (Publication 9 shows a released English blob, E6/E7 PASS);
P1 must reconfirm each publication's English release + build a Reading Room payload. Any lacking English
becomes **HOLD (TRANSLATION)**.

### Speeches — `kalaignar-assembly-speeches` + `kalaignar-public-speeches`

| Work | Tamil title | Source | Class | Notes |
|---|---|---|---|---|
| `sources/1971-namathu-nilai` → `speeches/1971/1971-namathu-nilai` | நமது நிலை (1971) | assembly | **READY** | Tamil complete + English verified (58/58 Gate-G, final closure PASS). **Edited two-House witness, `date: null`** — must not be catalogued as a single dated Assembly transcript; frame as an edited compilation booklet. |
| `speeches/idhaya-perikai` | இதய பேரிகை (1951) | public | **READY** | Tamil + English verified-complete (32/32). Multi-section booklet, no single speech date/venue — do not invent one; PDF-3 printer name unresolved (library-stamp occlusion, bibliographic only). |
| `speeches/palli-vazhkkai` | பள்ளி வாழ்க்கை (1952) | public | **READY** | Tamil + English verified-complete (76/76). Printed **compilation** of speeches; component dates/single venue not supplied — do not infer. Pre-1978 glyphs resolved to scan-supported characters. |

The 11 dated assembly speeches and `poonthottam`/`arappor`/`kalaivanar-nsk-memorial-day` are already
onboarded.

### Fiction — short stories — `kalaignar-short-stories`

Closed complete collections (Tamil/visual/English PASS) beyond the onboarded 1977 anthology + `kizhavan-kanavu`:

| Collection | Works | Class | Notes |
|---|---:|---|---|
| 2008 collection | 40 | **READY** | Tamil/visual/English 40/40 PASS. |
| 2004 collection | 34 | **READY** | Tamil/visual/English 34/34 PASS. |
| 1987 `கலைஞர் சொன்ன குட்டிக் கதைகள்` | 25 | **READY** | Tamil + English 25/25 PASS/CLOSED; final English release audit recorded. |
| 2009 new-story onboarding | 5 | **READY** | 5/5 CLOSED new canonical stories (separate from the 2009 existing-canonical witness comparison, 11/11, which are witnesses, not new works). |
| 1982 `முடியாத தொடர்கதை` | 5 | **NOT COMPLETE** | Tamil 1/5 closed; English not started. |
| `நடுத்தெரு நாராயணி` | — | **NOT COMPLETE** | Blocked from starting (waits on novels `வெள்ளிக்கிழமை`). |

**Mandatory P1 clearance for the 4 READY collections:** each member story must pass duplicate/canonical-identity
clearance against the existing 1977 anthology, `kizhavan-kanavu`, and across the collections, exactly as
the archive's per-story activation already does. Onboarding model = fiction **collections** (each collection
one discovery entry standing in for its member works, like the 1977 anthology). This is the single largest
READY partition (**104 member works**).

### Literary Commentary — `kalaignar-literary-commentary`

| Work | Class | Notes |
|---|---|---|
| `works/thirukkural` | ALREADY ONBOARDED | = `thirukkural`. |
| `works/sangatamil` (சங்கத் தமிழ்) | **NOT COMPLETE** | Active Gemini-transcription/structural-correction workflow. |
| `works/kuraloviyam` (குறளோவியம்) | **NOT COMPLETE** | Active; Part 001 Pass 1 through scan 111. |

### Quotes — `kalaignar-quotes`

| Work | Class | Notes |
|---|---|---|
| `collections/chinna-chinna-malargal` (கலைஞரின் சின்னச் சின்ன மலர்கள்) | **HOLD** | Archivally complete: 497/497 canonical Tamil (496 verified, 1 `needs_review` from a physical scan blemish — non-blocking to identity), full English 497/497 published, indexes published, COMPLETION recorded. **Blocker: PUBLICATION_MODEL** — the Digital Library has no `quotes` shelf or quote reader/route model; onboarding needs a new shelf + reader-model design + owner decision, not more source work. |

### Already-onboarded source repos (no new completed works)

- `nenjukku-needhi-archive` → memoir `nenjukku-neethi` — ALREADY ONBOARDED.
- `tolkappiyap-poonga` → `tholkappiyam` — ALREADY ONBOARDED (actively maintained: recent English toggle, malar-13 fix).
- `kalaignar-murasoli-letters` → `murasoli` — ALREADY ONBOARDED; Volume 43 FINAL RELEASE COMPLETE is existing-work maintenance, not a new work.

---

## READY LIST (grouped by shelf)

**Cinema Writing (1):** `ammaiyappan`. Reader model: cinema `scene` (archival navigation). Adapter exists (Manohara/Raja). Safeguard: archival scenes ≠ printed numbers; retained song occurrences not upgraded; keep separate from Film Songs anthology.

**Poetry (8):** thalaikettan-thambi · aanthaiyum-arasanum · poomudi · anna-kaviyarangam · gunanayagar-nehru · oruthalaik-kathal · kalaignarin-kaviyaranga-kavithaigal-1975 · kanchithan-annan. Reader models: standalone poem + poetry-publication (both exist from Wave 4). Confirm per-work standalone-vs-publication shape at P1.

**Novels → Fiction (2):** periya-idathup-pen · pudhaiyal. Reader model: novel sections (exists — `balipeedam-nokki`). Safeguards: pudhaiyal 2 physical-loss pages documented/never reconstructed; confirm periya-idathup-pen's qualification.

**Essays & Articles (5):** ina-muzhakkam · kolaikkalam · kudumbaththin-nalvilakku · sinthanaiyum-seyalum · vedhanai-ch-siraiyinindrum-viduthalai-pera. Reader model: essay publication (exists). Confirm English release + payload per publication at P1.

**Speeches (3):** namathu-nilai · idhaya-perikai · palli-vazhkkai. Reader model: speech (exists). Safeguards: no invented dates/venues; edited-compilation/edited-witness framing (`date: null` where applicable).

**Fiction — short-story collections (4 collections / 104 member works):** 2008 (40) · 2004 (34) · 1987 குட்டிக் கதைகள் (25) · 2009 new (5). Reader model: short story + fiction collection (exists — 1977 anthology). Mandatory duplicate-identity clearance at P1.

**TOTAL READY WORKS = 123** — comprising **19 standalone/publication works** (1 cinema + 8 poetry + 2 novels + 5 essays + 3 speeches) **+ 104 short-story member works across 4 new collections.**

## HOLD LIST (exact blockers)

| Work | Blocker | Minimum to reach READY |
|---|---|---|
| `kalaignar-quotes` / chinna-chinna-malargal | `PUBLICATION_MODEL` | Owner decision + design of a new Quotes shelf and a quote-collection reader/route model in the Digital Library; then a payload. (Archival work is already complete; the 1 `needs_review` is a non-blocking physical-blemish note.) |

## NOT-COMPLETE LIST

| Work | Repo | Current phase | Likely soon? |
|---|---|---|---|
| நாம் (naam) | cinema | dual-gate 13/67; English blocked; 2 physical-damage holds | Not near — verification early |
| வெள்ளிக்கிழமை (vellikkizhamai) | novels | canonical 118/179; assembly & English not started | Mid-transcription |
| மீசை முளைத்த வயதில் (meesai-mulaiththa-vayathil) | essays Pub 10 | P2 30/146; English blocked | Early |
| முடியாத தொடர்கதை (1982) | short-stories | Tamil 1/5; English not started | Early |
| நடுத்தெரு நாராயணி | short-stories | blocked (waits on vellikkizhamai) | No |
| சங்கத் தமிழ் (sangatamil) | literary-commentary | active transcription-correction | Unclear |
| குறளோவியம் (kuraloviyam) | literary-commentary | Part 001 Pass 1 through scan 111 | Early |
| இரத்தக் கண்ணீர் (iratha-kanneer) | stage-plays | pages 20/188; scene assembly & English not started | Early |

Stage-plays `ore-mutham`, `thiruvalar-desiyampillai`, `kagithapoo`, `manimagudam` are marked "closed"
in the plays HANDOVER but their per-work Digital-Library readiness (English + reader payload) is not
established from the top-level docs. `ore-mutham` explicitly has "completed Tamil + English workflows"
and is the strongest of these — but pending per-work confirmation it is treated conservatively:

| Work | Repo | Class | Notes |
|---|---|---|---|
| `works/ore-mutham` (ஒரே முத்தம்) | stage-plays | **HOLD → likely READY** | Tamil + English workflows CLOSED per HANDOVER; needs per-work reader/payload + structure confirmation at P1 before READY. Blocker: `STRUCTURE`/`PROVENANCE` confirmation only. |
| `works/thiruvalar-desiyampillai`, `works/kagithapoo`, `works/manimagudam` | stage-plays | **HOLD** | "Closed" but completion state (verified transcription + English + reader model) not established from top-level docs; `manimagudam` was historically excluded as incomplete at freeze. Blocker: `SOURCE_VERIFICATION`/`WORK_TYPE` confirmation. |

(These plays are conservatively HOLD rather than READY because P0 must not force READY on a `complete`
label without evidence of Digital-Library reader readiness.)

---

## FEASIBILITY ASSESSMENT

- **Total READY: 123 works** (19 standalone/publication + 104 short-story members), plus `ore-mutham`
  pending confirmation.
- Source repositories: **6** (cinema, poems, novels, essays, speeches ×2, short-stories).
- Distinct reader models: cinema-scene, standalone-poem, poetry-publication, novel-sections,
  essay-publication, speech, short-story, fiction-collection — **all already exist** in the implementation.
- Shelves affected: Cinema, Poetry, Fiction, Essays & Articles, Speeches.
- Projected catalogue: **78 → ~201 works** (Fiction 39 → 143, Poetry 6 → 14, Essays 4 → 9, Cinema 6 → 7,
  Speeches 14 → 17; collections 1 → 5).
- Route/sitemap growth (rough, precise counts need P1 registry enumeration): ammaiyappan ≈ 65 (landing +
  source + 63 scenes); short stories ≈ 104 × 2 + 4 collection landings ≈ **212**; poems ≈ 16–40 depending
  on publication items; novels: pudhaiyal/periya-idathup-pen section routes (tens–low hundreds); essays:
  5 publications × (landing + source + articles); speeches ≈ 6. Order of magnitude: **several hundred to
  ~1,000+ new routes / sitemap URLs**, and a comparable prerender/`.html` increase — the largest single
  route/build expansion in the project's history.
- Validator/CI complexity: one new source-linked validator per family + per-collection duplicate-identity
  proofs; the short-story collections carry the highest duplicate-identity and reviewability risk.

### Recommendation: **B — ONE WAVE, PARTITIONED INTERNALLY**

Run a single Wave-6 governance programme, but implement P1–P6 as **deterministic per-shelf/family batches**
rather than one monolithic change, because:

1. the reader models all already exist, so this is onboarding volume, not new architecture — one governance
   programme is coherent;
2. but 123 works across 6 repos and 5 shelves is far too large for one reviewable implementation PR, and the
   **104 short-story members** carry real duplicate-identity risk that must be cleared collection-by-collection;
3. deterministic batches (e.g. Cinema `ammaiyappan`; Poetry 8; Speeches 3; Novels 2; Essays 5; then the four
   short-story collections individually) keep each PR exact-head-reviewable and each production-verifiable,
   while the single Wave-6 census/close-out governs the whole set.

If review/production-acceptance burden proves too high even in batches, fall back to **C — MULTIPLE WAVES**
(the short-story backlog as its own wave is the natural split). **A — one monolithic wave — is not
recommended** given the scale and the fiction duplicate-identity risk.

## PROPOSED WAVE-6 STAGING (not executed)

- **P0** — global completed-work census *(this document)*
- **P1** — exact per-work source/tree freeze + deterministic payload foundation (per family batch), incl.
  short-story duplicate-identity clearance and per-work English/reader confirmation
- **P2** — reader/data generation + per-family validators
- **P3** — public routes / readers
- **P4** — catalogue / discovery / sitemap integration
- **P5** — library-wide cross-work / inventory regression hardening (the Wave-5 P4 pattern, extended)
- **P6** — production acceptance + final Wave-6 close

Each stage requires its own explicit owner authorization. **P1 is NOT authorized and has NOT started.**

## Scope confirmation

- **0** implementation-repository changes; **0** source-repository changes; **0** new public routes;
  **0** new catalogue entries; **0** sitemap change; **0** production change.
- This is control-repo documentation only. No onboarding has begun.
- **Wave 6 P1 is NOT authorized and has NOT started.**
