# Reading Room IA v2 — Owner HOLD Adjudication

**Created:** 2026-09-25.

**Status: READING ROOM IA v2 OWNER HOLD ADJUDICATION — COMPLETE / REVIEW-READY.**
**R2 — NOT STARTED / NOT AUTHORIZED.**

This is a **post-R1, control-only owner-adjudication stage**:
- implementation delta = **0**;
- source delta = **0**;
- production mutation = **0**.

It records the owner's decisions for all 34 frozen R1 HOLD rows as a **new overlay layer**. It creates no LibraryWork,
deletes or redirects nothing, and changes no catalogue, route, reader, sitemap or `/read`.

The machine-readable overlay is
[`READING_ROOM_IA_V2_RESOLVED_MANIFEST.json`](./READING_ROOM_IA_V2_RESOLVED_MANIFEST.json):
- 315 rows;
- every frozen R1 row is copied verbatim, plus the overlay fields `r1Decision`, `ownerDecisionRef` and `resolved`.

## 1. Live pins

| Item | Value |
|---|---|
| Control `pugazg/kalaignar-tribute` `main` (base) | `62739aac68ce28ba1a41c41f242288afea8f603e`, tree `64d17e3a3cb4bc2c00e4c2bb7f3a477cc2b07455` |
| Implementation `pugazg/kalaignar-autobiography` `main` | `f991043c3353abe9f2b334f7c8d57e433184d126` (0 open PRs; no R2 / IA-v2 branch) |
| Production | Vercel Production deployment `6638432286` for `f991043c…` |
| `kalaignar-poems` | `188d49cd4dcf2c6bbe2e9633841ff402b9959d08` (= live `main`); Wave-4 pin `969823195ea8943a67fad4286ab1bc7f1c876d56` |
| `kalaignar-literary-commentary` | `e23548b09547a2308407e60e5e67c1a03fee5354` (= live `main`), tree `2302d1fc6cbe9386a8010b344a9caba2f4913fa4` |
| `kalaignar-essays` | live `main` `63019a4d…`; the Meesai pin used is `b5fd2922898a56a8b6a75bf564bdfa91cd22869a` |
| `kalaignar-short-stories` | `7205a10892d0b208df2617766844f480b6a2c798` (= live `main`) |

All sources were read-only. `kalaignar-assembly-speeches` `main` advanced independently (owner source work) and is
not used by this stage.

## 2. Frozen R1 authority

| Frozen file | Blob (unchanged by this stage) |
|---|---|
| `READING_ROOM_IA_V2_R0_CENSUS.md` | `cee919231e161be1ee7335b30853e82b6e34e4f7` |
| `READING_ROOM_IA_V2_R1_IDENTITY_RECONCILIATION.md` | `42de6fa05049bf042c4d0e831fc69f188606d375` |
| `READING_ROOM_IA_V2_R1_MANIFEST.json` | `7013177259d8914258397a2894bdf299ae4c0f14` |
| `READING_ROOM_IA_V2_R1_TEXT_OVERLAP_EVIDENCE.json` | `34ff3b1b02fd2813919b48afe006e35262dbf065` |

Frozen R1 totals: 315 entries = CREATE 218 · KEEP_EXISTING 27 · ADD_WITNESS 16 · DO_NOT_PROMOTE 20 · HOLD 34. The
R1 floor was 553 and the raw upper bound 587.

## 3. R1 itself remains frozen

**R1 is not reopened or rewritten.** R0 and R1 remain COMPLETE / REVIEWED / FROZEN, and their files are byte-identical.
The owner decisions exist only in this record and in the resolved-manifest overlay. The frozen R1 manifest remains the
historical record of what R1 decided.

## 4. Methodology

1. **Authority.** The owner's decisions (§5) are explicit authority for identity, canonical choice and shelf.
2. **Source checks.** Where the owner's decision rests on a source relationship, the relationship was checked against
   direct source files at the pins above. No outside web source was used.
3. **Deterministic generation.** The resolved manifest was generated deterministically from the frozen R1 manifest:
   - the 34 HOLD rows were matched by `family|key`;
   - the generator fails unless each target is a unique HOLD row;
   - canonical ids reuse the frozen key; on a collision with a live id, slug or collection id, or an R1 proposed or
     reserved id, a deterministic shelf suffix is added:
     - `-kavithai` (Poetry) and `-katturai` (Essays), as in R1;
     - `-kaditham` (Letters) and `-urai` (Speeches), extended here.
