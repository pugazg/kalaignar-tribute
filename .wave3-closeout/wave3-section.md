## Bulk Onboarding Wave 3 — Essays & Articles / three-publication batch — ✅ COMPLETE and CLOSED

**The third bulk-onboarding activity.** Three release-complete publications from `pugazg/kalaignar-essays`
were published together on the existing Essays & Articles shelf:

1. **கயிற்றில் தொங்கிய கணபதி** / *Ganapathi Who Hung from the Rope* — 1 article, 17 scans;
2. **உணர்ச்சிமாலை** / *Garland of Emotion* — 10 articles, 50 scans;
3. **திராவிட சம்பத்து** / *Dravidian Wealth* — 2 articles, 16 scans, damaged/out-of-order source.

Implementation is merged and production-verified. **This section is the proposed durable control
closure: Wave 3 becomes COMPLETE and CLOSED in the control record only when this control-only PR is
independently reviewed at its exact head and merged.** Until then, do not treat the branch text alone
as a merged control checkpoint.

### Implementation identity and exact-head gate

| | |
|---|---|
| Implementation PR | `pugazg/kalaignar-autobiography#66` |
| First reviewed head — **REJECTED** | `d50aefae5cc5a665230a4185aab43d16c7dfeb81` |
| Exact independently approved head | **`c4f40f7f77a115700915f17e65c2a2a1ddf54bbd`** |
| Squash merge / implementation `main` | **`c4660c49edb20895d11751e4454942e46e8b0951`** |
| Merged tree | **`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`** |
| Parent/base | `4fd45a92663abbe70ff0c0a605168314cd36e44c` |
| Merged | 2026-09-02T08:07:00Z |
| Changed files | **23** — 15 implementation/CI and 8 generated |
| Diff size | **+13057 / -166** |
| Post-merge Library CI | run **`33607016982`** — success |
| Production deployment | Vercel — **success** for `c4660c49…` at 2026-09-02T08:09:30Z |

The approved PR-head tree and the squash-merged `main` tree are **exactly the same tree SHA**:
`c6360aaffa4afed0b51d46ef7fa3cc5b12a11e15`. The squash introduced no implementation drift.

#### Exact-head lesson — green CI is not an approval substitute

The first candidate head `d50aefae…` had green CI but **was not approved**. Independent exact-head
review found that `app/essays/[slug]/source/page.tsx` still emitted a hard-coded source-page metadata
string inherited from சக்கரவர்த்தியின் திருமகன், falsely telling every Wave-3 publication that it had
a first-edition/reprint distinction, a 14-article map and rights. The visible source component had been
generalized, but the route metadata had not.

The repair made `/source` metadata data-derived from each publication's own provenance, added validator
coverage for that exact defect class, and raised the Wave-3 validator from 472 assertions / 6 groups /
20 negative tests to **510 assertions / 7 groups / 23 negative tests**, all passing. The repaired head
`c4f40f7f…` was independently reviewed and **APPROVED FOR MERGE**; only that SHA was merged.

**Standing rule strengthened by Wave 3:** successful build/CI does not replace exact-head review, and
route metadata is part of source-form correctness. If a reviewed head changes, approval is void.

### Source freeze

| | |
|---|---|
| Source repository | `pugazg/kalaignar-essays` |
| **Frozen implementation pin** | **`6814e979fd3c2cefa14cbeb17eeec28164ce28f5`** |
| `publications/kayittril-thongiya-kanapathi` | **`ca1c92591b9389e60d44b9683af849e3a682e528`** |
| `publications/unarchchimaalai` | **`f49d77a0733ca75f7a96fb6a1cf4631e375b05d0`** |
| `publications/thiraavida-sampaththu` | **`fe0f6ea0482ac2cd0e8c4558edd3b452e249dbdd`** |

Source identities at the frozen release:

| work | controlling PDF | SHA-256 | scans |
|---|---|---|---:|
| கயிற்றில் தொங்கிய கணபதி | `TVA_BOK_0064013_கயிற்றில்_தொங்கிய_கணபதி.pdf` | `927d05fb27a2545d6732acd9bf8bde04dba2d22546d171b502703a773b40f45a` | 17 |
| உணர்ச்சிமாலை | `TVA_BOK_0063821_உணர்ச்சிமாலை.pdf` | `d2d45de049505218fd612bf71949135e34ecb317ffb5d003dfe59a3a0608461d` | 50 |
| திராவிட சம்பத்து | `TVA_BOK_0064196_திராவிட_சம்பத்து.pdf` | `09d567abb30a0beacc1efd1e1fb757f01da93968f5582c9b1b8859b87dac2165` | 16 |

The source repository is intentionally fast-moving because **`publications/ina-muzhakkam/` is active**.
At control-close-out preparation time its live `main` was
`8d3b3e6792f6b3a7783ff3621f4d5c8e3e9be4d4` (`Advance Ina Muzhakkam P5 frontier through scans 43-44`).
The three Wave-3 work trees at that newer live head were re-computed and remained **exactly** the frozen
values above. Therefore unrelated future source-`main` movement does not repin or reopen Wave 3.

**`இன முழக்கம்` was explicitly excluded** from Wave 3 because it was source-active. It is not the
fourth work in this batch and is not automatically selected for any later wave.

A second source-status lesson is retained for **கயிற்றில் தொங்கிய கணபதி**: its older
`PUBLICATION_COMPLETION_REVIEW.md` ends with historical wording that English work may begin, but the
later authoritative `translations/en/RELEASE_REPORT.md` records **E7 PASSED / English release gate
closed**. A stale earlier status paragraph must never override a later release authority.

