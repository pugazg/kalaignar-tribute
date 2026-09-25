# New Chat Bootstrap Prompt — Kalaignar Digital Library / READING ROOM IA v2 R2 — AUTHORIZED · R2 PLAN REVIEW-READY · IMPLEMENTATION NOT STARTED (R0, R1 and adjudication frozen; Waves 6, 7 and 8 closed at P5)

Continue as my **independent reviewer and prompt-provider for Claude Code** for the Kalaignar Digital
Library / Reading Room. **Live GitHub and production are authoritative. Do not trust copied SHAs, PR
bodies or this bootstrap if live state differs.**

## Mandatory startup order

1. Fetch live `pugazg/kalaignar-tribute` `main`, and inspect all open control PRs.
2. Read `projects/kalaignar-digital-library/HANDOVER.md` **completely**.
   - Its highest-precedence CURRENT checkpoint is **2026-09-25 — READING ROOM IA v2 R2 — AUTHORIZED · R2 PLAN —
     COMPLETE / REVIEW-READY · R2 IMPLEMENTATION — NOT STARTED**.
   - Directly below it is the frozen owner-adjudication checkpoint (COMPLETE / REVIEWED / FROZEN). Its
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
   - Then read `READING_ROOM_IA_V2_R2_PLAN.md`, the authorized R2 plan (category-first `/read` over the existing 335
     works). Check whether that control PR has been independently reviewed and merged.
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

**Reading Room IA v2 — R2 (owner-authorized; category-first information architecture).**
- **R2 — AUTHORIZED. R2 PLAN — COMPLETE / REVIEW-READY (2026-09-25). R2 IMPLEMENTATION — NOT STARTED.**
- The plan is `READING_ROOM_IA_V2_R2_PLAN.md`. It is control-only (implementation, source and production deltas 0).
- **Target:** `/read` shows exactly 9 category cards (no work cards, collection cards or Daily Kural). There are 9
  static category routes (`/read/autobiography`, `/read/letters`, `/read/fiction`, `/read/poetry`, `/read/drama`,
  `/read/cinema`, `/read/speeches`, `/read/essays`, `/read/literary-commentary`; 0 collisions with the 391 memoir
  chapter ids).
  - Every published work appears on exactly one category page (335). Collections are secondary only.
  - **Letters special case (frozen R0 §6.2):** `/read/letters` shows exactly one canonical work, `murasoli-letters`,
    plus a corpus summary (13 volumes · 688 letters · Volumes 42–54, derived from the Murasoli data) and a "Browse by
    volume & sequence" link to the existing `/murasoli` browser.
    - Never build a flat or exploded Letters model: no letter or volume LibraryWorks and no new volume routes.
    - `/murasoli/<id>` is unchanged.
  - The `life-writing` public Tamil label becomes `சுயசரிதை`.
  - Sitemap +9 (projected 5271).
- **R2 / R3 boundary:** R2 does not create the 249 CREATE works or perform the 5 canonical merges. The catalogue stays
  335 and collections 9; that work is R3. Where frozen records say "future R2" merge actions, they mean R3 under the
  plan.
- **Staging:** R2-A (category model and routes) → R2-B (category-only `/read`) → R2-C (provenance, sitemap and full
  regression), each gated by exact-head review.
- **Next:** independent review and merge of the R2 plan PR, then **R2-A** only.

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
  - The control-only PR `Reading Room IA v2 — owner HOLD adjudication lifecycle close-out` was merged as
    `pugazg/kalaignar-tribute#45` (merge `d66db0e05aef1f7691fbcabd502e4a7953028c24`).
- The R2 plan is recorded by the control-only PR `Reading Room IA v2 — R2 plan`.
  - It adds `READING_ROOM_IA_V2_R2_PLAN.md` and updates `HANDOVER.md` and this file.
  - No implementation or source change belongs to it.
  - Until that PR is merged, live control `main` remains authoritative.
  - It was merged as `pugazg/kalaignar-tribute#44` (merge `cc131a26501e714664ec80c011522cf0155dccb0`). The
    control-only PR `Reading Room IA v2 — owner HOLD adjudication lifecycle close-out` moves its lifecycle wording to
    COMPLETE / REVIEWED / FROZEN. It changes no decision.

**STOP. Wave 6, Wave 7 and Wave 8 are COMPLETE / CLOSED / FROZEN at P5. There is no Wave-8 P6. Reading Room IA v2
R0, R1 and owner HOLD adjudication are COMPLETE / REVIEWED / FROZEN. Resolved manifest HOLD = 0. R2 is AUTHORIZED; the
R2 PLAN is COMPLETE / REVIEW-READY; R2 IMPLEMENTATION is NOT STARTED. Begin R2-A only after the R2 plan PR is
independently reviewed and merged. Do not begin R3 (catalogue expansion / canonical merges), a new wave or any
maintenance activity without explicit owner authorization.**
