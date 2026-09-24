# Reading Room IA v2 — R1 Canonical Identity & Cross-Witness Reconciliation

**Created:** 2026-09-24.

**Status: READING ROOM IA v2 R1 — IDENTITY RECONCILIATION COMPLETE / REVIEW-READY.**
**R2 — NOT STARTED / NOT AUTHORIZED.**

This record is the durable R1 authority. It is **control-only and assessment-only**:
- implementation delta = **0**;
- source delta = **0**;
- production mutation = **0**.

It creates no LibraryWork and changes no catalogue count, route, reader, sitemap, collection behaviour or `/read`.
Live GitHub and production are authoritative.

Every decision below comes from one of two kinds of evidence:
- the live implementation payloads at the accepted boundary;
- the pinned source repositories, including their own audits, page maps and prefaces.

No title equality is used as identity evidence. No repository placement is used as genre or authorship evidence.

Frozen authority consumed:
- [`READING_ROOM_IA_V2_R0_CENSUS.md`](./READING_ROOM_IA_V2_R0_CENSUS.md) (R0 COMPLETE / REVIEWED / FROZEN). No R0
  decision is reopened.
- Waves 6, 7 and 8 remain COMPLETE / CLOSED / FROZEN at P5.

The machine-readable manifest is [`READING_ROOM_IA_V2_R1_MANIFEST.json`](./READING_ROOM_IA_V2_R1_MANIFEST.json):
- 315 entries;
- the deterministic output of the decisions recorded here.

The deterministic body-text overlap data is in
[`READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json`](./READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json).

---

