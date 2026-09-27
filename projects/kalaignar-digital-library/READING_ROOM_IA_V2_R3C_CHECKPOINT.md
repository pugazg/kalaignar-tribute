# Reading Room IA v2 — R3-C Checkpoint (Essays, Letters and Speech Promotions)

**Recorded:** 2026-09-27.

**Status: R3 — OWNER-AUTHORIZED ("let's start R3"). R3 PLAN — COMPLETE / REVIEWED / FROZEN. R3-A — COMPLETE / REVIEWED /
MERGED / PRODUCTION-ACCEPTED. R3-B — COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED. R3-C IMPLEMENTATION — COMPLETE /
REVIEWED / MERGED / PRODUCTION-ACCEPTED. R3-C CHECKPOINT — REVIEW-READY. R3-D — NOT STARTED.**

This is a **control-only lifecycle checkpoint**. It records an implementation stage that has already been independently
reviewed, merged and accepted on production.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

**Authority:**
- **Owner authorization (standing for all R3 stages):** "let's start R3".
- **The frozen R3 plan** [`READING_ROOM_IA_V2_R3_PLAN.md`](./READING_ROOM_IA_V2_R3_PLAN.md): `pugazg/kalaignar-tribute#50`
  → `bab2fd4d2008fc57f527b3627087f38755a16a64`.
- **The merged R3-A checkpoint** [`READING_ROOM_IA_V2_R3A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3A_CHECKPOINT.md):
  `#51` → `c2a17f0aa1481557c717429b3f4cf811a1875b48`.
- **The merged R3-B checkpoint** [`READING_ROOM_IA_V2_R3B_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3B_CHECKPOINT.md):
  `#52` → `41f7e0cb5ca70894b0943363567f8a37c636771d` (tree `27474299…`; parents `c2a17f0a…`, `f137153a…`; approved head →
  merge = 0 files). Its file keeps its reviewed "REVIEW-READY" wording, which the merge supersedes; it is not reopened.

---

## 1. Live pins (re-fetched 2026-09-27)

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base of this checkpoint) | `41f7e0cb5ca70894b0943363567f8a37c636771d` (tree `27474299…`) |
| Implementation `main` | `afef75f9eca8367c2905c0d080f5c1fd82729b04` (tree `6c4ad32aedc379c65a257b94f69687f0fbff0b1c`); 0 open implementation PRs |
| Production | Vercel deployment `6687856705` at `afef75f9…` |
| Source heads (unchanged) | poems `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` · literary-commentary `e23548b09547a2308407e60e5e67c1a03fee5354` · essays `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` · short-stories `7205a10892d0b208df2617766844f480b6a2c798` |

## 2. Merge record — implementation PR #107

- **Title:** "Reading Room IA v2 R3-C: Essays / Letters / Speech promotions (+87 works, 7 publications demoted)".
- **Review:** independent exact-head review — **FINAL PASS**. Merged by a normal merge commit, pinned to the approved head
  (`--match-head-commit`).

| Item | Value |
|---|---|
| Reviewed base | `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb` (the merged R3-B) |
| Approved head | `aeec6bdafba5d16793defe38099e4dd1a4fff57c` (tree `6c4ad32aedc379c65a257b94f69687f0fbff0b1c`) |
| Commits | exactly 3 (`79fe0af5` stage, `f9abd642` identity tests, `aeec6bda` validator reconciliation); not squashed, rebased or amended |
| Changed files | 22, +2618 / −169 |
| Merge commit | `afef75f9eca8367c2905c0d080f5c1fd82729b04`, merged 2026-09-27T04:06:06Z |
| Merge tree | `6c4ad32aedc379c65a257b94f69687f0fbff0b1c` (= approved-head tree) |
| First parent | `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb` |
| Second parent | `aeec6bdafba5d16793defe38099e4dd1a4fff57c` |
| Approved head → merge | **0 changed files** |
| Base → merge | exactly the three reviewed commits and the merge `afef75f9`, over the same 22 files (+2618 / −169) |
| PR state | MERGED / CLOSED |

