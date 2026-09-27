# Reading Room IA v2 — R3-D Checkpoint (Merges, Sangatamil, 1958 — Final R3 Implementation Stage)

**Recorded:** 2026-09-27.

**Status: R3 — OWNER-AUTHORIZED ("let's start R3"). R3 PLAN — COMPLETE / REVIEWED / FROZEN. R3-A, R3-B and R3-C — COMPLETE /
REVIEWED / MERGED / PRODUCTION-ACCEPTED. R3-D IMPLEMENTATION — COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED. R3-D
CHECKPOINT — REVIEW-READY. R3 IMPLEMENTATION — COMPLETE. R3 CLOSE-OUT — NOT YET FROZEN.**

This is a **control-only lifecycle checkpoint**. It records the final R3 implementation stage, which has already been
independently reviewed, merged and accepted on production. R3 is **not** declared closed here: this record itself still
requires independent exact-head review and merge.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.
- **No post-R3 activity has started** (no R4, no new wave, no maintenance).

**Authority:**
- **Owner authorization (standing for all R3 stages):** "let's start R3".
- **The frozen R3 plan** [`READING_ROOM_IA_V2_R3_PLAN.md`](./READING_ROOM_IA_V2_R3_PLAN.md): `pugazg/kalaignar-tribute#50`
  → `bab2fd4d2008fc57f527b3627087f38755a16a64`.
