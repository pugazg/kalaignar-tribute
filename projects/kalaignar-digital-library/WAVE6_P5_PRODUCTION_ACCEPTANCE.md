# Wave 6 — P5 Production Acceptance & Durable Control Close-Out

**Created:** 2026-09-17 · **Control-only record.** Implementation delta = **0**, source delta = **0**.
Live GitHub and production are authoritative; the SHAs below were re-fetched live before this record was written.

P5 is the independent production acceptance of the fully merged Wave-6 P1–P4 implementation plus the durable
control-state close-out. It made **no** implementation, payload, catalogue, collection, route, sitemap,
discovery, or source change. **P6 is NOT STARTED / NOT AUTHORIZED.**

---

## 1. Accepted implementation boundary

| Item | Value |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| Implementation `main` (P2–P4 squash merge of PR #87) | `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e` |
| Implementation `main` tree | `06c7ae8646ba85e61c973fecb5945ffbec256c39` |
| PR #87 | **MERGED / CLOSED**, `mergedAt` `2026-09-17T01:28:47Z`, squash SHA `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e` |
| Approved pre-merge head (immutable review) | `b34e05dcc27ba809e8f7c3743d2f4570614457eb` |
| Approved head tree | `06c7ae8646ba85e61c973fecb5945ffbec256c39` |
| Squash parent (single) | `171d7b373910ae16e5cbcc3d875b1b1e38e22d61` |
| **Approved-head-tree == merged-main-tree** | **PASS** (`06c7ae86…` == `06c7ae86…`) |

P1 was merged earlier via PR **#86**; P2–P4 via PR **#87**. No unreviewed implementation commit landed after PR #87.

## 2. Wave-6 population

| Segment | Works |
|---|---:|
| Batches 1–6 (cinema/drama/speeches/poetry/novels/essays) | 22 |
| Batch 7 (short stories) | 116 |
| **Total Wave-6 implemented works** | **138** |

`22 + 116 = 138`.

## 3. Final public surface (accepted)

| Metric | Value |
|---|---:|
| Catalogue — total published works | **216** |
| Catalogue — Fiction works | **157** |
| Non-empty shelves | 9 |
| Public collections | **6** |
| `STORY_SLUGS` (unique) | **154** |
| `/read` discovery entries | **77** |
| `/read` initially visible (cap 6) | **40** |
| Fiction discovery entries | **18** (over-cap → disclosure) |
| Sitemap URLs | **3909** |
| Sitemap duplicates | **0** |
| Build prerender routes | **3918** |
| Build `.html` files | **3913** |

### Collections (6)

| Collection | Members |
|---|---:|
| `1977-kalaignar-karunanidhiyin-sirukathaigal` (existing) | 37 |
| `2008-kalaignar-sonna-kathaigal` | 40 |
| `2004-kalaignarin-kuttik-kathaigal` | 34 |
| `1987-kalaignar-sonna-kuttik-kathaigal` | 25 |
| `1982-mudiyatha-thodarkathai` | 6 |
| `2009-16-kathaiyinile` | 16 |

## 4. Wave-6 route arithmetic (recorded durably)

```
Batches 1–6 routes           = 321
Batch 7 story routes         = 232   (116 stories × 2: reader + source)
Batch 7 collection routes    =   5   (2008, 2004, 1987, 1982, 2009 landings)
Total Wave-6 route delta      = 321 + 232 + 5 = 558
```

Consistent with the frozen pre-Wave-6 baselines:

```
prerender : 3360 + 558 = 3918
HTML      : 3355 + 558 = 3913
sitemap   : 3351 + 558 = 3909
```

Do not confuse LibraryWorks (216), collection membership, discovery entries (77), literary units, and public routes (558 Wave-6-contributed).

## 5. Production acceptance evidence

- **Production target:** `https://nenjukkuneethi.org`
- **Acceptance date:** 2026-09-17
- **Deployment/current-boundary proof:** production `/sitemap.xml` served **3909** URLs (3909 unique, 0 duplicates), matching the merged boundary; Batch-7-only routes (the five P4 collection landings and Batch-7 story reader+source pages) all returned HTTP 200 — production is serving the reviewed merged deployment.

### 5.1 Route sweep

- Expected Wave-6 route set, built from the committed manifests (`data/internal/wave6/p3-routes.json` cumulativeRoutes + `data/internal/wave6/b7-p3-routes.json` routes + the five `/collections/…` from `data/internal/wave6/b7-p4-integration.json`): **558**, unique **558**.
- Production result: **expected 558 · passed 558 (HTTP 200) · failed 0 · missing 0.**

### 5.2 Fail-closed (invalid routes → 404)

All returned **404**: `/stories/zzz-not-a-real-story`, `/stories/zzz-not-a-real-story/source`, `/collections/zzz-not-a-real-collection`, `/cinema/ammaiyappan/scene-999`, `/cinema/ammaiyappan/zzz`, `/plays/kagithapoo/zzz`, `/speeches/idhaya-perikai/zzz`, `/poems/aanthaiyum-arasanum/zzz`, `/novels/periya-idathup-pen/zzz`, `/essays/ina-muzhakkam/articles/zzz`. No redirect concealment.

### 5.3 `/read`

Production `/read`: all **9** shelves present; Fiction heading states **157 works** and **6 collections**; **6** collection cards; all **8** non-collection Batch-7 stories (`seerazhitha-sirippu`, `madurai-selavu`, `kondru-varuga`, `naattiya-kalarani`, `maanam`, `neruppu`, `vilaiyal-vangalaiyo`, `nanbana`) render as standalone discovery cards; **no** collection member is duplicated as its own card (verified across 2008/2004/2009/1982/1977 members); Fiction disclosure present; **6** `<details>` disclosures (Fiction now over-cap; the five other over-cap shelves unchanged).

### 5.4 Collection pages (6)

All HTTP 200 with exact member counts and no duplicates: 1977 = 37, 2008 = 40, 2004 = 34, 1987 = 25, 1982 = 6, 2009 = 16.
- **1987:** `jaadi-kutti-poduma` at source ordinal **2**, `kuruvi-rameswaram` at source ordinal **11**.
- **2009:** 16 members in exact 2009 source order; the collection-local page/scan extents are shown from the 2009 membership (e.g. `sumanthaval` pp. 59–76 / scans 64–81; `pugazhendhi` 77–84 / 82–89; `ayyo-raja` 169–177 / 174–182) — **not** the 1977 pages; the reprinted works' own provenance pages still pin the **1977** source (`76135e1b…`), so canonical provenance is not overwritten.

### 5.5 Plural membership

- `jaadi-kutti-poduma` — one LibraryWork, member of **2008 + 1987**.
- `kuruvi-rameswaram` — one LibraryWork, member of **2004 + 1987**.
- The eleven 1977 canonicals reprinted in 2009 remain single canonical works, members of both **1977 + 2009**, still textually controlled by their 1977 payload. Plural membership inflates neither catalogue work count (216) nor discovery entries (77).

### 5.6 P2 apparatus / interleaf

All nine P2-corrected stories (`kaasa-lesa`, `kondru-varuga`, `madurai-selavu`, `mudiyatha-thodarkathai`, `nandiyur-nariyappan`, `nariyur-nandiyappan`, `petra-pillaiyai-vitra-thaai`, `seemaan-veettu-seekkaali`, `seerazhitha-sirippu`) render apparatus-clean in production (0 hits for `Source-layout note` / `Historical-glyph gate` / `SOURCE-VISUAL CLOSED` / `intervening-non-story` / stage/fidelity annotations). `madurai-selavu`: Tamil stream excludes the scan-25 `intervening-non-story` interleaf, its genuine English scan-25 continuation is preserved, and no interleaf note is exposed. The merged-main P2 fidelity validator re-ran at **5347 checks / 0 failed** (exact Tamil + printed-page attribution, exact English source-marker anchors, 0 apparatus leaks).

### 5.7 Semantic restraint (regression, no regressions)

`oruthalaik-kathal` = one verse-novel / poetry publication with 11 source sections (not 11 poems); Ammaiyappan archival segments are not source-numbered scenes; Kagithapoo has no invented Scene 22/23; Thiruvalar has no invented act/scene numbering; Namathu Nilai has no fabricated single date; Idhaya Perikai / Palli Vazhkkai have no invented date or venue; 1975 Kaviyaranga keeps ordinals 01 / 02 / 04; Periya Idathup Pen = 7 archive sections (not 18); Pudhaiyal = 52 literary units / 54 direct routes; Kudumbaththin has no invented edition/year; Vedhanai remains a government `செய்தி`/message (not a speech); `nandiyur-nariyappan` and `nariyur-nandiyappan` remain distinct; `தேனலைகள்` and `நடுத்தெரு நாராயணி` remain excluded.

### 5.8 Production sitemap

`/sitemap.xml`: **3909** URLs, **0** duplicates. All **237** Batch-7 URLs present (232 story + 5 collection), **0** missing, **0** extra (production `/stories/` count = 308 = 154 × 2; `/collections/` count = 6).

## 6. Merged-main regression (read-only, exact pins)

Clean checkout of `main` `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e` (tree `06c7ae8646…`); Batch-7 validators run against the pinned source `7205a108…`, the 1977 collection/anthology validators against the pinned `76135e1b…`.

- `tsc --noEmit` (root + scripts): clean.
- `git diff --check`: clean; `git status` clean (tracked).
- Production build: **3918 prerender / 3913 HTML**.
- Suites green (0 failed): Batch-7 P1 source/control (1999) · Batch-7 P2 independent fidelity (5347) · Batch-7 P2 render/runtime (737) · Batch-7 P3 routes (710) · Batch-7 P4 integration **with source re-derivation** (2069) · 1977 short-story archive (ALL PASS) · source-linked collection validator (83) · historical Wave-6 P3 build (398) · historical Wave-6 Batches 1–6 P4 integration (166) · shelf-disclosure (90) · collections (258) · poetry-architecture (118) · Wave-6 B1–B6 · Wave-5 P2/P3/P4 cinema regression/integrity/UI · daily-kural · standalone-poem-ui · publication-ui · p3-publication-ui · publication-landing-copy · p4-witness integrity/UI · sitemap duplicate/set checks. **28/28 local suites passed.**
- `validator contract`: green on this exact tree in the exact-head CI run (`35170239750`); not re-run locally only because the other Wave-6 source repositories are not checked out in this workspace.

## 7. Exact-head CI

Library CI run **`35170239750`** (head `b34e05dc…`, identical tree to merged `main`): `typecheck • build` **SUCCESS** · `archival validators` **SUCCESS**, including 1977 short-story archive, `Collections — 1977 anthology declaration`, Batch-7 P1 source/control, Batch-7 P2 fidelity, Batch-7 P4 source-order re-derivation, and validator contract. Vercel deployment **SUCCESS**; Vercel Preview Comments **SUCCESS**; unresolved feedback **0**.

## 8. Immutability

| Repo | Boundary | Delta |
|---|---|---:|
| Implementation `pugazg/kalaignar-autobiography` | `main` `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e`, tree `06c7ae8646ba85e61c973fecb5945ffbec256c39` | **0** |
| Batch-7 source `pugazg/kalaignar-short-stories` | `main` `7205a10892d0b208df2617766844f480b6a2c798`, tree `1be34cc368fbc96ff72933a004a074ef840168ee` | **0** |

P5 created only this control record and the control-doc updates in `pugazg/kalaignar-tribute`. No implementation or source write occurred.

## 9. Decision

**WAVE-6 P5 PRODUCTION ACCEPTANCE — PASS.**

**P6 is NOT STARTED / NOT AUTHORIZED.** The next execution activity requires separate explicit owner direction.
