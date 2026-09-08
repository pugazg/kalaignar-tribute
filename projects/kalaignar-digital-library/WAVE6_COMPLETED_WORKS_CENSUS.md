# Wave 6 P0 — Global Completed-Works Census

**Wave 6 P0 COMPLETE — census only. P1 NOT STARTED / NOT AUTHORIZED.**

Read-only assessment of which completed archival works across the `pugazg` Kalaignar source
repositories are ready for Digital Library onboarding. Authorizes **no** onboarding and **no**
implementation/source change. Classifications: **READY / HOLD / ALREADY ONBOARDED / NOT COMPLETE**.
"Complete" in a source repo does not automatically mean Digital-Library-ready. Every count below is
derived from **unique canonical work identities** (source-entry count ≠ canonical-work count), and
classifications for physically-damaged or per-work-closed works were adjudicated from each work's own
per-work documents, not only the repo root handovers.

> This revision corrects the first head (`5e0ec141…`, NOT APPROVED): the 1987 identity count
> (23 distinct, not 25 source entries), adds the 1997 story `நண்பனா?`, fully adjudicates the four
> closed stage plays from their per-work docs, verifies all five essays' English release, and recomputes
> every count from the classified rows.

## Live boundary at census time (2026-09-08)

| | |
|---|---|
| Control `main` | `c0e56199b8fe608148e7a5ac39a8be82bed83ad4` (tree `9bd264b121477e2cbf1512c5ccb22f581f8776dc`) |
| Implementation `main` | `632476baa40ebbe94083ec41a6c8f4a26dfec77c` (tree `6a4b2cd6bdcdada399cdb27247e485527813a7b2`) |
| Open PRs (control / implementation) | 0 / 0 |
| Wave 5 | COMPLETE / CLOSED (P0–P5) |
| Current public catalogue | **78 works**, 9 shelves, 1 collection |

## Repositories inspected

**13 Kalaignar archival/source repositories** inspected: `nenjukku-needhi-archive`,
`kalaignar-murasoli-letters`, `kalaignar-poems`, `kalaignar-stage-plays`, `kalaignar-cinema-works`,
`kalaignar-short-stories`, `kalaignar-novels`, `kalaignar-essays`, `kalaignar-literary-commentary`,
`tolkappiyap-poonga`, `kalaignar-assembly-speeches`, `kalaignar-public-speeches`, `kalaignar-quotes` —
**plus the implementation repository `pugazg/kalaignar-autobiography`** (the Digital Library itself, used
to establish the already-onboarded set; it is not one of the source repositories).
Excluded (not Kalaignar-authored publishable works): DMK, DMK-achievements-2021-2026, Dravidian-Method,
Kalaignar-Legacy, Minequest, Silpathikaram, ab-2, anna-corpus (Annadurai), aytham, classical-tamil,
kalaignar-bio-documentary (video), manimekalai-cinematic-adaptation (scholarly adaptation),
multimodal-fact-verification, nannul, sangam-literature-corpus, tolk-ppiyam-english-translation,
tolkappiyam-arivagam.

## Already-onboarded set (from implementation `main`) — 78 works

Life Writing 1 (`nenjukku-neethi`) · Letters 1 (`murasoli`) · Literary Commentary 2 (`tholkappiyam`,
`thirukkural`) · Cinema Writing 6 · Drama 5 · Essays & Articles 4 · Fiction 39 (1 novel + 38 short
stories = 37-story 1977 anthology + `kizhavan-kanavu`) · Poetry 6 · Speeches 14. Murasoli/memoir/
Tholkappiyam/Thirukkural completed additions (e.g. Murasoli Volume 43) are **existing-work maintenance**,
not new Wave-6 works.

---

## MASTER CENSUS — candidate (not-yet-onboarded) works

### Cinema Writing — `kalaignar-cinema-works`

| Work | Tamil title | Class | Evidence / notes |
|---|---|---|---|
| `works/ammaiyappan` | அம்மையப்பன் | **READY** | Canonical Tamil 105/105 dual-gate; 63 archival scenes; 1,025 dialogue units; English 63/63 · 1,210 units reconciliation PASS; reader/export QA PASS; **Reading Room payload complete-verified QA PASS** (`f00efb81…`). Distinct full screenplay/dialogue booklet (`TVA_BOK_0064230`), NOT the Film Songs anthology's 6 unresolved *Ammayappan* songs. Safeguard: archival scenes = navigation not printed numbers; 5 retained song occurrences not upgraded; keep separate from Film Songs anthology. |
| `works/naam` | நாம் | **NOT COMPLETE** | Dual-gate verified 13/67; PDF 5 & 10 physical-damage holds; derivatives/English blocked. |

