# Reading Room IA v2 — R2-A Checkpoint (Category Model + Nine Category Routes)

**Recorded:** 2026-09-26.

**Status: R2 PLAN — COMPLETE / REVIEWED / FROZEN. R2-A — COMPLETE / REVIEWED / MERGED. R2-B — NOT STARTED / NOT
AUTHORIZED. R2-C — NOT STARTED. R3 — NOT AUTHORIZED.**

This is a **control-only lifecycle checkpoint**. It records an implementation stage that has already been
independently reviewed and merged.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

Merging R2-A to implementation `main` triggered the existing Vercel Git integration, so production now serves R2-A
(§4). This record states that fact rather than claiming an unchanged production surface.

Authority: [`READING_ROOM_IA_V2_R2_PLAN.md`](./READING_ROOM_IA_V2_R2_PLAN.md) §17 (R2-A row) and §9 (Letters special
case).

---

## 1. Live pins (re-fetched 2026-09-26)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `811fdc214f5e290cca5d18b660a29d27b4d43b37` (tree `7a06fc28538f91e90b629df38ff0392359d164f4`) |
| Implementation `pugazg/kalaignar-autobiography` `main` | `19c0ee15a5a78d04852be2144a72a0328d307400` (tree `d899d04f6eebfdece3a215a1f62899c72b0af4df`) |
| Source repositories (unchanged) | poems `188d49cd` · literary-commentary `e23548b0` · essays `63019a4d` · short-stories `7205a108` |

## 2. Merge record — implementation PR #102

- **Title:** "Reading Room IA v2 R2-A: category model, nine /read category routes, Letters corpus".
- **Review:** independent exact-head review — **PASS**. The PR was merged by a normal merge commit, pinned to the approved head.

| Item | Value |
|---|---|
| Approved head | `1607b8923f6aa7f2640543c31326ded3d93ebcdc` (parent `87ec4ab39047ebe663e132ce78a823ac27942c94`) |
| Approved tree | `d899d04f6eebfdece3a215a1f62899c72b0af4df` |
| Commits | exactly 2 (`87ec4ab3`, `1607b892`); not squashed, rebased or amended |
| Changed files | 31, +724 / −27 |
| Merge commit | `19c0ee15a5a78d04852be2144a72a0328d307400`, merged 2026-09-26T02:06:24Z |
| Merge tree | `d899d04f6eebfdece3a215a1f62899c72b0af4df` (= approved tree) |
| First parent | `f991043c3353abe9f2b334f7c8d57e433184d126` (previous implementation `main`) |
| Second parent | `1607b8923f6aa7f2640543c31326ded3d93ebcdc` (approved head) |
| Approved head → merge | **0 changed files** |
| PR state | MERGED / CLOSED |

## 3. CI at the merge commit

GitHub Actions `Library CI`, run `36210629536` (push, `main`, `19c0ee15…`): **COMPLETED / SUCCESS**.

| Job | Result |
|---|---|
| `typecheck • build` | SUCCESS |
| `archival validators` | SUCCESS |

At the approved head `1607b892…`, both jobs and the Vercel preview were also SUCCESS.

## 4. Deployment state (recorded as found)

- The Vercel commit status on `19c0ee15…` is **success** ("Deployment has completed").
- GitHub deployment `6673494910` was created by `vercel[bot]` on 2026-09-26T02:11:12Z.
  - It has **environment `Production`**, ref `19c0ee15…`, state success.
  - Its `production_environment` flag reads `false`. The previous Production deployment (`6638432286`, `f991043c…`)
    reports the same, so the flag is how this integration reports; the environment name is authoritative.
- **Production therefore auto-deployed R2-A.** The previous Production deployment was `6638432286` at `f991043c…`.
  - This was the repository's existing automatic deploy of `main`, not a manual deployment.
  - No manual deployment was performed or authorized.
