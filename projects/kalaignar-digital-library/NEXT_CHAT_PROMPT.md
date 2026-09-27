# New Chat Bootstrap Prompt — Kalaignar Digital Library / READING ROOM IA v2 R3 — PLAN FROZEN · R3-A–R3-D COMPLETE / MERGED / PRODUCTION-ACCEPTED · R3 IMPLEMENTATION COMPLETE · R3 CLOSE-OUT NOT YET FROZEN (R0, R1 and adjudication frozen; Waves 6, 7 and 8 closed at P5)

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub and production are authoritative. Do not trust copied SHAs, PR
bodies or this bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`, and inspect all open control PRs.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely**.
   - Its highest-precedence CURRENT checkpoint is **2026-09-27 — READING ROOM IA v2 R3 — R3-D COMPLETE / REVIEWED /
     MERGED / PRODUCTION-ACCEPTED · R3 IMPLEMENTATION COMPLETE · R3 CLOSE-OUT NOT YET FROZEN**.
   - Directly below it is the R3-C checkpoint (2026-09-27). It was merged as `#53` → `39ada6b2…`, which supersedes its
     "REVIEW-READY" wording; its "R3-D NOT STARTED" statements are historical.
   - Directly below it is the R3-B checkpoint (2026-09-27). It was merged as `#52` → `41f7e0cb…`, which supersedes its
     "REVIEW-READY" wording; its "R3-C NOT STARTED" statements are historical.
   - Directly below it is the R3-A checkpoint (2026-09-26). It was merged as `#51` → `c2a17f0a…`, which supersedes its
     "REVIEW-READY" wording; its "R3-B NOT STARTED" statements are historical.
   - Directly below it is the R3 planning checkpoint (2026-09-26). Its "planning in progress / implementation not
     started" statements are historical.
   - Below that is the R2 close-out checkpoint (2026-09-26). It was merged as `#49` → `c4c3ccd4…`, which
     supersedes its "REVIEW-READY" wording; its "R3 NOT AUTHORIZED" status is historical.
   - Below that is the R2-B checkpoint (2026-09-26). Its "R2-C NOT STARTED" and "sitemap 5262" statements are
     historical.
   - Below that is the R2-A checkpoint (2026-09-26). Its "R2-B NOT STARTED" and "`/read` still the old
     landing" statements are historical.
   - Below that is the R2 plan checkpoint (2026-09-25). Its "REVIEW-READY / R2 IMPLEMENTATION — NOT STARTED"
     status is historical.
   - Below that is the frozen owner-adjudication checkpoint (COMPLETE / REVIEWED / FROZEN). Its
     "R2 NOT STARTED / NOT AUTHORIZED" status is historical.
   - Directly below it is the frozen R1 checkpoint (**READING ROOM IA v2 R1 — IDENTITY RECONCILIATION COMPLETE /
     REVIEWED / FROZEN**). Its "34 HOLD items remain unresolved" status is historical.
   - Directly below it is the frozen R0 checkpoint (**READING ROOM IA v2 R0 — CLASSIFICATION CENSUS COMPLETE /
     REVIEWED / FROZEN**). Its "R1 NOT STARTED" status is historical.
   - Below that, **2026-09-24 — WAVE 8 P5 PRODUCTION ACCEPTANCE — PASS · WAVE 8 COMPLETE / CLOSED / FROZEN
     AT P5** remains the latest closed onboarding-wave checkpoint.
   - The Wave-8 P0 checkpoint below that is the historical selection authority. Its "P1 NOT STARTED" status is
     superseded.
