# Reading Room IA v2 — R3 Plan (Canonical-Work Promotion and Catalogue Reconciliation)

**Created:** 2026-09-26.

**Status: R3 — OWNER-AUTHORIZED ("let's start R3"). R3 PLAN — REVIEW-READY (awaiting independent exact-head review).
R3 IMPLEMENTATION — NOT STARTED.**

This is a **control-only planning record**:
- implementation delta = **0**;
- source delta = **0**;
- production mutation = **0**.

It creates no LibraryWork, performs no merge, writes no witness data, changes no reader or route, and edits no frozen
record. Every number below was re-derived from the frozen resolved manifest and the live implementation at the pins in
§2. None is copied from the authorizing prompt.

**R3 implementation (R3-A) may begin only after this plan is independently exact-head reviewed and merged.** Each
implementation stage is then its own exact-head-reviewed PR (§13).

---

## 1. Authorization and lifecycle

| Stage | Status |
|---|---|
| R0 | COMPLETE / REVIEWED / FROZEN |
| R1 | COMPLETE / REVIEWED / FROZEN |
| Owner HOLD adjudication | COMPLETE / REVIEWED / FROZEN (resolved manifest HOLD = 0) |
| R2 (plan, R2-A, R2-B, R2-C, close-out) | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED (close-out `pugazg/kalaignar-tribute#49` → `c4c3ccd4…`) |
| **R3** | **OWNER-AUTHORIZED — "let's start R3". PLANNING IN PROGRESS (this record). IMPLEMENTATION NOT STARTED.** |

- The merged R2 close-out file still reads "close-out — REVIEW-READY": that is its exact reviewed text. Its merge
  (`#49`) supersedes the wording, and it is **not** reopened.
- The frozen resolved manifest names the merge/witness actions `futureR2Actions`. Under the frozen R2 plan (§6) those are
  **R3** actions. The field is **not** renamed inside the frozen manifest.

## 2. Live pins (re-fetched 2026-09-26)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this plan) | `c4c3ccd4b0c3130e0fa96f1e8f140a2b9ff1f458`, tree `fe4595c4088ab789515b066a52712d562e1c4d49`; 0 open control PRs |
| Implementation `pugazg/kalaignar-autobiography` `main` | `597e65fde3266baffda98351de716507368b5ebc`, tree `da22e2f49f7db1be94591acb2838f28e69c3a2e8` (the R2-C merge); 0 open PRs; no R3 branch |
| Production | Vercel deployment `6674301852` at `597e65fd…` (environment `Production`) |

**Moving source heads (observed, not controlling):**

| Repository | Head |
|---|---|
| `pugazg/kalaignar-poems` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` |
| `pugazg/kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` |
| `pugazg/kalaignar-essays` | `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` |
| `pugazg/kalaignar-short-stories` | `7205a10892d0b208df2617766844f480b6a2c798` |

These heads do **not** replace the work-specific pins the implementation records. The controlling pin for each
publication is the one in its catalogue entry and payload (§11). The essays publications alone are pinned at three
different `kalaignar-essays` commits, none of them the current head.

## 3. Frozen authorities read (blobs at `c4c3ccd4`)

| File | Blob | Role in R3 |
|---|---|---|
| `READING_ROOM_IA_V2_R0_CENSUS.md` | `cee919231e161be1ee7335b30853e82b6e34e4f7` | product direction; keep-one-work exceptions; preservation constraints (§11) |
| `READING_ROOM_IA_V2_R1_IDENTITY_RECONCILIATION.md` | `42de6fa05049bf042c4d0e831fc69f188606d375` | identity rules (§12), witness vocabulary, exclusions |
| `READING_ROOM_IA_V2_R1_MANIFEST.json` | `7013177259d8914258397a2894bdf299ae4c0f14` | historical R1 decisions |
| `READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json` | `34ff3b1b02fd2813919b48afe006e35262dbf065` | overlap evidence |
| `READING_ROOM_IA_V2_OWNER_HOLD_ADJUDICATION.md` | `9cec1d37517662029d42f002393aa48cb2992363` | OD1–OD9; Sangatamil §10; 1958 §11; Meesai `ezhuthoviyam` §12 |
| `READING_ROOM_IA_V2_RESOLVED_MANIFEST.json` | `b7b3530d54ba9c354b43313eecd69e78e76a92b5` | **the R3 input**: 315 resolved rows, `futureR2Actions`, Sangatamil and 1958 blocks |
| `READING_ROOM_IA_V2_R2_PLAN.md` | `706755a133064ebb6ce961f64c82dcde948ab872` | R2/R3 boundary (§6); §§1–20 frozen |
| `READING_ROOM_IA_V2_R2A_CHECKPOINT.md` · `…_R2B_CHECKPOINT.md` · `…_R2_CLOSEOUT.md` | `e19f3045…` · `521dc191…` · `5597f8d2…` | the delivered R2 surface R3 builds on |

None of these is edited by this plan or by any R3 stage.

## 4. R3 starting census (re-derived)

### 4.1 Decision arithmetic — the frozen resolved manifest

```
315 rows = CREATE 249 + KEEP_EXISTING 27 + ADD_WITNESS 19 + DO_NOT_PROMOTE 20 + HOLD 0
```

**CREATE by final shelf:** Poetry **162** · Essays & Articles **84** · Letters **2** · Speeches **1** = 249.

**CREATE by shelf / subtype:** `poetry/poem` 137 · `poetry/ezhuthoviyam` 25 · `essays-articles/essay` 84 ·
`letters/letter` 2 · `speeches/public-speech` 1.

**CREATE by family:**

| Family | CREATE | Parent publication (live LibraryWork today) |
|---|---:|---|
| `poetry-kaalap` | 57 | `kaalap-pezhaiyum-kavithai-saaviyum` |
| `poetry-kavithaigal` | 74 | `kalaignarin-kavithaigal` |
| `poetry-1975` | 3 | `kalaignarin-kaviyaranga-kavithaigal-1975` |
| `ina-prose` | 5 | `ina-muzhakkam` |
| `ina-poem` | 3 | `ina-muzhakkam` (unit 6 `கவிதைகள்`) |
| `essays-kolaikkalam` | 6 | `kolaikkalam` |
| `essays-perumoochu` | 13 | `perumoochu` |
| `essays-sinthanaiyum-seyalum` | 50 (48 essays + 2 letters) | `sinthanaiyum-seyalum` |
| `essays-thiraavida-sampaththu` | 2 | `thiraavida-sampaththu` |
| `essays-thudikkum-ilamai` | 2 (1 essay + 1 speech) | `thudikkum-ilamai` |
| `essays-unarchchimaalai` | 9 | `unarchchimaalai` |
| `meesai` | 25 | `meesai-mulaiththa-vayathil` |
| **Total** | **249** | 11 distinct publications |

**The other 66 rows:**
- **KEEP_EXISTING 27:**
  - 8 standalone poems;
  - the 3 poetry publications;
  - `oruthalaik-kathal`;
  - 15 existing essays-shelf works: the 8 contributing essay publications, plus 7 works that stay single
    (`pesum-kalai-valarppom`, `sakkaravarththiyin-thirumagan`, `aaru-maatha-kadungkaaval`, `viduthalai-kilarcci`,
    `kayittril-thongiya-kanapathi`, `kudumbaththin-nalvilakku`, `vedhanai-ch-siraiyinindrum-viduthalai-pera`).
- **ADD_WITNESS 19** (§8.1).
- **DO_NOT_PROMOTE 20:**
  - the 14 `சக்கரவர்த்தியின் திருமகன்` installments;
  - the 3 `ஆறுமாதக் கடுங்காவல்` parts;
  - the 2 `விடுதலைக் கிளர்ச்சி` parts;
  - the ina `கவிதைகள்` container heading.

### 4.2 Identity uniqueness and leakage

- **249 canonical ids, 249 unique.**
- Against the live implementation at `597e65fd`, collisions are **0** with all three:
  - the 335 LibraryWork ids;
  - the 335 LibraryWork slugs;
  - the 9 collection ids.
- **No R3 action has leaked into implementation `main`:**
  - no CREATE id is a LibraryWork;
  - no CREATE `currentRoute` is any LibraryWork's `href`;
  - the 5 merge sources are still separate published Fiction works, and no merge target exists;
  - no R3 registry, contribution module or branch exists.
- Two strings appear in live code, and neither is leakage:
  - `green-parrot` and `sorgga-logaththil` are the **existing** item/unit route slugs whose units R1 named the ids after;
  - `scripts/test-read-categories.ts` holds R2's R3-exclusion assertions.

## 5. Route census and the `இன முழக்கம்` poem identity decision

### 5.1 Census

| Measure | Count |
|---|---:|
| CREATE rows | 249 |
| Distinct frozen `currentRoute` values | 247 |
| CREATE rows whose route is a live, one-to-one public child route (in the live sitemap, used by no other CREATE row) | **246** |
| CREATE rows without a standalone route | **3** |

- **The 246:**
  - poem item routes `/poems/<publication>/<item>`: 57 + 74 + 3 = 134;
  - essay-unit routes `/essays/<publication>/articles/<unit>`: 25 Meesai + 5 ina prose + 82 other essay units = 112.
- **The three route gaps** are the `இன முழக்கம்` unit-6 poems that R1 made canonical. All three share
  `/essays/ina-muzhakkam/articles/kavithaigal`.

| CREATE id | Title | Ordinal | Scans |
|---|---|---|---|
| `ina-muzhakkam-poem-04` | `வா!` | 6.4 | 43 |
| `ina-muzhakkam-poem-07` | `மாணவர் எழுச்சி.` | 6.7 | 44 |
| `ina-muzhakkam-poem-08` | `வாளிங்கே!` | 6.8 | 45–48 |

- **The same container also holds 8 of the 19 witness rows** (ina 6.1, 6.2, 6.3, 6.5, 6.6, 6.9, 6.10, 6.11), which
  equally have no standalone route.

### 5.2 Live payload verification

`public/data/essays/ina-muzhakkam/publication.json` (pin `kalaignar-essays@564add708b8bd942fa9d5f505b083955248873d0`)
has unit `kavithaigal` with **37 Tamil blocks**:
- **11 `subheading` blocks** carry exactly the 11 printed poem titles, each with its source scan and printed page;
- the 26 paragraph blocks between them are the poem bodies.
- The English layer also has **37 blocks**, with its 11 subheadings in the same positions ("Scale of Justice!" …
  "Varna or Death?").
- Poem boundaries are therefore **source-printed and machine-derivable** without inventing structure.
- The article reader (`components/ArticleReader.tsx`) renders printed subheadings but gives them **no anchor id** today.

**Source pages are shared between poems.** Derived from the blocks' `sourcePages`: **six of the unit's nine scans
(41–49) each carry two adjacent poems.**

| Scan | Poems |
|---|---|
| 41 | 6.1, 6.2 |
| 42 | 6.2, 6.3 |
| 43 | 6.4 `வா!`, 6.5 |
| 44 | 6.6, 6.7 `மாணவர் எழுச்சி.` |
| 48 | 6.8 `வாளிங்கே!` (scans 45–48), 6.9 |
| 49 | 6.10, 6.11 |

The printed 1951 book presents the eleven as **one continuous printed run under one heading, `கவிதைகள்`** (unit 6,
scans 41–49), not as separately paginated pieces.

### 5.3 Decision — stable fragment identity on the existing container route

**Chosen:** each of the 11 unit-6 poems gets a stable, source-derived **fragment identity** on the existing route,
keyed by its printed ordinal. Examples:
- `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-4` (`வா!`);
- `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-7`;
- `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-8`.

The same scheme covers the 8 witness fragments `#poem-6-1` … `#poem-6-11`.
- The three CREATE works take these fragment hrefs as their canonical reading locator.
- The eight witnesses use them as witness locators.
- R3-B adds a stable `id` to the eleven printed subheadings of this unit, in both languages, derived from the ordinal.
  That is the **only** reader change, and it is additive: attributes only, with no change to text, order or layout.

**Why a fragment, not new child routes.**
- **Faithfulness.** The source prints the eleven as one continuous run under one heading, and six of its nine pages
  are shared between adjacent poems.
  - A separate route per poem would split those six shared printed pages across pages of the site.
  - It would also detach each poem from the only printed context it has.
  - It would invent a route level (`…/articles/kavithaigal/<poem>`) that no other essay unit has.
  - The boundaries themselves are printed, so neither option invents a boundary. The difference is whether the site
    presents the poems in their printed sequence, and the fragment does.
- **No duplication.** A fragment reuses the one verified payload. Child routes would need a second rendering path for
  block slices of the same text.
- **Not convenience.** The fragment model *adds* work: a new href-uniqueness contract (below) and anchor ids that
  validators must pin. It is chosen for faithfulness.
- **Rejected alternative, for the record:** separate child routes (+3, or +11 if the witnesses were routed) are
  feasible, because the printed subheadings bound each poem. They remain available if the owner prefers
  independently paged poems at plan review. They would change the route, build and sitemap arithmetic in §12 by +3 or
  +11.

### 5.4 The canonical-href uniqueness contract (final)

Today every published LibraryWork has a unique `href`; `test-read-categories` asserts 335 unique hrefs. R3 replaces
this with an explicit contract:
1. **Every canonical `href` string is unique.** A fragment is part of the string, so the three ina hrefs are unique.
2. **A pathname may be shared** only by canonical works whose hrefs are fragments of **one declared container unit**
   (exactly: the three ina poems on `/essays/ina-muzhakkam/articles/kavithaigal`). Any other pathname collision fails.
3. **No canonical `href` equals any publication href or any witness locator.** A witness never shares a canonical
   locator.
4. **Every canonical pathname is a live, prerendered public route.** Fragments must match an anchor id that the
   rendered unit emits.

## 6. Publication-container resolution (family by family)

### 6.1 The question

R0's product direction is Category → canonical work → reading units, and a publication must not replace independently
readable works in normal discovery. The live catalogue still carries **publication-level LibraryWorks**. These are
`poetry-publication` or `article`-reader containers whose units R1 and the adjudication have now decided, one by one.