### Source-form architecture shipped

The existing Essays implementation was still partly a one-publication model. Wave 3 generalized only
what the three sources required:

- source-page and page-transition printed numerals are nullable — absence stays absence;
- article coverage is ordered `scanRuns[]`, not a single `{from,to}` range;
- printed pagination is a discriminated `range | partial | none` witness;
- article numbering distinguishes printed contents numbers from archive reading ordinals;
- first-edition, controlling-edition and publication-wide printed-page facts are optional/source-led;
- `projectRights` is optional — no rights block was invented for the three Wave-3 pamphlets;
- damaged/out-of-order sources can carry explicit `readingOrder` and `physicalCondition` provenance;
- landing, article, source UI and all three route metadata families are source-form-aware through
  `lib/essay-source-facts.ts`.

The importer is deterministic and pinned: one shared Wave-3 Essays parser/core plus explicit work
declarations, historical source commit + per-work tree guards, no source PDFs vendored and byte-identical
reruns from clean state.

### திராவிட சம்பத்து — source order must remain non-normalized

This publication is the structural stress case and must not be simplified later:

- article 1 **திராவிட சம்பத்து**: ordered scan runs **`5–6, 13–16`**;
- article 2 **ஐயர் அறிவிக்கிறார்!**: ordered scan runs **`12, 3`** — the descending order is deliberate;
- reconstructed physical reading order:
  **`1 → 2 → 9 → 10 → 5 → 6 → 13 → 14 → 15 → 16 → 7 → 8 → 11 → 12 → 3 → 4`**;
- no visible printed pagination is invented;
- torn/missing source text is **not reconstructed**.

Production preserves these facts. The visible `/source` body summarizes the damage/reading-order
provenance; the exact reconstruction policy and literal arrow sequence are carried in the deployed
provenance record rather than rendered as full visible rows. Record this distinction precisely — the
facts are **available**, but not every datum is printed in the visible source-page body.

### Production boundary

Wave 3 moved the public census as follows:

| metric | pre-Wave-3 | post-Wave-3 | delta |
|---|---:|---:|---:|
| Published works | 68 | **71** | +3 |
| Essays & Articles works | 1 | **4** | +3 |
| Non-empty shelves | 9 | **9** | 0 |
| **Next build static-route count** | 3109 | **3128** | **+19** |
| Prerendered `.html` files | 3101 | **3120** | **+19** |
| **Sitemap URLs** | 3097 | **3116** | **+19** |

The `.html`, static-route and sitemap figures are **three distinct measurements** even though each
happened to move by +19. Sitemap duplicates: **0**. The Essays route family contains **35** URLs after
Wave 3: 19 from the new batch plus 16 from சக்கரவர்த்தியின் திருமகன்.

Production verification checked **all 19/19** new Wave-3 routes individually and all returned 200.
The existing 16 சக்கரவர்த்தியின் திருமகன் routes also remained 200.

The previously rejected metadata defect was verified absent in production:

- கயிற்றில் தொங்கிய கணபதி `/source`: single article; no 14-article, reprint, 2018 or rights claim;
- உணர்ச்சிமாலை `/source`: 10-article map; no 14-article, reprint or rights claim;
- திராவிட சம்பத்து `/source`: 2-article map + damage + reconstructed-reading-order metadata; no
  14-article, reprint or rights claim;
- சக்கரவர்த்தியின் திருமகன் `/source`: its real 14-article map, first-edition/reprint distinction and
  established rights record remain intact.

Other production fidelity checks: உணர்ச்சிமாலை has 10 article navigation entries and excludes scan 50's
மணமகள் advertisement; கயிற்றில் தொங்கிய கணபதி publishes one article and excludes advertisement scans
16–17. No source absence was normalized into an invented publication fact.

### Validator and reference regression

Final Wave-3 batch validator: **510 assertions · 7 groups · 0 failed**. **23/23 negative tests proven**,
including wrong pin/tree drift, missing/duplicate article, quotation/voice corruption, imported
advertisements, invented pagination/reprint/rights, rejection of the intentionally frozen
`strict-reviewed` vocabulary, flattening `5–6, 13–16` to `5–16`, sorting `12, 3` to `3, 12`, replacing
the reconstructed reading order with numeric scan order, accidental Ina Muzhakkam inclusion, reference
regression and restoration of the rejected hard-coded source metadata.

**சக்கரவர்த்தியின் திருமகன் is the regression benchmark.** Its generated JSON changed shape because
the shared types generalized, so byte identity was not claimed. Semantic equivalence was proved:
14 articles; identical Tamil and English reading blocks; same slugs/order/titles/contents witnesses and
page transitions; 1956 first edition; 2018 controlling reprint; printed page count 80; established
rights record; mixed-voice behavior intact. Its validator passed **188 assertions, 0 failed** and its
16 production routes remained healthy.

### Standing state after Wave 3

- **Wave 4 is NOT SELECTED, NOT AUTHORIZED and no Wave-4 readiness census has started.** Closing Wave 3
  selects nothing. Wait for explicit owner authorization before any next-wave readiness or selection.
- **Film Songs formal control close-out remains pending** and requires its own explicit authorization.
- **Validator migration remains PAUSED.**
- **Native mobile remains ON HOLD.**
- **Manimagudam is never auto-selected**; it requires its own release/readiness gate and owner
  authorization if considered later.
- **`kalaivanar-nsk-memorial-day-audio-06` is never auto-selected**; it remains separate source-active
  archive work.

**Do not reopen Wave 3** merely because the Essays source repository continues to advance for other
publications.

---