4. **Proof of change scope.** Removing the overlay fields from every resolved row reproduces the frozen R1 row exactly,
   for all 315 rows. The 281 non-HOLD rows carry a `resolved` object that mirrors the frozen decision, classification,
   shelf and subtype, with `adjudicated: false`.

## 5. Owner decision groups (explicit owner authority)

| Ref | Decision | HOLD rows |
|---|---|---:|
| OD1 | `ஒருதலைக் காதல்` is canonical. `அன்பால் அவனை விலைகொள்ள முடியுமோ?` (Kaalap 37) is an alternate/reprinted witness of its opening (section-1) material | 1 |
| OD2 | `கேட்டுண்டோ?` is canonical. `பொதுவுடைமையே!` and `யோசித்துப் பார்!` are witnesses | 3 |
| OD3 | `பச்சைக் கிளி` is canonical, on Poetry. Meesai 14 remains a witness, and the existing Fiction work `சிறை கொடியது` becomes a witness | 1 |
| OD4 | Meesai 1, 2 and 13 are canonical. The shorter, later 2004 stories are witnesses | 3 |
| OD5 | `சொர்க்க லோகத்தில்` is canonical. The later `சொர்க்கத்திற்கு வந்தது எப்படி?` is a witness; the shelf stays Essays & Articles | 1 |
| OD6 | The 1958 `தேனலைகள்` and Meesai 16–26 are the same underlying book/content under different titles with the chapter order changed. The 11 units are canonical (Poetry, `எழுத்தோவியம்`) | 11 |
| OD7 | The remaining 11 Meesai `எழுத்தோவியங்கள்` are canonical Poetry | 11 |
| OD8 | The two letter-form pieces are canonical Letters (not Murasoli corpus) | 2 |
| OD9 | `துடிக்கும் இளமை` is a canonical Speech | 1 |
| **Total** | | **34** |

## 6–8. The 34 original HOLD rows: before → after, and witness targets

Every row below was frozen as `HOLD` in R1. Each appears exactly once.