## 1. Live pins

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base) | `99ce1dbcc724b5daaa1716bd9a9ea90452fc32e0`, tree `5def281955a2f4c693075969421b59ac028ac1ba` (R0 close-out, PR #41) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `f991043c3353abe9f2b334f7c8d57e433184d126`, tree `87ca371b084c337ba2163caa6c336615174074e9`; 0 open PRs; no IA-v2/R1 branch |
| Production | Vercel Production deployment `6638432286` for `f991043c…` (no deploy in R1) |
| Poems source | `pugazg/kalaignar-poems` `969823195ea8943a67fad4286ab1bc7f1c876d56` (tree `e382ee02…`; Wave-4 pin: Kaalap, Kavithaigal, 4 standalones) and `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` (tree `fb35686d…`; = live `main`; 1975, Oruthalaik, 6 standalones) |
| Essays source | `pugazg/kalaignar-essays` at the pins recorded per work: `bff35320…` (சக்கரவர்த்தியின் திருமகன்), `6814e979…` (உணர்ச்சிமாலை, திராவிட சம்பத்து, கயிற்றில்…), `564add70…` (இன முழக்கம், கொலைக்களம், சிந்தனையும் செயலும், …), `b5fd2922…` (ஆறுமாதக் கடுங்காவல், துடிக்கும் இளமை, பெருமூச்சு, விடுதலைக் கிளர்ச்சி, மீசை முளைத்த வயதில், பேசும் கலை வளர்ப்போம்) |
| 1958 தேனலைகள் source | `pugazg/kalaignar-short-stories` `7205a10892d0b208df2617766844f480b6a2c798` (tree `1be34cc3…`), `collections/1958-thenalaigal` tree `44ab41e680d412f94d70a91d4d820ea1b99f85cc` |

All source repositories were read at those commits, read-only.

## 2. Exact scope

**In scope:**

| Workstream | Units |
|---|---|
| R1-A Poetry | 148 candidates = 10 standalone poem works + 58 Kaalap items + 77 Kavithaigal items + 3 active 1975 items |
| 1975 represented ranges | 5 |
| R1-B Essays | 104 titled units in the nine containers |
| R1-C `ina-muzhakkam` | 6 top-level units + the 11 poems inside unit 6 |
| R1-D `meesai-mulaiththa-vayathil` | 26 units + the 1958 `தேனலைகள்` (12 headings) |
| R1-E | a global duplicate/reprint audit over all of the above |

**Out of scope:**
- the R0 keep-one-work exceptions (verified, not reopened);
- Cinema song identity (deferred);
- every R0-preserved Fiction, Speeches, Drama and Literary Commentary work.

## 3. Methodology

1. **Evidence base.** The live Tamil text of every unit was extracted from the accepted implementation payloads.
   This produced 328 candidate texts: 10 standalone poems, 138 publication items, the 11 Oruthalaik sections, 158 essay
   units and the 11 ina poems.
2. **Reference corpora.** Reprints were searched across shelves in:
   - all 154 stories;
   - all 117 speeches;
   - all 8 novels;
   - all 688 Murasoli letters (public 48–54 and the frozen internal 42–47).
3. **Two independent text comparisons.** Normalisation to Tamil letters only is a comparison aid, never authority.
   - **8-character shingle containment** in both directions, plus the **longest contiguous shared passage**. A pair is
     significant when the shared passage is at least 150 normalised characters. The measured noise ceiling across 1,054
     overlapping pairs was 149. Short poems were also checked by high-coverage rules.
   - **Word-bigram coverage** in both directions (≥ 0.25).
   - The two methods produced the **same relationship set**. A targeted 6-gram sweep of Meesai against the stories found
     nothing new.
4. **Qualitative inspection.** Every significant pair was inspected: printed headings, dates and occasions, openings and
   closings, verbatim-line counts, and the direction of containment.
5. **Source documents.** Identity, dating and authorship were settled from the source repositories' own records:
   - the Wave-4 cross-witness audit and its 2026-09-06 addendum;
   - the 1968 `விடுதலை வீரர்கள் ஐவர்` audit;
   - the 1975 page-map;
   - the குணநாயகர் நேரு boundary audit;
   - the Meesai author preface (என்னுரை, 19.5.2002);
   - the 1958 தேனலைகள் intake;
   - the உணர்ச்சிமாலை publication-source note;
   - the Bharathiar University secondary-witness crosswalk. It is external English and corroborative only.
6. **Relationship vocabulary.**

| Relationship | Meaning |
|---|---|
| SAME-CANONICAL alternate witness | the same work in another printing |
| SHARED_PASSAGE | distinct works that reuse lines |
| QUOTATION | one work quotes a few lines of another |
| EXCERPT | a later shorter text is contained in a longer one |
| SOURCE_LIMITED | cannot be decided from the available text |

## 4. Poetry reconciliation (R1-A)

| Family | Candidates | CREATE | ADD_WITNESS | KEEP_EXISTING | HOLD |
|---|---:|---:|---:|---:|---:|
| Standalone poem works | 10 | — | 2 | 8 | — |
| Kaalap (2006) | 58 | 57 | — | — | 1 |
| Kavithaigal (1995 4th ed.) | 77 | 72 | 3 | — | 2 |
| 1975 active items | 3 | 3 | — | — | — |
| **Total** | **148** | **132** | **5** | **8** | **3** |

**Same-canonical relationships established** (body-text + source evidence):

| Canonical work | Alternate witness | Status | Evidence |
|---|---|---|---|
| `idhayathai-thanthidu-anna` (existing) | Kavithaigal item 01 | already live | Wave-4 audit; overlap 0.95/0.94 |
| `idhayathai-thanthidu-anna` | 1975 scans 9–20 `எம் அண்ணா — இதய மன்னா!` | **NEW** | 1975 page-map "existing Anna witness"; text 0.945/0.940 |
| `thennan-kathai` (existing) | Kavithaigal item 02 | already live | Wave-4 audit; 0.95/0.95 |
| `gunanayagar-nehru` (existing) | Kavithaigal item 19 `நேரு கண்ட ஜனநாயகம்` | **NEW** | see note 1 below |
| `gunanayagar-nehru` | 1975 scans 21–32 (`நேரு பிறந்தநாள் கவியரங்கில் … 14-11-70`) | **NEW** | 1975 page-map "existing Nehru witness"; text 0.87 with item 19 |
| new ← Kavithaigal 06 `விடுதலை வீரர்கள்` | 1975 scans 71–77; external 1968 `விடுதலை வீரர்கள் ஐவர்` | NEW / audited | 1975 page-map; source 1968 audit PASS (external, not onboarded) |
| new ← Kavithaigal 17 `வாழ்வெனும் பாதையில்` | 1975 scans 33–45 | NEW | 1975 page-map (pages untranscribed; source-declared) |
| new ← Kavithaigal 26 `தந்தை பெரியார்` | 1975 scans 78–84 | NEW | 1975 page-map (source-declared) |
| new ← Kavithaigal 39 `பன்னீர்ச்செல்வமே!` | உணர்ச்சிமாலை unit 10 `கவிதையல்ல - கண்ணீர்க்கடல் !` (1951) | NEW | see note 2 below |
| new ← Kavithaigal 49, 50, 51, 53, 54, 55 | இன முழக்கம் (1951) poems 6.1, 6.2, 6.3, 6.11, 6.9, 6.10 | NEW | overlap 0.81–1.00. 6.3 `சைவரே!` = 51 `புயல் என அறிக!` has a different title but the same body |

Notes:
1. **`gunanayagar-nehru` ← Kavithaigal item 19.**
   - The booklet's own performance note reads `(முதல்வர் கலைஞர் அவர்கள் 14.11.1970-ல் ... கவிதை.)`, which is the same
     occasion as item 19's heading (14.11.1970, the Chennai Nehru kaviyarangam).
   - The two share the same opening and closing, and 118 of the booklet's 170 lines appear verbatim in item 19.
2. **Kavithaigal item 39 ← உணர்ச்சிமாலை unit 10.** Both are the same A.T. Panneerselvam elegy, with the same
   opening and closing and 22 lines verbatim.

**Shared passages between distinct works** (recorded, not merged):
- *பூமுடி* (1965) → *அண்ணா கவியரங்கம்* (1968) → *இதயத்தைத் தந்திடு அண்ணா* (1969).
- Kavithaigal 41 (Anna 75th anniversary) → *அணையா விளக்கு அண்ணா* (dated 15-9-2008).
- Kavithaigal 14 (8.12.68, Bombay) ↔ 1975 item 01 (29-4-71, Puducherry). The printed occasions differ, and about 23% of
  lines are shared.
- Inside Kavithaigal: 16↔64, 23/26/30↔32 and 28↔35 (12 shared lines).

**Quotations:**
- Kavithaigal 06 and Kaalap 52 quote lines of the 1951 poem *மாணவர் எழுச்சி*.
- Murasoli letter `m49-l3775` quotes Kavithaigal 45.
- `m51-l3912` quotes Kavithaigal 53.
- `m49-l3807` quotes *பூமுடி*.

**HOLD (3):**
- **Kaalap 37 `அன்பால் அவனை விலைகொள்ள முடியுமோ?` (2006).** It reprints about 60% of *ஒருதலைக் காதல்* section 1
  (1998 verse novel): 100 of 167 lines verbatim, overlap 0.88/0.89.
- **Kavithaigal 52 `கேட்டுண்டோ?`.** It equals ina 6.5 and 6.6 combined.
- **Kavithaigal 56 `பச்சைக் கிளி`.** It equals Meesai 14 and is also the existing Fiction work *சிறை கொடியது*.

**Authorship.** Every Poetry candidate belongs to a Kalaignar-authored publication. The only non-Kalaignar material in
scope is 1975 ordinal 03 (Rajaji, scan 66) and scans 69–70 (Bharathidasan). Both are already excluded, and neither is
reintroduced.

## 5. 1975 represented-range mapping

All 84 scans are accounted for by the source's own `indexes/page-map.md`. Ranges 9–32 were verified against their
transcribed page records.

| Scans | Source classification | Canonical identity | Verification |
|---|---|---|---|
| 9–20 | existing Anna witness | `idhayathai-thanthidu-anna` (existing) | text: range ⊂ work 0.945, work ⊂ range 0.940 |
| 21–32 | existing Nehru witness (14-11-70) | `gunanayagar-nehru` (existing), with Kavithaigal 19 | text: 0.87 with item 19; 0.92 of the booklet inside the range |
| 33–45 | existing `வாழ்வெனும் பாதையில்` witness | new work from Kavithaigal 17 | source-declared (pages not transcribed) |
| 71–77 | existing `விடுதலை வீரர்கள்` | new work from Kavithaigal 06 | source-declared |
| 78–84 | existing `தந்தை பெரியார்` | new work from Kavithaigal 26 | source-declared |

**None of the five ranges corresponds to items 01, 02 or 04**, so all three are CREATE.

The ranges do **not** correspond to "the 10 standalone poems" in general:
- two map to existing standalone works;
- three map to Kavithaigal items that R1 promotes.

## 6. Essays 104-unit reconciliation (R1-B)

| Container | Units | CREATE | ADD_WITNESS | DO_NOT_PROMOTE | HOLD | Basis |
|---|---:|---:|---:|---:|---:|---|
| `sakkaravarththiyin-thirumagan` | 14 | — | — | 14 | — | note 1 |
| `unarchchimaalai` | 10 | 9 | 1 | — | — | unit 10 is the verse elegy witness of Kavithaigal 39; the book's printed note says the pieces first appeared in "முரசொலி", "மாலைமணி" |
| `thiraavida-sampaththu` | 2 | 2 | — | — | — | independent units; unit 1 title equals the publication title |
| `kolaikkalam` | 6 | 6 | — | — | — | independent units |
| `sinthanaiyum-seyalum` | 50 | 48 | — | — | 2 | note 2 |
| `aaru-maatha-kadungkaaval` | 3 | — | — | 3 | — | note 3 |
| `thudikkum-ilamai` | 4 | 1 | 2 | — | 1 | note 4 |
| `perumoochu` | 13 | 13 | — | — | — | independent political articles |
| `viduthalai-kilarcci` | 2 | — | — | 2 | — | note 5 |
| **Total** | **104** | **79** | **3** | **19** | **3** | |

Notes:
1. **`sakkaravarththiyin-thirumagan` — DEPENDENT_SECTION.** The 14 units are **serial installments** of one rebuttal of
   Rajaji's *Kalki* serial.
   - Unit 1 announces the series.
   - Unit 3 argues from `சென்ற இதழில்`.
   - 12 of the 14 carry issue or chapter cross-references, and they follow the Ramayana order.
   - Decision: keep it as one work.
2. **`sinthanaiyum-seyalum`.**
   - Units 1 and 2 are letter-form (`உடன்பிறப்பே,`), which raises a shelf question.
   - Unit 26 shares a passage with three later Murasoli letters (SHARED_PASSAGE). It remains distinct.
   - The "தொடரும்/தொடர்ச்சி" hits in this book are ordinary words, not serial markers.
3. **`aaru-maatha-kadungkaaval` — DEPENDENT_SECTION.** Its three parts form one continuous 1953 prison narrative, and
   unit 3 opens mid-sentence.
4. **`thudikkum-ilamai`.**
   - Unit 1 is a delivered speech, which raises a shelf question (HOLD).
   - Unit 2 is an essay (CREATE).
   - Units 3 and 4 are section-level witnesses of the **existing** speech work *இதய பேரிகை*, sections
     `பூம்புகார் மாநாடு.` and `வெற்றி விளக்கு!` (ADD_WITNESS).
5. **`viduthalai-kilarcci` — DEPENDENT_SECTION.** Unit 1 is a prologue ending
   `இது வேங்கையை விரட்டும் படலத்திற்கு அடுத்த படலம்…`.

**Authorship.**
- Every container prints Kalaignar as author.
- Every unit is predominantly `authored-text`. 139 of the 158 essay units contain `quoted-text` segments; these are quotations embedded
  in his prose, not third-party units.
- No unit was found to be contributed or third-party.

**Title collisions.** Unit title equals the publication title in:
- `ina-muzhakkam` 1;
- `thiraavida-sampaththu` 1;
- `kolaikkalam` 1;
- `perumoochu` 1;
- `thudikkum-ilamai` 1 (HOLD);
- `unarchchimaalai` 1 (spacing variant);
- `sakkaravarththiyin-thirumagan` 1 (not promoted);
- `viduthalai-kilarcci` 2 (not promoted).

Canonical work ids are kept distinct from publication ids (§12).

## 7. `ina-muzhakkam` (R1-C)

The source is `TVA_BOK_0063958`, first edition September 1951 (முன்னேற்றப் பண்ணை), authored by Kalaignar.

**Top-level units:**

| Unit | Decision |
|---|---|
| 1 `இன முழக்கம்` | **CREATE** (title-collision rule applies) |
| 2 `சொர்க்க லோகத்தில்` | **HOLD** — see below |
| 3 `முரசறைவாய்` | **CREATE** |
| 4 `பழிக்குப் பழி` | **CREATE** |
| 5 `ஆரியம் பேசுகிறது` | **CREATE** |
| 6 `கவிதைகள்` | **DO_NOT_PROMOTE** — a container heading, not a work |

Unit 2 contains 90% of the existing Fiction work `சொர்க்கத்திற்கு வந்தது எப்படி?` (2004 anthology), a later
re-edited shorter text.

**Unit-6 poems:**

| Poem | Decision |
|---|---|
| 6.1 நியாயத் திராசு! | ADD_WITNESS → Kavithaigal 49 |
| 6.2 ஏற்பரோ! | ADD_WITNESS → 50 |
| 6.3 சைவரே! | ADD_WITNESS → 51 `புயல் என அறிக!` |
| 6.4 வா! | **CREATE** — no match anywhere |
| 6.5 பொதுவுடைமையே! | **HOLD** — with Kavithaigal 52 |
| 6.6 யோசித்துப் பார்! | **HOLD** — wholly inside Kavithaigal 52 |
| 6.7 மாணவர் எழுச்சி. | **CREATE** — see note 1 |
| 6.8 வாளிங்கே! | **CREATE** — see note 2 |
| 6.9 தோல்வி எப்பொழுது? | ADD_WITNESS → 54 |
| 6.10 இன்னுமா கூச்சல்? | ADD_WITNESS → 55 |
| 6.11 வருணமா? மரணமா? | ADD_WITNESS → 53 (dated 1944 in the author's 2002 preface) |

Notes:
1. **6.7.** It is quoted in Kavithaigal 06 and Kaalap 52. BU *Shower of Poetry* I entry 4, "Students' Awakening!"
   (1945), corresponds at title level only.
2. **6.8.** The 1977 story *சந்தனக்கிண்ணம்* quotes 15 lines. The author's 2002 preface names this long poem
   `புறநானூற்றுத் தாய்` (1945, குடியரசு). That alternate title is recorded, and the printed heading is retained.

**Result:** 7 new works (4 essays, 3 poems), 6 witnesses, 3 HOLD and 1 not promotable.

## 8. `மீசை முளைத்த வயதில்` and the 1958 `தேனலைகள்` (R1-D)

**Bibliographic facts from the source:**
- 1st edition 3.6.2002, 2nd edition October 2006 (தமிழ்க்கனி பதிப்பகம்).
- The author's preface (என்னுரை, dated 19.5.2002) describes the book as a compilation of his youthful writings:
  - 1942 onward;
  - poems of the 1940s, quoting the openings of ina 6.11, 6.8 and 6.1;
  - pieces "written in Trichy prison during the 1953 six-month sentence and after release", which "ஏற்கனவே தனித்தனி
    நூல்களாக வெளிவந்துள்ளன; பல பதிப்புகளாக".
- He calls them `எழுத்தோவியங்கள்`.
- The essays-repository location is **not** genre evidence.

**Literary form (from the text):**

| Units | Form |
|---|---|
| 1–10 | lyrical prose-poems (apostrophic prose paragraphs) |
| 11 | dialogue prose-poem |
| 12, 15 | rhapsodic prose-poems |
| 13 | aphoristic prose-poem |
| 14 | verse poem |
| 16–26 | narrative rhythmic-prose pieces with dialogue |

The narrow-column lineation of 11–26 is typesetting: lines break mid-sentence. It is not verse.

**Cross-shelf identity (existing Fiction LibraryWorks from the 2004 anthology `கலைஞரின் குட்டிக் கதைகள்`).** Each
2004 story is a shorter, re-edited text contained in the Meesai unit:

| Meesai unit | Contains existing Fiction work | Share of the story inside the unit |
|---|---|---|
| 1 `பிறையே` | `நீயும் கைதி - நானும் கைதி` | 91–93% |
| 2 `ஆடிக்காற்று` | `ஆடிக் காற்றே!` | 93–95% |
| 13 `புகழ்` | `புகழே நீ ஒரு புதிர்` | 98% |
| 14 `பச்சைக்கிளி` | `சிறை கொடியது` (and = Kavithaigal 56) | 72–78% |

**1958 `தேனலைகள்`.** The source is `TVA_BOK_0064030`: December 1958, 12 `அலை` pieces, image-only and **untranscribed**.

| 1958 heading | Relationship to Meesai (not text-verified) |
|---|---|
| அலை 1 முத்தாரம் | indicated → unit 16 `தேனலைகள்`, which closes `பின்னர் இரவெல்லாம் முத்தாரம் தொடுத்தார்`; extent fits |
| அலை 2 மயிலிறகு | title → unit 26 |
| அலை 3 முத்துமாலை | **no proven counterpart** |
| அலை 4 மடல் | title → unit 24 |
| அலை 5–11 தோழி … சேவல் சண்டை | title **and exact consecutive order** → units 17–23 |
| அலை 12 ஆண்டு விழா | title → unit 25 |

- Extents are consistent for the 10 title pairs: about 556–776 Meesai characters per 1958 printed page.
- **No body text of the 1958 book is available, so no heading is labelled an alternate witness.** The relationship
  is probable one-to-one for 10 headings, indicated for முத்தாரம், and unproven for முத்துமாலை.
- The short-story repository's classification of the 1958 pieces is not controlling.

**Meesai decisions: all 26 HOLD.**

| Units | Blocker |
|---|---|
| 1, 2, 13, 14 | cross-shelf identity with existing Fiction works (and Kavithaigal 56) |
| 16–26 | 1958 relationship SOURCE_LIMITED; shelf also undecided |
| 3–12, 15 | identity cleared (no duplicate anywhere in the library); **shelf decision pending** |

The 11 units 3–12 and 15 are therefore "promotable on a shelf decision": once the owner fixes the shelf for prose-poems,
they can be created. **Promotable now: 0. Shelf distribution: undecided.**

## 9. Authorship findings

- **Poetry.** All candidates are Kalaignar's. The only excluded material is Rajaji (1975 ordinal 03) and Bharathidasan
  (1975 scans 69–70).
- **Essays and ina.** All containers print Kalaignar as author. No third-party or contributed unit was found.
  Embedded quotations are not units.
- **Meesai.** The author's own preface attributes the pieces to himself.
- **The 1958 book** prints `கலைஞர் மு. கருணாநிதி M.L.A`.
- Nothing is attributed from repository placement.

## 10. Duplicate / reprint / witness findings (R1-E)

**Cross-shelf findings that do not change any R0-preserved work:**
- *பேசும் கலை வளர்ப்போம்* section 6 contains 96% of the existing Fiction work *நடக்குமா நடக்காதா?* (2008
  anthology). This is an EXCERPT relation; pesum stays one work and no action is taken.
- The four Meesai ↔ 2004-anthology relations and ina 2 ↔ 2004-anthology are HOLD.
- *துடிக்கும் இளமை* 3 and 4 ↔ *இதய பேரிகை* sections are ADD_WITNESS.

**Within and across publications:** see §4. There is no duplicate among the 57 Kaalap CREATE items, the 72 Kavithaigal
CREATE items, the 79 Essays CREATE units, or the 7 ina CREATE units.

## 11. Unresolved HOLD items (35)

| # | Item(s) | Question for the owner |
|---:|---|---|
| 1 | Kaalap 37 ↔ ஒருதலைக் காதல் §1 | Is a verse-novel section reprinted standalone under its own title a separate canonical poem, or a witness of the verse novel? |
| 2 | Kavithaigal 52 + ina 6.5 + ina 6.6 | One poem (1995) or two poems (1951)? |
| 3 | Kavithaigal 56 + Meesai 14 + Fiction `சிறை கொடியது` | One canonical work across Poetry and Fiction? Which shelf? |
| 4 | Meesai 1, 2, 13 + Fiction `நீயும் கைதி…`, `ஆடிக் காற்றே!`, `புகழே நீ ஒரு புதிர்` | Is the 2004 story a witness of the Meesai piece (merge), or a separate work? |
| 5 | ina 2 + Fiction `சொர்க்கத்திற்கு வந்தது எப்படி?` | same question as 4 |
| 6 | Meesai 16–26 (11) + 1958 தேனலைகள் | Needs 1958 transcription or visual comparison, plus a shelf decision |
| 7 | Meesai 3–12, 15 (11) | Shelf for lyrical prose-poems (`எழுத்தோவியம்`): Poetry, Essays or Fiction? |
| 8 | sinthanaiyum 1, 2 | Letter-form pieces in an essay book: Essays or Letters? |
| 9 | thudikkum 1 | A delivered speech in an essay booklet: Essays or Speeches? |

That is 35 HOLD units in total: 3 Poetry, 2 ina poems, 1 ina prose, 3 Essays and 26 Meesai.

## 12. Reusable canonical-identity rules

1. **Promotion.** A unit may become a canonical LibraryWork only when all of these hold:
   - it has an independently printed, source-supported identity (its own heading or title);
   - its boundaries are source-supported;
   - its authorship is established;
   - it is independently meaningful and readable;
   - it is **not** an installment, part, prologue or numbered section of one coherent work (serial back-references,
     mid-sentence openings and "next chapter" closings are dependency evidence);
   - duplicate, reprint and witness reconciliation has completed against **all** shelves.
2. **Multiple witnesses.** Editions, anthology appearances, standalone-plus-anthology printings, textual variants and
   translations are witnesses and provenance of **one** work, never duplicate LibraryWorks. Witness text is never
   reconciled or normalised across witnesses.
3. **Identity versus title.**
   - Title equality is never identity.
   - Title inequality is never non-identity (e.g. `சைவரே!` = `புயல் என அறிக!`).
   - Identity requires body text **plus** source or bibliographic evidence (printed occasion and date, audit records).
4. **Shared passage is not identity.** Distinct dated occasions that reuse lines stay distinct works, and the reuse is
   recorded as SHARED_PASSAGE. Short quotations are recorded as QUOTATION.
5. **Publication/container versus work.** A publication and one of its units may share a title, but their identities
   are never conflated. A promoted unit whose slug collides with an existing id gets a deterministic suffix: `-katturai`
   for essays and `-kavithai` for poems.
6. **Existing routes.** No publication-unit route is destroyed because the unit gains canonical identity. Later
   implementation keeps it as a witness or publication route, or as an alias.
7. **Cross-shelf identity** (a Poetry, Essays or Meesai unit whose text is an existing Fiction or Speeches work) is
   never resolved by creating a new work. It is either a witness of the existing work or an explicit owner decision.
8. **Source-limited sources** (untranscribed, image-only) never ground an alternate-witness label. Title, sequence and
   extent evidence is recorded as indicative only.

## 13. Final R1 promotion manifest

Every row below is also in `READING_ROOM_IA_V2_R1_MANIFEST.json`.
- Decisions are `CREATE`, `KEEP_EXISTING`, `ADD_WITNESS`, `DO_NOT_PROMOTE` or `HOLD`.
- Proposed ids for CREATE are the unit's existing public slug, with the collision rule in §12 applied. Exactly 4
  collisions were resolved: `ina-muzhakkam-katturai`, `kolaikkalam-katturai`, `perumoochu-katturai`,
  `thiraavida-sampaththu-katturai`.
- All 218 proposed ids are unique.
- English titles are the existing project-created titles.

#### Poetry — 10 existing standalone poems

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
|  | **KEEP_EXISTING** | existing `aanthaiyum-arasanum` | ஆந்தையும் அரசனும்! | Andhai and the King! | poetry / poem | aanthaiyum-arasanum (standalone) | UNIQUE_CANONICAL_POEM |  | existing canonical standalone poem; no identity overlap found |
|  | **KEEP_EXISTING** | existing `anaiya-vilakku-anna` | அணையா விளக்கு அண்ணா | Anna, the Inextinguishable Lamp | poetry / poem | anaiya-vilakku-anna (standalone) | UNIQUE_CANONICAL_POEM |  | 2008 (15-9-2008) presiding poem reuses 36 of 67 lines of Kavithaigal item 41 (Anna 75th-anniversary poem); distinct works — SHARED_PASSAGE |
|  | **KEEP_EXISTING** | existing `anna-kaviyarangam` | அண்ணா கவியரங்கம் | Anna Kaviyarangam | poetry / poem | anna-kaviyarangam (standalone) | UNIQUE_CANONICAL_POEM |  | shares 68 lines with இதயத்தைத் தந்திடு அண்ணா and reuses பூமுடி; distinct dated works — SHARED_PASSAGE |
|  | **ADD_WITNESS** | existing `gunanayagar-nehru` | குணநாயகர் நேரு | Nehru, the Noble Leader | poetry / poem | gunanayagar-nehru (standalone) | UNIQUE_CANONICAL_POEM | kalaignarin-kavithaigal item 19 (democracy-as-nehru-saw-it) [NEW]; kalaignarin-kaviyaranga-kavithaigal-1975 scans 21–32 ('நேரு பிறந்தநாள் கவியரங்கில் … 14-11-70') [NEW] | existing canonical standalone poem; no identity overlap found |
|  | **ADD_WITNESS** | existing `idhayathai-thanthidu-anna` | இதயத்தைத் தந்திடு அண்ணா | Lend Me Your Heart, Anna | poetry / poem | idhayathai-thanthidu-anna (standalone) | UNIQUE_CANONICAL_POEM | kalaignarin-kavithaigal item 01 (give-me-your-heart-anna) [already live (POETRY_WITNESS_RELATIONS)]; kalaignarin-kaviyaranga-kavithaigal-1975 scans 9–20 ('எம் அண்ணா — இதய மன்னா!') [NEW] | existing canonical standalone poem; no identity overlap found |
|  | **KEEP_EXISTING** | existing `kanchithan-annan` | காஞ்சிதான் அண்ணன் | Kanchi Is Anna | poetry / poem | kanchithan-annan (standalone) | UNIQUE_CANONICAL_POEM |  | existing canonical standalone poem; no identity overlap found |
|  | **KEEP_EXISTING** | existing `marathi` | மறத்தி | The Valiant Woman | poetry / poem | marathi (standalone) | UNIQUE_CANONICAL_POEM |  | existing canonical standalone poem; no identity overlap found |
|  | **KEEP_EXISTING** | existing `poomudi` | பூமுடி | Flower Crown | poetry / poem | poomudi (standalone) | UNIQUE_CANONICAL_POEM |  | its 24 lines are reused inside அண்ணா கவியரங்கம் (1968) and இதயத்தைத் தந்திடு அண்ணா (1969); distinct dated works — SHARED_PASSAGE, not witness |
|  | **KEEP_EXISTING** | existing `thalaikettan-thambi` | தலைகேட்டான் தம்பி | The Younger Brother Who Asked for a Head | poetry / poem | thalaikettan-thambi (standalone) | UNIQUE_CANONICAL_POEM |  | existing canonical standalone poem; no identity overlap found |
|  | **KEEP_EXISTING** | existing `thennan-kathai` | தென்னவன் காதை | தென்னவன் காதை | poetry / poem | thennan-kathai (standalone) | UNIQUE_CANONICAL_POEM | kalaignarin-kavithaigal item 02 (the-tale-of-the-southerner) [already live] | existing canonical standalone poem; no identity overlap found |

#### Poetry — காலப் பேழையும் கவிதைச் சாவியும் (58)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `the-common-world` | பொது உலகம் | The Common World | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 01 (2006) (10–11) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 2 | **CREATE** | `stagewise-development` | படிமுறை வளர்ச்சி | Stagewise Development | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 02 (2006) (12–15) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 3 | **CREATE** | `a-story-of-the-magnet-stone` | ‘காந்தக்கல்’ கதையொன்று! | A Story of the ‘Magnet Stone’! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 03 (2006) (16–19) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 4 | **CREATE** | `the-stone-age-that-was-a-better-age-if-it-does-not-return` | அன்றிருந்த கற்காலம் - இனி அமையாவிடின் நற்காலம்! | The Stone Age That Was — A Better Age If It Does Not Return! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 04 (2006) (20–24) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 5 | **CREATE** | `we-need-a-heart-of-gold-we-need-the-love-it-gives` | தங்க மனம் வேண்டும்; அது தந்திடும் அன்பு வேண்டும்! | We Need a Heart of Gold; We Need the Love It Gives! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 05 (2006) (25–28) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 6 | **CREATE** | `the-knife-belongs-to-the-enemy-the-blood-is-what-we-give` | கத்தி பகைவுடையது; இரத்தம் நாம் தருவது! | The Knife Belongs to the Enemy; The Blood Is What We Give! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 06 (2006) (29–34) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 7 | **CREATE** | `the-form-of-an-age-in-history` | வரலாற்றுக் காலத்தின் கோலம்! | The Form of an Age in History! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 07 (2006) (35–39) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 8 | **CREATE** | `sweat-falling-from-the-brow-the-ribcage-breaking` | நெற்றி வியர்வை உதிர; நெஞ்செலும்பு ஒடிய! | Sweat Falling from the Brow; the Ribcage Breaking! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 08 (2006) (40–43) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 9 | **CREATE** | `what-truth-does-the-conversation-reveal` | உரையாடல் உணர்த்திடும் உண்மை என்ன? | What Truth Does the Conversation Reveal? | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 09 (2006) (44–49) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 10 | **CREATE** | `the-ancient-tamils-international-connections` | பழந்தமிழர் பன்னாட்டுத் தொடர்பு! | The Ancient Tamils' International Connections! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 10 (2006) (50–53) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 11 | **CREATE** | `marks-of-identity-here-and-there` | ஆங்காங்கு அடையாள முத்திரைகள்! | Marks of Identity Here and There! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 11 (2006) (54–57) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 12 | **CREATE** | `valli-s-marriage-in-the-garden-of-history` | வரலாற்றுப் பூங்காவில் வள்ளித் திருமணம்! | Valli's Marriage in the Garden of History! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 12 (2006) (58–63) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 13 | **CREATE** | `the-unbroken-alliance-that-made-kharavela-tremble` | காரவேலன் கண்டு நடுங்கிய கட்டுக்குலையாக் கூட்டணி! | The Unbroken Alliance That Made Kharavela Tremble! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 13 (2006) (64–67) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 14 | **CREATE** | `the-history-of-kanaka-and-vijaya-carrying-the-stone` | கனக விஜயர் கல் சுமந்த வரலாறு! | The History of Kanaka and Vijaya Carrying the Stone! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 14 (2006) (68–77) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 15 | **CREATE** | `let-us-drink-this-aryan-tea` | பருகிடலாம் இந்த “ஆரிய” தேநீரை! | Let Us Drink This “Aryan” Tea! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 15 (2006) (78–81) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 16 | **CREATE** | `as-a-flavour-united-within-the-segment` | சுளையில் ஒன்றியிருக்கும் சுவையாக! | As a Flavour United Within the Segment! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 16 (2006) (82–87) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 17 | **CREATE** | `from-where-is-world-history-to-come` | உலக வரலாறு எங்கிருந்து வருவது? | From Where Is World History to Come? | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 17 (2006) (88–95) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 18 | **CREATE** | `we-seek-what-remains-after-the-rubbing-away` | தேய்ந்தது போக மிச்சத்தைத் தேடுகின்றோம்! | We Seek What Remains After the Rubbing Away! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 18 (2006) (96–98) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 19 | **CREATE** | `a-historical-event-to-grieve-over` | வருந்தத்தக்க வரலாற்று நிகழ்ச்சி! | A Historical Event to Grieve Over! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 19 (2006) (99–102) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 20 | **CREATE** | `even-in-falling-he-is-victory-s-favoured-son` | வீழினும் அவன் வெற்றித் திருமகனே! | Even in Falling, He Is Victory's Favoured Son! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 20 (2006) (103–106) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 21 | **CREATE** | `where-culture-is-maimed-they-would-not-even-wish-to-look` | பண்பாட்டுக்கு ஊனம் எனில் பார்க்கவும் விரும்பார்! | Where Culture Is Maimed, They Would Not Even Wish to Look! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 21 (2006) (107–111) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 22 | **CREATE** | `why-then-the-question-that-is-my-question` | “பிறகேன் வினா? என்பதே என் வினா!” | “Why, Then, the Question? — That Is My Question!” | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 22 (2006) (112–116) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 23 | **CREATE** | `kundalakesi-who-speaks-the-strength-of-feminism` | பெண்ணியத்தின் திண்மை கூறும் குண்டலகேசி! | Kundalakesi, Who Speaks the Strength of Feminism! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 23 (2006) (117–119) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 24 | **CREATE** | `this-tamil-land-two-thousand-years-ago` | ஈராயிரம் ஆண்டின் முன்னே இந்தத் தமிழ் நிலம்! | This Tamil Land, Two Thousand Years Ago! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 24 (2006) (120–123) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 25 | **CREATE** | `kannagi-s-emphasis-on-culture` | கலாச்சாரத்தின்மீது கண்ணகி காட்டிய அழுத்தம் | Kannagi's Emphasis on Culture | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 25 (2006) (124–127) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 26 | **CREATE** | `awake-here-is-the-dawn-of-a-classical-language` | விழித்தெழுக; இதோ செம்மொழி விடியல்! | Awake; Here Is the Dawn of a Classical Language! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 26 (2006) (128–131) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 27 | **CREATE** | `it-will-surely-be-opened-to-show-the-way` | வழிகாட்டும் வண்ணம்; திறக்கப்படுவது திண்ணம்! | It Will Surely Be Opened, to Show the Way! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 27 (2006) (132–135) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 28 | **CREATE** | `the-ancient-civilisation-that-spread-across-the-whole-world` | பார் முழுதும் பரவிய பழம்பெரும் நாகரிகம்! | The Ancient Civilisation That Spread Across the Whole World! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 28 (2006) (136–139) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 29 | **CREATE** | `mother-give-us-bear-us-treasures-of-self-respect` | தாயே தந்திடு எமக்கு தன்மானச் செல்வங்களை ஈன்று! | Mother, Give Us — Bear Us Treasures of Self-Respect! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 29 (2006) (140–144) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 30 | **CREATE** | `the-measure-of-his-power-his-just-sceptre` | ஆற்றலின் அளவுகோல்; அவன் செங்கோல்! | The Measure of His Power: His Just Sceptre! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 30 (2006) (145–147) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 31 | **CREATE** | `the-mother-full-of-dignity-and-the-stainless-son` | மாண்பு நிறை தாயும் மாசற்ற மகனும்! | The Mother Full of Dignity and the Stainless Son! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 31 (2006) (148–151) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 32 | **CREATE** | `kovoorar-questions-heads-bow-down` | கோவூரார் கேள்வியுறும் - குனிந்திடும் தலையுறும் | Kovoorar Questions — Heads Bow Down | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 32 (2006) (152–156) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 33 | **CREATE** | `is-seruppaazhi-erindha-an-honorific-title` | “செருப்பாழி எறிந்த” என்பது சிறப்புப் பட்டமா? | Is “Seruppaazhi-Erindha” an Honorific Title? | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 33 (2006) (157–160) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 34 | **CREATE** | `it-did-not-vanish-it-was-reborn` | மறையவில்லை; மறுமலர்ச்சி பெற்றது! | It Did Not Vanish; It Was Reborn! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 34 (2006) (161–166) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 35 | **CREATE** | `a-noble-friendship-higher-than-life-itself` | உயிரினும் மேலான உயர்ந்த நட்பு! | A Noble Friendship Higher Than Life Itself! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 35 (2006) (167–172) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 36 | **CREATE** | `he-is-young-he-is-a-son-of-tamil` | இளையவன்; அவன் ஒரு தமிழ் மகன்! | He Is Young; He Is a Son of Tamil! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 36 (2006) (173–178) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 37 | **HOLD** | — | அன்பால் அவனை விலைகொள்ள முடியுமோ? | Can He Be Bought with Love? | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 37 (2006) (179–185) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | 2006 item reprints ~60% of ஒருதலைக் காதல் section 1 (1998 verse novel): 100/167 lines verbatim, body overlap 0.88/0.89 — is an excerpted section of a verse novel, reprinted standalone under its own title, a separate canonical poem or a witness of the verse novel's section? owner decision |
| 38 | **CREATE** | `he-who-lives-in-the-hearts-of-the-grateful` | நன்றியுடையோர் நெஞ்சில் வாழ்வோன்! | He Who Lives in the Hearts of the Grateful! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 38 (2006) (186–190) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 39 | **CREATE** | `not-one-who-came-on-his-own-one-brought-by-the-commander` | தானாக வந்தவரல்ல; தளபதியால் கொண்டுவரப்பட்டவர்! | Not One Who Came on His Own; One Brought by the Commander! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 39 (2006) (191–194) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 40 | **CREATE** | `the-tenderness-and-compassion-shown-by-the-soil-of-kanchi` | காஞ்சி மண் காட்டிய கனிவும் கருணையும் | The Tenderness and Compassion Shown by the Soil of Kanchi | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 40 (2006) (195–199) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 41 | **CREATE** | `let-us-protect-it-the-pallava-capital` | பாதுகாப்போம்; பல்லவர் தலைநகரம்! | Let Us Protect It: The Pallava Capital! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 41 (2006) (200–203) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 42 | **CREATE** | `the-charters-proclaim-it` | பட்டயங்கள், பறைசாற்றுகின்றன! | The Charters Proclaim It! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 42 (2006) (204–206) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 43 | **CREATE** | `the-tamil-tradition-of-the-dravidian-race` | திராவிட இனத்தின் தமிழர் மரபு! | The Tamil Tradition of the Dravidian Race! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 43 (2006) (207–210) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 44 | **CREATE** | `the-iron-pillar-and-the-wings-of-flies` | இரும்புத் தூணும் ஈக்களின் இறகும்! | The Iron Pillar and the Wings of Flies! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 44 (2006) (211–215) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 45 | **CREATE** | `father-rajaraja-and-the-son-who-captivated-hearts` | தந்தை இராசராசனும், சிந்தை கவர்ந்த செல்வனும்! | Father Rajaraja and the Son Who Captivated Hearts! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 45 (2006) (216–219) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 46 | **CREATE** | `the-three-crowned-chola-who-stood-as-a-model` | முன்மாதிரியாகத் திகழ்ந்த மும்முடிச் சோழன்! | The Three-Crowned Chola Who Stood as a Model! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 46 (2006) (220–225) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 47 | **CREATE** | `that-future-age-will-be-a-precious-age` | அந்த வருங்காலமே; அருங்காலமாகும்! | That Future Age Will Be a Precious Age! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 47 (2006) (226–235) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 48 | **CREATE** | `the-undying-art-of-sculpture-and-the-beautiful-art-of-painting` | அழியாத சிற்பக் கலையும், அழகிய ஓவியக் கலையும்! | The Undying Art of Sculpture and the Beautiful Art of Painting! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 48 (2006) (236–240) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 49 | **CREATE** | `they-saw-many-battlefields-they-won-in-naval-war-too` | களம் பல கண்டனர்; கடற்போரிலும் வென்றனர்! | They Saw Many Battlefields; They Won in Naval War Too! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 49 (2006) (241–245) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 50 | **CREATE** | `the-field-of-blood-itself-became-the-coronation-hall` | குருதிக்களமே; கொலு மண்டபம் ஆனது! | The Field of Blood Itself Became the Coronation Hall! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 50 (2006) (246–251) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 51 | **CREATE** | `marriages-too-can-bring-a-turn` | திருமணங்களாலும் வருவதுண்டு திருப்பம்! | Marriages Too Can Bring a Turn! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 51 (2006) (252–256) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 52 | **CREATE** | `a-culture-that-announces-an-invasion-in-advance` | படையெடுப்பை முன்கூட்டியே அறிவிக்கும் பண்பாடு! | A Culture That Announces an Invasion in Advance! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 52 (2006) (257–262) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit; quotes lines of the 1951 poems மாணவர் எழுச்சி / இன்னுமா கூச்சல் (QUOTATION only) |
| 53 | **CREATE** | `tamil-escaped-the-sea-deluge-it-found-the-last-sangam` | கடற்கோளில் தப்பிய தமிழ்; கடைச் சங்கம் கண்டது! | Tamil Escaped the Sea-Deluge; It Found the Last Sangam! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 53 (2006) (263–270) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 54 | **CREATE** | `he-who-won-the-battle-of-talaiyalanganam` | தலையாலங்கானத்துச் செருவென்றான்! | He Who Won the Battle of Talaiyalanganam! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 54 (2006) (271–276) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 55 | **CREATE** | `nedunchezhiyan-and-nedunalvadai` | நெடுஞ்செழியனும் நெடுநல்வாடையும்! | Nedunchezhiyan and Nedunalvadai! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 55 (2006) (277–284) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 56 | **CREATE** | `when-attachment-goes-beyond-its-bounds-it-burns-as-frenzy` | பற்று கடந்தால், பற்றி எரியும் வெறியே! | When Attachment Goes Beyond Its Bounds, It Burns as Frenzy! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 56 (2006) (285–288) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 57 | **CREATE** | `what-prize-is-fitting-for-the-beauty-of-a-simile` | உவமை அழகுக்கு உரிய பரிசு என்னவாம்! | What Prize Is Fitting for the Beauty of a Simile! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 57 (2006) (289–295) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |
| 58 | **CREATE** | `beside-the-enemy-sword-s-edge-let-us-labour-all-our-days` | பகைவாள் முனை மருங்க; நாள் எல்லாம் உழைப்போம்! | Beside the Enemy Sword's Edge; Let Us Labour All Our Days! | poetry / poem | kaalap-pezhaiyum-kavithai-saaviyum item 58 (2006) (296–299) | UNIQUE_CANONICAL_POEM |  | source item-title-map: each numbered item is a separate poem/work unit; Wave-4 title census 0 intersections; R1 body-text sweep: no identity overlap with any library unit |

#### Poetry — கலைஞரின் கவிதைகள் (77)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **ADD_WITNESS** | existing `idhayathai-thanthidu-anna` | இதயத்தைத் தந்திடு அண்ணா | Give Me Your Heart, Anna | poetry / poem | kalaignarin-kavithaigal item 01 (1995 4th ed.) (18–31) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of existing `idhayathai-thanthidu-anna` | Wave-4 cross-witness audit; body overlap 0.95/0.94 |
| 2 | **ADD_WITNESS** | existing `thennan-kathai` | தென்னவன் காதை | The Tale of the Southerner | poetry / poem | kalaignarin-kavithaigal item 02 (1995 4th ed.) (34–42) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of existing `thennan-kathai` | Wave-4 cross-witness audit; body overlap 0.95/0.95 |
| 3 | **CREATE** | `indrajit` | இந்திரஜித் | Indrajit | poetry / poem | kalaignarin-kavithaigal item 03 (1995 4th ed.) (43–54) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 4 | **CREATE** | `hiranyan` | இரணியன் | Hiranyan | poetry / poem | kalaignarin-kavithaigal item 04 (1995 4th ed.) (55–61) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 5 | **CREATE** | `king-vali` | வாளி மன்னன் | King Vali | poetry / poem | kalaignarin-kavithaigal item 05 (1995 4th ed.) (62–69) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 6 | **CREATE** | `freedom-fighters` | விடுதலை வீரர்கள் | Freedom Fighters | poetry / poem | kalaignarin-kavithaigal item 06 (1995 4th ed.) (72–79) | UNIQUE_CANONICAL_POEM | kalaignarin-kaviyaranga-kavithaigal-1975 scans 71–77 [NEW (source-declared, pages untranscribed)]; விடுதலை வீரர்கள் ஐவர் (1968, TVA_BOK_0004067) — external, not in the library [audited in source (not onboarded)] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; 3 lines of the 1951 poem மாணவர் எழுச்சி are quoted inside it — QUOTATION |
| 7 | **CREATE** | `the-five-senses` | ஐம்புலன் | The Five Senses | poetry / poem | kalaignarin-kavithaigal item 07 (1995 4th ed.) (80–89) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 8 | **CREATE** | `the-pilavanga-year` | பிலவங்க ஆண்டு | The Pilavanga Year | poetry / poem | kalaignarin-kavithaigal item 08 (1995 4th ed.) (90–100) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 9 | **CREATE** | `love-or-valour` | காதலா - வீரமா? | Love or Valour? | poetry / poem | kalaignarin-kavithaigal item 09 (1995 4th ed.) (101–115) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 10 | **CREATE** | `six-in-the-noble-scripture` | அருமறையில் அறுவர் | Six in the Noble Scripture | poetry / poem | kalaignarin-kavithaigal item 10 (1995 4th ed.) (116–127) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 11 | **CREATE** | `new-path` | புதிய பாதை | New Path | poetry / poem | kalaignarin-kavithaigal item 11 (1995 4th ed.) (128–137) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 12 | **CREATE** | `ten-possessions` | உடைமைகள் பத்து | Ten Possessions | poetry / poem | kalaignarin-kavithaigal item 12 (1995 4th ed.) (138–143) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 13 | **CREATE** | `water-family` | நீர்க் குடும்பம் | The Water Family | poetry / poem | kalaignarin-kavithaigal item 13 (1995 4th ed.) (144–154) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 14 | **CREATE** | `bharathidasan` | பாரதிதாசன் | Bharathidasan | poetry / poem | kalaignarin-kavithaigal item 14 (1995 4th ed.) (155–169) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; distinct from 1975 item 01: printed occasions differ (8.12.68 Bombay vs 29-4-71 Puducherry); ~23% shared lines — SHARED_PASSAGE |
| 15 | **CREATE** | `bharathiyar` | பாரதியார் | Bharathiyar | poetry / poem | kalaignarin-kavithaigal item 15 (1995 4th ed.) (170–174) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 16 | **CREATE** | `pongal-festival-day` | பொங்கல் திருநாள் | Pongal Festival Day | poetry / poem | kalaignarin-kavithaigal item 16 (1995 4th ed.) (175–184) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; shares 9–10 lines with item 64 — SHARED_PASSAGE |
| 17 | **CREATE** | `on-the-path-called-life` | வாழ்வெனும் பாதையில் | On the Path Called Life | poetry / poem | kalaignarin-kavithaigal item 17 (1995 4th ed.) (185–196) | UNIQUE_CANONICAL_POEM | kalaignarin-kaviyaranga-kavithaigal-1975 scans 33–45 [NEW (source-declared, pages untranscribed)] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 18 | **CREATE** | `arithmetic` | கணக்கு | Arithmetic | poetry / poem | kalaignarin-kavithaigal item 18 (1995 4th ed.) (197–204) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 19 | **ADD_WITNESS** | existing `gunanayagar-nehru` | நேரு கண்ட ஜனநாயகம் | Democracy as Nehru Saw It | poetry / poem | kalaignarin-kavithaigal item 19 (1995 4th ed.) (205–215) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of existing `gunanayagar-nehru` | booklet performance note '(முதல்வர் கலைஞர் அவர்கள் 14.11.1970-ல் ... கவிதை.)' = item-19 heading 14.11.1970 Chennai Nehru kaviyarangam; same opening and closing; 118/170 booklet lines verbatim in item 19 |
| 20 | **CREATE** | `thank-you-thank-you` | நன்றி, நன்றி! | Thank You, Thank You! | poetry / poem | kalaignarin-kavithaigal item 20 (1995 4th ed.) (216–217) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 21 | **CREATE** | `silver-jubilee` | வெள்ளி விழா | Silver Jubilee | poetry / poem | kalaignarin-kavithaigal item 21 (1995 4th ed.) (218–226) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 22 | **CREATE** | `anna-is-here` | அண்ணன் இருக்கின்றார் | Anna Is Here | poetry / poem | kalaignarin-kavithaigal item 22 (1995 4th ed.) (227–229) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 23 | **CREATE** | `anna-a-poetry-assembly` | அண்ணன் ஒரு கவியரங்கம் | Anna, a Poetry Assembly | poetry / poem | kalaignarin-kavithaigal item 23 (1995 4th ed.) (230–236, 238–238) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 24 | **CREATE** | `a-walking-journey-for-tamil-to-flourish` | தமிழ் வளர வழிநடைப் பயணம் | A Walking Journey for Tamil to Flourish | poetry / poem | kalaignarin-kavithaigal item 24 (1995 4th ed.) (237–237, 239–244) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 25 | **CREATE** | `for-the-world-to-flourish` | வையம் தழைக்க | For the World to Flourish | poetry / poem | kalaignarin-kavithaigal item 25 (1995 4th ed.) (245–253) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 26 | **CREATE** | `father-periyar` | தந்தை பெரியார் | Father Periyar | poetry / poem | kalaignarin-kavithaigal item 26 (1995 4th ed.) (254–260) | UNIQUE_CANONICAL_POEM | kalaignarin-kaviyaranga-kavithaigal-1975 scans 78–84 [NEW (source-declared, pages untranscribed)] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; 26 lines reused inside item 32 — SHARED_PASSAGE; BU secondary witness notes an earlier Periyar poem embedded in it |
| 27 | **CREATE** | `akam-creations` | அகத்துறைப் படைப்புகள் | Akam Creations | poetry / poem | kalaignarin-kavithaigal item 27 (1995 4th ed.) (261–266) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 28 | **CREATE** | `pongal-festival` | பொங்கல் விழா | Pongal Festival | poetry / poem | kalaignarin-kavithaigal item 28 (1995 4th ed.) (267–272) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 29 | **CREATE** | `a-silappathikaram-feast` | சிலப்பதிகார விருந்து | A Silappathikaram Feast | poetry / poem | kalaignarin-kavithaigal item 29 (1995 4th ed.) (273–285) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 30 | **CREATE** | `on-annas-path` | அண்ணா வழியில் | On Anna's Path | poetry / poem | kalaignarin-kavithaigal item 30 (1995 4th ed.) (286–292) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 31 | **CREATE** | `i-shall-walk-on-our-ayya-and-annas-path` | நடந்திடுவேன் நமது அய்யா, அண்ணா வழியில்! | I Shall Walk on Our Ayya and Anna's Path! | poetry / poem | kalaignarin-kavithaigal item 31 (1995 4th ed.) (293–296) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 32 | **CREATE** | `presiding-poem-three-great-celebrations` | முப்பெரும் விழாக் கவியரங்கம் தலைமைக் கவிதை | Presiding Poem at the Three Great Celebrations Poetry Assembly | poetry / poem | kalaignarin-kavithaigal item 32 (1995 4th ed.) (297–310) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; reuses passages of items 23, 26, 30 — SHARED_PASSAGE |
| 33 | **CREATE** | `in-a-changing-town` | மாறி வரும் ஊரினிலே | In a Changing Town | poetry / poem | kalaignarin-kavithaigal item 33 (1995 4th ed.) (311–317) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 34 | **CREATE** | `views-of-society` | சமுதாயப் பார்வைகள்...! | Views of Society...! | poetry / poem | kalaignarin-kavithaigal item 34 (1995 4th ed.) (318–328) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 35 | **CREATE** | `kalaivanar-arangam-poetry-assembly` | கலைவாணர் அரங்கக் கவியரங்கம் | Kalaivanar Arangam Poetry Assembly | poetry / poem | kalaignarin-kavithaigal item 35 (1995 4th ed.) (329–332) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 36 | **CREATE** | `chithirai-festival-presiding-poem` | "சித்திரைத் திருநாள்" தலைமைக் கவிதை! | "Chithirai Festival" — Presiding Poem! | poetry / poem | kalaignarin-kavithaigal item 36 (1995 4th ed.) (333–345) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 37 | **CREATE** | `three-letters-thoughts-three-times-three` | எழுத்துக்கள் மூன்று - எண்ணங்கள் மும்மூன்று | Three Letters — Thoughts Three Times Three | poetry / poem | kalaignarin-kavithaigal item 37 (1995 4th ed.) (346–361) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 38 | **CREATE** | `on-arignar-annas-path` | “அறிஞர் அண்ணா வழியில்” | “On Arignar Anna’s Path” | poetry / poem | kalaignarin-kavithaigal item 38 (1995 4th ed.) (362–371) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 39 | **CREATE** | `panneerselvam` | பன்னீர்ச்செல்வமே! | Panneerselvam! | poetry / poem | kalaignarin-kavithaigal item 39 (1995 4th ed.) (374–375) | UNIQUE_CANONICAL_POEM | unarchchimaalai unit 10 கவிதையல்ல - கண்ணீர்க்கடல் ! (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 40 | **CREATE** | `mother-arts-foremost-son` | கலைத்தாயின் தலைச் செல்வன்! | Mother Art’s Foremost Son! | poetry / poem | kalaignarin-kavithaigal item 40 (1995 4th ed.) (376–378) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 41 | **CREATE** | `we-move-as-your-shadow` | உன் நிழலாக அசைகின்றோம்! | We Move as Your Shadow! | poetry / poem | kalaignarin-kavithaigal item 41 (1995 4th ed.) (379–381) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; reused (36/67 lines) inside the 2008 standalone அணையா விளக்கு அண்ணா — SHARED_PASSAGE |
| 42 | **CREATE** | `long-live-jeeva` | வாழ்க ஜீவா | Long Live Jeeva | poetry / poem | kalaignarin-kavithaigal item 42 (1995 4th ed.) (382–383) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 43 | **CREATE** | `the-fallen-hero` | மறைந்த மாவீரன் | The Fallen Hero | poetry / poem | kalaignarin-kavithaigal item 43 (1995 4th ed.) (384–389) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 44 | **CREATE** | `my-dear-friend-why-did-you-leave` | என் இனிய நண்பா! ஏன் பிரிந்தாய்? | My Dear Friend! Why Did You Leave? | poetry / poem | kalaignarin-kavithaigal item 44 (1995 4th ed.) (390–391) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 45 | **CREATE** | `today-is-your-birthday` | இன்றைக்கு உன்றன் பிறந்த நாள் | Today Is Your Birthday | poetry / poem | kalaignarin-kavithaigal item 45 (1995 4th ed.) (394–395) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; quoted (84% of the poem) inside Murasoli letter m49-l3775 — QUOTATION |
| 46 | **CREATE** | `no-one-day-called-his-birthday` | அவன் பிறந்தநாள் என ஒன்றில்லை! | There Is No One Day Called His Birthday! | poetry / poem | kalaignarin-kavithaigal item 46 (1995 4th ed.) (396–397) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 47 | **CREATE** | `precious-remedy-anbazhaga-beloved-sibling` | அருமருந்தே! அன்பழக உடன்பிறப்பே! | Precious Remedy! Anbazhaga, Beloved Sibling! | poetry / poem | kalaignarin-kavithaigal item 47 (1995 4th ed.) (398–399) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 48 | **CREATE** | `rationalist-pandianar` | பகுத்தறிவுப் பாண்டியனார்! | Rationalist Pandianar! | poetry / poem | kalaignarin-kavithaigal item 48 (1995 4th ed.) (400–402) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 49 | **CREATE** | `scales-of-justice` | நியாயத் தராசு | The Scales of Justice | poetry / poem | kalaignarin-kavithaigal item 49 (1995 4th ed.) (403–403) | UNIQUE_CANONICAL_POEM | ina-muzhakkam unit 6 poem 6.1 நியாயத் திராசு! (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 50 | **CREATE** | `would-they-accept` | ஏற்பாரோ? | Would They Accept? | poetry / poem | kalaignarin-kavithaigal item 50 (1995 4th ed.) (404–404) | UNIQUE_CANONICAL_POEM | ina-muzhakkam 6.2 ஏற்பரோ! (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 51 | **CREATE** | `know-it-as-a-storm` | புயல் என அறிக! | Know It as a Storm! | poetry / poem | kalaignarin-kavithaigal item 51 (1995 4th ed.) (405–405) | UNIQUE_CANONICAL_POEM | ina-muzhakkam 6.3 சைவரே! (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 52 | **HOLD** | — | கேட்டுண்டோ? | Have You Heard? | poetry / poem | kalaignarin-kavithaigal item 52 (1995 4th ed.) (406–406) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | HOLD: Kavithaigal item 52 கேட்டுண்டோ? (16 lines) ≈ இன முழக்கம் (1951) poems 6.5 பொதுவுடைமையே! + 6.6 யோசித்துப் பார்! combined (6.6 wholly contained, 6.5 50–82%); one-poem-vs-two identity unresolved |
| 53 | **CREATE** | `varna-or-death` | வருணமா? மரணமா? | Varna or Death? | poetry / poem | kalaignarin-kavithaigal item 53 (1995 4th ed.) (407–407) | UNIQUE_CANONICAL_POEM | ina-muzhakkam 6.11 வருணமா? மரணமா? (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 54 | **CREATE** | `when-does-defeat-come` | தோல்வி எப்பொழுது? | When Does Defeat Come? | poetry / poem | kalaignarin-kavithaigal item 54 (1995 4th ed.) (408–408) | UNIQUE_CANONICAL_POEM | ina-muzhakkam 6.9 தோல்வி எப்பொழுது? (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 55 | **CREATE** | `still-this-clamour` | இன்றுமா கூச்சல்? | Still This Clamour? | poetry / poem | kalaignarin-kavithaigal item 55 (1995 4th ed.) (409–409) | UNIQUE_CANONICAL_POEM | ina-muzhakkam 6.10 இன்னுமா கூச்சல்? (1951) [NEW] | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 56 | **HOLD** | — | பச்சைக் கிளி | Green Parrot | poetry / poem | kalaignarin-kavithaigal item 56 (1995 4th ed.) (410–412) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | HOLD: same text as மீசை முளைத்த வயதில் unit 14 பச்சைக்கிளி (33/40 lines verbatim, overlap 0.97) AND prose-formatted inside existing Fiction LibraryWork சிறை கொடியது (2004 anthology; 72–78% of the story); cross-shelf identity decision required |
| 57 | **CREATE** | `fountain-of-imagination` | கற்பனை ஊற்று | Fountain of Imagination | poetry / poem | kalaignarin-kavithaigal item 57 (1995 4th ed.) (413–414) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 58 | **CREATE** | `o-sky-pour-down` | வானமே பொழிக நீ! | O Sky, Pour Down! | poetry / poem | kalaignarin-kavithaigal item 58 (1995 4th ed.) (415–416) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 59 | **CREATE** | `a-letter-in-verse` | கவிதையில் ஒரு மடல்! | A Letter in Verse! | poetry / poem | kalaignarin-kavithaigal item 59 (1995 4th ed.) (417–417) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 60 | **CREATE** | `will-he-realise-who-knows` | அவர் உணர்வாரோ! யார் அறிவார்? | Will He Realise? Who Knows? | poetry / poem | kalaignarin-kavithaigal item 60 (1995 4th ed.) (418–419) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 61 | **CREATE** | `let-it-whirl-as-a-battle-sword` | போர்வாளாய்ச் சுழலட்டும்! | Let It Whirl as a Battle-Sword! | poetry / poem | kalaignarin-kavithaigal item 61 (1995 4th ed.) (420–421) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 62 | **CREATE** | `whose-names-have-still-not-appeared` | இன்னும் யார் யார் பெயர்கள் வரவில்லை? | Whose Names Have Still Not Appeared? | poetry / poem | kalaignarin-kavithaigal item 62 (1995 4th ed.) (422–424) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 63 | **CREATE** | `a-drop-of-honey` | ஒரு சொட்டுத் தேன்! | A Drop of Honey! | poetry / poem | kalaignarin-kavithaigal item 63 (1995 4th ed.) (425–427) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 64 | **CREATE** | `let-it-sprout-as-seed-and-put-forth-roots` | விதையாய் முளைத்து விழுதுகள் விடட்டும்! | Let It Sprout as Seed and Put Forth Roots! | poetry / poem | kalaignarin-kavithaigal item 64 (1995 4th ed.) (428–428) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit; reuses 9 lines of item 16 (1970 Pongal radio poem) — SHARED_PASSAGE |
| 65 | **CREATE** | `he-calls-the-sun-an-ice-cube` | சூரியனைப் பனிக்கட்டி என்கின்றார்! | He Calls the Sun an Ice Cube! | poetry / poem | kalaignarin-kavithaigal item 65 (1995 4th ed.) (429–432) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 66 | **CREATE** | `dont-stop-your-stride` | நடையை நிறுத்தாதே! | Don't Stop Your Stride! | poetry / poem | kalaignarin-kavithaigal item 66 (1995 4th ed.) (433–434) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 67 | **CREATE** | `a-backwater-full-of-ignorant-folk` | பாமரர் நிறைந்த பட்டிக்காடு! | A Backwater Full of Ignorant Folk! | poetry / poem | kalaignarin-kavithaigal item 67 (1995 4th ed.) (435–437) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 68 | **CREATE** | `tamil-nadu-is-being-looted` | கொள்ளை போகுதம்மா தமிழ்நாடு | Tamil Nadu Is Being Looted | poetry / poem | kalaignarin-kavithaigal item 68 (1995 4th ed.) (438–439) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 69 | **CREATE** | `what-kind-of-country-is-this` | என்ன தேசமடா இது? | What Kind of Country Is This? | poetry / poem | kalaignarin-kavithaigal item 69 (1995 4th ed.) (440–442) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 70 | **CREATE** | `come-let-us-tear-off-the-mask` | முகமூடி கிழித்தெறிவோம் வாரீர்! | Come, Let Us Tear Off the Mask! | poetry / poem | kalaignarin-kavithaigal item 70 (1995 4th ed.) (443–445) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 71 | **CREATE** | `what-is-the-answer-tell-us` | பதில் என்ன? பகர்ந்திடுக! | What Is the Answer? Tell Us! | poetry / poem | kalaignarin-kavithaigal item 71 (1995 4th ed.) (446–447) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 72 | **CREATE** | `ka-ka-ka` | கா, கா, கா! | Kā, Kā, Kā! | poetry / poem | kalaignarin-kavithaigal item 72 (1995 4th ed.) (448–449) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 73 | **CREATE** | `let-us-rise-in-the-east-like-the-sun` | பகலவனாய்க் கிழக்கில் உதித்திடுவோம்! | Let Us Rise in the East Like the Sun! | poetry / poem | kalaignarin-kavithaigal item 73 (1995 4th ed.) (450–452) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 74 | **CREATE** | `is-this-diversion-justified` | திசை திருப்பல் நியாயம்தானா? | Is This Diversion Justified? | poetry / poem | kalaignarin-kavithaigal item 74 (1995 4th ed.) (453–454) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 75 | **CREATE** | `it-is-over-a-comedy-drama` | நடந்து முடிந்ததம்மா; ஒரு நகைச்சுவை நாடகம்! | It Is Over—a Comedy Drama! | poetry / poem | kalaignarin-kavithaigal item 75 (1995 4th ed.) (455–456) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 76 | **CREATE** | `there-are-some-countries` | சில நாடுகள் இருக்கின்றன! | There Are Some Countries! | poetry / poem | kalaignarin-kavithaigal item 76 (1995 4th ed.) (457–460) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |
| 77 | **CREATE** | `you-bless-your-footwear` | உன் காலணியை வாழ்த்துகிறாய் | You Bless Your Footwear | poetry / poem | kalaignarin-kavithaigal item 77 (1995 4th ed.) (461–464) | UNIQUE_CANONICAL_POEM |  | 1995 anthology item file (one canonical file per indexed poem); R1 body-text sweep: no identity overlap with any library unit |

#### Poetry — கலைஞரின் கவியரங்கக் கவிதைகள் 1975 (3 active items)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `at-the-revolutionary-poets-poetry-gathering` | புரட்சிக் கவிஞர் பாட்டரங்கில் / முதல்வர் கலைஞர் தலைமைக் கவிதை | At the Revolutionary Poet's Poetry Gathering / Chief Minister Kalaignar's Presiding Poem | poetry / poem | kalaignarin-kaviyaranga-kavithaigal-1975 intake item 01 (1975 1st ed.) (46–57) | UNIQUE_CANONICAL_POEM |  | event 29-4-71 Puducherry (Bharathidasan 80th birthday) presiding poem; not any of the five already-represented ranges; shares ~23% of lines with Kavithaigal item 14 (8.12.68 Bombay) — distinct occasion — SHARED_PASSAGE |
| 2 | **CREATE** | `at-the-parambu-hill-festival-for-the-great-patron-pari` | பறம்புமலைப் பாரி வள்ளல் விழாக் / கவியரங்கில் / முதல்வர் கலைஞரின் தலைமைக் கவிதை | At the Parambu Hill Festival for the Great Patron Pari / At the Poetry Gathering / Chief Minister Kalaignar's Presiding Poem | poetry / poem | kalaignarin-kaviyaranga-kavithaigal-1975 intake item 02 (1975 1st ed.) (58–65) | UNIQUE_CANONICAL_POEM |  | event 5-5-71 Parambu Hill / Pari festival presiding poem; not any represented range; no library overlap (BU Shower-of-Poetry I entry 17 is an external English witness only) |
| 4 | **CREATE** | `chief-minister-kalaignars-reply-poem` | “முதல்வர் கலைஞரின் பதில் கவிதை” | “Chief Minister Kalaignar's Reply Poem” | poetry / poem | kalaignarin-kaviyaranga-kavithaigal-1975 intake item 04 (1975 1st ed.) (67–68) | UNIQUE_CANONICAL_POEM |  | Kalaignar's reply poem to the non-Kalaignar Rajaji poem on scan 66 (ordinal 03 excluded); no library overlap |

#### இன முழக்கம் — top-level units (6)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `ina-muzhakkam-katturai` | இன முழக்கம் | The Clarion Call of the Race | essays-articles / essay | ina-muzhakkam unit 1 (1951 1st ed.) (6–13) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title equals the publication title — keep canonical identity distinct from the publication |
| 2 | **HOLD** | — | சொர்க்க லோகத்தில் | In the Heavenly Realm | essays-articles / essay | ina-muzhakkam unit 2 (1951 1st ed.) (14–24) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | contains 90% of the existing Fiction LibraryWork சொர்க்கத்திற்கு வந்தது எப்படி? (2004 anthology) — a later shorter re-edited text; cross-shelf identity decision required |
| 3 | **CREATE** | `murasaraivai` | முரசறைவாய் | Beat the Drum | essays-articles / essay | ina-muzhakkam unit 3 (1951 1st ed.) (25–29) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 4 | **CREATE** | `pazhikku-pazhi` | பழிக்குப் பழி | Revenge for Revenge | essays-articles / essay | ina-muzhakkam unit 4 (1951 1st ed.) (30–37) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 5 | **CREATE** | `aariyam-pesugirathu` | ஆரியம் பேசுகிறது | Aryanism Speaks | essays-articles / essay | ina-muzhakkam unit 5 (1951 1st ed.) (38–39) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 6 | **DO_NOT_PROMOTE** | — | கவிதைகள் | Poems | — / — | ina-muzhakkam unit 6 (1951 1st ed.) (41–49) | DEPENDENT_NOT_PROMOTABLE |  | archive heading கவிதைகள் is a container of 11 poems, not a work; its poems are reconciled individually |

#### இன முழக்கம் — unit 6 poems (11)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 6.1 | **ADD_WITNESS** | — | நியாயத் திராசு! | Scale of Justice! | poetry / poem | ina-muzhakkam unit 6 poem 1 (1951 1st ed.) (41) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `scales-of-justice` | earlier (1951) witness of Kavithaigal item 49 — see that entry |
| 6.2 | **ADD_WITNESS** | — | ஏற்பரோ! | Will They Accept! | poetry / poem | ina-muzhakkam unit 6 poem 2 (1951 1st ed.) (41, 42) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `would-they-accept` | earlier (1951) witness of Kavithaigal item 50 — see that entry |
| 6.3 | **ADD_WITNESS** | — | சைவரே! | Saivites! | poetry / poem | ina-muzhakkam unit 6 poem 3 (1951 1st ed.) (42) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `know-it-as-a-storm` | earlier (1951) witness of Kavithaigal item 51 — see that entry |
| 6.4 | **CREATE** | `ina-muzhakkam-poem-04` | வா! | Come! | poetry / poem | ina-muzhakkam unit 6 poem 4 (1951 1st ed.) (43) | UNIQUE_CANONICAL_POEM |  | no overlap anywhere in the library |
| 6.5 | **HOLD** | — | பொதுவுடைமையே! | Common Ownership! | poetry / poem | ina-muzhakkam unit 6 poem 5 (1951 1st ed.) (43) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | with Kavithaigal item 52 (one-poem-vs-two) |
| 6.6 | **HOLD** | — | யோசித்துப் பார்! | Think It Over! | poetry / poem | ina-muzhakkam unit 6 poem 6 (1951 1st ed.) (44) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | with Kavithaigal item 52 (one-poem-vs-two); wholly contained in item 52 |
| 6.7 | **CREATE** | `ina-muzhakkam-poem-07` | மாணவர் எழுச்சி. | Student Uprising. | poetry / poem | ina-muzhakkam unit 6 poem 7 (1951 1st ed.) (44) | UNIQUE_CANONICAL_POEM |  | no identity overlap; 3 lines quoted inside Kavithaigal item 06 and lines quoted in Kaalap item 52 (QUOTATION); BU Shower-of-Poetry I entry 4 'Students' Awakening!' (dated 1945) is a title-level external correspondence only |
| 6.8 | **CREATE** | `ina-muzhakkam-poem-08` | வாளிங்கே! | Here Is the Sword! | poetry / poem | ina-muzhakkam unit 6 poem 8 (1951 1st ed.) (45, 46, 47, 48) | UNIQUE_CANONICAL_POEM |  | no identity overlap; 15 lines quoted inside the 1977 Fiction work சந்தனக்கிண்ணம் (QUOTATION); the author's 2002 Meesai preface quotes its opening and names it the long poem 'புறநானூற்றுத் தாய்' (1945, குடியரசு) — alternate title recorded, printed ina heading retained |
| 6.9 | **ADD_WITNESS** | — | தோல்வி எப்பொழுது? | When Will There Be Defeat? | poetry / poem | ina-muzhakkam unit 6 poem 9 (1951 1st ed.) (48) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `when-does-defeat-come` | earlier (1951) witness of Kavithaigal item 54 — see that entry |
| 6.10 | **ADD_WITNESS** | — | இன்னுமா கூச்சல்? | Still This Clamour? | poetry / poem | ina-muzhakkam unit 6 poem 10 (1951 1st ed.) (49) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `still-this-clamour` | earlier (1951) witness of Kavithaigal item 55 — see that entry |
| 6.11 | **ADD_WITNESS** | — | வருணமா? மரணமா? | Varna or Death? | poetry / poem | ina-muzhakkam unit 6 poem 11 (1951 1st ed.) (49) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `varna-or-death` | earlier (1951) witness of Kavithaigal item 53 — see that entry |

#### Essays — `unarchchimaalai`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `unarchchi-maalai` | உணர்ச்சி மாலை | Garland of Emotion | essays-articles / essay | unarchchimaalai unit 1 (6–9) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title உணர்ச்சி மாலை ≈ publication title உணர்ச்சிமாலை — keep identities distinct |
| 2 | **CREATE** | `puratchi-valarntha-kathai` | புரட்சி வளர்ந்த கதை | The Story of How the Revolution Grew | essays-articles / essay | unarchchimaalai unit 2 (10–15) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 3 | **CREATE** | `pogiran-pogiran` | போகிறான்;போகிறான்..! | He Goes; He Goes..! | essays-articles / essay | unarchchimaalai unit 3 (16–18) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 4 | **CREATE** | `iravanan-nam-pattan` | இராவணன் நம் பாட்டன் | Ravana Is Our Grandfather | essays-articles / essay | unarchchimaalai unit 4 (19–29) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 5 | **CREATE** | `ingalla-irashyavil` | இங்கல்ல! இரஷ்யாவில் | Not Here! In Russia | essays-articles / essay | unarchchimaalai unit 5 (30–32) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 6 | **CREATE** | `3-57-90` | 3, 57, 90. | 3, 57, 90. | essays-articles / essay | unarchchimaalai unit 6 (33–38) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 7 | **CREATE** | `30-1-1948` | 30-1-1948 | 30-1-1948 | essays-articles / essay | unarchchimaalai unit 7 (39–41) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 8 | **CREATE** | `paththiniye-unpol` | பத்தினியே உன்போல்...! | O Chaste Woman, Like You...! | essays-articles / essay | unarchchimaalai unit 8 (42–44) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 9 | **CREATE** | `annai-nagammaiyar` | அன்னை நாகம்மையார்! | Mother Nagammaiyar! | essays-articles / essay | unarchchimaalai unit 9 (45–47) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 10 | **ADD_WITNESS** | — | கவிதையல்ல - கண்ணீர்க்கடல் ! | Not a Poem — an Ocean of Tears! | poetry / poem | unarchchimaalai unit 10 (48–49) | SAME_CANONICAL_POEM_ALTERNATE_WITNESS | → witness of proposed `panneerselvam` | verse elegy = Kavithaigal item 39 பன்னீர்ச்செல்வமே! (see that entry); not an essay |

#### Essays — `thiraavida-sampaththu`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `thiraavida-sampaththu-katturai` | திராவிட சம்பத்து | Dravidian Wealth | essays-articles / essay | thiraavida-sampaththu unit 1 (5–6, 13–16) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title equals the publication title; non-contiguous scan runs preserved |
| 2 | **CREATE** | `aiyar-arivikkirar` | ஐயர் அறிவிக்கிறார்! | Iyer Announces! | essays-articles / essay | thiraavida-sampaththu unit 2 (12–12, 3–3) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |

#### Essays — `kolaikkalam`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `kolaikkalam-katturai` | கொலைக்களம்! | The Killing Field! | essays-articles / essay | kolaikkalam unit 1 (5–9) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title equals the publication title |
| 2 | **CREATE** | `asthi-karaiyattum` | ‘அஸ்தி’ கரையட்டும்! | Let the ‘Ashes’ Dissolve! | essays-articles / essay | kolaikkalam unit 2 (10–16) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 3 | **CREATE** | `paliyai-niruththungal` | பலியை நிறுத்துங்கள்! | Stop the Sacrifice! | essays-articles / essay | kolaikkalam unit 3 (17–22) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 4 | **CREATE** | `vizhalukku-neer-iraiththu` | விழலுக்கு நீர் இறைத்து... | Watering the Weeds... | essays-articles / essay | kolaikkalam unit 4 (23–27) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 5 | **CREATE** | `sothanai` | சோதனை! | Search! | essays-articles / essay | kolaikkalam unit 5 (28–33) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 6 | **CREATE** | `veeramuzhakkam-seythiduveer` | வீரமுழக்கஞ் செய்திடுவீர்! | Raise the Heroic Cry! | essays-articles / essay | kolaikkalam unit 6 (34–40) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |

#### Essays — `sinthanaiyum-seyalum`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **HOLD** | — | பாசியும் - தூசியும்! | Moss and Dust! | essays-articles / essay | sinthanaiyum-seyalum unit 1 (18–23) | MIXED_OR_GENRE_UNRESOLVED |  | letter-form piece (opens 'உடன்பிறப்பே,') inside an essay collection; Letters shelf holds only the Murasoli corpus — shelf decision (Essays vs Letters) required; no duplicate found |
| 2 | **HOLD** | — | அதிக உயரம் தாண்டுவதற்கு | To Clear a Greater Height | essays-articles / essay | sinthanaiyum-seyalum unit 2 (24–27) | MIXED_OR_GENRE_UNRESOLVED |  | letter-form piece (opens 'உடன்பிறப்பே,', signed 'அன்புள்ள மு.க.'); shelf decision required; no duplicate found |
| 3 | **CREATE** | `en-peyar-puratchi` | என் பெயர் புரட்சி! | My Name Is Revolution! | essays-articles / essay | sinthanaiyum-seyalum unit 3 (28–32) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 4 | **CREATE** | `kurukulam` | குருகுலம்! | Gurukulam! | essays-articles / essay | sinthanaiyum-seyalum unit 4 (33–35) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 5 | **CREATE** | `jananayaga-neri` | ஜனநாயக நெறி | The Way of Democracy | essays-articles / essay | sinthanaiyum-seyalum unit 5 (36–38) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 6 | **CREATE** | `vaakkuseettin-valimai` | வாக்குச்சீட்டின் வலிமை | The Power of the Ballot | essays-articles / essay | sinthanaiyum-seyalum unit 6 (39–41) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 7 | **CREATE** | `suyamariyathai-thirumanam` | சுயமரியாதைத் திருமணம் | Self-Respect Marriage | essays-articles / essay | sinthanaiyum-seyalum unit 7 (42–45) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 8 | **CREATE** | `manithanin-marupakkam` | மனிதனின் மறுபக்கம் | The Other Side of Man | essays-articles / essay | sinthanaiyum-seyalum unit 8 (46–48) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 9 | **CREATE** | `vinnai-thottu-mannil-pudhaivatha` | விண்ணைத் தொட்டு மண்ணில் புதைவதா? | Touching the Sky, Buried in the Earth? | essays-articles / essay | sinthanaiyum-seyalum unit 9 (49–51) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 10 | **CREATE** | `manithanum-marupiraviyum` | மனிதனும் மறுபிறவியும் | Man and Rebirth | essays-articles / essay | sinthanaiyum-seyalum unit 10 (52–55) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 11 | **CREATE** | `vetri-tholvi` | வெற்றி தோல்வி! | Victory and Defeat! | essays-articles / essay | sinthanaiyum-seyalum unit 11 (56–58) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 12 | **CREATE** | `azhukkaru` | அழுக்காறு | Azhukkaaru | essays-articles / essay | sinthanaiyum-seyalum unit 12 (59–61) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 13 | **CREATE** | `miguthikkan` | மிகுதிக்கண்... | When the Limit Is Crossed... | essays-articles / essay | sinthanaiyum-seyalum unit 13 (62–65) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 14 | **CREATE** | `valivum-polivum` | வலிவும், பொலிவும்! | Strength and Radiance! | essays-articles / essay | sinthanaiyum-seyalum unit 14 (66–68) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 15 | **CREATE** | `inbamum-thunbamum` | இன்பமும் துன்பமும்! | Joy and Sorrow! | essays-articles / essay | sinthanaiyum-seyalum unit 15 (69–74) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 16 | **CREATE** | `ozhukkam` | ஒழுக்கம் | Conduct | essays-articles / essay | sinthanaiyum-seyalum unit 16 (75–77) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 17 | **CREATE** | `vasiya-marunthu` | வசிய மருந்து | The Enchantment Drug | essays-articles / essay | sinthanaiyum-seyalum unit 17 (78–81) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 18 | **CREATE** | `sothida-sogam` | சோதிட சோகம்! | Astrological Sorrow! | essays-articles / essay | sinthanaiyum-seyalum unit 18 (82–84) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 19 | **CREATE** | `aanmiga-aazhkadal` | ஆன்மிக ஆழ்கடல் | A Deep Ocean of Spirituality | essays-articles / essay | sinthanaiyum-seyalum unit 19 (85–89) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 20 | **CREATE** | `thenil-kuzhaithu-koduthaalum` | தேனில் குழைத்துக் கொடுத்தாலும்...! | Even If Mixed with Honey...! | essays-articles / essay | sinthanaiyum-seyalum unit 20 (90–93) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 21 | **CREATE** | `viyaathikku-viruntha` | வியாதிக்கு விருந்தா? | A Feast for Disease? | essays-articles / essay | sinthanaiyum-seyalum unit 21 (94–97) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 22 | **CREATE** | `vilaiyaattu` | விளையாட்டு | Sport | essays-articles / essay | sinthanaiyum-seyalum unit 22 (98–100) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 23 | **CREATE** | `thannai-velvaan` | தன்னை வெல்வான் | He Who Conquers Himself | essays-articles / essay | sinthanaiyum-seyalum unit 23 (101–103) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 24 | **CREATE** | `idlar` | இட்லர் | Hitler | essays-articles / essay | sinthanaiyum-seyalum unit 24 (104–108) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 25 | **CREATE** | `ingarsaal` | இங்கர்சால் | Ingersoll | essays-articles / essay | sinthanaiyum-seyalum unit 25 (109–111) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 26 | **CREATE** | `magalir-ida-othukkeedu` | மகளிர் இட ஒதுக்கீடு! | Women's Reservation! | essays-articles / essay | sinthanaiyum-seyalum unit 26 (112–116) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; a verbatim passage of ~560–660 normalised characters recurs in three later Murasoli letters (m43-l3464 dated 07-03-2010, m49-l3785, m52-l3941; at most 38% of the essay) — later reuse, SHARED_PASSAGE; the essay remains a distinct work |
| 27 | **CREATE** | `thiyanam` | தியானம்??? | Meditation??? | essays-articles / essay | sinthanaiyum-seyalum unit 27 (117–122) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 28 | **CREATE** | `vibaththu` | விபத்து | Accident | essays-articles / essay | sinthanaiyum-seyalum unit 28 (123–125) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 29 | **CREATE** | `chinnathirai-selvi` | சின்னத்திரை “செல்வி” | The Small-Screen “Selvi” | essays-articles / essay | sinthanaiyum-seyalum unit 29 (126–129) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 30 | **CREATE** | `marunthena-onru` | மருந்தென ஒன்று! | A Thing Called Medicine! | essays-articles / essay | sinthanaiyum-seyalum unit 30 (130–133) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 31 | **CREATE** | `siriya-noolthaan` | சிறிய நூல்தான் | Only a Small Book | essays-articles / essay | sinthanaiyum-seyalum unit 31 (134–138) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 32 | **CREATE** | `mandela` | மண்டேலா | Mandela | essays-articles / essay | sinthanaiyum-seyalum unit 32 (139–144) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 33 | **CREATE** | `thondullam` | தொண்டுள்ளம் | Spirit of Service | essays-articles / essay | sinthanaiyum-seyalum unit 33 (145–147) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 34 | **CREATE** | `magalir-perani` | மகளிர் பேரணி! | Women's Rally! | essays-articles / essay | sinthanaiyum-seyalum unit 34 (148–151) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 35 | **CREATE** | `thirikadugam` | திரிகடுகம் | Thirikadugam | essays-articles / essay | sinthanaiyum-seyalum unit 35 (152–154) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 36 | **CREATE** | `theekkuchchi-thedatheer` | தீக்குச்சி தேடாதீர்! | Don't Look for a Matchstick! | essays-articles / essay | sinthanaiyum-seyalum unit 36 (155–158) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 37 | **CREATE** | `silambum-maniyum` | சிலம்பும் மணியும்! | The Anklet and the Gem! | essays-articles / essay | sinthanaiyum-seyalum unit 37 (159–162) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 38 | **CREATE** | `seynnanri` | செய்ந்நன்றி | Gratitude for Help Received | essays-articles / essay | sinthanaiyum-seyalum unit 38 (163–166) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 39 | **CREATE** | `pagutharivu-paathai` | பகுத்தறிவுப் பாதை! | The Path of Rationalism! | essays-articles / essay | sinthanaiyum-seyalum unit 39 (167–172) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 40 | **CREATE** | `penniyap-puratchi` | பெண்ணியப் புரட்சி! | A Feminist Revolution! | essays-articles / essay | sinthanaiyum-seyalum unit 40 (173–177) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 41 | **CREATE** | `vali-arivikkum-vaayillaa-mozhi` | வலி அறிவிக்கும் வாயில்லா மொழி! | The Mute Language That Tells of Pain! | essays-articles / essay | sinthanaiyum-seyalum unit 41 (178–181) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 42 | **CREATE** | `varumun-kaappathaa-vanthapin-kaappathaa` | வருமுன் காப்பதா? வந்தபின் காப்பதா? | Protect Before It Comes? Or After It Comes? | essays-articles / essay | sinthanaiyum-seyalum unit 42 (182–187) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 43 | **CREATE** | `enge-sorgam-enge-sorgam` | எங்கே சொர்க்கம்? எங்கே சொர்க்கம்? | Where Is Heaven? Where Is Heaven? | essays-articles / essay | sinthanaiyum-seyalum unit 43 (188–191) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 44 | **CREATE** | `guru-peedamum-kural-peedamum` | குரு பீடமும்; குறள் பீடமும்! | The Guru Peedam and the Kural Peedam! | essays-articles / essay | sinthanaiyum-seyalum unit 44 (192–194) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 45 | **CREATE** | `iraiyanaar-kuralum-iniyavai-naarpathum` | இறையனார் குறளும்; இனியவை நாற்பதும்! | Iraiyanar's Kural and Iniyavai Narpathu! | essays-articles / essay | sinthanaiyum-seyalum unit 45 (195–198) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 46 | **CREATE** | `padagukku-oru-kanakku-naattukku-oru-kanakkaa` | படகுக்கு ஒரு கணக்கு; நாட்டுக்கு ஒரு கணக்கா? | One Calculation for a Boat; Another for a Country? | essays-articles / essay | sinthanaiyum-seyalum unit 46 (199–203) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 47 | **CREATE** | `kalasangal-kalangarai-vilakkangalaagalam` | கலசங்கள், கலங்கரை விளக்கங்களாகலாம்! | Finials Can Become Lighthouses! | essays-articles / essay | sinthanaiyum-seyalum unit 47 (204–209) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 48 | **CREATE** | `nalvazhikku-naattarayyaavin-urai` | நல்வழிக்கு நாட்டாரய்யாவின் உரை! | Nattarayya's Commentary on Nalvazhi! | essays-articles / essay | sinthanaiyum-seyalum unit 48 (210–213) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 49 | **CREATE** | `anthaathi-paadiya-aruthakutti-naadar` | அந்தாதி பாடிய அருதகுட்டி நாடார் | Aruthakutti Nadar Who Sang an Anthathi | essays-articles / essay | sinthanaiyum-seyalum unit 49 (214–220) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 50 | **CREATE** | `sinthanai-sey-maname` | சிந்தனை செய் மனமே | Think, O Mind | essays-articles / essay | sinthanaiyum-seyalum unit 50 (221–225) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |

#### Essays — `perumoochu`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **CREATE** | `perumoochu-katturai` | பெருமூச்சு | A Deep Sigh | essays-articles / essay | perumoochu unit 1 (7–10) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title equals the publication title |
| 2 | **CREATE** | `maaligai-amaiththida-vareer` | மாளிகை அமைத்திட வாரீர்! | Come, Let Us Build the Mansion! | essays-articles / essay | perumoochu unit 2 (11–16) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 3 | **CREATE** | `manthirigal-kulai-nadukkam` | மந்திரிகள் குலை நடுக்கம் | Ministers Tremble in Fear | essays-articles / essay | perumoochu unit 3 (17–20) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 4 | **CREATE** | `vaapas-veerargal` | வாபஸ் வீரர்கள்! | Heroes of Retreat! | essays-articles / essay | perumoochu unit 4 (21–23) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 5 | **CREATE** | `podhu-makkalukku-thani-echarikkai` | பொது மக்களுக்குத் தனி எச்சரிக்கை | A Special Warning to the Public | essays-articles / essay | perumoochu unit 5 (24–36) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 6 | **CREATE** | `siruvargal` | சிறுவர்கள் | Youngsters | essays-articles / essay | perumoochu unit 6 (37–40) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 7 | **CREATE** | `ahimsa-vilasam` | “அஹிம்சா விலாசம்” | “Ahimsa Vilasam” | essays-articles / essay | perumoochu unit 7 (41–48) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 8 | **CREATE** | `thindivanam-theerargaal` | திண்டிவனம் தீரர்காள்! | O Heroes of Tindivanam! | essays-articles / essay | perumoochu unit 8 (49–52) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 9 | **CREATE** | `seval-koovugirathu` | சேவல் கூவுகிறது! | The Rooster Crows! | essays-articles / essay | perumoochu unit 9 (53–56) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 10 | **CREATE** | `maadottigal` | மாடோட்டிகள்! | Cattle-Drivers! | essays-articles / essay | perumoochu unit 10 (57–62) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 11 | **CREATE** | `therthal-kovalan` | தேர்தல் கோவலன்! | Election Kovalan! | essays-articles / essay | perumoochu unit 11 (63–70) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 12 | **CREATE** | `sindhiththunarga-seetramuraadheer` | சிந்தித்துணர்க! சீற்றமுறாதீர்! | Think and Understand! Do Not Grow Angry! | essays-articles / essay | perumoochu unit 12 (71–76) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |
| 13 | **CREATE** | `boom-boom-boom` | பூம்! பூம்! பூம்! | Boom! Boom! Boom! | essays-articles / essay | perumoochu unit 13 (77–80) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate |

#### Essays — `thudikkum-ilamai`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **HOLD** | — | துடிக்கும் இளமை | Throbbing Youth | essays-articles / essay | thudikkum-ilamai unit 1 (5–12) | MIXED_OR_GENRE_UNRESOLVED |  | a delivered speech ('தலைவரே! தாய்மாரே! … வணக்கம்', students' annual day) printed in an essay booklet — shelf decision (Essays vs Speeches) required; no duplicate found |
| 2 | **CREATE** | `annamalaikku-arogara` | அண்ணாமலைக்கு அரோகரா! | Arohara to Annamalai! | essays-articles / essay | thudikkum-ilamai unit 2 (13–19) | UNIQUE_CANONICAL_ESSAY |  | separately titled unit; Kalaignar-authored publication; R1 body-text sweep (8-char shingles + word bigrams vs all poems, essays, 154 stories, 117 speeches, 8 novels, 688 Murasoli letters): no duplicate; title-equals-publication does not apply (publication title is unit 1) |
| 3 | **ADD_WITNESS** | existing `idhaya-perikai` | பூம்புகார் | Poompuhar | speeches / essay | thudikkum-ilamai unit 3 (20–24) | SAME_CANONICAL_ESSAY_ALTERNATE_WITNESS | → witness of existing `idhaya-perikai` | section-level witness of the existing Speeches LibraryWork இதய பேரிகை, section 3 'பூம்புகார் மாநாடு.' (97% of the unit inside it) — do not create |
| 4 | **ADD_WITNESS** | existing `idhaya-perikai` | வெற்றி விளக்கு! | Lamp of Victory! | speeches / essay | thudikkum-ilamai unit 4 (25–29) | SAME_CANONICAL_ESSAY_ALTERNATE_WITNESS | → witness of existing `idhaya-perikai` | section-level witness of the existing Speeches LibraryWork இதய பேரிகை, section 4 'வெற்றி விளக்கு!' (81% of the unit inside it) — do not create |

#### Essays — `sakkaravarththiyin-thirumagan`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **DO_NOT_PROMOTE** | — | சக்கரவர்த்தியின் திருமகன் | Chakravarthi's Son | essays-articles / essay | sakkaravarththiyin-thirumagan unit 1 (9–15) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 2 | **DO_NOT_PROMOTE** | — | தேகமும் உணர்வும் | Body and Feeling | essays-articles / essay | sakkaravarththiyin-thirumagan unit 2 (16–21) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 3 | **DO_NOT_PROMOTE** | — | சதி நிரூபிக்கப்படுகிறது | The Conspiracy Is Proven | essays-articles / essay | sakkaravarththiyin-thirumagan unit 3 (22–25) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 4 | **DO_NOT_PROMOTE** | — | காமராஜன் ஆட்கொண்ட தசரதராஜன்! | Dasaratha Raja in the Grip of Kama-Raja! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 4 (26–29) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 5 | **DO_NOT_PROMOTE** | — | பரத்துவாஜா ஆஸ்ரமமா - பாரிஸ் நகரத்து ‘பாரா’? | Bharadvaja's Ashram—or a Paris 'Bar'? | essays-articles / essay | sakkaravarththiyin-thirumagan unit 5 (30–37) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 6 | **DO_NOT_PROMOTE** | — | இராமன் காட்டேகியது ஏன்? ரிஷியின் சாபமா? கைகேயி கோபமா? | Why Did Rama Go to the Forest? A Rishi's Curse? Kaikeyi's Anger? | essays-articles / essay | sakkaravarththiyin-thirumagan unit 6 (38–42) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 7 | **DO_NOT_PROMOTE** | — | விபீஷணருக்கு விடை யளிப்போம்! | Let Us Answer Vibhishana! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 7 (43–49) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 8 | **DO_NOT_PROMOTE** | — | நாடாண்ட மன்னன் நாதியற்று செத்தான் | The King Who Ruled the Land Died with No One to Tend Him | essays-articles / essay | sakkaravarththiyin-thirumagan unit 8 (50–54) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 9 | **DO_NOT_PROMOTE** | — | தந்தை மகனும் தருமம் தவறியவர்கள்! | Father and Son—Both Strayed from Dharma! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 9 (55–60) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 10 | **DO_NOT_PROMOTE** | — | விஷ்ணு அவதாரம் எனப்படும் ராமனிடம்! | To Rama, Who Is Said to Be Vishnu's Incarnation! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 10 (61–64) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 11 | **DO_NOT_PROMOTE** | — | நடப்பதெல்லாம் நாராயணன் செயலா? | Is Everything That Happens Narayana's Doing? | essays-articles / essay | sakkaravarththiyin-thirumagan unit 11 (65–70) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 12 | **DO_NOT_PROMOTE** | — | மாரீசனைத் துரத்திச் சென்ற ராமனிடம் | To Rama Who Went Chasing Maricha | essays-articles / essay | sakkaravarththiyin-thirumagan unit 12 (71–73) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 13 | **DO_NOT_PROMOTE** | — | துரோகிகள் சந்திப்பு! | Traitors Meet! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 13 (74–78) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |
| 14 | **DO_NOT_PROMOTE** | — | காரியமாகும் வரையில் காலைப் பிடி ! | Hold Their Feet Until Your Purpose Is Achieved! | essays-articles / essay | sakkaravarththiyin-thirumagan unit 14 (79–82) | DEPENDENT_SECTION |  | serial installments of one running rebuttal of Rajaji's Kalki serial: unit 1 announces the series; unit 3 argues from 'சென்ற இதழில்'; 12/14 units carry issue/chapter cross-references; installments follow the Ramayana narrative order — KEEP one work |

#### Essays — `aaru-maatha-kadungkaaval`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **DO_NOT_PROMOTE** | — | முரசு | The Drum | essays-articles / essay | aaru-maatha-kadungkaaval unit 1 (10–65) | DEPENDENT_SECTION |  | three parts (முரசு / களம் / சிறை, 66k/43k/126k chars) of one continuous 1953 prison narrative; unit 1 opens with the June-15 departure; unit 3 opens mid-sentence ('தான், …') — KEEP one work |
| 2 | **DO_NOT_PROMOTE** | — | களம் | The Battlefield | essays-articles / essay | aaru-maatha-kadungkaaval unit 2 (66–106) | DEPENDENT_SECTION |  | three parts (முரசு / களம் / சிறை, 66k/43k/126k chars) of one continuous 1953 prison narrative; unit 1 opens with the June-15 departure; unit 3 opens mid-sentence ('தான், …') — KEEP one work |
| 3 | **DO_NOT_PROMOTE** | — | சிறை | Prison | essays-articles / essay | aaru-maatha-kadungkaaval unit 3 (108–223) | DEPENDENT_SECTION |  | three parts (முரசு / களம் / சிறை, 66k/43k/126k chars) of one continuous 1953 prison narrative; unit 1 opens with the June-15 departure; unit 3 opens mid-sentence ('தான், …') — KEEP one work |

#### Essays — `viduthalai-kilarcci`

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **DO_NOT_PROMOTE** | — | வேங்கையை விரட்டும் படலம் | The Chapter of Driving Away the Tiger | essays-articles / essay | viduthalai-kilarcci unit 1 (4–7) | DEPENDENT_SECTION |  | unit 1 is a prologue that ends 'இது வேங்கையை விரட்டும் படலத்திற்கு அடுத்த படலம்…' leading into unit 2, the publication-titled main body (61 scans) — KEEP one work |
| 2 | **DO_NOT_PROMOTE** | — | விடுதலைக் கிளர்ச்சி | Liberation Uprising | essays-articles / essay | viduthalai-kilarcci unit 2 (8–68) | DEPENDENT_SECTION |  | unit 1 is a prologue that ends 'இது வேங்கையை விரட்டும் படலத்திற்கு அடுத்த படலம்…' leading into unit 2, the publication-titled main body (61 scans) — KEEP one work |

#### மீசை முளைத்த வயதில் (26)

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | **HOLD** | — | பிறையே | O Crescent! | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 1 (2002 1st ed.; 2006 2nd ed.) (18–20) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | existing Fiction LibraryWork நீயும் கைதி - நானும் கைதி (2004 anthology) is a shorter re-edited text contained in this unit (story 91–93% inside) — cross-shelf identity decision required |
| 2 | **HOLD** | — | ஆடிக்காற்று | Aadi Wind | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 2 (2002 1st ed.; 2006 2nd ed.) (21–23) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | existing Fiction LibraryWork ஆடிக் காற்றே! (2004 anthology) is a shorter re-edited text contained in this unit (story 93–95% inside) — cross-shelf identity decision required |
| 3 | **HOLD** | — | கருப்புப் பெண் | Black Woman | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 3 (2002 1st ed.; 2006 2nd ed.) (24–27) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 4 | **HOLD** | — | கடலே | O Sea! | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 4 (2002 1st ed.; 2006 2nd ed.) (28–30) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 5 | **HOLD** | — | ஆறு | River | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 5 (2002 1st ed.; 2006 2nd ed.) (31–33) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 6 | **HOLD** | — | வாழிய வைகறை | Hail the Dawn! | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 6 (2002 1st ed.; 2006 2nd ed.) (34–35) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 7 | **HOLD** | — | அகப்பை சித்தர் | The Ladle Siddhar | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 7 (2002 1st ed.; 2006 2nd ed.) (36–38) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 8 | **HOLD** | — | மலையே வாழி | Hail, Mountain! | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 8 (2002 1st ed.; 2006 2nd ed.) (39–41) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 9 | **HOLD** | — | தளிர் | Tender Shoot | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 9 (2002 1st ed.; 2006 2nd ed.) (42–45) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 10 | **HOLD** | — | விண்மீன் | Star | UNDECIDED / lyrical prose-poem (apostrophic prose paragraphs) | meesai-mulaiththa-vayathil unit 10 (2002 1st ed.; 2006 2nd ed.) (46–48) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 11 | **HOLD** | — | தனிமை | Solitude | UNDECIDED / dialogue prose-poem | meesai-mulaiththa-vayathil unit 11 (2002 1st ed.; 2006 2nd ed.) (49–54) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 12 | **HOLD** | — | நாடக மேடை | The Stage | UNDECIDED / rhapsodic prose-poem (narrow-column rhythmic prose) | meesai-mulaiththa-vayathil unit 12 (2002 1st ed.; 2006 2nd ed.) (55–56) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 13 | **HOLD** | — | புகழ் | Fame | UNDECIDED / aphoristic prose-poem | meesai-mulaiththa-vayathil unit 13 (2002 1st ed.; 2006 2nd ed.) (57–58) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | existing Fiction LibraryWork புகழே நீ ஒரு புதிர் (2004 anthology) is a shorter re-edited text contained in this unit (story 98% inside) — cross-shelf identity decision required |
| 14 | **HOLD** | — | பச்சைக்கிளி | Green Parrot | UNDECIDED / verse poem | meesai-mulaiththa-vayathil unit 14 (2002 1st ed.; 2006 2nd ed.) (59–61) | POSSIBLE_OVERLAP_NEEDS_REVIEW |  | existing Fiction LibraryWork சிறை கொடியது (2004 anthology) is a shorter re-edited text contained in this unit (story 72–78% inside); also = Kavithaigal item 56 (verse) — cross-shelf identity decision required |
| 15 | **HOLD** | — | தமிழே | O Tamil! | UNDECIDED / rhapsodic prose-poem (narrow-column rhythmic prose) | meesai-mulaiththa-vayathil unit 15 (2002 1st ed.; 2006 2nd ed.) (62–62) | MIXED_OR_GENRE_UNRESOLVED |  | no duplicate anywhere in the library (poems, essays, stories, speeches, novels, Murasoli letters); identity cleared; shelf/genre decision pending (author calls the book's pieces 'எழுத்தோவியங்கள்' in the 2002 preface; not essays in form) |
| 16 | **HOLD** | — | தேனலைகள் | Honey Waves | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 16 (2002 1st ed.; 2006 2nd ed.) (63–71) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 1 முத்தாரம் (indicated: unit closes 'முத்தாரம் தொடுத்தார்'; extent fits) by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 17 | **HOLD** | — | தோழி | Friend | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 17 (2002 1st ed.; 2006 2nd ed.) (72–77) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 5 தோழி by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 18 | **HOLD** | — | மருதாணி | Henna | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 18 (2002 1st ed.; 2006 2nd ed.) (78–84) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 6 மருதாணி by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 19 | **HOLD** | — | அருவி | Waterfall | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 19 (2002 1st ed.; 2006 2nd ed.) (85–90) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 7 அருவி by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 20 | **HOLD** | — | முறம் | Winnowing Tray | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 20 (2002 1st ed.; 2006 2nd ed.) (91–95) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 8 முறம் by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 21 | **HOLD** | — | யாழ் | Yaazh | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 21 (2002 1st ed.; 2006 2nd ed.) (96–102) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 9 யாழ் by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 22 | **HOLD** | — | சிற்பி | The Sculptor | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 22 (2002 1st ed.; 2006 2nd ed.) (103–114) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 10 சிற்பி by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 23 | **HOLD** | — | சேவல் சண்டை | Cockfight | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 23 (2002 1st ed.; 2006 2nd ed.) (115–122) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 11 சேவல் சண்டை by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 24 | **HOLD** | — | மடல் | Letter | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 24 (2002 1st ed.; 2006 2nd ed.) (123–128) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 4 மடல் by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 25 | **HOLD** | — | ஆண்டு விழா | Annual Festival | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 25 (2002 1st ed.; 2006 2nd ed.) (129–135) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 12 ஆண்டு விழா by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |
| 26 | **HOLD** | — | மயிலிறகு | Peacock Feather | UNDECIDED / narrative rhythmic-prose piece with dialogue (1958 'அலை' cycle) | meesai-mulaiththa-vayathil unit 26 (2002 1st ed.; 2006 2nd ed.) (136–145) | SOURCE_LIMITED_UNRESOLVED |  | probable counterpart of 1958 தேனலைகள் அலை 2 மயிலிறகு by title + sequence (Meesai 17–23 = அலை 5–11 in order) + proportional extent (~556–776 Meesai chars per 1958 printed page); 1958 source is image-only and untranscribed, so body identity is NOT established — SOURCE_LIMITED; do not label as alternate witness |

#### Existing publications / one-work entries

| # | Decision | Canonical id | Tamil title | English title | Shelf / type | Source unit (scans) | Classification | Witnesses / relations | Evidence |
|---:|---|---|---|---|---|---|---|---|---|
|  | **KEEP_EXISTING** | existing `kaalap-pezhaiyum-kavithai-saaviyum` | காலப் பேழையும் கவிதைச் சாவியும் | The Casket of Time and the Key of Poetry | poetry / (existing) | kaalap-pezhaiyum-kavithai-saaviyum | EXISTING_LIBRARY_WORK |  | publication container (58 items) — retained; becomes publication/witness context for its promoted poems |
|  | **KEEP_EXISTING** | existing `kalaignarin-kavithaigal` | கலைஞரின் கவிதைகள் | Kalaignar's Poems | poetry / (existing) | kalaignarin-kavithaigal | EXISTING_LIBRARY_WORK |  | publication container (77 items; 5 groups) — retained as publication/witness context |
|  | **KEEP_EXISTING** | existing `kalaignarin-kaviyaranga-kavithaigal-1975` | கலைஞரின் கவியரங்கக் கவிதைகள் | Kalaignar's Poetry-Gathering Poems (1975) | poetry / (existing) | kalaignarin-kaviyaranga-kavithaigal-1975 | EXISTING_LIBRARY_WORK |  | publication container (items 01/02/04 + 5 represented ranges) — retained as publication/witness context |
|  | **KEEP_EXISTING** | existing `oruthalaik-kathal` | ஒருதலைக் காதல் | One-Sided Love | poetry / (existing) | oruthalaik-kathal | EXISTING_LIBRARY_WORK |  | ONE verse novel; 11 dependent sections (R0) — its section 1 is reprinted as Kaalap item 37 (HOLD) |
|  | **KEEP_EXISTING** | existing `ina-muzhakkam` | இன முழக்கம் | The Clarion Call of the Race | essays-articles / (existing) | ina-muzhakkam | EXISTING_LIBRARY_WORK |  | mixed publication — retained as publication context |
|  | **KEEP_EXISTING** | existing `unarchchimaalai` | உணர்ச்சிமாலை | Garland of Emotion | essays-articles / (existing) | unarchchimaalai | EXISTING_LIBRARY_WORK |  | publication container — retained |
|  | **KEEP_EXISTING** | existing `thiraavida-sampaththu` | திராவிட சம்பத்து | Dravidian Wealth | essays-articles / (existing) | thiraavida-sampaththu | EXISTING_LIBRARY_WORK |  | publication container — retained |
|  | **KEEP_EXISTING** | existing `kolaikkalam` | கொலைக்களம்! | The Killing Field | essays-articles / (existing) | kolaikkalam | EXISTING_LIBRARY_WORK |  | publication container — retained |
|  | **KEEP_EXISTING** | existing `sinthanaiyum-seyalum` | சிந்தனையும் செயலும் | Thought and Action | essays-articles / (existing) | sinthanaiyum-seyalum | EXISTING_LIBRARY_WORK |  | publication container — retained |
|  | **KEEP_EXISTING** | existing `perumoochu` | பெருமூச்சு | The Deep Sigh | essays-articles / (existing) | perumoochu | EXISTING_LIBRARY_WORK |  | publication container — retained |
|  | **KEEP_EXISTING** | existing `thudikkum-ilamai` | துடிக்கும் இளமை | Restless Youth | essays-articles / (existing) | thudikkum-ilamai | EXISTING_LIBRARY_WORK |  | mixed publication (speech + essay + speech-section witnesses) — retained |
|  | **KEEP_EXISTING** | existing `meesai-mulaiththa-vayathil` | மீசை முளைத்த வயதில் | At the Age the Moustache Sprouted | essays-articles / (existing) | meesai-mulaiththa-vayathil | EXISTING_LIBRARY_WORK |  | publication container — retained; all 26 units HOLD |
|  | **KEEP_EXISTING** | existing `sakkaravarththiyin-thirumagan` | சக்கரவர்த்தியின் திருமகன் | Chakravarthi's Son | essays-articles / (existing) | sakkaravarththiyin-thirumagan | EXISTING_LIBRARY_WORK |  | ONE serialized work (14 dependent installments) |
|  | **KEEP_EXISTING** | existing `aaru-maatha-kadungkaaval` | ஆறுமாதக் கடுங்காவல் | Six Months of Rigorous Imprisonment | essays-articles / (existing) | aaru-maatha-kadungkaaval | EXISTING_LIBRARY_WORK |  | ONE continuous prison narrative (3 dependent parts) |
|  | **KEEP_EXISTING** | existing `viduthalai-kilarcci` | விடுதலைக் கிளர்ச்சி | The Freedom Uprising | essays-articles / (existing) | viduthalai-kilarcci | EXISTING_LIBRARY_WORK |  | ONE work (prologue + main body) |
|  | **KEEP_EXISTING** | existing `pesum-kalai-valarppom` | பேசும் கலை வளர்ப்போம் | Let Us Cultivate the Art of Speaking | essays-articles / (existing) | pesum-kalai-valarppom | EXISTING_LIBRARY_WORK |  | ONE work, 19 dependent numbered sections (R0); note: its section 6 contains 96% of the existing Fiction work நடக்குமா நடக்காதா? (2008 anthology) — EXCERPT relation recorded, no action |
|  | **KEEP_EXISTING** | existing `kayittril-thongiya-kanapathi` | கயிற்றில் தொங்கிய கணபதி | Ganapathi Who Hung from the Rope | essays-articles / (existing) | kayittril-thongiya-kanapathi | EXISTING_LIBRARY_WORK |  | single article (R0) |
|  | **KEEP_EXISTING** | existing `kudumbaththin-nalvilakku` | குடும்பத்தின் நல்விளக்கு | The Good Lamp of the Family | essays-articles / (existing) | kudumbaththin-nalvilakku | EXISTING_LIBRARY_WORK |  | single-article pamphlet (R0) |
|  | **KEEP_EXISTING** | existing `vedhanai-ch-siraiyinindrum-viduthalai-pera` | வேதனைச் சிறையினின்றும் விடுதலை பெற | To Win Release from the Prison of Suffering | essays-articles / (existing) | vedhanai-ch-siraiyinindrum-viduthalai-pera | EXISTING_LIBRARY_WORK |  | single message (R0) |
|  | **ADD_WITNESS** | existing `idhaya-perikai` | இதய பேரிகை | Idhaya Perikai | speeches / (existing) | idhaya-perikai | EXISTING_LIBRARY_WORK | thudikkum-ilamai unit 3 பூம்புகார் → section 3 'பூம்புகார் மாநாடு.' [NEW]; thudikkum-ilamai unit 4 வெற்றி விளக்கு! → section 4 'வெற்றி விளக்கு!' [NEW] | existing Speeches work (7 headed sections, R0 keep); receives two section-level witnesses |

## 14. Projected post-R2 catalogue arithmetic (calculated, not implemented)

**Assumption A (additive; preservation-first).** R2 creates every CREATE entry. Every existing LibraryWork is
retained, including the publication containers, as publication and witness context. No HOLD is created.

```
New Poetry works      = Kaalap 57 + Kavithaigal 72 + 1975 3 + ina poems 3      = 135
New Essays works      = unarchchimaalai 9 + thiraavida 2 + kolaikkalam 6
                        + sinthanaiyum 48 + perumoochu 13 + thudikkum 1 + ina essays 4 = 83
New works from ina    = 4 essays + 3 poems                                     =   7 (included above)
Promotable Meesai     = 0 now (11 identity-cleared pending one shelf decision; 15 blocked)
HOLD                  = 35
Total CREATE          = 135 + 83                                               = 218

Projected catalogue   = 335 + 218 = 553
  Life Writing 1 · Letters 1 · Fiction 162 · Poetry 14 + 135 = 149 · Drama 11 · Cinema Writing 10
  · Speeches 117 · Essays & Articles 15 + 83 = 98 · Literary Commentary 4
  1 + 1 + 162 + 149 + 11 + 10 + 117 + 98 + 4 = 553
```

**Existing works gaining NEW witnesses:** 3.
- `idhayathai-thanthidu-anna` (+1975 scans 9–20);
- `gunanayagar-nehru` (+ Kavithaigal 19, + 1975 scans 21–32);
- `idhaya-perikai` (+ thudikkum 3, 4 at section level).

`thennan-kathai` keeps its live witness with nothing new.

**New works created with witnesses attached:** 10 (Kavithaigal 06, 17, 26, 39, 49, 50, 51, 53, 54, 55).

**The HOLD range is not frozen.** Resolving the 35 HOLD units could add between 0 and 35 works, depending on the owner
decisions in §11 (several resolve to witnesses rather than works). The projection is therefore **553 (floor), up to 588**.

**Modelling note (R2's decision, not R1's).** R2 might instead turn a fully decomposed container publication into a
publication view rather than a LibraryWork. That would reduce the total by the number so converted. R1 does not decide
this, and no existing LibraryWork is proposed for removal.

## 15. Explicit exclusions

**Not promoted:**
- the 11 Oruthalaik sections;
- the 19 pesum-kalai sections;
- the three single-article Essays works;
- the 14 சக்கரவர்த்தியின் திருமகன் installments;
- the 3 ஆறுமாதக் கடுங்காவல் parts;
- the 2 விடுதலைக் கிளர்ச்சி parts;
- the ina `கவிதைகள்` container heading.

**Not in scope:**
- all Fiction, Speeches, Drama, Literary Commentary, Letters and Life Writing works (R0);
- Cinema song identity (deferred);
- the external 1968 `விடுதலை வீரர்கள் ஐவர்` volume (recorded as a witness, not onboarded);
- the Bharathiar University English books (secondary witnesses only).

**Not included:**
- 1975 ordinal 03 (Rajaji);
- scans 69–70 (Bharathidasan).

## 16. Preservation constraints

- Every existing public route stays valid:
  - `/poems/<publication>/<item>`;
  - `/essays/<publication>/articles/<unit>`;
  - `/stories/…`, `/speeches/…`;
  - every `/source` page.
- A later phase adds canonical-work routes and keeps publication-unit routes as witness or publication routes, or as
  aliases.
- Existing LibraryWork ids and slugs are unchanged. Proposed ids never reuse an existing id, slug or collection id.
- Existing witness relations (`POETRY_WITNESS_RELATIONS`, 2) remain. New relations are additive.
- Witness texts are never merged or normalised: the Thennan scan-151 exception, 1968 variants, 1951 ina variants and
  Meesai variants all stay attached to their own witness.
- Source conditions and qualifications carry over unchanged.

## Status

**READING ROOM IA v2 R1 — IDENTITY RECONCILIATION COMPLETE / REVIEW-READY.** Implementation, source and production
deltas are all 0.

**R2 — NOT STARTED / NOT AUTHORIZED.** R2 (implementation) requires independent review of this record and explicit owner
authorization. HOLD items require owner decisions (§11) before they can enter R2.
