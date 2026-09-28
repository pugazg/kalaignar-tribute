# Wave 9 P0 — Completed-Works Census & Digital-Library Readiness

**WAVE 9 — OWNER-AUTHORIZED. P0 COMPLETED-WORKS / READINESS CENSUS — REVIEW-READY. P1 NOT STARTED / NOT AUTHORIZED.**
(Owner authorization: "then let us proceed with next wave.")

**Created:** 2026-09-28 · **Control documentation only.** Implementation delta = **0**, source delta = **0** (read-only
clones only), production delta = **0** (read-only requests only). Live GitHub is authoritative; every SHA, tree and count
below was fetched or re-derived live for this record.

Waves 6, 7 and 8 remain **COMPLETE / CLOSED / FROZEN AT P5**. Reading Room IA v2 R0–R3 remain **frozen** (R3 CLOSED,
`pugazg/kalaignar-tribute#55` → `8d409ad8…`) and are not reopened by this record.

> **Accounting rule — read first.** A census *candidate* is not a LibraryWork. Only the `READY_NEW_CANONICAL` class can
> change the catalogue count; `READY_COLLECTION`, `READY_COVERAGE_EXPANSION` and `READY_WITNESS_OR_RELATION` change
> collections, coverage or provenance only; `HOLD_OWNER_DECISION` and `NOT_COMPLETE` change nothing until resolved.
> Never summarize Wave 9 as "N new works" from the candidate total.

---

## 1. Live boundary (verified 2026-09-28)

| Repo | `main` | Open PRs |
|---|---|---:|
| control `pugazg/kalaignar-tribute` | `8d409ad8164960ccb056b957926e9de53217cea8` | 0 |
| implementation `pugazg/kalaignar-autobiography` | `7fe9a4f0b8a7b543efd1cf0b533d80b0e65ab853` (tree `cd1f1367be4320cff34c58db30be843708de650e`) | 0 |

Live state agrees with the expected post-R3 boundary; **no difference** was found.
- **Canonical catalogue 568**: Life Writing 1 · Letters 3 · Fiction 157 · Poetry 173 · Drama 11 · Cinema Writing 10 ·
  Speeches 118 · Essays & Articles 91 · Literary Commentary 4 (re-derived from `publishedWorks()` at `cd1f1367`).
- **Publication records 11** · **collections 9** (1977, 1982, 1987, 2004, 2008, 2009 short-story anthologies, `arumbu-1978`,
  `muthukkuliyal-part-1`, `muthukkuliyal-part-2`).
- **Murasoli coverage**: the one `murasoli-letters` work carries Volumes **42–54** (13 volumes).
- **Production sitemap 5271** paths; build 5280 / 5275; R3 COMPLETE / REVIEWED / MERGED / PRODUCTION-ACCEPTED / CLOSED /
  FROZEN.

## 2. Source repositories inspected (final pins)

Every relevant live `pugazg` repository was cloned read-only at `main` and re-fetched before commit. Six repositories
advanced during the census; each advance was reconciled (§13) and the pins below are the reconciled final heads.