| # | Ref | Family / R1 key | Tamil title | R1 → resolved | Canonical id | Shelf / subtype | Witness / R2 note |
|---:|---|---|---|---|---|---|---|
| 1 | OD1 | poetry-kaalap / `can-he-be-bought-with-love` | அன்பால் அவனை விலைகொள்ள முடியுமோ? | HOLD → **ADD_WITNESS** | `oruthalaik-kathal` | poetry / poem (reprinted witness) | witness of existing `oruthalaik-kathal` |
| 2 | OD2 | poetry-kavithaigal / `have-you-heard` | கேட்டுண்டோ? | HOLD → **CREATE** | `have-you-heard` | poetry / poem | witness rows: ina-muzhakkam-poem-05, ina-muzhakkam-poem-06 |
| 3 | OD3 | poetry-kavithaigal / `green-parrot` | பச்சைக் கிளி | HOLD → **CREATE** | `green-parrot` | poetry / poem | witness rows: pachchaikkili; R2: merge existing `sirai-kodiyathu` as witness |
| 4 | OD5 | ina-prose / `sorgga-logaththil` | சொர்க்க லோகத்தில் | HOLD → **CREATE** | `sorgga-logaththil` | essays-articles / essay | R2: merge existing `sorgaththirku-vandhathu-eppadi` as witness |
| 5 | OD2 | ina-poem / `ina-muzhakkam-poem-05` | பொதுவுடைமையே! | HOLD → **ADD_WITNESS** | `have-you-heard` | poetry / poem (witness) | witness of proposed `have-you-heard` |
| 6 | OD2 | ina-poem / `ina-muzhakkam-poem-06` | யோசித்துப் பார்! | HOLD → **ADD_WITNESS** | `have-you-heard` | poetry / poem (witness) | witness of proposed `have-you-heard` |
| 7 | OD8 | essays-sinthanaiyum-seyalum / `paasiyum-thoosiyum` | பாசியும் - தூசியும்! | HOLD → **CREATE** | `paasiyum-thoosiyum` | letters / letter | — |
| 8 | OD8 | essays-sinthanaiyum-seyalum / `athiga-uyaram-thaanduvatharku` | அதிக உயரம் தாண்டுவதற்கு | HOLD → **CREATE** | `athiga-uyaram-thaanduvatharku` | letters / letter | — |
| 9 | OD9 | essays-thudikkum-ilamai / `thudikkum-ilamai` | துடிக்கும் இளமை | HOLD → **CREATE** | `thudikkum-ilamai-urai` | speeches / public-speech | — |
| 10 | OD4 | meesai / `piraiye` | பிறையே | HOLD → **CREATE** | `piraiye` | poetry / ezhuthoviyam | R2: merge existing `neeyum-kaithi-naanum-kaithi` as witness |
| 11 | OD4 | meesai / `adikkaatru` | ஆடிக்காற்று | HOLD → **CREATE** | `adikkaatru` | poetry / ezhuthoviyam | R2: merge existing `aadik-kaatre` as witness |
| 12 | OD7 | meesai / `karuppu-pen` | கருப்புப் பெண் | HOLD → **CREATE** | `karuppu-pen` | poetry / ezhuthoviyam | — |
| 13 | OD7 | meesai / `kadale` | கடலே | HOLD → **CREATE** | `kadale` | poetry / ezhuthoviyam | — |
| 14 | OD7 | meesai / `aaru` | ஆறு | HOLD → **CREATE** | `aaru` | poetry / ezhuthoviyam | — |
| 15 | OD7 | meesai / `vaazhiya-vaikarai` | வாழிய வைகறை | HOLD → **CREATE** | `vaazhiya-vaikarai` | poetry / ezhuthoviyam | — |
| 16 | OD7 | meesai / `agappai-siththar` | அகப்பை சித்தர் | HOLD → **CREATE** | `agappai-siththar` | poetry / ezhuthoviyam | — |
| 17 | OD7 | meesai / `malaiye-vaazhi` | மலையே வாழி | HOLD → **CREATE** | `malaiye-vaazhi` | poetry / ezhuthoviyam | — |
| 18 | OD7 | meesai / `thalir` | தளிர் | HOLD → **CREATE** | `thalir` | poetry / ezhuthoviyam | — |
| 19 | OD7 | meesai / `vinmeen` | விண்மீன் | HOLD → **CREATE** | `vinmeen` | poetry / ezhuthoviyam | — |
| 20 | OD7 | meesai / `thanimai` | தனிமை | HOLD → **CREATE** | `thanimai` | poetry / ezhuthoviyam | — |
| 21 | OD7 | meesai / `naadaga-medai` | நாடக மேடை | HOLD → **CREATE** | `naadaga-medai` | poetry / ezhuthoviyam | — |
| 22 | OD4 | meesai / `pugazh` | புகழ் | HOLD → **CREATE** | `pugazh` | poetry / ezhuthoviyam | R2: merge existing `pugazhe-nee-oru-pudhir` as witness |
| 23 | OD7 | meesai / `tamizhe` | தமிழே | HOLD → **CREATE** | `tamizhe` | poetry / ezhuthoviyam | — |
| 24 | OD6 | meesai / `thenalaigal` | தேனலைகள் | HOLD → **CREATE** | `thenalaigal` | poetry / ezhuthoviyam | 1958 publication |
| 25 | OD6 | meesai / `thozhi` | தோழி | HOLD → **CREATE** | `thozhi` | poetry / ezhuthoviyam | 1958 chapter — அலை 5 |
| 26 | OD6 | meesai / `maruthaani` | மருதாணி | HOLD → **CREATE** | `maruthaani` | poetry / ezhuthoviyam | 1958 chapter — அலை 6 |
| 27 | OD6 | meesai / `aruvi` | அருவி | HOLD → **CREATE** | `aruvi` | poetry / ezhuthoviyam | 1958 chapter — அலை 7 |
| 28 | OD6 | meesai / `muram` | முறம் | HOLD → **CREATE** | `muram` | poetry / ezhuthoviyam | 1958 chapter — அலை 8 |
| 29 | OD6 | meesai / `yaazh` | யாழ் | HOLD → **CREATE** | `yaazh` | poetry / ezhuthoviyam | 1958 chapter — அலை 9 |
| 30 | OD6 | meesai / `sirpi` | சிற்பி | HOLD → **CREATE** | `sirpi` | poetry / ezhuthoviyam | 1958 chapter — அலை 10 |
| 31 | OD6 | meesai / `seval-sandai` | சேவல் சண்டை | HOLD → **CREATE** | `seval-sandai` | poetry / ezhuthoviyam | 1958 chapter — அலை 11 |
| 32 | OD6 | meesai / `madal` | மடல் | HOLD → **CREATE** | `madal` | poetry / ezhuthoviyam | 1958 chapter — அலை 4 |
| 33 | OD6 | meesai / `aandu-vizha` | ஆண்டு விழா | HOLD → **CREATE** | `aandu-vizha` | poetry / ezhuthoviyam | 1958 chapter — அலை 12 |
| 34 | OD6 | meesai / `mayiliragu` | மயிலிறகு | HOLD → **CREATE** | `mayiliragu` | poetry / ezhuthoviyam | 1958 chapter — அலை 2 |

