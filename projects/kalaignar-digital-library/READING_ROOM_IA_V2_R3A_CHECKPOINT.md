# Reading Room IA v2 — R3-A Checkpoint (Identity and Relation Foundation)

**Recorded:** 2026-09-26.

**Status: R3 — OWNER-AUTHORIZED ("let's start R3"). R3 PLAN — COMPLETE / REVIEWED / FROZEN. R3-A IMPLEMENTATION —
COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED. R3-A CHECKPOINT — REVIEW-READY. R3-B, R3-C, R3-D — NOT STARTED.**

This is a **control-only lifecycle checkpoint**. It records an implementation stage that has already been independently
reviewed, merged and accepted on production.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

R3-A is the foundation stage and changes nothing public. Its production acceptance therefore proves **invariance**, not
just availability (§5).

**Authority:**
- The frozen R3 plan [`READING_ROOM_IA_V2_R3_PLAN.md`](./READING_ROOM_IA_V2_R3_PLAN.md): merged as
  `pugazg/kalaignar-tribute#50` → `bab2fd4d2008fc57f527b3627087f38755a16a64`, approved head `650ed021…`, 0 content
  delta.
  - The owner approved all three review decisions: Ina fragment identities; the 11 publications become publication
    records (final 568); stages A → B → C → D.
  - The merged plan file still reads "R3 PLAN — REVIEW-READY", its exact reviewed text. The merge supersedes it, and the
    file is not reopened.
- **R3 owner authorization:** "let's start R3".

---

## 1. Live pins (re-fetched 2026-09-26)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `bab2fd4d2008fc57f527b3627087f38755a16a64` (tree `a1c64f77be3896ce86751df989d7b5405667d8d9`) |
| Implementation `main` | `06731e0eaaa6f1228388add726204a2df694c649` (tree `5c2bf2c94b0ae567969e1bba7c47643670f00b5d`); 0 open implementation PRs |
| Production | Vercel deployment `6677444493` at `06731e0e…` |
| Source heads (unchanged) | poems `188d49cd` · literary-commentary `e23548b0` · essays `63019a4d` · short-stories `7205a108` |

## 2. Merge record — implementation PR #105

- **Title:** "Reading Room IA v2 R3-A: identity and relation foundation (no public change)".
- **Review:** independent exact-head review — **PASS**. The PR was merged by a normal merge commit, pinned to the
  approved head.

| Item | Value |
|---|---|
| Reviewed base | `597e65fde3266baffda98351de716507368b5ebc` (the merged R2-C) |
| Approved head | `be1d6d4f8135fc73e5bf09c350269711639269ff` (tree `5c2bf2c9…`) |
| Commits | exactly 2 (`70a521e6`, `be1d6d4f`); not squashed, rebased or amended |
| Changed files | 13, +35,730 / −0 |
| Exact-head CI | `Library CI` run `36232814181` — `typecheck • build` SUCCESS, `archival validators` SUCCESS; Vercel Preview success |
| Merge commit | `06731e0eaaa6f1228388add726204a2df694c649`, merged 2026-09-26T09:54:34Z |
| Merge tree | `5c2bf2c94b0ae567969e1bba7c47643670f00b5d` (= approved-head tree) |
| First parent | `597e65fde3266baffda98351de716507368b5ebc` |
| Second parent | `be1d6d4f8135fc73e5bf09c350269711639269ff` |
| Approved head → merge | **0 changed files** |
| Base → merge | exactly `70a521e6`, `be1d6d4f` and the merge `06731e0e`, over the same 13 files |
| PR state | MERGED / CLOSED |

**The 13 files:**
- `.github/workflows/library-ci.yml`;
- in `data/internal/r3/`: `READING_ROOM_IA_V2_RESOLVED_MANIFEST.frozen.json`, `identity-manifest.json`,
  `pre-r3-boundary.json`, `relations.json`;
- `data/library.ts`, `data/poems.ts`;
- `lib/collection-members.ts`, `lib/read-ia-r3-contribution.ts`, `lib/work-relations.ts`;
- `package.json`;
- `scripts/build-r3-identity.ts`, `scripts/test-r3-identity.ts`.

## 3. Merge CI and deployment

- **Merge CI:** `Library CI` run `36234184588` on `06731e0e…` — **COMPLETED / SUCCESS**. `typecheck • build` SUCCESS;
  `archival validators` SUCCESS.
- **Deployment (recorded as found):** the Vercel commit status is success.
  - GitHub deployment `6677444493` was created by `vercel[bot]` at 2026-09-26T10:00:10Z, environment `Production`,
    state success.
  - It is the existing automatic deploy of `main`. No manual deployment was made.

## 4. What R3-A delivered (foundation only)

- **The frozen resolved manifest, vendored byte-for-byte:** git blob **`b7b3530d54ba9c354b43313eecd69e78e76a92b5`**. It
  is a read-only generator input and is never edited.
- **The frozen pre-R3 boundary** (`pre-r3-boundary.json`, sha256 `d2975f49…`): the live R2 state at `597e65fd`, recorded
  once and pinned.
  - 335 LibraryWork records (digest `ed5611bc…`).
  - 9 collections (`08799c11…`).
  - Discovery entries.
  - The 5271-path sitemap set (sha256 `c65c6377…`).
  - Build 5280 / 5275.