| # | Repository | `main` | tree | Since last census |
|---:|---|---|---|---|
| 1 | `kalaignar-novels` | `408100aa9ca291d8c350f8826363db29f98597f7` | `2172e9e9fa1fc323499f7294796e9bff5eb0fe40` | advanced (Payumpuli closure; new `ore-ratham` intake) |
| 2 | `kalaignar-novels-2` | `30c16def7ac07562041d1f6ed6c2cfcb8a242d8c` | `0c30c3ad26d81514e8ed16deb7c31e8cdf89db91` | new parallel archive (ரோமாபுரிப் பாண்டியன்) |
| 3 | `kalaignar-novels-3` | `165bcde6ba2b4b1189b590e79e18f7ac507aae2f` | `43d0aadef18016f44aef776ae44ef60b15914c3f` | new parallel archive (பொன்னர் சங்கர்) |
| 4 | `kalaignar-novels-4` | `660032f4eb17b1493f0b1081eadc315e64b403ac` | `4c4733565e2983bfb8bed222d740ce0887ae0213` | new parallel archive (தென்பாண்டிச் சிங்கம்) |
| 5 | `kalaignar-assembly-speeches` | `1179ade756288d1cb0e7f3f4a4f4a1df2a432d72` | `91dca167d301e19c0f5d8c83aac193236ccaa06e` | advanced (2007 Part-1 complete) |
| 6 | `kalaignar-public-speeches` | `c184b4df7a43386f0da83b5be2ffb0d3b8f08230` | `a9dc3173e35b5dd80984f49f7d88ea820d1ee6d3` | advanced (new collections/speeches) |
| 7 | `kalaignar-stage-plays` | `521fe5452e3e9ed54baa81e672325ce6ba501c5e` | `cea50efb13baf27390b794b39b76b039a9ccaead` | = Wave-8 P0 pin |
| 8 | `kalaignar-murasoli-letters` | `d16db3e4c435cb063d155f8e9a5b9e62b12317fe` | `77fa52580cbceef2568fc5c64899fa366e4796e1` | advanced |
| 9 | `kalaignar-quotes` | `f7e0983ff7c16949da78c48e860c8519b85e1eef` | `3077342f177f48a95667e5a61327dcdff2d08642` | = Wave-7 P0 pin |
| 10 | `kalaignar-adaptations` | `0379184cbd4a6349dd8e1d68e71c505790dd8555` | `fb30fb7b29b243a7c0dcbb0ea4faf718c92cdd87` | new (தாய் காவியம்) |
| 11 | `kalaignar-essays` | `63019a4dd7fcbd6815edb8ef15bb70b4cd9c8447` | `6a54477b231be7e9faff10864a0caaeb850077ae` | = R3 pin |
| 12 | `kalaignar-poems` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` | `fb35686d8313db5e99ff49e7c28cb4decfc1c429` | = Wave-7 / R3 pin |
| 13 | `kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` | `2302d1fc6cbe9386a8010b344a9caba2f4913fa4` | = Wave-8 P0 pin |
| 14 | `kalaignar-short-stories` | `7205a10892d0b208df2617766844f480b6a2c798` | `1be34cc368fbc96ff72933a004a074ef840168ee` | = Wave-7 P0 pin |
| 15 | `kalaignar-cinema-works` | `8c1fc37a089cb23173e6b8725f7d31200ea83d7b` | `8009cdfa17637e722ee10b5c9f8910211f915af3` | = Wave-7 P0 pin |
| 16 | `nenjukku-needhi-archive` | `0508dde6d96119deeab4155bfe0191128a420ad9` | `32698ceb9225554d1edbb7b2e30561e0e37eefae` | = Wave-7 P0 pin |
| 17 | `tolkappiyap-poonga` | `42d13d78b8bd21a5459de9bd3ad28dd45c993e7c` | `71402414018f66675691e90c368b5bd5333ea9bf` | = Wave-7 P0 pin |
| 18 | `kalaignar-bio-documentary` | `dc3f0b3d2be9dc8f30e839ce1403c0c76c959081` | `1aeac59392d1af83c3ea14c0dc338e0f9b8d77c2` | out of scope (video production) |
| 19 | `Kalaignar-Legacy` | `0441afa46a29812e1586926049c1132c0f30bd81` | `01310042df30d68c0751cf014801b1ea769dd25b` | out of scope (web app) |
| 20 | `Silpathikaram` | `b1baa89607db3ca8ebfb5acb0e695120ee653243` | `80ce0e134158f6f73417c1b09ef6d06d9e6638ad` | out of scope (Iḷaṅkō Aṭikaḷ adaptation research) |
| 21 | `tolkappiyam-arivagam` | `15fdb00d2873aa7f2ed180a2cbd416cab51cf540` | `787265a34ce29da7012b4aedb3bd1acac0ef6c44` | out of scope (application) |

Not inspected as out of scope (non-Kalaignar or tooling, as Wave 7 §13): `anna-corpus`, `aytham`, `DMK`,
`DMK-achievements-2021-2026`, `Dravidian-Method`, `classical-tamil`, `sangam-literature-corpus`, `nannul`,
`tolk-ppiyam-english-translation`, `manimekalai-cinematic-adaptation`, `multimodal-fact-verification`, `Minequest`, `ab-2`.

Per-input subtree pins (the import boundary; a later source commit that leaves these trees unchanged is not drift):

| Input | Path | Tree |
|---|---|---|
| பாயும்புலி பண்டாரக வன்னியன் | `kalaignar-novels` `works/payumpuli-pandaraka-vanniyan` | `31e135ca8a8df370b2de4f6ee58a59c4ecd8778e` |
| 2007 financial-statement Part-1 source package | `kalaignar-assembly-speeches` `sources/2007-financial-statement-speeches-part-1` | `aed25d1a5559492ae541e794402f5987331af944` |
| புராணப்போதை collection record | `kalaignar-public-speeches` `collections/puranappothai-1958` | `29a321ad84a8517c6157b31ca7dc282d5e56ef70` |
| Murasoli Volume 1 | `kalaignar-murasoli-letters` `volumes/volume-01` | `ffa292a7ce7797f0f57cfaf6da4f7c0418384c17` |
| Murasoli Volume 41 | `kalaignar-murasoli-letters` `volumes/volume-41` | `e1c5fd49cc67a9416ec250405216956d372121fc` |
| சின்னச் சின்ன மலர்கள் | `kalaignar-quotes` `collections/chinna-chinna-malargal` | `b4a8380c8a434b61ee62e07b40828c15729e60f9` |

(Per-speech subtree trees are listed in §5.)

## 3. Frozen prior-wave authority used (read, not edited)

`WAVE6_P5_PRODUCTION_ACCEPTANCE.md` · `WAVE7_COMPLETED_WORKS_CENSUS.md` (frozen Wave-7 P0; its READY / HOLD / NOT_COMPLETE
populations and deferral ledger) · `WAVE7_P5_PRODUCTION_ACCEPTANCE.md` · `WAVE8_COMPLETED_WORKS_CENSUS.md` (frozen Wave-8
P0; its closed-scope exclusions §12) · `WAVE8_P5_PRODUCTION_ACCEPTANCE.md` · `READING_ROOM_IA_V2_R3_CLOSEOUT.md` (the
post-R3 568-work catalogue) · `HANDOVER.md`.

## 4. Methodology

1. **Enumerate** every work, collection, volume and speech directory in each live source repository (not a stale
   list); include every previously deferred item (Wave-7 NOT_COMPLETE / HOLD, Wave-8 §12 exclusions).
2. **Readiness from the archive's own records**, never from a root navigation table alone: per-page `status` /
   `visual_fidelity` front matter, section and English records, per-unit `metadata.json`, collection constituent maps,
   and the final-closure / release documents. Root-table claims were cross-checked against the per-record evidence.
3. **Identity reconciliation against the post-R3 568-work catalogue** (exported from `publishedWorks()`,
   `LIBRARY_PUBLICATIONS`, `LIBRARY_COLLECTIONS` and the Murasoli indexes at implementation tree `cd1f1367`): source-path
   match, id/slug match, normalized Tamil-title match, date match and declared witness relations. Proposed ids were
   checked for collisions (0).
4. **Fail closed on uncertain identity**: an item whose identity against an existing work is not established by the
   source is classified `HOLD_OWNER_DECISION`, never `READY_NEW_CANONICAL`.
5. **Whole canonical work** controls readiness: a completed Part of an incomplete novel, or completed constituents of an
   active booklet, are not READY on their own.
6. **Drift reconciliation**: all heads re-fetched immediately before commit; every advance diffed and re-classified.

## 5. Candidate-by-candidate readiness table

Tamil / English give the archive's own final state. "Δ cat." is the catalogue effect **if later implemented** (P0
projection only).

### 5.1 Novels

| # | Candidate | Source / path | Tamil | English | Closure | Class | Δ cat. |
|---:|---|---|---|---|---|---|---:|
| N1 | **பாயும்புலி பண்டாரக வன்னியன்** (`payumpuli-pandaraka-vanniyan`) | `kalaignar-novels` `works/payumpuli-pandaraka-vanniyan` | **477 / 477** page records `verified` + visual `verified`; assembled Tamil **94 / 94** sections `verified` | **94 / 94** sections `source-checked`; whole-Part bilingual review, glossary reconciliation, release/readiness **PASS / CLOSED** for Parts 001–016 | Parts **001–016 FINAL CLOSED / FROZEN**; book ends at Part016 / scan 477; unresolved blockers **0** | **READY_NEW_CANONICAL** (with provenance qualification, §12) | +1 Fiction |
| N2 | ரோமாபுரிப் பாண்டியன் (`romapuri-pandian`) | `kalaignar-novels-2` | 183 page records (167 verified · 16 needs-review) | 28 sections so far | Parts 001–010 of **39** supplied (root README); review work continuing | NOT_COMPLETE | 0 |
| N3 | பொன்னர் சங்கர் (`ponnar-sankar`) | `kalaignar-novels-3` | 225 page records (215 verified · 10 needs-review) | 26 sections so far | Parts 001–003 closed; Part 004 Pass 1 in progress; Parts 005–008 pending | NOT_COMPLETE | 0 |
| N4 | தென்பாண்டிச் சிங்கம் (`thenpandi-singam`) | `kalaignar-novels-4` | 215 page records (186 verified · 29 needs-review) | 33 sections so far | Parts 007–018 pending | NOT_COMPLETE | 0 |
| N5 | ஒரே இரத்தம் (`ore-ratham`, 1980, `TVA_BOK_0064094`) | `kalaignar-novels` `works/ore-ratham` (added during this census) | 0 / 136 page records | not started | source intake / setup only | NOT_COMPLETE | 0 |

Existing novels (`arumbu`, `balipeedam-nokki`, `nadutheru-narayani`, `periya-idathup-pen`, `pudhaiyal`,
`sarapallam-samundi`, `surulimalai`, `vellikkizhamai`) are ALREADY_ONBOARDED.

### 5.2 Assembly speeches — `நிதிநிலை அறிக்கை மீது கலைஞரின் சட்டமன்ற உரைகள் (பாகம் - 1)` (2007)

Controlling source `TVA_BOK_0065523_நிதிநிலை_அறிக்கை_மீது_கலைஞரின்_சட்டமன்ற_உரை_1.pdf` · SHA-256
`e2bc9965ae2f03008e85abaedd7f601971a5699d8a92c044e9bd2346496c3932` · 546 physical pages · தமிழ்க்கனி பதிப்பகம், May 2007.
The archive's completed-source handover states: **"All 19 mapped speech units have completed their applicable archival
workflow."** Per-unit `metadata.json` confirms, for **all 19**: `transcription.status = verified`,
`translation.status = verified`, `release.status = released` (Gate H PASS).

Reconciliation: the live catalogue holds 15 works from this repository (10 industries debates, `udhaya-kathir`,
`namathu-nilai`, `1971-namathu-vilakkam`, the two 1973 `இருளும் ஒளியும்` replies). **None of the 19 Part-1 units is a
LibraryWork.**

| உரை | Printed date | Source scans | Archive dir / subtree | Identity finding | Class | Δ cat. |
|---:|---|---|---|---|---|---:|
| 1 | 5.3.1958 | 18–24 | `speeches/1958/1958-03-05-financial-statement-debate` `e2fb0f07` | new dated Assembly speech | **READY_NEW_CANONICAL** | +1 |
| 2 | 4.3.1959 | 25–33 | `1959-03-04-…` `31f5e707` | new | **READY_NEW_CANONICAL** | +1 |
| 3 | 16.3.1960 | 34–42 | `1960-03-16-…` `fd6060f0` | new | **READY_NEW_CANONICAL** | +1 |
| 4 | 6.3.1961 | 43–48 | `1961-03-06-…` `e3251ecf` | new | **READY_NEW_CANONICAL** | +1 |
| 5 | 2.7.1962 | 49–59 | `1962-07-02-…` `a86da0f6` | new | **READY_NEW_CANONICAL** | +1 |
| 6 | 7.3.1963 | 60–75 | `1963-03-07-…` `09bb238d` | new (≠ `1963-03-21-industries-debate`) | **READY_NEW_CANONICAL** | +1 |
| 7 | 7.3.1964 | 76–89 | `1964-03-07-…` `a79ced59` | new | **READY_NEW_CANONICAL** | +1 |
| 8 | 4.3.1966 | 90–112 | `1966-03-04-…` `5a4ea587` | new | **READY_NEW_CANONICAL** | +1 |
| 9 | 29.3.1971 | 113–116 | `1971-03-29-…` `055eb9d7` | `is_parallel_witness: true` → the 29-3-1971 Assembly event inside **`namathu-nilai`** (an edited two-House booklet that the library holds as one canonical work) | **HOLD_OWNER_DECISION** | 0 or +1 |
| 10 | 29.6.71 | 117–151 | `1971-06-29-…` `d441a002` | `is_parallel_witness: true` → the 29-6-1971 Assembly event inside **`1971-namathu-vilakkam`** | **HOLD_OWNER_DECISION** | 0 or +1 |
| 11 | 10.3.1972 | 152–190 | `1972-03-10-…` `a21e1fbb` | new | **READY_NEW_CANONICAL** | +1 |
| 12 | 07.03.1973 | 191–230 | `1973-03-07-financial-statement-debate` `449239ab` | **independent parallel witness** of the existing canonical `1973-03-07-financial-statement-reply` (archive keeps the reply as the sole same-date canonical record) | **READY_WITNESS_OR_RELATION** | 0 |
| 13 | 14.03.1974 | 231–262 | `1974-03-14-…` `a83c268f` | new | **READY_NEW_CANONICAL** | +1 |
| 14 | 10.03.1975 | 263–319 | `1975-03-10-…` `e1b0c36c` | new | **READY_NEW_CANONICAL** | +1 |
| 15 | 03.08.1977 | 320–355 | `1977-08-03-…` `0fc532f8` | new | **READY_NEW_CANONICAL** | +1 |
| 16 | 1.3.1978 | 356–388 | `1978-03-01-…` `f3089acc` | new | **READY_NEW_CANONICAL** | +1 |
| 17 | 22 & 23.3.1979 | 389–481 | `1979-03-22-and-23-financial-statement-debate` `8000d33f` | new; **multi-date source unit** — `date: null`, not in single-date indexes by design; **no single canonical date may be invented** | **READY_NEW_CANONICAL** (qualified) | +1 |
| 18 | 09.07.1980 | 482–510 | `1980-07-09-…` `22296ae5` | new | **READY_NEW_CANONICAL** | +1 |
| 19 | 06.03.1982 | 511–545 | `1982-03-06-…` `90d64938` | new | **READY_NEW_CANONICAL** | +1 |
| C | — | 1–546 | `sources/2007-financial-statement-speeches-part-1` `aed25d1a` | anthology container (collection / publication surface or none) | **HOLD_OWNER_DECISION** | 0 |

Result: **16 READY_NEW_CANONICAL** (1–8, 11, 13–19), **1 READY_WITNESS_OR_RELATION** (12), **2 HOLD_OWNER_DECISION** (9,
10). The 2007 anthology itself is a publication container (`HOLD_OWNER_DECISION`, §8). It is **not** mechanically 19 new
works.

### 5.3 Public speeches

Reconciliation: 115 speech directories at the live head; **102** are LibraryWorks (5 standalone + முத்துக் குளியல் I 61
+ II 36). The 13 directories that are not LibraryWorks are classified below (plus one duplicate workspace, §10).

**புராணப்போதை — 1958 multi-speech booklet** (`collections/puranappothai-1958`; `TVA_BOK_0024505`; SHA-256
`3af4d1ba35742975fd3308f199f5e70bcdf0fb0ac3d8d6381a237cad39916785`; 102 scans; முன்னேற்றப் பண்ணை, முதல் பதிப்பு: பிப்ரவரி
1958). Collection status **FINAL-CLOSED / FULLY ARCHIVED — 6/6 constituents FINAL CLOSED / RELEASE READY**, Tamil 6/6 and
English 6/6 `verified-complete`. The booklet introduction says these are written forms of speeches delivered at
various places in Chennai; **no constituent-specific date or venue is established** (none may be inferred). Duplicate
gate PASS (later 1987/2004 குட்டிக் கதைகள் collections are distinct sources).

| # | Constituent | PDF / printed | Pages | Archive dir / subtree | Class | Δ cat. |
|---:|---|---|---:|---|---|---:|
| P1 | குட்டிக் கதைகள்! குரங்காட்டம்! | 8–28 / 7–27 | 21 | `kuttik-kathaigal-kurangaattam` `b8a32d30` | **READY_NEW_CANONICAL** | +1 |
| P2 | சடுகுடு விளையாட்டா? சவால் சண்டையா? | 29–45 / 28–44 | 17 | `sadugudu-vilaiyaatta-savaal-sandaiya` `b36e0ada` | **READY_NEW_CANONICAL** | +1 |
| P3 | மீண்டும் கிளைவ் ? | 46–51 / 45–50 | 6 | `meendum-clive` `1a4ad5b0` | **READY_NEW_CANONICAL** | +1 |
| P4 | ‘பங்கீடு’ ஒழிப்பு! பகவான் மீது பாரம்! | 52–65 / 51–64 | 14 | `pangeedu-ozhippu-bhagavan-meethu-baram` `08ed95cd` | **READY_NEW_CANONICAL** | +1 |
| P5 | கேள்விக் குறி! | 66–79 / 65–78 | 14 | `kelvik-kuri` `e1a3250b` | **READY_NEW_CANONICAL** | +1 |
| P6 | புராணப் போதை! | 80–101 / 79–100 | 22 | `puranap-pothai` `0794b595` | **READY_NEW_CANONICAL** | +1 |
| PC | புராணப்போதை (container) | 1–102 | — | `collections/puranappothai-1958` `29a321ad` | **READY_COLLECTION** (model decision, §14) | 0 (collections +1 if a `LibraryCollection`) |

**Standalone public speeches:**

| # | Candidate | Source | Tamil / English | Identity finding | Class | Δ cat. |
|---:|---|---|---|---|---|---:|
| S1 | காஞ்சிபுரம் — மொழிப்போர் தியாகிகளின் வீர வணக்க நாள் கூட்டத்தில் ஆற்றிய வீர உரை (`kaanchipuram-mozhippor-thiyagigal-veera-vanakka-naal-urai`, subtree `37c6e334`) | `TVA_BOK_0065743`; speech body PDF 26–41 (16 pp.) | T1/T2/T3 complete-verified; E1/E2/E3 complete, `verified_complete: true`; **FINAL CLOSED / RELEASE READY** | new; date not stated (do not infer); venue காஞ்சிபுரம். The booklet's PDF 1–23 reproduce the existing Murasoli letter **`m46-l3606`** «விஷம்; ஒரு துளி போதாதா?» (2012-02-03) and are excluded from the speech body | **READY_NEW_CANONICAL** | +1 |
| S1-R | booklet PDF 1–23 ↔ `murasoli-letters` letter `m46-l3606` | same | — | witness of an existing letter | **READY_WITNESS_OR_RELATION** (optional) | 0 |
| S2 | களத்தில் கருணாநிதி (`kalathil-karunanidhi`, subtree `024c04c9`) | `TVA_BOK_0064241`; 76 pp. | T1/T2/T3 76/76 PASS; E1 + fidelity review 76/76 PASS; **FINAL CLOSED / RELEASE READY** | new; **23-12-1951**, ராபின்சன் பார்க், சென்னை (from the PDF4 preface); இளங்கோ பதிப்பகம், மாயூரம், முதற்பதிப்பு—52 | **READY_NEW_CANONICAL** (qualified: one printed folio `not-positively-readable`) | +1 |
| S3 | வரலாற்றுச் சுவடு (`varalattru-suvadu`, subtree `76e187ee`) | DMK Head Office 'அறிவகம்' publication; 33 scans; speech pp. 4–25 (22) | Tamil `verified-complete` / FROZEN (58 corrections / 0 unresolved); English `verified-complete` (E2 PASS, E3 PASS); `archive_status: closed` | new; venue மதுரை அமெரிக்கன் கல்லூரி; date not stated | **READY_NEW_CANONICAL** | +1 |
| S4 | கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழா உரை — ஒலிப்பதிவு 06 (`kalaivanar-nsk-memorial-day-audio-06`, subtree `4b43b13b`) | Tamil Digital Library audio `002_06`; 00:26:22.080; SHA-256 `6f0149229196b1d6df092d9fee006253591afec7ba9512bfbeb46dd0ab82c836` | T2 43/43 PASS; T3 verified-complete / FROZEN; E3 PASS; **FINAL CLOSED / RELEASE READY** (was NOT_COMPLETE at Wave 7) | a **different binary** from the onboarded `kalaivanar-nsk-memorial-day` (00:07:23.559); date/venue not established; whether it is a separate speech or another/longer recording of the **same memorial-day event** is **not established** by the source | **HOLD_OWNER_DECISION** | 0 or +1 |

**முல்லைக் கொல்லை — 1954 compiled booklet** (`collections/mullaik-kollai-1954`; `TVA_BOK_0064364`; SHA-256
`1e14d215de1b109292ba2b2ba03f73cf844978d2d6b1bb4f912c3ca64733a15f`; 80 scans). Collection status **ACTIVE**.

| # | Constituent | PDF | State | Class | Δ cat. |
|---:|---|---|---|---|---:|
| M1 | முல்லைக் கொல்லை (`mullaik-kollai`, `70750e0f`) | 7–18 | FINAL CLOSED / RELEASE READY (2026-09-27) | **HOLD_OWNER_DECISION** | 0 until decided |
| M2 | அத்தை மகள் (`aththai-magal`, `1983bd7a`) | 19–47 | FINAL CLOSED / RELEASE READY (2026-09-28) | **HOLD_OWNER_DECISION** | 0 until decided |
| M3 | நம் மேடை (`nam-medai`, `950a525a`) | 48–56 | Tamil T1 complete; T2 Batch 1 in progress; `release_readiness: not-ready` | NOT_COMPLETE | 0 |
| M4 | “கைத்தறி வாங்கலையோ” | 57–62 | not started (no archive directory) | NOT_COMPLETE | 0 |
| M5 | இலட்சிய இதழ்கள் | 63–67 | not started (no archive directory) | NOT_COMPLETE | 0 |
| MC | முல்லைக் கொல்லை (container) | 1–80 | booklet active | NOT_COMPLETE | 0 |

M1–M2 are held (not READY) because the parent booklet is still active, **and** the source back-matter records that at
least one piece appeared in `திராவிடன்` (December 1952) — whether these are speeches, articles or another form is an
owner/IA question the archive explicitly leaves open (it records no speech date, venue or event). PDF 69–70 («‘முரசொலி’
துப்பாக்கி») is supplementary author text outside the contents list and is not a constituent.

### 5.4 Murasoli letters (existing `murasoli-letters` work)

| # | Candidate | Tamil | English | Class | Δ cat. |
|---:|---|---|---|---|---:|
| L1 | **Volume 1** (22.10.1968–01.12.1974; `volumes/volume-01`, `ffa292a7`) — `Vol1.pdf`, SHA-256 `02eda7e7bb74d6d611351319ea87bc7761df6e9c5e73cc28883940b62d1fc6df`, 401 pp.; சீதை பதிப்பகம், 2022 | 401 / 401 structural + visual/textual-fidelity **PASS**; letters **110 / 110** complete (`chapters/` 110 × `status: complete`) | **110 / 110 FINAL RELEASE COMPLETE**; bilingual alignment 110 / 110 | **READY_COVERAGE_EXPANSION** of `murasoli-letters` (qualified, §12) | 0 |
| L2 | Volume 41 (25.11.2007–21.01.2009; `e1c5fd49`) | 151 / 402 page records; 14 / 58 letters (3306–3319) + 3320 partial | BLOCKED pending Tamil gates | NOT_COMPLETE | 0 |

Volumes 42–54 are ALREADY_ONBOARDED under `murasoli-letters`. (The source archive's Volume 49 still records its second
visual/textual-fidelity gate as pending; the public payload for 48–54 predates this archival format — recorded for
information, no Wave-9 action.)

### 5.5 Quotes

| # | Candidate | Source state | Class | Δ cat. |
|---:|---|---|---|---:|
| Q1 | கலைஞரின் சின்னச் சின்ன மலர்கள் (`chinna-chinna-malargal`, `b4a8380c`) | `TVA_BOK_0065639`, 249 pp.; **497 / 497** quote records — 496 `verified_from_scan` + **1 `needs_review` (`KQ-CCM-0391`, a physical blemish obscures one terminal glyph — a permanent source-limited exception)**; indexes 497/497; English 497/497 reviewed and published; `COMPLETION.md` durable status complete. Unchanged since the Wave-7 pin. | **HOLD_OWNER_DECISION** — source readiness **complete with qualification**; blocked only by the product/IA decision (the Digital Library has no Quotes shelf; nine Reading Room categories) | 0 (a tenth category is not implied) |

### 5.6 Adaptations

| # | Candidate | State | Class | Δ cat. |
|---:|---|---|---|---:|
| A1 | கலைஞரின் கவிதை நடையில் கார்க்கியின் 'தாய்' காவியம் (`thaai-kaaviyam`) | 3 processing Parts reported; only Part 001 (scans 1–135) registered; 135 page records (60 verified · 75 needs-review); Pass 2A batches 001–006 (through scan 60); no English | NOT_COMPLETE | 0 |

## 6. Canonical identity reconciliation (post-R3 568-work catalogue)

- **Proposed new canonical ids (27 = 26 works + 1 collection)**, all the source's own slugs, **0 collisions** with any
  existing work id, slug, publication id or collection id:
  `payumpuli-pandaraka-vanniyan`; `1958-03-05-financial-statement-debate`, `1959-03-04-…`, `1960-03-16-…`,
  `1961-03-06-…`, `1962-07-02-…`, `1963-03-07-…`, `1964-03-07-…`, `1966-03-04-…`, `1972-03-10-…`, `1974-03-14-…`,
  `1975-03-10-…`, `1977-08-03-…`, `1978-03-01-…`, `1979-03-22-and-23-financial-statement-debate`, `1980-07-09-…`,
  `1982-03-06-…`; `kuttik-kathaigal-kurangaattam`, `sadugudu-vilaiyaatta-savaal-sandaiya`, `meendum-clive`,
  `pangeedu-ozhippu-bhagavan-meethu-baram`, `kelvik-kuri`, `puranap-pothai`;
  `kaanchipuram-mozhippor-thiyagigal-veera-vanakka-naal-urai`, `kalathil-karunanidhi`, `varalattru-suvadu`;
  collection `puranappothai-1958`.
  (The assembly ids follow the live precedent of the ten `*-industries-debate` works.)
- **No READY_NEW_CANONICAL candidate duplicates an existing LibraryWork** by source path, id, date or normalized title
  (the only title-prefix hits were unrelated: Audio-06 ↔ its sibling, held; காஞ்சிபுரம் ↔ an unrelated முத்துக் குளியல் II
  wedding speech).
- **Witness relations** (no new work): உரை 12 ↔ `1973-03-07-financial-statement-reply`; காஞ்சிபுரம் booklet PDF 1–23 ↔
  `murasoli-letters` / `m46-l3606`.
- **Held identities:** உரை 9 ↔ `namathu-nilai`; உரை 10 ↔ `1971-namathu-vilakkam`; Audio-06 ↔ `kalaivanar-nsk-memorial-day`.
- The frozen R3 merges are not reopened; the five merged stories remain merged witnesses.

## 7. READY population

| Class | Count | Members |
|---|---:|---|
| READY_NEW_CANONICAL | **26** | N1 (Fiction 1) · 2007 உரை 1–8, 11, 13–19 (Speeches 16) · புராணப்போதை P1–P6 (Speeches 6) · S1, S2, S3 (Speeches 3) |
| READY_COLLECTION | **1** | PC — புராணப்போதை container |
| READY_COVERAGE_EXPANSION | **1** | L1 — Murasoli Volume 1 |
| READY_WITNESS_OR_RELATION | **2** | உரை 12 ↔ 1973-03-07 reply; காஞ்சிபுரம் booklet PDF 1–23 ↔ `m46-l3606` |

Qualified READY items: N1 (source-hash provenance gaps), உரை 17 (multi-date, no single canonical date), S2 (one printed
folio not positively readable), L1 (stale metadata field; non-contiguous coverage) — §12.

## 8. HOLD / owner-decision population — 7

| # | Item | Why held |
|---:|---|---|
| H1 | 2007 உரை 9 (29.3.1971) | new dated canonical speech, or parallel witness of the booklet-level work `namathu-nilai`? The source archive indexes it as the dated record and marks it a parallel witness; the library models the booklet as the canonical work. |
| H2 | 2007 உரை 10 (29.6.1971) | same question against `1971-namathu-vilakkam`. |
| H3 | Audio-06 | separate canonical speech, or witness/longer recording of the same memorial-day event as `kalaivanar-nsk-memorial-day`? Not established by the source. |
| H4 | `chinna-chinna-malargal` | source complete (qualified); needs an explicit Quotes publication / shelf / reader decision (no tenth category is assumed). |
| H5 | முல்லைக் கொல்லை M1 | parent booklet active; form (speech vs article, «திராவிடன்» 1952 provenance) and shelf undecided. |
| H6 | அத்தை மகள் M2 | same as H5. |
| H7 | 2007 Part-1 anthology container | should the anthology be a `LibraryCollection` (as முத்துக் குளியல்) given that 1 unit is a witness, 2 are held and 1 is multi-date? Or no container record? |

## 9. NOT_COMPLETE population — 10

N2 ரோமாபுரிப் பாண்டியன் · N3 பொன்னர் சங்கர் · N4 தென்பாண்டிச் சிங்கம் · N5 ஒரே இரத்தம் · L2 Murasoli Volume 41 · A1
`thaai-kaaviyam` · M3 நம் மேடை · M4 “கைத்தறி வாங்கலையோ” · M5 இலட்சிய இதழ்கள் · MC முல்லைக் கொல்லை (container).

## 10. ALREADY_ONBOARDED, witness-only and coverage ledger (outside the candidate total)

- **All 568 canonical works** (see §1); the 11 publication records; the 9 collections.
- **Previously deferred items now resolved:** `sangatamil` (Wave-7 NOT_COMPLETE → onboarded Wave 8); `ore-mutham`
  (Wave-7 HOLD → onboarded Wave 8); `1970-09-09-no-confidence-motion` (listed among Wave-7 NOT_COMPLETE items 4–9) is
  live as `udhaya-kathir`; Wave-7 NOT_COMPLETE items 4–8 (1958–1962 financial-statement debates) are now **READY**
  (§5.2); `payumpuli-pandaraka-vanniyan` and Audio-06 have closed (§5).
- **Murasoli Volumes 42–54** — live under `murasoli-letters`.
- **The five R3-D merged stories** — active merged witnesses (not new work).
- **Source collections of `kalaignar-short-stories` without a public collection** (`1950-vazha-mudiyathavargal`,
  `1953-naadum-naadagamum`, `1953-thappivittargal`, `1956-thaaymai`, `1958-thenalaigal`, `1969-kannadakkam`,
  `1976-nalayini`, `1979-pazhakkoodai`, `1997-dravida-iyakka-ezhuthalar-sirukathaigal`) — witness/provenance containers
  decided in Waves 6–7; the repository is unchanged since the Wave-7 pin; not re-proposed.
- **`nenjukku-needhi-archive`, `tolkappiyap-poonga`, `kalaignar-cinema-works` (incl. `kalaignar-thirai-isai-paadalgal`),
  `kalaignar-stage-plays`, `kalaignar-essays`, `kalaignar-poems`, `kalaignar-literary-commentary`** — every work
  directory maps to an existing LibraryWork or publication record; unchanged since their last census.
- **Duplicate workspace / source-path drift (observation, no Wave-9 action):** the source repository deduplicated C37 on
  2026-09-19 (`5bcf6854`, "deduplicate C37"): the directory the live LibraryWork `pazhaiya-varalaarum-ilaiya-thalaimuraiyum`
  pins (`speeches/pazhaiya-varalaarum-ilaiya-thalaimuraiyum` at `6ca57fe2…`) no longer exists at the live head; the
  surviving directory is the former variant `speeches/pazhaiya-varalarum-ilaiya-thalaimuraiyum`. The library's pinned
  commit still contains the path, so nothing is broken; any future re-pin must follow the surviving directory.

## 11. Projected catalogue delta (P0 projection — NOT current state)

| Shelf | Current | READY_NEW_CANONICAL only | If every HOLD later resolves to a new work |
|---|---:|---:|---:|
| Life Writing | 1 | 1 | 1 |
| Letters | 3 | 3 | 3 |
| Fiction | 157 | **158** | 158 |
| Poetry | 173 | 173 | 173 |
| Drama | 11 | 11 | 11 |
| Cinema Writing | 10 | 10 | 10 |
| Speeches | 118 | **143** (+16 +6 +3) | up to 146 (+ H1, H2, H3) |
| Essays & Articles | 91 | 91 | shelf of H5/H6 undecided (+2 on some shelf) |
| Literary Commentary | 4 | 4 | 4 |
| **Total** | **568** | **594** (+26) | up to **599** (+31); H4 would additionally need a new category |

Collections: **9 → 10** if புராணப்போதை becomes a `LibraryCollection` (11 if the 2007 anthology container is also
approved). Publication records: **11**, unchanged unless a container is modelled as a publication record. Murasoli
remains **one** work; Volume 1 changes coverage only (Volumes 1 + 42–54).

## 12. Route / sitemap implications (P0 projection — derived from live route patterns)

Live patterns: a speech = `/speeches/<slug>` + `/source` (2 routes); a novel = landing + `/source` + one route per
section (e.g. `surulimalai` = 28); a Murasoli letter = 1 route; a collection = 1 route.

| Input | Projected routes |
|---|---:|
| N1 Payumpuli (94 sections incl. front matter) | ≈ 96 |
| 25 READY speeches × 2 | 50 |
| L1 Murasoli Volume 1 (110 letters) | 110 |
| PC புராணப்போதை collection page | 1 |
| **Total (READY only)** | **≈ 257** → sitemap **≈ 5528** (from 5271) |

Every figure is a projection; the stage PR that implements an input must derive and freeze its own counts from a clean
build. No route is added, removed or redirected by this P0.

## 13. Source-condition qualifications and drift

- **N1 Payumpuli — provenance.** Controlling-source SHA-256s are recorded in the Part final-closure records for **Parts
  009–016 only**; the monolithic PDF hash and the Part 001–008 split hashes remain **PENDING** in `metadata/source.md`
  (sizes and exact filenames are recorded for all 16). P1 must carry recorded hashes only; never invent one. The historic
  `270→271` "PENDING direct audit" notes are superseded by the Part-010 boundary audit (**GENUINE CONTINUATION / AUDITED
  / PASS**). Edition: ராக்போர்ட் பப்ளிகேஷன்ஸ், முதல் பதிப்பு 1991; `TVA_BOK_0065744`.
- **2007 உரை 17** — two printed dates (22 & 23.3.1979), no internal date divider: `date: null`; no single date may be
  invented or used for ordering/indexing as though single.
- **2007 உரை 9 / 10 / 12** — the archive's own parallel-witness declarations are authoritative; no released layer of
  the 1971 booklets or the 1973 reply may be modified.
- **புராணப்போதை** — the source prints February 1958 (a user-supplied 1953 is recorded as a discrepancy, not adopted); no
  constituent date or venue.
- **S2 களத்தில் கருணாநிதி** — one printed folio is `not-positively-readable` (a recorded source exception).
- **L1 Murasoli Volume 1** — `metadata.yml` still carries `transcription_status: "first-pass-complete"`, stale against
  the README's audited final status; P1 must re-derive statistics from the records, not from that field. Coverage after
  import would be **non-contiguous** (1, then 42–54). The legacy `volumes/volume-1/` tree is migration evidence only;
  `volumes/volume-01/` is canonical.
- **Q1** — `KQ-CCM-0391` permanent source-limited `needs_review`.
- **Drift during census (reconciled):** `kalaignar-novels` `3ff1c707` → `408100aa` (new `works/ore-ratham` intake →
  N5 NOT_COMPLETE; Payumpuli subtree unchanged `31e135ca`); `kalaignar-public-speeches` `38683790` → `c184b4df`
  (நம் மேடை T2 Batch 1 — M3 still NOT_COMPLETE); `kalaignar-adaptations` `3a78a08e` → `0379184c` (Pass 2A to scan 60 —
  A1 still NOT_COMPLETE); at the pre-PR re-fetch, `kalaignar-novels-2` `10e0da65` → `30c16def` (ரோமாபுரிப் பாண்டியன்
  review commit "Part011 Pass2B batch1", 10 page/control files — N2 still NOT_COMPLETE), `kalaignar-novels-3` `b6070f1a` → `165bcde6` (பொன்னர் சங்கர் Part 004
  Pass 1 Batch 1, scans 216–225 — N3 still NOT_COMPLETE; this archive is actively advancing) and `tolkappiyam-arivagam`
  `16123f74` → `15fdb00d` (application/editorial work — still out of scope). No READY classification changed.

## 14. Explicit Wave-9 P1 questions (owner decisions; P1 is NOT authorized)

1. **Scope:** which READY segments should P1 take, and in what order (e.g. Payumpuli; 2007 Assembly Part-1; புராணப்போதை;
   three standalone speeches; Murasoli Volume 1)?
2. **2007 உரை 9 and 10:** new dated canonical speeches, or witness relations of `namathu-nilai` /
   `1971-namathu-vilakkam`?
3. **Audio-06:** separate canonical speech, or witness of `kalaivanar-nsk-memorial-day`?
4. **புராணப்போதை container:** a `LibraryCollection` (as முத்துக் குளியல்), a publication record, or constituents only?
5. **2007 Part-1 anthology container:** a collection/publication surface, or constituents only?
6. **Quotes (`chinna-chinna-malargal`):** authorize a Quotes publication model (a tenth category or another surface), or
   keep HOLD?
7. **முல்லைக் கொல்லை:** wait for the whole booklet, or onboard closed constituents individually; and on which shelf
   (speeches vs essays/articles) given the «திராவிடன்» 1952 provenance?
8. **Murasoli Volume 1:** accept non-contiguous coverage (1 + 42–54) of the one `murasoli-letters` work?
9. **Optional witness relations:** record உரை 12 and the காஞ்சிபுரம் booklet's letter reproduction as relation records?
10. **Maintenance (separate authorization):** re-pin `pazhaiya-varalaarum-ilaiya-thalaimuraiyum` provenance after the
    source's C37 deduplication?

## 15. Census totals and lifecycle

```
READY_NEW_CANONICAL            26
READY_COLLECTION                1
READY_COVERAGE_EXPANSION        1
READY_WITNESS_OR_RELATION       2
HOLD_OWNER_DECISION             7
NOT_COMPLETE                   10
--------------------------------
TOTAL CANDIDATES               47
```

Outside the 47: ALREADY_ONBOARDED (568 works, 11 publications, 9 collections, Murasoli 42–54), the witness/duplicate
ledger (§10) and out-of-scope repositories (§2).

Consistency checks: 26 = 1 + 16 + 6 + 3; 2007 Part-1 = 16 + 1 + 2 = 19; புராணப்போதை 6 + container; முல்லைக் கொல்லை 2
HOLD + 3 NOT_COMPLETE + container; projected catalogue 568 + 26 = 594; Speeches 118 + 25 = 143; Fiction 157 + 1 = 158.

**WAVE 9 — OWNER-AUTHORIZED. P0 COMPLETED-WORKS / READINESS CENSUS — REVIEW-READY. P1 NOT STARTED / NOT AUTHORIZED.**
Waves 6, 7 and 8 remain COMPLETE / CLOSED / FROZEN AT P5. Reading Room IA v2 R0–R3 remain frozen and are not reopened.
Implementation delta **0** · source delta **0** · production delta **0**.
