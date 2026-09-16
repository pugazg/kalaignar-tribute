# Wave 6 — Batch 7 (Short Stories) — Deterministic Canonical Manifest

**Created:** 2026-09-16 · **Control-only census refresh. No implementation, payload, route, catalogue, source, or control-programme change is authorized by this document.**

Batch 7 is **one combined implementation batch** = **all currently completed canonical short-story works** in `pugazg/kalaignar-short-stories` that are **not yet implemented**. The internal source/provenance groups below are **validation partitions only**, not separate implementation batches (the old B7–B11 split is superseded). **Batch-7 P1 has NOT started.**

## Source freeze (live re-verified 2026-09-16)

| Item | Value |
|---|---|
| Source repo | `pugazg/kalaignar-short-stories` |
| Source `main` commit | `7205a10892d0b208df2617766844f480b6a2c798` |
| Source `main` tree | `1be34cc368fbc96ff72933a004a074ef840168ee` |
| `stories/` subtree | `0898900e58e07b4fba941ba13080b6b1bcfa62f8` |
| `collections/` subtree | `9a6afcdc2efb6970a23435a6a75cff794ffbf3e1` |

## Deterministic reconciliation (why the count is exact)

`stories/` holds **154** canonical short-story work directories. Of these, **38 are already implemented** in `pugazg/kalaignar-autobiography` (the 37-member 1977 anthology `1977-kalaignar-karunanidhiyin-sirukathaigal` + the standalone `kizhavan-kanavu`). The remaining **116** are the Batch-7 population:

```
154 stories/ dirs − 37 (1977 anthology members) − 1 (kizhavan-kanavu) = 116 Batch-7 canonical works
```

Cross-checked three independent ways, all = 116:
1. `154 − 38 already-implemented = 116`.
2. Sum of the source/provenance group counts below: `40 + 34 + 23 + 5 + 6 + 3 + 2 + 1 + 1 + 1 = 116`.
3. The ten group slug-sets are pairwise disjoint and their union has exactly 116 unique slugs, none of which is a 1977-anthology member or `kizhavan-kanavu`.

## Count derivation by internal validation/provenance group

| # | Source group | Source PDF id | `collections/<dir>` subtree SHA | New canonical works | Closure (Tamil/source · English) |
|---:|---|---|---|---:|---|
| 1 | 2008 `கலைஞர் சொன்ன கதைகள்` | `TVA_BOK_0065857` | `8e1d32ca52140bd4eed7bb5efc97b2c1e7eebac5` | **40** | 40/40 PASS · 40/40 PASS — CLOSED |
| 2 | 2004 `கலைஞரின் குட்டிக் கதைகள்` | `TVA_BOK_0065567` | `a5d4a2005fb15b585023923bfa0f552c3e286bff` | **34** | 34/34 PASS · 34/34 PASS — CLOSED |
| 3 | 1987 `கலைஞர் சொன்ன குட்டிக் கதைகள்` (2nd ed.) | `TVA_BOK_0065566` | `c5ad6dc4caf787d79175f7a83ef3fef1c9d74fde` | **23** | Tamil/source PASS / CLOSED — 25/25 identities resolved as 23 distinct canonicals + 2 witness-only. English 25/25 PASS / CLOSED; the 2 witness-only entries use 1987 witness-local English and do not overwrite controlling canonical English. |
| 4 | 2009 `16 கதையினிலே` | `TVA_BOK_0065745` | `4cd568ad0cdb58698dae5671936d184cec35b807` | **5** | 5/5 PASS · 5/5 PASS — CLOSED (11 existing-canonical witnesses separate) |
| 5 | 1982 `முடியாத தொடர்கதை` | `TVA_BOK_0065572` | `126630867369f525934092b40dda20e667b49ffa` | **6** | Tamil/source CLOSED · English CLOSED |
| 6 | Periodical canonicals (3 magazines) | — | (story-local, under `stories/`) | **3** | Each Tamil/source CLOSED · English CLOSED |
| 7 | 1976 `நளாயினி` | `TVA_BOK_0065574` | `6ff2a5d25bd3d925774c6f098e963940d29e5efb` | **2** | 2/2 PASS · 2/2 PASS — CLOSED (6 witnesses separate) |
| 8 | 1969 `கண்ணடக்கம்` | `TVA_BOK_0064095` | `b6b61ffbf60d3ddfbf23c3d3495362945389d6b3` | **1** | Tamil/source CLOSED · English CLOSED (source closed under the only available copy) |
| 9 | 1953 `தப்பிவிட்டார்கள்` | `TVA_BOK_0064098` | `f1f4f496c46f86fba10b3a531a1363e2572d15b9` | **1** | Tamil/source CLOSED · English CLOSED (3 witnesses separate) |
| 10 | 1997 `திராவிட இயக்க எழுத்தாளர் சிறுகதைகள்` | `TVA_BOK_0064315` | `6a904c1023a97ccfa7cd3392c81a3332dadbb52f` | **1** | Tamil/source PASS · English PASS — CLOSED (8 existing-canonical witnesses + 1 cross-repo exclusion separate) |
| | **TOTAL** | | | **116** | |