### Drama — `kalaignar-stage-plays` (adjudicated per-work)

| Work | Tamil title | Class | Evidence / notes |
|---|---|---|---|
| `works/kagithapoo` | காகிதப்பூ (1967) | **READY** | Tamil 41/41 verified; scene assembly **23/23 CLOSED, final review PASS**; English **23/23 CLOSED, final review PASS**; blocking translation issues **0**. Safeguard: source-visible compression (Scenes 2–5), the **unnumbered `காட்சி` between Scene 21 and Scene 24**, no invented Scenes 22/23, no normalization. Drama reader family adapts directly. |
| `works/manimagudam` | மணிமகுடம் (2010, 6th ed.) | **READY** | Tamil **170/170 COMPLETE**; scenes **47/47 PASS**; English **47/47 PASS**; unresolved assembly/English **0/0**. Safeguard: the user-supplied **1962 Madurai** performance claim is **catalogue context, not controlling-source fact** — the scan independently supplies May 1956 (Tiruchirappalli) and Sept 1963 stagings; keep source-derived performance evidence separate from user context. |
| `works/thiruvalar-desiyampillai` | திருவாளர் தேசீயம்பிள்ளை (1965, 2nd ed.) | **READY WITH QUALIFICATION** | 49/49 processed; **40/49 verified**; 7/7 Tamil SRUs assembled/reviewed PASS; English **7/7 reviewed, final PASS**. Qualification: **9 documented source-condition holds** (front-matter physical loss 1,3,4,5; body paper-loss 7,8,9; unresolved clusters 35,36) — localized, terminal physical loss, visibly represented, never reconstructed, provenance complete. Accepted on the **pudhaiyal principle** (documented terminal physical loss is publishable when the workflow is exhausted, no fabrication, holds represented). Safeguard: source has no numbered scenes/acts (7 editorial SRUs); scan-47 `உதயசூரியன் கோலம்` is an intertitle; scan-48 has no printed `முற்றும்`. |
| `works/ore-mutham` | ஒரே முத்தம் (1964, 5th ed.) | **HOLD — SOURCE_VERIFICATION** | Workflow exhausted/CLOSED: 131/131 processed; Tamil scenes 33/33 audit PASS; English 33/33 reviewed PASS; no fabrication; holds represented; provenance complete. **But 28/131 scans are terminal `blocked` (27 scene-relevant) ≈ 21% of the source**, spread across the main play. Reasoning: this is an order of magnitude more terminal unresolved reading text than the accepted precedents (pudhaiyal 2/448 ≈ 0.4%; Tirumbippaar front-matter crop only; thiruvalar 9/49 mostly front-matter). The extent of gapped public reading text is **too substantial for clean public onboarding** under the current source evidence. This is an **owner decision**: the workflow is honest and closed, so the owner may elect READY-WITH-QUALIFICATION; absent that, P0 holds it to avoid weakening the archival standard. Not NOT-COMPLETE (nothing more to process from current source). |

### Poetry — `kalaignar-poems`

Eight Phase-4 **RELEASE-CLEARED** works (Tamil FINAL-CLEARED + reviewed/released English) per `README.md`
"Preserved completed work", none onboarded → all **READY** (Poetry):
`thalaikettan-thambi` · `aanthaiyum-arasanum` · `poomudi` · `anna-kaviyarangam` · `gunanayagar-nehru` ·
`oruthalaik-kathal` · `kalaignarin-kaviyaranga-kavithaigal-1975` · `kanchithan-annan`. Confirm
standalone-vs-publication reader shape per work at P1 (`anna-kaviyarangam` and
`kalaignarin-kaviyaranga-kavithaigal-1975` may be multi-item publications). The active Bharathiar
University secondary-witness lane is report-only and not a blocker.

### Novels (→ Fiction shelf) — `kalaignar-novels`

| Work | Tamil title | Class | Evidence / notes |
|---|---|---|---|
| `works/periya-idathup-pen` | பெரிய இடத்துப் பெண் | **READY** | Source audit complete; assembled Tamil PASSED; English VERIFIED ("release-ready with qualification" — confirm exact qualification at P1). Reader model = novel sections. |
| `works/pudhaiyal` | புதையல் | **READY** | 448 canonical / **446 complete / 2 physical-loss `needs-review`**; English VERIFIED; release-ready with qualification. The 2 physical-loss pages are documented, non-blocking, never reconstructed. |
| `works/vellikkizhamai` | வெள்ளிக்கிழமை | **NOT COMPLETE** | Canonical 118/179; assembly & English not started/blocked. (Blocks short-stories `நடுத்தெரு நாராயணி`.) |