**HOLD transitions:** HOLD → CREATE **31**; HOLD → ADD_WITNESS **3** (Kaalap 37, ina 6.5, ina 6.6).

**Witness targets:**
- Kaalap 37 → existing `oruthalaik-kathal`.
- ina 6.5 and 6.6 → proposed `have-you-heard`.
- Meesai 14 (frozen ADD_WITNESS, unchanged) → proposed `green-parrot`, which is now CREATE.

All witness targets resolve deterministically, whether to a live LibraryWork or to a CREATE id in this manifest.

## 9. Future R2 merge actions for existing LibraryWorks (not performed here)

Five existing Fiction LibraryWorks are to stop being separate canonical identities and become witnesses or versions
of the newly selected canonical works.
- They are **not** mutated, deleted or redirected in this stage.
- All five are members of the 2004 anthology `2004-kalaignarin-kuttik-kathaigal`. R2 must preserve that membership
  as a witness or publication appearance, and must preserve their routes.

| Existing LibraryWork id (live, exact) | Title | Current route | Canonical target | Ref |
|---|---|---|---|---|
| `sirai-kodiyathu` | சிறை கொடியது | `/stories/sirai-kodiyathu` | `green-parrot` (Poetry) | OD3 |
| `neeyum-kaithi-naanum-kaithi` | நீயும் கைதி - நானும் கைதி | `/stories/neeyum-kaithi-naanum-kaithi` | `piraiye` (Poetry) | OD4 |
| `aadik-kaatre` | ஆடிக் காற்றே! | `/stories/aadik-kaatre` | `adikkaatru` (Poetry) | OD4 |
| `pugazhe-nee-oru-pudhir` | புகழே நீ ஒரு புதிர் | `/stories/pugazhe-nee-oru-pudhir` | `pugazh` (Poetry) | OD4 |
| `sorgaththirku-vandhathu-eppadi` | சொர்க்கத்திற்கு வந்தது எப்படி? | `/stories/sorgaththirku-vandhathu-eppadi` | `sorgga-logaththil` (Essays & Articles) | OD5 |

Each id was resolved from the live implementation catalogue (`f991043c`) by exact Tamil title, with exactly one match
each.

**Additional witness links, not merges:**
- Kaalap 37 → `oruthalaik-kathal` (its own row).
- Sangatamil sections 092–102 → `oruthalaik-kathal` (provenance only; §10).
- The 1958 `தேனலைகள்` → Meesai 16–26 (an external publication witness; not a LibraryWork; §11).

## 10. Sangatamil ↔ `ஒருதலைக் காதல்`: verified

**Source.** `kalaignar-literary-commentary@e23548b0` `works/sangatamil`:
- Page `0425-kaikkilai-oruthalaik-kaadhal-divider.md` is a full-page divider.
- It is followed by the 11 numbered sections `092`–`102` (`oruthalaik-kaadhal-01` … `-11`, source pages 0426–0496).
- The divider **visibly reads `ஒருதலைக் காதல்`**. Its Gate-B source note removes the unsupported repository heading
  `கைக்கிளை`, which survives only in the file name. This record therefore does not claim a printed `கைக்கிளை` heading.

**Comparison.** The standalone `oruthalaik-kathal` (11 sections) was compared with the 11 Sangatamil sections in a full
11×11 matrix (8-character shingle containment; a comparison aid, not authority).
- **Every Sangatamil section's best match is the same-numbered standalone section.**
- Diagonal containment ranges from 0.922 to 0.985 (listed below); off-diagonal values are 0.071 at most; section sizes
  are near-identical.

