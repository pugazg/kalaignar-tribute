# New Chat Bootstrap Prompt — Kalaignar Digital Library / Claude Prompt Provider

Paste the following into a fresh ChatGPT window.

---

Continue as my **reviewer and prompt-provider for Claude Code** for the **Kalaignar Digital Library / Reading Room** at:

`https://nenjukkuneethi.org/read`

The native mobile app work is **ON HOLD**. Do not restart mobile development unless I explicitly reactivate it.

## Mandatory first step

Use the GitHub connector and read this file completely:

`pugazg/kalaignar-tribute/projects/kalaignar-digital-library/HANDOVER.md`

Then inspect the live implementation repository:

`pugazg/kalaignar-autobiography`

— its current `main`, its open PRs, and the deployed production site.

In order, every time: fetch live control `main` → read `HANDOVER.md` completely → fetch implementation
`main` → inspect open PRs in both repositories → check the deployed production site.

**Treat current GitHub `main`, open PRs and deployed site state as authoritative** over any SHA, count or status paragraph written in a handover, including this file.

## ⚠️ CURRENT STATE — 2026-09-04, post-Wave-5-P2 (cinema public readers; catalogue deferred) (supersedes everything below)

**The "Where the project actually stands" list further below stops at Phase 7 and is HISTORICAL.** Its
work and shelf counts are stale. **Live GitHub wins over anything in it.**

Measured at the current production boundary: implementation `main`
**`cf6a952ca9f0edea254d9c72b48ef333523bfd51`**, tree
**`9bf711784a86458f95a333c6f4c1768cbe65f690`**, **0 open implementation PRs**, **76 published works**
(**Cinema Writing 4** · **Poetry 6**), **1 collection**, **9 non-empty shelves**, **40 fully-expanded
`/read` discovery entries**, **32 initially visible discovery entries**, **3360 prerender-manifest
routes**, **3262 sitemap URLs**, **0 sitemap duplicates**, **147 `/poems/` URLs**. The continuity-only
prerendered `.html` figure is **3355** and is **not** the prerender-manifest route count.

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · **Poetry 6** · Drama 5 ·
**Cinema Writing 4** · Speeches 14 · Essays & Articles 4 · Literary Commentary 2. Total **76**.

**Bulk Onboarding Wave 5 — Cinema Writing is IN PROGRESS** (Manthiri Kumari + Raja Rani). **P0 census,
P1 source-freeze/data-foundation and P2 public readers are COMPLETE** (P1 PR #75 squash `7cc0546f…`;
P2 PR #76 squash `cf6a952c…`). P2 made both works directly readable — `/cinema/manthiri-kumari` (18
routes) and `/cinema/raja-rani` (71 routes), **+89 direct public routes**, all 200 with invalid children
404 — but kept them **out of the catalogue**: neither is in `data/library.ts`, `/read` discovery or the
sitemap, so works/discovery/sitemap are unchanged (only the build route count moved to prerender 3360 /
`.html` 3355). **Wave 5 is NOT closed** — **P3 (catalogue/discovery/sitemap exposure: works 76 → 78,
Cinema Writing 4 → 6) is the planned next stage but requires a separate owner authorization and has not
started.** See the Wave-5 section in `HANDOVER.md` for the frozen source pins, artifact hashes, route
contract and durable source semantics.

