# Wave 7 P0 — Completed-Works Census & Digital-Library Readiness

**WAVE 7 P0 — COMPLETE / REVIEWED / FROZEN.**
**WAVE 7 P1 — NOT STARTED / NOT AUTHORIZED.**

**Created:** 2026-09-17 · **Control documentation only.** This record froze the read-only Wave-7 P0
census after its discovery → correction → independent-review cycle. It authorizes **no** implementation,
payload, catalogue, discovery, route, sitemap, reader, source, or production change. Live GitHub is
authoritative; the SHAs below were re-verified live immediately before freezing.

Wave 6 remains **COMPLETE / CLOSED / FROZEN at P5** (historical closed state — not reopened).

---

## 1. Frozen boundaries (re-verified at freeze)

| Repo | main | tree |
|---|---|---|
| control `pugazg/kalaignar-tribute` | `5f957562850912d9753f3782686fa7606de117dc` | `75c96ac5636f7816ebe18139c2184510189ec0ef` |
| implementation `pugazg/kalaignar-autobiography` | `2a1029482f95fbc8cae6417e3a88dcbb1c8e1c3e` | `06c7ae8646ba85e61c973fecb5945ffbec256c39` |

Open control PRs at census = 0; open implementation PRs = 0.

### 1.1 Thirteen source pins (final P0)

| # | Repo | main | tree |
|---:|---|---|---|
| 1 | nenjukku-needhi-archive | `0508dde6d9` | `32698ceb92` |
| 2 | kalaignar-murasoli-letters | `6270f4dd16` | `2b19633aeb` |
| 3 | kalaignar-poems | `188d49cd4d` | `fb35686d83` |
| 4 | kalaignar-stage-plays | `e3b2ea8879` | `80febe1e06` |
| 5 | kalaignar-cinema-works | `8c1fc37a08` | `8009cdfa17` |
| 6 | kalaignar-short-stories | `7205a10892` | `1be34cc368` |
| 7 | kalaignar-novels | `9f9c187feb` | `8ba79e6e62` |
| 8 | kalaignar-essays | `b5fd292289` | `9fbb5bfb1c` |
| 9 | kalaignar-literary-commentary | `d542b4cc37` | `f5a663672e` |
| 10 | tolkappiyap-poonga | `42d13d78b8` | `7140241401` |
| 11 | kalaignar-assembly-speeches | `7a7fed1d0e` | `b08fc42e5a` |
| 12 | kalaignar-public-speeches | `6ca57fe207` | `23306338a5` |
| 13 | kalaignar-quotes | `f7e0983ff7` | `3077342f17` |

## 2. ALREADY_ONBOARDED baseline (live implementation)

`LibraryWork` = **216** — Fiction 157 · Speeches 17 · Poetry 14 · Essays & Articles 9 · Drama 8 ·
Cinema Writing 7 · Literary Commentary 2 · Life Writing 1 · Letters 1. Public collections **6** ·
`STORY_SLUGS` **154** · `/read` **77** discovery / **40** visible. Outside the candidate total below.

## 3. Frozen final census arithmetic

```
READY                       115
READY_WITH_QUALIFICATION      2
HOLD_SOURCE_VERIFICATION      0
HOLD_PUBLICATION_MODEL        1
HOLD_OWNER_DECISION           1
NOT_COMPLETE                  9
--------------------------------
TOTAL UNIQUE CANDIDATES      128
```

Outside the 128: ALREADY_ONBOARDED (216); existing-work maintenance; witness-only evidence; duplicate
workspaces; publication/collection containers that are not canonical works; out-of-scope repositories.
No approximate range remains.

## 4. READY — 115

**Cinema (3):** `maruthanattu-ilavarasi`, `vandikkaran-magan`, `naam`.
**Drama (1):** `iratha-kanneer`.
**Novels (5):** `arumbu`, `nadutheru-narayani`, `sarapallam-samundi`, `surulimalai`, `vellikkizhamai`.
> `arumbu` and `nadutheru-narayani` are **two separate canonical works** sharing the 1978 `அரும்பு` publication provenance (`collections/arumbu-1978/`). Do not merge.