If every unit of a publication becomes one of the following, then keeping the publication as a canonical work would
list the same text **twice** in `/read/<category>` (once as the book, once as its works):
- a canonical work;
- a witness of a canonical work;
- a non-promotable heading.

That double-counting is exactly what R0 forbids in reverse. The adjudication (§14) marked 579 provisional for this
reason.

### 6.2 Evidence: every contributing publication is fully decomposed

Using the live route census (landing + `/source` + one route per unit) against the resolved manifest:

| Publication (live LibraryWork) | Shelf now | Units | CREATE | ADD_WITNESS (target) | DNP | Unaccounted units |
|---|---|---:|---:|---|---:|---:|
| `kaalap-pezhaiyum-kavithai-saaviyum` | Poetry | 58 | 57 | 1 (item 37 → `oruthalaik-kathal`) | 0 | **0** |
| `kalaignarin-kavithaigal` | Poetry | 77 | 74 | 3 (items 01, 02, 19 → existing standalone poems) | 0 | **0** |
| `kalaignarin-kaviyaranga-kavithaigal-1975` | Poetry | 3 (+ 5 represented scan ranges) | 3 | the 5 ranges are witnesses (§8) | 0 | **0** |
| `meesai-mulaiththa-vayathil` | Essays | 26 | 25 | 1 (unit 14 → `green-parrot`) | 0 | **0** |
| `ina-muzhakkam` | Essays | 6 (+ 11 poems in unit 6) | 5 prose + 3 poems | 8 poems → Kavithaigal CREATE works | 1 (the `கவிதைகள்` heading) | **0** |
| `unarchchimaalai` | Essays | 10 | 9 | 1 (unit 10 → `panneerselvam`) | 0 | **0** |
| `thiraavida-sampaththu` | Essays | 2 | 2 | 0 | 0 | **0** |
| `kolaikkalam` | Essays | 6 | 6 | 0 | 0 | **0** |
| `sinthanaiyum-seyalum` | Essays | 50 | 50 (48 essays + 2 letters) | 0 | 0 | **0** |
| `perumoochu` | Essays | 13 | 13 | 0 | 0 | **0** |
| `thudikkum-ilamai` | Essays | 4 | 2 (1 speech + 1 essay) | 2 (units 3, 4 → `idhaya-perikai` sections) | 0 | **0** |

The units are counted from the live payloads, and the route counts agree: landing + `/source` + units = 60, 79, 5, 28,
8, 12, 4, 8, 52, 15 and 6 sitemap URLs respectively.

### 6.3 Decisions

| Publication | Decision (option) | Source-supported justification |
|---|---|---|
| `kaalap-pezhaiyum-kavithai-saaviyum` | **2 — becomes a secondary publication surface; ceases to be canonical** | Source `indexes/item-title-map.md` (at `96982319`): "Each numbered item is a separate poem/work unit … Do not collapse the 58 items into one undifferentiated assembled poem." The book-level apparatus (the 14-item title-witness register, edition, rights) belongs to the publication surface, which is kept. |
| `kalaignarin-kavithaigal` | **2** | Source `PHASE3_CANONICAL_ASSEMBLY.md` / `README.md` (at `96982319`): the whole-volume file was "structurally inappropriate for this anthology and has been removed"; the model is "one stable numeric canonical file per indexed poem/item". The five source groups are publication structure and stay on the publication surface. |
| `kalaignarin-kaviyaranga-kavithaigal-1975` | **2** | Source README (at `188d49cd`): "NEW-ITEM-ONLY SCOPE". The book contributes 3 new poems and 5 witness ranges of other canonical poems. It is a source-witness publication, not a work. |
| `meesai-mulaiththa-vayathil` | **2** | All 26 units are separately titled canonical assemblies (R0 §6.9) that resolve to 25 Poetry works plus 1 witness. The front matter (foreword, preface) is publication apparatus. OD6 treats the book as the same content as the 1958 `தேனலைகள்`, which is itself a publication, not a work. |
| `ina-muzhakkam` | **2** | A mixed 1951 publication (R0, R1 §7): 5 prose works, 3 new poems and 8 witness poems. Unit 6 `கவிதைகள்` is DO_NOT_PROMOTE as a heading. Nothing remains that is a work of its own. |
| `unarchchimaalai` | **2** | Its printed note says the pieces "first appeared in முரசொலி, மாலைமணி". It is a collection of separately published pieces: 9 works plus 1 elegy witness. |
| `thiraavida-sampaththu` | **2** | 2 independent units (R1 §6); unit 1 shares the publication title, and R1 rule 5 keeps the unit id distinct (`thiraavida-sampaththu-katturai`). |
| `kolaikkalam` | **2** | 6 independent units; the unit-1 title collision is resolved by `kolaikkalam-katturai`. |
| `sinthanaiyum-seyalum` | **2** | 50 independent units. The "தொடரும்/தொடர்ச்சி" hits are ordinary words, not serial markers (R1 §6 note 2). |
| `perumoochu` | **2** | 13 independent political articles (R1 §6). |
| `thudikkum-ilamai` | **2** | A mixed booklet: a speech, an essay and two section-level witnesses of the existing `இதய பேரிகை`. It holds no dependent whole. |

**No contributing publication qualifies for option 1 or 3.** None establishes a dependent whole distinct from its
units:
- the only dependent-whole cases in these families were already decided as **KEEP one work** and are not containers of
  CREATE works: `oruthalaik-kathal`, `pesum-kalai-valarppom`, `sakkaravarththiyin-thirumagan`,
  `aaru-maatha-kadungkaaval`, `viduthalai-kilarcci`;
- keeping a fully decomposed book canonical *in addition to* its works (option 1) would double-list every text in
  category discovery.

**Option 4 applies to all eleven as the compatibility treatment.** The publication stays a first-class **publication
record**, with every existing URL, reader and `/source` page, but it is **not** a canonical LibraryWork (§6.4).

**The other KEEP_EXISTING rows stay canonical.** Of the 27 KEEP_EXISTING rows, the 11 publications above are
demoted. The other **16** stay canonical and unchanged:
- the 8 standalone poems, including `thennan-kathai`;
- `oruthalaik-kathal`;
- the 7 single essays-shelf works (`pesum-kalai-valarppom`, `sakkaravarththiyin-thirumagan`,
  `aaru-maatha-kadungkaaval`, `viduthalai-kilarcci`, `kayittril-thongiya-kanapathi`, `kudumbaththin-nalvilakku`,
  `vedhanai-ch-siraiyinindrum-viduthalai-pera`).

The three receiving rows (`idhayathai-thanthidu-anna`, `gunanayagar-nehru`, `idhaya-perikai`) also stay canonical and
only gain witnesses.

### 6.4 What "publication record" means (compatibility treatment)

- **A new registry.** The eleven publications move from `LIBRARY_WORKS` into a new exported registry of publication
  records (proposed `LIBRARY_PUBLICATIONS`, in `data/library.ts` beside `LIBRARY_WORKS`).
  - Each record is **verbatim** its former catalogue record: id, slug, titles, href, source pins, edition, rights,
    `unitCount`, `provenanceHref`.
  - It gains a `kind: "source-publication"` discriminator.
  - The reader payloads under `public/data/poems/<pub>/` and `public/data/essays/<pub>/` are **unchanged**.
- **URLs unchanged.** `/poems/<pub>`, `/poems/<pub>/source`, `/essays/<pub>`, `/essays/<pub>/source` and every unit
  route stay exactly as they are.
- **Membership is derived, never typed.** Each publication's units are enumerated from its own payload. Each unit's
  role comes from the R3 identity manifest (§8.2): canonical work, witness, or dependent heading.
- **Discovery.** Publications leave the primary work list of `/read/<category>`. Each category page's secondary
  (R2-C) section lists the publications that hold at least one of that category's canonical works, derived from
  membership, so no publication is placed by hand:
  - Meesai → Poetry;
  - Ina → Poetry and Essays;
  - Sinthanaiyum → Essays and Letters;
  - Thudikkum → Essays and Speeches.
- **Every promoted work** carries a derived "Published in" link to its publication record.
- **Existing consumers are migrated, never broken silently.** `lib/witness.ts` today resolves witness counterparts
  through `publishedWorks()`. A demoted `kalaignarin-kavithaigal` would make the two live Anna/Thennan witness links
  render nothing, so R3-B moves that lookup to the publication registry and a validator pins that the two links still
  render.

### 6.5 Final arithmetic

```
Live catalogue (597e65fd)                                     335
+ CREATE (resolved manifest)                                 +249   → raw add-only 584
− publication containers demoted to publication records      − 11   (3 Poetry + 8 Essays; §6.3)
− canonical merges (existing Fiction works become witnesses)  −  5   (§7)
= FINAL canonical LibraryWorks                                 568
```

| Shelf | Now | + CREATE | − demoted | − merged | **Final** |
|---|---:|---:|---:|---:|---:|
| Life Writing | 1 | 0 | 0 | 0 | **1** |
| Letters | 1 | +2 | 0 | 0 | **3** |
| Fiction | 162 | 0 | 0 | −5 | **157** |
| Poetry | 14 | +162 | −3 | 0 | **173** |
| Drama | 11 | 0 | 0 | 0 | **11** |
| Cinema Writing | 10 | 0 | 0 | 0 | **10** |
| Speeches | 117 | +1 | 0 | 0 | **118** |
| Essays & Articles | 15 | +84 | −8 | 0 | **91** |
| Literary Commentary | 4 | 0 | 0 | 0 | **4** |
| **Total** | **335** | **+249** | **−11** | **−5** | **568** |

```
1 + 3 + 157 + 173 + 11 + 10 + 118 + 91 + 4 = 568
```

**Every subtraction:**
- **−11 demotions.**
  - Poetry −3: `kaalap-pezhaiyum-kavithai-saaviyum`, `kalaignarin-kavithaigal`,
    `kalaignarin-kaviyaranga-kavithaigal-1975`.
  - Essays −8: `meesai-mulaiththa-vayathil`, `ina-muzhakkam`, `unarchchimaalai`, `thiraavida-sampaththu`,
    `kolaikkalam`, `sinthanaiyum-seyalum`, `perumoochu`, `thudikkum-ilamai`.
  - Each is fully decomposed (§6.2), stays a publication record with every URL (§6.4), and none of its text leaves the
    library.
- **−5 merges.** `sirai-kodiyathu`, `neeyum-kaithi-naanum-kaithi`, `aadik-kaatre`, `pugazhe-nee-oru-pudhir` and
  `sorgaththirku-vandhathu-eppadi` (frozen OD3–OD5). Each becomes a witness of its canonical target, keeping its route
  and its 2004-anthology appearance (§7).

**568 supersedes the provisional 579.** The difference is exactly the 11 container demotions, which the adjudication
(§14) anticipated.

**Collections stay 9** (Fiction 7, Speeches 2), with unchanged membership and member counts (§7).

## 7. The five canonical merges — preservation design

### 7.1 The constraint

| Existing Fiction work (live) | 2004 ordinal | Canonical target | Target introduced in |
|---|---:|---|---|
| `neeyum-kaithi-naanum-kaithi` | 2 | `piraiye` (Meesai 1, Poetry) | R3-B |
| `sorgaththirku-vandhathu-eppadi` | 14 | `sorgga-logaththil` (Ina unit 2, Essays) | R3-C |
| `aadik-kaatre` | 17 | `adikkaatru` (Meesai 2, Poetry) | R3-B |
| `sirai-kodiyathu` | 20 | `green-parrot` (Kavithaigal 56, Poetry) | R3-B |
| `pugazhe-nee-oru-pudhir` | 23 | `pugazh` (Meesai 13, Poetry) | R3-B |

- All five are members of `2004-kalaignarin-kuttik-kathaigal` (34 members, ordinals as above).
- `collectionMemberWorks()` resolves `members[].workId` against `LIBRARY_WORKS` and **fails closed**. Deleting the five
  LibraryWorks would therefore break the build, and it is **forbidden**.
- Their routes `/stories/<slug>` and `/stories/<slug>/source` are generated from `STORY_SLUGS`, which does **not**
  depend on `LIBRARY_WORKS`. The routes therefore survive a catalogue change mechanically; R3 pins that they do.

### 7.2 Model — one relation record per merged work; collection data untouched

- **Relation record.** Each merge is one record in the single relation registry (§8.2): relation `merged-witness`,
  level `work`.
  - Its witness descriptor is the **complete former LibraryWork record, verbatim**: id, slug, titles, href, source pins,
    descriptions.
  - It adds the canonical target and the owner-decision reference (OD3/OD4/OD5).
  - This is the only place the legacy record lives. It is not duplicated in `LIBRARY_WORKS`, the collections or the
    story data.
- **`LIBRARY_COLLECTIONS` is not edited.** The 2004 collection still lists `{ workId: "sirai-kodiyathu", ordinal: 20 }`
  and so on, because **the printed 2004 book contains the old-title witness**, not the canonical poem. Membership is
  never repointed.
- **Collection resolution learns one rule.** A member id resolves to a canonical LibraryWork, **or** to a
  `merged-witness` record, which yields the printed witness plus its canonical target.
  - Anything else still fails closed.
  - The collection page therefore still shows 34 entries in printed order. Each of the five shows its printed title,
    links its preserved story route, and carries a derived "canonical work: …" link.
- **The story route keeps the witness text.** `/stories/<slug>` keeps serving the old-title text exactly as printed:
  witness text is never merged or normalised (R1 rule 2).
  - R3-D adds a derived, additive notice linking the canonical work.
  - `/source` is unchanged.
  - Citations and deep links to the story URL keep working.
- **The canonical work lists its witnesses.** Its page lists the merged story (and any other witness) in a "Witnesses /
  also published as" block, derived from the registry by reverse lookup.

