## ⚠️ CURRENT STATE — 2026-09-02, post-Wave-3 (supersedes the phase list below)

**The "Where the project actually stands" list below stops at Phase 7 and is HISTORICAL.** Its work
and shelf counts are stale. It is kept for completed-phase detail and has not been retro-edited.
**Live GitHub wins over anything in it.**

Measured at the Wave-3 production boundary: implementation `main`
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

**This control-only PR proposes the durable Wave-3 close-out. The control record becomes closed only
when this PR is independently exact-head reviewed and merged.**

### NEXT ACTIVITY AFTER THIS CONTROL CLOSE-OUT

**Wave 4 is NOT SELECTED, NOT AUTHORIZED, and no Wave-4 readiness census has started.** Do not select,
rank, census or implement a next wave merely because Wave 3 is closing. Wait for explicit owner
authorization for the next activity.

Standing exclusions/status remain unchanged: Film Songs formal control close-out is separate and still
pending; validator migration is **PAUSED**; native mobile is **ON HOLD**; Manimagudam is never
auto-selected and requires its own readiness gate + owner authorization; `kalaivanar-nsk-memorial-day-audio-06`
is a separate source-active archive and is never auto-selected.