**Essays (6):** `aaru-maatha-kadungkaaval`, `thudikkum-ilamai`, `perumoochu`, `viduthalai-kilarcci`, `meesai-mulaiththa-vayathil`, `pesum-kalai-valarppom`.
**Assembly speeches (3):** `1971-namathu-vilakkam`, `1973-03-07-financial-statement-reply`, `1973-03-08-financial-statement-reply`.
> `இருளும் ஒளியும்` (1973) is the publication/container relation for the two 1973 constituent speeches — not an extra catalogue work.

### 4.1 Public speeches — 97 (Part I 61 + Part II 36; intersection 0)

Derived at pin `6ca57fe20706ebcb59f3432e8067fd11a1565b54`. Excludes the 5 already-onboarded standalone
speeches, Audio-06, and the duplicate C37 workspace.

#### முத்துக் குளியல் — பாகம் I — 61 canonical constituents
- `aadithanar-piranthanaal-vizha`
- `aazhvargal-aaivu-maiya-vizha-1997`
- `alagabath-maanadu`
- `annai-teresa-padathirappu`
- `annai-velangkanni-aalaya-velli-vizha`
- `bharathi-vizha`
- `bharathiyar-vizha-1997`
- `bharathiyum-pudhumaip-pengalum`
- `doctor-radhakrishnan-virudhu-vazhangu-vizha`
- `dr-ambedkar-palkalaikkazhaga-thodakka-vizha`
- `ezhaiyin-sirippil`
- `haikku-kavithaigal`
- `ilaignargal-kattalaiyidum-kaalam`
- `ilakkiyathil-tamilagam`
- `ilakkuvanar`
- `ilangkovadigal-1`
- `ilangkovadigal-2`
- `ilangkovadigal-3`
- `ilangkovadigal-4`
- `irasarasan-silai`
- `irumozhi-pothum`
- `ithayangal-iyanthirangal-aagavendam`
- `kalai-valarppom`
- `kalaivanar`
- `kambar-vizha-1`
- `kambar-vizha-2`
- `kannimara-pothu-noolaga-nootrandu-vizha`
- `kappalottiya-tamizhan`
- `karuthuch-suthanthiram`
- `koozhaangkallai-vairamaakkuvom`
- `kural-vazhi-nadappir`
- `maanagaratchiyil-sudhandhira-ponvizha`
- `maanavargalum-arasiyalum`
- `madurai-theendamai-ozhippu-maanadu`
- `malark-kaatchi`
- `manappuratchi-thevai`
- `mozhimanam-peruvom`
- `naam-jananayagam-naan-sarvathikaram`
- `naam-ore-saathi-tamizhsaathi`
- `nadaga-dasar`
- `nila-mutram`
- `paththirikaip-penne`
- `payitru-mozhi`
- `pazhaiya-varalaarum-ilaiya-thalaimuraiyum`
- `pirappokkum`
- `punitha-thomaiyar`
- `rukmani-lakshmipathi-nutrandu-vizha`
- `salem-periyar-palkalaikkazhaga-thodakka-vizha`
- `sangakala-tamizh-naanayangkal-nool-veliyeettu-vizha`
- `sudhandhira-ponvizha-thamizhaga-thiyagigal-vazhiyanuppu-vizha`
- `sudhandhira-thina-ponvizha`
- `tamilin-solvalam`
- `tamilisai-iyakkam`
- `tamilkkudi-magan`
- `tamizhukku-niram-undu`
- `thathuvam`
- `umamaheswaranar`
- `vallalar-vazhi-ethu`
- `valluvarkkor-aalayam`
- `vasathiyullor-vazhi-viduga`
- `yathum-oore-yavarum-kelir`

