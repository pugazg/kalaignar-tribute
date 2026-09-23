# Wave 7 — P5 Production Acceptance & Durable Control Close-Out

**Created:** 2026-09-23 · **Control-only record.** Implementation delta = **0**, source delta = **0**,
production mutation = **0**. Live GitHub and production are authoritative; every SHA and count below was
re-fetched or re-derived live before this record was written.

P5 is the independent production acceptance of the fully merged Wave-7 P1–P4 implementation, together with
the two pre-P5 public-provenance maintenance corrections, and the durable control-state close-out. It made
**no** implementation, payload, catalogue, collection, route, sitemap, discovery, source or production change.

**Decision: WAVE-7 P5 PRODUCTION ACCEPTANCE — PASS. WAVE 7 COMPLETE / CLOSED / FROZEN AT P5. There is no
Wave-7 P6.**

This record supersedes, as *current programme state*, the "WAVE 7 P1 — NOT STARTED / NOT AUTHORIZED" banner of
[`WAVE7_COMPLETED_WORKS_CENSUS.md`](./WAVE7_COMPLETED_WORKS_CENSUS.md). That banner was true when P0 froze; the
census itself is **not** rewritten and remains the historical selection authority.

---

## 1. Accepted implementation boundary

| Item | Value |
|---|---|
| Implementation repo | `pugazg/kalaignar-autobiography` |
| **Accepted implementation `main`** | **`cf769d06c1bdb4abc58b5ef2c26e609a777b4923`** (merge of PR #96) |
| **Accepted tree** | **`35d64fb97f7bed1e26c3bb09fea5649db9d1e348`** |
| Open implementation PRs at acceptance | **0** |
| Control base for this record | `pugazg/kalaignar-tribute` `main` `3732822d86b9ed194a4b39cc36ec52c97c6ce346`, tree `dd47fe4c98a37f0d22d701f8f9da71f98586ad66` |
| Open control PRs at acceptance (before this one) | **0** |
| Production | `https://nenjukkuneethi.org` — Vercel **Production** deployment `6617736028` for `cf769d06…`, state **success** |

The P5 regression checkout was a clean detached worktree at exactly `cf769d06…`; its tree re-computed to
`35d64fb9…` (== live `main`).

## 2. Implementation PR / merge boundaries (Wave 7 P1–P4 + pre-P5 maintenance)

Every PR below was independently reviewed at its exact head and merged only at that head (normal merge
commits, approved head == merge second parent).

| PR | Scope | Approved head | Merge commit |
|---|---|---|---|
| #88 | B1 Cinema P1 — freeze + import 3 works (hidden) | `71a6f269798267495b2cb01ad058ea6c5adcf0d5` | `ef7241b58077ec5c63644f1eed39d39e77f34df7` |
| #89 | B1 Cinema P2–P4 — publish 3 works | `52cf4f4c1cba0559c26e9da4282408b843034bba` | `82d38a7f032d92e3e851fa8b74c29db3fd50e4de` |
| #90 | B2–B4 P1 — freeze + import 13 works (hidden) | `323a9f6fe119dd15a6b635d707783ca806289015` | `90da19169d4a323dfd0dfbe954ef56040d6cd35e` |
| #91 | B2–B4 P2–P4 — publish 13 works + `arumbu-1978` | `5540bbf693f98b3c6120fc4a2ffc11bcce5a4ac2` | `aa5e790b51e070b4d1eced9f0259e0196f1744b4` |
| #92 | B4 correction — விடுதலைக் கிளர்ச்சி archival leak / 2-unit coverage; பேசும் கலை வளர்ப்போம் source-section model; B4 notes | `82783476f9a2015863e1112fa1c0ac31731ceaff` | `ec371a31714bc0e449a7342b746a8814bfab708f` |
| #93 | Essay public-provenance boundary (allowlisted projection) + Wave-6 B6 notes | `5617e1e10947889edaaa3f6c8fa9d6823b97bb47` | `4e6381806470ee2f5c9a3026cdc388d9f4b9c349` |
| #94 | B5a / B5b / B6 / Kuraloviyam P1–P4 — 101 works + 2 முத்துக் குளியல் collections | `9b465df0ff56613ab2eebf51e81c3d24b71e40b1` | `66ed3502271f7211995f9607c264b832f8875e2d` |
| #95 | Maintenance — Drama `/source` public-provenance projection (no archival change) | `dc8f28229517d8a61e425a60b58d35f76c964825` | `36720015b6e7c6f0152c48791bada187f5edd2dc` |
| #96 | Maintenance — Wave-3 essay public notes: drop "Bulk Onboarding Wave 3" (importer-level) | `7ba8fd0aba90e8204ef084f415e8cdbaad57d821` | **`cf769d06c1bdb4abc58b5ef2c26e609a777b4923`** |

PR #95 and #96 are scoped maintenance of already-published public surfaces, integrated into the accepted final
boundary. They are **not** Wave-7 works and add nothing to the Wave-7 count.

## 3. Wave-7 population = 117

Re-derived from the committed manifests (`data/internal/wave7/b1-cinema.json`, `b2-b4-p1-manifest.json`,
`b5-b6-speeches-manifest.json`) and `data/wave7-b5-b6-k-catalogue.ts`; every id is published, and the 117 are
unique.

| Segment | Class | Works |
|---|---|---:|
| B1 Cinema — `maruthanattu-ilavarasi`, `vandikkaran-magan`, `naam` | READY | 3 |
| B2 Drama — `iratha-kanneer` | READY | 1 |
| B3 Novels — `arumbu`, `nadutheru-narayani`, `sarapallam-samundi`, `surulimalai`, `vellikkizhamai` | READY | 5 |
| B4 Essays — `aaru-maatha-kadungkaaval`, `thudikkum-ilamai`, `perumoochu`, `viduthalai-kilarcci`, `meesai-mulaiththa-vayathil`, `pesum-kalai-valarppom` | READY | 6 |
| B5a Public speeches — முத்துக் குளியல் Part I | READY | 61 |
| B5b Public speeches — முத்துக் குளியல் Part II | READY | 36 |
| B6 Assembly — `1971-namathu-vilakkam`, `1973-03-07-financial-statement-reply`, `1973-03-08-financial-statement-reply` | READY | 3 |
| **READY subtotal** | | **115** |
| `nachuk-koppai` (Drama) | READY WITH QUALIFICATION | 1 |
| `kuraloviyam` (Literary Commentary) | READY WITH QUALIFICATION | 1 |
| **Wave-7 implemented canonical works** | | **117** |

Cross-check against the frozen P0 census: the census's Part I list (61) is set-equal to B5a, its Part II list
(36) is set-equal to B5b, and its 18 non-speech READY slugs equal B1 + B2 + B3 + B4 + B6. Collections and
publication containers (`arumbu-1978`, முத்துக் குளியல் I/II, இருளும் ஒளியும்) are **not** counted as works.

## 4. Final catalogue / shelf census

Pre-Wave-7 figures are re-derived from live `main` by removing the 117 Wave-7 ids (not copied from a prompt).

| Shelf | Pre-Wave-7 | Final | Δ |
|---|---:|---:|---:|
| Life Writing | 1 | 1 | 0 |
| Letters | 1 | 1 | 0 |
| Poetry | 14 | 14 | 0 |
| Cinema Writing | 7 | **10** | +3 |
| Drama | 8 | **10** | +2 |
| Fiction | 157 | **162** | +5 |
| Essays & Articles | 9 | **15** | +6 |
| Speeches | 17 | **117** | +100 |
| Literary Commentary | 2 | **3** | +1 |
| **Total** | **216** | **333** | **+117** |

`LIBRARY_WORKS` = 333, all `state: "published"`, 333 unique ids; non-empty shelves 9.

## 5. Collection census — 9

| Collection | Members | Wave |
|---|---:|---|
| `1977-kalaignar-karunanidhiyin-sirukathaigal` | 37 | pre-Wave-7 |
| `2008-kalaignar-sonna-kathaigal` | 40 | pre-Wave-7 |
| `2004-kalaignarin-kuttik-kathaigal` | 34 | pre-Wave-7 |
| `1987-kalaignar-sonna-kuttik-kathaigal` | 25 | pre-Wave-7 |
| `1982-mudiyatha-thodarkathai` | 6 | pre-Wave-7 |
| `2009-16-kathaiyinile` | 16 | pre-Wave-7 |
| **`arumbu-1978`** | **4** | Wave 7 (B3) |
| **`muthukkuliyal-part-1`** | **61** | Wave 7 (B5a) |
| **`muthukkuliyal-part-2`** | **36** | Wave 7 (B5b) |

- `arumbu-1978`: exactly 4 members — `arumbu`, `sarapallam-samundi`, `periya-idathup-pen` (existing Wave-6 work,
  non-controlling 1978 witness), `nadutheru-narayani`; all resolve to canonical LibraryWorks; `arumbu` and
  `nadutheru-narayani` are two distinct works with distinct routes; no collection id is also a LibraryWork.
- முத்துக் குளியல் Part I: 61 members, 61 unique, ordinals 1–61 == the frozen manifest's source order; C37 counted
  **once** (`pazhaiya-varalaarum-ilaiya-thalaimuraiyum`, ordinal 37); the duplicate-workspace slug
  `pazhaiya-varalarum-ilaiya-thalaimuraiyum` is in neither the catalogue nor the sitemap and returns 404.
- முத்துக் குளியல் Part II: 36 members, 36 unique, ordinals 1–36 == source order.
- Part I ∩ Part II = **0**; Part I ⊆ B5a; Part II ⊆ B5b. Collections do not inflate the 333 LibraryWork count.

## 6. Discovery census (`discoveryShelves()`, live `main`)

| Shelf | Works | Discovery entries |
|---|---:|---:|
| Life Writing | 1 | 1 |
| Letters | 1 | 1 |
| Fiction | 162 | **20** |
| Poetry | 14 | 14 |
| Drama | 10 | 10 |
| Cinema Writing | 10 | 10 |
| Speeches | 117 | 22 |
| Essays & Articles | 15 | 15 |
| Literary Commentary | 3 | 3 |
| **Total** | **333** | **96** |

Initially visible (cap 6 per shelf) = **41**. Speeches = 2 முத்துக் குளியல் collection cards + 20 standalone
speeches (17 pre-Wave-7 + the 3 B6 assembly speeches). No collection member is also a standalone discovery card.

## 7. Wave-7 route arithmetic = 870

Reconstructed from committed route registries — not hand-typed:

| Segment | Source of the route list | Routes |
|---|---|---:|
| B1 Cinema | `data/internal/wave7/b1-p3-routes.json` `works[].routes` (declared total 133) | **133** |
| B2–B4 direct routes | `data/internal/wave7/b2-b4-p3-routes.json` `works[].routes` (declared 224 = drama 83 + novels 62 + essays 79) | 224 |
| B3 collection landing | `/collections/arumbu-1978` (`data/collections.ts`) | 1 |
| **B2–B4 subtotal** | | **225** |
| B5/B6/Kuraloviyam | `WAVE7_B5_B6_K_ROUTES` — 100 speeches × (reader + `/source`) 200 + Kuraloviyam 310 (landing + source + 308 units) + 2 collection landings | **512** |
| **Total** | | **870** |

- Expected 870 · unique **870** · no duplicate.
- The B5/B6/K set is additionally **set-equal** to an independent derivation from the frozen manifests
  (`b5-b6-speeches-manifest.json` works + collections; `kuraloviyam-manifest.json` hash-pinned `units/*.json`).
- By route family: cinema 133 · plays 83 · novels 62 · essays 79 · collections 3 · speeches 200 · kuraloviyam 310.
- Consistent with the frozen pre-Wave-7 production baseline:

```
sitemap   : 3909 + 870 = 4779
prerender : 3918 + 870 = 4788
html      : 3913 + 870 = 4783
```

## 8. Production route sweep (2026-09-23)

- All **870** expected routes fetched from `https://nenjukkuneethi.org` with redirects **not** followed:
  **870 × HTTP 200 · 0 non-200 · 0 redirects · 0 missing**.
- 277 representative pages were additionally fetched as HTML **and** RSC (`RSC: 1`) — all 200.

## 9. Fail-closed checks (invalid routes → 404)

All **37** returned **404** directly (no redirect concealment):

- Cinema: `/cinema/naam/scene-046`, `/cinema/naam/scene-000`, `/cinema/naam/zzz`,
  `/cinema/maruthanattu-ilavarasi/segment-011`, `/cinema/maruthanattu-ilavarasi/scene-001`,
  `/cinema/vandikkaran-magan/scene-073`, `/cinema/zzz-not-a-film`
- Drama: `/plays/iratha-kanneer/62`, `/plays/iratha-kanneer/00`, `/plays/nachuk-koppai/19`,
  `/plays/nachuk-koppai/zzz`, `/plays/zzz-not-a-play`, `/plays/zzz-not-a-play/source`
- Novels: `/novels/surulimalai/28-chapter-28`, `/novels/surulimalai/zzz`, `/novels/arumbu/02-arumbu`,
  `/novels/zzz-not-a-novel`, `/novels/zzz-not-a-novel/source`
- Essays: `/essays/viduthalai-kilarcci/articles/zzz`, `/essays/viduthalai-kilarcci/articles/article-03`,
  `/essays/pesum-kalai-valarppom/articles/section-20`, `/essays/pesum-kalai-valarppom/articles/section-00`,
  `/essays/zzz-not-an-essay`, `/essays/zzz-not-an-essay/source`
- Speeches: `/speeches/zzz-not-a-speech`, `/speeches/zzz-not-a-speech/source`, `/speeches/tamilin-solvalam/zzz`,
  `/speeches/1971-namathu-vilakkam/zzz`, `/speeches/iruzhum-ozhiyum`,
  `/speeches/pazhaiya-varalarum-ilaiya-thalaimuraiyum` (C37 duplicate workspace)
- Kuraloviyam: `/kuraloviyam/entry-301`, `/kuraloviyam/entry-000`, `/kuraloviyam/zzz`, `/kuraloviyam/part-001`
- Collections: `/collections/zzz-not-a-real-collection`, `/collections/muthukkuliyal-part-3`,
  `/collections/iruzhum-ozhiyum`

Plus the surulimalai source gap: `/novels/surulimalai/06-chapter-06`, `/07-chapter-07`, `/06`, `/07` → **404**.

## 10. Production `/read` acceptance

Measured in a live browser session on `https://nenjukkuneethi.org/read`:

- **9** shelves; **96** discovery cards; **41** initially visible; **6** `<details>` disclosures (Fiction,
  Poetry, Drama, Cinema Writing, Speeches, Essays & Articles).
- Headings: Fiction `162 படைப்புகள் · 7 தொகுப்புகள்` (20 cards, incl. `arumbu-1978`); Speeches
  `117 படைப்புகள் · 2 தொகுப்புகள்` (22 cards: `/collections/muthukkuliyal-part-1`, `/collections/muthukkuliyal-part-2`
  + 20 standalone, the last three being the B6 assembly speeches); Literary Commentary 3 (`/tholkappiyam`,
  `/thirukkural`, **`/kuraloviyam`**).
- No முத்துக் குளியல் member and no `arumbu-1978` member appears as its own `/read` card; the live collection
  pages list 61 / 36 / 4 members, Part I ∩ Part II = 0.
- The three B1 cinema works have `/read` cards.
- Holds / NOT_COMPLETE absent from catalogue **and** production sitemap: `chinna-chinna-malargal`, `ore-mutham`,
  `sangatamil`, `payumpuli-pandaraka-vanniyan`, `kalaivanar-nsk-memorial-day-audio-06`, the six 2007
  financial-statement / no-confidence Part-1 units; no `/quotes` route.

## 11. Batch acceptance

**B1 Cinema.** `maruthanattu-ilavarasi`, `vandikkaran-magan`, `naam` — canonical LibraryWorks, discoverable,
sitemap-exposed, all 133 routes 200, `/source` pages carry the pinned commit `8c1fc37a…` (positive control), no
hidden/P1 state serialized.

**B2 Drama.** `iratha-kanneer` published; `/source` 200; 0 internal fields in HTML/RSC; **0 of 2010**
reading-text probes present in `/source` HTML/RSC (control: 2005 present on the reader landing). All 10 Drama
`/source` pages: positive controls pass, 0 internal fields.

**B3 Novels.** Five distinct canonical works; `arumbu` («அரும்பு — The Bud») and `nadutheru-narayani`
(«நடுத்தெரு நாராயணி») have separate landings and identities; `surulimalai` source page states *"The source prints
chapters with no chapters 6 or 7 in its own numbering; the assembled reading layer preserves that gap exactly and
invents no chapter 6/7"*, and the reader lists chapters 1–5 then 8…; `arumbu-1978` is a collection, not a work.

**B4 Essays.**
- `viduthalai-kilarcci`: exactly two units — `வேங்கையை விரட்டும் படலம்` (scans 4–7) and `விடுதலைக் கிளர்ச்சி`
  (scans 8–68); the landing labels them 1 and 2 as *archive reading-order numbers, not printed* (no printed
  contents page); no archival trailer / source comment in either article body.
- `pesum-kalai-valarppom`: exactly 19 source-numbered sections (`section-01`…`section-19`); no titles invented;
  the source page states that the book prints no contents page and that the section numbers are source-printed.

**Wave-3 essay maintenance (PR #96; not a Wave-7 work).** `kayittril-thongiya-kanapathi`, `unarchchimaalai`,
`thiraavida-sampaththu`: live HTML + RSC carry both durable notes (*"The controlling PDF is not vendored into this
repository and is never fetched at runtime."* · *"This publication prints no contents page; article ordinals are
archive reading ordinals."*) and no `Bulk Onboarding` / `Wave 3` wording.

**B5a / B5b.** All 97 முத்துக் குளியல் constituents published; Part I 61 / Part II 36 (see §5, §12).

**B6.** Three separate canonical works. `இருளும் ஒளியும்` appears on the two 1973 `/source` pages only as the
printed book title (container), is not a fourth LibraryWork, and has no route. 7 March (scans 4–40, printed 3–39)
and 8 March (scans 41–62, printed 40–61) are distinct witnesses with **0** shared text blocks.

## 12. Qualified-work acceptance

### `nachuk-koppai` — READY WITH QUALIFICATION (published)

Live `/plays/nachuk-koppai/source`:
- 63 scan pages; page records for dramatic-body scans 5–63 (front matter 1–4) governed by the work's page-layer audit;
- exactly **one** documented source-condition hold: **scan 22 · unit 05 (Scene 5)** — *"The two adjacent clusters
  on scan 22 are unreadable; their character identity is NOT invented and no Unicode is supplied. Scene 5 is
  otherwise complete and source-faithful. This is the single terminal textual source-condition hold, carried
  transparently in both layers and never reconstructed, inferred, modernized or silently repaired."*;
- *"This work is accepted READY WITH QUALIFICATION."*;
- catalogue card: *"one terminal source textual-condition hold at scan 22 / Scene 5 is carried transparently —
  never reconstructed"*.

Recorded precisely: the P0 census figure *63/63 processed, 62 verified* is represented publicly as 63 scans with
exactly one terminal hold scan (scan 22); a literal "62 verified" count is not printed. This is the representation
reviewed and merged in PR #91 and re-reviewed in PR #95; it is unchanged here.

Internal archival record (retained, not public): frozen `hidden` {discoverable/sitemapExposed/publicRoute false,
note *"Wave 7 Batch 2 P1 hidden foundation."*}, `wave: 7`, `batch: 2`, `shelf: "drama"`,
`readiness: "ready-with-qualification"`; the hold keeps `scene`, `markerKind`, `locus`. `iratha-kanneer` likewise
retains its frozen P1 record (`readiness: "ready"`). Neither is serialized publicly (PR #95 projection).

### `kuraloviyam` — READY WITH QUALIFICATION (published)

Exactly **one** LibraryWork (Literary Commentary). Live `/kuraloviyam/source` verification block:
visual **666 / 666** · Tamil textual **662 / 666** · English (project-created) **662 / 666** · source-limited scans
**13, 14, 15, 19** — *"their unreadable words are not transcribed, not translated, and not inferred. This is the
source's condition; not pending work."* The six `TVA_BOK_0065733_…part_00N…pdf` intake files are listed as transfer
splits of one 666-scan book — *"they are not six separate works."* No Tamil or English 666/666 claim. The public
provenance payload carries `blocked: 0`; the visible page expresses it as "not pending work" rather than a separate
"blocked" row. `front-04` (scans 13–15, handwritten facsimiles) supplies no transcription; `front-06` (scan 19)
marks the washed-out wording `[சில சொற்கள் மூல ஸ்கேனில் தெளிவில்லாததால் ஊகிக்கப்படவில்லை]`.

## 13. Condensed-English speech policy

Frozen manifest classification over the 100 Wave-7 speeches: **45 condensed** (all B5a) + **55 full**
(B5a 16 + B5b 36 + B6 3). No speech was reclassified during P5.

- Live `/source` pages: the "English form — condensed English rendering, not a full translation (English / Tamil
  word ratio …)" row appears on **exactly the 45** manifest-condensed speeches and on **none** of the 55 full ones.
- `tamilin-solvalam` (condensed): ratio **0.13** shown; catalogue `english: "partial"`, card *"English: condensed
  rendering"*; the source archive status (*"verified-complete · condensed English rendering (not a full
  translation)"*) is a separate row from the Digital Library's measured *English form*; reader in English layer,
  both UI languages: *"A condensed English rendering, not a full translation … (about 13% of the length of the
  Tamil). The complete, authoritative text is the Tamil original."*
- `vallalar-vazhi-ethu` (Part I, full) and `ambur-sampangi-illa-manavizha` (Part II, full): catalogue
  `english: "complete"`; reader shows *"A verified, source-linked faithful English reading translation. The Tamil
  original remains authoritative."*; no condensed label.

## 14. Public provenance / serialization acceptance

Production HTML **and** RSC of 277 pages (554 payloads) scanned for serialized keys `hidden`, `wave`, `batch`,
`readiness`, `discoverable`, `sitemapExposed`, `publicRoute`, `sourceTree`, `archiveVerification`,
`releaseReadiness`, `sourceAuthority`, `workId`, `shelf`, `sourcePdfCommitted`, `rightsAction`, `locus`,
`markerKind`, `readingUnits` and the text `hidden foundation` / `Bulk Onboarding`.

- **0** hits for `hidden`, `wave`, `batch`, `readiness`, `discoverable`, `sitemapExposed`, `publicRoute`,
  `sourceTree`, `archiveVerification`, `sourceAuthority`, `locus`, `markerKind`, `hidden foundation`,
  `Bulk Onboarding` on any page.
- All 117 speech `/source`, 10 Drama `/source`, 15 essay `/source`, 5 Wave-7 novel `/source`, 3 Wave-7 cinema
  `/source` pages and Kuraloviyam `/source` pass **positive controls** (pinned source commit + scan filename present
  in both HTML and RSC).
- Remaining key-name matches were classified, not waived: `shelf` / `workId` occur only on `/read` and collection
  pages as public catalogue fields (a work card's shelf; a collection member's work id); `readingUnits` occurs only
  on Drama **reader** pages (the reading text belongs there — 0 on `/source`); `releaseReadiness`,
  `sourcePdfCommitted`, `rightsAction` occur on novel `/source` pages as the long-standing public novel-provenance
  shape (identical on pre-Wave-7 `balipeedam-nokki` and Wave-6 `periya-idathup-pen`), carrying durable public
  values rendered by `NovelSource` (e.g. *"English verified (project-created); Tamil remains authoritative"*,
  *"nationalisation"*), and `rightsAction` on `sakkaravarththiyin-thirumagan` `/source` via the PR #93 allowlist.
  None is internal workflow state; the Wave-7 novel archival `hidden` / `wave` / `batch` / `readiness` /
  `sourceTree` fields are not serialized.

## 15. Final sitemap

Production `/sitemap.xml`: **4779** URLs · **4779** unique · **0** duplicates · single origin
`https://nenjukkuneethi.org`. Expected Wave-7 routes **870 / 870 present · 0 missing**; non-Wave-7 entries **3909**
(== the frozen pre-Wave-7 baseline).

## 16. Merged-main regression (read-only, exact pins)

Clean detached checkout of `cf769d06…` (tree `35d64fb9…`). Source archives fetched **by SHA** with the Library CI
fetch step run verbatim (30 pinned checkouts, read-only, disposable directory).

- `tsc --noEmit`: clean · `git diff --check`: clean · `git status`: clean before and after.
- Production build: **4788 prerender / 4783 HTML** (4791 static pages generated).
- CI `archival validators` job re-run locally, every step: **all pass** — incl. Wave-7 B1 cinema source-pin
  fidelity; Wave-7 B2–B4 P1 source/import (235) and P2 source render fidelity (2550); Wave-7 B5/B6/K P1
  source/import (1585) and P2 source render fidelity (6465); B5/B6/K deterministic regeneration (`--verify`,
  310 files + manifest byte-identical); Wave-3 essays (ALL PASS, 510); Wave-6 B1–B6; Wave-6 B7 P1 (2008, with the
  frozen control artifact `ceccd2a5…` for set-equality) / P2 fidelity (5347) / P4 source re-derivation (1931);
  1977 anthology; collections declaration; Thirukkural; validator contract (upheld).
- CI `typecheck • build` job re-run locally, all **45** steps pass — incl. collections, shelf disclosure,
  Wave-5/6 regressions, Wave-6 B7 P1–P4, Wave-7 B1 P1–P4, B2–B4 P1-hidden / P2 render (1128) / P3 (518) / P4 (698),
  B5/B6/K P1-hidden (215) / P2 render (2484) / P3 (1136) / P4 (459), essay public provenance (430), B5/B6/K public
  provenance (2783), Drama public provenance (158), Poetry witness integrity/UI.
- Full `test:*` sweep with the pinned sources: **49 / 49 pass** (46 directly; the three source-argument
  scripts `test:wave6-b7-p2-fidelity` 5347, `test:wave7-b1-cinema` 59, `test:wave7-b2-b4-p1` 235 pass when given
  their pinned checkouts, exactly as the CI archival job invokes them).
- The source-dependent B3 novel pin `cc5c7fe5…` differs from the P0 census pin `9f9c187f…`; independently
  re-verified that all five Batch-3 work subtrees are byte-identical at both commits (as the committed manifest's
  drift note states).

## 17. CI and deployment evidence

- Latest merged-main Library CI for the accepted tree: run **`35880810427`** on `cf769d06…` — `typecheck • build`
  **SUCCESS** · `archival validators` **SUCCESS**.
- Exact-head PR CI for #96: run `35879988273` on approved head `7ba8fd0a…` (tree `35d64fb9…`, identical to merged
  `main`) — SUCCESS.
- Vercel Production deployment `6617736028` for `cf769d06…` — **success**; commit status `Vercel=success`.

## 18. Immutability

| Repo | Boundary | Delta |
|---|---|---:|
| Implementation `pugazg/kalaignar-autobiography` | `main` `cf769d06c1bdb4abc58b5ef2c26e609a777b4923`, tree `35d64fb97f7bed1e26c3bb09fea5649db9d1e348` | **0** |
| Production `https://nenjukkuneethi.org` | Vercel production for `cf769d06…` | **0** (read-only fetches only) |
| Source repositories | frozen Wave-7 pins below (P5 fetched by SHA, read-only; wrote nothing) | **0** |

Wave-7 source witnesses (from the committed manifests; not repinned to moving source `main`):

| Segment | Repository | Pin | Tree |
|---|---|---|---|
| B1 Cinema | `kalaignar-cinema-works` | `8c1fc37a089cb23173e6b8725f7d31200ea83d7b` | `8009cdfa17637e722ee10b5c9f8910211f915af3` |
| B2 Drama | `kalaignar-stage-plays` | `e3b2ea8879964ab8f5b6cfffad79aeab9a7ca26b` | `80febe1e06e4cb3060f8b8bc403bffa7298ad115` |
| B3 Novels | `kalaignar-novels` | `cc5c7fe535c5fab35e87f91b8325d6801afec46c` (P0 pin `9f9c187f…`; 5 subtrees identical) | `253bc973c9dd7f94934ac67a61221d9771240537` |
| B4 Essays | `kalaignar-essays` | `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` | `9fbb5bfb1c3aa4e42046807669ed6929da8a9797` |
| B5a / B5b | `kalaignar-public-speeches` | `6ca57fe20706ebcb59f3432e8067fd11a1565b54` | `23306338a527a62cd8100b56f6bc99ca09772098` |
| B6 | `kalaignar-assembly-speeches` | `7a7fed1d0e3eb24a396effc10854b178f32bd0cf` | `b08fc42e5a7e17b08c8dfcfee7cefb987e45b09c` |
| Kuraloviyam | `kalaignar-literary-commentary` | `d542b4cc3749bf1966e3537d1eb34d421344faf5` | `f5a663672e3184cf435cbf7603cca7e6248c0049` |

Several source repositories' live `main` has advanced since P0 (context only; not drift for the pinned cohort).

P5 created only this record and the `HANDOVER.md` / `NEXT_CHAT_PROMPT.md` updates in `pugazg/kalaignar-tribute`.

## 19. Outside the Wave-7 implemented population (unchanged, not decided here)

- HOLD: `chinna-chinna-malargal` (PUBLICATION_MODEL — no Quotes shelf) · `ore-mutham` (OWNER_DECISION).
- NOT_COMPLETE at P0: `sangatamil`, `payumpuli-pandaraka-vanniyan`, `kalaivanar-nsk-memorial-day-audio-06`, the six
  2007 assembly Part-1 units. Not re-censused; anything completed after the P0 freeze belongs to a future,
  separately authorized wave.

## 20. Decision

**WAVE-7 P5 PRODUCTION ACCEPTANCE — PASS.**

**WAVE 7 COMPLETE / CLOSED / FROZEN AT P5.** The lifecycle P0 → P1 → P2 → P3 → P4 → P5 is complete; P0–P5 are
frozen historical stages and the accepted implementation boundary above is immutable.

**There is no Wave-7 P6.** Any future onboarding requires a separately authorized new wave (with its own census);
any repair of an already-published work is separately authorized maintenance — never "P6".