`40 + 34 + 23 + 5 + 6 + 3 + 2 + 1 + 1 + 1 = 116`.

## Newly completed canonicals since the old census (old 103 → 116, delta **13**)

The 2026-09-08 P0 census counted 103 (`2008 40 + 2004 34 + 1987 23 + 2009 5 + 1997 1`). The following **13** completed since and are added here:

- **1982 (6):** `petra-pillaiyai-vitra-thaai`, `kaasa-lesa`, `seemaan-veettu-seekkaali`, `nandiyur-nariyappan`, `nariyur-nandiyappan`, `mudiyatha-thodarkathai`. (**`நந்தியூர் நரியப்பன்` and `நரியூர் நந்தியப்பன்` are SEPARATE canonical stories — never collapse.**)
- **1976 (2):** `naattiya-kalarani`, `maanam`.
- **Periodical (3):** `seerazhitha-sirippu` (காஞ்சி பொங்கல் மலர் 1966), `madurai-selavu` (முரசொலி பொங்கல் மலர் 1960), `kondru-varuga` (முரசொலி பொங்கல் மலர் 1952).
- **1969 (1):** `neruppu`.
- **1953 `தப்பிவிட்டார்கள்` (1):** `vilaiyal-vangalaiyo`.

`6 + 2 + 3 + 1 + 1 = 13`.

---

## The exact 116 canonical work identities (slugs = `stories/<slug>/`)

### Group 1 — 2008 (40)
`antha-naal-vanthilai` · `appadithan-sirippen` · `aththiri-paachaa` · `edukkavo-kokkavo` · `ezhuchikku-adaiyaalam` · `ice-katti` · `idhayam-pesugirathu` · `idikkup-pin-mazhai` · `iramanai-patri-iraman` · `jaadi-kutti-poduma` · `kadamai-kanniyam-kattuppadu` · `kaniyum-kanaiyum` · `kannil-kaal` · `kazhuthaiyin-kathai` · `koottani` · `maanum-perumaanum` · `mamiyar-udaithaal-mattum-manchattiya` · `mayil-ravanan` · `naakkuth-tamil-manakkum` · `nadakkuma-nadakkatha` · `nalvazhiyum-nalla-vazhiyum` · `nandri-sollum-neram` · `neethi-devathaiye` · `onnu-kuduma` · `paarur-pola` · `panithuliyil-panai-maram` · `panthalile-paagarkai` · `porumaikku-saandru` · `pulivaal` · `saavi-thaan-illai` · `seera-vendama` · `seruppodu-iru` · `thalaiyil-malai` · `thalaiyum-nuniyum` · `thamizan-endru-sollada` · `theriyatha-pechu` · `thum-pam-theem-thom` · `unakku-vayathenna` · `vennai-uruguthu-veyilil` · `verum-kai-muzham-podum`