#### முத்துக் குளியல் — பாகம் II — 36 canonical constituents
- `ambur-sampangi-illa-manavizha`
- `annai-teresa-nool-veliyittu-vizha`
- `ayyanan-ambalam-padathirappu-vizha`
- `chennai-aazhvargal-aaivu-maiya-vizha-urai`
- `chennai-chennai-puranagar-vanigargal-sanga-maanadu`
- `chennai-erodu-tamizhanban-noolgal-veliyittu-vizha`
- `chennai-exnora-rotary-niruvanangalin-paarattu-vizha`
- `chennai-nathigam-ramasami-illa-manavizha`
- `chennai-thiraiyulagam-nadathiya-paarattu-vizha`
- `chennai-thiripura-orumaippattu-thina-koottam`
- `chennai-thiyagigal-manimandapa-thirappuvizha`
- `desiya-ilainjar-kondatta-thodakka-vizha`
- `indiya-suvishesha-thiruchabai-vizha`
- `isaithamizhin-unmai-varalaru-nool-veliyittu-vizha`
- `kanchi-manimozhiyar-illa-manavizha`
- `kanchipuram-cvm-annamalai-illa-manavizha`
- `karl-marx-mozhipeyarppu-noolgal-jamadhagni-veliyittu-vizha`
- `kavikko-abdul-raguman-manivizha`
- `madurai-madha-nallinakka-maanadu`
- `madurai-vazhakkarinjar-sanga-125-aavathu-aanduvizha`
- `may-thina-vizha`
- `murasoli-arakkattalai-virudhu-vazhangu-vizha`
- `muthamizh-peravai-vizha`
- `nagarkovil-jeevanandham-manimandapa-thirappuvizha`
- `nellikuppam-pugazhendhi-manavizha`
- `perayar-ezra-sargunam-manivizha`
- `pidil-kumbakonam-rajamanickam-pillai-nootraandu-vizha`
- `purusai-gopalarathinam-illa-manavizha`
- `puthandu-isaivizha`
- `rajapalayam-kumarasami-raja-nootraandu-vizha`
- `thiraippada-virudhu-vazhangum-vizha`
- `thiru-vi-ka-kalki-noolgalukku-parivuthogai-vazhangum-vizha`
- `thiruvalluvar-vizha`
- `thiruvannamalai-arunai-poriyiyal-kalloori-pattamalippu-vizha`
- `tn-rajarathinam-pillai-nootraandu-vizha`
- `veeran-sundaralingam-ninaivu-grama-thirappuvizha`

## 5. READY WITH QUALIFICATION — 2

- **`nachuk-koppai`** (drama, 1951): workflow complete; Tamil/English closed; 63/63 processed; 62 verified; **one terminal source-condition hold at scan 22**; Scene 5 inherits that hold; publication must preserve the qualification.
- **`kuraloviyam`** (literary commentary): six Parts, scans 1–666; archival + maintained-English workflow **COMPLETE / CLOSED** (`PART_006_FINAL_CLOSURE.md`, `NEXT_CHAT_PROMPT_KURALOVIYAM.md`); visual verified 666/666; Tamil textual verified 662; English release-ready 662; **Part-001 scans 13, 14, 15, 19 deliberately source-limited**; blocked 0; derived sections complete; no required Kuraloviyam workflow remains. The four source-limited pages are permanent documented source conditions, not unfinished work. (Stale `GR1 next` wording in `works/kuraloviyam/HANDOVER.md`/README is documentation-cleanup maintenance only; do not reopen.)

## 6. HOLD — 2

- **`chinna-chinna-malargal`** — **HOLD / PUBLICATION_MODEL**: archivally + English ready (497/497) but the Digital Library has no approved Quotes shelf/reader/publication model.
- **`ore-mutham`** — **HOLD / OWNER_DECISION**: 131 scans processed; 103 verified; **28 terminal blocked**; 27/28 blocked scans scene-relevant; 18/33 scenes hold-bearing; Tamil + English workflows honestly closed for current evidence. Not READY without explicit owner acceptance of that source-condition magnitude, or materially stronger source evidence.

## 7. NOT COMPLETE — 9

