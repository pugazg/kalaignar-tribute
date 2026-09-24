# Reading Room IA v2 — R0 Classification Census

**Created:** 2026-09-24.

**Status: READING ROOM IA v2 R0 — CLASSIFICATION CENSUS COMPLETE / REVIEW-READY.**
**R1 — NOT STARTED / NOT AUTHORIZED BY THIS R0.**

This record is **control-only and assessment-only**:
- implementation delta = **0**;
- source delta = **0**;
- production mutation = **0**.

Live GitHub and production are authoritative. Every count below was re-derived from the live implementation
registries at the pinned commit (§1), not copied from the authorizing prompt. Every structural claim cites the
live payload or the pinned source document it rests on.

Reading Room IA v2 is a **newly owner-authorized initiative**, separate from the onboarding waves:
- Waves 6, 7 and 8 remain **COMPLETE / CLOSED / FROZEN at P5**. This record does not reopen or rename them.
- It does not edit any wave census or P5 acceptance record.
- It changes no catalogue entry, route, sitemap, reader or collection behaviour.

---

## 1. Authoritative live pins

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this record) | `78888627be63b9b3d4e04afd8908cb4d17d82d59`, tree `af291166b646d89591610e480cb2d4f4bde54c6a` (merge of Wave-8 P5 control PR #39) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `f991043c3353abe9f2b334f7c8d57e433184d126`, tree `87ca371b084c337ba2163caa6c336615174074e9`. Compare with the accepted Wave-8 boundary: identical, ahead 0. 0 open PRs. |
| Production | `https://nenjukkuneethi.org`, still Vercel Production deployment `6638432286` for `f991043c…` (no deploy in R0) |
| Files read (live, at `f991043c`) | `data/library.ts`, `data/collections.ts`, `data/wave6-b7-catalogue.ts`, `data/wave7-b5-b6-k-catalogue.ts`, `components/LibraryHome.tsx`, `app/read/page.tsx`, `data/poems.ts`, and `public/data/essays/*/publication.json`, `public/data/speeches/1971-namathu-vilakkam/*` |

Source documents consulted, read-only, each at the pin the implementation records for that work:

| Repository | Pin | Tree | Used for |
|---|---|---|---|
| `pugazg/kalaignar-poems` | `969823195ea8943a67fad4286ab1bc7f1c876d56` | `e382ee02c8f333da9ddfd61f3c9858b97c65cf3b` | Kaalap Pezhai, Kalaignarin Kavithaigal |
| `pugazg/kalaignar-poems` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` (= live `main`) | `fb35686d8313db5e99ff49e7c28cb4decfc1c429` | 1975 poetry-gathering book, Oruthalaik Kathal |
| `pugazg/kalaignar-essays` | `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` | — | Pesum Kalai Valarppom, Meesai Mulaiththa Vayathil |
| `pugazg/kalaignar-assembly-speeches` | `7a7fed1d0e3eb24a396effc10854b178f32bd0cf` | — | நமது விளக்கம் |

## 2. Owner-authorized product direction (recorded, not implemented)

The Reading Room is to move toward:

```
Reading Room  →  Category  →  Individual canonical work  →  reading units
```

Today the `/read` landing page mixes shelf headings, individual works and source-publication collections. The
direction replaces that mix with the hierarchy above.

- A source publication or anthology must **not** replace independently readable member works in normal
  discovery.
- Collections and publications may remain as any of the following:
  - provenance / publication history;
  - an alternate "browse this edition/anthology" surface;
  - a meaningful ordered grouping;
  - a genuinely dependent reading structure.
- Collection membership **by itself** must not make a canonical work disappear from category browsing.
- Existing public URLs and citation identities are **preservation constraints** (§11).

**Tamil shelf label.** The reader-facing label `வாழ்க்கை எழுத்து` is rejected as awkward, and the proposed public
Tamil label is **`சுயசரிதை`**. The stable internal shelf id `life-writing` is **not** renamed in R0. The live
`SHELVES` label is still `வாழ்க்கை எழுத்து` / "Life Writing".

## 3. Live baseline (re-derived)

From `publishedWorks()`, `LIBRARY_COLLECTIONS` and `discoveryShelves()` at `f991043c`:

| Shelf (id) | Live Tamil / English label | Works | Discovery entries | of which collection cards | Initially visible |
|---|---|---:|---:|---:|---:|
| `life-writing` | வாழ்க்கை எழுத்து / Life Writing | 1 | 1 | 0 | 1 |
| `letters` | கடிதங்கள் / Letters | 1 | 1 | 0 | 1 |
| `fiction` | புனைகதை / Fiction | 162 | 20 | 7 | 6 |
| `poetry` | கவிதைகள் / Poetry | 14 | 14 | 0 | 6 |
| `drama` | நாடகங்கள் / Drama | 11 | 11 | 0 | 6 |
| `cinema-writing` | திரை எழுத்து / Cinema Writing | 10 | 10 | 0 | 6 |
| `speeches` | உரைகள் / Speeches | 117 | 22 | 2 | 6 |
| `essays-articles` | கட்டுரைகள் / Essays & Articles | 15 | 15 | 0 | 6 |
| `literary-commentary` | இலக்கிய உரை / Literary Commentary | 4 | 4 | 0 | 4 |
| **Total** | | **335** | **98** | **9** | **42** |

```
335 = 1 + 1 + 162 + 14 + 11 + 10 + 117 + 15 + 4
LIBRARY_WORKS = 335 · all published · 335 unique ids · 335 unique slugs
LibraryCollections = 9
Initially visible = Σ min(6, entries per shelf) = 1+1+6+6+6+6+6+6+4 = 42
```

## 4. Current discovery behaviour and collection-substitution arithmetic

The behaviour is in `discoveryShelves()` (`data/collections.ts`) and `LibraryHome` (`INITIAL_WORKS_PER_SHELF = 6`).
For each shelf, the entry list is built as follows:

1. **every collection on that shelf comes first**, as one card each;
2. then come the shelf's works, **excluding any work for which `collectionsForWork(id).length > 0`**, meaning
   membership in one *or more* collections;
3. the first 6 entries render as cards, and the rest sit in a native `<details>` "Show N more" disclosure.

The shelf heading still counts **works**, for example "162 works · 7 collections". The collection cards therefore
**substitute** for their member works in `/read` discovery.

**The member works are not missing from the catalogue.** Each is a published canonical `LibraryWork` with its
own route, `/source` provenance, citation identity and sitemap entry. They are hidden **only** by the current
discovery policy.

| | Fiction | Speeches | Total |
|---|---:|---:|---:|
| Collections (cards) | 7 | 2 | **9** |
| Member slots across collections | 162 | 97 | 259 |
| **Unique member works hidden by substitution** | **149** | **97** | **246** |
| Works not in any collection (standalone discovery cards) | 13 | 20 | 33 |

```
335 − 246 + 9 = 98   (current discovery entries)
```

- **Fiction breakdown.**
  - The 149 hidden works are **145 short stories + 4 novels**. The 4 novels are the members of `arumbu-1978`:
    `arumbu`, `sarapallam-samundi`, `periya-idathup-pen`, `nadutheru-narayani`.
  - The 13 standalone works are:
    - 9 short stories: `kizhavan-kanavu`, `seerazhitha-sirippu`, `madurai-selavu`, `kondru-varuga`,
      `naattiya-kalarani`, `maanam`, `neruppu`, `vilaiyal-vangalaiyo`, `nanbana`;
    - 4 novels: `balipeedam-nokki`, `pudhaiyal`, `surulimalai`, `vellikkizhamai`.
- **Speeches breakdown.**
  - The 97 hidden works are all members of `muthukkuliyal-part-1` (61) or `muthukkuliyal-part-2` (36). The two
    sets do not overlap.
  - The 20 standalone works are 15 assembly speeches + 5 public speeches: `poonthottam`, `arappor`,
    `kalaivanar-nsk-memorial-day`, `idhaya-perikai`, `palli-vazhkkai`.
- **Plural membership.** 259 slots − 246 unique = **13** works that belong to two collections. Each is still
  **one** canonical work.
  - 11 are the 1977 canonicals reprinted in the 2009 anthology: `pugazhendhi`, `nalayini`, `kuppai-thotti`,
    `sangilichami`, `thappivittargal`, `thappavillai`, `ezhai`, `kannadakkam`, `vazha-mudiyathavargal`,
    `ayyo-raja`, `sumanthaval`.
  - `jaadi-kutti-poduma` belongs to 1987 + 2008.
  - `kuruvi-rameswaram` belongs to 1987 + 2004.

## 5. The nine current collections

All 9 use `kind: "anthology"`, the only kind the type admits. For every collection:
- `memberCount.value` = member rows = unique members;
- every member resolves to a published `LibraryWork`;
- ordinals are carried on all members except `arumbu-1978`, whose source establishes no member numbering.

| # | Collection id | Shelf | Title | Members |
|---:|---|---|---|---:|
| 1 | `1977-kalaignar-karunanidhiyin-sirukathaigal` | Fiction | கலைஞர் கருணாநிதியின் சிறுகதைகள் | 37 |
| 2 | `1982-mudiyatha-thodarkathai` | Fiction | முடியாத தொடர்கதை | 6 |
| 3 | `1987-kalaignar-sonna-kuttik-kathaigal` | Fiction | கலைஞர் சொன்ன குட்டிக் கதைகள் | 25 |
| 4 | `2004-kalaignarin-kuttik-kathaigal` | Fiction | கலைஞரின் குட்டிக் கதைகள் | 34 |
| 5 | `2008-kalaignar-sonna-kathaigal` | Fiction | கலைஞர் சொன்ன கதைகள் | 40 |
| 6 | `2009-16-kathaiyinile` | Fiction | 16 கதையினிலே | 16 |
| 7 | `arumbu-1978` | Fiction | அரும்பு (1978 தொகுப்பு) | 4 |
| 8 | `muthukkuliyal-part-1` | Speeches | முத்துக் குளியல் — பாகம் I | 61 |
| 9 | `muthukkuliyal-part-2` | Speeches | முத்துக் குளியல் — பாகம் II | 36 |

**R0 conclusion.** None of the nine collection objects establishes a dependency that warrants suppressing its
members from normal category discovery.
- Every member is an independently readable, independently routed canonical work.
- The collection itself is a publication grouping: an edition, anthology or printed contents order. It is
  historically and source-meaningful, but it is not a reading structure its members depend on.
- R1 should treat the nine as **secondary collection/publication views** (provenance, "Published in / Appears
  in", and optional edition browsing), **not** as substitutes for member `LibraryWork`s.
- **Plural membership must be preserved.** A work appearing in more than one source publication stays one
  canonical work, with each publication recorded as context (§4).

## 6. Shelf-by-shelf classification

### 6.1 Life Writing — 1 work

`nenjukku-neethi` (`memoir`, reader `volume-chapter`, 391 chapters across the six volume indexes
`volume1…6.index.json`).

- **KEEP one canonical work.** Its volumes and chapters remain dependent internal reading units.
- The proposed reader-facing Tamil shelf label is **`சுயசரிதை`**. The internal id `life-writing` is not renamed
  at R0.

### 6.2 Letters — 1 work

`murasoli-letters` (`letters`, reader `letter`): Volumes 42–54, 13 volumes, 688 letters, 5141 physical pages
(Wave-8 P5 acceptance).

- **KEEP the current canonical corpus/work identity** for R0.
- Individual letters already have stable routes (`/murasoli/<id>`) and reading identity. The route id is
  identity; the printed number is not.
- **Do not explode the 688 letters into LibraryWorks** during this initiative without separate owner
  authorization.
- Corpus navigation by volume and sequence is legitimate here. It should be handled specially on the Letters
  category page.

### 6.3 Fiction — 162 works

Re-derived: **154 short stories** (`short-story` / reader `story`) + **8 novels** (`novel` / reader `novel`) =
**162**.

- Every short story is an independent canonical work.
- Every novel is an independent canonical work. Novel chapters and sections remain dependent reading units.
- Anthology membership is provenance and alternate-publication context. It must not suppress the member in
  normal discovery.
- The seven Fiction collections remain useful secondary publication views, not primary identities.
- `arumbu-1978` groups four **novels**. That grouping is publication context only; the four stay four works,
  and `arumbu` and `nadutheru-narayani` stay distinct.

### 6.4 Speeches — 117 works

Re-derived: **117** canonical speech works (102 `public-speech` + 15 `assembly-speech`; reader `speech` for all).

- All 117 remain independently discoverable.
- `முத்துக் குளியல்` Part I / Part II remain publication/anthology context for their 97 member speeches. Those
  97 must not be represented **only** by two collection cards.
- **Source-faithful exception: `1971-namathu-vilakkam` / நமது விளக்கம்.**
  - The booklet's introduction records two House replies: **Legislative Assembly 29-6-1971** and **Legislative
    Council 30-6-1971**.
  - The body (scans 4–60) is printed as one continuous editorial unit, with "no securely printed internal
    House divider". That is the wording of
    `kalaignar-assembly-speeches@7a7fed1d:speeches/1971/1971-namathu-vilakkam/README.md` and
    `sources/1971-namathu-vilakkam/house-date-evidence.md`.
  - The live payload preserves it as "one edited two-House witness" with `date: null`.
  - **KEEP one canonical source-faithful work.** Do not invent two ranges, and do not split it into two
    LibraryWorks from the two dates.
- **`udhaya-kathir`** (1970 no-confidence reply; 29 sections) remains **one** speech/work with its internal
  sections.

### 6.5 Drama — 11 works

All 11 are `stage-play`: `silappathikaram-nataka-kappiyam`, `bharathayanam`, `anarkali`, `socrates`,
`cheran-senguttuvan`, `kagithapoo`, `manimagudam`, `thiruvalar-desiyampillai`, `iratha-kanneer`, `nachuk-koppai`,
`ore-mutham`.

- All remain independent canonical works. Scenes and reading units are dependent.
- **No semantic split is proposed.** Ore Mutham's 30 + 3 separately numbered scenes stay internal to one work.

### 6.6 Literary Commentary — 4 works

- `tholkappiya-poonga` (reader `commentary-unit`);
- `thirukkural-kalaignar-urai` (reader `kural-commentary`, 1330 Kurals);
- `kuraloviyam` (`commentary-unit`, 300 entries);
- `sangatamil` (`commentary-unit`, 104 reading sections).

All four remain canonical works. Commentary units, Kurals and sections remain internal reading units. **Do not
promote hundreds of commentary units to LibraryWorks** in this initiative.

### 6.7 Cinema Writing — 10 works (observation only; outside R1)

The owner-authorized redesign covers Fiction, Poetry, Speeches and Essays discovery. It is **not** broadened into
a Cinema implementation.

- **Future-review observation only:** `kalaignar-thirai-isai-paadalgal` (`film-song-collection`, 54 songs) is
  structurally a collection of individual lyrics. It may deserve a future canonical-song identity review. That
  review is **DEFERRED / OUTSIDE R1**.
- The other nine cinema books remain publication/work identities with dependent scenes or segments:
  - `manohara`, `parasakthi`, `tirumbippaar`, `raja-rani`, `ammaiyappan`, `maruthanattu-ilavarasi`,
    `vandikkaran-magan`, `naam` (reader `scene`);
  - `manthiri-kumari` (reader `film-booklet`).

### 6.8 Poetry — 14 works (no post-migration count frozen)

The live catalogue has 10 `poem` works and 4 `poetry-publication` works.

**Ten standalone poems** remain canonical independent poems:
`idhayathai-thanthidu-anna`, `anaiya-vilakku-anna`, `marathi`, `thennan-kathai`, `thalaikettan-thambi`,
`aanthaiyum-arasanum`, `poomudi`, `anna-kaviyarangam`, `gunanayagar-nehru`, `kanchithan-annan`.

**Three publication containers whose source establishes independently addressable poem units:**

1. **`kaalap-pezhaiyum-kavithai-saaviyum`** — 58 / 58 items.
   - The source `poems/kaalap-pezhaiyum-kavithai-saaviyum/indexes/item-title-map.md` (at `96982319`) states:
     - "Each numbered item is a separate poem/work unit …";
     - "Do not collapse the 58 items into one undifferentiated assembled poem."
   - The live catalogue also keeps a title-witness register of 14 items whose contents and title-page titles
     differ, stored as separate witnesses.
   - **R0: CONTAINER OF INDEPENDENT POEMS — PROMOTION CANDIDATE.**
2. **`kalaignarin-kavithaigal`** — 77 / 77 items.
   - The source (`PHASE3_CANONICAL_ASSEMBLY.md`, `README.md`, at `96982319`) records the history. An earlier
     whole-volume file "was structurally inappropriate for this anthology and has been removed". The corrected
     model is "one stable numeric canonical file per indexed poem/item" (`sections/01.md` … 77 files).
   - **R0: ANTHOLOGY OF INDEPENDENT POEMS — PROMOTION CANDIDATE.**
   - **Known canonical overlaps with standalone works.** `POETRY_WITNESS_RELATIONS` in `data/poems.ts` declares
     exactly two, each `same-canonical-poem-alternate-witness`:
     - `idhayathai-thanthidu-anna` ↔ item `give-me-your-heart-anna` (இதயத்தைத் தந்திடு அண்ணா);
     - `thennan-kathai` ↔ item `the-tale-of-the-southerner` (தென்னவன் காதை).
   - These must become **multiple publication witnesses of ONE canonical poem**, never duplicate LibraryWorks.
   - R1 must run a full title/source/cross-witness de-duplication over all 77 items (and the 58 Kaalap items)
     before any catalogue arithmetic. The two declared relations are "at least", not "exactly".
3. **`kalaignarin-kaviyaranga-kavithaigal-1975`** — 3 active Kalaignar items, intake ordinals **01, 02, 04**.
   - The source README (at `188d49cd`) declares "NEW-ITEM-ONLY SCOPE".
   - Ordinal 03, on scan 66, is "a non-Kalaignar Rajaji source/context insert and is not canonical Kalaignar
     material" (`PHASE3_BOUNDARY_JOIN_AUDIT.md`). Scans 69–70 are Bharathidasan.
   - The ranges "9–20, 21–32, 33–45, 71–77, 78–84 remain skip-only" as already represented (`SOURCE_INTAKE.md`),
     so they were deliberately not reopened.
   - **R0: 3 INDEPENDENT POEM WORKS / SOURCE-WITNESS PUBLICATION — PROMOTION CANDIDATE.**

**Exception: `oruthalaik-kathal` — KEEP one canonical LibraryWork.**
- The live catalogue records "A verse-novel publication: 11 source sections (not 11 independent poems)".
- The source README (at `188d49cd`) describes one illustrated work: 101 scans, "canonical sections 11/11",
  "95/95 = 84 text-bearing + 11 illustration-only", and a "full-work editorial-consistency review".
- Its 11 sections remain dependent sections.

**No final post-migration Poetry work count is frozen at R0.** Cross-witness identity reconciliation must come
first.

### 6.9 Essays & Articles — 15 works (no post-migration count frozen)

The live `subtype` values are 10 `essay-collection`, 3 `essay` and 2 `single-article-pamphlet`, and all 15 use
reader `article`. `subtype` alone is **not** trusted: classification below comes from the unit structure in each
`public/data/essays/<pub>/publication.json`. That structure totals **158 units**.

**Single / source-coherent works — KEEP one canonical work each:**

| Work | Units | Basis |
|---|---:|---|
| `kayittril-thongiya-kanapathi` | 1 | one article |
| `kudumbaththin-nalvilakku` | 1 | one-article pamphlet |
| `vedhanai-ch-siraiyinindrum-viduthalai-pera` | 1 | one message/publication |
| `pesum-kalai-valarppom` | 19 | one coherent work, detailed below |

`pesum-kalai-valarppom`:
- Its 19 units are untitled `source-section`s (`section-01`…`19`).
- The source `P3_ASSEMBLY_AUDIT.md` (at `b5fd2922`) records "only source-visible numbered headings 1–19 are used;
  no descriptive titles were invented".
- The same audit records **12** intentional shared (mid-page) transition scans: 12, 16, 22, 27, 31, 34, 38, 51,
  55, 67, 70, 79.
- **KEEP one work.** The 19 sections remain dependent reading units.

**Publication containers of separately assembled, titled article/prose units:**

| Work | Titled units | Live `subtype` |
|---|---:|---|
| `sakkaravarththiyin-thirumagan` | 14 | essay-collection |
| `unarchchimaalai` | 10 | **essay** (subtype understates the structure) |
| `thiraavida-sampaththu` | 2 | **essay** (subtype understates the structure) |
| `kolaikkalam` | 6 | essay-collection |
| `sinthanaiyum-seyalum` | 50 | essay-collection |
| `aaru-maatha-kadungkaaval` | 3 | essay-collection |
| `thudikkum-ilamai` | 4 | essay-collection |
| `perumoochu` | 13 | essay-collection |
| `viduthalai-kilarcci` | 2 | essay-collection |

**R0: PUBLICATION CONTAINER OF INDEPENDENT TITLED UNITS — PROMOTION CANDIDATE**, subject to de-duplication and
authorship checks before R1 creates any canonical work identity.
- In several containers, a unit carries the publication's own title:
  - unit 1: `sakkaravarththiyin-thirumagan`, `thiraavida-sampaththu`, `thudikkum-ilamai`, `perumoochu`,
    `kolaikkalam`, `unarchchimaalai` (as `உணர்ச்சி மாலை`), and the mixed `ina-muzhakkam`;
  - unit 2: `viduthalai-kilarcci`.
- R1 must distinguish a promoted title-unit's identity from the publication's.

**Mixed publication: `ina-muzhakkam` — 6 top-level units.**
- Units 1–5 are prose/article units: இன முழக்கம், சொர்க்க லோகத்தில், முரசறைவாய், பழிக்குப் பழி, ஆரியம் பேசுகிறது.
- Unit 6 is `கவிதைகள்`. The live payload preserves **11** poem subheadings inside it: நியாயத் திராசு!, ஏற்பரோ!,
  சைவரே!, வா!, பொதுவுடைமையே!, யோசித்துப் பார்!, மாணவர் எழுச்சி., வாளிங்கே!, தோல்வி எப்பொழுது?, இன்னுமா
  கூச்சல்?, வருணமா? மரணமா?.
- **R0: MIXED PUBLICATION.** R1 must not create six "essay" works blindly. It should evaluate the first five as
  essay candidates and the 11 titled poems as **Poetry** candidates, with publication provenance retained.

**Genre/identity review: `meesai-mulaiththa-vayathil` — 26 separately titled canonical assemblies.**
- Titles include பிறையே, ஆடிக்காற்று, கடலே, ஆறு, விண்மீன், தமிழே, யாழ்.
- The source stores them under the essays repository's `publications/meesai-mulaiththa-vayathil/articles/`, a
  frozen tree of 26 files at `b5fd2922`.
- Sample bodies have a lyrical, prose-poetic form (for example, unit 1 opens *"பிறையே! வானக் கடலலையின் நுரையே!"*).
- Meesai unit 16 is titled `தேனலைகள்`.
- The frozen Wave-6 records establish a cross-repository representation/overlap between the 1958 book
  `தேனலைகள்` (12 mapped headings) and `மீசை முளைத்த வயதில்`.
- R0 does **not** establish:
  - which of the 12 headings correspond to which of the 26 Meesai units;
  - whether the relationship is one-to-one, partial, or at publication level.
- No identity is inferred from the shared title alone (§8, item 4).
- **R0: 26 INDEPENDENTLY TITLED UNITS — CANONICAL-IDENTITY CANDIDATES; FINAL SHELF/GENRE NOT YET DECIDED.** They
  are not relabelled as poems or essays at R0. R1 requires an explicit source/genre assessment before assigning a
  shelf.

**Slug uniqueness is not canonical uniqueness.** A slug-level comparison across all 158 live essay units found
**0** duplicate unit slugs across publications. This is **not** sufficient to prove canonical uniqueness. R1 must
compare titles, source witnesses, authorship and reprint relationships before creating any new LibraryWork (see
§8, item 4).

**No final post-migration Essays count is frozen at R0.**

## 7. Exact known exceptions (keep as one work)

| Work | Shelf | Why it stays one canonical work |
|---|---|---|
| `nenjukku-neethi` | Life Writing | volumes/chapters are dependent units |
| `murasoli-letters` | Letters | corpus identity kept; 688 letters stay routed units (no explosion without separate authorization) |
| `1971-namathu-vilakkam` | Speeches | one continuous edited two-House booklet; no printed House divider |
| `udhaya-kathir` | Speeches | one speech with 29 internal sections |
| `oruthalaik-kathal` | Poetry | one illustrated verse novel; 11 sections, not 11 poems |
| `pesum-kalai-valarppom` | Essays | one work; untitled source-numbered sections 1–19 with 12 mid-page transitions |
| `kayittril-thongiya-kanapathi`, `kudumbaththin-nalvilakku`, `vedhanai-ch-siraiyinindrum-viduthalai-pera` | Essays | single article / pamphlet / message |
| all 11 Drama, all 4 Literary Commentary, all 10 Cinema works | — | scenes / commentary units / segments are dependent (Cinema song identity deferred) |

## 8. Unresolved identity questions (for R1; not decided here)

1. **Poetry cross-witness de-duplication.** Kaalap's 58 and Kavithaigal's 77 items must be reconciled against the
   10 standalone poems and against each other. At least two overlaps are declared (இதயத்தைத் தந்திடு அண்ணா, தென்னவன்
   காதை). A full title/source audit is required.
2. **The 1975 book's "already represented" ranges** (scans 9–20, 21–32, 33–45, 71–77, 78–84). R0 does not
   establish which canonical works or witnesses represent them. R1 must map them before promoting items 01, 02
   and 04, so that nothing is duplicated.
3. **`ina-muzhakkam`**: essay identity for units 1–5, and Poetry identity for the 11 poems in unit 6.
4. **`meesai-mulaiththa-vayathil`**: shelf/genre of 26 units, plus a recorded cross-repository overlap whose
   exact relationship is unresolved.
   - The frozen Wave-6 records (`WAVE6_COMPLETED_WORKS_CENSUS.md`, `WAVE6_BATCH7_SHORT_STORIES.md`, `HANDOVER.md`)
     say the 1958 book **`தேனலைகள்`** (`TVA_BOK_0064030`, short-stories `collections/1958-thenalaigal`, 12 mapped
     headings, transcription deferred) is "already represented in the essays / கட்டுரைகள் workstream under
     `மீசை முளைத்த வயதில்`". It was therefore excluded from the short-story backlog.
   - Meesai unit 16 is itself titled `தேனலைகள்`.
   - R1 must compare the 1958 source's 12 mapped headings against the 26 Meesai units and determine the exact
     relationship before promoting any affected unit.
     - Possible outcomes include one-to-one alternate witnesses, partial overlap, publication/container-level
       overlap, or another source-supported relationship.
     - R0 does not decide among them, and no identity is inferred from the shared title of unit 16 alone.
   - **Do not label the 1958 headings as alternate witnesses until that identity reconciliation has established
     it.**
   - The shelf decision (Poetry, Essays or otherwise) must take the established relationship into account.
5. **Publication-titled first units** (§6.9): the promoted unit identity must be kept distinct from the
   container publication identity.
6. **Essay authorship and reprints.** All units need authorship confirmation (Kalaignar-authored vs. quoted or
   contributed material) and reprint relationships across the nine containers before new identities are created.
7. **Cinema song identity** (`kalaignar-thirai-isai-paadalgal`, 54 songs): deferred, outside R1.
8. **Final route names** for category pages, and the redirect/alias strategy (§9). These are not chosen at R0.

## 9. Intended IA shape (not chosen, not implemented)

```
/read  →  category cards only
       →  category page  →  individual canonical works  →  work reader / internal reading units
```

Possible category pages include `/read/autobiography` (or an equivalent stable route), `/read/letters`,
`/read/fiction`, `/read/poetry`, `/read/drama`, `/read/cinema`, `/read/speeches`, `/read/essays` and
`/read/literary-commentary`. **R0 does not choose or implement final route names.** This is the intended shape
only.

Collections and publications should be reachable from:
- provenance ("Published in", "Appears in");
- optional collection/publication browsing;
- work pages, where useful.

They should not occupy the same primary hierarchy as the category itself.

## 10. What R0 changed

Only this record, plus the `HANDOVER.md` checkpoint and `NEXT_CHAT_PROMPT.md` update in `pugazg/kalaignar-tribute`.

| Surface | Delta |
|---|---:|
| Implementation `pugazg/kalaignar-autobiography` (`f991043c…`) | **0** |
| Source repositories (all read-only at recorded pins) | **0** |
| Production `https://nenjukkuneethi.org` | **0** |
| Catalogue / routes / sitemap / readers / collection behaviour | **0** |
| Frozen Wave-6/7/8 census and P5 acceptance records | **0** (not edited) |

## 11. Preservation constraints for R1 and later

- **Every existing public route stays valid**, across all live route families:
  - works: `/stories`, `/novels`, `/poems`, `/plays`, `/cinema`, `/speeches`, `/essays`;
  - `/murasoli`, `/thirukkural`, `/tholkappiyam`, `/kuraloviyam`, `/sangatamil`;
  - `/collections`, `/read`;
  - every nested reading-unit route (for example `/essays/<pub>/articles/<slug>`, `/murasoli/<id>`);
  - every `/source` page.
- Later design must prefer **additive category routes**, with **redirects or aliases** where needed, rather
  than breaking citations.
- Canonical ids and slugs do not change. A promoted unit gains an identity **in addition to** its existing
  publication-unit route; the old route is never removed silently.
- Plural collection membership stays single-identity.
- Collection pages keep their printed order, ordinals and collection-local extents. They move to a secondary
  view; they are not deleted.
- Tamil stays authoritative. Source qualifications and condensed-English labels carry over unchanged:
  - Murasoli 3681;
  - Sangatamil scan 8;
  - `nachuk-koppai` scan 22;
  - Kuraloviyam scans 13/14/15/19;
  - the 45 condensed-English speeches.
- Promotion of any unit to a `LibraryWork` requires source-backed identity evidence. It never follows from
  titles or filenames alone.

## 12. Status

**READING ROOM IA v2 R0 — CLASSIFICATION CENSUS COMPLETE / REVIEW-READY.**

**R1 — NOT STARTED / NOT AUTHORIZED BY THIS R0.** R1 (implementation) requires separate explicit owner
authorization after independent review of this census. Waves 6, 7 and 8 remain COMPLETE / CLOSED / FROZEN at
P5; this initiative is not a wave and is never "P6".
