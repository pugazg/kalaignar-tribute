# Reading Room IA v2 — R3-B Checkpoint (Poetry Promotions)

**Recorded:** 2026-09-27.

**Status: R3 — OWNER-AUTHORIZED ("let's start R3"). R3 PLAN — COMPLETE / REVIEWED / FROZEN. R3-A — COMPLETE / REVIEWED /
MERGED / PRODUCTION-ACCEPTED. R3-A CHECKPOINT — COMPLETE / REVIEWED / MERGED. R3-B IMPLEMENTATION — COMPLETE / REVIEWED /
MERGED / PRODUCTION-ACCEPTED. R3-B CHECKPOINT — REVIEW-READY. R3-C — NOT STARTED. R3-D — NOT STARTED.**

This is a **control-only lifecycle checkpoint**. It records an implementation stage that has already been independently
reviewed, merged and accepted on production.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

**Authority:**
- **Owner authorization (standing for all R3 stages):** "let's start R3".
- **The frozen R3 plan** [`READING_ROOM_IA_V2_R3_PLAN.md`](./READING_ROOM_IA_V2_R3_PLAN.md): merged as
  `pugazg/kalaignar-tribute#50` → `bab2fd4d2008fc57f527b3627087f38755a16a64`.
- **The merged R3-A checkpoint** [`READING_ROOM_IA_V2_R3A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3A_CHECKPOINT.md):
  `pugazg/kalaignar-tribute#51` → `c2a17f0aa1481557c717429b3f4cf811a1875b48` (tree `812c25be…`; parents `bab2fd4d…`,
  `ddfe6a28…`; approved head → merge = 0 files). Its file keeps its reviewed "REVIEW-READY" wording, which the merge
  supersedes; it is not reopened.

---

## 1. Live pins (re-fetched 2026-09-27)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `c2a17f0aa1481557c717429b3f4cf811a1875b48` (tree `812c25be…`) |
| Implementation `main` | `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb` (tree `b65c541734b62a8cb4e21ffd52ff598a480019e1`); 0 open implementation PRs |
| Production | Vercel deployment `6687152070` at `109e4bfd…` |
| Source heads (unchanged) | poems `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` · literary-commentary `e23548b09547a2308407e60e5e67c1a03fee5354` · essays `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` · short-stories `7205a10892d0b208df2617766844f480b6a2c798` |

## 2. Merge record — implementation PR #106

- **Title:** "Reading Room IA v2 R3-B: Poetry promotions (+162 works, 4 publications demoted)".
- **Review:** the first exact-head review of `5ee995d9…` found one validator correction (below). The corrected head
  `1826e546…` then passed independent exact-head review — **FINAL PASS** — and was merged by a normal merge commit,
  pinned to the approved head (`--match-head-commit`).

| Item | Value |
|---|---|
| Reviewed base | `06731e0eaaa6f1228388add726204a2df694c649` (the merged R3-A) |
| Approved head | `1826e54651c491cb8c090bd986ebbef6fc5ce4a8` (tree `b65c541734b62a8cb4e21ffd52ff598a480019e1`) |
| Commits | exactly 4 (`4aee6967`, `2f07312c`, `5ee995d9`, `1826e546`); not squashed, rebased or amended |
| Changed files | 47, +6466 / −338 |
| Merge commit | `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb`, merged 2026-09-27T02:35:21Z |
| Merge tree | `b65c541734b62a8cb4e21ffd52ff598a480019e1` (= approved-head tree) |
| First parent | `06731e0eaaa6f1228388add726204a2df694c649` |
| Second parent | `1826e54651c491cb8c090bd986ebbef6fc5ce4a8` |
| Approved head → merge | **0 changed files** |
| Base → merge | exactly the four reviewed commits and the merge `109e4bfd`, over the same 47 files (+6466 / −338) |
| PR state | MERGED / CLOSED |

**The review correction (fourth commit `1826e546`):**
- The first-pass reconciliation of the historical Wave-8 negative guard for `நகைச் சுவைப் பகுதி.` exempted any non-Murasoli
  R3-published work. That was too broad.
- The corrected guard asserts that the catalogue records matching the unchanged probe `nagai|சுவைப்|comedy` are
  **exactly** `["it-is-over-a-comedy-drama"]` (the R3-B Kavithaigal poem "It Is Over—a Comedy Drama!",
  `/poems/kalaignarin-kavithaigal/it-is-over-a-comedy-drama`). Any second match fails.
- Old reviewed head `5ee995d9…` → corrected head: exactly one file, `scripts/validate-wave8-p4-integration.ts`, +3 / −3;
  no runtime or generated R3 file changed.

## 3. CI, Preview and deployment