### Essays & Articles — `kalaignar-essays` (all five English-verified now)

Publications 1–9 RELEASE COMPLETE / FROZEN; Publication 10 in progress. 4 onboarded. The 5 not-onboarded
complete publications are each confirmed **Tamil FROZEN + English RELEASE COMPLETE / FROZEN**:

| Work | Tamil title | English release | Class |
|---|---|---|---|
| `publications/ina-muzhakkam` | இன முழக்கம் | COMPLETE / RELEASED / FROZEN (E6 PASS, E7 RELEASE COMPLETE) | **READY** |
| `publications/kolaikkalam` | கொலைக்களம் | COMPLETE / RELEASED / FROZEN (6/6 verified articles) | **READY** |
| `publications/kudumbaththin-nalvilakku` | குடும்பத்தின் நல்விளக்கு | COMPLETE / RELEASED / FROZEN | **READY** |
| `publications/sinthanaiyum-seyalum` | சிந்தனையும் செயலும் | RELEASE COMPLETE / FROZEN (E0/E6/E7 PASS) | **READY** |
| `publications/vedhanai-ch-siraiyinindrum-viduthalai-pera` | வேதனைச் சிறையினின்றும் விடுதலை பெற | RELEASE COMPLETE / FROZEN (verified) | **READY** |
| `publications/meesai-mulaiththa-vayathil` | மீசை முளைத்த வயதில் | — (P2 30/146; English blocked) | **NOT COMPLETE** |

### Speeches — `kalaignar-assembly-speeches` + `kalaignar-public-speeches`

| Work | Tamil title | Source | Class | Notes |
|---|---|---|---|---|
| `speeches/1971/1971-namathu-nilai` | நமது நிலை (1971) | assembly | **READY** | Tamil complete + English verified (Gate-G 58/58, final closure PASS). Edited two-House witness, **`date: null`** — not a single dated Assembly transcript. |
| `speeches/idhaya-perikai` | இதய பேரிகை (1951) | public | **READY** | Tamil + English verified-complete (32/32). Multi-section booklet, no single date/venue; PDF-3 printer name unresolved (library stamp — bibliographic only). |
| `speeches/palli-vazhkkai` | பள்ளி வாழ்க்கை (1952) | public | **READY** | Tamil + English verified-complete (76/76). Printed compilation; component dates/venue not supplied — do not infer. |

### Fiction — short stories — `kalaignar-short-stories` (unique canonical identities)

**Source-entry count is not canonical-work count.** Each collection's stories were duplicate/canonical
rechecked at activation; witness-only entries map to an existing controlling canonical work and are
**witness relations, not new LibraryWorks**.

| Collection dir | Source entries | New unique works | Class | Notes |
|---|---:|---:|---|---|
| `2008-kalaignar-sonna-kathaigal` | 40 | **40** | READY | Tamil/visual/English 40/40 PASS. |
| `2004-kalaignarin-kuttik-kathaigal` | 34 | **34** | READY | Tamil/visual/English 34/34 PASS. |
| `1987-kalaignar-sonna-kuttik-kathaigal` | 25 | **23** | READY | 25/25 identity-routing COMPLETE; **23 distinct + 2 witness-only**: Story 2 `அராபியக் கதை` = witness of canonical `ஜாடி குட்டி போடுமா?`; Story 11 `குருவி ராமேஸ்வரம்` = witness of an existing 2004 canonical story. Record the 2 as witness relations, not works. |
| `2009-16-kathaiyinile` | 16 | **5** | READY | 5 new canonical stories CLOSED; the other 11 are existing-canonical witnesses (comparison 11/11 CLOSED), not new works. |
| `1997-dravida-iyakka-ezhuthalar-sirukathaigal` | 10 | **1** | READY | Only **`நண்பனா?`** (`stories/nanbana/`) is new canonical — Tamil PASS, visual PASS, English PASS/complete, 0 unresolved; confirmed absent from implementation. 8 entries are pre-existing witnesses; `நடுத்தெரு நாராயணி` is deferred to short-novel handling. |
| `1982-mudiyatha-thodarkathai` | 5 | 0 | **NOT COMPLETE** | Source container of **5 separate story targets**, not one work — counted as **5 distinct NOT-COMPLETE candidate works** (see the per-story preflight below). Only Story 1 has closed Tamil; English not released; Stories 2–5 not transcribed. |
| `நடுத்தெரு நாராயணி` (in 1997) | — | 0 | **NOT COMPLETE** | Deferred/blocked (waits on novels `வெள்ளிக்கிழமை`); counted once. |

