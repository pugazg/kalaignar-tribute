# Wave 8 — P5 Production Acceptance & Durable Control Close-Out

**Created:** 2026-09-24 · **Control-only record.** Implementation delta = **0**, source delta = **0**,
production mutation = **0**. Live GitHub and production are authoritative. Every SHA and count below was
re-fetched or re-derived live before this record was written. Production was read with GET requests only.

P5 is the independent production acceptance of the fully merged Wave-8 implementation (P1–P4, PRs #97–#101) and
the durable control close-out. It made **no** change to implementation, payloads, catalogue, collections, routes,
sitemap, discovery, source or production.

**Decision: WAVE-8 P5 PRODUCTION ACCEPTANCE — PASS. WAVE 8 COMPLETE / CLOSED / FROZEN AT P5. There is no
Wave-8 P6.**

As *current programme state*, this record supersedes the "WAVE 8 P1 — NOT STARTED / NOT AUTHORIZED" status of
[`WAVE8_COMPLETED_WORKS_CENSUS.md`](./WAVE8_COMPLETED_WORKS_CENSUS.md). That status was true when P0 froze. The
census is **not** rewritten and remains the historical selection and readiness authority. Its P0 projection
(catalogue 333 → 335, Letters 1 → 1, Drama 10 → 11, Literary Commentary 3 → 4, collections 9) is now
**realized** and is confirmed below.

---

## 1. Accepted implementation boundary

| Item | Value |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| **Accepted implementation `main`** | **`f991043c3353abe9f2b334f7c8d57e433184d126`** (merge of PR #101) |
| **Accepted tree** | **`87ca371b084c337ba2163caa6c336615174074e9`** |
| Parents | `d04093e42c4e631620218e18802f15e0ca923ccf` (P3 merge) · `42cfdf79fe001cd7588d7c30a6b1a193e0233703` (approved P4 head) |
| Commits on `main` after #101 | **0** (compare `f991043c…...main` = identical, ahead 0 / behind 0) |
| Open implementation PRs at acceptance | **0** |
| Control base for this record | `pugazg/kalaignar-tribute` `main` `03bd9159e32f94b2d507dcef94b94f95f9210629`, tree `f2cdb39390343a1c44e63199575d4b10624c3f01` |
| Open control PRs at acceptance (before this one) | **0** |
| Production | `https://nenjukkuneethi.org` — Vercel **Production** deployment `6638432286` for `f991043c…`, state **success** |

The P5 regression checkout was a clean, detached worktree at exactly `f991043c…`. Its tree recomputed to
`87ca371b…`, which equals live `main`.

## 2. Wave-8 implementation PR / merge boundaries (#97–#101)

Each PR below was re-fetched live and is **MERGED**. Each was independently reviewed at its exact head and merged
only at that head, as a normal merge commit whose second parent is the approved head.

| PR | Stage | Title | Approved head | Merge commit | Merged (UTC) |
|---|---|---|---|---|---|
| #97 | P1 | Wave 8 P1 — hidden data foundation (Murasoli 42–47, Ore Mutham, Sangath Tamil) | `fb8405ae6f09d3af9f852d8d0acc7e659a4c73c7` | `893408a85e194f19c25085dc2e29a6042ef44820` | 2026-09-24T04:09:36Z |
| #98 | P1 correction | Wave 8 P1 correction — prevent Sangath Tamil ornaments entering provenance runs | `c01e501bbda1546ba05d79990ed3558f5ef91095` | `b53a1c3b43bff6564cb40f177dabf2ec782f784b` | 2026-09-24T07:56:39Z |
| #99 | P2 | Wave 8 P2 — fidelity and hidden reader layer | `945cd05c8eab670063771b085c2259d39f665755` | `e1086f3d1e4b254621d6fea05bc879848203d323` | 2026-09-24T09:13:01Z |
| #100 | P3 | Wave 8 P3 — direct hidden routes | `8bccb83df7176406bfdd950059b59a9f97efb59c` | `d04093e42c4e631620218e18802f15e0ca923ccf` | 2026-09-24T11:23:59Z |
| #101 | P4 | Wave 8 P4 — publish Murasoli 42–47, Ore Mutham and Sangath Tamil | `42cfdf79fe001cd7588d7c30a6b1a193e0233703` | **`f991043c3353abe9f2b334f7c8d57e433184d126`** | 2026-09-24T13:01:32Z |

- **PR #98** is the corrective part of P1. It is inside the accepted Wave-8 boundary and is not a new work.
- **PR #101's approved head** includes the final truthfulness correction `42cfdf79`:
  - the Murasoli model comments state that the printed number is neither identity nor unique;
  - the Drama public-provenance success output reports **11 Drama `/source` pages**, a figure derived from the data.

## 3. Frozen Wave-8 source pins (not repinned)

P5 fetched each pin **by SHA** into a disposable directory, read-only, and wrote nothing to any source repository.

| Segment | Repository | Frozen pin | Tree | Work / volume subtrees |
|---|---|---|---|---|
| B1 Murasoli 42–47 | `pugazg/kalaignar-murasoli-letters` | `bd0bb7904c85bdbfe05aa4970ac098d701a6967f` | `ff604c584ab05d0d769abe4a0c685b79a7a79e5b` | see below |
| B2 ஒரே முத்தம் | `pugazg/kalaignar-stage-plays` | `521fe5452e3e9ed54baa81e672325ce6ba501c5e` | `cea50efb13baf27390b794b39b76b039a9ccaead` | `works/ore-mutham` `0839c6efc7bfd41fd11d30db3a46b0a2b3c901e6` |
| B3 சங்கத் தமிழ் | `pugazg/kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` | `2302d1fc6cbe9386a8010b344a9caba2f4913fa4` | `works/sangatamil` `25231d62c62e22228a248fd2976e0ee9c43939c1` |

Murasoli volume subtrees at the frozen pin, re-read live. Each equals the P0/P1 authority.

| Volume | Subtree |
|---|---|
| `volumes/volume-42` | `0bb4cfe677badd63fb0fbf5b66ea0fae9897339d` |
| `volumes/volume-43` | `35162a6263ed7e9eb7aba872008f86d1d185ee2c` |
| `volumes/volume-44` | `b9142e10a44df2e58d365066de098ffa4a9c351d` |
| `volumes/volume-45` | `9efc967a226b519888fa3cf9af4eca6b8c70a5c7` |
| `volumes/volume-46` | `f111d393681b384aed7c288353a16931ca083fb0` |
| `volumes/volume-47` | `71998ba7bcc3aa0d800a44bcd89d9d61c09c7a7f` |

**Source-main drift (context only; not drift for the Wave-8 cohort):**
- `kalaignar-murasoli-letters`: live `main` has moved to `d16db3e4c435cb063d155f8e9a5b9e62b12317fe`, whose latest
  commits are Volume 41 transcription.
  - The six Volume 42–47 subtrees are **identical** at live `main` and at the frozen pin.
  - Wave 8 stays pinned to `bd0bb790…`. A moving source `main` is never a reason to reopen Wave 8.
- `kalaignar-stage-plays` and `kalaignar-literary-commentary`: live `main` still equals the frozen pin.
- All three source repositories have **0** open PRs.

## 4. Wave-8 population and identity semantics

Wave 8 consisted of **8 source publication inputs** (Murasoli Volumes 42, 43, 44, 45, 46, 47; ஒரே முத்தம்;
சங்கத் தமிழ்). Those inputs produced only **+2 canonical LibraryWorks**, so Wave 8 is never "8 works".

| Segment | Result | LibraryWork delta |
|---|---|---:|
| B1 — Murasoli Volumes 42–47 | Coverage expansion of the **existing** `murasoli-letters` work; **342** new letter records | **0** |
| B2 — ஒரே முத்தம் | `ore-mutham` — exactly one new **Drama** LibraryWork | **+1** |
| B3 — சங்கத் தமிழ் | `sangatamil` — exactly one new **Literary Commentary** LibraryWork | **+1** |
| **Total** | | **+2** (catalogue 333 → 335) |

Collections delta = **0**.

**Murasoli identity rule:** a letter's identity is its route id, not its printed number. Printed numbers are
carried exactly as printed and are not unique (§11).

## 5. Final catalogue and shelf census

Re-derived from merged `main` (the Library CI "Reading Room collections" and "shelf disclosure" steps, and P4
integration) and from the production `/read` shelf headings (§6). The two sources agree.

| Shelf | Pre-Wave-8 | Final | Δ |
|---|---:|---:|---:|
| Life Writing | 1 | 1 | 0 |
| Letters | 1 | 1 | 0 |
| Fiction | 162 | 162 | 0 |
| Poetry | 14 | 14 | 0 |
| Drama | 10 | **11** | +1 (`ore-mutham`) |
| Cinema Writing | 10 | 10 | 0 |
| Speeches | 117 | 117 | 0 |
| Essays & Articles | 15 | 15 | 0 |
| Literary Commentary | 3 | **4** | +1 (`sangatamil`) |
| **Total** | **333** | **335** | **+2** |

- `LIBRARY_WORKS` holds 335 entries, all `state: "published"`, with **335** unique ids and **335** unique slugs.
  This was checked directly on the accepted tree, and P4 integration (121 / 0) re-derives it independently.
- Collections, checked directly on the accepted tree, are exactly:
  - the six pre-Wave-7 collections: `1977-…`, `1982-…`, `1987-…`, `2004-…`, `2008-…`, `2009-16-kathaiyinile`;
  - `arumbu-1978`, `muthukkuliyal-part-1`, `muthukkuliyal-part-2`.
- There is exactly one Letters LibraryWork, `murasoli-letters`. Its description now reads "— Volumes 42–54" and
  its coverage stays partial / partial.
- `ore-mutham` appears exactly once:
  - shelf Drama, subtype `stage-play`, Tamil and English complete;
  - `unitCount` 33, labelled "scenes (30 + 3 in the comedy section)".
- `sangatamil` appears exactly once:
  - shelf Literary Commentary, reader structure **`commentary-unit`** (never `kural-commentary`);
  - Tamil **partial** and English **partial**, because the permanently source-limited scan 8 is description-only;
  - `unitCount` 104, labelled "reading sections".

## 6. Collections and discovery census

- **Collections: 9** (unchanged; Wave 8 adds no collection).
- **Production `/read`** (`https://nenjukkuneethi.org/read`, HTML fetched 2026-09-24):

| Shelf | Works (heading) | Discovery entries | Initially visible |
|---|---:|---:|---:|
| Life Writing | 1 | 1 | 1 |
| Letters | 1 | 1 | 1 |
| Fiction | 162 | 20 | 6 |
| Poetry | 14 | 14 | 6 |
| Drama | 11 | 11 | 6 |
| Cinema Writing | 10 | 10 | 6 |
| Speeches | 117 | 22 | 6 |
| Essays & Articles | 15 | 15 | 6 |
| Literary Commentary | 4 | 4 | 4 |
| **Total** | **335** | **98** | **42** |

- Discovery went 96 → **98**, and initially visible went 41 → **42**. Drama was already at its cap of 6, so only
  Literary Commentary (3 → 4) adds a visible card.
- There is exactly **one** Murasoli card (`/murasoli`), and **0** `/murasoli/…` volume or letter cards.
- `/plays/ore-mutham` sits on the Drama shelf, and there are 0 `/plays/ore-mutham/…` cards (no supplementary-part
  card).
- `/sangatamil` sits on the Literary Commentary shelf, and there are 0 `/sangatamil/…` section cards.
- **Sangatamil card** (production): *"… 102 பகுதிகள்; ஸ்கேன் 8-இன் கையெழுத்து முன்னுரைக் கடிதம் மூலத்தின் நிலையான
  வரம்புடையது — படியெடுக்கப்படவில்லை"*. It carries the permanent scan-8 limitation.
- **Ore Mutham card** (production): *"மேடை நாடகம்: 30 காட்சிகள்; அதன்பின் தனித் தலைப்புடைய நகைச் சுவைப் பகுதி. —
  அதன் காட்சிகள் 1–3 தனியாக எண்ணிடப்பட்டவை"*. It states 30 scenes plus a separately numbered 3, never a
  sequential 33.

## 7. Wave-8 route arithmetic = 483

The route set was reconstructed from the committed, frozen P3 manifest
`data/internal/wave8/wave8-p3-routes.json` in the accepted tree. It was not hand-typed.

| Family | Composition | Routes |
|---|---|---:|
| Murasoli | 342 letter readers (`/murasoli/m42-…` … `/murasoli/m47-…`) | **342** |
| Ore Mutham | landing + `/source` + 30 `main-NN` + 3 `nagai-suvai-NN` | **35** |
| Sangatamil | landing + `/source` + 104 reading sections | **106** |
| **Total** | 483 unique, no duplicates | **483** |

```
342 + 35 + 106 = 483
sitemap   : 4779 + 483 = 5262
prerender : 4788 + 483 = 5271
html      : 4783 + 483 = 5266
generated static pages : 4791 + 483 = 5274
```

**P3 created these 483 routes, direct but undiscovered. P4 published the same 483 routes**, adding catalogue,
discovery and sitemap exposure. **P4 added zero build routes**: build totals are identical at the P3 and P4
merges. The P3 manifest was left frozen as the P3 record. P4's own record is
`data/internal/wave8/wave8-p4-publication.json`.

## 8. Production deployment evidence

- **GitHub deployment:** `6638432286`, environment **Production**, sha `f991043c…`, created
  2026-09-24T13:05:36Z, latest status **success**.
  - It is the most recent Production deployment (the previous two were `6636647120` for `d04093e4` and
    `6634338716` for `e1086f3d`).
- **Vercel commit status:** `Vercel` = **success**, "Deployment has completed". The Vercel deployment reference is
  `rain-drops/kalaignar-autobiography/4nWTKRiP6iujd6NGukPEyhN3pgrn`, deployment URL
  `kalaignar-autobiography-4lcnh3ehn-rain-drops.vercel.app`.
- **Production is served by Vercel:** `server: Vercel`, edge region `bom1`, `x-vercel-cache: HIT`.
- **Production serves the accepted surface:** every figure in §6, §9–§15 was measured on
  `https://nenjukkuneethi.org` and matches the merged-main build exactly (5262-URL sitemap, the 42–54 Murasoli
  indexes, 98/42 discovery).
- **Acceptance window:** production sweeps ran 2026-09-24 between 13:39Z and 13:42Z.

## 9. Full 483-route production sweep

- **Mechanism:**
  - a read-only Node `fetch` harness requested every route in the committed P3 manifest from
    `https://nenjukkuneethi.org`, 8 at a time, with `redirect: "manual"` (a 3xx counts as a failure and is never
    followed);
  - a second pass requested every route with `RSC: 1`.
- **HTML result: expected 483 · passed 483 (HTTP 200) · failed 0 · missing 0 · redirects 0** (50,767,731 bytes).
- **RSC result:** 483 × HTTP 200 with `content-type: text/x-component` · 0 failed (32,755,216 bytes).
- **Positive controls**, 483 / 483 in HTML and 483 / 483 in RSC: every response contains its own route's last path
  segment. Every HTML response also carries its family's render marker:
  - Murasoli `data-testid="wave8-letter-body"`;
  - Ore scenes `data-testid="play-part"`, Ore landing `play-part-group`;
  - Sangatamil sections `sangatamil-section`, Sangatamil source `sangatamil-source`.

## 10. Invalid-route 404 sweep

All **10** returned a genuine **HTTP 404**, requested with redirects not followed. None redirected to a landing.

| Route | Status |
|---|---|
| `/murasoli/m42-l3377` | 404 |
| `/murasoli/m46-l3636` | 404 |
| `/murasoli/m46-l3644` | 404 |
| `/murasoli/m46-l3645` | 404 |
| `/murasoli/m46-l3646` | 404 |
| `/plays/ore-mutham/31` | 404 |
| `/plays/ore-mutham/main-31` | 404 |
| `/plays/ore-mutham/nagai-suvai-04` | 404 |
| `/sangatamil/105-extra` | 404 |
| `/sangatamil/section-1` | 404 |

## 11. Murasoli production acceptance

Production `/data/murasoli/index.json` and `/data/murasoli/letters-index.json` were fetched directly, and every
figure below was re-derived from them.

- **Volumes:** exactly `42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54`, in that order in both indexes.
  `volumeCount` is **13**.
- **Letters:** **688** in total, with **688 unique route ids**.

| Vol | 42 | 43 | 44 | 45 | 46 | 47 | 48 | 49 | 50 | 51 | 52 | 53 | 54 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Letters | 64 | 56 | 53 | 55 | 55 | 59 | 58 | 53 | 50 | 49 | 50 | 50 | 36 |

- **Wave-8 (42–47) 342 + legacy (48–54) 346 = 688.**
- **Physical pages:** Wave-8 **2409** + legacy **2732** = **5141**. This equals `totalPages`.
- **Legacy 48–54 entries** in both indexes are **unchanged**, byte-for-byte as JSON, relative to the accepted P3
  boundary `d04093e4…`.
- **Public metadata safety:**
  - Wave-8 letter entries carry only `id`, `number`, `date`, `title`, `pages`, `pageCount`.
  - `pages` is empty for all 342, so no legacy page ids were invented.
  - Wave-8 volumes carry `textProvenance: "source-verified-page-records"`.
  - No hidden P1 workflow or fidelity field appears (§18).
- **Numbering anomalies are preserved and accepted.** The printed number is not identity.
  - Vol 42: printed **3154** sits between **3376** and **3378**, and there is **no 3377**.
  - Vol 46: two distinct printed **3637** records, `m46-l3637-indre-selga-inithe-velga` and
    `m46-l3637-en-uyirinumelana-anbu-udanpirappukkale`.
  - There is **no 3636** and no **3644–3646**.
  - Printed **3647, 3648, 3649** each appear once in Vol 46 (`m46-l3647…9`) and once in Vol 47 (`m47-l3647…9`), as
    independent records.
- **Letter 3681** (`m47-l3681`):
  - the index lists printed number 3681 with `pageCount` **4** (its surviving source pages only);
  - the production page renders printed pages 248–251 only and exposes the permanent source-condition notice
    (`data-testid="source-condition"`, `data-missing-printed-pages="252"`);
  - printed page **252** is absent;
  - there is no reconstruction and no fabricated closing or signature.
- **Representative pages** `/murasoli/m42-l3364`, `/murasoli/m42-l3154`, both Vol-46 3637 routes,
  `/murasoli/m47-l3681` and `/murasoli/m48-l3706` all returned **200**.
- **Boundary navigation:** `m47-l3705 → m48-l3706` and `m48-l3706 → m47-l3705` are both present on production.
  42–54 is one published collection within the one `murasoli-letters` work.

## 12. Ore Mutham production acceptance

- The production identity is `/plays/ore-mutham`. The landing and `/source` both return **200**.
- **35 routes** = landing + source + 33 reading units:
  - main scenes `main-01`…`main-30` (1–30);
  - the separate **`நகைச் சுவைப் பகுதி.`** with supplementary scenes `nagai-suvai-01`…`03` (1–3).
- `/plays/ore-mutham/main-30` renders *காட்சி 30 / 30* and links to `/plays/ore-mutham/nagai-suvai-01`.
- `nagai-suvai-01` renders *நகைச் சுவைப் பகுதி. · காட்சி 1 / 3*. None of the 35 Ore pages numbers a scene 31, 32 or 33.
- There is exactly one Drama work, and no supplementary-part card appears on `/read`.
- **Rights scope.** The production `/source` rights block applies to `underlying-work-authored-by-kalaignar` and
  states:
  - *"Nationalisation applies to Kalaignar's underlying authored play."*
  - *"It does NOT extend to the edition's publisher/imprint matter …"*
  - the project-created English layer *"is not covered by the nationalisation of the Tamil work."*

## 13. Sangatamil production acceptance

- `/sangatamil` and `/sangatamil/source` return **200**, and all **104** section routes return 200. Wave-8
  Sangatamil therefore totals **106** routes.
- **Structure:** **104 reading sections** = `000-front-matter` + **102 literary sections** + `103-back-matter`.
  The two figures are not conflated: the catalogue card says 102 பகுதிகள், and `unitCount` is 104 reading sections.
- There is exactly one Literary Commentary work, with reader structure `commentary-unit`.
- **Printed source citations are distinct** from Kalaignar's text. On `/sangatamil/001-malarmari-pozhiginren`, the
  verse carries `data-role="quotation"` and the printed citation carries `data-role="source-citation"`.

## 14. Source-condition / qualification acceptance

Both permanent qualifications are visible and honest on production. They are **accepted source conditions, not
unfinished P5 work**.

- **Murasoli 3681 — source-incomplete.** Printed page 252 is missing and is never reconstructed. The notice is
  present and page 252 is absent (§11).
- **Sangatamil scan 8 — permanent source-limited handwritten foreword.**
  - `/sangatamil/000-front-matter` carries the scan-8 block with `data-role="source-limited"`: *"இப்பக்கத்திலுள்ள
    முழுப்பக்கக் கையெழுத்துக் கடிதம் படியெடுக்கப்படவில்லை; அதன் சொற்கள் இங்கு தரப்படுவதில்லை. இது இவ்வெளியீட்டின்
    நிலையான முடிவு."*
  - The word "pending" does not appear on the page.
  - The foreword is not reconstructed.
  - Catalogue coverage stays Tamil partial / English partial.

## 15. Production sitemap

Production `https://nenjukkuneethi.org/sitemap.xml` (HTTP 200):

- **5262** URLs, **5262** unique, **0** duplicates.
- **Exact-set comparison** against the committed P3 manifest: expected **483**, present **483**, missing **0**.
  - Family set equality: Murasoli **342 / 342**, Ore Mutham **35 / 35**, Sangatamil **106 / 106**.
  - **0** Wave-8-shaped URLs appear outside the manifest.
- Removing the 483 Wave-8 routes leaves exactly **4779** URLs, equal to the pre-Wave-8 accepted boundary.

## 16. Merged-main regression (read-only, exact pins)

**Checkout.** A clean, detached worktree at `f991043c…`, with tree `87ca371b…` recomputed. Tracked status was
clean before and after the runs.

**Source checkouts.**
- The Library CI steps were run locally, verbatim, from `.github/workflows/library-ci.yml`. `npm ci` was the only
  step skipped, because `node_modules` is a shared checkout.
- The pinned source archives were earlier-wave checkouts.
- The Wave-8 frozen pins were freshly fetched by SHA from the committed P1 manifest, exactly as CI does.

**Hygiene and build.**
- `git diff --check`: clean. `tsc --noEmit`: clean.
- Production build: **5274 / 5274** static pages generated · **5271** prerender routes · **5266** HTML.
- The non-fatal `Newsreader` font-override notice is pre-existing, and the build exits 0.

**`typecheck • build` job, run locally: 50 / 50 steps pass (0 failed).** Wave-8 results:

| Check | Result |
|---|---|
| Wave 8 P1 hidden | **106 checks / 0 failed** |
| Wave 8 P2 render | **12,183 / 0** |
| Wave 8 P3 route manifest | `wave8-p3-routes.json` verified **byte-identical** (deterministic regeneration) |
| Wave 8 P3 routes | **914 / 0** |
| Wave 8 P4 publication generator | Murasoli indexes + publication record verified **byte-identical** |
| Wave 8 P4 integration | **121 / 0** |
| Wave 8 P4 UI | **40 / 0** |
| Drama public provenance | **172 / 0**, output *"11 Drama /source pages: archival P1 records retained · projection allowlisted …"* |

Every earlier-wave regression step also passes in this job. Examples:
- Reading Room collections: *"335 works · 9 collection · 98 discovery entries · Fiction 162 works / 20 entries"*.
- Shelf disclosure: *"335 works across 9 shelves · 98 discovery entries · 42 initially visible · 6 disclosures"*.
- Wave-6 B2 drama 273 / 0 · Wave-6 B5 novels 179 / 0 · Wave-6 B6 essays 135 / 0.
- Wave-7 B5/B6/K P1 hidden 215 / 0.
- Poetry witness integrity and UI.

**`archival validators` job, run locally: 37 / 37 steps pass (0 failed).** Wave-8 results:

| Check | Result |
|---|---|
| `import-wave8 --verify` against the freshly fetched frozen pins | *"8 artifacts + manifest byte-identical to a fresh regeneration from the frozen pins"* |
| Wave 8 P2 independent source fidelity | *"PASS — 71000 checks (PRESENCE → STRUCTURE → EQUALITY against the frozen sources)"* |

Earlier-wave results in this job:
- every earlier source-pin validator (ALL PASS);
- Wave-6 B6 essays 2823 / 0 · Wave-6 B5 novels 5813 / 0;
- Wave-7 B2–B4 P2 2550 / 0 · Wave-7 B5/B6/K P2 6465 / 0;
- B5/B6/K `--verify` 310 files + manifest byte-identical;
- validator contract upheld.

## 17. Exact merged-main CI

Checks for `f991043c3353abe9f2b334f7c8d57e433184d126` were re-fetched live.

| Check | Result |
|---|---|
| Library CI run `36002868420` (push, `main`) — `typecheck • build` | **SUCCESS** (completed 2026-09-24T13:05:14Z) |
| Library CI run `36002868420` — `archival validators` | **SUCCESS** (completed 2026-09-24T13:02:46Z) |
| Vercel (commit status) / GitHub Production deployment `6638432286` | **SUCCESS** |
| Combined commit status | **success** |

The exact-head PR CI for #101 was run `36001215733` on the approved head `42cfdf79…`, whose tree `87ca371b…` is
identical to merged `main`. Its result: **SUCCESS**.

## 18. Public serialization safety

**Scope.** All **483** Wave-8 production responses were scanned as HTML (483) **and** RSC (483), together with the
two public Murasoli index JSON files: **968 payloads** in total.

**What the scan looks for.**
- Serialized property keys (`"key":` or `\"key\":`): `releaseState`, `currentCheckpoint`, `verification`,
  `provenanceIds`, `tamilStatus`, `englishStatus`, `visualFidelity`, `locatedBy`, `sourceTree`, `repoTree`,
  `readiness`.
- The text `hidden foundation`.
- Keys are matched only in serialized-key form. Ordinary prose words such as "source" or "verified" are therefore
  not flagged.

**Detector positive control.** The same detector, run over the 12 hidden internal Wave-8 JSON files in the
accepted tree, fires on `currentCheckpoint`, `englishStatus`, `locatedBy`, `provenanceIds`, `releaseState`,
`repoTree`, `sourceTree`, `tamilStatus`, `verification`, `visualFidelity`. This proves it detects the hidden
shape.

**Page positive controls.** 483 / 483 HTML and 483 / 483 RSC responses were confirmed to be the page for their own
route (§9).

**Result: 0 leaks on 968 payloads.**

## 19. Immutability / delta table

| Repo / surface | Boundary | Delta |
|---|---|---:|
| Implementation `pugazg/kalaignar-autobiography` | `main` `f991043c3353abe9f2b334f7c8d57e433184d126`, tree `87ca371b084c337ba2163caa6c336615174074e9`; 0 open PRs | **0** |
| Production `https://nenjukkuneethi.org` | Vercel Production deployment `6638432286` for `f991043c…` | **0** (read-only GETs only) |
| `pugazg/kalaignar-murasoli-letters` | frozen `bd0bb790…` (live `main` `d16db3e4…`: Vol-41 work only) | **0** |
| `pugazg/kalaignar-stage-plays` | frozen `521fe545…` (= live `main`) | **0** |
| `pugazg/kalaignar-literary-commentary` | frozen `e23548b0…` (= live `main`) | **0** |
| Control `pugazg/kalaignar-tribute` | this record + `HANDOVER.md` + `NEXT_CHAT_PROMPT.md` only | 3 files |

`WAVE8_COMPLETED_WORKS_CENSUS.md` is **not** modified.

## 20. Final decision

**WAVE-8 P5 PRODUCTION ACCEPTANCE — PASS.**

**WAVE 8 COMPLETE / CLOSED / FROZEN AT P5.** The lifecycle ran to completion:
- P0 — census / owner-selected scope / readiness;
- P1 — hidden data foundation;
- P2 — fidelity and reader layer;
- P3 — direct routes while undiscovered;
- P4 — publication / catalogue / discovery / sitemap;
- P5 — independent production acceptance and durable control close-out.

P0–P5 are frozen historical stages, and the accepted implementation boundary above is immutable.

**There is no Wave-8 P6.** Any later activity requires explicit owner authorization, as either:
- a **separately authorized new wave** with its own census; or
- **specifically scoped, evidence-backed maintenance or repair** of already-published works.

Neither is ever called "P6".
