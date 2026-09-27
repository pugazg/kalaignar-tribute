# Reading Room IA v2 — R3 Close-out (Canonical-Work Promotion and Catalogue Reconciliation)

**Recorded:** 2026-09-27.

**Status: R3 PLAN — COMPLETE / REVIEWED / FROZEN. R3-A, R3-B, R3-C and R3-D — COMPLETE / REVIEWED / MERGED /
PRODUCTION-ACCEPTED. All four R3 checkpoints — COMPLETE / REVIEWED / MERGED. R3 IMPLEMENTATION — COMPLETE. This close-out
record — REVIEW-READY (awaiting independent exact-head review). R3 is not declared CLOSED until this record is reviewed
and merged. No R4, new wave or maintenance activity is authorized.**

This is the **control-only** final record of the R3 stage. It records implementation work that has already been
independently reviewed, merged and accepted on production, and it adds nothing to it.
- Implementation delta from this control activity = **0**.
- Source delta = **0**.
- Manual production mutation = **0**.

Every implementation merge reached production through the repository's existing Vercel Git integration (automatic deploy
of `main`). No manual deployment was made at any stage, and none was made for this close-out.

**Owner authorization (verbatim):** "let's start R3".

## 1. Frozen authority (unchanged by this record)

| Record | Role | Git blob at close-out base `8c451053…` |
|---|---|---|
| [`READING_ROOM_IA_V2_R3_PLAN.md`](./READING_ROOM_IA_V2_R3_PLAN.md) | the frozen R3 plan (`#50` → `bab2fd4d…`) | `f3325c0543d2e4d34b6a02dfa16034a63c7139fb` |
| [`READING_ROOM_IA_V2_RESOLVED_MANIFEST.json`](./READING_ROOM_IA_V2_RESOLVED_MANIFEST.json) | the frozen resolved manifest (owner adjudication `#44`) | `b7b3530d54ba9c354b43313eecd69e78e76a92b5` |
| [`READING_ROOM_IA_V2_R3A_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3A_CHECKPOINT.md) | R3-A record (`#51`) | `f2fb798b4933e27bf9841fea1479120bc7b9523c` |
| [`READING_ROOM_IA_V2_R3B_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3B_CHECKPOINT.md) | R3-B record (`#52`) | `2dc350c1480939d58361e542e3ebe59d3401bc19` |
| [`READING_ROOM_IA_V2_R3C_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3C_CHECKPOINT.md) | R3-C record (`#53`) | `750b77bae128525a8fd9c268c5e5392b66a5d088` |
| [`READING_ROOM_IA_V2_R3D_CHECKPOINT.md`](./READING_ROOM_IA_V2_R3D_CHECKPOINT.md) | R3-D record (`#54`) | `ca3e91de139e94501c54346b8dd2ac16812c64cd` |

Each checkpoint file keeps its reviewed "REVIEW-READY" wording, which its merge supersedes. None is edited here. The
vendored implementation copy of the resolved manifest (`data/internal/r3/*.frozen.json`) is the same blob `b7b3530d…`.

## 2. The four implementation stages

Every implementation PR was merged by a normal merge commit pinned to its independently approved exact head
(`--match-head-commit`); none was squashed, rebased or amended, and every merge tree equals its approved-head tree
(approved head → merge = 0 files).

| Stage | Implementation PR | Approved head | Merge (tree) | Head CI / merge CI | Production deployment | Control checkpoint |
|---|---|---|---|---|---|---|
| **R3-A** — identity and relation foundation (no public change) | `pugazg/kalaignar-autobiography#105` | `be1d6d4f8135fc73e5bf09c350269711639269ff` | `06731e0eaaa6f1228388add726204a2df694c649` (`5c2bf2c9…`) | `36232814181` / `36234184588` | `6677444493` | `#51` → `c2a17f0aa1481557c717429b3f4cf811a1875b48` |
| **R3-B** — Poetry promotions (+162, 4 publications demoted) | `#106` | `1826e54651c491cb8c090bd986ebbef6fc5ce4a8` | `109e4bfdc1dcff2a26c51a0cd566ca7799e14aeb` (`b65c5417…`) | `36257100065` / `36288951207` | `6687152070` | `#52` → `41f7e0cb5ca70894b0943363567f8a37c636771d` |
| **R3-C** — Essays / Letters / Speech promotions (+87, 7 demoted) | `#107` | `aeec6bdafba5d16793defe38099e4dd1a4fff57c` | `afef75f9eca8367c2905c0d080f5c1fd82729b04` (`6c4ad32a…`) | `36290571028` / `36293330835` | `6687856705` | `#53` → `39ada6b24973ca65b8ec68357b0a5f0cfbac48e4` |
| **R3-D** — five merges, Sangatamil, 1958 (final) | `#108` | `483bb2e45badbf846f61394abc6a1114f92b39b2` | `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853` (`cd1f1367be4320cff34c58db30be843708de650e`) | `36296338864` / `36297650051` | `6688540026` | `#54` → `8c451053b50093ce5f2fc622c576ac77b76a8f53` |

- **R3-D merge:** parents `afef75f9…` and `483bb2e4…`; approved head → merge = **0 files**; base → merge = exactly the three
  reviewed commits (`3732a560`, `79626f36`, `483bb2e4`) plus the merge, over 29 files (+539 / −104).
- **R3-D CI:** exact-head `Library CI` run `36296338864` — `typecheck • build` SUCCESS, `archival validators` SUCCESS. Merge
  CI run `36297650051` — SUCCESS / SUCCESS on the first attempt.
- **R3-D production:** Vercel deployment `6688540026`, the automatic Production deploy of `7fe9a4f0…`. Its read-only
  production acceptance is recorded in the merged R3-D checkpoint (§5) and is not repeated or re-run here.
- **Transient CI note (recorded in the stage checkpoints):** the `typecheck • build` job failed intermittently inside
  `next/font`'s Google-font loader before any validator ran — once at the R3-B review head and twice at the R3-C merge. Each
  time only the failed job was re-run on the same commit, with no code change, and it succeeded (R3-B head attempt 2; R3-C
  merge attempt 3). R3-D needed no re-run.

## 3. Final R3 arithmetic (frozen)

**Resolved manifest (authority):** 315 rows = CREATE **249** · KEEP_EXISTING **27** · ADD_WITNESS **19** · DO_NOT_PROMOTE
**20** · HOLD **0**.

**Final implementation (`main` `7fe9a4f0…`):**
- all **249** CREATE identities are canonical LibraryWorks, each exactly once, on their frozen shelf and subtype;
- **0** CREATE identities are dormant;
- all **20** DO_NOT_PROMOTE rows are non-canonical.

| Measure | Pre-R3 boundary | **Final** |
|---|---:|---:|
| Canonical catalogue | 335 | **568** |
| Life Writing | 1 | **1** |
| Letters | 1 | **3** |
| Fiction | 162 | **157** |
| Poetry | 14 | **173** |
| Drama | 11 | **11** |
| Cinema Writing | 10 | **10** |
| Speeches | 117 | **118** |
| Essays & Articles | 15 | **91** |
| Literary Commentary | 4 | **4** |
| Publication records | 0 | **11** (Poetry 3, Essays & Articles 8) |
| Collections | 9 | **9** (byte-identical) |

`1 + 3 + 157 + 173 + 11 + 10 + 118 + 91 + 4 = 568` — the frozen plan's §6.5 final (`335 + 249 − 11 − 5`).

**`READ_IA_R3_CONTRIBUTION` (derived from the stage state and active relations, never typed):** works **+233** · Fiction
**−5** · Poetry **+159** · Essays & Articles **+76** · Letters **+2** · Speeches **+1** · all other shelves 0 · collections
0 · build 0 · sitemap 0.

**The 11 publication records** (not canonical works; every landing, reader and `/source` kept; each its former record
verbatim minus `state`): R3-B — `kaalap-pezhaiyum-kavithai-saaviyum`, `kalaignarin-kavithaigal`,
`kalaignarin-kaviyaranga-kavithaigal-1975`, `meesai-mulaiththa-vayathil`; R3-C — `ina-muzhakkam`, `unarchchimaalai`,
`thiraavida-sampaththu`, `kolaikkalam`, `sinthanaiyum-seyalum`, `perumoochu`, `thudikkum-ilamai`.

## 4. The five canonical merges (frozen)

| Legacy story | 2004 ordinal | Canonical work |
|---|---:|---|
| `neeyum-kaithi-naanum-kaithi` | 2 | `piraiye` |
| `sorgaththirku-vandhathu-eppadi` | 14 | `sorgga-logaththil` |
| `aadik-kaatre` | 17 | `adikkaatru` |
| `sirai-kodiyathu` | 20 | `green-parrot` |
| `pugazhe-nee-oru-pudhir` | 23 | `pugazh` |

- The five legacy ids are **no longer canonical LibraryWorks**; each is exactly one **active `merged-witness`** record,
  carrying its former LibraryWork record verbatim.
- All five `/stories/<slug>` routes and all five `/stories/<slug>/source` routes remain public; **no redirect** was
  introduced; story payloads are unchanged.
- The 2004 anthology `2004-kalaignarin-kuttik-kathaigal` retains all **34** printed members at their original ordinals;
  `LIBRARY_COLLECTIONS` is byte-identical to the pre-R3 registry, and no member was repointed.

## 5. Final relation census (frozen)

**49** relations — **49 active**, **0 dormant**.

| Class / level | Records |
|---|---:|
| source-publication / work | 20 |
| source-publication / section | 2 |
| merged-witness / work | 5 |
| commentary-section / section | 11 |
| external-publication / chapter | 10 |
| external-publication / publication | 1 |
| **Total** | **49** (source-publication 22 · merged-witness 5 · commentary-section 11 · external-publication 11) |

Every active relation targets a published canonical work. The registry is the single generated authority
(`data/internal/r3/relations.json`); no second registry exists.

## 6. Sangatamil (frozen treatment)

- Sangatamil remains exactly **one** Literary Commentary LibraryWork; **0** Sangatamil sections are LibraryWorks.
- Sections **092–102** map one-to-one to `oruthalaik-kathal` sections **1–11**.
- The **canonical side** displays the relations: the `oruthalaik-kathal` landing lists all eleven (with its existing
  Kaalap witness) and each section page its one.
- The **Sangatamil side** displays **no reverse relation UI**; `/sangatamil` and its 104 section pages are otherwise
  unchanged, and no Sangatamil payload or source text changed.

## 7. The 1958 `தேனலைகள்` (frozen treatment)

- **10 chapter-level** mappings: அலை 2 → `mayiliragu` · 4 → `madal` · 5 → `thozhi` · 6 → `maruthaani` · 7 → `aruvi` ·
  8 → `muram` · 9 → `yaazh` · 10 → `sirpi` · 11 → `seval-sandai` · 12 → `aandu-vizha`.
- **1 publication-level** relation: `thenalaigal` ↔ the 1958 book as a whole. **அலை 1** («முத்தாரம்») is
  publication-level only; no chapter equivalence is asserted.
- **அலை 3 `முத்துமாலை` remains unmapped.**
- The 1958 publication has **no public route**, is **not a LibraryWork** and is **not ingested**.

## 8. Route, build and sitemap boundary (frozen)

- **Build:** 5280 prerendered / 5275 HTML — unchanged from the pre-R3 boundary.
- **Sitemap:** 5271 paths, set hash `c65c63775fc684afd6e70c842b67ac366ceb42c7f267055a19602ce4da1fb2b3` — the pre-R3 set.
- No route was added, removed or redirected across R3; there are no fragment sitemap entries; the five legacy story routes
  (and their `/source`) are preserved.
- **Canonical href contract:** 568 unique ids, slugs and href strings; the only shared pathname is the declared Ina
  fragment cohort (`ina-muzhakkam-poem-04`, `-07`, `-08` on `/essays/ina-muzhakkam/articles/kavithaigal`).

## 9. Source boundary (re-fetched 2026-09-27, unchanged)

| Source repository | Head |
|---|---|
| `pugazg/kalaignar-poems` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` |
| `pugazg/kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` |
| `pugazg/kalaignar-essays` | `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` |
| `pugazg/kalaignar-short-stories` | `7205a10892d0b208df2617766844f480b6a2c798` |

**Source delta across R3 = 0.** No source repository was modified and nothing was ingested.

## 10. No post-R3 work (verified before this record was committed)

- Implementation `main` is still `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853`; control `main` was `8c451053…`.
- **0 open PRs** in `pugazg/kalaignar-autobiography`, `pugazg/kalaignar-tribute` and the four source repositories — no R4
  implementation PR, no new wave PR and no maintenance PR.
- Existing historical R3 branches are not new work; none was deleted.

## 11. Lifecycle

| Stage | Status |
|---|---|
| R0 · R1 · owner adjudication | COMPLETE / REVIEWED / FROZEN |
| R2 | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED |
| R3 | OWNER-AUTHORIZED ("let's start R3") |
| R3 PLAN | COMPLETE / REVIEWED / FROZEN |
| R3-A · R3-B · R3-C · R3-D | COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED |
| R3-A · R3-B · R3-C · R3-D checkpoints | COMPLETE / REVIEWED / MERGED (`#51`, `#52`, `#53`, `#54`) |
| **R3 IMPLEMENTATION** | **COMPLETE** |
| **R3 CLOSE-OUT (this record)** | **REVIEW-READY** |
| **R3** | **Not yet declared CLOSED** — only on the independent review and merge of this record |
| R4 / new wave / maintenance | **NOT AUTHORIZED** |

**Next:** independent exact-head review and merge of this close-out. Only then is R3 CLOSED. Any further work requires
explicit new owner authorization.