#### 1982 `முடியாத தொடர்கதை` per-story identity preflight (read-only)

The anthology is a **source container, not a canonical work**. A fresh read-only live-`main` duplicate/
canonical search (repository routing note: "GitHub searches on live `main` for all five exact headings and
distinctive fragments returned no existing canonical story match") plus a check against the 78 onboarded
works found **no existing canonical match** for any of the five. Each is a distinct future short-story
candidate; none is a duplicate.

| # | Title | Existing canonical workspace | Unique-identity status | Archival phase | English | Class |
|---:|---|---|---|---|---|---|
| 1 | `பெற்ற பிள்ளையை விற்ற தாய்` | `stories/petra-pillaiyai-vitra-thaai/` (new canonical) | unique; no existing match | Tamil/source PASS/CLOSED (22/22) | not released (collection-wide Tamil phase unfinished) | **NOT COMPLETE** |
| 2 | `காசா லேசா` | none | unique; no existing match (recheck on activation) | not transcribed (NEXT) | not started | **NOT COMPLETE** |
| 3 | `சீமான் வீட்டு சீக்காளி` | none | unique; no existing match (recheck on activation) | not transcribed | not started | **NOT COMPLETE** |
| 4 | `நந்தியூர் நரியப்பன்` | none | unique; no existing match (recheck on activation) | not transcribed | not started | **NOT COMPLETE** |
| 5 | `முடியாத தொடர்கதை` (≠ the collection title) | none | unique; no existing match (recheck on activation) | not transcribed | not started | **NOT COMPLETE** |

So the 1982 source contributes **5 NOT-COMPLETE candidate works**, not one. It is **not** a projected
Wave-6 public collection (it is incomplete).

**Unique new short-story works = 40 + 34 + 23 + 5 + 1 = 103.** Mandatory P1 duplicate-identity clearance
across all collections and against the 1977 anthology + `kizhavan-kanavu` (the archive already routes
per story; P0 has resolved the canonical-vs-witness classification above).

### Literary Commentary — `kalaignar-literary-commentary`

`works/thirukkural` ALREADY ONBOARDED. `works/sangatamil` (சங்கத் தமிழ்) and `works/kuraloviyam`
(குறளோவியம்) — **NOT COMPLETE** (active transcription/correction).

### Quotes — `kalaignar-quotes`

| Work | Class | Notes |
|---|---|---|
| `collections/chinna-chinna-malargal` (கலைஞரின் சின்னச் சின்ன மலர்கள்) | **HOLD — PUBLICATION_MODEL** | Archivally complete: 497/497 canonical Tamil (496 verified, 1 `needs_review` physical-blemish, non-blocking), English 497/497 published, indexes published, COMPLETION recorded. Blocker: the Digital Library has **no Quotes shelf or quote reader/route model** — onboarding needs a new shelf + reader-model design + owner decision, not more source work. |

### Already-onboarded source repos (no new completed works)

`nenjukku-needhi-archive` → memoir; `tolkappiyap-poonga` → tholkappiyam; `kalaignar-murasoli-letters` →
murasoli (Volume 43 FINAL RELEASE COMPLETE is existing-work maintenance).

---

## READY LIST (grouped by shelf) — recomputed from the rows above

| Shelf | READY works | Items |
|---|---:|---|
| Cinema Writing | 1 | ammaiyappan |
| Drama | 3 | kagithapoo, manimagudam, thiruvalar-desiyampillai (with qualification) |
| Poetry | 8 | thalaikettan-thambi, aanthaiyum-arasanum, poomudi, anna-kaviyarangam, gunanayagar-nehru, oruthalaik-kathal, kalaignarin-kaviyaranga-kavithaigal-1975, kanchithan-annan |
| Fiction — novels | 2 | periya-idathup-pen, pudhaiyal (with qualification) |
| Fiction — short stories | 103 | 2008 (40) + 2004 (34) + 1987 (23) + 2009 (5) + நண்பனா? (1) |
| Essays & Articles | 5 | ina-muzhakkam, kolaikkalam, kudumbaththin-nalvilakku, sinthanaiyum-seyalum, vedhanai-ch-siraiyinindrum-viduthalai-pera |
| Speeches | 3 | namathu-nilai, idhaya-perikai, palli-vazhkkai |

Standalone/publication works = 1 + 3 + 8 + 2 + 5 + 3 = **22**. Short-story member works = **103**.

**TOTAL READY WORKS = 22 + 103 = 125.**

All required reader models already exist (cinema-scene, drama-scene/SRU, standalone-poem,
poetry-publication, novel-sections, essay-publication, speech, short-story, fiction-collection).

## HOLD LIST (exact blockers)

| Work | Blocker | Minimum to reach READY |
|---|---|---|
| stage-plays `ore-mutham` | `SOURCE_VERIFICATION` | Owner decision to accept ~21% terminal documented physical-source loss (27 scene-relevant blocked scans) for public onboarding, or improved source condition. Workflow is already exhausted/closed. |
| quotes `chinna-chinna-malargal` | `PUBLICATION_MODEL` | Owner decision + design of a Quotes shelf and a quote-collection reader/route model, then a payload. Archival work is already complete. |

## NOT-COMPLETE LIST — 12 candidate works (counted by individual work identity)

| Work | Repo | Phase | Likely soon? |
|---|---|---|---|
| நாம் | cinema | dual-gate 13/67; English blocked | No |
| வெள்ளிக்கிழமை | novels | canonical 118/179; assembly/English not started | Mid |
| மீசை முளைத்த வயதில் (essays Pub 10) | essays | P2 30/146; English blocked | Early |
| நடுத்தெரு நாராயணி | short-stories → short-novel | deferred (waits on வெள்ளிக்கிழமை); counted once | No |
| சங்கத் தமிழ் | literary-commentary | active transcription-correction | Unclear |
| குறளோவியம் | literary-commentary | Part 001 Pass 1 through scan 111 | Early |
| இரத்தக் கண்ணீர் | stage-plays | pages 20/188; assembly/English not started | Early |
| 1982 Story 1 `பெற்ற பிள்ளையை விற்ற தாய்` | short-stories | Tamil CLOSED; English not released | Mid |
| 1982 Story 2 `காசா லேசா` | short-stories | not transcribed (NEXT) | Early |
| 1982 Story 3 `சீமான் வீட்டு சீக்காளி` | short-stories | not transcribed | Early |
| 1982 Story 4 `நந்தியூர் நரியப்பன்` | short-stories | not transcribed | Early |
| 1982 Story 5 `முடியாத தொடர்கதை` | short-stories | not transcribed | Early |

**NOT COMPLETE = 12** (7 single works + the 5 individual 1982 stories). `நடுத்தெரு நாராயணி` is counted
exactly once despite living in the short-story archive with intended short-novel handling.

## Candidate totals (from individual work identities)

| Class | Works |
|---|---:|
| READY | **125** |
| HOLD | **2** |
| NOT COMPLETE | **12** |
| **Total not-yet-onboarded candidate works** | **139** |
| ALREADY ONBOARDED | 78 |

---

## RECOMPUTED PROJECTIONS (onboarding all 125 READY works)

**Derivation is from the individual READY rows only; the two novels are inside the fiction total below,
not double-counted in any standalone figure.**

**Projected catalogue: 78 + 125 = 203 works.**

Projected shelf census:

| Shelf | Now | Δ | After |
|---|---:|---:|---:|
| Life Writing | 1 | 0 | 1 |
| Letters | 1 | 0 | 1 |
| Fiction | 39 | +105 (2 novels + 103 short stories) | **144** |
| Poetry | 6 | +8 | 14 |
| Drama | 5 | +3 | 8 |
| Cinema Writing | 6 | +1 | 7 |
| Speeches | 14 | +3 | 17 |
| Essays & Articles | 4 | +5 | 9 |
| Literary Commentary | 2 | 0 | 2 |
| **Total** | **78** | **+125** | **203** |

(Fiction: 39 → 39 + 2 + 103 = **144**. Consistent with the 203 total: 78 + 125 = 203.)

**Projected collections: 1 → 5.** New `LibraryCollection` objects come from actual anthology sources that
group member works, not from every source PDF: **2008, 2004, 1987, 2009** each become a collection. The
**1997** source does **not** become a public collection (only `நண்பனா?` is new — it onboards as a
**standalone** fiction story; the 8 pre-existing entries are witnesses and `நடுத்தெரு நாராயணி` is
deferred). The 2009 collection's exact membership (whether it also groups its 11 existing-canonical
witness works, which the plural `collectionsForWork` model supports) is a P1 decision.