- **Exact-head CI:** `Library CI` run `36257100065` on `1826e546…` — `typecheck • build` SUCCESS, `archival validators`
  SUCCESS.
  - Its first `typecheck • build` attempt failed on a transient `next/font` Google-font fetch error (`Newsreader`),
    unrelated to the one-script change; the failed job was re-run on the same head (attempt 2) and succeeded.
- **Exact-head Vercel Preview:** SUCCESS / Ready
  (`https://kalaignar-autobiography-kxizxtg7i-rain-drops.vercel.app`, behind Vercel Deployment Protection).
  - **Protected Preview UI acceptance — PASS**, read-only, after the owner signed in to Vercel in the browser pane: the
    same checks as §5, with the same results.
- **Merge CI:** `Library CI` run `36288951207` on `109e4bfd…` — **COMPLETED / SUCCESS**. `typecheck • build` SUCCESS;
  `archival validators` SUCCESS.
- **Deployment (recorded as found):** the Vercel commit status is success.
  - GitHub deployment `6687152070` was created by `vercel[bot]` at 2026-09-27T02:41:22Z, environment `Production`,
    state success.
  - It is the existing automatic deploy of `main`. No manual deployment was made.

## 4. What R3-B delivered

**Stage state on merged `main`:** `published = [R3-A, R3-B]` (the generator's `PUBLISHED_STAGES`; every generated
artefact regenerates byte-identically under `build-r3-identity --verify`).

- **162 R3 identities published** as canonical LibraryWorks, generated into `data/r3-catalogue.ts`, each at its existing
  reading route (`readerStructure: "publication-unit"`):
  - `poetry-kaalap` 57 · `poetry-kavithaigal` 74 · `poetry-1975` 3 · `ina-poem` 3 · `meesai` 25.
  - **87** CREATE identities remain dormant (R3-C).
- **4 publications demoted to publication records** (`LIBRARY_PUBLICATIONS`), each its former LibraryWork record
  verbatim minus `state`, plus only `kind: "source-publication"` and `demotedIn: "R3-B"`. None remains a canonical
  LibraryWork; every landing, reader and `/source` route is kept.
  - Poetry: `kaalap-pezhaiyum-kavithai-saaviyum`, `kalaignarin-kavithaigal`, `kalaignarin-kaviyaranga-kavithaigal-1975`.
  - Essays & Articles: `meesai-mulaiththa-vayathil`.
  - Category pages list them in a secondary bilingual **நூல்கள் / Publications** section: Poetry 3, Essays 1.
- **Ina fragment identities:** the three `இன முழக்கம்` poems are canonical works at
  `/essays/ina-muzhakkam/articles/kavithaigal#poem-6-4` (`வா!`), `#poem-6-7` (`மாணவர் எழுச்சி.`) and `#poem-6-8`
  (`வாளிங்கே!`). The unit emits stable anchors `poem-6-1` … `poem-6-11` on its printed poem headings, with a scroll
  margin that clears the sticky header. These are the only canonical works sharing a pathname.
- **Relations:** the 18 R3-B relations are active. Witness notes render on both ends; scan-range and external witnesses
  render as text (they have no page). The two Wave-4 links render exactly as before.
- **Validators:** `test:r3-identity` was extended (823 checks), with 8 sabotage controls each proven to fail it:
  missing identity; container kept canonical; extra demotion; R3-C activated early; Ina anchor removed; duplicate href;
  DO_NOT_PROMOTE row published; witness activated before its target.
  - Earlier-wave validators were reconciled without weakening: counts add the derived `READ_IA_R3_CONTRIBUTION` terms;
    record and membership checks use the pre-R3 projection (`lib/read-ia-r3-projection.ts`); the Wave-4 archival
    validators reconcile item promotion explicitly against `identity-manifest.json`;
    `build-wave8-p4-publication --verify` stays byte-identical.

| Item | Pre-R3 boundary | After R3-B |
|---|---|---|
| Canonical catalogue | 335 | **493** |
| Shelves (life / letters / fiction / poetry / drama / cinema / speeches / essays / lit. comm.) | 1/1/162/14/11/10/117/15/4 | **1/1/162/173/11/10/117/14/4** |
| `LIBRARY_PUBLICATIONS` | 0 | **4** (Poetry 3, Essays 1) |
| Relations | 49: 2 active / 47 dormant | 49: **20 active / 29 dormant** (R3-C 2 · R3-D 27) |
| Collections | 9 | **9**, records byte-identical to the boundary |
| Build | 5280 / 5275 | **5280 / 5275** |
| Sitemap | 5271 (`c65c6377…`) | **5271, same set** |

**`READ_IA_R3_CONTRIBUTION` (derived from the stage state, never typed):** works **+158** · Poetry **+159** · Essays &
Articles **−1** · all other shelves 0 · collections 0 · build 0 · sitemap 0.