3. Read `projects/kalaignar-digital-library/READING_ROOM_IA_V2_R0_CENSUS.md`, the R0 classification census for
   the owner-authorized Reading Room IA v2 initiative (control-only). It is frozen historical authority: merged in
   `pugazg/kalaignar-tribute#40` (normal merge `399319ea7995c24a06da6866babefe086751afe6`, approved head
   `200d00b2…`, 0 content delta). Verify this against live GitHub.
   - Then read `READING_ROOM_IA_V2_R1_IDENTITY_RECONCILIATION.md`, the R1 identity authority, with its machine-readable
     `READING_ROOM_IA_V2_R1_MANIFEST.json` and `READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json`.
   - R1 is frozen historical authority: merged in `pugazg/kalaignar-tribute#42` (normal merge
     `1d12bd6dbf262d570c3199b3eb6d681cef62f0dc`, approved head `531bec4f…`, 0 content delta; lifecycle close-out
     #43 → `62739aac…`). Verify this against
     live GitHub.
   - Then read `READING_ROOM_IA_V2_OWNER_HOLD_ADJUDICATION.md` and `READING_ROOM_IA_V2_RESOLVED_MANIFEST.json`, the
     owner decisions for all 34 R1 HOLD rows (an overlay; R1 unchanged). These are frozen historical authority:
     merged in `pugazg/kalaignar-tribute#44` (normal merge `cc131a26501e714664ec80c011522cf0155dccb0`, approved head
     `87d4294e…`, 0 content delta). Verify this against live GitHub.
   - Then read `READING_ROOM_IA_V2_R2_PLAN.md`, the R2 plan (category-first `/read` over the existing 335 works). It
     is COMPLETE / REVIEWED / FROZEN: merged in `pugazg/kalaignar-tribute#46` (normal merge
     `811fdc214f5e290cca5d18b660a29d27b4d43b37`, approved head `df99c0ea…`, 0 content delta). Never edit §§1–20.
   - Then read `READING_ROOM_IA_V2_R2A_CHECKPOINT.md`, the R2-A lifecycle record (implementation
     `pugazg/kalaignar-autobiography#102` → `19c0ee15…`; merged as control `pugazg/kalaignar-tribute#47` →
     `a9600327…`).
   - Then read `READING_ROOM_IA_V2_R2B_CHECKPOINT.md`, the R2-B lifecycle and production-acceptance record
     (implementation `pugazg/kalaignar-autobiography#103` → `89c68255…`; merged as control `pugazg/kalaignar-tribute#48`
     → `4156aa09…`).
   - Then read `READING_ROOM_IA_V2_R2_CLOSEOUT.md`, the final R2 record: R2-C (`#104` → `597e65fd…`), production
     acceptance and the final arithmetic. It was merged as control `pugazg/kalaignar-tribute#49` → `c4c3ccd4…`.
   - Then read `READING_ROOM_IA_V2_R3_PLAN.md`, the R3 plan (owner: "let's start R3"). It is COMPLETE / REVIEWED /
     FROZEN, merged as `pugazg/kalaignar-tribute#50` → `bab2fd4d…`. Its file keeps the reviewed "REVIEW-READY" wording,
     which the merge supersedes. Never edit it.
   - Then read `READING_ROOM_IA_V2_R3A_CHECKPOINT.md`, the R3-A record (implementation `#105` → `06731e0e…`, production
     invariance). It was merged as control `pugazg/kalaignar-tribute#51` → `c2a17f0a…`.
   - Then read `READING_ROOM_IA_V2_R3B_CHECKPOINT.md`, the R3-B record (implementation `#106` → `109e4bfd…`, Poetry
     promotions, production acceptance). It was merged as control `pugazg/kalaignar-tribute#52` → `41f7e0cb…`.
   - Then read `READING_ROOM_IA_V2_R3C_CHECKPOINT.md`, the R3-C record (implementation `#107` → `afef75f9…`, Essays /
     Letters / Speech promotions, production acceptance). It was merged as control `pugazg/kalaignar-tribute#53` →
     `39ada6b2…`.
   - Then read `READING_ROOM_IA_V2_R3D_CHECKPOINT.md`, the R3-D record (implementation `#108` → `7fe9a4f0…`, merges,
     Sangatamil, 1958, final production acceptance). Check whether its control PR has been independently reviewed and
     merged.
4. Read `projects/kalaignar-digital-library/WAVE8_P5_PRODUCTION_ACCEPTANCE.md`, the durable Wave-8 acceptance and
   close-out record.
5. Read `projects/kalaignar-digital-library/WAVE8_COMPLETED_WORKS_CENSUS.md` as the **historical P0 selection and
   readiness authority**.
   - It was frozen by control PR `pugazg/kalaignar-tribute#37`, merge `cc99ebb6a2c35130a6b42ac2051f7907fbc9129c`.
   - Its "P1 NOT STARTED / NOT AUTHORIZED" banner and its 333 → 335 projection are historical. The P5 record
     supersedes the banner as current state and confirms the projection as realized.
   - Never edit it.
6. Read the prior closure records as history:
   - `WAVE7_P5_PRODUCTION_ACCEPTANCE.md` and `WAVE7_COMPLETED_WORKS_CENSUS.md`;
   - `WAVE6_P5_PRODUCTION_ACCEPTANCE.md`.
7. Fetch live `pugazg/kalaignar-autobiography` `main`, and inspect all open implementation PRs.
8. Treat live GitHub and production as authoritative. Any newer legitimate live state supersedes this bootstrap.

## CURRENT state

**Reading Room IA v2 — R3 (owner-authorized: "let's start R3"; canonical-work promotion and catalogue reconciliation).**
- **Lifecycle:** R3 OWNER-AUTHORIZED · **R3 PLAN — COMPLETE / REVIEWED / FROZEN** (#50 → `bab2fd4d…`) · **R3-A —
  COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (implementation #105 → `06731e0e…`) · R3-A checkpoint —
  COMPLETE / REVIEWED / MERGED (#51 → `c2a17f0a…`) · **R3-B — COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED**
  (implementation #106 → `109e4bfd…`) · R3-B checkpoint — COMPLETE / REVIEWED / MERGED (#52 → `41f7e0cb…`) · **R3-C —
  COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (implementation #107 → `afef75f9…`) · R3-C checkpoint —
  COMPLETE / REVIEWED / MERGED (#53 → `39ada6b2…`) · **R3-D — COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED**
  (implementation #108 → `7fe9a4f0…`) · R3-D checkpoint — REVIEW-READY · **R3 IMPLEMENTATION — COMPLETE** · **R3 CLOSE-OUT
  — NOT YET FROZEN**.
- **Input:** the frozen resolved manifest (`b7b3530d…`), vendored byte-for-byte in the implementation at
  `data/internal/r3/`: 315 = CREATE 249 · KEEP 27 · WITNESS 19 · DO_NOT_PROMOTE 20 · HOLD 0. It is never edited, and
  its `futureR2Actions` field means R3.
- **Frozen plan decisions (owner-approved):**
  - 246 promotions reuse existing child routes; the 3 `இன முழக்கம்` poems get fragment identities (`#poem-6-N`).
  - The 11 fully decomposed publications become publication records (not canonical works; every URL kept).
  - **Final 568 canonical works** (1/3/157/173/11/10/118/91/4); collections 9; build and sitemap +0.
- **R3-A foundation (live, no public change):**
  - Generator `scripts/build-r3-identity.ts` (`--verify`) produces `identity-manifest.json` (249 identities, 0
    published) and the one relation registry `relations.json`: 49 records (22 / 5 / 11 / 11), **2 active (Anna,
    Thennan), 47 dormant**.
  - The pre-R3 boundary is frozen (`pre-r3-boundary.json`: catalogue 335, collections 9, sitemap 5271 set hash
    `c65c6377…`, build 5280 / 5275).
  - `LIBRARY_PUBLICATIONS` is empty; the merged-witness resolver is dormant; `READ_IA_R3_CONTRIBUTION` is all 0.
  - **The stage switch** is `PUBLISHED_STAGES` in the generator.
- **R3-B (live; implementation `main` `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb`, tree `b65c5417…`):**
  - Stage state `[R3-A, R3-B]`: **162** identities are canonical works (Kaalap 57 · Kavithaigal 74 · 1975 3 · Ina 3 ·
    Meesai 25), generated into `data/r3-catalogue.ts` at their existing routes; 87 remain dormant.
  - **Catalogue 493** (1/1/162/173/11/10/117/14/4); `READ_IA_R3_CONTRIBUTION` works +158, Poetry +159, Essays −1,
    collections / build / sitemap 0.
  - **`LIBRARY_PUBLICATIONS` = 4** (Kaalap, Kavithaigal, 1975, Meesai; former records verbatim minus `state`), shown in
    a Publications section on their category pages; every route kept.
  - Ina `#poem-6-4/7/8` canonical; anchors `poem-6-1` … `poem-6-11`.
  - **Relations: 20 active / 29 dormant** (R3-C 2 · R3-D 27). The five `merged-witness` records are dormant, R3-D.
  - Collections 9 (unchanged) · sitemap 5271 (`c65c6377…`, unchanged) · build 5280 / 5275.
  - Validator reconciliation pattern: counts add the derived R3 terms; record / membership checks use
    `lib/read-ia-r3-projection.ts` (pre-R3 projection); `test:r3-identity` (823 checks) pins the projected delta.
- **R3-C (live; implementation `main` `afef75f9eca8367c2905c0d080f5c1fd82729b04`, tree `6c4ad32a…`):**
  - Stage state `[R3-A, R3-B, R3-C]`: **all 249** identities are canonical works, each once on its frozen shelf and
    subtype; **0** dormant. R3-C added 87 (Essays 84 · Letters 2 · Speech 1) at their existing essay-unit routes, each
    inheriting its parent's source pin and metadata exactly.
  - **Catalogue 573** (1/3/162/173/11/10/118/91/4); `READ_IA_R3_CONTRIBUTION` works +238, Poetry +159, Essays +76,
    Letters +2, Speeches +1, collections / build / sitemap 0.
  - **`LIBRARY_PUBLICATIONS` = 11** (Poetry 3, Essays 8), each its former record verbatim minus `state`.
  - **Letters:** `murasoli-letters` + exactly the two OD8 Letters at their Sinthanaiyum routes (validators:
    `R3_OD8_LETTERS` / `isOd8Letter`). **Speech:** `thudikkum-ilamai-urai` at its existing article route.
  - **Relations: 22 active / 27 dormant** (all R3-D). `idhaya-perikai` (a Speech) shows its two section witnesses via
    `SpeechReader`'s optional `witnessLinks`.
  - The five merge sources remain canonical Fiction works; every merge target (incl. `sorgga-logaththil`) is canonical.
  - Collections 9 (unchanged) · sitemap 5271 (`c65c6377…`, unchanged) · build 5280 / 5275. `test:r3-identity` 1130 checks.
- **R3-D — final (live; implementation `main` `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853`, tree `cd1f1367…`):**
  - Stage state `[R3-A, R3-B, R3-C, R3-D]`. **Catalogue 568** (1/3/157/173/11/10/118/91/4) = frozen plan §6.5;
    `READ_IA_R3_CONTRIBUTION` works +233, Fiction −5, Poetry +159, Essays +76, Letters +2, Speeches +1, all else 0.
  - **Five merges** (legacy story → canonical): `neeyum-kaithi-naanum-kaithi` → `piraiye`, `sorgaththirku-vandhathu-eppadi`
    → `sorgga-logaththil`, `aadik-kaatre` → `adikkaatru`, `sirai-kodiyathu` → `green-parrot`, `pugazhe-nee-oru-pudhir` →
    `pugazh`. Legacy records live only in their active `merged-witness` relations (`R3_MERGED_WITNESSES` excludes them
    from `LIBRARY_WORKS`); story routes / `/source` / payloads preserved; `collectionMemberWorks()` resolves through
    `lib/collection-members.ts`; `LIBRARY_COLLECTIONS` untouched (2004 anthology 34 entries, ordinals kept).
  - **Relations 49 / 49 active / 0 dormant.** Sangatamil is canonical-side only (`CANONICAL_SIDE_ONLY` in
    `lib/witness.ts`; Sangatamil pages pinned unchanged). 1958 தேனலைகள்: 10 chapter + 1 publication-level notes, அலை 3
    unmapped; the Meesai landing's OD6 note is derived (`publicationRelationNote`).
  - Validators admit the five merges narrowly (`R3_MERGED_LEGACY` / `mergedLegacyRecord` in
    `lib/read-ia-r3-projection.ts`). `test:r3-identity` 1001 checks.
  - Collections 9 · publications 11 · sitemap 5271 (`c65c6377…`, unchanged) · build 5280 / 5275 · source delta 0.
- **Next:** independent exact-head review and merge of the R3-D checkpoint. **No R4, new wave or maintenance** is
  authorized; R3 is not declared closed until that checkpoint merges.
- **CI note:** `Library CI`'s build step intermittently fails inside `next/font` (`Failed to find font override values for
  font Newsreader`; `TypeError … loader.js:112`) when Google Fonts misbehaves for the runner. It is environmental: re-run
  the failed job on the same commit, and record the attempt.

**Reading Room IA v2 — R2 (owner-authorized; category-first information architecture).**
- **Lifecycle:**
  - R0 — COMPLETE / REVIEWED / FROZEN.
  - R1 — COMPLETE / REVIEWED / FROZEN.
  - Owner HOLD adjudication — COMPLETE / REVIEWED / FROZEN.
  - **R2 PLAN — COMPLETE / REVIEWED / FROZEN** (#46 → `811fdc21…`).
  - **R2-A — COMPLETE / REVIEWED / MERGED** (implementation #102 → `19c0ee15…`).
  - **R2-B — COMPLETE / REVIEWED / MERGED** (implementation #103 → `89c68255…`).
  - **R2-C — COMPLETE / REVIEWED / MERGED** (implementation #104 → `597e65fd…`; owner: "Authorize R2-C and proceed
    with R2-C.").
  - **R2 IMPLEMENTATION — COMPLETE / PRODUCTION-ACCEPTED.**
  - **R2 close-out — MERGED** (`pugazg/kalaignar-tribute#49` → `c4c3ccd4…`).
  - **R3 — OWNER-AUTHORIZED** (see the R3 block above for its current stage).
- **Durable R2 facts (implementation `main` `597e65fde3266baffda98351de716507368b5ebc`, tree `da22e2f4…`):**
  - **`/read` is the category-first landing:** exactly **9 category cards** linking the nine category routes.
    - It shows no work card, collection card, disclosure or Daily Kural.
    - The work count is primary; collections are secondary, only for Fiction (162 · 7) and Speeches (117 · 2).
  - **9 category routes:** `/read/autobiography`, `/read/letters`, `/read/fiction`, `/read/poetry`, `/read/drama`,
    `/read/cinema`, `/read/speeches`, `/read/essays`, `/read/literary-commentary`. They collide with 0 of the 391
    memoir chapter ids.
    - They are built from `data/read-categories.ts`, `components/LibraryCategoryPage.tsx` and
      `components/LibraryHome.tsx` (`CategoryCard`).
    - The validator is `scripts/test-read-categories.ts` (`test:read-categories`, 440 checks).
  - **Category pages** list every canonical work individually, then a secondary bilingual **தொகுப்புகள் /
    Collections** section (existing `CollectionCard`) only where the shelf has collections: Fiction 7, Speeches 2.
  - **The shared `life-writing` Tamil label is `சுயசரிதை`.**
  - **Daily Kural is no longer on `/read`** (the component, its logic and its test are retained); `/read` is fully
    static.
  - **Catalogue 335** (1 / 1 / 162 / 14 / 11 / 10 / 117 / 15 / 4), with each work on exactly one category page.
    **Collections 9.**
    - `discoveryShelves()` is kept unchanged as a data model (98 / 42) and is not rendered.
  - **Letters:** one canonical work, `murasoli-letters`, plus 13-volume / 688-letter corpus navigation (Volumes
    42–54), linking to `/murasoli`. No letter or volume is a LibraryWork.
  - **Sitemap 5271** (= pre-R2 5262 + the 9 category URLs, 0 duplicates).
    - The pre-R2 set is preserved exactly (sha256 `5e017f02…`, pinned in `test:read-categories`).
    - The build is prerender 5280 / HTML 5275.
  - **`lib/read-ia-r2-contribution.ts`** is the single derived R2 contribution (`build` = `sitemap` =
    `READ_CATEGORY_ROUTES.length` = 9). Historical build/sitemap validators add it as an explicit term.
  - Every implementation merge to `main` auto-deploys to Production via the Vercel Git integration. The final R2
    deployment is `6674301852`. No manual deployment has been made.
- **R2 / R3 boundary:** R2 does not create the 249 CREATE works or perform the 5 canonical merges. R3 delta = 0.
  Where frozen records say "future R2" merge actions, they mean R3.
- R2 is complete. The next activity is the R3 block above.

**Reading Room IA v2 — owner HOLD adjudication (frozen authority; post-R1 overlay; control-only).**
- **READING ROOM IA v2 OWNER HOLD ADJUDICATION — COMPLETE / REVIEWED / FROZEN (2026-09-25; merged via PR #44,
  `cc131a26…`).** At freeze R2 was not yet authorized; see the R2 block above.
- Records: `READING_ROOM_IA_V2_OWNER_HOLD_ADJUDICATION.md` and `READING_ROOM_IA_V2_RESOLVED_MANIFEST.json` (the frozen
  R1 315 rows copied verbatim, plus an owner overlay). R1 is not reopened.
- All 34 original HOLD rows have owner decisions (OD1–OD9), so the **resolved HOLD = 0**. Resolved totals:
  CREATE 249 · KEEP_EXISTING 27 · ADD_WITNESS 19 · DO_NOT_PROMOTE 20.
- **Projection:** raw add-only `335 + 249 = 584`. Five existing Fiction works (`sirai-kodiyathu`,
  `neeyum-kaithi-naanum-kaithi`, `aadik-kaatre`, `pugazhe-nee-oru-pudhir`, `sorgaththirku-vandhathu-eppadi`) are future
  R2 merge/witness targets, giving a **provisional** net of 579. That figure is not the final website count.
- All 34 owner decisions are closed and frozen. Reopen only for a genuine source-backed defect or an explicit later
  owner correction.
- The owner has since authorized R2 (see the R2 block above). The adjudication's "future R2" merge actions are R3 under
  the R2 plan.

**Reading Room IA v2 — R1 (frozen authority; canonical identity + cross-witness reconciliation; control-only).**
- **READING ROOM IA v2 R1 — COMPLETE / REVIEWED / FROZEN (2026-09-24; merged via PR #42, `1d12bd6d…`).** R2 was not
  yet authorized at R1 freeze; see the R2 block above.
- R1 is control-only: implementation delta 0, source delta 0, production mutation 0, and no LibraryWork created.
- **Results:** 315 manifest entries.

| Workstream | Result |
|---|---|
| Poetry (148) | CREATE 132 · ADD_WITNESS 5 · KEEP 8 · HOLD 3 |
| Essays (104) | CREATE 79 · ADD_WITNESS 3 · DO_NOT_PROMOTE 19 · HOLD 3 |
| `ina-muzhakkam` | CREATE 7 · ADD_WITNESS 6 · HOLD 3 |
| Meesai (26) | ADD_WITNESS 1 · HOLD 25 |

- **Projection (not implemented):** `335 + 218 = 553` floor. `553 + 34 = 587` is a raw upper bound only (every
  remaining HOLD resolving as a new work) and is not a frozen count. Poetry would become 149 and Essays 98.
- **34 HOLD items** have explicit owner questions (R1 §11):
  - the canonical poem `green-parrot` (Kavithaigal 56 + Meesai 14, settled as one poem) ↔ the Fiction work
    `சிறை கொடியது`, and its shelf;
  - cross-shelf Meesai 1/2/13 and ina 2 ↔ 2004-anthology Fiction works;
  - the 1958 `தேனலைகள்` (untranscribed; SOURCE_LIMITED);
  - the prose-poem shelf;
  - Kaalap 37 ↔ ஒருதலைக் காதல் §1;
  - Kavithaigal 52 ↔ ina 6.5/6.6;
  - letter-form and speech-form units in essay books.
- At R1 freeze, 34 owner HOLD decisions were open. They are now decided in the owner-adjudication overlay above, and
  the frozen R1 record itself is unchanged.

**Reading Room IA v2 — R0 (frozen authority).**
- **READING ROOM IA v2 R0 — CLASSIFICATION CENSUS COMPLETE / REVIEWED / FROZEN (2026-09-24; merged via PR #40,
  `399319ea…`).**
- R0 is control-only: implementation delta 0, source delta 0, production mutation 0. Its record is
  [`READING_ROOM_IA_V2_R0_CENSUS.md`](./READING_ROOM_IA_V2_R0_CENSUS.md).
- **Direction (recorded, not implemented):** `Reading Room → Category → Individual canonical work → reading
  units`.
  - Collections and publications become secondary provenance / edition views and must not substitute for
    member works.
  - Existing URLs and citation identities are preserved (additive category routes plus redirects or aliases).
  - The proposed public Tamil label for `life-writing` is `சுயசரிதை` (the internal id is unchanged).
- **Today:** `discoveryShelves()` hides **246** collection-member works from `/read` (Fiction 149 + Speeches 97)
  behind **9** collection cards: `335 − 246 + 9 = 98` discovery entries, 42 visible. Those works remain published
  canonical LibraryWorks.
- **Classification:**
  - Poetry promotion candidates: Kaalap 58, Kavithaigal 77, 1975 items 01/02/04 (cross-witness de-duplication
    first).
  - Essays promotion candidates: 9 titled-unit containers.
  - Mixed: `ina-muzhakkam`.
  - Genre undecided: `meesai-mulaiththa-vayathil`.
  - Kept as one work: `oruthalaik-kathal`, `pesum-kalai-valarppom`, `1971-namathu-vilakkam`, `udhaya-kathir`,
    `nenjukku-neethi`, `murasoli-letters`.
  - Cinema song identity is deferred.
  - No post-migration Poetry or Essays count is frozen.
- R0 was consumed by R1 without reopening.

**Wave 8 status (latest closed onboarding wave).**
- **WAVE 8 P5 PRODUCTION ACCEPTANCE — PASS (2026-09-24). WAVE 8 COMPLETE / CLOSED / FROZEN AT P5. There is no
  Wave-8 P6.**
- P0–P5 are complete and frozen:
  - P1 #97 (+ #98 correction), P2 #99, P3 #100, P4 #101;
  - P5 is control-only: implementation delta 0, source delta 0, production mutation 0.

**Accepted implementation boundary:** `pugazg/kalaignar-autobiography` `main`
**`f991043c3353abe9f2b334f7c8d57e433184d126`**, tree **`87ca371b084c337ba2163caa6c336615174074e9`** (merge of
PR #101, approved head `42cfdf79fe001cd7588d7c30a6b1a193e0233703`). Production is `https://nenjukkuneethi.org`,
served by Vercel Production deployment `6638432286` for that commit.

**Wave-8 population.** 8 source publication inputs produced only **+2 canonical LibraryWorks**:
- Murasoli Vols 42–47 are a coverage expansion of the **existing** `murasoli-letters` work (342 letters; +0 works);
- `ore-mutham` is +1 Drama work;
- `sangatamil` is +1 Literary Commentary work.

**Final public surface:**

| Measure | Value |
|---|---|
| Catalogue | **335** — Life Writing 1 · Letters 1 · Fiction 162 · Poetry 14 · Drama **11** · Cinema Writing 10 · Speeches 117 · Essays & Articles 15 · Literary Commentary **4** |
| Collections | **9** |
| `/read` | discovery **98** / visible **42** |
| Sitemap | **5262 / 0 dup** |
| Build | **5271** prerender / **5266** HTML / **5274** generated static pages |
| Wave-8 route delta | **483** (Murasoli 342 · Ore Mutham 35 · Sangatamil 106) — created at P3, published at P4, 0 build routes added at P4 |

**Murasoli.**
- **Volumes 42–54 · 688 letters (342 + 346) · 5141 physical pages (2409 + 2732)**, one published sequence;
  `m47-l3705 ↔ m48-l3706`.
- The route id is identity; the printed number is not.
- Preserved anomalies:
  - 3154 sits between 3376 and 3378, with no 3377;
  - Vol 46 has two distinct 3637 records;
  - there is no 3636 and no 3644–3646;
  - 3647–3649 appear in both Vols 46 and 47.

**Accepted permanent source conditions** (not pending work; never reconstruct):
- Murasoli **3681** is source-incomplete: printed p. 252 is absent and the notice is shown.
- Sangatamil **scan 8** is a handwritten foreword that is permanently source-limited. Coverage is Tamil partial /
  English partial.

**Ore Mutham:** main scenes 1–30, then the separate `நகைச் சுவைப் பகுதி.` with scenes 1–3 numbered afresh (never
31–33).

**Sangatamil:** reader structure `commentary-unit`; 104 reading sections = front matter + **102 literary sections**
+ back matter.

**Frozen Wave-8 source pins** (never repin):
- `kalaignar-murasoli-letters` `bd0bb7904c85bdbfe05aa4970ac098d701a6967f`. Its source `main` has moved (Vol-41
  work); that is expected and does not reopen Wave 8.
- `kalaignar-stage-plays` `521fe5452e3e9ed54baa81e672325ce6ba501c5e`.
- `kalaignar-literary-commentary` `e23548b09547a2308407e60e5e67c1a03fee5354`.

**Wave 7 and Wave 6.**
- **Wave 7: COMPLETE / CLOSED / FROZEN AT P5 (2026-09-23).** Population 117; its accepted boundary `cf769d06…` /
  tree `35d64fb9…` is now historical.
- **Wave 6: COMPLETE / CLOSED / FROZEN AT P5.** Wave 5 is complete and closed.

## Route arithmetic (durable)

```
R2-C   : sitemap +9 category URLs (no page added)
         5262 + 9 = 5271 (sitemap) ; 5280 (prerender) ; 5275 (html)
R2-B   : /read landing only — 0 routes added or removed
         5262 (sitemap) ; 5280 (prerender) ; 5275 (html)
R2-A   : 9 static category pages (build only; sitemap unchanged)
         5262 (sitemap) ; 5271 + 9 = 5280 (prerender) ; 5266 + 9 = 5275 (html)
Wave 8 : Murasoli 342 + Ore Mutham 35 + Sangatamil 106 = 483
         4779 + 483 = 5262 (sitemap) ; 4788 + 483 = 5271 (prerender) ; 4783 + 483 = 5266 (html) ; 4791 + 483 = 5274 (static pages)
Wave 7 : B1 133 + B2–B4 225 + B5/B6/K 512 = 870
         3909 + 870 = 4779 (sitemap) ; 3918 + 870 = 4788 (prerender) ; 3913 + 870 = 4783 (html)
Wave 6 : Batches 1–6 321 + Batch-7 stories 232 + Batch-7 collections 5 = 558
         3351 + 558 = 3909 (sitemap) ; 3360 + 558 = 3918 (prerender) ; 3355 + 558 = 3913 (html)
```

## Durable semantic facts (do not regress)

- Wave 7:
  - `nachuk-koppai` has one terminal source-condition hold at scan 22 / Scene 5.
  - `kuraloviyam` has scans 13, 14, 15 and 19 permanently source-limited.
  - 45 Wave-7 speeches carry honestly labelled condensed English.
- Wave 6:
  - Plural collection membership is live (`jaadi-kutti-poduma`, `kuruvi-rameswaram`, the eleven 1977/2009
    canonicals).
  - `நந்தியூர் நரியப்பன்` and `நரியூர் நந்தியப்பன்` are distinct works.
- Public provenance pages serialize allowlisted projections only. No internal workflow state is published.

## Outside the closed waves (not decided; not pending work)

- `chinna-chinna-malargal` / Quotes (no Quotes shelf).
- Murasoli Vol 1 and Vol 41.
- The Wave-7 P0 NOT_COMPLETE items not taken up by Wave 8 (`payumpuli-pandaraka-vanniyan`, Audio-06, the 2007
  assembly Part-1 units).

Any of these requires a separately authorized new wave with its own census.

## Workflow contract

- **Claude Code performs GitHub writes, branches, commits, PR corrections and merges.**
- **The reviewer independently reviews exact live state and supplies prompts.** Every stage merges only at its
  exact reviewed head, as a normal merge.
- **Live GitHub and production beat copied prompts and reports.**
- Wave-8 P5 is recorded by the control-only PR `Wave 8 P5 — production acceptance and durable control close-out`.
  - It adds `WAVE8_P5_PRODUCTION_ACCEPTANCE.md` and updates `HANDOVER.md` and this file.
  - No implementation or source change belongs to it.
  - It was merged as `pugazg/kalaignar-tribute#39` (merge `78888627be63b9b3d4e04afd8908cb4d17d82d59`).
- Reading Room IA v2 R0 is recorded by the control-only PR `Reading Room IA v2 — R0 classification census`.
  - It adds `READING_ROOM_IA_V2_R0_CENSUS.md` and updates `HANDOVER.md` and this file.
  - No implementation or source change belongs to it.
  - It was merged as `pugazg/kalaignar-tribute#40` (merge `399319ea7995c24a06da6866babefe086751afe6`). The
    control-only PR `Reading Room IA v2 — R0 lifecycle close-out` moves its lifecycle wording to COMPLETE /
    REVIEWED / FROZEN. It changes no finding. It was merged as `pugazg/kalaignar-tribute#41` (merge
    `99ce1dbcc724b5daaa1716bd9a9ea90452fc32e0`).
- Reading Room IA v2 R1 is recorded by the control-only PR `Reading Room IA v2 — R1 canonical identity and
  cross-witness reconciliation`.
  - It adds the R1 record, manifest and evidence, and updates `HANDOVER.md` and this file.
  - No implementation or source change belongs to it.
  - It was merged as `pugazg/kalaignar-tribute#42` (merge `1d12bd6dbf262d570c3199b3eb6d681cef62f0dc`). The
    control-only PR `Reading Room IA v2 — R1 lifecycle close-out` moves its lifecycle wording to COMPLETE /
    REVIEWED / FROZEN. It changes no decision. It was merged as `pugazg/kalaignar-tribute#43` (merge
    `62739aac68ce28ba1a41c41f242288afea8f603e`).
- The owner HOLD adjudication is recorded by the control-only PR `Reading Room IA v2 — owner HOLD adjudication`.
  - It adds the adjudication record and the resolved manifest, and updates `HANDOVER.md` and this file.
  - Frozen R0 and R1 files are untouched.
  - It was merged as `pugazg/kalaignar-tribute#44` (merge `cc131a26501e714664ec80c011522cf0155dccb0`).
  - The control-only PR `Reading Room IA v2 — owner HOLD adjudication lifecycle close-out` moves its lifecycle wording
    to COMPLETE / REVIEWED / FROZEN and changes no decision. It was merged as `pugazg/kalaignar-tribute#45` (merge
    `d66db0e05aef1f7691fbcabd502e4a7953028c24`).
- The R2 plan is recorded by the control-only PR `Reading Room IA v2 — R2 plan`.
  - It adds `READING_ROOM_IA_V2_R2_PLAN.md` and updates `HANDOVER.md` and this file.
  - No implementation or source change belongs to it.
  - It was merged as `pugazg/kalaignar-tribute#46` (merge `811fdc214f5e290cca5d18b660a29d27b4d43b37`, approved head
    `df99c0ea…`).
- R2-A was implemented by `pugazg/kalaignar-autobiography#102` (approved head `1607b892…`, 2 commits; merge
  `19c0ee15a5a78d04852be2144a72a0328d307400`, tree `d899d04f…`).
  - Its lifecycle is recorded by the control-only PR `Reading Room IA v2 — R2-A checkpoint`, merged as
    `pugazg/kalaignar-tribute#47` (merge `a9600327de2e9c786ee3ee25dbce8db6edb7ed98`, approved head `8ea201d9…`).
- R2-B was implemented by `pugazg/kalaignar-autobiography#103` (approved head `07dd8a7f…`, 1 commit; merge
  `89c682553d6ba07a96e966bb982d60ebe0cd8b47`, tree `cb70d857…`).
  - Its lifecycle and production acceptance are recorded by the control-only PR `Reading Room IA v2 — R2-B
    checkpoint`, merged as `pugazg/kalaignar-tribute#48` (merge `4156aa0937419523bff5c6df873a1f48a95a6709`, approved
    head `d03ff8b2…`).
- R2-C was implemented by `pugazg/kalaignar-autobiography#104` (approved head `3b3b8868…`, 1 commit; merge
  `597e65fde3266baffda98351de716507368b5ebc`, tree `da22e2f4…`).
  - The final R2 record is the control-only PR `Reading Room IA v2 — R2 close-out`, merged as
    `pugazg/kalaignar-tribute#49` (merge `c4c3ccd4b0c3130e0fa96f1e8f140a2b9ff1f458`, approved head `e688e462…`).
- R3 planning is recorded by the control-only PR `Reading Room IA v2 — R3 plan`.
  - It adds `READING_ROOM_IA_V2_R3_PLAN.md` and updates `HANDOVER.md` and this file.
  - No implementation, source or production change belongs to it.
  - It was merged as `pugazg/kalaignar-tribute#50` (merge `bab2fd4d2008fc57f527b3627087f38755a16a64`, approved head
    `650ed021…`).
- R3-A was implemented by `pugazg/kalaignar-autobiography#105` (approved head `be1d6d4f…`, 2 commits; merge
  `06731e0eaaa6f1228388add726204a2df694c649`, tree `5c2bf2c9…`).
  - Its lifecycle and production invariance are recorded by the control-only PR `Reading Room IA v2 — R3-A checkpoint`,
    which adds `READING_ROOM_IA_V2_R3A_CHECKPOINT.md` and updates `HANDOVER.md` and this file. It was merged as
    `pugazg/kalaignar-tribute#51` (merge `c2a17f0aa1481557c717429b3f4cf811a1875b48`, approved head `ddfe6a28…`).
- R3-B was implemented by `pugazg/kalaignar-autobiography#106` (approved head `1826e546…`, 4 commits; merge
  `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb`, tree `b65c5417…`).
  - Its lifecycle and production acceptance are recorded by the control-only PR `Reading Room IA v2 — R3-B checkpoint`,
    which adds `READING_ROOM_IA_V2_R3B_CHECKPOINT.md` and updates `HANDOVER.md` and this file. It was merged as
    `pugazg/kalaignar-tribute#52` (merge `41f7e0cb5ca70894b0943363567f8a37c636771d`, approved head `f137153a…`).
- R3-C was implemented by `pugazg/kalaignar-autobiography#107` (approved head `aeec6bda…`, 3 commits; merge
  `afef75f9eca8367c2905c0d080f5c1fd82729b04`, tree `6c4ad32a…`).
  - Its lifecycle and production acceptance are recorded by the control-only PR `Reading Room IA v2 — R3-C checkpoint`,
    which adds `READING_ROOM_IA_V2_R3C_CHECKPOINT.md` and updates `HANDOVER.md` and this file. It was merged as
    `pugazg/kalaignar-tribute#53` (merge `39ada6b24973ca65b8ec68357b0a5f0cfbac48e4`, approved head `5af384a6…`).
- R3-D was implemented by `pugazg/kalaignar-autobiography#108` (approved head `483bb2e4…`, 3 commits; merge
  `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853`, tree `cd1f1367…`).
  - Its lifecycle and final production acceptance are recorded by the control-only PR `Reading Room IA v2 — R3-D
    checkpoint`, which adds `READING_ROOM_IA_V2_R3D_CHECKPOINT.md` and updates `HANDOVER.md` and this file.
  - Until that PR is merged, live control `main` remains authoritative.

**STOP. Wave 6, Wave 7 and Wave 8 are COMPLETE / CLOSED / FROZEN at P5. There is no Wave-8 P6. Reading Room IA v2
R0, R1 and owner HOLD adjudication are COMPLETE / REVIEWED / FROZEN. Resolved manifest HOLD = 0. R2 is COMPLETE /
REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED. R3 is OWNER-AUTHORIZED ("let's start R3"); the R3 PLAN is COMPLETE /
REVIEWED / FROZEN; R3-A, R3-B, R3-C and R3-D are COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED; R3 IMPLEMENTATION is
COMPLETE; R3 CLOSE-OUT is NOT YET FROZEN (the R3-D checkpoint awaits independent exact-head review and merge). No R4, new
wave or maintenance activity is authorized. Do not begin a new wave or any maintenance activity without explicit owner
authorization.**
