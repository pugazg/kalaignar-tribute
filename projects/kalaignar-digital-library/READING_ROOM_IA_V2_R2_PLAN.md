# Reading Room IA v2 — R2 Plan (Category-First Information Architecture)

**Created:** 2026-09-25.

**Status: R2 — AUTHORIZED. R2 PLAN — COMPLETE / REVIEWED / FROZEN. R2-A — COMPLETE / REVIEWED / MERGED. R2-B — NOT
STARTED / NOT AUTHORIZED. R2-C — NOT STARTED.**

**Lifecycle note (added 2026-09-26; lifecycle wording only — §§1–20 are unchanged).**
- This plan passed independent exact-head review (PASS). It was merged as `pugazg/kalaignar-tribute#46` by a normal
  merge `811fdc214f5e290cca5d18b660a29d27b4d43b37`, pinned to the approved head
  `df99c0ea9bc3f0dfaadde9417be762ec9fb6a6c1` (0 content delta). It is now frozen.
- R2-A was implemented, reviewed and merged as `pugazg/kalaignar-autobiography#102` (merge `19c0ee15…`). See
  [`READING_ROOM_IA_V2_R2A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R2A_CHECKPOINT.md).
- R2-B requires a separate owner authorization; this plan does not by itself authorize it.
- The header text below, including "No R2 implementation branch exists", describes this plan as written at its creation.

This is a **control-only planning record**:
- implementation delta = **0**;
- source delta = **0**;
- production mutation = **0**.

No R2 implementation branch exists and none is created by this plan.

---

## 1. Authorization record

The owner explicitly stated: **"Authorize R2 and proceed with R2 planning."**
- R2 is therefore **AUTHORIZED**.
- This activity is **planning only**. Implementation (R2-A onward) starts only after independent review and merge of
  this plan, and each implementation stage keeps the exact-head review gate.

## 2. Live pins

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base) | `d66db0e05aef1f7691fbcabd502e4a7953028c24`, tree `e2f1647606f5412c974ab076a44674d98835f96d` (merge of #45) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `f991043c3353abe9f2b334f7c8d57e433184d126`, tree `87ca371b084c337ba2163caa6c336615174074e9`; 0 open PRs; no R2 / IA-v2 / category branch |
| Production | Vercel Production deployment `6638432286` for `f991043c…` |
| Framework | Next.js `^14.2.35`, App Router (`app/`) |

## 3. Frozen authority (unchanged by this plan)

| Record | Blob |
|---|---|
| `READING_ROOM_IA_V2_R0_CENSUS.md` | `cee919231e161be1ee7335b30853e82b6e34e4f7` |
| `READING_ROOM_IA_V2_R1_IDENTITY_RECONCILIATION.md` | `42de6fa05049bf042c4d0e831fc69f188606d375` |
| `READING_ROOM_IA_V2_R1_MANIFEST.json` | `7013177259d8914258397a2894bdf299ae4c0f14` |
| `READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json` | `34ff3b1b02fd2813919b48afe006e35262dbf065` |
| `READING_ROOM_IA_V2_OWNER_HOLD_ADJUDICATION.md` (post-#45) | `9cec1d37517662029d42f002393aa48cb2992363` |
| `READING_ROOM_IA_V2_RESOLVED_MANIFEST.json` | `b7b3530d54ba9c354b43313eecd69e78e76a92b5` |

- **Resolved manifest:** 315 rows = CREATE 249 · KEEP_EXISTING 27 · ADD_WITNESS 19 · DO_NOT_PROMOTE 20 · HOLD 0.
- **Owner decisions:** HOLD→CREATE 31 · HOLD→ADD_WITNESS 3.
- **Projection:** raw 584; provisional pre-R2 net 579.
- **Use in R2:** none. This is R3 authority (§6).

## 4. Current implementation architecture (inspected at `f991043c`)

**Data model**
- **`data/library.ts`:**
  - `ShelfId` and `SHELVES`: 9 shelves, each with `order`, `ta` and `en`; `life-writing` has the Tamil label
    `வாழ்க்கை எழுத்து`.
  - `LIBRARY_WORKS` (335) and `publishedWorks()`.
  - `visibleShelves()`: shelves with their published works, in taxonomy order, omitting empty shelves.
- **`data/collections.ts`:**
  - `LIBRARY_COLLECTIONS` (9) and `collectionsForWork()`.
  - `discoveryShelves()`: collections first, then works that belong to no collection. This is the
    collection-substitution model.

**The `/read` landing**
- `app/read/page.tsx` renders `<LibraryHome dailyKural={<DailyKural />} />` with `export const revalidate = 900`.
  That revalidation exists only to keep the Daily Kural fresh.
- `components/LibraryHome.tsx` (client) provides:
  - the header (Home link, `கலைஞர் மின்னூலகம்`, `Kalaignar Digital Library`, intro copy);
  - `shelfIcon` (a `ShelfId`→icon map), `accentFor`, `WorkCard`, `CollectionCard`, `DiscoveryCard`;
  - `INITIAL_WORKS_PER_SHELF = 6` with a native `<details>` overflow disclosure.

**`/read` namespace**

| Route | Handled by |
|---|---|
| `/read` | `app/read/page.tsx` |
| `/read/nenjukku-neethi` | `app/read/nenjukku-neethi/page.tsx` (static) |
| `/read/[id]` | `app/read/[id]/page.tsx` — `generateStaticParams()` over `chapterIndex` (391 ids, pattern `v{1–6}-ch{nn}`); unknown ids → `notFound()` |

**Where things are used**
- **`DailyKural`:** rendered only in `app/read/page.tsx`. `components/DailyKural.tsx` and `lib/daily-kural.ts` have no
  other consumer.
- **Back-links to `/read`:** about 30 reader, source and landing components link to `/read` (mostly labelled
  "மின்னூலகம்"). They stay valid, because `/read` remains the library landing.
- **Sitemap:** `app/sitemap.ts` emits `/read`, `/read/nenjukku-neethi` and the 391 `/read/{chapter}` URLs, among others.
  The live baseline is 5262 URLs with 0 duplicates.

**Tests coupled to the current `/read`**
- **Rendered-`/read` assertions (7 scripts):** these import `LibraryHome` and assert rendered cards, so they need R2
  rework:
  - `test-shelf-disclosure`, `test-collections`, `test-wave8-p4-publication-ui`, `test-standalone-poem-ui`;
  - `test-wave5-p4-cinema-ui`, `validate-wave6-p4-integration`, `validate-wave5-p4-cinema-integrity`.
- **Data-level assertions (about 20 validators):** these assert `discoveryShelves()` totals (98 / 42 and
  per-shelf entries). They keep passing if `discoveryShelves()` is retained unchanged.
- **Sitemap and build pins (many validators):** these pin whole-build totals (sitemap 5262; build 5271 / 5266 / 5274).
  Today they reconcile through derived contribution modules; `lib/wave8-contribution.ts` alone has 23 users.

## 5. R2 scope

R2 implements the category-first hierarchy over the **existing live catalogue of 335 works**:

```text
/read  →  category (9)  →  canonical LibraryWork (existing)  →  existing work reader / reading units
```

## 6. Explicit R2 / R3 boundary

**R2 is information architecture only.** It does **not**:
- create any of the 249 resolved-manifest CREATE works;
- perform the five existing-work canonical merges;
- implement Sangatamil or 1958 `தேனலைகள்` witness metadata;
- vendor or ingest new source content;
- create new readers;
- change any canonical identity decision;
- expand the catalogue towards 579.

All of that belongs to the later **R3 — canonical-work promotion / catalogue reconciliation** stage, which consumes the
frozen resolved manifest.

**Terminology note.** The frozen owner-adjudication record and the resolved manifest call these merge/witness actions
"future R2" (field `futureR2Actions`), because they were written before the owner split the work into R2 and R3.
- Those frozen files are **not edited**.
- Under this plan, every action they label "future R2" is scheduled for **R3**, and R2 performs none of them. The five R3 merges are:
- `sirai-kodiyathu` → `green-parrot`
- `neeyum-kaithi-naanum-kaithi` → `piraiye`
- `aadik-kaatre` → `adikkaatru`
- `pugazhe-nee-oru-pudhir` → `pugazh`
- `sorgaththirku-vandhathu-eppadi` → `sorgga-logaththil`

## 7. Category-route map (chosen)

| Shelf id (unchanged) | Public Tamil | English | Route |
|---|---|---|---|
| `life-writing` | **`சுயசரிதை`** (was `வாழ்க்கை எழுத்து`) | Life Writing | `/read/autobiography` |
| `letters` | `கடிதங்கள்` | Letters | `/read/letters` |
| `fiction` | `புனைகதை` | Fiction | `/read/fiction` |
| `poetry` | `கவிதைகள்` | Poetry | `/read/poetry` |
| `drama` | `நாடகங்கள்` | Drama | `/read/drama` |
| `cinema-writing` | `திரை எழுத்து` | Cinema Writing | `/read/cinema` |
| `speeches` | `உரைகள்` | Speeches | `/read/speeches` |
| `essays-articles` | `கட்டுரைகள்` | Essays & Articles | `/read/essays` |
| `literary-commentary` | `இலக்கிய உரை` | Literary Commentary | `/read/literary-commentary` |

- Stored shelf ids are **not** renamed.
- The only label change is the public Tamil label of `life-writing`. It is a single-line edit (`data/library.ts:45`),
  and `வாழ்க்கை எழுத்து` occurs nowhere else in `app/`, `components/`, `lib/`, `data/` or `scripts/`.

## 8. `/read` landing contract (after R2-B)

- It renders **exactly 9 category cards**, in `SHELVES` order.
- It renders **no** individual work cards, collection cards, anthology cards or publication-container cards.
- It renders **no** Daily Kural panel (§11).
- Each card shows:
  - the Tamil label and the English label;
  - the canonical work count (primary);
  - the shelf icon, reusing the existing `shelfIcon` map;
  - a link to the category route.
- Fiction and Speeches add the collection count as secondary metadata, e.g. `162 works · 7 collections`. The old
  collection-substituted discovery count is never shown.
- The existing header (Home link, `கலைஞர் மின்னூலகம்`, `Kalaignar Digital Library`), the design language, dark mode,
  focus rings and language toggle are preserved.
- Metadata: `/read` is described as the category-first Kalaignar Digital Library. It no longer enumerates a few named
  works.

## 9. Category-page contract

- Each category page lists **every published canonical LibraryWork** whose `shelf` is that category, derived from
  `publishedWorks()`.
- **Collection membership never suppresses a work.** All 145 anthology-member short stories and 4 anthology-member
  novels appear on `/read/fiction`, and all 97 `முத்துக் குளியல்` speeches appear on `/read/speeches`.
- **Order:** the existing deterministic catalogue (declaration) order. No chronology, alphabetical or Tamil collation,
  popularity or ranking is introduced.
- Work entries reuse the existing `WorkCard` presentation, which links to the work's current `href`. Existing work
  readers are untouched.
- **Expected counts:** autobiography 1 · letters 1 · fiction 162 · poetry 14 · drama 11 · cinema 10 · speeches 117 ·
  essays 15 · literary-commentary 4 = **335**. Every work appears on exactly one category page.
- Every category page links back to `/read`.

**Letters special case** (frozen R0 §6.2: *"Corpus navigation by volume and sequence is legitimate here. It should be
handled specially on the Letters category page."*)
- `/read/letters` has exactly **one** canonical LibraryWork, `murasoli-letters`, displayed once.
- Because this work is a corpus — currently **13 volumes and 688 letters, Volumes 42–54** — the category page also
  provides corpus-level volume/sequence wayfinding into the existing `/murasoli` browser, with a clear "Browse by
  volume & sequence" affordance.
- The existing `/murasoli` surface remains the authoritative detailed volume/sequence browser. The category page does
  **not** duplicate the full 688-letter navigation. A small derived summary (for example the volume range and counts)
  is allowed, and a fuller embedded summary only if later implementation evidence shows it is beneficial.
- Volume-range and corpus-count metadata shown on the page is derived from the same authoritative Murasoli data
  (`public/data/murasoli/index.json`: `volumeCount`, `volumes[].volume`; `letters-index.json`: letter count). It is not
  a duplicated hand-typed catalogue fact.
- **Volumes and individual letters remain dependent corpus navigation, not LibraryWorks.**
  - No volume or letter becomes a canonical identity.
  - No new volume routes are invented.
  - `/murasoli/<letter-id>` is unchanged; the route id stays the identity, and the printed letter number is never the
    route identity.
  - The `murasoli-letters` canonical identity and the 335-work catalogue are unchanged.

```text
/read/letters
  → canonical work: murasoli-letters (1)
  → corpus summary · Browse by volume & sequence
  → /murasoli  (existing volume-grouped navigation)
      → /murasoli/<letter-id>  (existing, unchanged)
```
- Metadata per category identifies the Kalaignar Digital Library, the category and canonical-work browsing. No
  historical or source claims are fabricated.

## 10. Collection / provenance treatment

- All 9 `LibraryCollection`s, all `/collections/...` routes and `collectionsForWork()` stay unchanged.
- Category pages may show a **visually secondary** "Collections / தொகுப்புகள்" section, reusing `CollectionCard`,
  **after** the full work list: Fiction 7, Speeches 2, all other categories 0.
- A collection never replaces a member work.
- **`discoveryShelves()` is retained unchanged** as a data function. `/read` simply stops rendering it. This keeps the
  roughly 20 data-level validators green without rewriting frozen history.
- No new `LibraryCollection` objects are created from publications known to the resolved manifest; that is outside R2.

## 11. DailyKural treatment

- `DailyKural` is rendered **only** on `/read`. R2-B stops rendering it there.
- `components/DailyKural.tsx`, `lib/daily-kural.ts` and `test:daily-kural` are **retained**; no Thirukkural
  functionality is removed.
- No new placement is invented.
- The `revalidate = 900` on `app/read/page.tsx` exists only for the Daily Kural. R2-B may drop it, but only after
  verifying that the prerender and HTML counts are unaffected; otherwise it is kept.

## 12. Implementation file-impact plan

**New files**

| File | Purpose |
|---|---|
| `data/read-categories.ts` | the **single category registry**: `ShelfId` → `{ slug, route, metaTitle, metaDescription }` for all 9 shelves; helpers `categoryForShelf(id)`, `worksInCategory(id)` (from `publishedWorks()`), `collectionsInCategory(id)` (from `LIBRARY_COLLECTIONS`). It stores no work membership. |
| `components/LibraryCategoryPage.tsx` | one shared category page: header, work list (`WorkCard`), secondary collections (`CollectionCard`), back-link, plus one small optional corpus slot used only by Letters |
| Letters corpus treatment (inside `LibraryCategoryPage`, or a small `components/LettersCorpusSummary.tsx`) | shows the corpus summary (13 volumes · 688 letters · Volumes 42–54) derived from the existing `public/data/murasoli/index.json` and `letters-index.json`, plus a "Browse by volume & sequence" link to `/murasoli`. No new data model, route or identity; `/murasoli` and `MurasoliLibrary` are reused, not rebuilt |
| `components/CategoryCard.tsx` (or a section inside `LibraryHome`) | the `/read` category card |
| `app/read/{autobiography,letters,fiction,poetry,drama,cinema,speeches,essays,literary-commentary}/page.tsx` | 9 thin static route files, each `generateMetadata` + `<LibraryCategoryPage shelf="…"/>` |
| `lib/read-ia-r2-contribution.ts` | derived reconciliation (`sitemap` / `build` = number of registry routes, i.e. 9), following the established `lib/wave8-contribution.ts` pattern |
| `scripts/test-read-categories.ts` (+ `test:read-categories` in `package.json` and a CI step) | the R2 acceptance validator (§16) |

**Modified files**

| File | Change |
|---|---|
| `data/library.ts` | `life-writing` Tamil label → `சுயசரிதை` (one line) |
| `components/LibraryHome.tsx` | landing body → 9 category cards; `WorkCard` / `CollectionCard` / `shelfIcon` / `accentFor` exported for reuse (no visual change to cards) |
| `app/read/page.tsx` | stop rendering `DailyKural`; category-first metadata |
| `app/sitemap.ts` | +9 category URLs from the registry |
| 7 rendered-`/read` scripts (§4) | move their card assertions from the `/read` landing to the matching category page and assert the new landing contract; no weakening |
| sitemap / build-pinned validators | add the derived `R2` term, and exclude the 9 category routes from any frozen pre-wave route remainder; no hand-typed totals |
| `.github/workflows/library-ci.yml` | one step for `test:read-categories` |

**Not modified:** every existing reader, work route, collection route and `/source` route; `discoveryShelves()`;
`LIBRARY_WORKS`; `LIBRARY_COLLECTIONS`; the resolved manifest.

## 13. Route-collision analysis

- **Memoir chapters:** the 9 category slugs were checked against all **391** memoir chapter ids (`v{1–6}-ch{nn}`) from
  `chapterIndex` at `f991043c`, and against `nenjukku-neethi`. There are **0 collisions**.
- **Static versus dynamic routes:** in the Next.js App Router, static segments (`app/read/fiction/…`) take precedence
  over the dynamic `app/read/[id]`. None of the 9 slugs is a chapter id, so no chapter URL changes behaviour, and
  unknown ids still `notFound()`.
- **Memoir route:** the `[id]` route is **not** refactored.
- **Top-level namespaces:** `/cinema`, `/speeches` and `/essays` are distinct from `/read/cinema`, `/read/speeches`
  and `/read/essays`. There is no technical collision; the category pages are an index over those readers.

## 14. Catalogue and category arithmetic (re-derived from live `f991043c`)

| Metric | Before R2 | After R2 |
|---|---:|---:|
| LibraryWorks (published / unique ids) | 335 / 335 | 335 / 335 |
| Shelf counts (life-writing · letters · fiction · poetry · drama · cinema · speeches · essays · literary-commentary) | 1 · 1 · 162 · 14 · 11 · 10 · 117 · 15 · 4 | unchanged |
| Categories | 9 | 9 |
| Collections | 9 (Fiction 7, Speeches 2) | 9 |
| `/read` primary cards | 98 discovery entries / 42 initially visible | **9 category cards** |
| `discoveryShelves()` (retained data function) | 98 / 42 | 98 / 42 (not rendered on `/read`) |
| Resolved-manifest CREATE items implemented | 0 | **0** |
| R3 canonical merges performed | 0 | **0** |

Check: 1 + 1 + 162 + 14 + 11 + 10 + 117 + 15 + 4 = **335**. Every published work sits on exactly one shelf.

## 15. Sitemap projection

- **R2 adds exactly 9 public category routes.** The sitemap goes from 5262 URLs (0 duplicates) to a **projected
  5271 / 0 duplicates**.
- The **build** gains 9 static pages. Projected: prerender 5271 → 5280, HTML 5266 → 5275, generated static pages
  5274 → 5283.
- These are planning projections. Implementation must derive and verify the exact counts from the live build, and must
  not force them if a legitimate concurrent route change has occurred.

## 16. Acceptance tests (for implementation; defined here)

All tests are to be implemented in `scripts/test-read-categories.ts` unless an existing test is the natural owner. The
existing CI also runs, in full.

1. **Landing**
   - `/read` returns 200 and renders exactly 9 category cards, with unique links equal to the 9 registry routes.
   - It renders 0 work cards, 0 collection cards and no Daily Kural panel.
   - The `life-writing` card shows `சுயசரிதை`.
2. **Category coverage**
   - Each of the 9 routes returns 200 and shows exactly 1 / 1 / 162 / 14 / 11 / 10 / 117 / 15 / 4 work entries
     (total 335).
   - The union of work entries is all 335 published ids, each appearing exactly once across all category pages.
   - Every anthology member (149 Fiction works, 97 Speeches) is present individually.
3. **Letters corpus (special case)**
   - `/read/letters` returns 200.
   - The canonical LibraryWork count on the page is 1.
   - `murasoli-letters` appears exactly once as a canonical work.
   - The corpus treatment identifies **13 volumes / 688 letters** (Volumes 42–54). The values either match this
     accepted baseline or are derived equivalently from live `public/data/murasoli/index.json` and
     `letters-index.json`.
   - A clear link to `/murasoli` is present.
   - No individual letter and no volume is rendered as a LibraryWork.
   - `/murasoli` and representative `/murasoli/<id>` routes (for example `m42-l3364` and `m48-l3706`) remain valid.
4. **Collections**
   - The Fiction page exposes 7 secondary collection links, the Speeches page 2, and the others 0.
   - Collection entries never replace work entries.
   - All 9 `/collections/<id>` routes are unchanged.
5. **Route preservation**
   - `/read/nenjukku-neethi` and all 391 `/read/{chapter}` routes return 200.
   - A representative work route, child route and `/source` route in every reader family (stories, novels, poems,
     plays, cinema, speeches, essays, murasoli, thirukkural, tholkappiyam, kuraloviyam, sangatamil) keeps its behaviour.
   - Invalid routes still 404 (for example `/read/v9-ch99` and `/read/not-a-category`).
6. **Sitemap**
   - All 9 category URLs appear exactly once, with 0 duplicates.
   - The pre-R2 URL set is a subset of the post-R2 set, so no URL disappears.
   - Total = pre-R2 + 9, derived rather than typed.
7. **Catalogue invariance**
   - 335 works; the shelf counts above; 9 collections.
   - The resolved-manifest blob is unchanged.
   - None of the 249 CREATE ids exists as a LibraryWork.
   - The 5 R3 merge sources are still separate Fiction works.
8. **Regression**
   - Run `npm run typecheck`, `npm run lint`, `npm run build` and `npm run validate`.
   - Run `test:collections`, `test:shelf-disclosure` (rescoped), `test:daily-kural` (component still passes) and the
     full CI (`library-ci.yml` build and archival jobs).
   - Check accessibility on the modified surfaces: headings, landmarks, focus rings, the 44px touch target, dark-mode
     contrast and `lang` attributes.

## 17. Staged implementation sequence

Each stage is one implementation PR, gated by exact-head review.

| Stage | Contents | `/read` landing |
|---|---|---|
| **R2-A — Category model + routes** | `data/read-categories.ts`; `LibraryCategoryPage`; 9 static category routes plus metadata; **the Letters corpus treatment (§9)**; `test-read-categories` (coverage, invariance and the Letters tests in §16.3); reuse exports from `LibraryHome` | unchanged (still the discovery view) |
| **R2-B — Category-only `/read`** | landing → 9 category cards; `சுயசரிதை`; `DailyKural` removed from `/read`; primary work / collection discovery removed from `/read`; the 7 rendered-`/read` tests re-scoped | switched |
| **R2-C — Provenance, sitemap and full regression** | secondary collection sections; sitemap +9; `lib/read-ia-r2-contribution.ts` reconciliation of pinned validators; full route-preservation, accessibility and CI; implementation close-out candidate | final |

The Letters corpus treatment belongs to R2-A because it is part of the frozen category contract.
- If implementation convenience requires its visual enhancement to land in R2-C, R2-A must at minimum establish the
  contract and the Letters tests.
- The final R2 completion gate (§20) requires it in every case.

If the live architecture makes the sitemap reconciliation smaller when it lands together with the new routes, R2-C's
sitemap part may move into R2-A. The semantic boundaries stay the same either way.

## 18. Rollback / preservation constraints

- **Additive only**, except for what the `/read` landing itself renders.
- No existing URL, route, reader, `/source` page, collection or citation identity is removed, renamed or redirected.
- Rollback of R2-B restores the previous `LibraryHome` body. The R2-A routes are additive and can remain.
- Frozen R0 and R1 records, the adjudication record and the resolved manifest are never edited by R2.
- No production deployment is part of R2 planning. Deploying implementation stages follows the normal merge-to-`main`
  process after review.

## 19. Explicit exclusions

- The 249 CREATE rows.
- The five R3 merges.
- Sangatamil and 1958 witness implementation.
- New source ingestion and new readers.
- Canonical-identity or shelf changes.
- New sorting or search features.
- Relocating Daily Kural.
- Converting publications into collections.
- Updating the roughly 30 `/read` back-links to category routes. They remain valid; any such refinement is separate
  and optional.
- R3.
- Production deployment in this planning stage.

## 20. Completion criteria

R2 is complete when:
- R2-A, R2-B and R2-C are merged at reviewed exact heads;
- every acceptance test in §16 passes on a clean build of the final implementation head;
- remote CI (typecheck • build, archival validators) and Vercel succeed;
- production verification confirms `/read` shows 9 category cards, the 9 category pages show 335 works in total, and
  the sitemap equals the pre-R2 set plus 9 with 0 duplicates;
- `/read/letters` provides the Letters corpus treatment (§9): 1 canonical work, 13 volumes / 688 letters as corpus
  navigation only, and a link into `/murasoli`;
- a control close-out records R2 COMPLETE with implementation, source and catalogue invariance.

Catalogue expansion then proceeds only in a separately authorized **R3**.