**The five canonical merges are R3-D and have not started.** All five `merged-witness` records are `state: dormant`,
`introducedIn: R3-D`. The five merge-source stories (`sirai-kodiyathu`, `neeyum-kaithi-naanum-kaithi`, `aadik-kaatre`,
`pugazhe-nee-oru-pudhir`, `sorgaththirku-vandhathu-eppadi`) remain canonical Fiction works and collection members.

## 5. Production acceptance (read-only, `nenjukkuneethi.org`, deployment `6687152070`)

- **`/read`:** exactly **9** category cards — Life Writing 1 · Letters 1 · Fiction 162 · 7 collections · **Poetry 173** ·
  Drama 11 · Cinema Writing 10 · Speeches 117 · 2 collections · **Essays & Articles 14** · Literary Commentary 4.
- **`/read/poetry`:** exactly **173** canonical work cards (173 unique hrefs) and exactly **3** Publication cards
  (`kaalap-pezhaiyum-kavithai-saaviyum`, `kalaignarin-kavithaigal`, `kalaignarin-kaviyaranga-kavithaigal-1975`); none of
  the three is a work card. Promoted cards link to the existing child readers.
- **`/read/essays`:** exactly **14** canonical work cards and exactly **1** Publication card
  (`meesai-mulaiththa-vayathil`), which is not a work card.
- **Routes:**
  - all **185** distinct Poetry and Essays card targets return 200;
  - all 4 publication landings and all 4 `/source` routes return 200;
  - representative child readers return 200, including the three 1975 item slug routes;
  - invalid examples return 404: `/poems/kalaignarin-kaviyaranga-kavithaigal-1975/03`,
    `/poems/oruthalaik-kathal/section-0`, `/poems/no-such-poem`,
    `/essays/meesai-mulaiththa-vayathil/articles/no-such-article`, `/poems/kalaignarin-kavithaigal/no-such-item`,
    `/read/no-such-category`.
- **Ina fragments** (each followed from its `/read/poetry` card): `#poem-6-4` → `வா!`, `#poem-6-7` → `மாணவர் எழுச்சி.`,
  `#poem-6-8` → `வாளிங்கே!`. Each heading lands 112 px from the top, clear of the 49 px sticky header; all anchors
  `poem-6-1` … `poem-6-11` exist.
- **Active witness UI:**
  - the two pre-R3 links (Anna, Thennan) are intact on both ends;
  - Idhayathai also shows its 1975 witness (scans 9–20) as text;
  - `gunanayagar-nehru` shows its Kavithaigal witness (linked both ways) and its 1975 witness (scans 21–32);
  - `oruthalaik-kathal` ↔ the Kaalap unit `can-he-be-bought-with-love`, linked both ways;
  - the Ina `kavithaigal` unit shows its 8 active notes, linking the 8 Kavithaigal poems;
  - `green-parrot` ↔ the Meesai unit `பச்சைக்கிளி`, linked both ways.
- **Dormant relations are invisible:** no witness UI for either R3-C relation (the two Thudikkum Ilamai units and
  `/speeches/idhaya-perikai`), for any of the five merges (source stories and published target pages), for the
  Sangatamil section relations (`oruthalaik-kathal` and its sections), or for the 1958 `தேனலைகள்` relations (the
  published Meesai target pages).
- **Sitemap:** **5271** paths, 0 duplicates, 0 fragment entries; set hash **`c65c6377…`** — identical to the pre-R3
  set (0 added, 0 removed). The build is **5280** prerender / **5275** HTML, enforced by the merge CI.

## 6. Lifecycle

| Stage | Status |
|---|---|
| R0 · R1 · owner adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED |
| R3 | OWNER-AUTHORIZED ("let's start R3") |
| R3 PLAN | COMPLETE / REVIEWED / FROZEN (`#50` → `bab2fd4d…`) |
| R3-A | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#105` → `06731e0e…`) |
| R3-A CHECKPOINT | COMPLETE / REVIEWED / MERGED (`#51` → `c2a17f0a…`) |
| **R3-B IMPLEMENTATION** | **COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (`pugazg/kalaignar-autobiography#106` → `109e4bfd…`) |
| **R3-B CHECKPOINT (this record)** | **REVIEW-READY** |
| **R3-C** | **NOT STARTED** |
| **R3-D** | **NOT STARTED** (the five merges remain dormant R3-D records) |

**Next:** independent exact-head review and merge of this checkpoint. Only then **R3-C** (Essays / Letters / Speech:
+87 − 7 → 573; 2 relations), under the standing R3 authorization and its own exact-head review gate. R3-D follows R3-C.