- **Merged checkpoints** (each file keeps its reviewed "REVIEW-READY" wording, which its merge supersedes; none is reopened):
  - R3-A [`READING_ROOM_IA_V2_R3A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3A_CHECKPOINT.md): `#51` → `c2a17f0a…`;
  - R3-B [`READING_ROOM_IA_V2_R3B_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3B_CHECKPOINT.md): `#52` → `41f7e0cb…`;
  - R3-C [`READING_ROOM_IA_V2_R3C_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3C_CHECKPOINT.md): `#53` →
    `39ada6b24973ca65b8ec68357b0a5f0cfbac48e4` (tree `d472f35e…`; parents `41f7e0cb…`, `5af384a6…`; approved head → merge =
    0 files).

---

## 1. Live pins (re-fetched 2026-09-27)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `39ada6b24973ca65b8ec68357b0a5f0cfbac48e4` (tree `d472f35e…`) |
| Implementation `main` | `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853` (tree `cd1f1367be4320cff34c58db30be843708de650e`); 0 open implementation PRs |
| Production | Vercel deployment `6688540026` at `7fe9a4f0…` |
| Source heads (unchanged) | poems `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` · literary-commentary `e23548b09547a2308407e60e5e67c1a03fee5354` · essays `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` · short-stories `7205a10892d0b208df2617766844f480b6a2c798` |

## 2. Merge record — implementation PR #108

- **Title:** "Reading Room IA v2 R3-D: five canonical merges, Sangatamil and 1958 relations (final R3 stage)".
- **Review:** independent exact-head review — **FINAL PASS**. Merged by a normal merge commit, pinned to the approved head
  (`--match-head-commit`).

| Item | Value |
|---|---|
| Reviewed base | `afef75f9eca8367c2905c0d080f5c1fd82729b04` (the merged R3-C) |
| Approved head | `483bb2e45badbf846f61394abc6a1114f92b39b2` (tree `cd1f1367be4320cff34c58db30be843708de650e`) |
| Commits | exactly 3 (`3732a560` stage, `79626f36` final-state tests, `483bb2e4` validator reconciliation); not squashed, rebased or amended |
| Changed files | 29, +539 / −104 |
| Merge commit | `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853`, merged 2026-09-27T05:35:37Z |
| Merge tree | `cd1f1367be4320cff34c58db30be843708de650e` (= approved-head tree) |
| First parent | `afef75f9eca8367c2905c0d080f5c1fd82729b04` |
| Second parent | `483bb2e45badbf846f61394abc6a1114f92b39b2` |
| Approved head → merge | **0 changed files** |
| Base → merge | exactly the three reviewed commits and the merge `7fe9a4f0`, over the same 29 files (+539 / −104) |
| PR state | MERGED / CLOSED |

## 3. CI, Preview and deployment

- **Exact-head CI:** `Library CI` run `36296338864` on `483bb2e4…` — `typecheck • build` SUCCESS, `archival validators`
  SUCCESS (first attempt).
- **Exact-head Vercel Preview:** SUCCESS / Ready (`https://kalaignar-autobiography-m72eemu2t-rain-drops.vercel.app`, behind
  Vercel Deployment Protection).
  - **Protected Preview UI acceptance — PASS**, read-only under the owner's Vercel sign-in in the browser pane: the same
    checks as §5, with the same results.
- **Merge CI:** `Library CI` run `36297650051` on `7fe9a4f0…` — **COMPLETED / SUCCESS**, both jobs on the first attempt (the
  intermittent `next/font` Google-font fetch failure did not recur).
- **Deployment (recorded as found):** GitHub deployment `6688540026`, created by `vercel[bot]` at 2026-09-27T05:40:15Z,
  environment `Production`, state success — the existing automatic deploy of `main`. No manual deployment was made.

## 4. What R3-D delivered

**Final stage state on merged `main`:** `published = [R3-A, R3-B, R3-C, R3-D]`. Every generated artefact regenerates
byte-identically under `build-r3-identity --verify`.

- **All 249 CREATE identities are canonical**, each exactly once on its frozen shelf and subtype; **0** dormant. All **20**
  DO_NOT_PROMOTE rows remain non-canonical.
- **The five canonical merges (OD3–OD5)**, through the one relation registry (no second registry):

  | Legacy story | 2004 ordinal | Canonical work |
  |---|---:|---|
  | `neeyum-kaithi-naanum-kaithi` | 2 | `piraiye` |
  | `sorgaththirku-vandhathu-eppadi` | 14 | `sorgga-logaththil` (Essay) |
  | `aadik-kaatre` | 17 | `adikkaatru` |
  | `sirai-kodiyathu` | 20 | `green-parrot` |
  | `pugazhe-nee-oru-pudhir` | 23 | `pugazh` |

  - Each legacy id has left `LIBRARY_WORKS` (the generated `R3_MERGED_WITNESSES`) and exists exactly once, as its active
    `merged-witness` record carrying its former LibraryWork record verbatim. Each target is canonical exactly once.
  - Story payloads are unchanged (pinned by sha256); `/stories/<slug>` and `/stories/<slug>/source` are preserved, with no
    redirect. Each story page gains only a derived, work-type-aware notice (`… கவிதையின் / கட்டுரையின் ஒரு மூல ஆதாரப்
    பதிப்பு`) linking its canonical work; each canonical work lists its legacy story. `green-parrot` keeps its Meesai
    `பச்சைக்கிளி` witness and gains `sirai-kodiyathu`, neither duplicated.
- **The 2004 anthology is preserved.** `LIBRARY_COLLECTIONS` is byte-identical to the frozen pre-R3 registry; no member is
  repointed. `collectionMemberWorks()` resolves through the merged-witness resolver (`lib/collection-members.ts`), which
  still fails closed and names the collection. `2004-kalaignarin-kuttik-kathaigal` shows **34** entries in printed order;
  the five merged entries keep ordinals 2 / 14 / 17 / 20 / 23, their printed old titles and story links, and gain a derived
  canonical-work link; the other 29 resolve as canonical works.
- **Sangatamil — canonical side only.** 11 `commentary-section` relations map Sangatamil 092–102 one-to-one to
  `oruthalaik-kathal` §1–§11. The `oruthalaik-kathal` landing shows all 11 plus its existing Kaalap witness; each section
  page shows exactly its matching Sangatamil section. A named `CANONICAL_SIDE_ONLY` rule stops any reverse note:
  `/sangatamil` and all 104 section pages are unchanged (pinned by `test:r3-identity`, normalized, to the R3-C build).
  Sangatamil remains one Literary Commentary LibraryWork; no section is a LibraryWork; no payload changed.
- **1958 `தேனலைகள்`** (frozen plan §10: December 1958, TVA_BOK_0064030, `kalaignar-short-stories@7205a108`
  `collections/1958-thenalaigal/README.md`; not a LibraryWork, no route, not ingested):
  - **10 chapter-level** relations, each carrying its `alai`: 2 `mayiliragu` · 4 `madal` · 5 `thozhi` · 6 `maruthaani` ·
    7 `aruvi` · 8 `muram` · 9 `yaazh` · 10 `sirpi` · 11 `seval-sandai` · 12 `aandu-vizha`; each page shows "… அலை N «…»
    ஆகவும் வெளியானது: தேனலைகள் (1958)", with no link.
  - **1 publication-level** relation (`thenalaigal`, no `alai`): "related to the 1958 publication …; the source indicates
    அலை 1 «முத்தாரம்»; no chapter equivalence is asserted".
  - **அலை 3 `முத்துமாலை` has no relation** — enforced on the relation registry (the word in the `thenalaigal` essay's own
    printed text is source text, not a relation).
  - The Meesai landing keeps its publication surface and gains only the derived OD6 note: units 16–26 are the same
    underlying content as தேனலைகள் (December 1958) under different titles and order; 10 அலைகள் map chapter by chapter;
    அலை 1 relates at publication level only; அலை 3 is not mapped. No 1958 link is rendered.
- **Validators:** `test:r3-identity` (1001 checks) pins the final state, with 11 sabotage controls each proven to fail it
  (one legacy work left canonical; one legacy relation removed; an extra Fiction work merged; one target changed; one story
  route deleted; one collection member repointed; reverse Sangatamil rendering allowed; an அலை 3 mapping added; a chapter
  target changed; an `alai` on the publication record; the 1958 publication promoted to a LibraryWork).
  - Earlier-wave validators were reconciled narrowly: Fiction counts add the derived −5; Batch-7 / Reading Room
    validators admit exactly the five frozen legacy→target pairs (`R3_MERGED_LEGACY` / `mergedLegacyRecord`, only while
    each relation is active) as their verbatim record, on which every field assertion still runs;
    `build-wave8-p4-publication --verify` stays byte-identical.

| Item | After R3-C | **Final (after R3-D)** |
|---|---|---|
| CREATE identities published / dormant | 249 / 0 | **249 / 0** |
| Canonical catalogue | 573 | **568** |
| Shelves (life / letters / fiction / poetry / drama / cinema / speeches / essays / lit. comm.) | 1/3/162/173/11/10/118/91/4 | **1/3/157/173/11/10/118/91/4** |
| Publication records | 11 | **11** (Poetry 3, Essays 8; unchanged) |
| Relations | 49: 22 active / 27 dormant | **49: 49 active / 0 dormant** |
| Collections | 9 | **9**, byte-identical to the pre-R3 boundary |
| Build | 5280 / 5275 | **5280 / 5275** |
| Sitemap | 5271 (`c65c6377…`) | **5271, same set** |

**Relation census (final):** source-publication 22 (work 20 · section 2) · merged-witness 5 (work) · commentary-section 11
(section) · external-publication 11 (chapter 10 · publication 1). Every active target is a published canonical work.

**`READ_IA_R3_CONTRIBUTION` (derived from the stage state and the active merged-witness relations, never typed):** works
**+233** · Fiction **−5** · Poetry **+159** · Essays & Articles **+76** · Letters **+2** · Speeches **+1** · all other
shelves 0 · collections 0 · build 0 · sitemap 0.

## 5. Production acceptance (read-only, `nenjukkuneethi.org`, deployment `6688540026`)

- **`/read`:** exactly 9 category cards — 1 · 3 · **157** · 7 collections · 173 · 11 · 10 · 118 · 2 collections · 91 · 4.
- **`/read/fiction`:** **157** canonical work cards (157 unique) and **7** collection cards; none of the five legacy ids is a
  work card.
- **Five merges:** all five `/stories/<slug>` and `/stories/<slug>/source` routes return 200 (no redirect). Each story page
  links its canonical target with work-type-aware wording (`கட்டுரையின்` for `sorgga-logaththil`, `கவிதையின்` for the four
  poems); each canonical page lists its legacy story; `green-parrot` lists `pachchaikkili` and `sirai-kodiyathu`, once each.
- **2004 collection:** **34** rows, ordinals 1–34 in order; the five merged rows at 2 / 14 / 17 / 20 / 23 show their printed
  titles, story links and canonical links; the other 29 rows carry one link each.
- **Sangatamil:** the `oruthalaik-kathal` landing shows all 11 Sangatamil links plus the Kaalap witness; sections 1–11 each
  link exactly `/sangatamil/092…` … `/sangatamil/102…`; `/sangatamil` and its section pages show no reverse note or link.
- **1958:** the 10 chapter pages show their exact அலை number and heading; `thenalaigal` shows only the publication-level
  note; the Meesai landing shows the OD6 note and no 1958 link; no 1958 route exists (404).
- **R3-B / R3-C preserved:** Anna and Thennan, `gunanayagar-nehru`, Kaalap ↔ `oruthalaik-kathal`, the Ina unit's 8 notes,
  Ina anchors `poem-6-1` … `poem-6-11`, `green-parrot` ↔ Meesai, `idhaya-perikai` sections 3 / 4, the OD8 Letters
  (`/read/letters` = Murasoli + the two Sinthanaiyum routes) and `thudikkum-ilamai-urai` (its article route).
- **Routes:** all **540** distinct category-card targets return 200; all 11 publication landings and `/source` routes and
  `/sangatamil` + `/sangatamil/source` return 200; invalid examples return 404.
- **Rendered change set:** the local R3-D build (tree `cd1f1367`) compared with Production R3-C changed exactly **37**
  sitemap pages — `/read`, `/read/fiction`, the 2004 collection, the five story pages, the five canonical targets, the
  Meesai landing, the ten chapter-mapped Meesai works, `thenalaigal`, the `oruthalaik-kathal` landing and its eleven section
  pages — with **0** Sangatamil and **0** `/source` pages changed. With the relation / witness-note blocks removed, all 34
  reader pages equal the R3-C Production baseline: no story, poem or essay text changed. After deployment, Production R3-D
  equals that build on all 5271 pages.
- **Canonical href contract (merged tree):** 568 unique ids, slugs and href strings; the only shared pathname is
  `/essays/ina-muzhakkam/articles/kavithaigal` (`ina-muzhakkam-poem-04`, `-07`, `-08`); no merged-story locator is
  canonical; all five story locators remain public witness routes.
- **Sitemap:** **5271** paths, 0 duplicates, 0 fragment entries, set hash **`c65c6377…`** (0 added, 0 removed; all five
  story routes and their `/source` routes present). Build **5280** / **5275**, enforced by the merge CI.

## 6. Lifecycle

| Stage | Status |
|---|---|
| R0 · R1 · owner adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED |
| R3 | OWNER-AUTHORIZED ("let's start R3") |
| R3 PLAN | COMPLETE / REVIEWED / FROZEN (`#50` → `bab2fd4d…`) |
| R3-A | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#105` → `06731e0e…`; checkpoint `#51` → `c2a17f0a…`) |
| R3-B | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#106` → `109e4bfd…`; checkpoint `#52` → `41f7e0cb…`) |
| R3-C | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#107` → `afef75f9…`; checkpoint `#53` → `39ada6b2…`) |
| **R3-D IMPLEMENTATION** | **COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (`pugazg/kalaignar-autobiography#108` → `7fe9a4f0…`) |
| **R3-D CHECKPOINT (this record)** | **REVIEW-READY** |
| **R3 IMPLEMENTATION** | **COMPLETE** (final catalogue 568 = frozen plan §6.5) |
| **R3 CLOSE-OUT** | **NOT YET FROZEN** |

**Next:** independent exact-head review and merge of this checkpoint. R3 is not declared closed by this record. No R4, new
wave or maintenance activity is authorized or started.