**Projected discovery entries (approximate — P1 confirms):** currently 42. Fiction discovery would grow
from 3 to ≈10 (5 collections — 1977 + 2008 + 2004 + 1987 + 2009 — plus ≈5 standalone: balipeedam-nokki,
kizhavan-kanavu, periya-idathup-pen, pudhaiyal, nanbana); poetry 6→14; drama 5→8; cinema 6→7; speeches
14→17; essays 4→9. Approximate total ≈ **69** discovery entries, subject to the 2009 collection-membership
decision.

**Rough route/sitemap impact (precise counts need P1 registry enumeration):** ammaiyappan ≈ 65
(landing + source + 63 scenes); drama ≈ 83 (kagithapoo 25 + manimagudam 49 + thiruvalar 9); short stories
≈ 103 × 2 + 4 collection landings ≈ 210; novels (pudhaiyal/periya-idathup-pen section routes) tens–low
hundreds; essays 5 × (landing + source + articles); poems 8 × (landing + source, more where publications);
speeches ≈ 6. Order of magnitude: **≈ 600–1,000+ new routes / sitemap URLs**, with a comparable
prerender/`.html` increase — the largest single build expansion in the project's history.

---

## FEASIBILITY ASSESSMENT

- READY = **125 works** (22 standalone/publication + 103 short-story members) across **8 source
  repositories** (`kalaignar-cinema-works`, `kalaignar-stage-plays`, `kalaignar-poems`,
  `kalaignar-novels`, `kalaignar-essays`, `kalaignar-assembly-speeches`, `kalaignar-public-speeches`,
  `kalaignar-short-stories`) and **6 Digital Library shelves** (Cinema Writing, Drama, Poetry, Fiction,
  Essays & Articles, Speeches); all reader models already exist.