- **The deterministic generator** `scripts/build-r3-identity.ts`, with `--verify`.
  - It refuses to run on any manifest-blob or boundary-hash mismatch, and fails closed on any unmapped unit.
  - **`identity-manifest.json`:**
    - the census;
    - all 249 CREATE identities (Poetry cohort introduced in R3-B: 162; the rest in R3-C: 87);
    - the 3 Ina fragment locators;
    - the 11 publications' unit-role maps;
    - the stage state.
  - **`relations.json`:** the one relation registry.
  - A **generated** `POETRY_WITNESS_RELATIONS` view in `data/poems.ts`. Its literal is byte-identical; only markers were
    added.
- **Runtime layers:**
  - `lib/work-relations.ts`: derived `witnessesOf`, `canonicalFor`, `publicationAppearances`, `activeMergedWitness`.
  - An empty `LIBRARY_PUBLICATIONS`, with the `LibraryPublication` type (a former record verbatim, plus `kind` and
    `demotedIn`).
  - The **dormant** merged-witness collection resolver (`lib/collection-members.ts`); it is not rendered.
  - `lib/read-ia-r3-contribution.ts`: every term derived from the stage state.
- **Validator:** `scripts/test-r3-identity.ts` (`test:r3-identity`, plus a CI step), 746 checks. Five sabotages were
  each proven to fail it:
  - remove a relation;
  - duplicate a relation;
  - alter the manifest pin;
  - activate R3-B early;
  - publish a CREATE identity.

**Stage state on merged `main`:** `published = [R3-A]`.

| Item | Value |
|---|---|
| Manifest | 315 = CREATE 249 · KEEP_EXISTING 27 · ADD_WITNESS 19 · DO_NOT_PROMOTE 20 · HOLD 0 |
| CREATE ids | 249 unique; 0 live collisions |
| **Relation registry** | **49** = source-publication 22 · merged-witness 5 · Sangatamil 11 · 1958 11 |
| Relation stages | live-pre-R3 2 · R3-B 18 · R3-C 2 · R3-D 27 |
| **Active relations** | **exactly 2** (Anna, Thennan) |
| **Dormant relations** | **47** |
| Published CREATE identities | **0** |
| `LIBRARY_PUBLICATIONS` | **empty** |
| `READ_IA_R3_CONTRIBUTION` | **0** for works, shelves, collections, discovery, visible, build and sitemap |

## 5. Production acceptance — invariance (read-only, `nenjukkuneethi.org`, deployment `6677444493`)

- **Every sitemap page is unchanged.** All **5271** production sitemap URLs return 200. Each page's HTML, after removing
  only `<script>`/`<link>` tags and `/_next/static` asset paths, is **identical to the pre-R3 base build** of tree
  `da22e2f4`.
  - 5271 of 5271 are the same, with 0 differing and 0 missing.
  - This covers `/read`, all 9 category pages, all 9 collection pages, every publication, every reader and every
    `/source` page.
- **Catalogue and categories:**
  - 335 canonical works (1/1/162/14/11/10/117/15/4), with category pages byte-identical to R2.
  - `/read` is the same 9-category landing.
  - The 11 future-demotion publications are still canonical LibraryWorks, and no publication is demoted.
- **Relations.**
  - Only the Anna and Thennan witness links render.
    - Both Kavithaigal item pages link back.
    - Both standalone pages' payloads carry exactly their one relation id and link.
    - `gunanayagar-nehru` carries no Kavithaigal-19 link (dormant).
  - There is no new witness UI, no Sangatamil relation on `oruthalaik-kathal`, no 1958 relation on the Meesai pages, no
    merged-story notice, and no Ina `poem-6-N` anchor.
- **Collections.** 9, with membership and rendered pages unchanged. The five future merge sources are each still listed
  once as ordinary Fiction works on `/read/fiction`.
- **Sitemap and build.** The sitemap has **5271** URLs with set hash **`c65c6377…`**, unchanged. The build is **5280**
  prerender / **5275** HTML, enforced by the merge CI's `test:r3-identity`. No route was added, removed, redirected or
  repurposed. Invalid examples return 404.
- **Frozen boundary.** The catalogue records digest is still `ed5611bc…`, the collections are unchanged, and the R3
  public terms are all 0.

## 6. Lifecycle

| Stage | Status |
|---|---|
| R0 · R1 · owner adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED |
| R3 | OWNER-AUTHORIZED ("let's start R3") |
| R3 plan | COMPLETE / REVIEWED / FROZEN (`#50` → `bab2fd4d…`) |
| **R3-A implementation** | **COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (`pugazg/kalaignar-autobiography#105` → `06731e0e…`) |
| **R3-A checkpoint (this record)** | **REVIEW-READY** |
| **R3-B / R3-C / R3-D** | **NOT STARTED** |

**Next:** independent exact-head review and merge of this checkpoint. Only then **R3-B** (Poetry promotions:
+162 − 4 → 493), under the standing R3 authorization and its own exact-head review gate.
- R3-B switches the stage state to include `R3-B`.
- It generates the Poetry catalogue slice, moves the 4 Poetry-stage publications into `LIBRARY_PUBLICATIONS`, adds the
  Ina anchor ids, and activates the 18 R3-B relations.