- **Live production spot-check** of `https://nenjukkuneethi.org` on 2026-09-26:

  | Page | Result |
  |---|---|
  | `/read/autobiography`, `/read/letters`, `/read/fiction`, `/read/poetry`, `/read/drama`, `/read/cinema`, `/read/speeches`, `/read/essays`, `/read/literary-commentary` | 200 |
  | `/read/not-a-category` | 404 |
  | `/read/v1-ch01`, `/read/v6-ch01`, `/read/nenjukku-neethi`, `/murasoli`, `/murasoli/m42-l3364` | 200 |
  | `/read` | still the pre-R2 discovery landing: 9 shelf sections, 0 category cards, Daily Kural present, `life-writing` shown as `வாழ்க்கை எழுத்து` |
  | `/read/letters` | corpus summary (Volumes 42–54) and a `/murasoli` browse link are served |
  | `/sitemap.xml` | 5262 URLs, 0 category URLs |

## 5. What R2-A delivered

| Deliverable | File |
|---|---|
| Category registry — the single route registry: 9 `ShelfId`s → `/read/<slug>` plus metadata. It stores no membership; `worksInCategory()` derives from `publishedWorks()` | `data/read-categories.ts` |
| Shared category UI — every published work on the shelf, individually, in catalogue order, reusing `WorkCard`, with a link back to `/read` | `components/LibraryCategoryPage.tsx` |
| Letters corpus treatment | `components/LettersCorpusSummary.tsx`, `lib/murasoli-corpus.ts` |
| Nine thin static routes | `app/read/{autobiography,letters,fiction,poetry,drama,cinema,speeches,essays,literary-commentary}/page.tsx` |
| R2-A validator (`test:read-categories`, CI step) | `scripts/test-read-categories.ts` |
| Reuse exports only (`WorkCard`, `shelfIcon`); `/read` renders byte-identically | `components/LibraryHome.tsx` |

**Route map and counts**

| Shelf id | Route | Works |
|---|---|---:|
| `life-writing` | `/read/autobiography` | 1 |
| `letters` | `/read/letters` | 1 |
| `fiction` | `/read/fiction` | 162 |
| `poetry` | `/read/poetry` | 14 |
| `drama` | `/read/drama` | 11 |
| `cinema-writing` | `/read/cinema` | 10 |
| `speeches` | `/read/speeches` | 117 |
| `essays-articles` | `/read/essays` | 15 |
| `literary-commentary` | `/read/literary-commentary` | 4 |
| **Total** | | **335** |

- Route collisions with the 391 memoir chapter ids and with `nenjukku-neethi`: **0**.
- `/read/[id]` still prerenders exactly the 391 chapters, and unknown ids still fail closed.
- Every published LibraryWork appears on **exactly one** category page, checked against the rendered markup.
- Collection membership never suppresses a work: all 149 Fiction collection members and all 97 `முத்துக் குளியல்`
  speeches are listed individually.
- **Catalogue 335 · collections 9 · catalogue delta 0.**

## 6. Letters special case (frozen R0 §6.2; R2 plan §9)

- `/read/letters` has exactly **one** canonical LibraryWork, `murasoli-letters`.
- The corpus summary is derived at build time from `public/data/murasoli/index.json` (`volumeCount`, `volumes[].volume`)
  and `letters-index.json` (letter count, cross-checked per volume): **Volumes 42–54 · 13 volumes · 688 letters**.
- The "Browse by volume & sequence" link goes to `/murasoli`, which remains the detailed browser.
- No volume or individual letter became a LibraryWork. No volume route was invented. `/murasoli/<letter-id>` is
  unchanged, and the printed letter number is never the route identity.

## 7. Build and sitemap

| Measure | Before R2-A (`f991043c`) | After R2-A (`19c0ee15`) |
|---|---:|---:|
| Prerendered routes | 5271 | **5280** (+9) |
| HTML pages | 5266 | **5275** (+9) |
| Sitemap URLs | 5262 | **5262** (+0; category URLs 0) |