1. `sangatamil` — Tamil pipeline closed; maintained-English translation still active.
2. `payumpuli-pandaraka-vanniyan` — Part 001/16 only; release/closure blocked.
3. `kalaivanar-nsk-memorial-day-audio-06` — **distinct** recording (source file 06; duration `00:26:22.080`; SHA-256 `6f0149229196b1d6df092d9fee006253591afec7ba9512bfbeb46dd0ab82c836`; ≠ onboarded file-05 00:07:23.559 `7457004d3c3ee87722edfe6814e830d3521b834dcf29b4de45bb7174a2278148`); T1 provisional; T2/T3 not closed; English blocked. Not a duplicate of the onboarded shorter recording.
4. `1958-financial-statement-debate`
5. `1959-financial-statement-debate`
6. `1960-financial-statement-debate`
7. `1961-financial-statement-debate`
8. `1962-financial-statement-debate`
9. `1970-09-09-no-confidence-motion`

(Items 4–9 are canonical constituents of the incomplete 2007 financial-statement Part-1 assembly programme.)

## 8. Maintenance / witness / duplicate ledger (outside the 128)

**Existing-work maintenance:** `nenjukku-needhi` additional memoir material; `murasoli-letters` additional volumes / English work.
**Witness-only:** Bharathiar-University English poem witnesses; 1956 witnesses used for `arumbu` / `nadutheru-narayani`.
**Duplicate workspace:** `speeches/pazhaiya-varalarum-ilaiya-thalaimuraiyum` = **DUPLICATE WORKSPACE / SLUG VARIANT — NOT A SECOND CANONICAL WORK** of Part-I constituent 37/61 (31-08-1980, Karaikudi Alagappa Engineering College, PDF 286–305 / printed 285–304). Census identity key retained: `pazhaiya-varalaarum-ilaiya-thalaimuraiyum`. C37 counted once. No source mutation in this record.
**Publication/collection containers (not extra canonical works):** `முத்துக் குளியல் — பாகம் I`, `முத்துக் குளியல் — பாகம் II`, `இருளும் ஒளியும்`, `arumbu-1978`, the 2007 assembly anthologies.

## 9. Source drift observed during P0

`kalaignar-novels` advanced during the census to `9f9c187feb16dcc2a9afa7b7fa622db78738e4fc` (tree
`8ba79e6e62925c076374d2a5506a86d7a7303838`) from `payumpuli-pandaraka-vanniyan` Part-001
release-readiness activity. The five closed READY novel subtrees remained materially unchanged;
`payumpuli-pandaraka-vanniyan` remains NOT COMPLETE; census classifications were unaffected.

## 10. Future P1 planning (recorded; NOT authorized)

- B1 Cinema — 3 · B2 Drama — `iratha-kanneer` (qualified `nachuk-koppai` separately gated) · B3 Novels — 5 · B4 Essays — 6 · B5a Public speeches Part I — 61 · B5b Public speeches Part II — 36 · B6 Assembly speeches — 3 · qualified literary-commentary candidate — `kuraloviyam`.
- Potential future collections: முத்துக் குளியல் Part I; முத்துக் குளியல் Part II; possibly `இருளும் ஒளியும்`; possibly `arumbu-1978`. Member-work count, collection count and discovery-entry count are distinct and are not summed as catalogue works.

**This is planning only. Wave 7 P1 is NOT authorized by this record.**

## 11. Projection (NOT implementation state)

- READY only: `216 + 115 = 331`.
- READY + both qualified works (if later authorized): `216 + 117 = 333`.
- READY-only shelf projection: Speeches `17 → 117` · Cinema Writing `7 → 10` · Drama `8 → 9` · Fiction `157 → 162` · Essays & Articles `9 → 15`. Qualified additions are not silently included.

## 12. Remaining owner decisions

1. `ore-mutham` — keep HOLD or explicitly accept publication with 28 terminal source holds.
2. `chinna-chinna-malargal` — authorize a Quotes shelf/reader model, or keep HOLD.
3. Speech-collection UI/model for முத்துக் குளியல் (future `LibraryCollection` representation).
4. Optional later source-maintenance cleanup: Kuraloviyam stale GR1 summary text; duplicate C37 speech workspace/slug.

None of these prevents P0 census closure.

## 13. Out of scope

`anna-corpus` (C.N. Annadurai — different author), `aytham` (Tamil programming language), and all non-Kalaignar `pugazg` repositories (DMK/party, classical-Tamil corpora, other authors, bio-documentary, tooling).