## 3. CI, Preview and deployment

- **Exact-head CI:** `Library CI` run `36290571028` on `aeec6bda…` — `typecheck • build` SUCCESS, `archival validators`
  SUCCESS.
- **Exact-head Vercel Preview:** SUCCESS / Ready (`https://kalaignar-autobiography-b5w7wsjzy-rain-drops.vercel.app`, behind
  Vercel Deployment Protection).
  - **Protected Preview UI acceptance — PASS**, read-only under the owner's Vercel sign-in in the browser pane: the same
    checks as §5, with the same results.
- **Merge CI:** `Library CI` run `36293330835` on `afef75f9…` — **COMPLETED / SUCCESS**. `archival validators` SUCCESS
  (attempt 1); `typecheck • build` SUCCESS (attempt 3).
  - Attempts 1 and 2 of `typecheck • build` failed in the Build step, inside `next/font`'s Google loader (`Failed to find
    font override values for font Newsreader`; `TypeError … loader.js:112`), before any validator ran — the same
    transient Google-font fetch failure seen once at R3-B. The merge tree equals the approved-head tree, which built green
    in `36290571028`; only the failed job was re-run, on the same commit, with no change.
- **Deployment (recorded as found):** GitHub deployment `6687856705`, created by `vercel[bot]` at 2026-09-27T04:11:56Z,
  environment `Production`, state success — the existing automatic deploy of `main`. No manual deployment was made.

## 4. What R3-C delivered

**Stage state on merged `main`:** `published = [R3-A, R3-B, R3-C]`. Every generated artefact regenerates byte-identically
under `build-r3-identity --verify`; the 162 R3-B records are unchanged.

- **All 249 CREATE identities are published, each exactly once on its frozen shelf and subtype; 0 remain dormant.**
- **87 R3-C works**, generated into `data/r3-catalogue.ts` (not hand-typed), each at its existing essay-unit route
  (`readerStructure: "publication-unit"`) — no new route, reader or payload:
  - **Essays & Articles 84:** ina-prose 5 · kolaikkalam 6 · perumoochu 13 · sinthanaiyum-seyalum 48 ·
    thiraavida-sampaththu 2 · thudikkum-ilamai 1 · unarchchimaalai 9.
  - **Letters 2 (OD8):** `paasiyum-thoosiyum`, `athiga-uyaram-thaanduvatharku`.
  - **Speech 1 (OD9):** `thudikkum-ilamai-urai`.
  - Each inherits its parent publication's source repo / path / commit and metadata exactly (no unit-level pin exists):
    the historical pins `564add70…`, `6814e979…` and `b5fd2922…` are kept; nothing is invented. Descriptions state only
    publication, year, kind and archive ordinal.
- **7 publications demoted** (`LIBRARY_PUBLICATIONS` is now **11**: Poetry 3, Essays & Articles 8): `ina-muzhakkam`,
  `unarchchimaalai`, `thiraavida-sampaththu`, `kolaikkalam`, `sinthanaiyum-seyalum`, `perumoochu`, `thudikkum-ilamai`.
  Each is its former LibraryWork record verbatim minus `state`, plus only `kind: "source-publication"` and
  `demotedIn: "R3-C"`; every landing, reader and `/source` route is kept.
- **OD8 Letters:** `/read/letters` holds exactly `murasoli-letters`, `paasiyum-thoosiyum` and
  `athiga-uyaram-thaanduvatharku`. The two OD8 works read at their existing Sinthanaiyum routes; no `/letters/…` route
  exists. The Murasoli corpus summary stays on `murasoli-letters` only; no Murasoli volume is a LibraryWork. Validators
  admit exactly this pair (`R3_OD8_LETTERS` / `isOd8Letter` in `lib/read-ia-r3-projection.ts`), not a broad exception.
- **`thudikkum-ilamai-urai`:** a canonical Speech at `/essays/thudikkum-ilamai/articles/thudikkum-ilamai` (its existing
  article reader). `/speeches/thudikkum-ilamai-urai` does not exist and returns 404.
- **The two R3-C relations are active:** `r3:thudikkum-ilamai/poompuhar->idhaya-perikai` and
  `r3:thudikkum-ilamai/vetri-vilakku->idhaya-perikai` (class `source-publication`, level `section`).
  - `/speeches/idhaya-perikai` shows exactly two section witnesses — section 3 `பூம்புகார் மாநாடு.` and section 4
    `வெற்றி விளக்கு!` — through a new optional `witnessLinks` prop on `SpeechReader`, passed only when present; the speech
    body is unchanged.
  - Each witness unit links back to `idhaya-perikai`; neither is a canonical work.
- **Validators:** `test:r3-identity` (1130 checks) gained an R3-C block, with 10 sabotage controls each proven to fail it
  (missing R3-C identity; wrong shelf; omitted OD8 Letter; OD8 Letter treated as Murasoli; omitted
  `thudikkum-ilamai-urai`; container kept canonical; eighth demotion; only one R3-C relation active; `poompuhar` promoted;
  an R3-D merged-witness activated early).
  - Earlier-wave validators were reconciled without weakening: Letters / Speeches / Essays counts add the derived R3
    terms; the Wave-6 essays test accepts a demoted publication only as its verbatim publication record;
    `validate-wave3-essays.mjs` reconciles unit promotion explicitly against `identity-manifest.json` and keeps "invents no
    edition / unitCount / rights"; `build-wave8-p4-publication --verify` stays byte-identical.

| Item | After R3-B | After R3-C |
|---|---|---|
| Published CREATE identities | 162 (87 dormant) | **249 (0 dormant)** |
| Canonical catalogue | 493 | **573** |
| Shelves (life / letters / fiction / poetry / drama / cinema / speeches / essays / lit. comm.) | 1/1/162/173/11/10/117/14/4 | **1/3/162/173/11/10/118/91/4** |
| `LIBRARY_PUBLICATIONS` | 4 | **11** (Poetry 3, Essays 8) |
| Relations | 49: 20 active / 29 dormant | 49: **22 active / 27 dormant** (all R3-D) |
| Collections | 9 | **9**, byte-identical to the pre-R3 boundary |
| Build | 5280 / 5275 | **5280 / 5275** |
| Sitemap | 5271 (`c65c6377…`) | **5271, same set** |

**`READ_IA_R3_CONTRIBUTION` (derived from the stage state, never typed):** works **+238** · Poetry **+159** · Essays &
Articles **+76** · Letters **+2** · Speeches **+1** · all other shelves 0 · collections 0 · build 0 · sitemap 0.

**R3-D remains fully dormant.** The 27 dormant relations are exactly R3-D: 5 `merged-witness`, 11 Sangatamil
(`commentary-section`) and 11 1958 `தேனலைகள்` (`external-publication`). All five `merged-witness` records are
`state: dormant`, `introducedIn: R3-D`. The five merge-source stories (`sirai-kodiyathu`,
`sorgaththirku-vandhathu-eppadi`, `neeyum-kaithi-naanum-kaithi`, `aadik-kaatre`, `pugazhe-nee-oru-pudhir`) remain canonical
Fiction works; every merge target — now including `sorgga-logaththil` — is canonical. Fiction stays 162; the 2004
collection and the dormant collection resolver are unchanged. **No merge has been performed.**

## 5. Production acceptance (read-only, `nenjukkuneethi.org`, deployment `6687856705`)

- **`/read`:** exactly **9** category cards — 1 · **3** · 162 · 7 collections · 173 · 11 · 10 · **118** · 2 collections ·
  **91** · 4. No new category or collection.
- **`/read/essays`:** **91** canonical work cards (91 unique) and exactly **8** Publication cards (`meesai-mulaiththa-vayathil`,
  `ina-muzhakkam`, `unarchchimaalai`, `thiraavida-sampaththu`, `kolaikkalam`, `sinthanaiyum-seyalum`, `perumoochu`,
  `thudikkum-ilamai`); none is a work card.
- **`/read/letters`:** exactly **3** work cards — `/murasoli`, `/essays/sinthanaiyum-seyalum/articles/paasiyum-thoosiyum`,
  `/essays/sinthanaiyum-seyalum/articles/athiga-uyaram-thaanduvatharku`; the corpus summary is present; no Publications
  section.
- **`/read/speeches`:** **118** work cards and exactly **2** collections; `thudikkum-ilamai-urai` is present, linking
  `/essays/thudikkum-ilamai/articles/thudikkum-ilamai`.
- **`/read/poetry`:** 173 work cards and 3 Publication cards (unchanged).
- **Card counting:** the four pages hold 173 + 91 + 3 + 118 = **385** canonical work cards; the three Ina fragment cards
  share one pathname, so they resolve to **383** distinct pages — not two missing cards.
- **Routes:** all **383** distinct card targets return 200; all 11 publication landings and all 11 `/source` routes return
  200; representative R3-C child readers return 200. Invalid examples return 404, including the invented
  `/letters/paasiyum-thoosiyum` and `/speeches/thudikkum-ilamai-urai`.
- **Witness UI:**
  - `/speeches/idhaya-perikai` shows exactly the two R3-C section notes (sections 3 and 4), each linking its witness unit;
    both units link back;
  - R3-B is intact: Anna and Thennan (with Idhayathai's 1975 scans 9–20), `gunanayagar-nehru` (Kavithaigal link + 1975
    scans 21–32), `oruthalaik-kathal` ↔ Kaalap, the Ina unit's 8 notes, `green-parrot` ↔ Meesai `பச்சைக்கிளி`, and Ina
    anchors `poem-6-1` … `poem-6-11`.
- **R3-D invisible:** no witness, merged-story, Sangatamil or 1958 UI on the five merge-source stories, the merge-target
  pages (including `sorgga-logaththil`), `oruthalaik-kathal` sections, or the Meesai 1958 targets. The 2004 collection page
  still lists 34 members, the five merge sources as ordinary story links.
- **Rendered change set:** comparing all 5271 sitemap pages' normalized HTML (script / link / asset references removed),
  the change relative to R3-B is exactly **6** server-rendered pages — `/read`, `/read/essays`, `/read/letters`,
  `/read/speeches`, `/essays/thudikkum-ilamai/articles/poompuhar`, `/essays/thudikkum-ilamai/articles/vetri-vilakku`. After
  deployment, Production equals the R3-C build on all 5271 pages. No promoted reader body or demoted publication body
  changed; `idhaya-perikai` receives its notes through the client-rendered `SpeechReader` path.
- **Structural invariants (merged tree):** 573 unique ids, slugs and href strings; the three Ina fragment works are the only
  shared pathname; no active witness locator equals a canonical href; all 20 DO_NOT_PROMOTE rows remain non-canonical.
- **Sitemap:** **5271** paths, 0 duplicates, 0 fragment entries; set hash **`c65c6377…`** — the pre-R3 set (0 added, 0
  removed). Build **5280** / **5275**, enforced by the merge CI.

## 6. Lifecycle

| Stage | Status |
|---|---|
| R0 · R1 · owner adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED |
| R3 | OWNER-AUTHORIZED ("let's start R3") |
| R3 PLAN | COMPLETE / REVIEWED / FROZEN (`#50` → `bab2fd4d…`) |
| R3-A | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#105` → `06731e0e…`; checkpoint `#51` → `c2a17f0a…`) |
| R3-B | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED (`#106` → `109e4bfd…`; checkpoint `#52` → `41f7e0cb…`) |
| **R3-C IMPLEMENTATION** | **COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED** (`pugazg/kalaignar-autobiography#107` → `afef75f9…`) |
| **R3-C CHECKPOINT (this record)** | **REVIEW-READY** |
| **R3-D** | **NOT STARTED** (the five merges, Sangatamil and 1958 relations remain dormant) |

**Next:** independent exact-head review and merge of this checkpoint. Only then **R3-D** (5 merges, 11 Sangatamil and 11
1958 relations; 573 − 5 → **568**), under the standing R3 authorization and its own exact-head review gate.