- The +9 are exactly the nine category routes; 0 routes were removed.
- **Build reconciliation** (owner-approved for R2-A):
  - 14 historical build-pinned validators add `READ_IA_R2_CONTRIBUTION.build`, which equals
    `READ_CATEGORY_ROUTES.length`. It is derived from the same registry, never typed as a constant.
  - The frozen pre-Wave-6 route remainders (`validate-wave6-p3-build`, `validate-wave6-p4-integration`) exclude those
    same routes, and their frozen route-set SHA-256 still matches.
  - Existing baseline terms and the Wave-6/7/8 contributions remain. No validator was removed, and no invariant was
    weakened.
  - `test:read-categories` proves that the term corresponds exactly to the nine built category pages, and that none of
    them is in the sitemap.
- **Sitemap:** `app/sitemap.ts` is unchanged. Sitemap integration (+9 → projected 5271) and the
  `lib/read-ia-r2-contribution.ts` sitemap reconciliation belong to **R2-C**.

## 8. Preservation proofs (blobs identical at `f991043c`, approved head `1607b892` and merge `19c0ee15`)

| File | Blob | Therefore |
|---|---|---|
| `app/read/page.tsx` | `76b2e52a63697303fe90d6ad4017f1f35eba6f30` | `/read` is still the pre-R2 discovery landing; Daily Kural remains; `revalidate = 900` remains |
| `data/library.ts` | `aea4d042189d9dc1ea578ec8086afb55ee602fa6` | catalogue 335; the shared `life-writing` Tamil label is still `வாழ்க்கை எழுத்து` (the `சுயசரிதை` switch is R2-B) |
| `data/collections.ts` | `b7e8f4cef1cd1a2e88cc4cd7f08a7d8234dcb430` | collection model and `discoveryShelves()` unchanged; 9 collections |
| `app/sitemap.ts` | `99f60752988355b164acd491953ff6b04ef2dbf6` | no category URL in the sitemap |
| `app/read/[id]/page.tsx` | `ee47680cb94324382ea92bf3c49ba106c1cbec8c` | the 391 memoir chapter routes are intact |
| `app/read/nenjukku-neethi/page.tsx` | `8412efabb9520e64f3a849b7ad05d3ca1983656f` | the memoir collection page is unchanged |

## 9. R3 boundary — delta 0

R2-A implements **none** of the following, all of which remain R3 (not authorized):
- any of the **249** resolved-manifest CREATE candidates. None of their 249 canonical ids exists as a LibraryWork, and
  the test pins a digest of the 335 published ids at the R2 base;
- `sirai-kodiyathu → green-parrot`;
- `neeyum-kaithi-naanum-kaithi → piraiye`;
- `aadik-kaatre → adikkaatru`;
- `pugazhe-nee-oru-pudhir → pugazh`;
- `sorgaththirku-vandhathu-eppadi → sorgga-logaththil`;
- Sangatamil witness relations;
- 1958 `தேனலைகள்` witness relations.

The five merge sources remain separate Fiction works, and none of the five targets exists.

## 10. Lifecycle

| Stage | Status |
|---|---|
| R0 | COMPLETE / REVIEWED / FROZEN |
| R1 | COMPLETE / REVIEWED / FROZEN |
| Owner HOLD adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 plan | **COMPLETE / REVIEWED / FROZEN** (`pugazg/kalaignar-tribute#46`, approved head `df99c0ea…`, merge `811fdc21…`, exact-head review PASS) |
| **R2-A** | **COMPLETE / REVIEWED / MERGED** (`pugazg/kalaignar-autobiography#102` → `19c0ee15…`) |
| **R2-B** | **NOT STARTED / NOT AUTHORIZED** |
| R2-C | NOT STARTED |
| R3 | NOT AUTHORIZED |

**R2-B is not authorized by the overall R2 plan.** It requires a separate next-stage authorization after this
checkpoint is independently reviewed and merged. R2-B's scope:
- the category-only `/read`;
- the `சுயசரிதை` label;
- removing Daily Kural from `/read`;
- re-scoping the 7 rendered-`/read` tests.

**Next:** independent review and merge of this control checkpoint, then a separate owner authorization for R2-B.