**Bulk Onboarding Wave 4 — Poetry is COMPLETE and CLOSED** (PRs #69–#73, durable close `ad998113…`).
All six frozen Poetry source workspaces are publicly represented; Poetry went 1 → 6 and the catalogue
71 → 76. The two Poetry **publications** — காலப் பேழையும் கவிதைச் சாவியும் (58 units) and கலைஞரின்
கவிதைகள் (77 units) — hold **135 internal reading units** between them; those units are **not**
LibraryWorks and **not** collection members, and the publications are **not** collections, so
collections stay **1**. Exactly **two** cross-witness relations link the same canonical poem across a
standalone witness and a publication-item witness. See the Wave-4 section in `HANDOVER.md` for the full
durable contract.

Since the Wave-4 close, one **post-Wave-4 production regression repair** merged (implementation PR #74,
squash `946dc8a510ef5f836eab2af15d3b2d69ee9360c2`): the shared publication landing paragraph hard-coded
"58 … numbered first part" onto the 77-poem கலைஞரின் கவிதைகள்; its description now derives count and
grouping from each publication's own approved structure, with regression tests for both publications in
both languages. It is **NOT Wave 5 and NOT a reopening of Wave 4** — no data, payload, witness, route or
catalogue change, zero inventory/route delta, implementation backlog back to **0**. It authorized no new
activity.

### ⚠️ Works are not discovery entries — and publication units are neither

Five numbers now describe this state and they are not interchangeable:

- **76 published works** — the archival catalogue (Poetry contributes 6);
- **40 discovery entries** — what `/read` renders fully expanded, because one collection entry stands
  in for 37 Fiction works;
- **32 initially visible entries** — of those 40, before any disclosure is opened;
- **135 internal Poetry publication units** — reading units inside the two publications; **not** works,
  **not** collection members;
- **3271 prerender-manifest routes / 3266 `.html` / 3262 sitemap URLs** — three separate build and delivery metrics.

**Fiction holds 39 works and renders 3 discovery entries.** Never write "40 works", never call Fiction a
3-work shelf, and never call a Poetry publication a collection.

### Reading Room Wayfinding — Phase 0 + Phase 1 — ✅ COMPLETE and CLOSED

The durable control close-out is the checkpoint established by control PR **#21**.

**Resolve this against live control `main`, as always.** If you are reading this file from the
close-out branch before #21 has merged, the closure is still only proposed and live `main` remains
authoritative. Once #21 is on `main` — which is where a fresh chat reads this file — Wayfinding is
durably closed and needs no further control action.

Two phases, both merged and production-verified:

- **Phase 0 — shelf progressive disclosure.** PR **#67**, approved head `13f313b0…`, squash merge
  **`1bc1123ecfcbdd181221cf34f558d3f7129d17e0`**, CI `33647284338`. A six-entry cap per shelf behind a
  native `<details>`/`<summary>`; no model change, no route, no data claim. Initially visible cards
  71 → 30 at that boundary; works unchanged.
- **Phase 1 — the 1977 anthology collection.** PR **#68**, approved head `ca217592…`, squash merge
  **`1c6dcd81f0aa143a8e9b3162976c74dd18791058`**, CI `33706978869`. The first collection layer:
  `1977-kalaignar-karunanidhiyin-sirukathaigal`, 37 members, ordinals 1–37, at
  `/collections/1977-kalaignar-karunanidhiyin-sirukathaigal`, frozen at source commit `76135e1b…` and
  collection tree `d45434d4…`. **The 37 stories remain 37 independent works** with their own routes.

Architectural rules that now bind: membership is canonical in `LibraryCollection.members` only;
reverse membership is **plural** — `collectionsForWork()`, never the stale singular `collectionForWork()`;
`memberCount` (works in a collection) is not `unitCount` (reading units in one work); and member
resolution **fails closed** rather than silently dropping an unresolved member.

Two review lessons worth carrying: a pre-existing shared token does **not** exempt a new interactive
control from accessibility review; and where theme or state variants coexist, proving a bad class is
**absent** is not enough — the test must positively prove the required good state is **present**.

### Kalaignar Film Songs — E1–E4 — ✅ COMPLETE and CLOSED

Work: **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs** (`kalaignar-thirai-isai-paadalgal`).
The implementation and publication were already live; this control checkpoint closes the deliberately
separate documentation lifecycle.

**Resolve the closure against live control `main`.** If this file is being read from the Film Songs
close-out branch before its control PR has merged, closure is still only proposed and live control
`main` wins. Once that PR is on `main`, Film Songs is durably closed and needs no further formal
control action. Any lower statement that the Film Songs close-out is still pending is a historical
snapshot superseded by this CURRENT section.

Frozen source: `pugazg/kalaignar-cinema-works` @
**`d6f3128381235e80891cc6647d19464b838f4103`**, path `works/kalaignar-thirai-isai-paadalgal`.
At close-out preparation, source `main` itself still equals that exact pin — **no repin**. Controlling
scan `TVA_BOK_0065867`, SHA-256
`f0beac14c33ffc73c0231bd54ca57ec4093eef6e85072bd68ce48f7b5e258b05`; earlier authorship witness
`TVA_BOK_0065773`, SHA-256
`56d414a65a61a73b990632eadc17a3b1efdc764d47f64b851060c161a3f98e3b`, used for authorship evidence
only and for **no lyric text**.

Final corpus: **23 films · 54 numbered lyrics · 1105 paired Tamil/English line-cues · 8 cross-page
songs** (9, 19, 23, 24, 36, 37, 51, 52). The front-matter incipit
`ஆளப்பிறந்தவன் தமிழன் அவனிதனிலே` has no numbered lyric body and is **not Song 55**.

The durable authorship rule is **authorship certainty != display eligibility**: all **54** numbered
lyrics are displayable; **48** have established Kalaignar authorship; exactly **6**, songs **013–018**
of **அம்மையப்பன்**, remain individually **unresolved** and require the source-controlled
`ammayappan-unresolved` notice. `unresolved` never means “not Kalaignar's”. Song 012 is separately
established and does not receive that notice.

Staged implementation, all merged:

| stage | PR | final reviewed head | squash merge | purpose |
|---|---:|---|---|---|
| E1 | #57 | `912dcc759d4a8951c0899e5378d8a4181a304a42` | `c5fae2abac15d3b1e4f07d22862c4e865596d870` | deterministic data import + source-linked validator |
| CI gate | #58 | `494a833bb51a7962713ae5aa319838a5621dd222` | `1cd8c66344660d0d8e70b9f057ad577dc6a76cc7` | run the Film Songs validator in Library CI |
| E2 | #59 | `82c1198632a77659d1c5d6ad4a608324e4edd660` | `5580fe5c26f76828ff8f6f1351197381a4577ea0` | landing + 54 lyric readers |
| E3 | #60 | `502f31a1f617510883209d4548179463d0aaff23` | `780d1e28e9cacd073a5d44073243b87642c7b06d` | Reading Room catalogue exposure |
| E4 | #61 | `a97fd4c8fed7fedf8946a514e3d40e8a2a300d7f` | `2712080873d51e7cfb020295e20d4c32da803a7c` | sitemap exposure |

Public reader shape: **film → lyric**. Routes are one landing plus `song-001`…`song-054` — **55 pages**.
There are no film-level pages, no Film Songs `/source` page, and no `song-055`. The sitemap likewise
contains exactly those 55 URLs, reading lyric slugs from the released registry rather than rebuilding
them numerically.

Archival provenance is deliberately outside the served tree at
`data/internal/thirai-isai-paadalgal/provenance.json`. E1's first pass put it under Next.js `public/`;
independent review correctly rejected that because a “build-time only” label cannot make a public
static asset private. The final public runtime holds only reader-needed data; the internal record keeps
the source pin/hashes, page mappings, credits, archival attribution and verification details needed for
deterministic validation. **Moved, not discarded.**

The catalogue's `unitCount: 54` is a **corpus count, not an authorship count**. Rights remain
intentionally unset: applying a blanket Kalaignar nationalisation status to all 54 would resolve six
unresolved authorship questions through a rights field. Display eligibility, authorship certainty and
rights are three separate facts. English coverage is complete and `project-created`, not an official,
historical-published or source-witness translation.

Final Film Songs validator: **155 assertions / 0 failed**. It remains in `npm run validate` and the
Library CI `archival validators` job under the named **Kalaignar Film Songs** step. Validator-contract
migration remains **PAUSED**; current board **3 registered / 13 pending / 16 total**.

Two review lessons remain durable: **filesystem placement is the real public/private boundary**, not a
comment describing intent; and E4's registry-driven sitemap was correct even though its original
comment gave a false reason — a numeric 001–054 loop would not invent an unnumbered item. The correct
reason is that the released registry is the route-set authority and remains correct if numbering later
has gaps or changes.

### NEXT ACTIVITY — Wave 5 P3, pending separate owner authorization

**Bulk Onboarding Wave 5 — Cinema Writing (Manthiri Kumari + Raja Rani) is IN PROGRESS.** P0 (census),
P1 (source freeze / hidden data foundation, PR #75 squash `7cc0546f…`) and P2 (public readers/routes/
`/source` pages, PR #76 squash `cf6a952c…`) are **COMPLETE**.

Status:

- **Wave 5 P0 census — COMPLETE.**
- **Wave 5 P1 source freeze + data foundation — COMPLETE** (hidden; generated data under
  `public/data/cinema/{manthiri-kumari,raja-rani}/`, not in `data/library.ts`).
- **Wave 5 P2 public readers/routes/`/source` pages — COMPLETE** (+89 direct public routes; Manthiri 18,
  Raja Rani 71; all 200, invalid children 404; catalogue/discovery/sitemap unchanged, so the two works
  are directly readable but undiscoverable from `/read`).
- **Wave 5 P3 (catalogue/discovery/sitemap exposure — add both works to `data/library.ts`, works
  76 → 78, Cinema Writing 4 → 6, sitemap exposure) — PLANNED NEXT STAGE, NOT YET AUTHORIZED to start.**
  P3 needs a separate explicit owner authorization; then P4 (regression hardening), P5 (production
  verification + Wave-5 control close-out).
- Wave 4 — Poetry and its post-Wave-4 regression repair remain COMPLETE and CLOSED.

Do **not** begin P3 implicitly, add either cinema work to `data/library.ts`, expose them in `/read`,
change Cinema Writing 4 → 6 or works 76 → 78, or modify the sitemap for them. Do not repin the Wave-5
freeze `75b22046…` merely because the cinema source `main` advances for unrelated work — both selected
work trees (`225662fc…` / `abbc5cb8…`) remain unchanged. Do not
reopen closed Wave-4 Poetry works or rewrite the 12 pinned Poetry payloads without a newly discovered,
source-backed regression. Any new wave, if authorized, must run its own read-only source census first.

Standing exclusions unchanged: validator migration **PAUSED**; native mobile **ON HOLD**; Manimagudam
is never auto-selected and requires its own readiness gate; `kalaivanar-nsk-memorial-day-audio-06`
is never auto-selected; Phase 2 discovery search, chronology, Tamil-first sorting, `/read/browse` and
any second collection remain unauthorized. Theme-bootstrap and existing WorkCard contrast remain
recorded follow-up debt, not automatic work.

## ⚠️ CURRENT STATE — 2026-09-02, post-Wave-3 ⚠️ SUPERSEDED (kept as history)

**Superseded by the CURRENT checkpoint above** and kept only as history; its route and sitemap
counts predate the collection route. Measured at the Wave-3 production boundary: implementation `main`
**`c4660c49edb20895d11751e4454942e46e8b0951`**, **0 open implementation PRs**, **71 published works**,
**Essays & Articles 4**, **9 non-empty shelves**, **3128 Next build static-route count**, **3116 sitemap
URLs**. The continuity-only prerendered `.html` figure is **3120** and is not the static-route count.

Shelf census: Life Writing 1 · Letters 1 · Fiction 39 · Poetry 1 · Drama 5 · Cinema Writing 4 ·
Speeches 14 · **Essays & Articles 4** · Literary Commentary 2. Total **71**.

### Bulk Onboarding Wave 3 — Essays & Articles — ✅ COMPLETE; control closure proposed

Exactly three publications were onboarded together:

- `கயிற்றில் தொங்கிய கணபதி` — 1 article;
- `உணர்ச்சிமாலை` — 10 articles;
- `திராவிட சம்பத்து` — 2 articles, damaged/out-of-order source.

Implementation PR **#66**. First reviewed head `d50aefae5cc5a665230a4185aab43d16c7dfeb81`
was **NOT APPROVED** despite green CI because `/source` route metadata still leaked the reference work's
14-article/reprint/rights claims. Repaired exact head
**`c4f40f7f77a115700915f17e65c2a2a1ddf54bbd`** was independently reviewed and APPROVED FOR MERGE.
Squash `c4660c49edb20895d11751e4454942e46e8b0951`; merged tree
`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`; post-merge CI **33607016982 success**; Vercel production
success. Approved-head and merged trees are identical.

Frozen source: `pugazg/kalaignar-essays` @
**`6814e979fd3c2cefa14cbeb17eeec28164ce28f5`** with per-work trees:
`ca1c92591b9389e60d44b9683af849e3a682e528` ·
`f49d77a0733ca75f7a96fb6a1cf4631e375b05d0` ·
`fe0f6ea0482ac2cd0e8c4558edd3b452e249dbdd`. At control-close-out preparation the live source had
advanced to `8d3b3e6792f6b3a7783ff3621f4d5c8e3e9be4d4` for `இன முழக்கம்`; all three Wave-3 work trees were
rechecked and remained exactly frozen. Do not repin Wave 3 to moving source `main`.

Wave 3 added **+19 public URLs** and moved 68 → 71 works, Essays 1 → 4, static routes 3109 → 3128,
`.html` 3101 → 3120 and sitemap 3097 → 3116. All 19 new routes and all 16 reference-work routes were
production-verified 200. Final batch validator: **510 assertions / 7 groups / 0 failed**, **23/23
negative tests proven**. Reference validator: **188 assertions / 0 failed**.

`திராவிட சம்பத்து` must retain article scan runs `5–6, 13–16` and `12, 3`, reconstructed reading
order `1 → 2 → 9 → 10 → 5 → 6 → 13 → 14 → 15 → 16 → 7 → 8 → 11 → 12 → 3 → 4`, no invented printed
pagination and no reconstruction of torn text. Its visible `/source` page summarizes those provenance
facts; the exact sequence/policy is available in deployed provenance rather than fully rendered as
visible rows.

**This control-only PR proposed the durable Wave-3 close-out. That close-out is historical and already
merged; the CURRENT section above governs today's state.**

### NEXT ACTIVITY AFTER THIS CONTROL CLOSE-OUT — HISTORICAL

The following old statement is retained as history: at the Wave-3 close-out, Wave 4 had not yet been
authorized and Film Songs control closure was still pending. **Both statuses are superseded by the
CURRENT section above.**

Standing historical exclusions at that checkpoint remain useful context: validator migration was
**PAUSED**; native mobile **ON HOLD**; Manimagudam required its own readiness gate; and
`kalaivanar-nsk-memorial-day-audio-06` was a separate source-active archive.

## ⚠️ CURRENT STATE — 2026-09-02, post-Wave-2 ⚠️ SUPERSEDED (kept as history)

**The "Where the project actually stands" list below stops at Phase 7 and is HISTORICAL.** Its work
and shelf counts are stale. It is kept for the completed-phase detail it records, and has not been
retro-edited. **Live GitHub wins over anything in it.**

Measured live 2026-09-02: implementation `main` **`4fd45a92663abbe70ff0c0a605168314cd36e44c`**,
**0 open PRs**, **68 published works**, **39 Fiction works**, **9 non-empty shelves**,
**3109 Next build static-route count**, **3097 sitemap URLs**.

Shelf census: Life Writing 1 · Letters 1 · **Fiction 39** · Poetry 1 · Drama 5 · Cinema Writing 4 ·
Speeches 14 · Essays & Articles 1 · Literary Commentary 2. Total **68**.

These were measured now — SHA and open PRs from live GitHub, the census from `data/library.ts` at
that SHA, static routes from a production build, sitemap from the deployed site — not copied
forward.

### ⚠️ Three different page metrics — never use them interchangeably

**A site-wide TOTAL is not a wave's DELTA.** Wave 2's public contribution is **+74 URLs**
(37 reader routes + 37 `/source` routes). The build's static-route count is a *site-wide census* of
every prerendered route in the whole library. Never present the two as the same kind of number.

| metric | how it is measured | pre-Wave-2 | post-Wave-2 | delta |
|---|---|---|---|---|
| **Next build static-route count** | the `Generating static pages (N/N)` figure | 3035 | **3109** | **+74** |
| **Sitemap URLs** | `<loc>` entries in the deployed `sitemap.xml` | 3023 | **3097** | **+74** |

The two differ because the build count includes non-HTML route outputs and four non-indexed pages
(`/_not-found`, `/about`, `/privacy`, `/support`).

⚠️ **The prerendered `.html` file count is NOT the Next static-route count** and must never be quoted
as one. Post-Wave-2 those are **3101** and **3109** respectively; at the Wave-1 boundary they were
3027 and 3035. The `.html` count is the older "Prerendered pages" convention, re-measured for
continuity (a pre-Wave-1 rebuild returns exactly 3005) but measuring a different thing, and it is
**deliberately not carried as a current metric**.

*(The previous **2026-09-01 post-Wave-1** line — `0dc92fa0…`, 31 works, Fiction 2, Drama 5, 3035
static routes, 3023 sitemap URLs — is **superseded** and kept only as history, as is the pre-Wave-1
line before it: `56ca0c97…`, 27 works, 3005 prerendered pages, 3001 sitemap URLs, Drama 1.)*

### Bulk Onboarding Wave 2 — Fiction — ✅ COMPLETE and CLOSED

**The 37 short stories of the 1977 anthology கலைஞர் கருணாநிதியின் சிறுகதைகள்**, published together on
the Fiction shelf. PR **#65**, exact reviewed head **`2ba1ee3aaa5078ddc60463e45cb00bca36ae4f8d`**,
squash **`4fd45a92663abbe70ff0c0a605168314cd36e44c`**, merged tree `0a502927…`, 83 files, merged
2026-09-02T03:28:20Z; post-merge Library CI run `33587162687` success. Source pin
`pugazg/kalaignar-short-stories` @ **`76135e1b5d504128c15be6bf59937716e5517d78`**, collection tree
`d45434d46b1e779a880fff3d774d0fcb5833e477`, all 37 work trees frozen and guarded individually.

**`கிழவன் கனவு` was excluded** — a separate, earlier source, already published, and the short-story
regression benchmark. **It is not the 38th anthology story.**

**Wave 2 ran the exact-head sequence correctly end to end**: PR opened → exact head reviewed →
APPROVED FOR MERGE for `2ba1ee3a…` → head unchanged → merge → production verification → control
close-out. That is the standing process.

**The Story-29 lesson:** the first candidate pin `a9b333f1…` carried a real source defect — Story 29's
English page markers were shifted from scan 200 onward with scan 204 empty. Implementation **stopped
and reported it** rather than repairing downstream or dropping the story; the archive was corrected,
and the whole 37-tree freeze was recomputed against `76135e1b…` (only Story 29's tree changed, to
`e6eea7e2…`). **A source release gate is not permission to work around a source defect.**

Validator: **2522 assertions, 42 groups, 0 failures**; **17/17 negative tests proven**, including a
reconstruction of the old shifted anchoring. `கிழவன் கனவு` regression byte-equivalent. Full detail is
in `HANDOVER.md`.

### Bulk Onboarding Wave 1 — Drama — ✅ COMPLETE and CLOSED

**கலைஞரின் நான்மணி மாலை four-play batch** — பரதாயணம் / Bharathayanam · அனார்கலி / Anarkali ·
சாக்ரடீஸ் / Socrates · சேரன் செங்குட்டுவன் / Cheran Senguttuvan. **The first bulk-onboarding activity
in the Digital Library.** PR **#64**, squash **`0dc92fa0fd832b5932b8df75606ef049c9f261ea`**, reviewed
head `74c7f6dc…`, 24 files. Source pin `pugazg/kalaignar-stage-plays` @
**`145e52e88dbd009286f749a7f0e3520386e63244`** — one composite scan
(`TVA_BOK_0065576_நான்மணி_மாலை.pdf`, 54 scans), four frozen work trees, re-confirmed unchanged at
close-out while source `main` advances for **மணிமகுடம் only**.

Drama **1 → 5**, catalogue **27 → 31**, **+22 public URLs** (Bharathayanam 3 · Anarkali 6 ·
Socrates 7 · Cheran 6).

The architecture: `structureKind` (`scene-sequence` / `continuous-play`) and reading-unit `kind`
(`scene` / `closing-tableau` / `continuous-body`) are **source-structure** distinctions. The public
shelf and type are unchanged, and **there is no `continuous-play` catalogue subtype**.
**Bharathayanam prints no scenes** — one continuous reading unit, route slug `continuous-play`
(navigation only), catalogue `unitCount` **absent**, and it is never "Scene 1" or a "one-scene play".
**Socrates** publishes **13** verified Tamil introductory units from scans **27–28** before its **5**
source scenes — the intro is not a scene, has **no route**, and `/plays/socrates/00-introduction` is
**404**. Anarkali and Cheran hold **4** scenes each. Silappathikaram was carried through the model
rename with **byte-equivalent reading text** and its closing tableau is still **not Scene 39**.

Two durable engineering lessons came out of it — the **`empty == empty` validation trap** and the
**buffered CI-output trap**. Both are recorded in `HANDOVER.md` and both are now standing rules.
Final batch validator: **385 assertions, 7 groups, 0 failed, BATCH RESULT: ALL PASS** *(the pre-repair
355 is historical only)*.

**மணிமகுடம் / Manimagudam was excluded** because its source processing was incomplete at the freeze.
Its upstream movement does **not** add it to Wave 1, repin Wave 1, make it *automatically* eligible
for Wave 3, or authorize publication. **It is not permanently ineligible** — it remains source-active
and may become a legitimate candidate once it passes its own release/readiness gate and the owner
authorizes a wave including it.

Full detail is in `HANDOVER.md`.

### ⚠️ Exact-head review is MANDATORY before any merge

Wave 1's PR #64 was **merged before its final repaired head received independent ChatGPT exact-head
approval**; ChatGPT then performed an independent read-only **post-merge** review of the exact
merged implementation and accepted it. **That is not the
workflow and is not a precedent.**

**The standing rule:** Claude opens the PR → ChatGPT reviews the **exact current head** → ChatGPT
gives **APPROVED FOR MERGE** → only then does Claude merge. **If the head changes after approval, STOP
and re-review.** Bulk onboarding does not relax this gate.

### ⚙️ Bulk onboarding is the STANDING DEFAULT workflow

**Owner decision, recorded 2026-09-01.** This supersedes the older one-work-per-benchmark default and
the "no bulk import, no mass ingestion" constraint repeated in the historical lists further down.

1. identify a coherent batch by source release / source repository / public shelf;
2. perform a readiness census over the whole candidate set;
3. exclude incomplete or blocked works explicitly;
4. freeze each included work against source commit/tree identity;
5. use one coherent deterministic importer where appropriate;
6. use one coherent source-linked batch validator;
7. the validator **MUST still report and fail per work**;
8. preserve per-work provenance, rights and structural distinctions;
9. publish the coherent batch in one implementation PR where architecture allows;
10. use one independent ChatGPT review gate for the batch;
11. **ChatGPT reviews the EXACT current PR head and gives APPROVED FOR MERGE; merge only after that
    approval; if the head changes, STOP and re-review**;
12. **after merge, production verification, then one batch control close-out** — in that order;
13. **do not flatten source differences merely because the work is batched.**

Approval precedes merge, merge precedes production verification, and production verification precedes
the control close-out. `HANDOVER.md` carries this identical sequence.

**A batch validator must report per work and fail the whole batch on any one work's failure.**
Source-tree drift guards are **per work**, and a source repository pinned at multiple historical
commits needs **separate CI checkout directories**.

**Bulk is the default, not permission to mix.** It never authorizes combining incompatible or
incomplete sources, and it is not a claim that every future work must be bulked regardless of source
state. A work that is not source-ready is excluded explicitly.

**One-work benchmark cycles are now the EXCEPTION**, appropriate only where a work introduces a
genuinely new source form, reader architecture, unresolved rights/attribution boundary, unusual
structure, source-fidelity blocker, or implementation risk that should not be coupled to a batch.

**Two standing validator rules from Wave 1:**

- **Never let `empty == empty` certify completeness.** An importer and a validator may share a
  contract but must not share a defect that makes both derive the same empty value. For a source
  section known to exist, assert **NON-EMPTY source extraction before equality**:
  **prove presence → then prove structure → then prove equality.**
- **Validator success is not enough if the evidence cannot be read.** Avoid a final `process.exit()`
  when stdout may be buffered (Node discards buffered stdout on a pipe, which is what CI provides);
  prefer `process.exitCode`; keep deliberate fail-closed early exits; ensure failure paths report
  assertions rather than crash; test through a pipe as well as direct stdout.

### Speech Benchmark #4 — ✅ COMPLETE and CLOSED

**கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** / *Kalaivanar N. S. Krishnan
Memorial-Day Speech* (`kalaivanar-nsk-memorial-day`) — the **first audio-sourced speech** in the
Digital Library. Both stages are merged and independently verified:

- **A1** (audio-source model, import, validator, reader, provenance page, routes, sitemap, CI):
  PR **#62**, squash **`492b26ddd5681f085726ac802681c3fcbc7162f0`**
- **A2** (Reading Room catalogue onboarding): PR **#63**, squash
  **`56ca0c978e34afddde52595f2ce825872bd6aeef`**

Source pin `pugazg/kalaignar-public-speeches` @ **`1ef73a709a343390befe55dcdfb029427f527bf4`**, path
`speeches/kalaivanar-nsk-memorial-day`, tree **`256cbe2adc8dbc9c245be57196652ed79da48eeb`** — a
historical release state, re-confirmed unchanged even though source `main` keeps advancing.

The architecture: **an audio recording is a SOURCE FORM for an existing `public-speech`, not a new
public subtype.** No `audio-speech` subtype, no printed-page provenance, no media binary, no player,
no runtime media fetch. The **exact speech date is NOT established and no year is inferred**. The 12
timestamps are **approximate navigation markers**, never source-authored sections or catalogue units.
Nationalisation is scoped to Kalaignar's underlying Tamil speech and **excludes the source recording,
the recording master, third-party recording production and the project-created English**. The
source-linked validator is **102/102**.

⚠️ **`speeches/kalaivanar-nsk-memorial-day-audio-06/` is a SEPARATE archive** — a different
recording, under active upstream development, and the reason public-speeches `main` keeps moving. It
is **not** a revision of this benchmark, **not** a new pin, and **not** selected for publication.
Never conflate the two.

Full detail, including the durable lessons and the rights boundary, is in `HANDOVER.md`.

*(The previous **2026-08-30** line — `766d6868…`, 25 works, 2948 pages, 2944 sitemap URLs, Cinema
Writing 3, Speeches 13 — is **superseded** and kept only as history, as is the 2026-08-26 line before
it: `15405c7f…`, 24 works, 2853 pages, 2849 sitemap URLs, Cinema Writing 2.)*

Shipped after the Phase-7 narrative below: **Thirukkural — கலைஞர் உரை** (with Daily Kural), the
**Assembly-speech anthology** (Speeches → 13), **Phase B — கிழவன் கனவு** (Fiction → 2),
**Phase C — பராசக்தி** (Cinema Writing → 2), **Phase D — திரும்பிப்பார்**
(Cinema Writing → 3, catalogue → 25), **கலைஞர் திரை இசைப் பாடல்கள் / Kalaignar Film Songs**
(Cinema Writing → 4, catalogue → 26) and **Speech Benchmark #4** (Speeches → 14, catalogue → 27).

**Film Songs historical status at this checkpoint:** implementation and publication were live, but
the separate formal control-document close-out had not yet been performed. **That statement is now
superseded by the CURRENT Film Songs close-out section above.**

### Phase C — பராசக்தி: COMPLETE and CLOSED

C1 audit · C2 import (#48) · C2.1 attribution correction (#50) · C3 reader + source routes (#49) ·
C4 catalogue (#51) · C5 sitemap (#52) · C6 production audit. Source pin
`pugazg/kalaignar-cinema-works` @ `789b003b6c0dfcf0bc38b906037f92953fd8146f` (work-specific, and it
supersedes `a593db50…`). 48 Parasakthi sitemap URLs: 1 landing, 1 source, 46 scenes.

Three facts not to collapse: the booklet **prints** its 46 scene headings (Manohara's 57 are
archive-created navigation); headings **23 and 34 are never printed** and get no page or URL; and the
**songs are not all Kalaignar's** — six poets credited collectively, three evidence tiers (11
`external-source` / 2 `anthology-attributed` / 1 `canonical-context-explicit`), exactly two
occurrences his and both on anthology evidence, which is **not** an original-film credit. No blanket
rights block: Parasakthi is composite. **Do NOT reopen Parasakthi.**

## Phase D1 — திரும்பிப்பார் / Tirumbippaar readiness audit — COMPLETE

Audited at `pugazg/kalaignar-cinema-works` @ `ca7431f3de8f8b2367a65206b8a9739d87788413`; re-confirmed
unchanged at `03c89cd2bb3019c5f75c2bfbca14077a8d1f643b` (intervening commits are Raja Rani only).

### The original premise was wrong: the crop is NON-BLOCKING

Tirumbippaar was carried as partial/blocked over "an unresolved crop". The crop is real but sits in
**front matter**, not reading text:

- location: PDF **2**, lower printer/imprint line
- visible partial: `சிட்டி பிரஸ், மதுரை ரோ…`
- canonical screenplay begins at PDF **9** — seven pages later
- canonical range: PDF **9–112** / printed pp. **1–104**, **104/104 verified**, 0 draft, 0 review
- `additional_main_text_crop_or_duplicate_findings: []`; zero crop/illegible markers in any of the
  five canonical transcription parts

It is a printer's imprint — a bibliographic detail, not a word of the screenplay. It stays **partial
and unreconstructed** (no `மதுரை ரோடு`, no address or printer-name continuation), and is classified
**documented / unresolved / front matter / non-blocking**.

### Measured census at D1 — ⚠️ PRE-CORRECTION, SUPERSEDED

These were the figures at the D1 audit pin, **before** the user's textual-correction pass. They are
recorded for history only. **Do not reuse them** — the current verified census is in the D1.1 section
below (1042 dialogue records, 1330 translation units).

104 canonical pages (0 missing, 0 duplicate, `printed = pdf − 8` with 0 violations) · 93 scenes ·
~~1,040 dialogue records · 1,321 English units~~ · 39 entities / 45 labels.

Songs: 8 occurrences — **3 verified, 5 unresolved, 0 attributed to Kalaignar**. The three verified are
`external-source` only (பாரதிதாசன் ×1, கண்ணதாசன் ×2). No anthology tier, no full lyric body printed,
no Tamil song derivative invented from absent text. Work authorship is a direct printed cover credit:
`கதை - வசனம் — கலைஞர் மு. கருணாநிதி`. Rights: `உரிமையுடையது.` and `விலை ரூ. 0-10-0` are recorded as
printed 1953 statements, not a present-day determination — no blanket rights block.

---

## Phase D1.1 — canonical/derivative reconciliation — CONTENT PASS

The earlier D1.1 framing — "one remaining PDF-59 punctuation blocker" — is **superseded and no longer
the state**. That question was overtaken by a full textual-correction pass the user ran against the
controlling scan, which corrected the canonical Tamil across the work.

### Source authority

The controlling scan decides every reading. Readings are **not** judged by grammar, gender agreement,
expected syntax, character identity or modern usage. As-printed forms that look unusual are preserved
— `அறிமுகமானான்`, `விளையாடுகிறான்`, `மாடிக்குப் போகிறாள்`, `பெருமூச்ச`, `பரந்தாமான்`.

**`ஊஹும்` was verified directly by the user against the controlling PDF.** That reading is settled,
is preserved in every reading layer, and is not to be reopened or reverted to `ஊஹூம்`.

### What source PR #2 does

The correction pass updated canonical but did not consistently re-derive the dependent layers, so
`pugazg/kalaignar-cinema-works` **PR #2** reconciles them:

- 16 scene lines brought into line with corrected canonical (scenes 6, 7, 8, 16, 28, 41);
- one **canonical omission restored from the scan** — `கருடன் : இல்லை பரந்தாமன்.` is the first line of
  printed page 6 / PDF 14; canonical had dropped it and `scene-05` had it in the PDF 13 block. It is
  now in canonical once at the head of the PDF 14 block, in `scene-05` after the `pdf=14` anchor, not
  duplicated, and carried by dialogue record `tirumbippaar-s005-d007`;
- two dialogue records (`tirumbippaar-s006-d012`, `tirumbippaar-s028-d011`) whose live `text` still
  held the superseded `ஊஹூம்` corrected to `ஊஹும்`. No reading layer now contains `ஊஹூம்`.

### Validation — two distinct gates, reported separately

Earlier wording conflated these and wrongly called a normalized result "exact reconstruction".

**A. Strict textual equality** (exact trimmed-line identity; punctuation, ellipses, spacing, quote
glyphs all significant): **1173 of 1342 exact, 169 mismatches** (base was 1156 / 186).

**B. Normalized word-level alignment** (Tamil letters only): **1342 of 1342 aligned, 0 unaligned**
(base was 1325 / 17). This is *alignment*, not exact reconstruction.

Every Tamil-letter reading now matches canonical. The 169 strict mismatches are presentation-layer
only — 140 whitespace, 11 quote/dash glyph, 18 other punctuation (bracket type, ellipsis count). The
previously reported "29" is the whitespace-folded subset (11 + 18) and **still exists**; it is
deliberately untouched, since changing punctuation is outside a reading reconciliation.

### Census — recomputed, not carried over

The old **1040 dialogue / 1321 English unit** baselines are **obsolete and must not be reused**.

| | |
|---|---|
| canonical pages | **104** (PDF 9–112) — 83 `verified` + 21 `verified-reconciled`, 0 draft, 0 review |
| scenes | **93** |
| dialogue records | **1042** |
| translation units | **1330**, all verified |
| dialogue links | **1042 exactly once, 0 duplicates, 0 orphans, 0 unlinked** |
| character entities / labels | 39 / 45 |
| song occurrences | 8 — 3 verified, 5 unresolved, **0 attributed to Kalaignar** |

The **PDF-2 printer-imprint crop remains partial, documented and NON-BLOCKING** — it is front matter,
seven pages before canonical text begins, and is never reconstructed.

Ten `புண்ணகோடி` occurrences remain, all correction-history quotations or audit records and none in
live reading text; they are preserved as evidence. The entity ID `tirumbippaar-char-punnakodi` is
**not renamed** — an internal identifier referenced only within `characters/`, whose display label
already carries the corrected `புண்யகோடி`.

### Status

**D1.1 CONTENT RECONCILIATION: PASS — and source PR #2 is now MERGED**, squash
`d4b394a7b4582935792df4cf2840fbd466dd41c5` (the source `main` at that time; **now superseded by the
D1.2 merge `505b1ea7`**); branch deleted. Post-merge verification on that main: `ஊஹும்` 5/5/5 in transcription, scenes and
dialogues with **zero `ஊஹூம்` anywhere in the work**; the restored `கருடன் : இல்லை பரந்தாமன்.` is
canonical exactly once at the head of the PDF 14 block, in `scene-05` after the `pdf=14` anchor, not
duplicated, and carried by `tirumbippaar-s005-d007`; census 104 pages / 93 scenes / 1042 dialogue
records / 1330 translation units / 1042 links exactly once, 0 duplicates, 0 orphans, 0 unlinked.

## Phase D1.2 — strict derivative-fidelity audit — CONTENT PASS on PR #3 head

**Source PR #2 is merged** at `d4b394a7b4582935792df4cf2840fbd466dd41c5` — the source `main` at that
time, **now superseded by the D1.2 merge `505b1ea7`**. D1.1 is complete.

**D1.2 lives on source PR #3** (`fix/tirumbippaar-strict-derivative-fidelity`), validated on the clean
committed head **`49e1b2c4387190e4fe0aea822f8e68b338dccb9d`**.

The method finding stands: canonical could not serve as the punctuation authority, because it carried
OCR artifacts the scene layer did not, while elsewhere the scene was the faulty layer. Only the
controlling scan decided.

### Closure round

**Scene 45.** The user verified the PDF directly: the source prints `பாண்டியன் : தொழிலாளர்கள்` with no
full stop after the speaker name. Canonical and scene both carried `பாண்டியன். :`; both corrected. The
dialogue record `tirumbippaar-s045-d013` already held `பாண்டியன்` and is unchanged — it was correct and
the defect was above it. **No `பாண்டியன்.` variant created; the inventory stays at 45 exact labels.**

**Heading markers fully closed.** 18 location-opening markers (previous round) and now **22 of 22
scene-number closing markers**, each inspected individually on the scan: 19 that printed `)` and 3 that
had no glyph at all, all corrected to `]`. **0 unresolved.** Source anomalies preserved: scene 5
`காட்சி 5[`, scene 36 with no closing glyph, scene 43 `காட்சி 43].`.

### Gates on `49e1b2c4`

| gate | result |
|---|---|
| canonical↔scene source-visible | **0 mismatches** (1348/1348 exact text and page) |
| page attribution | **0** |
| scene↔dialogue text | **0 unexplained** (2 documented scene-72 records) |
| scene↔dialogue provenance | **0** |
| dialogue↔translation provenance | **0** |
| dialogue links | 1042 exactly once, 0 duplicate, 0 orphan, 0 unlinked |
| character source labels | **45** |
| translation/reader preflight | PASS |
| heading markers | **0 unresolved** |

Census: **104** canonical pages (0 draft, 0 review) · **93** scenes · **1042** dialogue records ·
**1330** translation units. `ஊஹும்` is user-verified and preserved at 5/5/5 with **0 `ஊஹூம்` in live
reading layers**. The **PDF-2 printer-imprint crop remains partial, documented and NON-BLOCKING**.

Reader and EPUB artifacts are **not** committed — CI regenerates them on push to `main`.

### Source PR #3 — MERGED · CI-fix PR #4 — MERGED · publication package COMPLETE

| stage | SHA |
|---|---|
| D1.2 source fidelity, PR #3 reviewed head | `49e1b2c4387190e4fe0aea822f8e68b338dccb9d` |
| PR #3 squash merge | `505b1ea7382bacb39c82d9f314668a67a38219bd` |
| CI-fix PR #4 reviewed head | `9bd4b1f370c7f6602648e5e3e1e7cfced4edd34e` |
| PR #4 squash merge | `b4ab599d8726f45780a72e5d4531d52583b7f220` |
| **CI publication commit — authoritative source pin** | **`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`** |

Both branches deleted; 0 open source PRs. **The authoritative Tirumbippaar source pin is
`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`.**

### Official publication CI — PASSED

`Tirumbippaar English reader QA`, run **`33247433975`** (#288) on `b4ab599d`, event `push`:
**completed / success**, all 11 steps of `qa-and-build` succeeded with **nothing skipped**. The
previously failing migration step now reports *"Reader gates already index-authoritative; nothing to
migrate."* and continues.

| step | result |
|---|---|
| reader preflight | **PASS** |
| whole-work QA | **PASS** — 93 scenes · 1330 units · 1042 dialogue links · 12 cross-page |
| deterministic EPUB 3 package | **PASS** — 93 scenes · 1330 units |
| metadata synchronization | **PASS** |
| generated-package commit | **PASS** — pushed `6a8c59c4`, 8 files |

**Official EPUB:** `works/tirumbippaar/editions/en/tirumbippaar-en.epub`, **370,204 bytes**, SHA-256
**`955ce8adffe318ccbb5f77cb65afebb6951b7c7ac3091343adf2fd3dcb996ae0`** — recomputed from final main and
identical to the CI-reported value, confirming the build is genuinely deterministic. `QA_REPORT.md`
**PASS** (1,330 verified / 0 review / 0 draft); `EPUB_QA_REPORT.md` **PASS**; `manifest.json` and
`package-manifest.json` both `complete-verified`, pinning `source_scan_sha256`
`973b9c3f7b84d6a1902a4a472af8799c783bf1ec2d6cd015796fc1df1ce59682` — the controlling scan.

### Final validation on `6a8c59c4`

| gate | result |
|---|---|
| canonical↔scene | **1348/1348 exact text; 1348/1348 exact text + page; 0 mismatches** |
| page attribution | **0** |
| scene↔dialogue text | **0 unexplained** (2 documented scene-72 structural records) |
| scene↔dialogue provenance | **0** |
| dialogue↔translation provenance | **0** |
| dialogue links | **1042 exactly once**, 0 duplicate, 0 orphan, 0 unlinked |
| translation QA / reader preflight | **PASS** |
| heading surfaces | 18 opening + 22 closing · **0 unresolved** |

Census: **104** canonical pages (83 `verified` + 21 `verified-reconciled`, **0 draft, 0 review**,
`printed = pdf − 8` with 0 violations) · **93** scenes · **1042** dialogue records · **1330**
translation units · **39** character entities / **45** exact source labels · **8** song occurrences
(3 verified, 5 unresolved, **0 attributed to Kalaignar**).

`ஊஹும்` is user-confirmed and preserved at **5/5/5** with **0 `ஊஹூம்` in live reading layers**.
Scene 45 reads **`பாண்டியன் : தொழிலாளர்கள்`** in canonical and scene; `tirumbippaar-s045-d013` holds
`speaker_label` `பாண்டியன்`, text `தொழிலாளர்கள்`, provenance PDF 59 / printed 51, and **no
`பாண்டியன்.` source-label variant exists**. Heading anomalies retained exactly as printed:
**`காட்சி 5[`**, **`காட்சி 36`** (no closing glyph), **`காட்சி 43].`**. The **PDF-2 printer-imprint
crop remains partial, front matter, documented, NON-BLOCKING and never reconstructed**.

### Status

**D1.1 COMPLETE · D1.2 COMPLETE · PUBLICATION PACKAGE COMPLETE.**

**Tirumbippaar source main was released for D2** at
`6a8c59c445890e568dfe65cc36c2900dd2a8a0b3`, now the published provenance authority.

*(Historical note, superseded: the earlier publication-CI failure on `505b1ea7` — run `33246879335` —
was a non-idempotent workflow migration step, not a source-content defect. It is fixed and resolved.)*

## Phase D2 — திரும்பிப்பார் / Tirumbippaar integration — ✅ COMPLETE and CLOSED

**TIRUMBIPPAAR PHASE D COMPLETE** — D1.1 · D1.2 · SOURCE PUBLICATION PACKAGE · D2.1 · D2.2 · D2.3 ·
D2.4 · D2.5 all COMPLETE. *(The not-yet-started note previously here is superseded and removed.)*

Source pin `6a8c59c445890e568dfe65cc36c2900dd2a8a0b3` · implementation `main` after D2.4
`766d68680cecca549d4d752e32561834f7dde0f5` · post-merge Library CI `33292800096` success · GitHub
Production deployment `6163236518` success for that SHA.

PR chain: **#53** D2.1 data · **#54** D2.2 reader/source routes · **#55** D2.3 catalogue ·
**#56** D2.4 sitemap.

Measured at the D2.5 boundary on **2026-08-30** — ⚠️ **site-wide totals since superseded**, see the
CURRENT STATE section above: 25 catalogue works · Cinema Writing 3
(`manohara → parasakthi → tirumbippaar`) · 2944 sitemap URLs with **95** Tirumbippaar (1 landing +
93 registry scenes + 1 source) · 2948 build pages. All 95 production URLs 200; sitemap scene set
equals the registry exactly; off-registry slugs 404. *(The **95 Tirumbippaar URLs** and the route
family are the durable Tirumbippaar facts; the catalogue/sitemap/page totals around them have moved
on.)*

Census at the pin: 104 pages · 93 scenes · 1042 dialogue records · 1330 English units · 39 entities ·
45 labels · 8 song/performance occurrences (3 verified to others, 5 unresolved, **0 Kalaignar**).

**Rights deliberately unset** for the whole publication — composite work, same posture as Parasakthi.
The 1953 `உரிமையுடையது.` notice is printed source evidence only. Credit is role-scoped to the printed
`கதை - வசனம்`.

**Settled, do not reopen:** `ஊஹும்` (5 live) not `ஊஹூம்` (0) · scene 45 `பாண்டியன் : தொழிலாளர்கள்` ·
headings `காட்சி 5[`, `காட்சி 36`, `காட்சி 43].`. Source-visible irregularity is **not** inferred to be
error from expected Tamil or punctuation convention.

**Do NOT reopen Tirumbippaar** absent an explicit new issue or a new source release.

---

## Where the project actually stands (completed — do NOT redo)

- **Phase 1 — Library Foundation:** COMPLETE, merged, production-verified.
- **Phase 2 — Cinema / Manohara:** COMPLETE, merged, production-verified.
- **Phase 3 — Speeches: ACTIVE, NOT complete.** Four benchmarks are done. *(Historical context: I asked at the time for the next work to come from a category **other than speeches**, which produced Phase 4 — Poetry. That pause is **historical and superseded**; Benchmark #4 has since run and closed. No FURTHER speech work is authorized.)*
  - **Benchmark #1 — உதயக் கதிர் / Udhaya Kathir** (assembly speech): COMPLETE, merged, production-verified (PR #18).
  - **Benchmark #2 — பூந்தோட்டம் / Poonthottam** (public speech): COMPLETE, merged, production-verified (PR #20), plus the PR #21 presentation/provenance hotfix.
  - **Benchmark #3 — அறப்போர் / Arappor** (public speech): COMPLETE, merged, production-verified (PR #23).
  - **Benchmark #4 — கலைவாணர் என். எஸ். கிருஷ்ணன் நினைவு நாள் விழாவில் கலைஞர் உரை** (public speech, **audio source**): **COMPLETE, merged, production-verified** — A1 PR #62 squash `492b26dd…`, A2 PR #63 squash `56ca0c97…`. Source pin `pugazg/kalaignar-public-speeches @ 1ef73a709a343390befe55dcdfb029427f527bf4`, tree `256cbe2a…`. First audio-sourced speech; `public-speech` retained, audio carried as source form. *(This line replaces the earlier "Speech Benchmark #4: NOT STARTED and NOT SELECTED", which is historical.)*
  - **Speech Benchmark #5: NOT STARTED / NOT SELECTED / NOT AUTHORIZED.**
- **Phase 4 — Poetry: ACTIVE.**
  - **Benchmark #1 — இதயத்தைத் தந்திடு அண்ணா / Lend Me Your Heart, Anna:** COMPLETE, merged, production-verified (PR #25, reviewed head `3653023d…`, squash `c2d1c46d…`, 2026-08-20T01:58:07Z, merge-SHA deployment `92kdGyRiKucdUPSywP2XqnZMx1g9`).
  - **Poetry Benchmark #2: NOT STARTED / NOT SELECTED / NOT APPROVED FOR IMPLEMENTATION.** A second work now EXISTS — at live `pugazg/kalaignar-poems` `2230a8d`, `poems/` holds `idhayathai-thanthidu-anna` (released) **and** `anaiya-vilakku-anna`. `anaiya-vilakku-anna` (அணையா விளக்கு அண்ணா) is **NOT READY**: of 19 source pages only **1** page record exists, Tamil assembly is **pending**, English translation is **pending**, and the work records **no SHA-256 and no byte size**. A candidate source exists, but it is **not approved for implementation**. Not cancelled; Phase 4 is not complete either. Verify live.
- **Phase 5 — Essays & Articles: ACTIVE.**
  - **Benchmark #1 — சக்கரவர்த்தியின் திருமகன் / Chakravarthi's Son:** COMPLETE, merged, production-verified (PR #27, reviewed head `929bb545…`, squash `bcb11396…`, 2026-08-20T10:15:15Z, merge-SHA deployment `AwU8uyXYHxthgez8ZGQWP1rTS3PF`). Source pin `pugazg/kalaignar-essays @ bff35320b668cb5beeaafc5faa58260c4f4473f8`. ONE publication holding 14 source-numbered articles.
  - **Phase-5 Benchmark #2: NOT STARTED / NOT SELECTED.**
- **Phase 6 — Fiction: benchmark 1 COMPLETE.**
  - **Benchmark #1 — பலிபீடம் நோக்கி / Towards the Sacrificial Altar** (novel): COMPLETE, merged, production-verified (PR #28, squash `992fd8d6…`). Source pin `pugazg/kalaignar-novels @ 9e80c567d4a2165178c5374a02210240140685bf`. ONE novel in THREE assembled reading sections. `ராயசம் வெங்கண்ணா` is section 2 of that novel, never a separate work.
  - **Fiction Benchmark #2: NOT STARTED / NOT SELECTED.** Fiction shipping first does not privilege Fiction next.
- **Phase 7 — Drama / Stage Plays: ACTIVE.**
  - **Benchmark #1 — சிலப்பதிகாரம் நாடகக் காப்பியம்** (stage play): **COMPLETE, merged, production-verified** (PR #29, squash `9aade1d4…`, verified 2026-08-21). Source pin `pugazg/kalaignar-stage-plays @ a66e62bbecaf63825b3db09a1d421401e1ab2e8e`. 38 numbered scenes plus a separate unnumbered closing tableau; that tableau is never Scene 39.
  - **Bulk Onboarding Wave 1 — Drama:** ✅ **COMPLETE, merged, production-verified and CLOSED** — பரதாயணம், அனார்கலி, சாக்ரடீஸ் and சேரன் செங்குட்டுவன், PR #64, squash `0dc92fa0…`, source pin `pugazg/kalaignar-stage-plays @ 145e52e88dbd009286f749a7f0e3520386e63244`. Drama 1 → **5**. *(This line replaces the earlier "Drama Benchmark #2: NOT STARTED / NOT SELECTED — `Anarkali`, `Cheran Senguttuvan` and `Socrates` have no controlling Tamil source", which is **historical**: controlling Tamil sources were released and those works are published. The 2009 published English witness remains **secondary comparison evidence only** and must never be reverse-translated into Tamil — that constraint is unchanged.)*
  - **Any further Drama work / a future Drama batch: NOT STARTED / NOT SELECTED / NOT AUTHORIZED.** **மணிமகுடம் / Manimagudam is NOT published** and is **not** automatically eligible.

**Last production application-code checkpoint at this handover:**

`9aade1d441bb314b5ab62f97b87b373d33db08c5`

That is the Phase-7 Drama Benchmark #1 / PR #29 squash merge, and it identifies the last **production application-code** state. It supersedes `992fd8d6cd7bfd89a2689574d0e2ef2728774a1a` (Phase 6), `bcb11396b2215bc2cc1e81873c0ce278ef98598a` (Phase 5), `c2d1c46d1c2d4e1f11722360848226208867789f` (Phase 4) and `ecf73cc8146cd9a9578c4aeaf73518b122ce569c` (Phase 3), which are now **historical** checkpoints only. Repository `main` may contain later **documentation-only** commits that do not change deployed application behaviour, and such a docs-only SHA is **never** a newer application-code checkpoint. If live `main` has moved past that SHA, **live state wins** — inspect it and reconcile before advising anything.

⚠️ **SUPERSEDED COUNTS (2026-09-01) — the per-shelf structural facts below still stand, the totals
do not.** The current census is **27 works across 9 non-empty shelves** with **Speeches 14** and
**Cinema Writing 4** (see CURRENT STATE at the top). The paragraph below is the Phase-7-era snapshot,
kept for the per-work structure it records.

`/read` currently publishes **11 works across 9 non-empty shelves** (Life Writing, Letters, **Poetry**, Cinema Writing, Speeches, **Essays & Articles**, Literary Commentary, **Fiction**, **Drama**). **நாடகங்கள் / Drama** holds exactly **1** work (`சிலப்பதிகாரம் நாடகக் காப்பியம்`, 38 scenes plus a separate closing tableau). **புனைவு / Fiction** holds exactly **1** work (`பலிபீடம் நோக்கி`, three sections); **கட்டுரைகள் / Essays & Articles** holds exactly **1** publication (14 articles inside it); **Poetry / கவிதைகள்** holds exactly **1** work; the **single** Speeches / உரைகள் shelf holds exactly **3** — Udhaya Kathir, Poonthottam and Arappor. Verify this live rather than trusting the numbers.

**Do NOT restart:** Phase 1, Phase 2 / Manohara, Speech Benchmarks #1–#3, **Speech Benchmark #4
(கலைவாணர் memorial-day audio speech — CLOSED)**, the PR #21 hotfix, Poetry Benchmark #1 (Idhayathai Thanthidu Anna), Phase-5 Essays Benchmark #1 (Sakkaravarththiyin Thirumagan), Phase-6 Fiction Benchmark #1 (Balipeedam Nokki), Phase-7 Drama Benchmark #1 (Silappathikaram Nataka Kappiyam), or mobile.

## Current poetry source pin

- **இதயத்தைத் தந்திடு அண்ணா:** `pugazg/kalaignar-poems` @ `42c156d7242fa799ea80adbb0c5f2b9eba078fe9`

At that source state, `poems/` contains **exactly one** work directory — `idhayathai-thanthidu-anna` — and the repository README says a *next* poem must begin again from its own startup/source-inspection workflow. **Do not pretend another released Poetry candidate is currently available.** Re-check live source state before advising.

## Current essays source pin

- **சக்கரவர்த்தியின் திருமகன்:** `pugazg/kalaignar-essays` @ `bff35320b668cb5beeaafc5faa58260c4f4473f8`

## Current speech source pins

- **Udhaya Kathir:** `pugazg/kalaignar-assembly-speeches` @ `b1b82402642d8f2cf36927d4752c8e7d28142fdd`
- **Poonthottam:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`
- **Arappor:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4`
- **Kalaivanar N. S. Krishnan Memorial-Day Speech:** `pugazg/kalaignar-public-speeches` @ `1ef73a709a343390befe55dcdfb029427f527bf4` (path `speeches/kalaivanar-nsk-memorial-day`, tree `256cbe2adc8dbc9c245be57196652ed79da48eeb`). Source `main` has advanced well past this pin for the **separate** `kalaivanar-nsk-memorial-day-audio-06` archive; the released work stays pinned here.

## Source repositories

The Digital Library progressively integrates verified/released works from:

- `pugazg/kalaignar-novels`
- `pugazg/kalaignar-short-stories`
- `pugazg/kalaignar-poems`
- `pugazg/kalaignar-assembly-speeches`
- `pugazg/kalaignar-essays`
- `pugazg/kalaignar-cinema-works`
- `pugazg/kalaignar-literary-commentary`
- `pugazg/kalaignar-stage-plays`
- `pugazg/kalaignar-public-speeches`

These repositories remain **authoritative** for their own transcription, verification, translation and provenance. The website consumes/vendors reader derivatives; it must **never** silently rewrite archival text, and a Digital Library integration must **never** edit a source archive. If a source defect is found, it is raised and fixed **upstream** in the source repository, then re-pinned downstream.

## Decided library shelves

1. Life Writing
2. Letters
3. Fiction — novels + short stories
4. Poetry
5. Drama
6. Cinema Writing
7. Speeches — public + Legislative Assembly (**one** shelf; `assembly-speech` / `public-speech` are **subtypes**)
8. Essays & Articles
9. Literary Commentary

Repository boundaries are not the same as public-library shelves. Empty shelves stay hidden.

## Manohara — completed, with one permanent caution

Phase 2 imported Manohara correctly from the authoritative `pugazg/kalaignar-cinema-works`. The accidental old website data under `public/data/cinema/manohara/parts/` was **removed** during that phase.

**Never resurrect those `parts/` files as source authority** — they were never an approved import, an integration boundary, or an authority for text, translation, counts, provenance or metadata. `pugazg/kalaignar-cinema-works` is the only source of truth for Manohara.

## Your role

**You are the reviewer and prompt provider. Claude Code performs every repository write.** You do not
commit and you do not merge — you review, you recommend, and you supply prompts. **Live GitHub state
wins over any SHA, count or status paragraph copied into a handover, including this file.** **Owner
authorization is required before a new benchmark starts**; being eligible for consideration is not
authorization.

Your job is to:

1. inspect live GitHub state;
2. review Claude execution reports independently and sceptically;
3. detect scope drift, duplicate integration, stale state, or source/provenance mistakes;
4. recommend merge / correction / stop;
5. provide complete ready-to-paste Claude prompts when I ask for the next activity;
6. keep the Digital Library handover updated as major milestones complete.

## Immediate next activity — ⚠️ SUPERSEDED BY CURRENT SECTION ABOVE

This lower section is historical operating context. The **current** next activity is already authorized:
**Wave 4 readiness census / selection — AUTHORIZED, NOT STARTED; implementation NOT YET AUTHORIZED.**
Where any wording below says Film Songs close-out is pending, or Wave 4 is unauthorized, the CURRENT
section above governs.

**Bulk Onboarding Wave 1 — Drama is COMPLETE and CLOSED** (PR #64 / `0dc92fa0…`; control close-out
recorded in `HANDOVER.md`), and **Speech Benchmark #4 is CLOSED** (A1 #62 / `492b26dd…`,
A2 #63 / `56ca0c97…`).

**Do NOT** select `kalaivanar-nsk-memorial-day-audio-06` as the next candidate. It is a **separate
recording and a separate source work**, still under upstream development — not a revision of the
closed Benchmark #4, not a new pin for it, and not established as ready for publication.

**Do not continue Tirumbippaar D2 work.** It is complete and production-verified. **Do not reopen
Speech Benchmark #4.**

**Known roadmap candidates after Tirumbippaar — historical list only; no item is preselected by this list:**

- printed public-speech booklets;
- audio / public speeches — *(the first audio speech has since shipped as Benchmark #4; further audio
  speeches remain candidates, none selected)*;
- cinema work / song-related follow-ups only if independently source-ready;
- **Mandhiri Kumari — historical snapshot said NOT ready; recheck live during the authorized census**;
- **Anaiyaa Vilakku Anna — historical snapshot said NOT ready; recheck live during the authorized census**;
- stage-play candidates only through their own readiness gates.

**Standing paused / held work — do not fold any of these into the next benchmark automatically:**

- **Validator migration remains PAUSED** after the Manohara migration, unless the owner explicitly
  resumes it.
- **Mobile remains ON HOLD.**
- **Manohara source-drift audit remains separate future work.**
- `ManoharaReader` "Kalaignar's original Tamil text" wording and `StorySource` universal
  scan-storage wording are **separate pre-existing questions**, to be reviewed only if/when those
  components are next touched.
- **Tirumbippaar internal catalogue comment** in `data/library.ts` says song/performance material
  "is not his" while five occurrences are unresolved — strictly, unresolved authorship does not
  establish that those five are someone else's. Safer future wording: *"song/performance material with
  mixed or unresolved authorship — three attributed to others, five unresolved, none attributed to
  Kalaignar."* Reviewed as **NON-BLOCKING**; fold it into a future PR that legitimately edits that
  comment, and do **not** open an implementation change for it on its own.
- A scoped **`WorkAttribution`** rights model for composite works remains a separate future issue.
- **Speech-model comment debt (from Speech Benchmark #4):** the top-level comment in
  `data/speeches.ts` and a nearby `SpeechReader` internal comment still describe the block stream in
  print-only terms ("printed section headings", "source-page boundaries"). Non-runtime, non-public
  explanatory debt. Fold into a future PR that legitimately edits those comments; do **not** open a
  change for it on its own.
- **Film Songs follow-ups:** the nullable section-label type mismatch, and the E3 catalogue-comment
  wording precision — both separate future work. **The formal Film Songs control close-out itself is
  closed by the CURRENT checkpoint once this control PR is merged.**
- **Stale `/read` metadata description** — the page-level description still names only the memoir,
  the letters and the commentary. Separate future work.

- **Poetry Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-5 Essays Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Fiction Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-7 Drama Benchmark #1:** COMPLETE / MERGED / PRODUCTION-VERIFIED.
- **Phase-6 Benchmark #2 (a second Fiction work):** NOT STARTED / NOT SELECTED.
- **Poetry Benchmark #2:** historical snapshot NOT READY; **recheck live in the authorized Wave 4 census** rather than carrying the old readiness state forward.
- **Phase-5 Benchmark #2 (a second Essays work):** NOT STARTED / NOT SELECTED.
- **Speech Benchmark #4:** ✅ **COMPLETE / MERGED / PRODUCTION-VERIFIED** — the first audio-sourced
  speech (A1 #62 `492b26dd…`, A2 #63 `56ca0c97…`). Closed; do not reopen.
- **Speech Benchmark #5:** NOT STARTED / NOT SELECTED / NOT AUTHORIZED. A fifth speech is eligible to
  be compared, but **`kalaivanar-nsk-memorial-day-audio-06` is not selected** and is not established
  as ready.

### Default for "Proceed with next activity"

**CURRENT OVERRIDE:** because the owner explicitly authorized Wave 4 readiness census / selection, a
plain continuation now means continue that **read-only census/selection** until it is complete. It does
**not** authorize Wave 4 implementation.

For the census, inspect live control, implementation and relevant source state and compare coherent
batch candidates category-neutrally. At minimum inspect live readiness across repositories such as
`pugazg/kalaignar-poems`, `pugazg/kalaignar-essays`, `pugazg/kalaignar-novels`,
`pugazg/kalaignar-short-stories`, `pugazg/kalaignar-stage-plays`, `pugazg/kalaignar-cinema-works`,
`pugazg/kalaignar-literary-commentary` and, where appropriate, speech repositories — but never assume
every repository contains an eligible work.

Judge candidates on released/verified source readiness, released English where bilingual publication
is intended, provenance completeness, architectural coherence, public shelf fit and source authority.
Identify a coherent Wave 4 batch, list exclusions/blockers explicitly, and report the selected batch.
**Stop before implementation.** Do not open an implementation PR until the owner separately authorizes
that selected Wave 4 implementation.

Whichever future work or batch is later authorized for implementation must use deterministic,
commit-pinned imports; preserve form-specific source structure; make no source-archive edits; vendor no
PDFs; use no runtime GitHub; make no mobile changes; and pass the exact-head review gate before merge.

## Source-faithful constraints (non-negotiable)

- Tamil is the authoritative layer; English is verified project/source-provided translation with its own provenance.
- **Never fabricate** a speech date, event, occasion, venue or audience the source does not establish.
- **Never infer** printed page or paragraph layout — not from punctuation, not from speaker count, not from a locally available PDF.
- **Unresolved source facts stay unresolved** and render neutrally; resolving them requires an upstream source-archive review that explicitly records the missing printed fact.
- Preserve difficult source-supported wording rather than normalizing it; keep translator notes.
- Distinguish archival/derived numbering from printed source numbering.
- Assembly speeches must preserve parliamentary exchanges/interjections where present.
- Deterministic pinned imports; generated reader data is regenerated by the importer, never hand-patched.

## Important source-readiness cautions

- `பலிபீடம் நோக்கி`: **INTEGRATED** as Phase-6 Benchmark #1. `ராயசம் வெங்கண்ணா` is embedded in the same novel, not a separate work. The spelling `ராயசம் வெங்கண்ணா` / Rayasam Venganna was taken from the controlling scanned source edition and corrected in the archive at `9e80c56`; the earlier `ராயசம் வெங்கண்ணு` / Rayasam Vengannu is **superseded**, not an alternative reading.
- Stage-play one-act English material for Anarkali / Cheran Senguttuvan / Socrates is a **secondary published-English witness** and must never be mislabelled as canonical Tamil work or reverse-translated. ⚠️ **Updated 2026-09-01:** controlling Tamil sources **have since been supplied** and all three are published by Bulk Onboarding Wave 1 — the "not yet supplied" half of this caution is historical. **The secondary-witness rule itself still stands**, and for **Bharathayanam no 2009 witness exists at all** — that is *not applicable*, not pending.
- Thirukkural — Kalaignar Commentary is not yet at a complete finished-work boundary in the source repository; do not publish it as complete without an explicit editorial/owner decision.
- Cinema scene IDs may be archival/derived rather than printed source numbering; preserve that distinction.
- Public-speech sources sometimes do not establish a single speech date/event; do not invent one.

_(These are planning snapshots. Verify against live source state before relying on any of them.)_

## Rights / provenance rule

`verified`, `archival-ready`, `release-ready` and `release-complete` are editorial/source-fidelity statuses — **not** automatic copyright or public-domain determinations.

Do not claim the Digital Library is official, authorized, public-domain or complete unless that has been separately established.

## Prompt style for Claude

Every Claude prompt should contain:

- mandatory startup reading;
- live repository inspection before edits;
- authoritative source repositories and exact pins for the activity;
- staged workflow;
- exact allowed changes;
- source/provenance constraints;
- route/backward-compatibility requirements;
- accessibility/responsive requirements;
- validator/build/Vercel checks on the exact head;
- branch/commit/PR discipline;
- exact scope exclusions;
- stop condition;
- structured final report;
- explicit instruction not to begin the next benchmark automatically.

## Start now

Read the current Digital Library handover completely, inspect live control and implementation state,
and verify the CURRENT checkpoint above. Then continue only the authorized bounded activity.

**Current bounded next activity: Wave 4 readiness census / selection — AUTHORIZED, NOT STARTED.**
Perform the live source-readiness census and coherent-batch selection when this Film Songs control
close-out is durably merged. **Do not implement the selected Wave 4 batch.** Validator migration stays
**PAUSED** and mobile stays **ON HOLD** unless explicitly resumed.

---
