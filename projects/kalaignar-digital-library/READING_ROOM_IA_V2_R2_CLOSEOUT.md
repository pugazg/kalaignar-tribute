# Reading Room IA v2 — R2 Close-out (Category-First Information Architecture)

**Recorded:** 2026-09-26.

**Status: R2 PLAN — COMPLETE / REVIEWED / FROZEN. R2-A, R2-B and R2-C — COMPLETE / REVIEWED / MERGED. R2
IMPLEMENTATION — COMPLETE / PRODUCTION-ACCEPTED. This close-out record — REVIEW-READY (awaiting independent exact-head
review). R3 — NOT AUTHORIZED.**

This is the **control-only** final record of the R2 stage. It records implementation work that has already been
independently reviewed, merged and accepted on production.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

Every implementation merge reached production through the repository's existing Vercel Git integration (automatic
deploy of `main`). No manual deployment was made at any stage.

- **Authority:** [`READING_ROOM_IA_V2_R2_PLAN.md`](./READING_ROOM_IA_V2_R2_PLAN.md) (frozen).
- **Stage records:** [`READING_ROOM_IA_V2_R2A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R2A_CHECKPOINT.md) and
  [`READING_ROOM_IA_V2_R2B_CHECKPOINT.md`](./READING_ROOM_IA_V2_R2B_CHECKPOINT.md), both unchanged.

**Owner authorizations (verbatim):**
- "Authorize R2 and proceed with R2 planning." (the plan)
- "R2-A IS AUTHORIZED." (R2-A only)
- "Authorize R2-B and proceed with R2-B."
- **"Authorize R2-C and proceed with R2-C."**

---

## 1. Live pins (re-fetched 2026-09-26)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this close-out) | `4156aa0937419523bff5c6df873a1f48a95a6709` (tree `cd4d67817d3790a7d1a3cf23c365f18b02b221a5`) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `597e65fde3266baffda98351de716507368b5ebc` (tree `da22e2f49f7db1be94591acb2838f28e69c3a2e8`); 0 open implementation PRs |
| Production | Vercel deployment `6674301852` at `597e65fd…` (environment `Production`, success) |
| Source repositories (unchanged throughout R2) | poems `188d49cd` · literary-commentary `e23548b0` · essays `63019a4d` · short-stories `7205a108` |

## 2. Implementation merges

Every stage was merged by a normal merge commit pinned to its approved head (`--match-head-commit`). None was squashed,
rebased or amended.

| Stage | PR | Reviewed base | Approved head (commits · files · diff) | Merge | Merge tree (= head tree) | Parents | Head → merge |
|---|---|---|---|---|---|---|---|
| R2-A | `#102` | `f991043c3353abe9f2b334f7c8d57e433184d126` | `1607b8923f6aa7f2640543c31326ded3d93ebcdc` (2 · 31 · +724/−27) | `19c0ee15a5a78d04852be2144a72a0328d307400` | `d899d04f6eebfdece3a215a1f62899c72b0af4df` | `f991043c…`, `1607b892…` | 0 files |
| R2-B | `#103` | `19c0ee15…` | `07dd8a7fdec4590014a39931cae0701c001b670c` (1 · 13 · +432/−356) | `89c682553d6ba07a96e966bb982d60ebe0cd8b47` | `cb70d85767739ed43d75d7db54ddaa6f41fdfdbe` | `19c0ee15…`, `07dd8a7f…` | 0 files |
| R2-C | `#104` | `89c68255…` | `3b3b886854c1ffa67763e0f51450985cb154e438` (1 · 23 · +197/−58) | `597e65fde3266baffda98351de716507368b5ebc` | `da22e2f49f7db1be94591acb2838f28e69c3a2e8` | `89c68255…`, `3b3b8868…` | 0 files |

For R2-C, base → merge is exactly `3b3b8868` plus `597e65fd` over the same 23 files (+197/−58), with no extra commit.

## 3. CI and deployments

| Stage | Library CI at approved head | Library CI at merge (`typecheck • build` + `archival validators`) | Production deployment (vercel[bot]) |
|---|---|---|---|
| R2-A | success | run `36210629536` — SUCCESS / SUCCESS | `6673494910` at `19c0ee15…` |
| R2-B | success | run `36212919374` — SUCCESS / SUCCESS | `6673879019` at `89c68255…` |
| R2-C | run `36214650585` — SUCCESS / SUCCESS | run `36215615102` — SUCCESS / SUCCESS | `6674301852` at `597e65fd…` (2026-09-26T03:46:58Z) |

- The Vercel commit status was success at every approved head and merge.
- The GitHub deployment objects report `production_environment: false`. So did the pre-R2 Production deployment
  (`6638432286` at `f991043c…`); the environment name `Production` is authoritative.

## 4. What R2 delivered

| Stage | Delivered |
|---|---|
| **R2-A** | The category registry `data/read-categories.ts` (9 `ShelfId`s → `/read/<slug>`, no membership stored). The shared `components/LibraryCategoryPage.tsx`. Nine static category routes. The Letters corpus treatment (`components/LettersCorpusSummary.tsx`, `lib/murasoli-corpus.ts`). The validator `scripts/test-read-categories.ts`. Build +9 pages. |
| **R2-B** | `/read` → exactly 9 category cards (`CategoryCard`), with the work count primary and collections secondary (Fiction 7, Speeches 2). The shared `life-writing` Tamil label is now `சுயசரிதை`. Daily Kural is removed from `/read` (component, logic and test retained), and `revalidate = 900` is removed. The discovery rendering and disclosure are retired from `/read`; `discoveryShelves()` is retained as data. The 7 rendered-`/read` tests were re-scoped without weakening. |
| **R2-C** | Secondary bilingual **தொகுப்புகள் / Collections** sections on category pages, after the full work list, using the existing `CollectionCard`: Fiction 7, Speeches 2, none elsewhere. **Sitemap +9**, derived from `READ_CATEGORY_ROUTES`. The canonical **`lib/read-ia-r2-contribution.ts`** (`build` = `sitemap` = `READ_IA_R2_ROUTES.length`; the R2-A object in `data/read-categories.ts` was removed, not duplicated). Every whole-build and whole-sitemap-pinned validator was reconciled by an explicit derived R2 term or exclusion. `test:read-categories` reached 440 checks. |

**R2-C validator reconciliation (census).** Historical terms were unchanged; R2 enters only as a derived additive or exclusion term.

| Scope | Files | R2 term |
|---|---|---|
| Whole-sitemap pin | `test-wave5-p3-cinema-catalogue`, `validate-wave5-p4-cinema-integrity`, `validate-wave7-b1-p1`, `validate-wave7-b1-p4-integration`, `validate-wave7-b2-b4-p4-integration`, `validate-wave7-b5-b6-k-p4-integration`, `validate-wave8-p1-hidden`, `validate-wave8-p3-routes` | + `R2.sitemap` |
| Sitemap pin and record remainder | `validate-wave6-p4-integration`, `validate-wave6-b7-p4-integration` | ± `R2.sitemap` |
| Sitemap pin and P3 remainder | `validate-wave8-p4-integration` | + `R2.sitemap`; remainder excludes `READ_IA_R2_ROUTES` |
| Record regeneration | `build-wave8-p4-publication.ts --verify` | Excludes the R2 category URLs, so the frozen Wave-8 P4 record (`data/internal/wave8/wave8-p4-publication.json`, blob `0cbec7a2…`) still regenerates byte-for-byte and is unchanged |
| Build-only pins | `validate-wave6-p3-build`, `validate-wave7-b1-p3-routes`, `validate-wave7-b2-b4-p1-hidden`, `validate-wave7-b2-b4-p3-routes`, `validate-wave7-b5-b6-k-p3-routes` | Import moved to the canonical module |

`test-collections` scopes the Fiction and Speeches page checks to the work grid plus the Collections section.

## 5. Final production acceptance (read-only, `nenjukkuneethi.org`, after deployment `6674301852`)

107 checks were run and 105 passed. The 2 that did not pass were `/speeches` and `/essays`, which I had wrongly added to
the list as representative routes. **No page exists at those URLs at any stage:** only `app/speeches/[slug]` and
`app/essays/[slug]` exist, both before R2 (`f991043c`) and now, and neither URL was ever in the sitemap. Representative
speech and essay routes (`/speeches/udhaya-kathir`, `/essays/meesai-mulaiththa-vayathil` and their `/source`) return
200. **There is no regression.**

**`/read`**

| Check | Result |
|---|---|
| Status | 200 |
| Category cards | exactly **9**, linking the nine routes in shelf order |
| Links in `<main>` | only those 9 (no work card, no collection card) |
| `<details>` | 0 |
| Daily Kural | none |
| First card | `சுயசரிதை` |
| Card counts | 1 · 1 · **162 · 7 collections** · 14 · 11 · 10 · **117 · 2 collections** · 15 · 4 |

**Category pages**

| Page | Work cards | Collection cards |
|---|---:|---:|
| `/read/autobiography` | 1 | 0 |
| `/read/letters` | 1 | 0 |
| `/read/fiction` | 162 | 7 (after the works) |
| `/read/poetry` | 14 | 0 |
| `/read/drama` | 11 | 0 |
| `/read/cinema` | 10 | 0 |
| `/read/speeches` | 117 | 2 (after the works) |
| `/read/essays` | 15 | 0 |
| `/read/literary-commentary` | 4 | 0 |
| **Total** | **335** (335 distinct) | **9** |

- All nine pages return 200, and no collection card sits inside a work grid.
- The seven pages without collections have **no Collections section and no empty heading**.
- **Collection links:** the 9 point to the existing `/collections/<id>` routes, all 200.
- **Letters:** one canonical work (`/murasoli`) plus Volumes 42–54 · 13 volumes · 688 letters, and the
  `/murasoli` browse link.

**Routes**
- **200:** `/read/nenjukku-neethi`, `/read/v1-ch01`, `/read/v6-ch01`, `/murasoli`, `/murasoli/m42-l3364`,
  `/murasoli/m48-l3706`, `/stories/kizhavan-kanavu` (+ `/source`), `/novels/balipeedam-nokki`,
  `/poems/kaalap-pezhaiyum-kavithai-saaviyum`, `/plays/ore-mutham` (+ `/main-30`), `/cinema/manohara`,
  `/cinema/parasakthi`, `/thirukkural`, `/tholkappiyam`, `/kuraloviyam`, `/sangatamil` (+ `/source`).
- **404:** `/read/v9-ch99`, `/read/not-a-category`, `/stories/not-a-real-story`,
  `/collections/not-a-real-collection`, `/murasoli/m42-l3377`.
- **All 5271 sitemap URLs return 200 on production.** That covers all 391 memoir chapters, every reader family, 331
  `/source` routes and the 9 collections.

**Sitemap:** **5271** URLs, 0 duplicates, each category URL exactly once. The sitemap minus the nine category routes
equals the frozen pre-R2 set **exactly**: 5262 paths, sha256 `5e017f0238ac1849ee4209e50306fe600125f84ee3c704bf527f29f747ffe2b5`,
measured on implementation tree `cb70d857` and pinned in `test:read-categories`.

## 6. Final R2 arithmetic

| Measure | Pre-R2 (`f991043c`) | R2-A | R2-B | R2-C (final) |
|---|---:|---:|---:|---:|
| Published LibraryWorks | 335 | 335 | 335 | **335** |
| Shelf counts (1/1/162/14/11/10/117/15/4) | ✓ | ✓ | ✓ | **✓** |
| Collections (Fiction 7, Speeches 2) | 9 | 9 | 9 | **9** |
| Category routes | 0 | 9 | 9 | **9** |
| `/read` primary cards | 98 discovery entries / 42 visible | unchanged | 9 category cards | **9 category cards** |
| Prerendered routes / HTML | 5271 / 5266 | 5280 / 5275 | 5280 / 5275 | **5280 / 5275** |
| Sitemap URLs | 5262 | 5262 | 5262 | **5271** (+9, 0 duplicates) |
| `READ_IA_R2_CONTRIBUTION` | — | build 9 | build 9 | **build 9 · sitemap 9** (derived) |

- The build figures at the R2-C merge are enforced by the build-pinned validators in merge CI run `36215615102`
  (SUCCESS).
- `discoveryShelves()` is unchanged as a data model (98 entries, 42 within the historical cap) and is no longer rendered.

## 7. Invariance

**Unchanged at the final merge `597e65fd…` relative to R2-B `89c68255…`:**

| File | Blob |
|---|---|
| `data/library.ts` | `d2d9922a…` |
| `data/collections.ts` | `b7e8f4ce…` |
| `components/LibraryHome.tsx` | `244eed97…` |
| `app/read/page.tsx` | `3bdd0369…` |
| `app/read/[id]/page.tsx` | `ee47680c…` |
| `app/read/nenjukku-neethi/page.tsx` | `8412efab…` |
| `components/LettersCorpusSummary.tsx` | `ca64279a…` |
| `lib/murasoli-corpus.ts` | `eba1d1ab…` |
| Frozen Wave-8 P4 record | `0cbec7a2…` |

The only R2-C application changes are `app/sitemap.ts`, `components/LibraryCategoryPage.tsx`,
`data/read-categories.ts` and the new `lib/read-ia-r2-contribution.ts`.

**Across R2 as a whole**
- **No existing public URL was removed, renamed, redirected or repurposed.** R2 added exactly the 9 category routes.
- **Source delta 0**, and no source was ingested.
- **Catalogue delta 0**, and no new reader was added.
- **R3 delta 0.**
  - None of the **249** resolved-manifest CREATE candidates exists as a LibraryWork. The published-id digest pinned at
    the R2 base still passes.
  - None of the five canonical merges occurred; all five sources remain separate Fiction works and no target exists:
    - `sirai-kodiyathu → green-parrot`;
    - `neeyum-kaithi-naanum-kaithi → piraiye`;
    - `aadik-kaatre → adikkaatru`;
    - `pugazhe-nee-oru-pudhir → pugazh`;
    - `sorgaththirku-vandhathu-eppadi → sorgga-logaththil`.
  - No Sangatamil or 1958 `தேனலைகள்` witness change occurred.

## 8. Lifecycle

| Stage | Status |
|---|---|
| R0 | COMPLETE / REVIEWED / FROZEN |
| R1 | COMPLETE / REVIEWED / FROZEN |
| Owner HOLD adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 plan | COMPLETE / REVIEWED / FROZEN (`pugazg/kalaignar-tribute#46` → `811fdc21…`) |
| R2-A | COMPLETE / REVIEWED / MERGED (`#102` → `19c0ee15…`; checkpoint `pugazg/kalaignar-tribute#47` → `a9600327…`) |
| R2-B | COMPLETE / REVIEWED / MERGED (`#103` → `89c68255…`; checkpoint `pugazg/kalaignar-tribute#48` → `4156aa09…`) |
| **R2-C** | **COMPLETE / REVIEWED / MERGED** (`#104` → `597e65fd…`) |
| **R2 implementation** | **COMPLETE / PRODUCTION-ACCEPTED** |
| **R2 close-out (this record)** | **REVIEW-READY — awaiting independent exact-head review** |
| **R3** | **NOT AUTHORIZED** |

**R3 is not authorized by the completion of R2.** R3 — the 249 CREATE works, the five canonical merges, and the
Sangatamil and 1958 `தேனலைகள்` witness relations recorded in the frozen resolved manifest (whose `futureR2Actions` mean
R3) — requires a separate explicit owner authorization after this close-out is independently reviewed and merged.