- The corrected population does not change the shape of the conclusion: the dominant risk remains the
  **103-work short-story partition** and its cross-collection + 1977 duplicate-identity clearance, now
  spread over four new collections.

### Recommendation: **B — ONE WAVE, PARTITIONED INTERNALLY** (unchanged)

One Wave-6 governance programme, implemented P1–P6 as **deterministic per-shelf/family batches**, because
the models exist (onboarding volume, not new architecture) yet 125 works across 6 repos are far too large
for one reviewable PR and the short-story duplicate-identity risk must be cleared collection-by-collection.
Fall back to **C — multiple waves** (short-stories as their own wave) if review/production-acceptance
burden is too high. **A — one monolithic wave — is not recommended.**

Recomputed batch list (each its own exact-head-reviewed, production-verified PR under the one programme):

1. **Cinema** — `ammaiyappan` (payload already QA-PASS in source).
2. **Drama** — `kagithapoo`, `manimagudam`, `thiruvalar-desiyampillai` (qualification documented).
3. **Speeches** — `namathu-nilai`, `idhaya-perikai`, `palli-vazhkkai`.
4. **Poetry** — the 8 release-cleared poems (resolve standalone vs publication per work).
5. **Essays** — the 5 frozen publications.
6. **Fiction / novels** — `periya-idathup-pen`, `pudhaiyal`.
7. **Fiction / short-story collections** — 2008, 2004, 1987, 2009 (four collection batches) + standalone
   `நண்பனா?`, each with duplicate-identity clearance. Largest and highest-risk partition.

Separate owner decisions (not part of this batch list): the **Quotes shelf/reader model** (to lift the
`chinna-chinna-malargal` HOLD) and whether to accept **`ore-mutham`** with its ~21% terminal loss.

## PROPOSED WAVE-6 STAGING (not executed)

**P0** census *(this document)* · **P1** exact per-work source/tree freeze + deterministic payload
foundation (per family batch, incl. short-story duplicate-identity clearance and per-work English/reader
confirmation) · **P2** reader/data generation + per-family validators · **P3** public routes/readers ·
**P4** catalogue/discovery/sitemap integration · **P5** library-wide cross-work/inventory regression
hardening · **P6** production acceptance + final Wave-6 close. Each stage needs its own explicit owner
authorization. **P1 is NOT authorized and has NOT started.**

## Scope confirmation

- **0** implementation-repository changes · **0** source-repository changes · **0** new public routes ·
  **0** new catalogue entries · **0** sitemap change · **0** production change.
- Control-repo documentation only. No onboarding has begun.
- **Wave 6 P1 is NOT authorized and has NOT started.**