### Group 2 — 2004 (34)
`aabasame-aabasam` · `aadik-kaatre` · `aandavan-dharisanam-kodutha-oor` · `adutha-piraviyil-aindhu-kanavan` · `anthak-kaalathile` · `aval-sonnaal` · `ilamai-kaalam` · `ilangai-mannar-parambarai` · `iruvarum-koodiyiruppathu-aathi-maalaithaan` · `kadalai-thoorppathu-miga-elithu` · `kaithiyin-kathai` · `kalliyum-rojavum` · `kazhuthile-oru-mudichu-atharku-oru-kathai` · `kizhavanin-manaivi` · `kollappada-vendiyathu-puli-aanaal` · `kootruvan-eppadip-mariththaan` · `krishnanaiyum-vidaatha-saathi` · `kuruvi-rameswaram` · `malaiyai-thookkuven` · `manaivi-sonna-vilakkam` · `muthiyavar-theerppu` · `naatham-ezhaathu-narambuthaan-arum` · `neeyum-kaithi-naanum-kaithi` · `pengalukku-en-meesai-thadiyillai` · `pudhir` · `pugazhe-nee-oru-pudhir` · `sirai-kodiyathu` · `sorgaththirku-vandhathu-eppadi` · `thalaivanin-parisu` · `uyirukku-vilai-aimbathu-latcham` · `valluvar-sonna-poi` · `veeran-thalai-kavizhnthathu-en` · `veeravadi` · `vignaanikku-thondraathu`

### Group 3 — 1987 (23)
`agaththinai-anbu` · `buddhar-unarththiya-unmai` · `hajrath-aliyum-yuthanum` · `iru-nigazhvugal` · `jayathrathanin-veezhchi` · `kadu-sendra-kumanan` · `kajini-mugamathuvum-kavignar-pardosiyum` · `kurikkol` · `kuzhanthaiyum-kiliyum` · `mana-maatram` · `mannanum-kuruviyum` · `mooli-mookkukkaran` · `narayana-narayana` · `paalum-thanneerum` · `pugazhendhip-pulavar-kathai` · `samiyarum-pookkariyum` · `sorgaththirku-senruvantha-azhagi` · `thenaliraman-kathai` · `thenaliraman-poonai` · `thennai-marathil-pul` · `thuraviyum-seedargalum` · `valvil-ori` · `yasodhara-kaviyam`

### Group 4 — 2009 (5)
`anil-kunju` · `ezhuthalar-ekalaivan` · `gandhi-desam` · `kollaipuram` · `malaravillai`

### Group 5 — 1982 (6)
`petra-pillaiyai-vitra-thaai` · `kaasa-lesa` · `seemaan-veettu-seekkaali` · `nandiyur-nariyappan` · `nariyur-nandiyappan` · `mudiyatha-thodarkathai`

### Group 6 — Periodical (3)
`seerazhitha-sirippu` · `madurai-selavu` · `kondru-varuga`

### Group 7 — 1976 (2)
`naattiya-kalarani` · `maanam`

### Group 8 — 1969 (1)
`neruppu`

### Group 9 — 1953 `தப்பிவிட்டார்கள்` (1)
`vilaiyal-vangalaiyo`

### Group 10 — 1997 (1)
`nanbana`

---

## Witness-only source entries (do NOT become new LibraryWorks)

These source entries are **comparison witnesses** against an existing canonical; they carry no new work identity and are already excluded from the 116:

- **1987 (2):** `அராபியக் கதை` → witness of canonical `ஜாடி குட்டி போடுமா?` (`jaadi-kutti-poduma`, 2008); `குருவி ராமேஸ்வரம்` → witness of an existing 2004 canonical (`kuruvi-rameswaram`).
- **2009 (11):** eleven existing-canonical witnesses (comparison 11/11 CLOSED).
- **1997 (8):** `kuppai-thotti`, `ezhai`, `kannadakkam`, `sabalam`, `originalil-ullapadi`, `sangilichami`, `thothukkili`, `pretha-visaranai` — all pre-existing canonicals witnessed by the 1997 source.
- **1976 (6):** `நளாயினி`, `காதல் கடிதம்`, `புரட்சிப் படம்`, `விஷம் இனிது`, `பாலைவன ரோஜா`, `அய்யோ ராஜா!` — existing canonicals (48/48 witness pages CLOSED).
- **1953 `தப்பிவிட்டார்கள்` (3):** `தப்பிவிட்டார்கள்`, `சபலம்`, `முந்நூறு ரூபாய்` — existing-canonical witnesses.
- **1969 (witnesses):** `கண்ணடக்கம்`, `வேணியின் காதலன்`, `அமிர்தமதி` — existing canonicals witnessed.
- **Periodical:** `பனங்குலை` (`panangulai`, முரசொலி பொங்கல் மலர் 1977) — existing-canonical cross-witness, **not** a new canonical.
- **Provenance-only / zero-new-canonical source programmes:** 1950 `வாழமுடியாதவர்கள்` (6 witnesses), 1953 `நாடும் நாடகமும்` (5 witnesses + 2 non-short-story units), 1956 `தாய்மை` (witnesses), 1979 `பழக்கூடை` (5 witnesses). Each contributes **0** Batch-7 works.