**Result, for each of the five:**
- one canonical identity;
- the old URL, the 2004 appearance, the ordinal and the provenance all preserved;
- 0 duplicate canonical works.
- The Fiction category drops by exactly 5. Fiction collections stay 7, and the 2004 member count stays 34 (a printed
  fact).

## 8. Witness and relation model

### 8.1 The 19 ADD_WITNESS rows (census)

**16 witness units:**

| # | Witness (family : key) | Locator | Target | Target kind | Level | Target exists by |
|---:|---|---|---|---|---|---|
| 1 | poetry-kaalap : `can-he-be-bought-with-love` (item 37) | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/can-he-be-bought-with-love` | `oruthalaik-kathal` | existing | work (reprint of section-1 material; OD1) | now |
| 2 | poetry-kavithaigal : `give-me-your-heart-anna` (01) | `/poems/kalaignarin-kavithaigal/give-me-your-heart-anna` | `idhayathai-thanthidu-anna` | existing | work (**already live** in `POETRY_WITNESS_RELATIONS`) | now |
| 3 | poetry-kavithaigal : `the-tale-of-the-southerner` (02) | `/poems/kalaignarin-kavithaigal/the-tale-of-the-southerner` | `thennan-kathai` | existing | work (**already live**) | now |
| 4 | poetry-kavithaigal : `democracy-as-nehru-saw-it` (19) | `/poems/kalaignarin-kavithaigal/democracy-as-nehru-saw-it` | `gunanayagar-nehru` | existing | work | now |
| 5–12 | ina-poem 6.1, 6.2, 6.3, 6.5, 6.6, 6.9, 6.10, 6.11 | `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-N` | `scales-of-justice`, `would-they-accept`, `know-it-as-a-storm`, `have-you-heard` (6.5 **and** 6.6; OD2), `when-does-defeat-come`, `still-this-clamour`, `varna-or-death` | CREATE | work | R3-B |
| 13 | essays-thudikkum-ilamai : `poompuhar` (unit 3) | `/essays/thudikkum-ilamai/articles/poompuhar` | `idhaya-perikai` § 3 `பூம்புகார் மாநாடு.` | existing | **section** | now |
| 14 | essays-thudikkum-ilamai : `vetri-vilakku` (unit 4) | `/essays/thudikkum-ilamai/articles/vetri-vilakku` | `idhaya-perikai` § 4 `வெற்றி விளக்கு!` | existing | **section** | now |
| 15 | essays-unarchchimaalai : `kavithaiyalla-kannirkkadal` (unit 10) | `/essays/unarchchimaalai/articles/kavithaiyalla-kannirkkadal` | `panneerselvam` | CREATE | work | R3-B |
| 16 | meesai : `pachchaikkili` (unit 14) | `/essays/meesai-mulaiththa-vayathil/articles/pachchaikkili` | `green-parrot` | CREATE | work | R3-B |

**3 receiving rows.** These are existing works that *gain* witnesses; they are not witness units themselves:
- `idhayathai-thanthidu-anna` ← 1975 scans 9–20;
- `gunanayagar-nehru` ← 1975 scans 21–32 (and item 19, above);
- `idhaya-perikai` ← thudikkum units 3 and 4 (above).

**Further witnesses carried on CREATE rows:**
- `freedom-fighters` ← 1975 scans 71–77, and the external 1968 `விடுதலை வீரர்கள் ஐவர்` (TVA_BOK_0004067, not in the
  library);
- `on-the-path-called-life` ← 1975 scans 33–45;
- `father-periyar` ← 1975 scans 78–84.

The three 1975 ranges on CREATE rows keep their frozen status "source-declared, pages untranscribed". R1 rule 8 applies:
the label is carried verbatim as indicative, never upgraded.

### 8.2 One authoritative relation registry (generated)

**Generated inputs.** Two committed, byte-checked outputs are generated at R3-A by one deterministic script (proposed
`scripts/build-r3-identity.ts`, with a `--verify` mode, following the `build-wave8-p4-publication.ts` pattern). Its
inputs are the **frozen resolved manifest** (read-only, blob-pinned), the live catalogue and the live reader payloads.
1. **`data/internal/r3/identity-manifest.json`:** the 249 CREATE works (id, titles, shelf, subtype, stage, parent
   publication, reading locator), the 11 publication records' unit-role map, and the stage state.
2. **`data/internal/r3/relations.json`:** every relation, exactly once:

| Relation class | Records | Level |
|---|---:|---|
| source-publication witnesses (§8.1: 16 units + 2 receiving-row extras + 4 CREATE-row extras) | 22 | `work` (20) / `section` (2) |
| merged existing works (§7) | 5 | `work`, relation `merged-witness` |
| Sangatamil ↔ `oruthalaik-kathal` (§9) | 11 | `section` |
| 1958 `தேனலைகள்` ↔ Meesai canonical works (§10) | 10 + 1 | `chapter` (10) / `publication` (1) |
| **Total** | **49** | |

**Record shape:**

```
{ id, canonicalId, relation, level, witness: WitnessRef, status, evidenceRef, ownerDecisionRef?, introducedIn }
WitnessRef =
  | { kind: "publication-unit",     publicationId, unitSlug, fragment? }   // Kaalap/Kavithaigal items, essay units, ina fragments
  | { kind: "publication-scan-range", publicationId, scans }               // the 1975 represented ranges
  | { kind: "commentary-section",   workId: "sangatamil", sectionRoute }   // §9
  | { kind: "external-publication", externalId, heading?, alai? }          // 1958 தேனலைகள், 1968 volume
  | { kind: "legacy-work",          record: <verbatim former LibraryWork> } // the five merges