| Sangatamil section | Best standalone match | Diagonal | Next best | Shingles (Sangatamil / standalone) |
|---|---:|---:|---:|---|
| sangatamil §01 (6 pages) | §1 | 0.939 | 0.044 | 5168 / 5197 |
| sangatamil §02 (6 pages) | §2 | 0.979 | 0.058 | 4249 / 4261 |
| sangatamil §03 (7 pages) | §3 | 0.922 | 0.064 | 6138 / 6176 |
| sangatamil §04 (6 pages) | §4 | 0.934 | 0.049 | 4405 / 4419 |
| sangatamil §05 (5 pages) | §5 | 0.985 | 0.041 | 3680 / 3652 |
| sangatamil §06 (7 pages) | §6 | 0.948 | 0.066 | 6058 / 6068 |
| sangatamil §07 (6 pages) | §7 | 0.936 | 0.067 | 4377 / 4394 |
| sangatamil §08 (7 pages) | §8 | 0.961 | 0.051 | 5655 / 5669 |
| sangatamil §09 (7 pages) | §9 | 0.945 | 0.067 | 5929 / 5947 |
| sangatamil §10 (8 pages) | §10 | 0.962 | 0.07 | 6327 / 6358 |
| sangatamil §11 (6 pages) | §11 | 0.977 | 0.071 | 4649 / 4661 |

**Result: CONFIRMED on direct evidence.**
- The canonical work remains `ஒருதலைக் காதல்` (`oruthalaik-kathal`).
- The standalone poetry publication and the Sangatamil `ஒருதலைக் காதல்` sequence are publication/source witnesses
  of the same canonical work, in the same order, with source-witness variants.
- **Sangatamil remains one Literary Commentary LibraryWork. No Sangatamil section becomes a LibraryWork.**

## 11. 1958 `தேனலைகள்`: owner determination and mapping

**Owner manual determination (OD6).** The 1958 `தேனலைகள்` (`TVA_BOK_0064030`, December 1958) and Meesai 16–26 are the
same underlying book/content, issued under different book titles with the chapter order changed.
- No further transcription is required to establish the publication identity.
- `SOURCE_LIMITED_UNRESOLVED` is retired for these rows.

**Mapping** (1958 headings from `kalaignar-short-stories@7205a108` `collections/1958-thenalaigal/README.md`):

| 1958 அலை | Heading | PDF scans | Printed pp. | Meesai unit | Level |
|---:|---|---|---|---|---|
| 1 | முத்தாரம் | 7–17 | 1–11 | 16 `thenalaigal` | publication-only (indicated, not mapped) |
| 2 | மயிலிறகு | 18–29 | 12–23 | 26 `mayiliragu` | chapter |
| 3 | முத்துமாலை | 30–38 | 24–32 | — (no established counterpart) | unmapped |
| 4 | மடல் | 39–44 | 33–38 | 24 `madal` | chapter |
| 5 | தோழி | 45–52 | 39–46 | 17 `thozhi` | chapter |
| 6 | மருதாணி | 53–60 | 47–54 | 18 `maruthaani` | chapter |
| 7 | அருவி | 61–67 | 55–61 | 19 `aruvi` | chapter |
| 8 | முறம் | 68–74 | 62–68 | 20 `muram` | chapter |
| 9 | யாழ் | 75–82 | 69–76 | 21 `yaazh` | chapter |
| 10 | சிற்பி | 83–95 | 77–89 | 22 `sirpi` | chapter |
| 11 | சேவல் சண்டை | 96–104 | 90–98 | 23 `seval-sandai` | chapter |
| 12 | ஆண்டு விழா | 105–111 | 99–105 | 25 `aandu-vizha` | chapter |

**12-headings versus 11-units bookkeeping.** This is a mapping and documentation matter, not a HOLD.
- **10 chapter-level links** rest on the owner's same-book determination, exact heading-title identity and consistent
  extent (about 556–776 Meesai characters per 1958 printed page, as recorded in frozen R1).
- **Meesai 16 `தேனலைகள்`** is recorded as a **publication-level** witness only.
  - Its text indicates அலை 1 `முத்தாரம்`: it closes `பின்னர் இரவெல்லாம் முத்தாரம் தொடுத்தார் இருவருமே!` and mentions
    முத்தாரம் three times and முத்துமாலை once.
  - No heading carries its title, so no chapter relation is asserted.
- **அலை 3 `முத்துமாலை`** has **no established Meesai counterpart**. No relation is invented.

## 12. Meesai Poetry / `எழுத்தோவியம்` treatment