## Cross-repository intentional exclusions (owner-clarified — do NOT reopen or count)

- **`தேனலைகள்` (1958 `தேனலைகள்`, `TVA_BOK_0064030`, `collections/1958-thenalaigal` subtree `44ab41e680d412f94d70a91d4d820ea1b99f85cc`):** the source contains **12 mapped headings** (transcription not started, DEFERRED). Per owner clarification, `தேனலைகள்` is **already represented in the essays / கட்டுரைகள் workstream under `மீசை முளைத்த வயதில்`**, so it was intentionally skipped in the short-story programme. Classification: **EXCLUDED — ALREADY REPRESENTED ELSEWHERE / CROSS-REPOSITORY OVERLAP.** Its 12 headings must **NOT** be added as Batch-7 short-story canonicals merely because the source exists; do not silently reopen. (The source repo's own note still calls them "new-canonical candidates"; that is superseded by the owner cross-repository clarification.)
- **`நடுத்தெரு நாராயணி`:** intentionally left out of the short-story onboarding programme because it is handled through the separate `அரும்பு` / short-novel source path (the source repo defers it to short-novel handling; it appears as a witness in 1956 `தாய்மை` and is deferred in the 1997 inventory). Classification: **EXCLUDED — represented via `அரும்பு` / short-novel handling.** Not in Batch 7. (No stronger identity claim than the source records support.)

Neither `தேனலைகள்` nor `நடுத்தெரு நாராயணி` inflates the Wave-6 short-story backlog.

## Collection-model audit (Batch-7 P1 decisions — not decided here)

Do not automatically make every source publication a public `LibraryCollection`. Recorded candidates:

| Source group | Suggested model | Note (owner decision at Batch-7 P1) |
|---|---|---|
| 2008 (40) | **public collection candidate** | one printed anthology; parallels the existing 1977 collection model |
| 2004 (34) | **public collection candidate** | one printed anthology |
| 1987 (23) | **public collection candidate** | one printed anthology (2nd ed. 1987) |
| 1982 (6) | **public collection candidate** | one printed anthology (6 stories) |
| 2009 (5) | **collection candidate — OPEN QUESTION** | Should collection membership include its 11 existing-canonical witnesses via the plural collection-membership model? **Flag as Batch-7 P1 owner decision.** |
| 1976 (2) | **provenance container / uncertain** | only 2 new canonicals inside an 8-story source; collection grouping unclear — Batch-7 P1 decision |
| 1953 `தப்பிவிட்டார்கள்` (1) | **provenance-only container** | single new canonical; not a public collection on its own |
| 1997 (1) | **NOT a public collection** | only `நண்பனா?` is new; do not create a collection solely because the source has 10 entries |
| 1969 (1) | **not a collection** | single new canonical (`neruppu`) |
| Periodical (3) | **not collections** | three standalone periodical stories |

Four disposition classes to carry into Batch-7 P1:
1. **canonical stories to onboard** — the 116 enumerated above;
2. **existing-canonical witnesses** — the witness list above (no new works);
3. **possible public collection grouping** — 2008 / 2004 / 1987 / 1982 (candidates) + the 2009 plural-membership open question;
4. **source/provenance-only containers** — 1950, 1953-naadum, 1956, 1979, 1997 (as a container), 1976 (as a container), 1953-thappivittargal (as a container), and the 1958/`நடுத்தெரு நாராயணி` exclusions.

## Status

- Batch-7 population: **116 canonical short-story works** (deterministic list above).
- Refreshed Wave-6 completed/READY population: **138** (`22` already-implemented non-short-story Wave-6 works + `116` Batch-7 short stories).
- **Batch-7 P1 has NOT started. Wave-6 P5 / P6 have NOT started.** No implementation, payload, route, catalogue, discovery, sitemap, source, or control-programme change is made by this manifest. Await explicit owner authorization.