```

- **Reverse lookups are derived, never stored.** They are `witnessesOf(canonicalId)`, `canonicalFor(locator)` and
  `publicationAppearances(publicationId)`.
- **No witness field is embedded in `LibraryWork` or `LibraryCollection` objects.**
- **The existing `POETRY_WITNESS_RELATIONS` (2 records) is migrated into the registry.** It becomes a derived
  compatibility view, so the Anna and Thennan links keep rendering byte-identically.
- **Nothing is written into the frozen manifest.** The runtime registry is generated *from* it, and `--verify` fails if
  the manifest blob differs from `b7b3530d…`.

### 8.3 Dependency graph — no witness before its target

- **Existing targets** (usable from R3-A onward): `oruthalaik-kathal`, `idhayathai-thanthidu-anna`, `thennan-kathai`,
  `gunanayagar-nehru`, `idhaya-perikai`.
- **Targets created in R3-B:**
  - `scales-of-justice`, `would-they-accept`, `know-it-as-a-storm`, `have-you-heard`, `when-does-defeat-come`,
    `still-this-clamour`, `varna-or-death`, `panneerselvam`, `green-parrot`, `freedom-fighters`,
    `on-the-path-called-life`, `father-periyar`;
  - the 11 Meesai 16–26 works (for §10);
  - `piraiye`, `adikkaatru` and `pugazh` (merge targets).
- **Target created in R3-C:** `sorgga-logaththil` (merge target).

**Publication order:**
- **R3-B:** all Poetry-target witnesses (rows 1–12, 15, 16, the 1975 ranges and the 1968 volume) — 18 records.
- **R3-C:** the two `idhaya-perikai` section witnesses — 2 records.
- **R3-D:** the 5 merges (targets from B and C), Sangatamil (11) and 1958 (11) — 27 records.

The **2** live Anna/Thennan records keep rendering throughout (migrated in R3-A without surface change).
`18 + 2 + 27 + 2 = 49`.

**A validator enforces the ordering:** every relation whose `introducedIn` stage is published must resolve its
`canonicalId` to a **published** canonical LibraryWork.

## 9. Sangatamil ↔ `ஒருதலைக் காதல்` (implemented in R3-D; designed here)

- **Where it lives.** It is 11 records in `relations.json`, class `commentary-section`, level `section`. Each maps
  `oruthalaik-kathal` section *n* (`/poems/oruthalaik-kathal/section-n`) to Sangatamil section `092+n−1`
  (`/sangatamil/092-oruthalaik-kaadhal-01` … `/sangatamil/102-oruthalaik-kaadhal-11`). Evidence comes from the frozen
  adjudication §10 (diagonal containment 0.922–0.985; divider page 0425 reads `ஒருதலைக் காதல்`).
- **`/sangatamil` is unchanged as a reader.**
  - No Sangatamil file, payload, route or rendering changes.
  - Sangatamil stays **one** Literary Commentary LibraryWork, and **no section becomes a LibraryWork**.
  - A validator pins the rendered Sangatamil landing and all 104 section pages byte-identical before and after R3-D.
    The only permitted difference is none.
- **The canonical side exposes it.** `oruthalaik-kathal` (landing and each section page) gets a derived "Also printed
  in `சங்கத் தமிழ்`" note that links the corresponding Sangatamil section. No text is duplicated, and no new work or
  route is created.

## 10. The 1958 `தேனலைகள்` (implemented in R3-D; designed here)

- **One external-publication record** in the registry: `1958-thenalaigal`.
  - Title `தேனலைகள்`, December 1958, TVA_BOK_0064030.
  - Source reference: `kalaignar-short-stories@7205a108`, `collections/1958-thenalaigal/README.md`.
  - Status: not transcribed and not in the library.
- **It is not a LibraryWork and not a route.** No frozen authority requires promoting it, so it is not promoted.

**10 chapter-level relations** (level `chapter`):

| அலை | Heading | Canonical work |
|---:|---|---|
| 2 | `மயிலிறகு` | `mayiliragu` |
| 4 | `மடல்` | `madal` |
| 5 | `தோழி` | `thozhi` |
| 6 | `மருதாணி` | `maruthaani` |
| 7 | `அருவி` | `aruvi` |
| 8 | `முறம்` | `muram` |
| 9 | `யாழ்` | `yaazh` |
| 10 | `சிற்பி` | `sirpi` |
| 11 | `சேவல் சண்டை` | `seval-sandai` |
| 12 | `ஆண்டு விழா` | `aandu-vizha` |

**1 publication-level relation** (level `publication`): `thenalaigal` (Meesai 16) ↔ the 1958 book as a whole. Its note
says it *indicates* அலை 1 `முத்தாரம்` and asserts **no** chapter equivalence (adjudication §11).

**அலை 3 `முத்துமாலை` has no relation.** A validator asserts that no record references அலை 3.

- **The levels are distinct by field, not by wording.** `level: "chapter"` carries `alai`; `level: "publication"`
  carries no `alai`. The UI renders them differently:
  - "Also published as அலை N `…` in `தேனலைகள்` (1958)";
  - "Related to the 1958 publication `தேனலைகள்`".
- **Where it shows.** The 11 canonical Meesai works' pages show it. The Meesai publication surface shows the book-level
  OD6 note: same underlying content, chapter order changed.

## 11. Source/data reuse, source pins and language coverage

**Reuse rule.**
- All 246 routed CREATE works **reuse their existing reader payload and route**.
- The 3 ina poems reuse the existing unit payload through fragments.
- **No text is duplicated** into a second reader, **no source is re-ingested**, and the parent publication surface is
  kept.
- R3 changes identity and catalogue records, not texts.

**Per-publication source pins** (controlling for every work promoted from that publication; from the live catalogue
entry and payload, not from moving heads):

| Publication | Source repo / path | Controlling pin | Tamil / English | Provenance surface for its works |
|---|---|---|---|---|
| `kaalap-pezhaiyum-kavithai-saaviyum` | `kalaignar-poems` / `poems/kaalap-pezhaiyum-kavithai-saaviyum` | `969823195ea8943a67fad4286ab1bc7f1c876d56` | complete / complete (project-created) | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/source` |
| `kalaignarin-kavithaigal` | `kalaignar-poems` / `poems/kalaignarin-kavithaigal` | `969823195ea8943a67fad4286ab1bc7f1c876d56` | complete / complete | `/poems/kalaignarin-kavithaigal/source` |
| `kalaignarin-kaviyaranga-kavithaigal-1975` | `kalaignar-poems` / `poems/kalaignarin-kaviyaranga-kavithaigal-1975` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` | complete / complete | `/poems/kalaignarin-kaviyaranga-kavithaigal-1975/source` |
| `ina-muzhakkam` | `kalaignar-essays` / `publications/ina-muzhakkam` | `564add708b8bd942fa9d5f505b083955248873d0` | 6/6 units Tamil + English | `/essays/ina-muzhakkam/source` |
| `kolaikkalam` | `kalaignar-essays` / `publications/kolaikkalam` | `564add708b8bd942fa9d5f505b083955248873d0` | 6/6 | `/essays/kolaikkalam/source` |
| `sinthanaiyum-seyalum` | `kalaignar-essays` / `publications/sinthanaiyum-seyalum` | `564add708b8bd942fa9d5f505b083955248873d0` | 50/50 | `/essays/sinthanaiyum-seyalum/source` |
| `unarchchimaalai` | `kalaignar-essays` / `publications/unarchchimaalai` | `6814e979fd3c2cefa14cbeb17eeec28164ce28f5` | 10/10 | `/essays/unarchchimaalai/source` |
| `thiraavida-sampaththu` | `kalaignar-essays` / `publications/thiraavida-sampaththu` | `6814e979fd3c2cefa14cbeb17eeec28164ce28f5` | 2/2 | `/essays/thiraavida-sampaththu/source` |
| `perumoochu` | `kalaignar-essays` / `publications/perumoochu` | `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` | 13/13 | `/essays/perumoochu/source` |
| `thudikkum-ilamai` | `kalaignar-essays` / `publications/thudikkum-ilamai` | `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` | 4/4 | `/essays/thudikkum-ilamai/source` |
| `meesai-mulaiththa-vayathil` | `kalaignar-essays` / `publications/meesai-mulaiththa-vayathil` | `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` | 26/26 | `/essays/meesai-mulaiththa-vayathil/source` |

**Relation-only sources (read-only; no ingestion):**

| Relation | Source | Pin |
|---|---|---|
| Sangatamil | `kalaignar-literary-commentary` / `works/sangatamil` | `e23548b09547a2308407e60e5e67c1a03fee5354` |
| 1958 `தேனலைகள்` | `kalaignar-short-stories` / `collections/1958-thenalaigal` | `7205a10892d0b208df2617766844f480b6a2c798` |
| the five merged stories | `kalaignar-short-stories` / `stories/<slug>` | `7205a10892d0b208df2617766844f480b6a2c798` (from their catalogue entries) |

**Rules for promoted-work records.**
- A promoted work's catalogue record inherits `sourceRepo`, `sourcePath` and `sourceCommit` from the parent
  publication. A unit-level source file is recorded **only** where the reader payload already records one. Rights and
  edition are inherited **only where the parent publication record carries them**.
  - The essays publications carry **no** `rights` block and no per-unit edition, so none is invented. That is the Wave-3
    validator's standing "invents NO rights/edition" rule.
- **English** is recorded as the parent's `project-created` English, since every unit has English blocks.
- **Descriptions** (`descTa`/`descEn`) are generated from verifiable facts only: publication title, year and ordinal.
  No literary summary is invented.
- **Provenance.** Each promoted work links its parent publication's `/source`. No per-work `/source` page is created;
  none exists in the source apparatus.

## 12. Route, build and sitemap projection

| Route class | Count | Build / HTML delta | Sitemap delta |
|---|---:|---:|---:|
| 1. canonical promotion onto an existing route | 246 | 0 | 0 |
| 2. new route for an identity gap | **0** (the 3 ina poems use fragments, §5.3) | 0 | 0 |
| 3. old witness route preserved after a merge (`/stories/<slug>` + `/source`) | 5 × 2 | 0 | 0 |
| 4. publication route preserved after demotion (landing + `/source` + units) | 11 publications | 0 | 0 |

**Projection:**
- **Catalogue:** 335 → **568**, with per-shelf counts as in §6.5.
- **Canonical hrefs:** 568 unique. The only shared pathname is the declared ina fragment set (3 works), per §5.4.
- **Build / prerender / HTML: +0 / +0.** R3 adds no page.
  - The 9 category routes already exist and simply list more works.
  - Collection and publication pages already exist.
- **Sitemap: +0.** Fragments are not sitemap URLs.
- **Route-preservation set:** the entire pre-R3 sitemap set (currently 5271 paths, frozen by hash at R3-A), plus the 391
  memoir chapters, all 9 collections and every `/source` route. None is removed, renamed, redirected or repurposed.
- **Not frozen here.** These totals become frozen only in each stage's reviewed PR, derived from a clean build. No
  whole-site total is hard-coded by this plan.
- **If the owner chooses child routes for the ina poems** (§5.3, rejected alternative), class 2 becomes +3 (or +11) on
  build, HTML and sitemap in R3-B, and every figure above moves by that derived amount.

## 13. Staged implementation sequence

Every stage:
- is one implementation PR, merged normally at its exact reviewed head;
- has full `Library CI` and Vercel green;
- has read-only production acceptance after its automatic deploy;
- is followed by a control checkpoint before the next stage is authorized to begin.

Stage boundaries follow the **dependency graph** (§8.3) and **shelf blast radius**:
- the foundation lands with no public change;
- promotions go shelf family by shelf family, targets before witnesses;
- the only operation that *removes* canonical identities (the merges) goes last, when every target exists.

The proposed four-stage shape was evaluated and is kept, with two refinements:
- the Meesai publication demotion moves to **R3-B**, because all its units become Poetry works or a Poetry witness
  there;
- the Ina publication demotion waits for **R3-C**, when its prose works exist.

### R3-A — Identity and relation foundation (no public change)

- **Scope:**
  - the generator and `--verify` (`scripts/build-r3-identity.ts`), and its two committed outputs (§8.2);
  - `LibraryPublication` types and an empty registry;
  - the collection-resolution rule for `merged-witness` records, dormant until R3-D;
  - relation-registry reverse lookups, and migration of `POETRY_WITNESS_RELATIONS` into the registry as a derived
    view;
  - the canonical-href contract (§5.4) as a validator;
  - **`lib/read-ia-r3-contribution.ts`**, deriving every catalogue, shelf, collection, discovery, build and sitemap term
    from the stage state (all 0 in R3-A);
  - the frozen pre-R3 sitemap-set hash.
- **Files:** new `scripts/build-r3-identity.ts`, `data/internal/r3/*.json`, `lib/read-ia-r3-contribution.ts`,
  `lib/work-relations.ts` and `scripts/test-r3-identity.ts`; small type additions in `data/library.ts` and
  `data/collections.ts`; `lib/witness.ts` reads the registry view.
- **Arithmetic:** catalogue **335** (unchanged); collections 9; build, HTML and sitemap **+0**.
- **Tests:**
  - resolved-manifest blob pin and 315-row census;
  - generator byte-identity;
  - 49 relations, each with a resolvable target class;
  - Anna and Thennan links render byte-identically;
  - `/read` and all category pages byte-identical;
  - all historical validators unchanged in outcome.
- **Rollback:** revert one PR; no public surface depends on it.
- **Excludes:** any LibraryWork change, any demotion, any rendered relation, and any reader change.

### R3-B — Poetry promotions

- **Scope:**
  - **+162 Poetry works:** Kaalap 57, Kavithaigal 74, 1975 3, ina poems 3 (fragment hrefs; subheading anchor ids),
    Meesai 25 (`ezhuthoviyam`, public form label `எழுத்தோவியம்`);
  - **demote 4** publications: `kaalap-pezhaiyum-kavithai-saaviyum`, `kalaignarin-kavithaigal`,
    `kalaignarin-kaviyaranga-kavithaigal-1975`, `meesai-mulaiththa-vayathil`;
  - publish the **18** Poetry-target witness relations (§8.3) through derived "Witnesses / Published in" blocks on
    the canonical and witness pages;
  - the secondary "Publications" entries on the Poetry (and Essays) category pages.
- **Canonical records** are generated into a catalogue slice, following the existing generated-catalogue pattern
  (`data/wave6-b7-catalogue.ts`, `data/wave7-b5-b6-k-catalogue.ts`). The 162 records are never hand-typed.
- **Arithmetic:** 335 + 162 − 4 = **493**. Poetry 14 → **173**; Essays 15 → **14**; others unchanged. Build, HTML and
  sitemap +0.
- **Reconciliation:**
  - validators that pin catalogue, shelf or discovery totals add the derived R3 terms;
  - Wave-4 archival validators that assert "no item slug is a catalogue id" and "14 Poetry works" are reconciled
    **explicitly**. They read the generated `identity-manifest.json` (`.mjs` cannot import TypeScript) and except exactly
    the promoted ids. They are never satisfied by file-layout coincidence.
- **Tests:**
  - every Poetry CREATE id is present exactly once;
  - `/read/poetry` lists 173;
  - each promoted card's href resolves;
  - the 3 ina fragment anchors are emitted in Tamil and English, and the ina unit text is byte-identical apart from
    the ids;
  - every R3-B relation target is published;
  - K37 → `oruthalaik-kathal`; K01, K02 and K19 → existing poems;
  - the 4 demoted publications keep every URL, and `/source` renders byte-identically.
- **Rollback:** revert one PR, which returns to the R3-A state.
- **Excludes:** essays, letters and speech promotions; merges; Sangatamil; 1958.

### R3-C — Essays, Letters and Speech promotions

- **Scope:**
  - **+84 Essays**: ina prose 5 (incl. `ina-muzhakkam-katturai`, `sorgga-logaththil`), kolaikkalam 6,
    perumoochu 13, sinthanaiyum 48, thiraavida 2, thudikkum 1, unarchchimaalai 9;
  - **+2 Letters**: `paasiyum-thoosiyum`, `athiga-uyaram-thaanduvatharku` (OD8, not Murasoli-corpus letters);
  - **+1 Speech**: `thudikkum-ilamai-urai` (OD9);
  - **demote 7**: `ina-muzhakkam`, `unarchchimaalai`, `thiraavida-sampaththu`, `kolaikkalam`, `sinthanaiyum-seyalum`,
    `perumoochu`, `thudikkum-ilamai`;
  - publish the **2** `idhaya-perikai` section-level witnesses.
- **Arithmetic:** 493 + 87 − 7 = **573**. Essays 14 → **91**; Letters 1 → **3**; Speeches 117 → **118**. Build, HTML
  and sitemap +0.
- **Letters special case, re-scoped:**
  - `/read/letters` lists `murasoli-letters` **and** the two OD8 letters;
  - the Murasoli corpus summary (13 volumes / 688 letters) remains attached to `murasoli-letters` only;
  - the R2 Letters test changes from "one canonical work" to "one Murasoli corpus work, plus exactly the OD8 letters".
- **Tests:**
  - every Essays, Letters and Speech CREATE id is present once;
  - Wave-3 and Wave-6 essays validators are reconciled explicitly, and "invents no rights/edition" still holds;
  - `idhaya-perikai` shows 2 section witnesses and its reader is otherwise unchanged;
  - all essay publication URLs are preserved.
- **Rollback:** revert one PR, which returns to the R3-B state.
- **Excludes:** merges, Sangatamil and 1958.

### R3-D — Merges, cross-publication provenance and final reconciliation

- **Scope:**
  - the **5 merges** (§7): legacy records move into `merged-witness` relations, collection resolution activates, and
    the witness notices appear on the 5 story routes;
  - **Sangatamil** (§9, 11 records);
  - **1958 `தேனலைகள்`** (§10, 11 records);
  - final catalogue, category, discovery and build/sitemap reconciliation;
  - the implementation close-out candidate.
- **Arithmetic:** 573 − 5 = **568**. Fiction 162 → **157**. Collections **9**, with the 2004 anthology still 34 printed
  entries. Build, HTML and sitemap +0.
- **Tests:**
  - the 5 story routes and their `/source` stay 200 and render the witness text unchanged apart from the notice;
  - the 2004 collection page shows 34 entries in printed order, each of the 5 with its printed title and a canonical
    link;
  - Sangatamil's rendered HTML is byte-identical;
  - `oruthalaik-kathal` shows 11 Sangatamil section links;
  - 10 chapter-level and 1 publication-level 1958 relations exist, and அலை 3 is absent;
  - the whole acceptance set (§14).
- **Rollback:** revert one PR, which returns to the R3-C state. Note that production then shows 573 works with the 5
  Fiction works still canonical.
- **Excludes:** anything beyond the frozen resolved manifest.

**Stage arithmetic summary:**

| Stage | Canonical works | Poetry | Essays | Letters | Speeches | Fiction | Collections | Build / sitemap delta |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| start (`597e65fd`) | 335 | 14 | 15 | 1 | 117 | 162 | 9 | — |
| R3-A | 335 | 14 | 15 | 1 | 117 | 162 | 9 | 0 / 0 |
| R3-B | 493 | 173 | 14 | 1 | 117 | 162 | 9 | 0 / 0 |
| R3-C | 573 | 173 | 91 | 3 | 118 | 162 | 9 | 0 / 0 |
| R3-D | **568** | **173** | **91** | **3** | **118** | **157** | **9** | 0 / 0 |

## 14. R3 acceptance invariants (machine-checkable)

Owned by a new `scripts/test-r3-identity.ts` (`test:r3-identity`, plus a CI step). Each stage asserts only what it has
published and pins the rest at the prior state.

1. **Frozen manifest.**
   - The resolved-manifest blob is `b7b3530d…`, with 315 rows.
   - CREATE 249 · KEEP 27 · WITNESS 19 · DO_NOT_PROMOTE 20 · HOLD 0.
   - The generator `--verify` is byte-identical.
2. **CREATE completeness.** At completion, every one of the 249 CREATE ids is a published canonical LibraryWork
   **exactly once**, on its resolved shelf and subtype.
3. **DO_NOT_PROMOTE.** None of the 20 rows is ever a LibraryWork.
4. **No witness is canonical.** No witness locator is any canonical href, and no witness row's key or id is a canonical
   id.
5. **Target before witness.** Every published relation's `canonicalId` is a published canonical LibraryWork.
6. **Merges.** For each of the 5:
   - the old URL and its `/source` are 200;
   - the id is not a canonical LibraryWork;
   - it is one `merged-witness` record;
   - its target is canonical.
7. **2004 anthology.** 34 entries in printed order and the same ordinals; each of the 5 resolves to its witness and
   canonical target; `memberCount` stays 34.
8. **Sangatamil.**
   - It remains exactly one Literary Commentary LibraryWork.
   - No Sangatamil section is a LibraryWork.
   - Its rendered pages are unchanged.
   - It has exactly 11 section relations, one-to-one in order.
9. **1958.** It has 10 `chapter` and 1 `publication` relation with the frozen mapping. No record mentions அலை 3. The
   1958 publication is not a LibraryWork.
10. **Relation levels.** `publication` / `chapter` / `section` / `work` are distinct by field. A `chapter` record
    requires `alai`; a `publication` record forbids it.
11. **Href contract (§5.4).** All canonical hrefs are unique. The only shared pathname is the declared ina fragment set.
    Every fragment matches an emitted anchor.
12. **Category completeness.** Every category page lists every canonical work on its shelf exactly once. No canonical
    work is hidden because it belongs to a publication or collection.
13. **Arithmetic.**
    - Totals equal the stage table (§13), derived from `lib/read-ia-r3-contribution.ts`; historical validators add
      its terms.
    - The final state is 568 with 1/3/157/173/11/10/118/91/4, collections 9, and build and sitemap +0.
14. **URL preservation.** The pre-R3 sitemap set (hash frozen at R3-A) is a subset of every later sitemap. No existing
    URL returns non-200 or redirects.
15. **Reader fidelity.** Every existing reader's rendered text is unchanged. The only additive differences are the ina
    anchor ids, the derived relation or "Published in" notices, and the merged-witness notices.
16. **Gates.** Full `Library CI` (both jobs) and Vercel green at every approved head and merge. Read-only production
    acceptance after every stage.

## 15. Validator reconciliation census (for R3-B/C/D)

**Pinned totals.** These scripts pin catalogue, shelf, collection or discovery totals and must add the derived R3 terms
(never new hand-typed totals). Scripts that also pin build or sitemap totals get R3 terms of 0 unless a stage's clean
build proves otherwise.

`test-collections`, `test-poetry-architecture`, `test-shelf-disclosure`, `test-standalone-poem-ui`,
`test-read-categories`, `test-essay-public-provenance`, `test-wave5-p3-cinema-catalogue`, `test-wave5-p4-cinema-ui`,
`test-wave6-b1-ammaiyappan`, `test-wave6-b2-drama`, `test-wave6-b3-speeches`, `test-wave6-b4-poetry`,
`test-wave6-b5-novels`, `test-wave6-b6-essays`, `test-wave7-b2-b4-p2-render`, `validate-wave5-p4-cinema-integrity`,
`validate-wave6-p3-build`, `validate-wave6-p4-integration`, `validate-wave6-b7-short-stories`,
`validate-wave6-b7-p3-routes`, `validate-wave6-b7-p4-integration`, `validate-wave7-b1-p1`, `validate-wave7-b1-p3-routes`,
`validate-wave7-b1-p4-integration`, `validate-wave7-b2-b4-p1-hidden`, `validate-wave7-b2-b4-p3-routes`,
`validate-wave7-b2-b4-p4-integration`, `validate-wave7-b5-b6-k-p1-hidden`, `validate-wave7-b5-b6-k-p4-integration`,
`validate-wave8-p1-hidden`, `validate-wave8-p4-integration`, and the generators `build-wave7-b1-p3-routes`,
`build-wave7-b2-b4-p3-routes`, `build-wave8-p3-routes` and `build-wave8-p4-publication`.

- The `build-wave8-p4-publication --verify` record must keep regenerating byte-identically, as in R2-C.

**Archival `.mjs` validators** that read `data/library.ts` as text:
- `validate-wave4-p1-standalone-poems`;
- `validate-wave4-p2-kaalap-pezhai` (asserts no item slug is a catalogue id);
- `validate-wave4-p3-kalaignarin-kavithaigal` (same, plus "14 top-level Poetry works");
- `validate-wave3-essays`;
- `validate-collections`;
- `validate-1977-short-stories`;
- `validate-kalaivanar-nsk-memorial-day`;
- `validate-naanmani-malai-plays`.

They are reconciled by reading the generated `identity-manifest.json`. Each keeps proving its historical cohort; R3
enters only as an explicit exception or term.

**The five merged Batch-7 stories.** Validators that expect them as published LibraryWorks
(`validate-wave6-b7-short-stories`, `validate-wave6-b7-p4-integration`, the Batch-7 catalogue generator checks) are
reconciled in R3-D to "published LibraryWork **or** `merged-witness` record", never by deleting the assertion.

## 16. What this planning PR changes

| Surface | Delta |
|---|---:|
| Implementation `pugazg/kalaignar-autobiography` (`597e65fd…`) | **0** |
| Source repositories | **0** |
| Production | **0** |
| Frozen R0 / R1 / adjudication / resolved-manifest / R2 plan / R2 checkpoints / R2 close-out / Wave-6/7/8 records | **0** (not edited) |
| Control | this plan, plus the `HANDOVER.md` CURRENT block and `NEXT_CHAT_PROMPT.md` |

## 17. Decisions for the owner at plan review

These are recorded as proposed, and are open to explicit owner correction at exact-head review:
1. **Ina unit-6 poems:** fragment identity on the existing route (§5.3), rather than 3 or 11 new child routes.
2. **Publication containers:** all eleven contributing publications become publication records rather than canonical
   works (§6.3), giving a **final 568** instead of the provisional 579.
3. **Stage order and boundaries** A → B → C → D, with the Meesai demotion in B and the Ina demotion in C (§13).

A correction to any of these changes only the derived arithmetic and stage contents, never the frozen identities.

## 18. Status

**R3 — OWNER-AUTHORIZED. R3 PLAN — REVIEW-READY. R3 IMPLEMENTATION — NOT STARTED.** R3-A requires this plan's
independent exact-head review and merge.

---

## Appendix A — The 249 CREATE works (derived from the frozen resolved manifest)

For each family, the parent publication, source pin, language coverage and provenance surface are in §11 (identical
for every work of a publication). Witness dependencies are in §8. The reading route is the work's existing public route,
reused unchanged. The three `#poem-6-N` entries are fragment locators on the existing ina unit route (§5.3).

**poetry-kaalap** — publication `kaalap-pezhaiyum-kavithai-saaviyum` · stage R3-B · 57 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 1 | `the-common-world` | பொது உலகம் | The Common World | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-common-world` |
| 2 | `stagewise-development` | படிமுறை வளர்ச்சி | Stagewise Development | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/stagewise-development` |
| 3 | `a-story-of-the-magnet-stone` | ‘காந்தக்கல்’ கதையொன்று! | A Story of the ‘Magnet Stone’! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/a-story-of-the-magnet-stone` |
| 4 | `the-stone-age-that-was-a-better-age-if-it-does-not-return` | அன்றிருந்த கற்காலம் - இனி அமையாவிடின் நற்காலம்! | The Stone Age That Was — A Better Age If It Does Not Return! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-stone-age-that-was-a-better-age-if-it-does-not-return` |
| 5 | `we-need-a-heart-of-gold-we-need-the-love-it-gives` | தங்க மனம் வேண்டும்; அது தந்திடும் அன்பு வேண்டும்! | We Need a Heart of Gold; We Need the Love It Gives! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/we-need-a-heart-of-gold-we-need-the-love-it-gives` |
| 6 | `the-knife-belongs-to-the-enemy-the-blood-is-what-we-give` | கத்தி பகைவுடையது; இரத்தம் நாம் தருவது! | The Knife Belongs to the Enemy; The Blood Is What We Give! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-knife-belongs-to-the-enemy-the-blood-is-what-we-give` |
| 7 | `the-form-of-an-age-in-history` | வரலாற்றுக் காலத்தின் கோலம்! | The Form of an Age in History! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-form-of-an-age-in-history` |
| 8 | `sweat-falling-from-the-brow-the-ribcage-breaking` | நெற்றி வியர்வை உதிர; நெஞ்செலும்பு ஒடிய! | Sweat Falling from the Brow; the Ribcage Breaking! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/sweat-falling-from-the-brow-the-ribcage-breaking` |
| 9 | `what-truth-does-the-conversation-reveal` | உரையாடல் உணர்த்திடும் உண்மை என்ன? | What Truth Does the Conversation Reveal? | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/what-truth-does-the-conversation-reveal` |
| 10 | `the-ancient-tamils-international-connections` | பழந்தமிழர் பன்னாட்டுத் தொடர்பு! | The Ancient Tamils' International Connections! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-ancient-tamils-international-connections` |
| 11 | `marks-of-identity-here-and-there` | ஆங்காங்கு அடையாள முத்திரைகள்! | Marks of Identity Here and There! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/marks-of-identity-here-and-there` |
| 12 | `valli-s-marriage-in-the-garden-of-history` | வரலாற்றுப் பூங்காவில் வள்ளித் திருமணம்! | Valli's Marriage in the Garden of History! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/valli-s-marriage-in-the-garden-of-history` |
| 13 | `the-unbroken-alliance-that-made-kharavela-tremble` | காரவேலன் கண்டு நடுங்கிய கட்டுக்குலையாக் கூட்டணி! | The Unbroken Alliance That Made Kharavela Tremble! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-unbroken-alliance-that-made-kharavela-tremble` |
| 14 | `the-history-of-kanaka-and-vijaya-carrying-the-stone` | கனக விஜயர் கல் சுமந்த வரலாறு! | The History of Kanaka and Vijaya Carrying the Stone! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-history-of-kanaka-and-vijaya-carrying-the-stone` |
| 15 | `let-us-drink-this-aryan-tea` | பருகிடலாம் இந்த “ஆரிய” தேநீரை! | Let Us Drink This “Aryan” Tea! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/let-us-drink-this-aryan-tea` |
| 16 | `as-a-flavour-united-within-the-segment` | சுளையில் ஒன்றியிருக்கும் சுவையாக! | As a Flavour United Within the Segment! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/as-a-flavour-united-within-the-segment` |
| 17 | `from-where-is-world-history-to-come` | உலக வரலாறு எங்கிருந்து வருவது? | From Where Is World History to Come? | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/from-where-is-world-history-to-come` |
| 18 | `we-seek-what-remains-after-the-rubbing-away` | தேய்ந்தது போக மிச்சத்தைத் தேடுகின்றோம்! | We Seek What Remains After the Rubbing Away! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/we-seek-what-remains-after-the-rubbing-away` |
| 19 | `a-historical-event-to-grieve-over` | வருந்தத்தக்க வரலாற்று நிகழ்ச்சி! | A Historical Event to Grieve Over! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/a-historical-event-to-grieve-over` |
| 20 | `even-in-falling-he-is-victory-s-favoured-son` | வீழினும் அவன் வெற்றித் திருமகனே! | Even in Falling, He Is Victory's Favoured Son! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/even-in-falling-he-is-victory-s-favoured-son` |
| 21 | `where-culture-is-maimed-they-would-not-even-wish-to-look` | பண்பாட்டுக்கு ஊனம் எனில் பார்க்கவும் விரும்பார்! | Where Culture Is Maimed, They Would Not Even Wish to Look! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/where-culture-is-maimed-they-would-not-even-wish-to-look` |
| 22 | `why-then-the-question-that-is-my-question` | “பிறகேன் வினா? என்பதே என் வினா!” | “Why, Then, the Question? — That Is My Question!” | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/why-then-the-question-that-is-my-question` |
| 23 | `kundalakesi-who-speaks-the-strength-of-feminism` | பெண்ணியத்தின் திண்மை கூறும் குண்டலகேசி! | Kundalakesi, Who Speaks the Strength of Feminism! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/kundalakesi-who-speaks-the-strength-of-feminism` |
| 24 | `this-tamil-land-two-thousand-years-ago` | ஈராயிரம் ஆண்டின் முன்னே இந்தத் தமிழ் நிலம்! | This Tamil Land, Two Thousand Years Ago! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/this-tamil-land-two-thousand-years-ago` |
| 25 | `kannagi-s-emphasis-on-culture` | கலாச்சாரத்தின்மீது கண்ணகி காட்டிய அழுத்தம் | Kannagi's Emphasis on Culture | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/kannagi-s-emphasis-on-culture` |
| 26 | `awake-here-is-the-dawn-of-a-classical-language` | விழித்தெழுக; இதோ செம்மொழி விடியல்! | Awake; Here Is the Dawn of a Classical Language! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/awake-here-is-the-dawn-of-a-classical-language` |
| 27 | `it-will-surely-be-opened-to-show-the-way` | வழிகாட்டும் வண்ணம்; திறக்கப்படுவது திண்ணம்! | It Will Surely Be Opened, to Show the Way! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/it-will-surely-be-opened-to-show-the-way` |
| 28 | `the-ancient-civilisation-that-spread-across-the-whole-world` | பார் முழுதும் பரவிய பழம்பெரும் நாகரிகம்! | The Ancient Civilisation That Spread Across the Whole World! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-ancient-civilisation-that-spread-across-the-whole-world` |
| 29 | `mother-give-us-bear-us-treasures-of-self-respect` | தாயே தந்திடு எமக்கு தன்மானச் செல்வங்களை ஈன்று! | Mother, Give Us — Bear Us Treasures of Self-Respect! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/mother-give-us-bear-us-treasures-of-self-respect` |
| 30 | `the-measure-of-his-power-his-just-sceptre` | ஆற்றலின் அளவுகோல்; அவன் செங்கோல்! | The Measure of His Power: His Just Sceptre! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-measure-of-his-power-his-just-sceptre` |
| 31 | `the-mother-full-of-dignity-and-the-stainless-son` | மாண்பு நிறை தாயும் மாசற்ற மகனும்! | The Mother Full of Dignity and the Stainless Son! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-mother-full-of-dignity-and-the-stainless-son` |
| 32 | `kovoorar-questions-heads-bow-down` | கோவூரார் கேள்வியுறும் - குனிந்திடும் தலையுறும் | Kovoorar Questions — Heads Bow Down | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/kovoorar-questions-heads-bow-down` |
| 33 | `is-seruppaazhi-erindha-an-honorific-title` | “செருப்பாழி எறிந்த” என்பது சிறப்புப் பட்டமா? | Is “Seruppaazhi-Erindha” an Honorific Title? | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/is-seruppaazhi-erindha-an-honorific-title` |
| 34 | `it-did-not-vanish-it-was-reborn` | மறையவில்லை; மறுமலர்ச்சி பெற்றது! | It Did Not Vanish; It Was Reborn! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/it-did-not-vanish-it-was-reborn` |
| 35 | `a-noble-friendship-higher-than-life-itself` | உயிரினும் மேலான உயர்ந்த நட்பு! | A Noble Friendship Higher Than Life Itself! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/a-noble-friendship-higher-than-life-itself` |
| 36 | `he-is-young-he-is-a-son-of-tamil` | இளையவன்; அவன் ஒரு தமிழ் மகன்! | He Is Young; He Is a Son of Tamil! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/he-is-young-he-is-a-son-of-tamil` |
| 37 | `he-who-lives-in-the-hearts-of-the-grateful` | நன்றியுடையோர் நெஞ்சில் வாழ்வோன்! | He Who Lives in the Hearts of the Grateful! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/he-who-lives-in-the-hearts-of-the-grateful` |
| 38 | `not-one-who-came-on-his-own-one-brought-by-the-commander` | தானாக வந்தவரல்ல; தளபதியால் கொண்டுவரப்பட்டவர்! | Not One Who Came on His Own; One Brought by the Commander! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/not-one-who-came-on-his-own-one-brought-by-the-commander` |
| 39 | `the-tenderness-and-compassion-shown-by-the-soil-of-kanchi` | காஞ்சி மண் காட்டிய கனிவும் கருணையும் | The Tenderness and Compassion Shown by the Soil of Kanchi | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-tenderness-and-compassion-shown-by-the-soil-of-kanchi` |
| 40 | `let-us-protect-it-the-pallava-capital` | பாதுகாப்போம்; பல்லவர் தலைநகரம்! | Let Us Protect It: The Pallava Capital! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/let-us-protect-it-the-pallava-capital` |
| 41 | `the-charters-proclaim-it` | பட்டயங்கள், பறைசாற்றுகின்றன! | The Charters Proclaim It! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-charters-proclaim-it` |
| 42 | `the-tamil-tradition-of-the-dravidian-race` | திராவிட இனத்தின் தமிழர் மரபு! | The Tamil Tradition of the Dravidian Race! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-tamil-tradition-of-the-dravidian-race` |
| 43 | `the-iron-pillar-and-the-wings-of-flies` | இரும்புத் தூணும் ஈக்களின் இறகும்! | The Iron Pillar and the Wings of Flies! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-iron-pillar-and-the-wings-of-flies` |
| 44 | `father-rajaraja-and-the-son-who-captivated-hearts` | தந்தை இராசராசனும், சிந்தை கவர்ந்த செல்வனும்! | Father Rajaraja and the Son Who Captivated Hearts! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/father-rajaraja-and-the-son-who-captivated-hearts` |
| 45 | `the-three-crowned-chola-who-stood-as-a-model` | முன்மாதிரியாகத் திகழ்ந்த மும்முடிச் சோழன்! | The Three-Crowned Chola Who Stood as a Model! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-three-crowned-chola-who-stood-as-a-model` |
| 46 | `that-future-age-will-be-a-precious-age` | அந்த வருங்காலமே; அருங்காலமாகும்! | That Future Age Will Be a Precious Age! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/that-future-age-will-be-a-precious-age` |
| 47 | `the-undying-art-of-sculpture-and-the-beautiful-art-of-painting` | அழியாத சிற்பக் கலையும், அழகிய ஓவியக் கலையும்! | The Undying Art of Sculpture and the Beautiful Art of Painting! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-undying-art-of-sculpture-and-the-beautiful-art-of-painting` |
| 48 | `they-saw-many-battlefields-they-won-in-naval-war-too` | களம் பல கண்டனர்; கடற்போரிலும் வென்றனர்! | They Saw Many Battlefields; They Won in Naval War Too! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/they-saw-many-battlefields-they-won-in-naval-war-too` |
| 49 | `the-field-of-blood-itself-became-the-coronation-hall` | குருதிக்களமே; கொலு மண்டபம் ஆனது! | The Field of Blood Itself Became the Coronation Hall! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/the-field-of-blood-itself-became-the-coronation-hall` |
| 50 | `marriages-too-can-bring-a-turn` | திருமணங்களாலும் வருவதுண்டு திருப்பம்! | Marriages Too Can Bring a Turn! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/marriages-too-can-bring-a-turn` |
| 51 | `a-culture-that-announces-an-invasion-in-advance` | படையெடுப்பை முன்கூட்டியே அறிவிக்கும் பண்பாடு! | A Culture That Announces an Invasion in Advance! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/a-culture-that-announces-an-invasion-in-advance` |
| 52 | `tamil-escaped-the-sea-deluge-it-found-the-last-sangam` | கடற்கோளில் தப்பிய தமிழ்; கடைச் சங்கம் கண்டது! | Tamil Escaped the Sea-Deluge; It Found the Last Sangam! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/tamil-escaped-the-sea-deluge-it-found-the-last-sangam` |
| 53 | `he-who-won-the-battle-of-talaiyalanganam` | தலையாலங்கானத்துச் செருவென்றான்! | He Who Won the Battle of Talaiyalanganam! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/he-who-won-the-battle-of-talaiyalanganam` |
| 54 | `nedunchezhiyan-and-nedunalvadai` | நெடுஞ்செழியனும் நெடுநல்வாடையும்! | Nedunchezhiyan and Nedunalvadai! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/nedunchezhiyan-and-nedunalvadai` |
| 55 | `when-attachment-goes-beyond-its-bounds-it-burns-as-frenzy` | பற்று கடந்தால், பற்றி எரியும் வெறியே! | When Attachment Goes Beyond Its Bounds, It Burns as Frenzy! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/when-attachment-goes-beyond-its-bounds-it-burns-as-frenzy` |
| 56 | `what-prize-is-fitting-for-the-beauty-of-a-simile` | உவமை அழகுக்கு உரிய பரிசு என்னவாம்! | What Prize Is Fitting for the Beauty of a Simile! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/what-prize-is-fitting-for-the-beauty-of-a-simile` |
| 57 | `beside-the-enemy-sword-s-edge-let-us-labour-all-our-days` | பகைவாள் முனை மருங்க; நாள் எல்லாம் உழைப்போம்! | Beside the Enemy Sword's Edge; Let Us Labour All Our Days! | poetry / poem | `/poems/kaalap-pezhaiyum-kavithai-saaviyum/beside-the-enemy-sword-s-edge-let-us-labour-all-our-days` |

**poetry-kavithaigal** — publication `kalaignarin-kavithaigal` · stage R3-B · 74 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 58 | `indrajit` | இந்திரஜித் | Indrajit | poetry / poem | `/poems/kalaignarin-kavithaigal/indrajit` |
| 59 | `hiranyan` | இரணியன் | Hiranyan | poetry / poem | `/poems/kalaignarin-kavithaigal/hiranyan` |
| 60 | `king-vali` | வாளி மன்னன் | King Vali | poetry / poem | `/poems/kalaignarin-kavithaigal/king-vali` |
| 61 | `freedom-fighters` | விடுதலை வீரர்கள் | Freedom Fighters | poetry / poem | `/poems/kalaignarin-kavithaigal/freedom-fighters` |
| 62 | `the-five-senses` | ஐம்புலன் | The Five Senses | poetry / poem | `/poems/kalaignarin-kavithaigal/the-five-senses` |
| 63 | `the-pilavanga-year` | பிலவங்க ஆண்டு | The Pilavanga Year | poetry / poem | `/poems/kalaignarin-kavithaigal/the-pilavanga-year` |
| 64 | `love-or-valour` | காதலா - வீரமா? | Love or Valour? | poetry / poem | `/poems/kalaignarin-kavithaigal/love-or-valour` |
| 65 | `six-in-the-noble-scripture` | அருமறையில் அறுவர் | Six in the Noble Scripture | poetry / poem | `/poems/kalaignarin-kavithaigal/six-in-the-noble-scripture` |
| 66 | `new-path` | புதிய பாதை | New Path | poetry / poem | `/poems/kalaignarin-kavithaigal/new-path` |
| 67 | `ten-possessions` | உடைமைகள் பத்து | Ten Possessions | poetry / poem | `/poems/kalaignarin-kavithaigal/ten-possessions` |
| 68 | `water-family` | நீர்க் குடும்பம் | The Water Family | poetry / poem | `/poems/kalaignarin-kavithaigal/water-family` |
| 69 | `bharathidasan` | பாரதிதாசன் | Bharathidasan | poetry / poem | `/poems/kalaignarin-kavithaigal/bharathidasan` |
| 70 | `bharathiyar` | பாரதியார் | Bharathiyar | poetry / poem | `/poems/kalaignarin-kavithaigal/bharathiyar` |
| 71 | `pongal-festival-day` | பொங்கல் திருநாள் | Pongal Festival Day | poetry / poem | `/poems/kalaignarin-kavithaigal/pongal-festival-day` |
| 72 | `on-the-path-called-life` | வாழ்வெனும் பாதையில் | On the Path Called Life | poetry / poem | `/poems/kalaignarin-kavithaigal/on-the-path-called-life` |
| 73 | `arithmetic` | கணக்கு | Arithmetic | poetry / poem | `/poems/kalaignarin-kavithaigal/arithmetic` |
| 74 | `thank-you-thank-you` | நன்றி, நன்றி! | Thank You, Thank You! | poetry / poem | `/poems/kalaignarin-kavithaigal/thank-you-thank-you` |
| 75 | `silver-jubilee` | வெள்ளி விழா | Silver Jubilee | poetry / poem | `/poems/kalaignarin-kavithaigal/silver-jubilee` |
| 76 | `anna-is-here` | அண்ணன் இருக்கின்றார் | Anna Is Here | poetry / poem | `/poems/kalaignarin-kavithaigal/anna-is-here` |
| 77 | `anna-a-poetry-assembly` | அண்ணன் ஒரு கவியரங்கம் | Anna, a Poetry Assembly | poetry / poem | `/poems/kalaignarin-kavithaigal/anna-a-poetry-assembly` |
| 78 | `a-walking-journey-for-tamil-to-flourish` | தமிழ் வளர வழிநடைப் பயணம் | A Walking Journey for Tamil to Flourish | poetry / poem | `/poems/kalaignarin-kavithaigal/a-walking-journey-for-tamil-to-flourish` |
| 79 | `for-the-world-to-flourish` | வையம் தழைக்க | For the World to Flourish | poetry / poem | `/poems/kalaignarin-kavithaigal/for-the-world-to-flourish` |
| 80 | `father-periyar` | தந்தை பெரியார் | Father Periyar | poetry / poem | `/poems/kalaignarin-kavithaigal/father-periyar` |
| 81 | `akam-creations` | அகத்துறைப் படைப்புகள் | Akam Creations | poetry / poem | `/poems/kalaignarin-kavithaigal/akam-creations` |
| 82 | `pongal-festival` | பொங்கல் விழா | Pongal Festival | poetry / poem | `/poems/kalaignarin-kavithaigal/pongal-festival` |
| 83 | `a-silappathikaram-feast` | சிலப்பதிகார விருந்து | A Silappathikaram Feast | poetry / poem | `/poems/kalaignarin-kavithaigal/a-silappathikaram-feast` |
| 84 | `on-annas-path` | அண்ணா வழியில் | On Anna's Path | poetry / poem | `/poems/kalaignarin-kavithaigal/on-annas-path` |
| 85 | `i-shall-walk-on-our-ayya-and-annas-path` | நடந்திடுவேன் நமது அய்யா, அண்ணா வழியில்! | I Shall Walk on Our Ayya and Anna's Path! | poetry / poem | `/poems/kalaignarin-kavithaigal/i-shall-walk-on-our-ayya-and-annas-path` |
| 86 | `presiding-poem-three-great-celebrations` | முப்பெரும் விழாக் கவியரங்கம் தலைமைக் கவிதை | Presiding Poem at the Three Great Celebrations Poetry Assembly | poetry / poem | `/poems/kalaignarin-kavithaigal/presiding-poem-three-great-celebrations` |
| 87 | `in-a-changing-town` | மாறி வரும் ஊரினிலே | In a Changing Town | poetry / poem | `/poems/kalaignarin-kavithaigal/in-a-changing-town` |
| 88 | `views-of-society` | சமுதாயப் பார்வைகள்...! | Views of Society...! | poetry / poem | `/poems/kalaignarin-kavithaigal/views-of-society` |
| 89 | `kalaivanar-arangam-poetry-assembly` | கலைவாணர் அரங்கக் கவியரங்கம் | Kalaivanar Arangam Poetry Assembly | poetry / poem | `/poems/kalaignarin-kavithaigal/kalaivanar-arangam-poetry-assembly` |
| 90 | `chithirai-festival-presiding-poem` | "சித்திரைத் திருநாள்" தலைமைக் கவிதை! | "Chithirai Festival" — Presiding Poem! | poetry / poem | `/poems/kalaignarin-kavithaigal/chithirai-festival-presiding-poem` |
| 91 | `three-letters-thoughts-three-times-three` | எழுத்துக்கள் மூன்று - எண்ணங்கள் மும்மூன்று | Three Letters — Thoughts Three Times Three | poetry / poem | `/poems/kalaignarin-kavithaigal/three-letters-thoughts-three-times-three` |
| 92 | `on-arignar-annas-path` | “அறிஞர் அண்ணா வழியில்” | “On Arignar Anna’s Path” | poetry / poem | `/poems/kalaignarin-kavithaigal/on-arignar-annas-path` |
| 93 | `panneerselvam` | பன்னீர்ச்செல்வமே! | Panneerselvam! | poetry / poem | `/poems/kalaignarin-kavithaigal/panneerselvam` |
| 94 | `mother-arts-foremost-son` | கலைத்தாயின் தலைச் செல்வன்! | Mother Art’s Foremost Son! | poetry / poem | `/poems/kalaignarin-kavithaigal/mother-arts-foremost-son` |
| 95 | `we-move-as-your-shadow` | உன் நிழலாக அசைகின்றோம்! | We Move as Your Shadow! | poetry / poem | `/poems/kalaignarin-kavithaigal/we-move-as-your-shadow` |
| 96 | `long-live-jeeva` | வாழ்க ஜீவா | Long Live Jeeva | poetry / poem | `/poems/kalaignarin-kavithaigal/long-live-jeeva` |
| 97 | `the-fallen-hero` | மறைந்த மாவீரன் | The Fallen Hero | poetry / poem | `/poems/kalaignarin-kavithaigal/the-fallen-hero` |
| 98 | `my-dear-friend-why-did-you-leave` | என் இனிய நண்பா! ஏன் பிரிந்தாய்? | My Dear Friend! Why Did You Leave? | poetry / poem | `/poems/kalaignarin-kavithaigal/my-dear-friend-why-did-you-leave` |
| 99 | `today-is-your-birthday` | இன்றைக்கு உன்றன் பிறந்த நாள் | Today Is Your Birthday | poetry / poem | `/poems/kalaignarin-kavithaigal/today-is-your-birthday` |
| 100 | `no-one-day-called-his-birthday` | அவன் பிறந்தநாள் என ஒன்றில்லை! | There Is No One Day Called His Birthday! | poetry / poem | `/poems/kalaignarin-kavithaigal/no-one-day-called-his-birthday` |
| 101 | `precious-remedy-anbazhaga-beloved-sibling` | அருமருந்தே! அன்பழக உடன்பிறப்பே! | Precious Remedy! Anbazhaga, Beloved Sibling! | poetry / poem | `/poems/kalaignarin-kavithaigal/precious-remedy-anbazhaga-beloved-sibling` |
| 102 | `rationalist-pandianar` | பகுத்தறிவுப் பாண்டியனார்! | Rationalist Pandianar! | poetry / poem | `/poems/kalaignarin-kavithaigal/rationalist-pandianar` |
| 103 | `scales-of-justice` | நியாயத் தராசு | The Scales of Justice | poetry / poem | `/poems/kalaignarin-kavithaigal/scales-of-justice` |
| 104 | `would-they-accept` | ஏற்பாரோ? | Would They Accept? | poetry / poem | `/poems/kalaignarin-kavithaigal/would-they-accept` |
| 105 | `know-it-as-a-storm` | புயல் என அறிக! | Know It as a Storm! | poetry / poem | `/poems/kalaignarin-kavithaigal/know-it-as-a-storm` |
| 106 | `have-you-heard` | கேட்டுண்டோ? | Have You Heard? | poetry / poem | `/poems/kalaignarin-kavithaigal/have-you-heard` |
| 107 | `varna-or-death` | வருணமா? மரணமா? | Varna or Death? | poetry / poem | `/poems/kalaignarin-kavithaigal/varna-or-death` |
| 108 | `when-does-defeat-come` | தோல்வி எப்பொழுது? | When Does Defeat Come? | poetry / poem | `/poems/kalaignarin-kavithaigal/when-does-defeat-come` |
| 109 | `still-this-clamour` | இன்றுமா கூச்சல்? | Still This Clamour? | poetry / poem | `/poems/kalaignarin-kavithaigal/still-this-clamour` |
| 110 | `green-parrot` | பச்சைக் கிளி | Green Parrot | poetry / poem | `/poems/kalaignarin-kavithaigal/green-parrot` |
| 111 | `fountain-of-imagination` | கற்பனை ஊற்று | Fountain of Imagination | poetry / poem | `/poems/kalaignarin-kavithaigal/fountain-of-imagination` |
| 112 | `o-sky-pour-down` | வானமே பொழிக நீ! | O Sky, Pour Down! | poetry / poem | `/poems/kalaignarin-kavithaigal/o-sky-pour-down` |
| 113 | `a-letter-in-verse` | கவிதையில் ஒரு மடல்! | A Letter in Verse! | poetry / poem | `/poems/kalaignarin-kavithaigal/a-letter-in-verse` |
| 114 | `will-he-realise-who-knows` | அவர் உணர்வாரோ! யார் அறிவார்? | Will He Realise? Who Knows? | poetry / poem | `/poems/kalaignarin-kavithaigal/will-he-realise-who-knows` |
| 115 | `let-it-whirl-as-a-battle-sword` | போர்வாளாய்ச் சுழலட்டும்! | Let It Whirl as a Battle-Sword! | poetry / poem | `/poems/kalaignarin-kavithaigal/let-it-whirl-as-a-battle-sword` |
| 116 | `whose-names-have-still-not-appeared` | இன்னும் யார் யார் பெயர்கள் வரவில்லை? | Whose Names Have Still Not Appeared? | poetry / poem | `/poems/kalaignarin-kavithaigal/whose-names-have-still-not-appeared` |
| 117 | `a-drop-of-honey` | ஒரு சொட்டுத் தேன்! | A Drop of Honey! | poetry / poem | `/poems/kalaignarin-kavithaigal/a-drop-of-honey` |
| 118 | `let-it-sprout-as-seed-and-put-forth-roots` | விதையாய் முளைத்து விழுதுகள் விடட்டும்! | Let It Sprout as Seed and Put Forth Roots! | poetry / poem | `/poems/kalaignarin-kavithaigal/let-it-sprout-as-seed-and-put-forth-roots` |
| 119 | `he-calls-the-sun-an-ice-cube` | சூரியனைப் பனிக்கட்டி என்கின்றார்! | He Calls the Sun an Ice Cube! | poetry / poem | `/poems/kalaignarin-kavithaigal/he-calls-the-sun-an-ice-cube` |
| 120 | `dont-stop-your-stride` | நடையை நிறுத்தாதே! | Don't Stop Your Stride! | poetry / poem | `/poems/kalaignarin-kavithaigal/dont-stop-your-stride` |
| 121 | `a-backwater-full-of-ignorant-folk` | பாமரர் நிறைந்த பட்டிக்காடு! | A Backwater Full of Ignorant Folk! | poetry / poem | `/poems/kalaignarin-kavithaigal/a-backwater-full-of-ignorant-folk` |
| 122 | `tamil-nadu-is-being-looted` | கொள்ளை போகுதம்மா தமிழ்நாடு | Tamil Nadu Is Being Looted | poetry / poem | `/poems/kalaignarin-kavithaigal/tamil-nadu-is-being-looted` |
| 123 | `what-kind-of-country-is-this` | என்ன தேசமடா இது? | What Kind of Country Is This? | poetry / poem | `/poems/kalaignarin-kavithaigal/what-kind-of-country-is-this` |
| 124 | `come-let-us-tear-off-the-mask` | முகமூடி கிழித்தெறிவோம் வாரீர்! | Come, Let Us Tear Off the Mask! | poetry / poem | `/poems/kalaignarin-kavithaigal/come-let-us-tear-off-the-mask` |
| 125 | `what-is-the-answer-tell-us` | பதில் என்ன? பகர்ந்திடுக! | What Is the Answer? Tell Us! | poetry / poem | `/poems/kalaignarin-kavithaigal/what-is-the-answer-tell-us` |
| 126 | `ka-ka-ka` | கா, கா, கா! | Kā, Kā, Kā! | poetry / poem | `/poems/kalaignarin-kavithaigal/ka-ka-ka` |
| 127 | `let-us-rise-in-the-east-like-the-sun` | பகலவனாய்க் கிழக்கில் உதித்திடுவோம்! | Let Us Rise in the East Like the Sun! | poetry / poem | `/poems/kalaignarin-kavithaigal/let-us-rise-in-the-east-like-the-sun` |
| 128 | `is-this-diversion-justified` | திசை திருப்பல் நியாயம்தானா? | Is This Diversion Justified? | poetry / poem | `/poems/kalaignarin-kavithaigal/is-this-diversion-justified` |
| 129 | `it-is-over-a-comedy-drama` | நடந்து முடிந்ததம்மா; ஒரு நகைச்சுவை நாடகம்! | It Is Over—a Comedy Drama! | poetry / poem | `/poems/kalaignarin-kavithaigal/it-is-over-a-comedy-drama` |
| 130 | `there-are-some-countries` | சில நாடுகள் இருக்கின்றன! | There Are Some Countries! | poetry / poem | `/poems/kalaignarin-kavithaigal/there-are-some-countries` |
| 131 | `you-bless-your-footwear` | உன் காலணியை வாழ்த்துகிறாய் | You Bless Your Footwear | poetry / poem | `/poems/kalaignarin-kavithaigal/you-bless-your-footwear` |

**poetry-1975** — publication `kalaignarin-kaviyaranga-kavithaigal-1975` · stage R3-B · 3 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 132 | `at-the-revolutionary-poets-poetry-gathering` | புரட்சிக் கவிஞர் பாட்டரங்கில் / முதல்வர் கலைஞர் தலைமைக் கவிதை | At the Revolutionary Poet's Poetry Gathering / Chief Minister Kalaignar's Presiding Poem | poetry / poem | `/poems/kalaignarin-kaviyaranga-kavithaigal-1975/at-the-revolutionary-poets-poetry-gathering` |
| 133 | `at-the-parambu-hill-festival-for-the-great-patron-pari` | பறம்புமலைப் பாரி வள்ளல் விழாக் / கவியரங்கில் / முதல்வர் கலைஞரின் தலைமைக் கவிதை | At the Parambu Hill Festival for the Great Patron Pari / At the Poetry Gathering / Chief Minister Kalaignar's Presiding Poem | poetry / poem | `/poems/kalaignarin-kaviyaranga-kavithaigal-1975/at-the-parambu-hill-festival-for-the-great-patron-pari` |
| 134 | `chief-minister-kalaignars-reply-poem` | “முதல்வர் கலைஞரின் பதில் கவிதை” | “Chief Minister Kalaignar's Reply Poem” | poetry / poem | `/poems/kalaignarin-kaviyaranga-kavithaigal-1975/chief-minister-kalaignars-reply-poem` |

**ina-poem** — publication `ina-muzhakkam` · stage R3-B · 3 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 135 | `ina-muzhakkam-poem-04` | வா! | Come! | poetry / poem | `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-4` *(fragment; §5.3)* |
| 136 | `ina-muzhakkam-poem-07` | மாணவர் எழுச்சி. | Student Uprising. | poetry / poem | `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-7` *(fragment; §5.3)* |
| 137 | `ina-muzhakkam-poem-08` | வாளிங்கே! | Here Is the Sword! | poetry / poem | `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-8` *(fragment; §5.3)* |

**meesai** — publication `meesai-mulaiththa-vayathil` · stage R3-B · 25 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 138 | `piraiye` | பிறையே | O Crescent! | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/piraiye` |
| 139 | `adikkaatru` | ஆடிக்காற்று | Aadi Wind | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/adikkaatru` |
| 140 | `karuppu-pen` | கருப்புப் பெண் | Black Woman | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/karuppu-pen` |
| 141 | `kadale` | கடலே | O Sea! | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/kadale` |
| 142 | `aaru` | ஆறு | River | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/aaru` |
| 143 | `vaazhiya-vaikarai` | வாழிய வைகறை | Hail the Dawn! | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/vaazhiya-vaikarai` |
| 144 | `agappai-siththar` | அகப்பை சித்தர் | The Ladle Siddhar | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/agappai-siththar` |
| 145 | `malaiye-vaazhi` | மலையே வாழி | Hail, Mountain! | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/malaiye-vaazhi` |
| 146 | `thalir` | தளிர் | Tender Shoot | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/thalir` |
| 147 | `vinmeen` | விண்மீன் | Star | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/vinmeen` |
| 148 | `thanimai` | தனிமை | Solitude | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/thanimai` |
| 149 | `naadaga-medai` | நாடக மேடை | The Stage | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/naadaga-medai` |
| 150 | `pugazh` | புகழ் | Fame | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/pugazh` |
| 151 | `tamizhe` | தமிழே | O Tamil! | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/tamizhe` |
| 152 | `thenalaigal` | தேனலைகள் | Honey Waves | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/thenalaigal` |
| 153 | `thozhi` | தோழி | Friend | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/thozhi` |
| 154 | `maruthaani` | மருதாணி | Henna | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/maruthaani` |
| 155 | `aruvi` | அருவி | Waterfall | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/aruvi` |
| 156 | `muram` | முறம் | Winnowing Tray | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/muram` |
| 157 | `yaazh` | யாழ் | Yaazh | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/yaazh` |
| 158 | `sirpi` | சிற்பி | The Sculptor | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/sirpi` |
| 159 | `seval-sandai` | சேவல் சண்டை | Cockfight | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/seval-sandai` |
| 160 | `madal` | மடல் | Letter | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/madal` |
| 161 | `aandu-vizha` | ஆண்டு விழா | Annual Festival | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/aandu-vizha` |
| 162 | `mayiliragu` | மயிலிறகு | Peacock Feather | poetry / ezhuthoviyam | `/essays/meesai-mulaiththa-vayathil/articles/mayiliragu` |

**ina-prose** — publication `ina-muzhakkam` · stage R3-C · 5 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 163 | `ina-muzhakkam-katturai` | இன முழக்கம் | The Clarion Call of the Race | essays-articles / essay | `/essays/ina-muzhakkam/articles/ina-muzhakkam` |
| 164 | `sorgga-logaththil` | சொர்க்க லோகத்தில் | In the Heavenly Realm | essays-articles / essay | `/essays/ina-muzhakkam/articles/sorgga-logaththil` |
| 165 | `murasaraivai` | முரசறைவாய் | Beat the Drum | essays-articles / essay | `/essays/ina-muzhakkam/articles/murasaraivai` |
| 166 | `pazhikku-pazhi` | பழிக்குப் பழி | Revenge for Revenge | essays-articles / essay | `/essays/ina-muzhakkam/articles/pazhikku-pazhi` |
| 167 | `aariyam-pesugirathu` | ஆரியம் பேசுகிறது | Aryanism Speaks | essays-articles / essay | `/essays/ina-muzhakkam/articles/aariyam-pesugirathu` |

**essays-kolaikkalam** — publication `kolaikkalam` · stage R3-C · 6 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 168 | `kolaikkalam-katturai` | கொலைக்களம்! | The Killing Field! | essays-articles / essay | `/essays/kolaikkalam/articles/kolaikkalam` |
| 169 | `asthi-karaiyattum` | ‘அஸ்தி’ கரையட்டும்! | Let the ‘Ashes’ Dissolve! | essays-articles / essay | `/essays/kolaikkalam/articles/asthi-karaiyattum` |
| 170 | `paliyai-niruththungal` | பலியை நிறுத்துங்கள்! | Stop the Sacrifice! | essays-articles / essay | `/essays/kolaikkalam/articles/paliyai-niruththungal` |
| 171 | `vizhalukku-neer-iraiththu` | விழலுக்கு நீர் இறைத்து... | Watering the Weeds... | essays-articles / essay | `/essays/kolaikkalam/articles/vizhalukku-neer-iraiththu` |
| 172 | `sothanai` | சோதனை! | Search! | essays-articles / essay | `/essays/kolaikkalam/articles/sothanai` |
| 173 | `veeramuzhakkam-seythiduveer` | வீரமுழக்கஞ் செய்திடுவீர்! | Raise the Heroic Cry! | essays-articles / essay | `/essays/kolaikkalam/articles/veeramuzhakkam-seythiduveer` |

**essays-perumoochu** — publication `perumoochu` · stage R3-C · 13 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 174 | `perumoochu-katturai` | பெருமூச்சு | A Deep Sigh | essays-articles / essay | `/essays/perumoochu/articles/perumoochu` |
| 175 | `maaligai-amaiththida-vareer` | மாளிகை அமைத்திட வாரீர்! | Come, Let Us Build the Mansion! | essays-articles / essay | `/essays/perumoochu/articles/maaligai-amaiththida-vareer` |
| 176 | `manthirigal-kulai-nadukkam` | மந்திரிகள் குலை நடுக்கம் | Ministers Tremble in Fear | essays-articles / essay | `/essays/perumoochu/articles/manthirigal-kulai-nadukkam` |
| 177 | `vaapas-veerargal` | வாபஸ் வீரர்கள்! | Heroes of Retreat! | essays-articles / essay | `/essays/perumoochu/articles/vaapas-veerargal` |
| 178 | `podhu-makkalukku-thani-echarikkai` | பொது மக்களுக்குத் தனி எச்சரிக்கை | A Special Warning to the Public | essays-articles / essay | `/essays/perumoochu/articles/podhu-makkalukku-thani-echarikkai` |
| 179 | `siruvargal` | சிறுவர்கள் | Youngsters | essays-articles / essay | `/essays/perumoochu/articles/siruvargal` |
| 180 | `ahimsa-vilasam` | “அஹிம்சா விலாசம்” | “Ahimsa Vilasam” | essays-articles / essay | `/essays/perumoochu/articles/ahimsa-vilasam` |
| 181 | `thindivanam-theerargaal` | திண்டிவனம் தீரர்காள்! | O Heroes of Tindivanam! | essays-articles / essay | `/essays/perumoochu/articles/thindivanam-theerargaal` |
| 182 | `seval-koovugirathu` | சேவல் கூவுகிறது! | The Rooster Crows! | essays-articles / essay | `/essays/perumoochu/articles/seval-koovugirathu` |
| 183 | `maadottigal` | மாடோட்டிகள்! | Cattle-Drivers! | essays-articles / essay | `/essays/perumoochu/articles/maadottigal` |
| 184 | `therthal-kovalan` | தேர்தல் கோவலன்! | Election Kovalan! | essays-articles / essay | `/essays/perumoochu/articles/therthal-kovalan` |
| 185 | `sindhiththunarga-seetramuraadheer` | சிந்தித்துணர்க! சீற்றமுறாதீர்! | Think and Understand! Do Not Grow Angry! | essays-articles / essay | `/essays/perumoochu/articles/sindhiththunarga-seetramuraadheer` |
| 186 | `boom-boom-boom` | பூம்! பூம்! பூம்! | Boom! Boom! Boom! | essays-articles / essay | `/essays/perumoochu/articles/boom-boom-boom` |

**essays-sinthanaiyum-seyalum** — publication `sinthanaiyum-seyalum` · stage R3-C · 50 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 187 | `paasiyum-thoosiyum` | பாசியும் - தூசியும்! | Moss and Dust! | letters / letter | `/essays/sinthanaiyum-seyalum/articles/paasiyum-thoosiyum` |
| 188 | `athiga-uyaram-thaanduvatharku` | அதிக உயரம் தாண்டுவதற்கு | To Clear a Greater Height | letters / letter | `/essays/sinthanaiyum-seyalum/articles/athiga-uyaram-thaanduvatharku` |
| 189 | `en-peyar-puratchi` | என் பெயர் புரட்சி! | My Name Is Revolution! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/en-peyar-puratchi` |
| 190 | `kurukulam` | குருகுலம்! | Gurukulam! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/kurukulam` |
| 191 | `jananayaga-neri` | ஜனநாயக நெறி | The Way of Democracy | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/jananayaga-neri` |
| 192 | `vaakkuseettin-valimai` | வாக்குச்சீட்டின் வலிமை | The Power of the Ballot | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vaakkuseettin-valimai` |
| 193 | `suyamariyathai-thirumanam` | சுயமரியாதைத் திருமணம் | Self-Respect Marriage | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/suyamariyathai-thirumanam` |
| 194 | `manithanin-marupakkam` | மனிதனின் மறுபக்கம் | The Other Side of Man | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/manithanin-marupakkam` |
| 195 | `vinnai-thottu-mannil-pudhaivatha` | விண்ணைத் தொட்டு மண்ணில் புதைவதா? | Touching the Sky, Buried in the Earth? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vinnai-thottu-mannil-pudhaivatha` |
| 196 | `manithanum-marupiraviyum` | மனிதனும் மறுபிறவியும் | Man and Rebirth | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/manithanum-marupiraviyum` |
| 197 | `vetri-tholvi` | வெற்றி தோல்வி! | Victory and Defeat! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vetri-tholvi` |
| 198 | `azhukkaru` | அழுக்காறு | Azhukkaaru | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/azhukkaru` |
| 199 | `miguthikkan` | மிகுதிக்கண்... | When the Limit Is Crossed... | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/miguthikkan` |
| 200 | `valivum-polivum` | வலிவும், பொலிவும்! | Strength and Radiance! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/valivum-polivum` |
| 201 | `inbamum-thunbamum` | இன்பமும் துன்பமும்! | Joy and Sorrow! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/inbamum-thunbamum` |
| 202 | `ozhukkam` | ஒழுக்கம் | Conduct | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/ozhukkam` |
| 203 | `vasiya-marunthu` | வசிய மருந்து | The Enchantment Drug | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vasiya-marunthu` |
| 204 | `sothida-sogam` | சோதிட சோகம்! | Astrological Sorrow! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/sothida-sogam` |
| 205 | `aanmiga-aazhkadal` | ஆன்மிக ஆழ்கடல் | A Deep Ocean of Spirituality | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/aanmiga-aazhkadal` |
| 206 | `thenil-kuzhaithu-koduthaalum` | தேனில் குழைத்துக் கொடுத்தாலும்...! | Even If Mixed with Honey...! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/thenil-kuzhaithu-koduthaalum` |
| 207 | `viyaathikku-viruntha` | வியாதிக்கு விருந்தா? | A Feast for Disease? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/viyaathikku-viruntha` |
| 208 | `vilaiyaattu` | விளையாட்டு | Sport | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vilaiyaattu` |
| 209 | `thannai-velvaan` | தன்னை வெல்வான் | He Who Conquers Himself | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/thannai-velvaan` |
| 210 | `idlar` | இட்லர் | Hitler | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/idlar` |
| 211 | `ingarsaal` | இங்கர்சால் | Ingersoll | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/ingarsaal` |
| 212 | `magalir-ida-othukkeedu` | மகளிர் இட ஒதுக்கீடு! | Women's Reservation! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/magalir-ida-othukkeedu` |
| 213 | `thiyanam` | தியானம்??? | Meditation??? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/thiyanam` |
| 214 | `vibaththu` | விபத்து | Accident | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vibaththu` |
| 215 | `chinnathirai-selvi` | சின்னத்திரை “செல்வி” | The Small-Screen “Selvi” | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/chinnathirai-selvi` |
| 216 | `marunthena-onru` | மருந்தென ஒன்று! | A Thing Called Medicine! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/marunthena-onru` |
| 217 | `siriya-noolthaan` | சிறிய நூல்தான் | Only a Small Book | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/siriya-noolthaan` |
| 218 | `mandela` | மண்டேலா | Mandela | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/mandela` |
| 219 | `thondullam` | தொண்டுள்ளம் | Spirit of Service | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/thondullam` |
| 220 | `magalir-perani` | மகளிர் பேரணி! | Women's Rally! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/magalir-perani` |
| 221 | `thirikadugam` | திரிகடுகம் | Thirikadugam | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/thirikadugam` |
| 222 | `theekkuchchi-thedatheer` | தீக்குச்சி தேடாதீர்! | Don't Look for a Matchstick! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/theekkuchchi-thedatheer` |
| 223 | `silambum-maniyum` | சிலம்பும் மணியும்! | The Anklet and the Gem! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/silambum-maniyum` |
| 224 | `seynnanri` | செய்ந்நன்றி | Gratitude for Help Received | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/seynnanri` |
| 225 | `pagutharivu-paathai` | பகுத்தறிவுப் பாதை! | The Path of Rationalism! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/pagutharivu-paathai` |
| 226 | `penniyap-puratchi` | பெண்ணியப் புரட்சி! | A Feminist Revolution! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/penniyap-puratchi` |
| 227 | `vali-arivikkum-vaayillaa-mozhi` | வலி அறிவிக்கும் வாயில்லா மொழி! | The Mute Language That Tells of Pain! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/vali-arivikkum-vaayillaa-mozhi` |
| 228 | `varumun-kaappathaa-vanthapin-kaappathaa` | வருமுன் காப்பதா? வந்தபின் காப்பதா? | Protect Before It Comes? Or After It Comes? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/varumun-kaappathaa-vanthapin-kaappathaa` |
| 229 | `enge-sorgam-enge-sorgam` | எங்கே சொர்க்கம்? எங்கே சொர்க்கம்? | Where Is Heaven? Where Is Heaven? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/enge-sorgam-enge-sorgam` |
| 230 | `guru-peedamum-kural-peedamum` | குரு பீடமும்; குறள் பீடமும்! | The Guru Peedam and the Kural Peedam! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/guru-peedamum-kural-peedamum` |
| 231 | `iraiyanaar-kuralum-iniyavai-naarpathum` | இறையனார் குறளும்; இனியவை நாற்பதும்! | Iraiyanar's Kural and Iniyavai Narpathu! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/iraiyanaar-kuralum-iniyavai-naarpathum` |
| 232 | `padagukku-oru-kanakku-naattukku-oru-kanakkaa` | படகுக்கு ஒரு கணக்கு; நாட்டுக்கு ஒரு கணக்கா? | One Calculation for a Boat; Another for a Country? | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/padagukku-oru-kanakku-naattukku-oru-kanakkaa` |
| 233 | `kalasangal-kalangarai-vilakkangalaagalam` | கலசங்கள், கலங்கரை விளக்கங்களாகலாம்! | Finials Can Become Lighthouses! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/kalasangal-kalangarai-vilakkangalaagalam` |
| 234 | `nalvazhikku-naattarayyaavin-urai` | நல்வழிக்கு நாட்டாரய்யாவின் உரை! | Nattarayya's Commentary on Nalvazhi! | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/nalvazhikku-naattarayyaavin-urai` |
| 235 | `anthaathi-paadiya-aruthakutti-naadar` | அந்தாதி பாடிய அருதகுட்டி நாடார் | Aruthakutti Nadar Who Sang an Anthathi | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/anthaathi-paadiya-aruthakutti-naadar` |
| 236 | `sinthanai-sey-maname` | சிந்தனை செய் மனமே | Think, O Mind | essays-articles / essay | `/essays/sinthanaiyum-seyalum/articles/sinthanai-sey-maname` |

**essays-thiraavida-sampaththu** — publication `thiraavida-sampaththu` · stage R3-C · 2 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 237 | `thiraavida-sampaththu-katturai` | திராவிட சம்பத்து | Dravidian Wealth | essays-articles / essay | `/essays/thiraavida-sampaththu/articles/thiraavida-sampaththu` |
| 238 | `aiyar-arivikkirar` | ஐயர் அறிவிக்கிறார்! | Iyer Announces! | essays-articles / essay | `/essays/thiraavida-sampaththu/articles/aiyar-arivikkirar` |

**essays-thudikkum-ilamai** — publication `thudikkum-ilamai` · stage R3-C · 2 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 239 | `thudikkum-ilamai-urai` | துடிக்கும் இளமை | Throbbing Youth | speeches / public-speech | `/essays/thudikkum-ilamai/articles/thudikkum-ilamai` |
| 240 | `annamalaikku-arogara` | அண்ணாமலைக்கு அரோகரா! | Arohara to Annamalai! | essays-articles / essay | `/essays/thudikkum-ilamai/articles/annamalaikku-arogara` |

**essays-unarchchimaalai** — publication `unarchchimaalai` · stage R3-C · 9 works

| # | Canonical id | Tamil title | English title | Shelf / subtype | Existing reading route |
|---:|---|---|---|---|---|
| 241 | `unarchchi-maalai` | உணர்ச்சி மாலை | Garland of Emotion | essays-articles / essay | `/essays/unarchchimaalai/articles/unarchchi-maalai` |
| 242 | `puratchi-valarntha-kathai` | புரட்சி வளர்ந்த கதை | The Story of How the Revolution Grew | essays-articles / essay | `/essays/unarchchimaalai/articles/puratchi-valarntha-kathai` |
| 243 | `pogiran-pogiran` | போகிறான்;போகிறான்..! | He Goes; He Goes..! | essays-articles / essay | `/essays/unarchchimaalai/articles/pogiran-pogiran` |
| 244 | `iravanan-nam-pattan` | இராவணன் நம் பாட்டன் | Ravana Is Our Grandfather | essays-articles / essay | `/essays/unarchchimaalai/articles/iravanan-nam-pattan` |
| 245 | `ingalla-irashyavil` | இங்கல்ல! இரஷ்யாவில் | Not Here! In Russia | essays-articles / essay | `/essays/unarchchimaalai/articles/ingalla-irashyavil` |
| 246 | `3-57-90` | 3, 57, 90. | 3, 57, 90. | essays-articles / essay | `/essays/unarchchimaalai/articles/3-57-90` |
| 247 | `30-1-1948` | 30-1-1948 | 30-1-1948 | essays-articles / essay | `/essays/unarchchimaalai/articles/30-1-1948` |
| 248 | `paththiniye-unpol` | பத்தினியே உன்போல்...! | O Chaste Woman, Like You...! | essays-articles / essay | `/essays/unarchchimaalai/articles/paththiniye-unpol` |
| 249 | `annai-nagammaiyar` | அன்னை நாகம்மையார்! | Mother Nagammaiyar! | essays-articles / essay | `/essays/unarchchimaalai/articles/annai-nagammaiyar` |
