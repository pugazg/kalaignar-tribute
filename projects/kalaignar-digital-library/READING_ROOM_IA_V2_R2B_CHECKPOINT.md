# Reading Room IA v2 — R2-B Checkpoint (Category-First `/read` Landing)

**Recorded:** 2026-09-26.

**Status: R2 PLAN — COMPLETE / REVIEWED / FROZEN. R2-A — COMPLETE / REVIEWED / MERGED. R2-B — COMPLETE / REVIEWED /
MERGED. R2-C — NOT STARTED / NOT AUTHORIZED. R3 — NOT AUTHORIZED.**

This is a **control-only lifecycle checkpoint**. It records an implementation stage that has already been
independently reviewed, merged and accepted on production.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

Merging R2-B to implementation `main` triggered the existing Vercel Git integration, and production now serves R2-B.
It was verified read-only (§4).

- **Authority:** [`READING_ROOM_IA_V2_R2_PLAN.md`](./READING_ROOM_IA_V2_R2_PLAN.md) §8 (landing contract), §11 (Daily
  Kural), §16 (acceptance tests), §17 (R2-B row).
- **Previous stage:** [`READING_ROOM_IA_V2_R2A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R2A_CHECKPOINT.md).
- **Owner authorization:** "Authorize R2-B and proceed with R2-B."

---

## 1. Live pins (re-fetched 2026-09-26)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `a9600327de2e9c786ee3ee25dbce8db6edb7ed98` (tree `0c04f956321de14c6291f55b40ff441c7ff53311`) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `89c682553d6ba07a96e966bb982d60ebe0cd8b47` (tree `cb70d85767739ed43d75d7db54ddaa6f41fdfdbe`); 0 open implementation PRs |
| Source repositories (unchanged) | poems `188d49cd` · literary-commentary `e23548b0` · essays `63019a4d` · short-stories `7205a108` |

## 2. Merge record — implementation PR #103

- **Title:** "Reading Room IA v2 R2-B: category-first /read landing".
- **Review:** independent exact-head review — **PASS**. The PR was merged by a normal merge commit, pinned to the
  approved head (`--match-head-commit`).

| Item | Value |
|---|---|
| Reviewed base | `19c0ee15a5a78d04852be2144a72a0328d307400` (the merged R2-A) |
| Approved head | `07dd8a7fdec4590014a39931cae0701c001b670c` (tree `cb70d85767739ed43d75d7db54ddaa6f41fdfdbe`) |
| Commits | exactly 1; not squashed, rebased or amended |
| Changed files | 13, +432 / −356 |
| Merge commit | `89c682553d6ba07a96e966bb982d60ebe0cd8b47`, merged 2026-09-26T02:50:06Z |
| Merge tree | `cb70d85767739ed43d75d7db54ddaa6f41fdfdbe` (= approved-head tree) |
| First parent | `19c0ee15a5a78d04852be2144a72a0328d307400` (reviewed old `main`) |
| Second parent | `07dd8a7fdec4590014a39931cae0701c001b670c` (approved head) |
| Approved head → merge | **0 changed files** |
| Base → merge | 2 commits (the approved head and the merge), the same 13 files; no extra commit |
| PR state | MERGED / CLOSED |

## 3. CI

| Commit | Library CI | `typecheck • build` | `archival validators` | Vercel |
|---|---|---|---|---|
| Approved head `07dd8a7f…` (pre-merge) | success | SUCCESS | SUCCESS | Preview success |
| Merge `89c68255…` (run `36212919374`, push to `main`) | COMPLETED / SUCCESS | SUCCESS | SUCCESS | success |

The build job at the merge includes the build-pinned validators: prerender **5280** and HTML **5275**, unchanged from R2-A.

## 4. Deployment and production acceptance (recorded as found; read-only)

- **Deployment:** the Vercel commit status on `89c68255…` is **success**. GitHub deployment `6673879019` was created by
  `vercel[bot]` on 2026-09-26T02:56:24Z, with environment `Production`.
  - This is the repository's existing automatic deploy of `main`. No manual deployment was performed.
  - The previous Production deployment was `6673494910` at `19c0ee15…` (R2-A).
- **Production acceptance** read `https://nenjukkuneethi.org` after the deploy: **0 failures**.

**`/read`**

| Check | Result |
|---|---|
| Status | 200 |
| Category cards | exactly **9** |
| Card links | exactly the nine R2-A routes in `SHELVES` order |
| Links in `<main>` | only those 9 |
| Work cards | **0** |
| Collection cards | **0** |
| `<details>` | **0** |
| Daily Kural | **absent** |
| First card | `சுயசரிதை` · Life Writing · 1 படைப்பு; the retired `வாழ்க்கை எழுத்து` appears nowhere |

**Card counts as served** (Tamil default):

| Card | Count |
|---|---|
| Life Writing | 1 படைப்பு |
| Letters | 1 படைப்பு |
| Fiction | **162 படைப்புகள் · 7 தொகுப்புகள்** |
| Poetry | 14 படைப்புகள் |
| Drama | 11 படைப்புகள் |
| Cinema Writing | 10 படைப்புகள் |
| Speeches | **117 படைப்புகள் · 2 தொகுப்புகள்** |
| Essays & Articles | 15 படைப்புகள் |
| Literary Commentary | 4 படைப்புகள் |

Only Fiction and Speeches carry a collection count.

**Other checks**
- All nine category routes return 200. The category pages list **335** works, 335 distinct.
- **`/read/letters`:**
  - its work grid holds exactly one canonical work (`/murasoli`);
  - the corpus figures read Volumes 42–54 · 13 volumes · 688 letters;
  - the browse link goes to `/murasoli`;
  - no individual letter is linked.
- **`/read/autobiography`** shows `சுயசரிதை`.
- **Existing routes:** 200 for `/read/nenjukku-neethi`, `/read/v1-ch01`, `/read/v6-ch01`, `/murasoli`,
  `/murasoli/m42-l3364`, `/murasoli/m48-l3706`, `/cinema/manohara`, `/plays/ore-mutham`, `/sangatamil`,
  `/poems/kaalap-pezhaiyum-kavithai-saaviyum`, `/thirukkural`, `/tholkappiyam` and `/kuraloviyam`, and for all 9
  `/collections/<id>`.
- **Invalid routes:** `/read/v9-ch99` and `/read/not-a-category` return 404.
- **`/sitemap.xml`:** **5262** URLs, 0 duplicates, **0 category URLs**.

## 5. What R2-B delivered

| Area | Change |
|---|---|
| `/read` landing (`components/LibraryHome.tsx`) | Exactly 9 category cards (`CategoryCard`), in `SHELVES` order, with routes from the R2-A registry `data/read-categories.ts`. Each card shows the shared Tamil label (`lang="ta"`), the English label, the shelf icon, the **canonical work count as the primary figure**, and the collection count as secondary metadata only where one exists. The discovery rendering (`DiscoveryCard`, `INITIAL_WORKS_PER_SHELF`, the shelf disclosures) was removed. `WorkCard`, `CollectionCard`, `shelfIcon` and `accentFor` are exported and visually unchanged. |
| Shared label (`data/library.ts`) | The `life-writing` public Tamil label is now **`சுயசரிதை`**, a one-line change. The shelf id, routes and works are unchanged. `/read` and `/read/autobiography` read it from this single source. |
| Daily Kural (`app/read/page.tsx`) | No longer imported or rendered on `/read`. `components/DailyKural.tsx`, `lib/daily-kural.ts` and `test:daily-kural` (still in CI) are retained. No new placement was made. |
| `revalidate = 900` | **Removed.** It existed only for the Daily Kural. Clean builds before and after: 5280 prerendered routes, 0 added, 0 removed. The only change is that `/read` became fully static (`initialRevalidateSeconds` 900 → `false`). |
| `/read` metadata | Describes the category-first library. |
| `data/read-categories.ts` | `collectionsInCategory()` (the secondary count, from `LIBRARY_COLLECTIONS`). |

## 6. Tests re-scoped (no weakening)

The seven rendered-`/read` test owners named by the plan were re-scoped. Their card assertions moved to the category
page that now renders them, and historical discovery arithmetic is kept as data-level invariants:

| Test | Re-scope |
|---|---|
| `test-shelf-disclosure` | Discovery model kept as data: 98 entries · 42 within the historical cap · 6 over-cap shelves. `/read` is proven to be the 9-card landing with no disclosure. Full delivery is proven on the rendered category pages (335, each once, in order, nothing hidden). |
| `test-collections` | Registry, membership and route tests are unchanged. `/read` has no collection or work card. Every member of all 7 Fiction and both Speeches collections is listed individually on its category page. |
| `test-standalone-poem-ui` | Card checks moved to `/read/poetry`. |
| `test-wave5-p4-cinema-ui` | Per-card semantics (EN and TA) moved to `/read/cinema`. |
| `test-wave8-p4-publication-ui` | Ore Mutham checks moved to `/read/drama`, Sangatamil to `/read/literary-commentary`, and Murasoli (one work card) to `/read/letters`. |
| `validate-wave6-p4-integration` | Discovery census kept as data. **New:** all 22 Wave-6 works are proven on their category pages. |
| `validate-wave5-p4-cinema-integrity` | A5 discovery arithmetic kept as data. **New:** `/read/cinema` lists all 10 Cinema works. |

- `test-wave5-p3-cinema-catalogue` changed one **comment only**.
- `test:read-categories` grew from 227 to 370 checks. It now also enforces:
  - the R2-B landing (EN and TA);
  - `சுயசரிதை` from the single shared source;
  - the Daily Kural and `revalidate` source contract;
  - `/read` prerendered static.

## 7. Invariance

| Measure | After R2-A | After R2-B |
|---|---:|---:|
| Published LibraryWorks | 335 | **335** |
| Shelf counts | 1/1/162/14/11/10/117/15/4 | unchanged |
| Collections | 9 | **9** |
| Prerendered routes / HTML | 5280 / 5275 | **5280 / 5275** (0 routes added or removed) |
| Sitemap URLs / category URLs | 5262 / 0 | **5262 / 0** |
| `READ_IA_R2_CONTRIBUTION.build` | 9 | **9** |
| `discoveryShelves()` (data model) | 98 entries / 42 within the historical cap | unchanged; no longer rendered |

Blobs at merge `89c68255…` that are unchanged from the R2-A state:

| File | Blob |
|---|---|
| `data/collections.ts` | `b7e8f4cef1cd1a2e88cc4cd7f08a7d8234dcb430` |
| `app/sitemap.ts` | `99f60752988355b164acd491953ff6b04ef2dbf6` |
| `app/read/[id]/page.tsx` | `ee47680cb94324382ea92bf3c49ba106c1cbec8c` |
| `app/read/nenjukku-neethi/page.tsx` | `8412efabb9520e64f3a849b7ad05d3ca1983656f` |

Intentionally changed by R2-B:

| File | Blob |
|---|---|
| `data/library.ts` | `d2d9922a50709e82b7f19761cf65d61e298c5b82` (the label line only) |
| `app/read/page.tsx` | `3bdd03694077d714cd87f2aecfdca24e5cb8c62a` |

## 8. R3 boundary — delta 0

R2-B implements none of the following, all of which remain R3 (not authorized):
- the **249** resolved-manifest CREATE candidates;
- the five canonical merges:
  - `sirai-kodiyathu → green-parrot`;
  - `neeyum-kaithi-naanum-kaithi → piraiye`;
  - `aadik-kaatre → adikkaatru`;
  - `pugazhe-nee-oru-pudhir → pugazh`;
  - `sorgaththirku-vandhathu-eppadi → sorgga-logaththil`;
- Sangatamil witness relations;
- 1958 `தேனலைகள்` witness relations.

`test:read-categories` still pins the digest of the 335 published ids at the R2 base, and it passes at the merge.

## 9. Lifecycle

| Stage | Status |
|---|---|
| R0 | COMPLETE / REVIEWED / FROZEN |
| R1 | COMPLETE / REVIEWED / FROZEN |
| Owner HOLD adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 plan | COMPLETE / REVIEWED / FROZEN (`pugazg/kalaignar-tribute#46` → `811fdc21…`) |
| R2-A | COMPLETE / REVIEWED / MERGED (`pugazg/kalaignar-autobiography#102` → `19c0ee15…`; checkpoint `pugazg/kalaignar-tribute#47` → `a9600327…`) |
| **R2-B** | **COMPLETE / REVIEWED / MERGED** (`pugazg/kalaignar-autobiography#103` → `89c68255…`; production accepted) |
| **R2-C** | **NOT STARTED / NOT AUTHORIZED** |
| R3 | NOT AUTHORIZED |

**R2-C is not authorized by the overall R2 plan.** It requires a separate owner authorization after this checkpoint is
independently reviewed and merged. Its scope (plan §17):
- secondary collection sections on the category pages;
- sitemap +9 (projected 5271);
- `lib/read-ia-r2-contribution.ts` sitemap reconciliation;
- full regression and implementation close-out.

**Next:** independent review and merge of this control checkpoint, then a separate owner authorization for R2-C.