**All 25 formerly-HOLD Meesai units** (OD4 ×3, OD6 ×11, OD7 ×11) resolve to:
- shelf **Poetry**;
- one stable internal subtype, **`ezhuthoviyam`**;
- the public form label **`எழுத்தோவியம்`** — poetic sketch / prose-poem, a hybrid poetic form that is not forced into a
  conventional metrical-poem model.

Meesai 14 stays the settled witness of `green-parrot` (Poetry).

**Source-supported rationale** (Meesai front matter at `kalaignar-essays@b5fd2922`, pages `0004`–`0016`):
- The foreword and preface use **`கவிதை`** 14 times, **`கவிதைப்பறவை`** (page 0009), **`கவிஞனின்`** and **`கவிஞராக`**.
- They call **`கடலே`** "**கடல் என்ற கவிதை**" (page 0010).
- The author's own preface uses `எழுத்தோவிய…` and `சொல்லோவியம்`.
- The pieces combine apostrophe, personification, sustained metaphor, lyrical imagery, rhythmic prose or verse, poetic
  allegory and condensed social/political argument.

**Form notes:**
- `தனிமை` — a dialogue-form poetic allegory, not a stage play.
- `அகப்பை சித்தர்` — an allegorical poetic sketch, not a separate short story.
- `நாடக மேடை` — a poetic meditation on theatre, not a Drama LibraryWork.

## 13. Resolved arithmetic

```
Resolved (315 rows): CREATE 249 · KEEP_EXISTING 27 · ADD_WITNESS 19 · DO_NOT_PROMOTE 20 · HOLD 0
249 + 27 + 19 + 20 + 0 = 315
Frozen R1 → resolved: CREATE 218 → 249 (+31) · ADD_WITNESS 16 → 19 (+3) · HOLD 34 → 0
New CREATE by shelf: Poetry 162 · Essays & Articles 84 · Letters 2 · Speeches 1
```

CREATE / ADD_WITNESS by family (resolved):

| Family | CREATE | ADD_WITNESS |
|---|---:|---:|
| poetry-standalone | 0 | 2 |
| poetry-kaalap | 57 | 1 |
| poetry-kavithaigal | 74 | 3 |
| poetry-1975 | 3 | 0 |
| ina-prose | 5 | 0 |
| ina-poem | 3 | 8 |
| essays-kolaikkalam | 6 | 0 |
| essays-perumoochu | 13 | 0 |
| essays-sinthanaiyum-seyalum | 50 | 0 |
| essays-thiraavida-sampaththu | 2 | 0 |
| essays-thudikkum-ilamai | 2 | 2 |
| essays-unarchchimaalai | 9 | 1 |
| meesai | 25 | 1 |
| existing-publication-or-work | 0 | 1 |

All 249 CREATE ids are unique, with **0** collisions against the live catalogue.

## 14. Provisional catalogue arithmetic (not final)

```
Raw add-only projection      = 335 + 249 = 584
Existing-work canonical merges (future R2; §9)  = 5
Provisional canonical-net projection = 584 − 5 = 579
```

**579 is provisional and pre-R2. It is not the final website count.** Later IA work may change how publication and
container LibraryWorks are represented.

Add-only shelf view (584):
```
Life Writing 1 · Letters 1 + 2 = 3 · Fiction 162 · Poetry 14 + 162 = 176 · Drama 11 · Cinema Writing 10
· Speeches 117 + 1 = 118 · Essays & Articles 15 + 84 = 99 · Literary Commentary 4
1 + 3 + 162 + 176 + 11 + 10 + 118 + 99 + 4 = 584
```

Net view (579): the five merges reduce Fiction from 162 to 157.

## 15. HOLD = 0

- **All 34 original HOLD rows have owner decisions.**
- **The resolved manifest has HOLD = 0.**
- The frozen R1 manifest still records HOLD = 34, as history.

## 16. Status

**READING ROOM IA v2 OWNER HOLD ADJUDICATION — COMPLETE / REVIEW-READY.**
- R0 — COMPLETE / REVIEWED / FROZEN.
- R1 — COMPLETE / REVIEWED / FROZEN.
- Waves 6–8 — COMPLETE / CLOSED / FROZEN at P5.

**R2 — NOT STARTED / NOT AUTHORIZED.** HOLD = 0 does **not** authorize R2. R2 requires independent review and merge of
this adjudication plus separate explicit owner authorization.
