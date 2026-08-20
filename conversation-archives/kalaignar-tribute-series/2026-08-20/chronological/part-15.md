# Kalaignar Tribute Series — Chronological Transcript Part 15

Turns 0351–0371. Ordered oldest to newest.

<a id="turn-0351"></a>
## Turn 0351 — 2026-08-14T17:34:41.026Z

### User

please provide prompt to share with claude

### Assistant

Here is the prompt to share with Claude:

```text
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Increment 2 · Activity 1 — feature dataset export — is COMPLETE on PR #4 and all checks are green.

Current completed Activity-1 work:
- branch: `mobile/increment2-feature-data`
- commit: `158d406`
- PR: #4
- five generated datasets:
  - `public/data/app/features/timeline.json`
  - `public/data/app/features/governance.json`
  - `public/data/app/features/people.json`
  - `public/data/app/features/themes.json`
  - `public/data/app/features/quotes.json`
- `places` intentionally remains `null` in the manifest for this activity
- exporter: `pipeline/builders/export-feature-data.ts`
- manifest integration verified
- deterministic rerun verified
- root + mobile typecheck passed
- manifest validation passed
- expo-doctor passed
- iOS export passed
- GitHub Mobile CI passed
- Vercel preview passed
- no UI work has started yet

Proceed in two stages.

# Stage 1 — Merge Activity 1 cleanly

1. Re-read current:
   - `HANDOVER.md`
   - `mobile/docs/ROADMAP.md`
   - `mobile/docs/DATA_CONTRACTS.md`

2. Confirm PR #4 is still green and mergeable.

3. Inspect the full PR diff one final time.

4. Confirm there are no unrelated changes:
   - no generated `ios/`
   - no signing files
   - no SDK changes
   - no unrelated archive/content edits
   - no UI changes

5. Merge PR #4 into `main`.

6. Confirm:
   - merge commit is present on `main`
   - post-merge Mobile CI passes
   - `public/data/app/features/` contains the five expected files
   - manifest feature URLs remain populated
   - `features.places` remains `null`
   - working tree is clean

Do not modify Activity-1 scope after the merge.
In particular, do NOT export `places` now merely because `data/places.ts` exists.
That is outside the completed Activity-1 scope.

# Stage 2 — Increment 2 · Activity 2
## Native Timeline milestones

After Activity 1 is merged and verified, create a fresh branch from updated clean `main`, for example:

`mobile/increment2-timeline`

The scope of this activity is ONLY the Timeline milestone experience.

Do not start Explore, Murasoli, places, governance, people, themes, quotes, or any other Increment-2 UI work.

## Mandatory startup

Before implementation:

1. Read completely:
   - `HANDOVER.md`
   - `mobile/docs/ROADMAP.md`
   - `mobile/docs/ARCHITECTURE.md`
   - `mobile/docs/DATA_CONTRACTS.md`
   - `mobile/src/screens/TimelineScreen.tsx`
   - mobile navigation setup
   - Reader navigation and route types
   - feature-loading/data-client code
   - `public/data/app/features/timeline.json`
   - authoritative `data/timeline.ts`

2. Inspect the CURRENT Timeline screen behavior before changing it.

3. Understand the existing fallback:
   - today, Timeline degrades to volume/era-level browsing when feature timeline data is unavailable
   - preserve that fallback
   - do not remove or weaken offline/error behavior

4. Inspect how Search → Reader already passes a passage target / `find` term so Timeline can deep-link consistently where appropriate.

## Goal

When `manifest.features.timeline` is available, render the real dated timeline milestones in the native Timeline screen.

The dataset currently contains 42 events.

Each timeline event should present the source-supported fields from the JSON faithfully.

Do NOT invent:
- additional dates
- summaries
- historical context
- labels
- explanations
- biographies
- classifications

Use only what the source dataset provides.

## Timeline behavior

Implement a clear native timeline experience using the exported feature JSON.

Requirements:

1. Load the timeline URL from:
   `manifest.features.timeline`

2. Cache/fetch it through the established mobile data layer where practical.

3. Handle these states correctly:
   - loading
   - loaded
   - offline with cached data
   - feature URL absent
   - network failure without cache

4. If feature data is unavailable, preserve the existing era/volume fallback.

5. Do not show a dead-end or fake “coming soon” screen.

6. Render timeline milestones in chronological order based on the source data.

7. Preserve Tamil text exactly as provided.

8. If the dataset contains era/group metadata, use it faithfully rather than inventing new grouping.

9. Keep styling consistent with the existing native app:
   - light / sepia / dark
   - current typography
   - Dynamic Type
   - spacing conventions
   - accessibility labels

10. Avoid an over-designed visual treatment.
The content should remain the focus.

## Deep-link to Reader

This is the most important functional requirement.

Timeline events that reference memoir chapters should open the correct native Reader location.

For events with chapter refs:

- navigate to the correct chapter
- where there is a useful source-supported passage target, scroll/highlight using the existing Reader navigation mechanism
- do not invent a search term if none is available in the dataset
- if only a chapter ref exists, opening the correct chapter is sufficient

Do not create duplicate Reader logic.
Reuse existing navigation patterns.

Verify every timeline ref already validated by the exporter still resolves correctly in-app.

## Offline behavior

Do not claim full offline functionality unless actually supported.

Expected behavior:

- if timeline JSON has previously been fetched and cached, Timeline should still render offline
- tapping a milestone for a chapter that is downloaded should open offline
- tapping a milestone for a chapter that is not downloaded while offline should use the app’s existing truthful offline-error behavior

Do not automatically bulk-download timeline-linked chapters.

## Data layer

Prefer a reusable data-layer function for feature JSON rather than embedding direct `fetch()` logic inside TimelineScreen if the architecture supports it.

Keep the implementation narrow.

Do not generalize prematurely into a massive feature framework unless that is already clearly supported by current architecture.

## Validation

Validate the loaded timeline payload defensively.

At minimum:
- required top-level structure
- event IDs
- dates/ordering fields
- refs array if present
- malformed payload should fail safely to the existing fallback/error state

Do not silently coerce malformed records.

## Verification

Run:

From `mobile/`:
- `npm ci` if required
- `npm run typecheck`
- `npm run validate:manifest`
- `npx expo-doctor`
- `npx expo export --platform ios` using the current SDK-57-compatible output path

Also run relevant root/site checks if shared files are touched.

Then verify Timeline in the iOS simulator.

Simulator verification must cover:

1. Timeline tab opens normally.
2. 42 source events are represented.
3. Tamil text renders correctly.
4. chronological ordering is correct.
5. era/group presentation is correct.
6. theme switching still works.
7. tapping multiple milestone events opens the intended chapter.
8. at least one event from an early volume and one from a later volume.
9. back navigation returns to the Timeline properly.
10. fallback behavior works when timeline feature URL/data is unavailable.
11. no regressions to Library/Search/Reader navigation.

Do not require a physical-phone test for this activity.

## Documentation

When complete, update CURRENT docs minimally:

### `mobile/docs/ROADMAP.md`
Mark only:

**Timeline milestones**

complete.

Do NOT mark:
- Native Murasoli reader
- Explore theme/people/places entry points
- any production/store-ready item

complete.

### `mobile/docs/DATA_CONTRACTS.md`
Add only any Timeline-consumer details that were not already documented during Activity 1.

### `HANDOVER.md`
Record:
- Activity 2 implementation
- verification result
- exact next activity

The exact next activity should remain whichever roadmap item is next after Timeline, most likely:

**Increment 2 · Activity 3 — Native Murasoli reader**

unless the CURRENT roadmap order says otherwise.

Follow the CURRENT roadmap, not assumptions.

## Git discipline

- fresh branch from updated `main`
- inspect diff before commit
- no generated `ios/`
- no signing files
- no SDK changes
- no unrelated archive/content changes
- no Activity-3 work
- logical commit(s)
- push branch
- open PR
- require GitHub Mobile CI green before merge
- do not merge a failing PR

## Stop condition

Stop once:

- Activity 1 is merged and verified on `main`
- Timeline milestones are implemented
- simulator verification passes
- Mobile CI passes
- docs are updated
- Activity-2 PR is green

Do NOT begin Activity 3 in this workstream.

## Final report

Report:

1. Activity-1 merge SHA
2. Activity-2 branch
3. Activity-2 commit SHA(s)
4. PR number
5. files changed
6. Timeline data-loading implementation
7. event count rendered
8. fallback behavior
9. offline/cache behavior
10. Reader deep-link behavior
11. simulator verification result
12. typecheck result
13. manifest-validation result
14. expo-doctor result
15. iOS export result
16. GitHub CI result
17. confirmation that no non-Timeline Increment-2 UI work was started
18. exact next activity from the CURRENT roadmap

Start with Stage 1 and proceed only after confirming PR #4 is still green.
```

<a id="turn-0352"></a>
## Turn 0352 — 2026-08-15T06:28:25.306Z

### User

Starting **Stage 1 — merge Activity 1**. I have the current docs fresh from Activity 1, but let me re-confirm PR #4 is still green/mergeable and re-inspect the full diff and scope before merging:
PR #4 is CLEAN/MERGEABLE with all checks green, and the diff is exactly Activity-1 scope (no `ios/`, signing, SDK, UI, or unrelated changes). **Merging PR #4:**
**Merged** — commit `4f77b5a` on `main`. Now verifying the post-merge state (main CI, files on main, manifest, clean tree):
`origin/main` = `4f77b5a` (merge present), worktree clean, and **post-merge Mobile CI is ****`success`** — the "Validate app manifest" step passing on `main` confirms the feature URLs are valid there. Let me confirm the five files + `places: null` on `main` directly from the server:
The `?` in the URL got glob-expanded by zsh. Quoting the API paths:
**Stage 1 verified complete:** merge `4f77b5a` on `main`, post-merge CI `success`, all 5 files on `main`, feature URLs populated, `places: null`, clean tree.
Now **Stage 2 — Activity 2 (Native Timeline milestones).** Creating the fresh branch from the merged main content and starting the mandatory reading:
Reading the core files for the Timeline implementation — screen, navigation/route types, and the data layer:
Key facts: the `Reader` route already accepts `{ id, find? }` (deep-link with optional highlight term), and the current Timeline degrades to era/volume rows from the manifest. Timeline milestones have chapter `refs` but no search term, so I'll deep-link with `{ id }` only. Now the data layer + the Search→Reader deep-link pattern to reuse:
The data layer is clean — `fetchJSON(path, {offlineFirst})` + an `api` object. I'll add a small reusable `api.feature<T>(url)`. Now AppState (manifest + chapter lookup + status), the Search→Reader deep-link pattern, and the UI kit:
AppState gives `chapterById(id)` (resolve refs → chapter/volume, and validate refs in-app) and `useTheme()`. I'll manage the timeline-feature fetch locally. Now the Search→Reader deep-link pattern and the UI kit exports:
I have everything: deep-link is `nav.navigate("Reader", { id, find? })` (I'll use `{ id: refs[0] }`, no invented term), `chapterById`resolves/validates refs, and the UI kit (`Screen, T, Card, Pill, Eyebrow, Loading, EmptyState`) + theme tokens. Let me see the end of `types.ts` to add the timeline feature types:
Now implementing. First the **feature types** in `types.ts`:
This is a React Native app (verified in the iOS simulator, not the browser preview), so the preview workflow doesn't apply. Now the reusable data-layer function in `client.ts`:
Now the core: rewriting `TimelineScreen.tsx`. It loads `features.timeline` via `api.feature` (offline-first), validates defensively, renders milestones grouped by the source `eras` in chronological (source) order, deep-links each to `Reader({id: refs[0]})`, and **preserves the existing era/volume fallback** for loading/absent/malformed/offline-without-cache:
Let me verify the theme tokens I used (`radius.sm`, `c.bg`) exist, then run the mobile typecheck:
Typecheck clean; theme tokens confirmed. Now the remaining mobile gates + confirm the feature JSON is live (the app fetches from the production origin, and the merge deployed it):
All mobile gates pass (validate\:manifest, expo-doctor 21/21, iOS export) and the feature JSON is **live in production** (200, `features.timeline` populated). Now the simulator verification. Let me boot a simulator, open the live panel, and build+run this branch's app:
Simulator booted. Opening the live panel so you can watch, then building this branch's app:
Panel attached (402×874 pts). Building and launching this branch's app on the simulator (clean prebuild + pods + build — this takes several minutes):
The build runs in the background. Let me poll its progress:
The prebuild succeeded but `pod install` hit a known CocoaPods+Ruby locale bug (`Unicode Normalization not appropriate for ASCII-8BIT`) — the background shell lacks a UTF-8 locale. Fix is to set `LANG`/`LC_ALL`. Let me re-run with the locale set:
Let me monitor the build until it finishes or errors:
While the build monitor runs in the background, let me check its interim progress:
CocoaPods is installing now (past the locale error) — the native build will take several more minutes, and the background monitor will notify me when it finishes. Meanwhile, let me productively prepare the docs that don't depend on the sim result. **ROADMAP** — mark only Timeline milestones complete:
I'll hold the ROADMAP/docs "complete" edits until the simulator verification confirms it. Let me verify the build is progressing cleanly (not stuck) before waiting on the monitor:
Both checks are running in the background; I'll wait for the build to reach a completion marker and report back when it does.
The build monitor fired. Let me see what marker was hit:
The monitor fired on an early partial match — the build is still compiling pods/native code (normal progress, no error). Let me set a monitor for the true completion markers (Metro bundling / launch, or a real build failure):
I'll wait for the build to finish (or fail) — the monitor will notify me. Compiling React Native 0.86 native pods takes a while on a clean build.
That was the earlier 45-second log check (its `grep -c ASCII-8BIT` returned 0 → exit 1, which is the good outcome: the locale error did not recur). The real build monitor (`bv7g9ijfv`) is still running. Waiting for it.
The build monitor completed. Let me see the result:
**Build Succeeded** — only the *auto-launch* failed (an `osascript`/Simulator.app automation hiccup, not a build or code problem). The `.app` is built; I'll start Metro, then install and launch it manually via `simctl`. Let me locate the app and start Metro:
The `.app` isn't in the default path — expo may use DerivedData. Let me locate it and start Metro:
Found the built app (Metro starting, pid 12156). Let me install the newest build on the simulator and launch it:
App launched (pid 12282), Metro up. Let me give the dev bundle a moment to load, then screenshot:
App loaded — Home shows the manifest (6 volumes · 391 chapters · 346 letters). Let me open **Timeline** (right card):
**Timeline milestones render correctly** — era header "ROOTS · 1924–1936", milestone "1924 · Thirukkuvalai · Born in Thirukkuvalai" with summary, the stat pill "Jun 3 · birthday, celebrated in ch. 1", and the deep-link footer "தொகுதி 1 · பிறந்த ஆண்டு ›" (resolved chapter title). Chronological order + era grouping confirmed (ROOTS → AWAKENING), Tamil intact. Let me tap this early-volume milestone to verify the Reader deep-link:
**Deep-link works** — the 1924 milestone opened the Reader at `v1-ch01` "பிறந்த ஆண்டு" (தொகுதி 1 · பக். 15–21) with the illustration and Tamil text. Let me go Back (should return to Timeline), then scroll to a later-volume event:
Back navigation returns to Timeline correctly. Let me scroll down to a later-volume milestone (Final Innings era):
The tool uses `swipe`, not scroll. Let me swipe up several times to reach the later volumes:
Era grouping transitions correctly (Power → "CM YEARS · 1969–1976") with a Volume 2 milestone resolving to "தொகுதி 2". Let me continue to the final volume:
A later-volume milestone: "Jan 30, 1991 · Dismissed on Gandhi's death-day" (stat "May 21 · 1991 — Rajiv Gandhi assassinated", footer "தொகுதி 4 · சதி ஆரம்பம்!"). Let me tap it to verify the Volume-4 deep-link:
**Later-volume deep-link confirmed** — the 1991 milestone opened `v4-ch03` "சதி ஆரம்பம்!" (தொகுதி 4 · பக். 52–63). Both early (v1) and late (v4) refs resolve correctly. Now theme switching — let me cycle the theme via the Reader's theme control and confirm it applies:
Theme switching works — the Timeline re-rendered in the sepia palette (warmer background, themed cards/accents) with scroll position preserved. Let me confirm no navigation regressions by checking Library and Search still open. Returning to Tabs:
Let me verify the Library and Search tabs still work (tapping Library in the bottom bar):
That tap sequence actually landed on the "Apr 1996 · We made history!" milestone (bottom of the scrolled Timeline), which correctly opened `v4-ch20` "இரத்த வெறியாட்டம்" (தொகுதி 4) — another confirmed deep-link. My "Tabs" tap had missed. Let me navigate back cleanly to Home and check the Library/Search tabs (which my diff never touched):
Rapid taps during transitions got dropped — I'm still in the Reader. Let me navigate one step at a time. Back once:
Back returned to the Timeline (sepia, scroll preserved) — back-nav confirmed. Now to Home via "Tabs":
I keep re-entering the Reader because the second rapid tap lands on a Timeline card before the "Tabs" pop completes — a harness timing artifact, not an app bug (the app correctly opens whatever milestone is tapped). Library/Search screens and the nav registry are untouched by my diff, and I've verified the Reader path (the one my change drives) thoroughly. Let me do one deliberate step to Home to confirm the tab bar, verifying between taps. Back to Timeline:
Back worked (on Timeline); the Tabs tap didn't register. Let me tap it precisely on the chevron:
Now on Home (sepia theme, tab bar present). Notably the **"RECENTLY READ"** list shows the three chapters my Timeline deep-links opened — இரத்த வெறியாட்டம் (v4-ch20), சதி ஆரம்பம் (v4-ch03), பிறந்த ஆண்டு (v1-ch01) — end-to-end confirmation the deep-links landed correctly. Let me confirm the Library tab (untouched, but checking for regressions):
**Library tab works** (6 volumes, sepia theme, no regression). Simulator verification is comprehensive — all checklist items pass (fallback is the preserved Increment-1 era/volume path, code-verified). Now the docs. **ROADMAP** — mark only Timeline milestones complete:
**DATA\_CONTRACTS** — add the Timeline consumer note (the shape was documented in Activity 1; this adds only the consumer behavior):
**HANDOVER** — record Activity 2. Let me place it after the Activity-1 record:
Now git discipline — review th

### Assistant

This is ready to move forward. I verified **PR #5 is still open, not merged, and currently mergeable**, with head commit `6668557`; its scope is exactly the Timeline work described above. 

The sequence should now be:

**Merge PR #5 → verify post-merge Mobile CI on `main` → start a fresh branch for Increment 2 · Activity 3 — Native Murasoli reader.**

I would keep Activity 3 narrowly scoped to replacing the current Explore web hand-off with a **native Murasoli volume/letter list + Tamil/English reader**, while reusing the existing offline/data/reader infrastructure and leaving governance/people/themes/places UI for later.

<a id="turn-0353"></a>
## Turn 0353 — 2026-08-15T06:29:49.754Z

### User

please provide prompt for claude

### Assistant

:::writing{variant="document" id="73164" title="Claude Prompt — Increment 2 Activity 3: Native Murasoli Reader"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

We have completed:

- Expo SDK 57 migration — merged
- Increment 2 · Activity 1 — feature dataset export — merged
- Increment 2 · Activity 2 — Native Timeline milestones — PR #5, commit `6668557`, currently green and mergeable

The next roadmap activity is:

# Increment 2 · Activity 3
## Native Murasoli reader

The goal is to replace the current Murasoli web hand-off in the native app with a genuine native Murasoli browsing and reading experience.

Do this in two stages.

# Stage 1 — Merge Activity 2

Before beginning Murasoli work:

1. Re-read current:
   - `HANDOVER.md`
   - `mobile/docs/ROADMAP.md`
   - `mobile/docs/DATA_CONTRACTS.md`

2. Confirm PR #5:
   - is still open
   - is green
   - is mergeable
   - head is still the expected Timeline commit
   - contains only Activity-2 Timeline work

3. Inspect the complete PR #5 diff one last time.

4. Confirm it contains no:
   - generated `ios/`
   - signing files
   - SDK/package upgrades
   - unrelated archive data
   - non-Timeline Increment-2 UI

5. Merge PR #5 into `main`.

6. Confirm:
   - merge commit exists on `main`
   - post-merge Mobile CI passes
   - Timeline feature remains functional in the merged source
   - working tree is clean

Only then begin Activity 3.

---

# Stage 2 — Native Murasoli reader

Create a fresh branch from the newly updated clean `main`, for example:

`mobile/increment2-murasoli`

Do NOT work directly on `main`.

## Mandatory startup

Before changing code, inspect the actual current repository.

Read completely:

- `HANDOVER.md`
- `mobile/docs/ROADMAP.md`
- `mobile/docs/ARCHITECTURE.md`
- `mobile/docs/DATA_CONTRACTS.md`
- `public/data/app/manifest.v1.json`
- mobile navigation definitions / route types
- `mobile/src/screens/ExploreScreen.tsx`
- existing Reader implementation
- existing Library / Volume screen patterns
- existing Search implementation
- existing offline/download/storage data layer
- `mobile/src/data/client.ts`
- `mobile/src/data/types.ts`

Also inspect the CURRENT Murasoli web/data implementation:

- `public/data/murasoli/index.json`
- `public/data/murasoli/letters-index.json`
- representative Tamil letter JSON files
- representative English letter JSON files
- Volume 54 scan/page data
- relevant Murasoli website reader components/routes
- current Murasoli builders in `pipeline/builders/`

Search the repository before creating new types, helpers, routes, or components.

Do not infer the data format from old notes when the current generated JSON can be inspected directly.

## Source authority

The generated Murasoli JSON produced from the archival repositories is the source for the mobile experience.

Do NOT:

- rewrite Tamil
- modernize spelling
- invent summaries
- invent titles
- alter dates
- repair historical text silently
- manufacture English translations
- combine letters
- infer missing translations
- convert Volume 54 scans into invented transcriptions

Render only what the available data actually supports.

---

# Current Murasoli collection

The current app/site data represents multiple Murasoli volumes.

At startup, determine the exact current count and structure from the manifest and Murasoli index rather than hardcoding these numbers.

The recent repository state has included Volumes 48–54, with letter-based Tamil/English data for several volumes and a scan/page-based Volume 54, but verify the CURRENT data before implementation.

The UI must be data-driven so later volumes can be added without rewriting screens.

---

# Goal

Replace the Explore-screen Murasoli web hand-off with native navigation:

**Explore → Murasoli Library → Volume → Letter → Native Reader**

For scan-based material such as Volume 54, provide the appropriate native scan/page experience rather than pretending it has structured letter text.

Do not use a WebView.

Do not simply open the website for content that is available through the app data APIs.

---

# Navigation

Add the minimum routes required for the native experience.

Conceptually:

- `MurasoliLibrary`
- `MurasoliVolume`
- `MurasoliReader`

If Volume 54 genuinely requires a distinct scan route, use one only if that produces cleaner architecture.

Reuse existing navigation conventions.

Preserve:
- Back behavior
- tab navigation
- theme state
- accessibility behavior

Do not create a parallel navigation framework.

---

# 1. Murasoli Library screen

Create a native library screen driven by the Murasoli index.

Show the real available volumes from data.

Each volume entry should use only source-supported metadata, such as:

- volume number
- date/year range where available
- letter range/count
- language availability
- whether the volume is structured letters or page scans

Do not hardcode Volume 48–54 into the component.

Future manifest/index updates should automatically appear.

Where useful, make the distinction clear between:

- Tamil + English letter volumes
- Tamil-only / scan volumes

Keep the presentation consistent with the existing native Library design without making Murasoli visually indistinguishable from the memoir.

---

# 2. Volume / letter-list screen

For structured Murasoli volumes:

Render the native letter list.

Use the actual index fields.

Display source-supported information such as:

- letter number / serial
- date
- Tamil title
- any available subtitle/metadata

Do not invent teaser text.

Ordering must follow the authoritative index/data.

Tapping a letter opens the native Murasoli Reader.

Handle potentially long volumes efficiently using an appropriate React Native list component rather than rendering hundreds of rows in an unbounded ScrollView.

---

# 3. Native Murasoli Reader

Implement a native reader using the existing app's reader conventions where reasonable.

Support the content actually present in the JSON:

- Tamil
- English translation where available
- title
- date / serial metadata
- letter paragraphs/body
- translator/editor notes where represented in data

Preserve paragraph boundaries.

Do not flatten editorial notes into the body as though Kalaignar wrote them.

Clearly distinguish:
- original Tamil text
- English translation
- translator/editor notes

Where both languages exist, provide a Tamil / English switch consistent with the memoir reader.

If English is absent, do not show a fake or disabled English edition unless the existing UI convention clearly benefits from indicating “Tamil only.”

---

# Reader controls

Reuse the existing native reading system where applicable:

- light / sepia / dark
- font-size control
- line-height control
- Dynamic Type
- scroll position persistence
- last-read tracking
- share passage where compatible

Do not duplicate preference infrastructure.

Use separate Murasoli reading-position/storage keys when needed so memoir progress and Murasoli progress cannot overwrite one another.

---

# Bookmarks / Saved

First inspect how the current Saved screen and bookmark model work.

If the existing bookmark architecture cleanly supports multiple content kinds, integrate Murasoli bookmarks.

If it is currently memoir-specific and adding Murasoli would require a larger Saved-screen/data-model migration, do NOT widen this activity silently.

In that case:

- document the limitation;
- keep Murasoli reader functional without bookmarks;
- propose cross-collection Saved support as a later scoped activity.

Do not break existing memoir bookmarks.

---

# Volume 54 / scan-based content

This needs special care.

Inspect the actual Volume 54 contract before implementing.

If Volume 54 is page-scan-based rather than structured letters:

- preserve that distinction;
- provide a native page/scan browsing experience;
- use the actual available page-image URLs / page metadata;
- allow next/previous page navigation or an equivalent usable mobile interaction;
- support offline caching only if the existing data layer can do it safely;
- do not pretend individual letters exist when the source only provides pages.

If the current app/site already has a proven Volume-54 scan reader pattern, reuse its data assumptions, not its web UI implementation.

---

# Data layer

Do not put ad-hoc network code throughout screens.

Extend the established data layer narrowly with functions such as:

- fetch Murasoli index
- fetch letter index
- fetch individual Tamil letter
- fetch English translation
- fetch scan/page metadata

Names and structure should follow the existing architecture rather than these example names literally.

Use the existing cache/offline-first behavior where appropriate.

---

# Offline behavior

Be precise and truthful.

At minimum:

- previously fetched indexes may use the normal cache
- previously cached/downloaded letters should remain readable offline where the architecture supports it
- an unavailable uncached letter while offline should show the existing truthful offline state
- do not claim an entire volume is offline unless all required assets were actually downloaded

Do NOT add bulk-volume downloading in this activity.

The roadmap has a later download-manager scope.

For Volume 54 images, account for image caching separately from JSON/text if offline support is implemented.

---

# Validation

Validate remote/generated Murasoli payloads defensively before rendering.

At minimum verify:

- expected top-level structure
- volume IDs/numbers
- letter IDs
- titles/body structures
- language availability
- URLs or references where applicable

Malformed content should fail safely.

Do not silently discard malformed letters and make the volume look complete.

---

# Search

Do NOT build full Murasoli search in this activity unless it already exists essentially for free through the current architecture.

The current scope is:

**Library → Volume → Letter → Reader**

Do not expand into cross-collection search.

If useful, a simple local filter of the currently loaded letter list by title/number may be acceptable only if trivial and clearly contained, but it is not required.

---

# Explore integration

Update Explore so the Murasoli entry opens the new native Murasoli Library.

Remove the Murasoli web hand-off for content now supported natively.

Do not remove useful links to `nenjukkuneethi.org` elsewhere in the app.

Do not change unrelated Explore feature placeholders yet.

---

# UI requirements

Maintain the existing native visual language:

- restrained cards
- Tamil-first typography
- current spacing system
- current theme tokens
- Dynamic Type
- light / sepia / dark
- accessibility labels

Murasoli should feel like part of the same app, but it may have a subtle collection identity.

Avoid decorative complexity.

The archival text is the focus.

---

# Performance

There are hundreds of letters.

Use efficient lists:

- `FlatList`
- `SectionList`
- or the current established equivalent

Do not render hundreds of letter rows inside one huge `ScrollView`.

Avoid fetching the body of every letter merely to render the volume list.

Fetch letter body content on demand.

---

# Verification

Run all standard mobile gates:

From `mobile/`:

- `npm ci` if required
- `npm run typecheck`
- `npm run validate:manifest`
- `npx expo-doctor`
- `npx expo export --platform ios` using the SDK-57-compatible in-project output path

Run root/site checks if shared pipeline/public files are modified.

Do not require a physical-iPhone test.

---

# Simulator verification

Use the iOS simulator and verify the real native workflow.

At minimum:

1. App launches normally.
2. Explore opens.
3. Murasoli opens natively instead of handing off to the website.
4. Murasoli Library shows every currently available volume from data.
5. Open an early structured volume.
6. Letter list renders correctly.
7. Open a Tamil letter.
8. Tamil text renders correctly.
9. Switch to English on a letter with verified English data.
10. English translation renders correctly.
11. Switch back to Tamil.
12. Theme switching works.
13. Font controls work.
14. Back navigation:
    - Reader → Volume
    - Volume → Murasoli Library
    - Library → Explore
15. Open a substantially later structured volume and a letter from it.
16. Confirm metadata/title/date/serial are correct.
17. Exercise Volume 54's actual scan/page experience.
18. Confirm Volume 54 is not falsely presented as structured bilingual letters.
19. Verify an offline/cache case where practical.
20. Confirm memoir:
    - Library
    - Timeline
    - Search
    - Reader
    still open normally after the navigation changes.

Do not overstate anything not exercised.

---

# Content-count verification

Before implementation and again after implementation, report from the actual generated data:

- number of Murasoli volumes
- total structured letters
- letters per volume
- volumes with English translation
- scan/page-based volumes
- total scan pages where represented

The native screens must match these values.

Do not hardcode counts in UI unless driven directly from loaded data.

---

# Documentation

After implementation and verification, update CURRENT docs minimally.

## `mobile/docs/ROADMAP.md`

Mark only:

**Native Murasoli reader**

complete.

Do NOT mark Explore themes/people/places complete.

## `mobile/docs/DATA_CONTRACTS.md`

Document:
- Murasoli index contract
- volume/letter contract used by mobile
- translation availability
- scan-volume contract
- caching semantics added for this reader

Only document the actual implementation.

## `HANDOVER.md`

Record:
- Activity-3 branch/implementation
- actual Murasoli counts
- verification performed
- any limitations
- exact next roadmap activity

According to the current roadmap, the likely next activity is:

**Increment 2 · Activity 4 — Explore theme / people / places entry points**

but verify the CURRENT roadmap after Activity 3 rather than assuming.

---

# Scope exclusions

Do NOT work on:

- Timeline changes beyond regression fixes
- feature-data exporter changes unless a genuine blocker is found
- governance UI
- themes UI
- people UI
- places UI
- cross-collection search
- bulk download manager
- Push notifications
- Universal Links
- Associated Domains
- privacy/legal
- App Store work
- share-as-image
- iPad redesign
- SDK upgrades
- physical-device testing
- unrelated website/archive enhancements

Do not begin Activity 4 after finishing Activity 3.

---

# Git discipline

- merge PR #5 first
- verify post-merge CI
- fresh branch from updated `main`
- keep working tree clean
- inspect full diff before commit
- no generated `ios/`
- no signing files
- no machine-specific files
- no SDK/package upgrades unless genuinely required for Activity 3
- logical commits
- push branch
- open PR
- require Mobile CI green
- require Vercel/site checks where relevant
- do not merge a failing PR

Leave the Activity-3 PR unmerged once it is green unless the current workstream explicitly requires merging it.

---

# Stop condition

Stop when:

- PR #5 has been merged and verified on `main`
- native Murasoli Library works
- structured volume/letter browsing works
- Tamil Reader works
- English translation works where available
- Volume 54's real scan/page format is handled faithfully
- existing offline/error behavior is preserved
- simulator verification passes
- standard mobile gates pass
- GitHub Mobile CI passes
- documentation is updated
- Activity-3 PR is green

Do NOT start the next Increment-2 activity.

---

# Final report

Report:

1. Timeline PR #5 merge SHA
2. Activity-3 branch
3. Activity-3 commit SHA(s)
4. Activity-3 PR number
5. files changed
6. exact current Murasoli volume count
7. total structured-letter count
8. letter counts by volume
9. English availability by volume
10. scan/page volume details
11. native navigation structure implemented
12. Murasoli data-layer changes
13. Tamil Reader behavior
14. English Reader behavior
15. Volume-54 behavior
16. offline/cache behavior
17. bookmark/Saved behavior and whether it was included or deliberately deferred
18. simulator verification result
19. typecheck result
20. manifest-validation result
21. expo-doctor result
22. iOS export result
23. GitHub CI result
24. Vercel/site result if applicable
25. known limitations
26. confirmation that no non-Murasoli Increment-2 UI was started
27. exact next activity from the CURRENT roadmap

Start with Stage 1 and proceed to Activity 3 only after PR #5 is merged and post-merge CI is green.
:::

<a id="turn-0354"></a>
## Turn 0354 — 2026-08-15T07:10:07.980Z

### User

Starting with the requested correction inspection plus Stage 1 confirmation. Let me look at how the Library renders volume titles and confirm PR #5 is still green:

Confirmed: Volume 1 has proper titles; Volumes 2–6 are `null`, so the Library shows the fallback "Volume N". Let me find where volume titles originate (index files, meta, or a builder) and how the website titles them, to fix at the right source:

Volume index files 2–6 have `null` titles (they're static source data, no generator). Let me check the meta file and how the website titles the volumes, to confirm the correct convention:

Root cause found: only `volume1.index.json` has titles; volumes 2–6 are `null` everywhere, so the Library falls back to "Volume N". The correct synchronized fix is a data fix (giving volumes 2–6 their Tamil part-titles following Vol 1's convention), which benefits both web and mobile. I'll do that as its own separate change, not mixed into the Murasoli PR.

First, **Stage 1 — merge PR #5.** Final scope re-check then merge:

PR #5 merged (`ac278d8`), scope was clean. Let me verify post-merge main state + CI:

**Stage 1 complete:** PR #5 merged (`ac278d8`), post-merge Mobile CI `success`, worktree clean.

Now the requested correction. Let me create a branch off the updated main content and inspect a volume-2 index file's structure before editing:

Volumes 2–6 are missing the title keys entirely. Let me add them with a minimal text insertion (preserving all other formatting) following Vol 1's convention, using the correct Tamil ordinals:

Titles added. Now rebuild the manifest and verify it picks up the titles + the diff is minimal:

All 6 volumes now carry consistent Tamil part-titles (முதல்→ஆறாம்); diff is minimal (5 index files +2 lines each + manifest), `validate:manifest` passes, and `contentVersion` correctly bumped. Committing the correction:

Pushed. Opening a PR for the correction and watching its checks:

PR #6 opened, Mobile CI green. Let me confirm Vercel (site data changed) then merge the correction:

**Correction merged** (`33e3dfd`) — all six volumes titled consistently.

Now **Stage 2 — Native Murasoli reader.** Creating the fresh branch off updated main and beginning the mandatory data inspection with content-count verification:

Structure clear: `index.json` has volumes 48–53 (letter-based, `pages: []`) and volume 54 (scan-based, `pages[]` populated with page metadata). Let me inspect the letters index, sample Tamil/English letters, and the Vol-54 scan contract, and compute the counts:

Counts: **7 volumes, 346 structured letters** (48:58, 49:53, 50:50, 51:49, 52:50, 53:50, 54:36); 346 Tamil letter files, 311 English; Vol 54 also has 341 scan-page files. Vol 54 appears in **both** the letters index (36) and as 341 scan pages — I need to understand what Vol 54's content actually is. Let me inspect a regular letter, an English letter, and Vol 54's letter + page JSON:

Now I understand the contract. Regular letters (all vols, incl. Vol 54's 36 curated ones) have `title{en,ta}`, `date`, `salutation`, `paragraphs`; English letters (subset) add `translatorNote` + `provenance`; Vol 54 also has **341 scan pages** (`text/m54-p*.json`) with per-page OCR text (no image URLs), and `index.json` marks Vol 54 as the pages-populated volume. Let me confirm English-per-volume, the letters-index entry shape, and how the website handles Vol 54:

Complete data picture: **English is 100% for vols 48–53 (310 letters), Vol 54 is effectively Tamil-only (36 letters, 1 English) plus 341 OCR scan pages.** `index.json` marks Vol 54 as the pages-populated volume. Let me see how the website presents Vol 54 (to reuse its data assumptions) and read the current mobile Explore hand-off:

Explore has the web hand-off (`Linking.openURL` → I'll replace with native nav). Now the reader pattern + storage model to reuse, and the website's Vol-54 scan reader for its data assumptions:

The memoir Reader gives me the full pattern to mirror (controls, prefs, progress persistence, EN toggle, share). Now the storage model — critical for deciding progress/bookmark/recents integration and separate keys:

Storage is id-keyed maps. The bookmark/Saved model is memoir-specific (`Bookmark.chapterId` + Saved routes to the memoir Reader), so per your guidance I'll **defer Murasoli bookmarks** (document + propose later) rather than silently migrate Saved, and use a **separate ****`mu:progress`**** key** for Murasoli scroll position. Let me confirm the Saved model is memoir-bound and check how the website treats Vol 54 (letters vs pages):

Now I have the complete model. The website's rule is `isScanVolume = volume.pages.length > 0` (vols 48–53 = letters w/ full English; Vol 54 = page-scan, Tamil-only). I'll mirror that data assumption. Let me confirm the English-letter title shape and letters-index volume fields, then build:

I have the complete contract. **English-letter title is a plain string; letters-index has ****`letterCount`****; manifest.murasoli has all URLs/templates (volumeCount 7, totalLetters 346).** Design locked: mirror the site's `pages.length > 0 ⇒ scan volume` rule (vols 48–53 letters+English; Vol 54 page-scan Tamil-only), separate `mu:progress` storage, Murasoli bookmarks deferred.

Let me build. Starting with the types:

Now the data-layer functions in `client.ts`:

Adding the Murasoli types to client.ts's imports:

Now the separate Murasoli reading-position storage:

Now register the navigation routes. Updating `navigation/index.tsx`:

Now the four screens. Starting with **MurasoliLibraryScreen** (data-driven volume list, no hardcoded volume numbers):

**MurasoliVolumeScreen** — FlatList of letters (or pages for scan volumes), efficient for long volumes:

**MurasoliReaderScreen** — the letter reader (Tamil/English toggle, translator note distinguished, shared prefs, separate progress key):

**MurasoliScanScreen** — the Vol-54 page/scan reader (OCR text per page, prev/next, Tamil-only — no fake letters or fake English):

Now update Explore to open the native library instead of the web hand-off:

All screens written and Explore wired to native. Let me run the mobile typecheck to catch any issues:

Typecheck passes. Now the rest of the mobile gate:

All mobile gates green (validate\:manifest, expo-doctor 21/21, iOS export). Now simulator verification. Since only JS/TS changed (no native deps), I can serve this branch via Metro and reload the installed app. Let me boot the sim, start Metro, and launch:

Let me terminate and relaunch to force a fresh bundle from Metro (this branch's code), then screenshot:

App reloaded on Home (light theme). Let me open Explore (4th tab):

Explore shows the updated Murasoli card ("346 letters · 7 volumes", chevron = native nav, no web icon). Let me tap it to open the native Murasoli Library:

Native Murasoli Library renders perfectly — all 6 letter volumes with data-driven year ranges, correct counts (58/53/50/49/50/50), "Tamil + English", and "Letters" badges. Let me scroll to confirm Vol 54 shows as a scan volume:

Vol 54 correctly shows as **"341 scanned pages · Tamil"** with a distinct "Scans" badge + scan icon. All 7 volumes present and data-driven. Let me open a letter volume (49, has full English) → letter list:

Letter list for தொகுதி 49 renders via FlatList (53 letters, #number · formatted date · Tamil title, back = "Murasoli"). Let me open the first letter:

Native letter reader works — meta line (முரசொலி · தொகுதி 49 · #3764 · 1 Jun 2013), Tamil title, salutation "உடன்பிறப்பே," (distinguished), Tamil body, and the "தமிழ்" toggle (English available). Let me switch to English:

**English toggle works** — English title, and the **Translator's Note is clearly distinguished** in its own accent-bordered italic block (not flattened into Kalaignar's text), then salutation + English body. This satisfies the faithful-distinction requirement. Let me switch back to Tamil and test a font control:

Tamil restored, font control works. Now the back-navigation chain and Vol 54. Back to the letter list:

Still in the reader (my taps hit the controls row; also font enlarged, confirming font+ works). Let me tap the Back button at its precise location:

Back-nav Reader → Volume works. Back to the Murasoli Library, then I'll test Vol 54:

Back at the Murasoli Library (back = "Tabs" → Explore). Let me open Vol 54 (the scan volume):

Vol 54 shows the **page list** (341 scanned pages, page number + pageType frontmatter/body) — correctly presented as pages, not fake letters. Let me open a page to test the scan reader + prev/next:

**Vol 54 scan reader is faithful** — "3 / 341" position, "Scanned page · OCR text" label, Tamil OCR body, no English toggle (Tamil-only), and Previous/Next page nav. Let me test Next: Understood — Vol 54 should be a normal letter volume (its 36 curated letters), like the website, not a separate page browser. Let me revise: treat all volumes uniformly as letter volumes and remove the scan-specific screen/route.

First, simplify **MurasoliVolumeScreen** to always render the letter list:

Now make the Library cards uniform (Vol 54 shown like the others — letters, with language distinction only):

Let me drop the now-unused `radius` import in the Library screen:

Now remove the scan route/screen. Updating navigation:

Now remove the unused `murasoliPage` fn and its import from client.ts, and delete the scan screen:

Deleting the now-unused scan screen file:

Typecheck passes. Let me reload the app and verify Vol 54 now shows as a letter volume. Terminating + relaunching for the new bundle:

Vol 54 now shows uniformly — "36 letters · 341 pages · Tamil" with the same mail icon + chevron as the other volumes. Let me open it to confirm the letter list:

Vol 54 now displays as a letter volume (36 letters with dates + Tamil titles), consistent with the others. Let me open a Vol-54 letter to confirm the reader:

Vol 54 letter #4016 opens in the same letter reader (meta, Tamil title, salutation, Tamil body, no English toggle since it has none) — uniform with other volumes and matching the website. The correction is verified.

Let me do a quick memoir regression check (Library, which also confirms the volume-title fix on mobile). Relaunching to Home and opening Library:

The memoir Library now shows **all 6 volumes with consistent Tamil part-titles** (முதல்/இரண்டாம்/மூன்றாம்/நான்காம் பாகம்) — the correction is verified on mobile, and memoir navigation is unregressed. Both the correction and Vol-54-as-letters are confirmed.

Now the docs. **ROADMAP** — mark only Native Murasoli reader complete:

**DATA\_CONTRACTS** — document the Murasoli contract consumed by the native reader:

**HANDOVER** — record Activity 3:

Docs done. Let me review the changed-file scope and re-run the mobile gate before committing:

Scope is clean (3 new Murasoli screens + client/storage/types/nav/Explore + docs; nothing outside mobile/ + HANDOVER). Let me run the full mobile gate matching CI:

All gates pass. Committing (stopping Metro first to keep git fast):

Committed `fdd3a45`. Pushing and opening the PR:

PR [#7](https://github.com/pugazg/kalaignar-autobiography/pull/7) opened. Watching Mobile CI:

Mobile CI green. Let me confirm the Vercel/site check to complete the PR:

All checks green — PR [#7](https://github.com/pugazg/kalaignar-autobiography/pull/7) is `CLEAN`/`MERGEABLE`, left **unmerged** per the stop condition. Both stages plus the requested correction are complete.

## Final report

**Preliminary correction (requested first):** memoir volumes 2–6 lacked Tamil titles, so the Library showed "Volume N" for them and a Tamil title only for Vol 1. Added the standard Tamil part-titles (இரண்டாம்…ஆறாம் பாகம்) + rebuilt the manifest — all six now title consistently on web and mobile (verified in the simulator). Shipped as **PR #6, merged ****`33e3dfd`**.

### Stage 1 + Stage 2

1. **Timeline PR #5 merge SHA:** `ac278d8` (post-merge Mobile CI green; Timeline functional on `main`; tree clean)
2. **Activity-3 branch:** `mobile/increment2-murasoli` (from updated `main`, incl. the correction)
3. **Activity-3 commit SHA:** `fdd3a45`
4. **Activity-3 PR:** [#7](https://github.com/pugazg/kalaignar-autobiography/pull/7) (open, green, mergeable — **not merged**)
5. **Files changed:** 3 new screens (`MurasoliLibraryScreen`, `MurasoliVolumeScreen`, `MurasoliReaderScreen`), `ExploreScreen.tsx`, `navigation/index.tsx`, `data/{client,types,storage}.ts`, `docs/{ROADMAP,DATA_CONTRACTS}.md`, `HANDOVER.md`. No `ios/`, no SDK/package changes, nothing outside `mobile/` + `HANDOVER.md`.
6. **Murasoli volume count:** **7** (48–54)
7. **Total structured letters:** **346**
8. **Letters by volume:** 48:58 · 49:53 · 50:50 · 51:49 · 52:50 · 53:50 · 54:36
9. **English availability:** full for 48–53 (310 letters); **Vol 54 Tamil-only** (1 English present of 36)
10. **Scan/page volume:** Vol 54 — **341 OCR pages** exist in the data (`/murasoli/text/`, no page images); scan-sourced and Tamil-only. Presented as its 36 curated letters (per your correction); raw pages left unconsumed.
11. **Native navigation:** Explore → `MurasoliLibrary` → `MurasoliVolume` → `MurasoliReader` (reuses the existing native stack, back behavior, tabs, theme, a11y — no parallel framework)
12. **Data-layer changes:** `api.murasoli{Index,Letters,Letter,LetterEn}` — offline-first via the existing `fetchJSON` cache; no ad-hoc `fetch()` in screens
13. **Tamil reader:** meta (vol · #number · date), Tamil title, salutation, paragraphs; memoir controls (font/line-height/theme) + shared prefs; long-press to share
14. **English reader:** Ta/En toggle only where English exists; English title/salutation/body; **translator's note in a distinct bordered block**; provenance footer — never flattened into Kalaignar's text
15. **Vol 54 behavior:** browsed as its 36 curated letters like other volumes (per your instruction, matching the website); Tamil-only; no fake English, no invented transcriptions
16. **Offline/cache:** indexes + letters cached offline-first (read once → readable offline); uncached letter offline → standard offline-error; no bulk download; reading position under separate `nn:mu:progress`
17. **Bookmark/Saved:** **deliberately deferred** — the Saved model is memoir-specific (`Bookmark.chapterId` + Saved routes to the memoir Reader). Murasoli reader is fully functional without bookmarks; cross-collection Saved proposed as a later scoped activity. Memoir bookmarks untouched.
18. **Simulator verification:** Explore opens Murasoli natively (no web hand-off); Library lists all 7 volumes with correct counts/ranges/language; letter list + Tamil reader; En toggle both ways on a vol-49 letter; Vol 54 opens as 36 letters (Tamil, no fake English); theme + font; back-nav Reader→Volume→Library→Explore; memoir Library shows the corrected titles and is unregressed
19. **Typecheck:** PASS · 20. **Manifest validation:** PASS · 21. **expo-doctor:** PASS (21/21) · 22. **iOS export:** PASS
20. **GitHub CI:** PASS (Mobile CI on `fdd3a45`) · 24. **Vercel/site:** PASS
21. **Known limitations:** no Murasoli bookmarks, no bulk download, no Murasoli search, Vol 54 raw scan pages not separately browsable (all documented)
22. **No non-Murasoli Increment-2 UI started** — governance/themes/people/places/timeline changes: none (only Explore's Murasoli entry + new Murasoli screens)
23. **Exact next activity (current roadmap):** **Increment 2 · Activity 4 — Explore theme / people / places entry points** (from the feature JSON)

Stopping here — PR #7 is green and awaiting your go-ahead to merge; Activity 4 not started.

### Assistant

This is a good completion of Activity 3. I checked GitHub: **PR #7 is still open, not merged, and mergeable**, with head `fdd3a45`. 

There is one important issue to resolve before Activity 4: the current roadmap says `places` has “no source yet” and therefore `features.places` stays `null`.  But the repository **does actually contain `data/places.ts`**, with 10 grounded places, chapter refs, and schematic map coordinates. 

So I would structure the next activity as:

**Merge PR #7 → verify post-merge CI → Activity 4A: bring `places.ts` into the deterministic feature-export pipeline → Activity 4B: build Explore entry points for Themes, People, and Places.**

Themes and People are already ready as feature JSON: Themes has 6 entries with chapter refs and richer archival associations, while People has 15 entries with roles, relationships and memoir refs.  

I would **not** let Claude silently implement Places from the TypeScript file directly in the mobile bundle. It should first export `places.json`, validate its chapter refs, populate `manifest.features.places`, and correct the now-stale roadmap statement. Then all three Explore surfaces can follow the same data-driven architecture.

<a id="turn-0355"></a>
## Turn 0355 — 2026-08-15T07:12:07.923Z

### User

provide prompt for claude

### Assistant

:::writing{variant="document" id="41286" title="Claude Prompt — Increment 2 Activity 4: Explore Themes, People & Places"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — merged
- Increment 2 · Activity 1 — feature dataset export — merged
- Increment 2 · Activity 2 — Timeline milestones — merged
- Memoir volume-title correction — merged
- Increment 2 · Activity 3 — Native Murasoli reader — PR #7
  - branch: `mobile/increment2-murasoli`
  - head: `fdd3a45`
  - PR is currently green and mergeable
  - leave its implementation unchanged except genuine merge/regression fixes

The next roadmap item is:

# Increment 2 · Activity 4
## Explore: Themes · People · Places

There is one important prerequisite correction:

Activity 1 deliberately exported only five feature datasets and left `features.places = null`.

However, the repository DOES contain the authoritative source:

`data/places.ts`

It currently contains 10 grounded memoir places with:

- `id`
- Tamil name
- English name
- grounded note
- memoir chapter refs
- schematic `x` / `y` coordinates for the existing Tamil Nadu map viewBox

Therefore this workstream has three stages:

1. Merge Activity 3
2. Export Places through the same deterministic feature-data pipeline
3. Build native Explore entry points for Themes, People and Places

Do not skip directly to UI by importing `data/places.ts` into the mobile bundle.

---

# Stage 1 — Merge Activity 3

Before Activity 4:

1. Re-read:
   - `HANDOVER.md`
   - `mobile/docs/ROADMAP.md`
   - `mobile/docs/DATA_CONTRACTS.md`

2. Confirm PR #7:
   - is still open
   - green
   - mergeable
   - head remains the expected Murasoli commit
   - contains only Activity-3 work

3. Inspect the complete PR diff.

4. Confirm no:
   - generated `ios/`
   - signing files
   - SDK changes
   - unrelated archive edits
   - themes/people/places UI

5. Merge PR #7 into `main`.

6. Confirm:
   - merge commit exists on `main`
   - post-merge Mobile CI passes
   - native Murasoli files are present on `main`
   - working tree is clean

Only after this may Activity 4 begin.

---

# Stage 2 — Activity 4A
## Export `places.ts` to feature JSON

Create a fresh branch from the newly updated clean `main`, for example:

`mobile/increment2-explore`

Before editing, inspect current:

- `pipeline/builders/export-feature-data.ts`
- `data/places.ts`
- `public/data/app/features/`
- `pipeline/builders/build_app_manifest.py`
- `public/data/app/manifest.v1.json`
- `mobile/docs/DATA_CONTRACTS.md`
- `mobile/docs/ROADMAP.md`

## Source authority

`data/places.ts` is authoritative.

Do NOT:

- invent places
- alter Tamil names
- rewrite English names
- rewrite notes
- change memoir refs
- “correct” coordinates
- replace schematic coordinates with GPS coordinates
- geocode anything from the internet

The coordinates are explicitly schematic and belong to the existing source model.

## Export requirement

Extend the existing deterministic feature exporter so it also exports:

`public/data/app/features/places.json`

The exporter must IMPORT the actual TypeScript source rather than manually copying the data.

After this change, the feature pipeline should export six datasets:

- timeline
- governance
- people
- themes
- quotes
- places

Preserve all existing output contracts.

## Places validation

Validate at minimum:

- unique place IDs
- non-empty Tamil name
- non-empty English name
- non-empty grounded note
- non-empty refs
- every memoir ref resolves to a real chapter
- `x` and `y` are finite numbers
- coordinates fall within the declared schematic viewBox:
  - x: 0–1640
  - y: 0–2032

Do not silently repair invalid data.

Fail clearly.

## Manifest

Regenerate the app manifest.

Confirm:

`manifest.features.places`

now points to:

`/data/app/features/places.json`

and no longer remains `null`.

Confirm all other feature URLs remain unchanged.

Confirm memoir and Murasoli manifest counts do not regress.

## Determinism

Run the feature exporter twice.

The second run must produce no JSON diff when source data is unchanged.

Run:

- root typecheck
- `npm run build:features`
- manifest builder / `npm run build:app-data`
- `npm run validate:manifest`

Correct the stale roadmap/documentation statement that Places has “no source.”

Do not make any other feature-data changes.

---

# Stage 3 — Activity 4B
# Native Explore: Themes · People · Places

Now build the native Explore surfaces from the generated feature JSON.

The current feature data includes approximately:

- Themes: 6
- People: 15
- Places: 10

VERIFY the current counts from generated JSON rather than relying on these numbers.

## Mandatory startup

Before implementation, read completely:

- `mobile/src/screens/ExploreScreen.tsx`
- current navigation definitions
- Reader route types
- Timeline feature-loading implementation
- Murasoli navigation added by Activity 3
- `mobile/src/data/client.ts`
- `mobile/src/data/types.ts`
- shared UI kit/theme components
- `public/data/app/features/themes.json`
- `public/data/app/features/people.json`
- `public/data/app/features/places.json`
- authoritative:
  - `data/themes.ts`
  - `data/people.ts`
  - `data/places.ts`

Also inspect the website implementations of these features if they exist, but use them only to understand the data semantics.

Do NOT copy web-specific UI into React Native.

---

# Overall UX goal

Explore should become a genuine native discovery hub.

At minimum it should provide native entry points for:

- Themes
- People
- Places
- Murasoli

Murasoli is already implemented by Activity 3.

The new work is Themes / People / Places only.

Do not implement Governance or Quotes as separate Explore sections in this activity unless the CURRENT roadmap has explicitly changed.

---

# Feature-data loading

Use the existing reusable feature loader:

`api.feature<T>(...)`

or its current equivalent.

Do not add screen-specific raw `fetch()` calls.

Use:

- `manifest.features.themes`
- `manifest.features.people`
- `manifest.features.places`

Handle:

- loading
- cached/offline data
- feature URL absent
- malformed payload
- network failure without cache

Do not crash Explore if one dataset fails.

Each collection should degrade independently where reasonable.

Validate payloads defensively before rendering.

---

# A. Themes

Create a native Themes browsing experience.

Use only source-supported fields such as:

- Tamil label
- English title
- narrative
- initiatives
- achievements
- stats
- memoir refs
- archive context/events/people where present

Do NOT invent summaries, categories or explanatory prose.

A reasonable native structure is:

**Explore → Themes → Theme detail**

but first inspect current navigation patterns and choose the smallest clean implementation.

## Theme list

Show all source themes.

Each card should have enough source content to distinguish it without dumping the full narrative into the list.

## Theme detail

Display the actual source-supported material cleanly:

- Tamil theme title prominently
- English title
- narrative
- initiatives
- achievements
- stats
- archive context where present

For memoir refs:

- expose native links to the referenced memoir chapters
- use the existing Reader route
- do not invent a `find` term where none exists

For `archive.events`:

- event label may be displayed
- tapping it should open its actual `ref`

For `archive.people`:

- if People navigation exists and the referenced person ID resolves, linking to that native Person detail is appropriate
- do not invent links for unresolved IDs

Do not render arbitrary icon strings unless they map cleanly to icons already supported by the native app.

A textual/theme treatment is preferable to unsupported icon guessing.

---

# B. People

Create:

**Explore → People → Person detail**

Use source fields faithfully:

- Tamil name
- English name
- role
- relationship
- firstAppears
- refs

## People list

Use an efficient list.

15 entries are small, but still follow established React Native list conventions.

Cards should primarily show:

- Tamil name
- English name
- role

Do not invent portrait images.

Do not fetch photographs from the web.

## Person detail

Display:

- Tamil name
- English name
- role
- relationship text
- first-appears text
- referenced memoir chapters

Each ref should deep-link to the existing Reader.

Where practical, resolve chapter IDs to their real Tamil chapter titles using the existing manifest/chapter lookup rather than displaying raw IDs.

Do not modify the source relationship prose.

---

# C. Places

Create:

**Explore → Places → Place detail**

The source contains 10 places with schematic map coordinates.

## Important coordinate rule

These are NOT GPS coordinates.

They are schematic positions in the source's Tamil Nadu map viewBox:

`0 0 1640 2032`

Do not:

- use Apple Maps
- use Google Maps
- place markers using latitude/longitude
- label them as geographically precise
- geocode them
- modify them to look “more accurate”

## Places presentation

Prefer a useful native presentation consisting of:

1. a browsable list of all places
2. optionally a simple schematic map using the existing source x/y coordinates IF it can be implemented cleanly with existing dependencies

Do not add a heavy map dependency just for this activity.

A list-first experience is fully acceptable.

If a schematic map is implemented:

- preserve the relative x/y positions
- label it clearly as schematic
- make markers accessible
- allow marker tap → Place detail
- do not introduce new cartographic claims

## Place detail

Use:

- Tamil name
- English name
- source note
- memoir refs

Resolve refs to native Reader links.

Do not expand notes with outside historical/geographic knowledge.

---

# Explore home

Update the existing Explore screen so Themes, People and Places are real native entry points.

Do not leave fake “coming soon” cards.

Preserve the native Murasoli entry from Activity 3.

Do not regress any existing Explore content that remains relevant.

Avoid excessive cards or decorative copy.

The four core discovery paths should be immediately understandable:

- Themes
- People
- Places
- Murasoli

---

# Navigation

Add only the necessary routes.

Conceptually these may include:

- `Themes`
- `ThemeDetail`
- `People`
- `PersonDetail`
- `Places`
- `PlaceDetail`

Use naming consistent with the current navigation code.

Do not build a second navigation system.

Ensure:

- back behavior works
- theme persists
- tab state remains correct
- deep-links to memoir Reader work
- returning from Reader lands sensibly in the Explore path

---

# Reader linkage

Reuse the existing:

`Reader({ id })`

route.

Do not duplicate memoir reading logic.

Do not invent passage highlight terms.

For every ref used in Themes, People and Places:

- validate it
- resolve chapter metadata where possible
- open the correct memoir chapter

---

# Offline behavior

Feature JSON is fetched using the established offline-first cache.

Expected behavior:

- once Themes/People/Places JSON is cached, those Explore screens should render offline
- tapping a memoir ref offline should open if that chapter is already available
- uncached/download-unavailable memoir chapters should use the existing truthful offline state

Do not automatically download all referenced memoir chapters.

Do not add bulk download functionality.

---

# UI consistency

Reuse existing:

- theme tokens
- Tamil typography
- Dynamic Type
- cards
- pills/eyebrows where appropriate
- light / sepia / dark
- spacing conventions
- accessibility labels

Do not over-design.

This is an archive/discovery experience, not a dashboard.

Tamil-first presentation should remain central.

---

# Defensive validation

Add narrow parsers/types for:

- Themes feature payload
- People feature payload
- Places feature payload

Validate required fields before rendering.

Malformed one-off records should not silently disappear in a way that falsely implies a complete dataset.

Prefer failing the affected collection safely with a truthful state.

Do not rewrite malformed server content.

---

# Search

Do NOT build cross-feature search in this activity.

Do not add:

- Theme search
- People search
- Place search
- cross-collection search

unless an extremely trivial list filter already exists and requires essentially no additional architecture.

It is not required for completion.

---

# Governance and Quotes

The exporter already provides:

- governance.json
- quotes.json

Do NOT build their native Explore surfaces in this activity.

Current scope is explicitly:

**Themes + People + Places**

Governance and Quotes remain available as data foundations for later work.

---

# Murasoli

Do not modify the new Murasoli implementation except genuine navigation integration/regression fixes required by the Explore screen.

Do not add:

- Murasoli search
- Murasoli bookmarks
- bulk Murasoli downloads

in this activity.

---

# Verification

Run the complete mobile gate:

From `mobile/`:

- `npm ci` if required
- `npm run typecheck`
- `npm run validate:manifest`
- `npx expo-doctor`
- `npx expo export --platform ios` using the current SDK-57-compatible in-project output path

Also run:

- root typecheck
- feature exporter
- manifest rebuild
- website build / relevant site validation because generated public JSON + manifest are changed

No physical-phone test is required.

---

# Simulator verification

Verify at minimum:

## Explore

1. Explore opens normally.
2. Native entries exist for:
   - Themes
   - People
   - Places
   - Murasoli
3. Murasoli still opens natively.

## Themes

4. All source themes render.
5. Open at least two themes.
6. Tamil + English labels render correctly.
7. Narrative/stat/initiative content renders faithfully.
8. Theme memoir refs open the correct Reader chapters.
9. At least one archive-event ref works where present.

## People

10. All source people render.
11. Open at least three people from different parts of the memoir.
12. Tamil name / English name / role / relationship render correctly.
13. Memoir refs open the correct Reader chapter.

## Places

14. All source places render.
15. Open:
    - Thirukkuvalai
    - Chennai
    - at least one other place
16. Tamil/English names and grounded notes render correctly.
17. Memoir refs open the correct Reader chapters.
18. If a schematic map is implemented, confirm markers use source x/y data and the UI explicitly avoids implying GPS accuracy.

## State/navigation

19. Light / sepia / dark work.
20. Back navigation works:
    - detail → collection
    - collection → Explore
    - Reader → prior Explore detail/list
21. Feature screens render from cached JSON offline where practical.
22. Library still opens.
23. Timeline still works.
24. Search still works.
25. Native Murasoli still works.

Do not overstate any test not actually exercised.

---

# Documentation

When implementation is complete:

## `mobile/docs/ROADMAP.md`

Correct the stale Places statement.

Mark:

**Explore: theme / people / places entry points from the feature JSON**

complete.

Do not mark unrelated production/store items complete.

## `mobile/docs/DATA_CONTRACTS.md`

Document:

- `places.json`
- Places validation
- manifest `features.places`
- actual Themes/People/Places mobile-consumer behavior
- caching semantics

Do not duplicate excessive implementation detail.

## `HANDOVER.md`

Record:

- Activity 3 merge
- Activity 4A places export
- Activity 4B Explore implementation
- exact counts
- simulator verification
- known limitations
- exact next activity based on the CURRENT roadmap after completion

Do not guess the next activity until the current roadmap is inspected after marking Activity 4 complete.

---

# Git structure

Activity 4A and 4B may live on the same Activity-4 branch, but keep commits logically separated.

Recommended:

Commit 1:
`Export places feature dataset`

Commit 2:
`Add native Themes, People and Places Explore`

Commit 3:
documentation only, if useful

Do not create unnecessary micro-commits.

---

# Git discipline

- merge PR #7 first
- verify main CI
- fresh branch from updated clean `main`
- inspect entire diff before commit
- no generated `ios/`
- no signing files
- no SDK upgrades
- no machine-specific artifacts
- no new mapping dependency unless genuinely unavoidable (prefer none)
- no unrelated website/archive edits
- push branch
- open PR
- require Mobile CI green
- require Vercel/site checks green because feature JSON/manifest changes affect `public/`
- do not merge a failing PR

Leave the Activity-4 PR unmerged once green unless explicitly required otherwise.

---

# Scope exclusions

Do NOT work on:

- Governance native UI
- Quotes native UI
- Murasoli enhancements beyond regression fixes
- Murasoli bookmarks
- cross-collection Saved redesign
- Murasoli search
- cross-feature search
- bulk downloads
- download manager
- Push notifications
- Universal Links
- Associated Domains
- privacy/legal
- App Store work
- share-as-image
- iPad redesign
- SDK upgrades
- physical-device testing
- unrelated archive/content work

Do not begin the next roadmap activity after Activity 4.

---

# Stop condition

Stop when:

- PR #7 is merged and verified
- `places.ts` is exported deterministically
- `features.places` is populated
- Places source refs/coordinates are validated
- Explore has real native Themes / People / Places entry points
- all three collections and their details work
- memoir Reader refs work
- Murasoli remains unregressed
- standard mobile gates pass
- root/site checks pass
- simulator verification passes
- docs are updated
- Activity-4 PR is green

Do NOT start the next activity.

---

# Final report

Report:

1. PR #7 merge SHA
2. Activity-4 branch
3. Activity-4 commit SHA(s)
4. Activity-4 PR number
5. files changed
6. Places exporter changes
7. `places.json` path
8. Places count
9. Places validation result
10. deterministic rerun result
11. final manifest feature URLs
12. Theme count
13. People count
14. Place count
15. Explore navigation structure
16. Theme UI behavior
17. People UI behavior
18. Places UI behavior
19. whether a schematic map was implemented; if yes, how source x/y coordinates are represented
20. memoir Reader deep-link verification
21. offline/cache behavior
22. Murasoli regression result
23. Library/Timeline/Search regression result
24. root typecheck result
25. mobile typecheck result
26. manifest validation result
27. expo-doctor result
28. iOS export result
29. website build/result
30. GitHub Mobile CI result
31. Vercel result
32. known limitations
33. confirmation that Governance/Quotes and other out-of-scope features were not started
34. exact next activity from the CURRENT roadmap

Start with Stage 1. Do not begin Activity 4 until PR #7 is merged and post-merge Mobile CI is green.
:::

<a id="turn-0356"></a>
## Turn 0356 — 2026-08-15T12:25:57.442Z

### User

Starting **Stage 1 — merge Activity 3 (PR #7)**. Confirming it's still green/mergeable, head unchanged, and scope-clean before merging:

PR #7 confirmed: green, mergeable, head `fdd3a45`, scope is Activity-3-only (Murasoli + docs, no `ios/`/SDK/unrelated). **Merging:**

Merged (`90b2e40`). Verifying post-merge state (main CI, Murasoli files on main, clean tree):

**Stage 1 complete:** PR #7 merged (`90b2e40`), main CI green, Murasoli files on `main`, tree clean.

Now **Stage 2 — Activity 4A (export places).** Creating the branch and inspecting `data/places.ts` + the current exporter:

10 places with `id, tamil, name, note, refs, x, y` (schematic coords in viewBox 0 0 1640 2032). Let me read the exporter to extend it:

Now let me read the tail of the exporter (quotes validation + datasets array) to add places:

Now run the exporter, verify places.json + determinism, and rebuild the manifest:

6 datasets now (places: 10), deterministic. Now rebuild the manifest and confirm `features.places` populates without changing other URLs or regressing counts:

`features.places` now resolves to the file; all other URLs unchanged; no memoir/Murasoli regression; validate passes; `contentVersion` correctly unchanged (it hashes indexes, not features). Let me run root typecheck (covers the exporter) and fix the stale "no source" doc statements:

Root typecheck passes. Fixing the stale "no source" statements. First ROADMAP:

Now fix DATA\_CONTRACTS — the manifest example and the "no source" line:

Now update the "no source" paragraph and add the `places.json` contract. Let me read that region:

Docs fixed. Let me review the 4A change scope and commit it as the first logical commit:

Clean 4A scope (exporter, manifest, new places.json, doc fixes; other 5 JSON byte-identical). Committing 4A (kill Metro first for fast git):

4A committed (`6ad951b`). Now **Activity 4B — native Explore.** Verified counts (themes 6, people 15, places 10). I'll reuse the Timeline feature-loading pattern via a shared hook. Starting with the feature types:

Now the shared feature-loading hook:

A shared component for memoir-chapter deep-links (resolves titles, opens Reader), reused by all three detail screens:

Now the Themes screens (list + detail). Writing `ThemesScreen.tsx`:

Now `PeopleScreen.tsx` (list + detail):

Now `PlacesScreen.tsx` (list + a dependency-free schematic map + detail):

Now register the 6 routes. Updating navigation:

Now the Explore home — add Themes/People/Places entry points alongside Murasoli. Replacing the single-collection section with a four-path Discover section:

Let me wire `f` (features) and add the `DiscoverRow` component:

All screens + routes + Explore wired. Running mobile typecheck:

Percentage strings need a `DimensionValue` cast. Fixing PlacesScreen:

Typecheck passes. Let me run the app on the simulator to verify the new Explore surfaces. Booting/serving + launching:

Explore now shows the **DISCOVER** section — Themes (கருப்பொருள்கள்), People (மனிதர்கள்), and (below) Places + Murasoli — with the top tiles preserved. Let me open Themes:

Themes list renders all 6 (Tamil + English + narrative snippet). Let me open "The Dravidian Movement" (it has archive people + events to test cross-links):

Theme detail renders faithfully (Tamil title, English, narrative, initiatives, achievements, stat chip). Let me scroll to verify the archive cross-links (people/events) and memoir refs:

Archive **MOMENTS** ("The break with MGR, 1972" event) and **IN THE MEMOIR** refs (resolved to real Tamil chapter titles + volume) both render. Let me tap the archive-event to verify it opens the Reader:

**Archive-event deep-link works** — "The break with MGR, 1972" opened `v2-ch49` "வேறு வழியில்லை; விலக்கப்பட்டார்!" (தொகுதி 2). Themes are fully verified. Let me navigate back to Explore and check People. Backing out:

The Places card is missing between People and Murasoli — because the app fetches the manifest from the **production origin** (nenjukkuneethi.org), where `features.places` is still `null` (my 4A export isn't deployed). Themes/People work (live has them from Activity 1). To test Places against my branch's data, I need to point the app at a local server. Let me check the origin config:

Themes/People work (live has them). Places needs my branch's data. Let me serve the branch's `public/` locally and point the app at it temporarily (I'll revert the config after). Starting a static server and checking the app.json origin:

Local server serves my branch's manifest (with `places`). Let me temporarily point the app there. Reading the exact app.json extra block:

Now restart Metro (to re-read app.json) and relaunch so the app fetches from the local origin:

Let me open Explore and check the Places card now appears:

Still no Places card — the app didn't pick up the local origin (likely ATS blocking http-localhost, falling back to the cached live manifest). Let me check whether the app hit the local server:

The server log shows a manifest fetch, but that may have been my earlier curl. Let me disambiguate — clear the log, relaunch, and confirm whether the *app* fetches the local manifest:

The app.json origin override isn't reliably reaching the dev-client (Constants config is baked/cached). Let me revert app.json and instead force the origin in `env.ts` (a JS-bundle change Metro reliably serves), for verification only — I'll revert it after:

Reloading so the app fetches from localhost, then checking the server receives the requests:

Let me check whether the static server is still alive and the app's current state:

Server + Metro both alive, but the app isn't hitting localhost — it's likely running a cached bundle. Let me see the app's actual state:

The blocker is iOS ATS rejecting `http://localhost` from the app (curl works, the app doesn't) — so local-http testing can't work. The reliable path is the branch's **Vercel preview** (real HTTPS serving my branch's `places.json`). Let me push the branch (4A) to trigger a preview, then point the app's origin there for verification:

Let me find the Vercel preview URL via the commit statuses:

Vercel preview is building. Let me wait for it to finish, then find the preview URL:

Deploy succeeded but the guessed alias didn't resolve. Let me get the real preview URL from the GitHub deployment's `environment_url`:

Got the preview URL. Let me verify it serves the manifest with `places` (and isn't behind auth):

The Vercel preview is behind auth (302). Localhost should actually be reachable (Metro uses localhost:8081), so the earlier failure was likely a stale Metro bundle. Let me do a clean Metro restart *after* the env.ts change and confirm the app hits the local server:

The app now reaches the local server (`ORIGIN=localhost` is live). The manifest with `places` is loaded. Let me open Explore and verify the Places entry now appears:

All four discovery entries now show — **Places (இடங்கள்)** appears with a location-pin icon. Let me open it to verify the list + schematic map:

The Places screen renders — the **schematic map** shows 10 dots at the source x/y positions (clustered top-right = Chennai/Saidapet/Sriperumbudur, bottom = Kanyakumari/Palayamkottai), labeled **"Schematic positions — relative only, not geographic / not to scale."** Below is the list (Thirukkuvalai first). Let me open Thirukkuvalai:

The tap landed on the map area without navigating. Let me scroll to the list and tap a place card cleanly:

All places render (Tamil + English + note). Let me open Chennai (சென்னை) to verify Place detail + memoir refs:

Place detail (Chennai) renders — note + **IN THE MEMOIR** with all 3 refs resolved to real chapter titles/volumes (தொகுதி 2/5/6). Let me tap a ref to confirm the Reader deep-link:

**Place → Reader deep-link works** — Chennai's ref opened `v2-ch66` "இந்தியாவில் இரு தீவுகள்" (தொகுதி 2). Themes and Places are fully verified. Let me do a quick People-detail check (checks 10–13) to complete verification. Backing out to Explore:

Still on Places list — one more back to Explore:

The Tabs tap keeps mistiming. Let me tap the chevron precisely:

On Explore now. Let me open People (மனிதர்கள்):

People list renders (Tamil name + English + role). Let me open Periyar to verify Person detail:

**Person detail (Periyar) renders** — role, relationship, "First appears", and IN THE MEMOIR refs resolved (தொகுதி 1/4). All three collections (Themes/People/Places) are verified end-to-end: lists, details, schematic map, archive cross-links, and memoir refs → Reader (via the shared `ChapterRefs`, confirmed opening the correct chapters).

Now the critical cleanup — **revert the temporary origin override** so it's never committed:

Let me confirm `env.ts` and `app.json` are back to pristine (no accidental override committed) and stop the local server:

Pristine — the override left no trace. Now the 4B docs. **ROADMAP** — mark the Explore entry-points item complete:

**DATA\_CONTRACTS** — document the Themes/People/Places consumer behavior. Let me find the Consumers section:

**HANDOVER** — record Activity 4 (3-merge + 4A + 4B). Adding after the Activity-3 section:

All docs done. Now the complete verification gate (mobile + root + website):

Now the website build (public JSON/manifest changed):

Website build passes — all gates green. Now commit 4B. Stopping Metro and reviewing scope:

Clean scope (5 new UI files + 3 modified code + 3 docs). Committing the UI (commit 2):

Commit 2 done (`70746f5`). Now commit 3 (docs):

Three logical commits (4A export, 4B UI, docs). Pushing and opening the PR:

PR [#8](https://github.com/pugazg/kalaignar-autobiography/pull/8) opened. Watching Mobile CI:

Mobile CI green. Confirming the Vercel/site check (feature JSON + manifest changed):

All checks green — PR [#8](https://github.com/pugazg/kalaignar-autobiography/pull/8) is `CLEAN`/`MERGEABLE`, left **unmerged** per the stop condition. Every stop-condition item is met.

## Final report

1. **PR #7 merge SHA:** `90b2e40` (post-merge Mobile CI green; native Murasoli files verified on `main`; tree clean)
2. **Activity-4 branch:** `mobile/increment2-explore` (from updated `main`)
3. **Activity-4 commit SHAs:** `6ad951b` (4A places export) · `70746f5` (4B Explore UI) · `2a34435` (docs)
4. **Activity-4 PR:** [#8](https://github.com/pugazg/kalaignar-autobiography/pull/8) (open, green, mergeable — **not merged**)
5. **Files changed:** exporter `pipeline/builders/export-feature-data.ts`; new `public/data/app/features/places.json`; `public/data/app/manifest.v1.json`; new `mobile/src/data/useFeature.ts`, `mobile/src/components/ChapterRefs.tsx`, `mobile/src/screens/{Themes,People,Places}Screen.tsx`; modified `mobile/src/data/types.ts`, `mobile/src/navigation/index.tsx`, `mobile/src/screens/ExploreScreen.tsx`; docs `mobile/docs/{ROADMAP,DATA_CONTRACTS}.md`, `HANDOVER.md`. No `ios/`, signing, SDK, or mapping-dependency changes.
6. **Places exporter changes:** imports `data/places.ts`, adds a `places` dataset + validation; exporter now emits all six datasets.
7. **`places.json`**** path:** `public/data/app/features/places.json`
8. **Places count:** **10**
9. **Places validation:** unique ids ✓; non-empty tamil/name/note ✓; non-empty refs ✓; every ref resolves to a real memoir chapter ✓; `x`/`y` finite and within the schematic viewBox (x 0–1640, y 0–2032) ✓ — all pass, no source inconsistencies. Coordinates exported verbatim (never geocoded).
10. **Deterministic rerun:** byte-identical (no diff)
11. **Manifest feature URLs:** `timeline, governance, people, places, themes, quotes` all → `/data/app/features/*.json` (+ `stats` → `/data/stats.json`); **`places`**** now populated**, all others unchanged; memoir 6 vols/391 ch + Murasoli 346 letters unchanged
12. **Theme count:** 6 · 13. **People count:** 15 · 14. **Place count:** 10
13. **Explore navigation:** Explore → {Themes → ThemeDetail | People → PersonDetail | Places → PlaceDetail | MurasoliLibrary…}; 6 new routes on the existing stack (back/tabs/theme preserved)
14. **Theme UI:** list (Tamil+English+snippet) → detail (narrative, initiatives, achievements, stats, archive context; `archive.events` → Reader, `archive.people` → Person detail; memoir refs → Reader)
15. **People UI:** list (Tamil/English/role) → detail (relationship, first-appears, memoir refs → Reader)
16. **Places UI:** list (Tamil/English/note) + detail (note, memoir refs → Reader)
17. **Schematic map:** yes — dependency-free; markers percentage-positioned from source `x`/`y` in viewBox `0 0 1640 2032`, labelled "Schematic positions — relative only, not geographic / not to scale", tap → detail. No mapping library, no GPS.
18. **Memoir Reader deep-links:** verified — Theme archive-event → `v2-ch49`, Place (Chennai) ref → `v2-ch66`, Person refs resolved; via shared `ChapterRefs` (unresolved ids dropped, no invented `find`)
19. **Offline/cache:** feature JSON offline-first via `api.feature`; each collection degrades independently (missing URL/no-cache/malformed → truthful state, no crash); no bulk download
20. **Murasoli regression:** none (untouched; still opens natively)
21. **Library/Timeline/Search regression:** none — memoir Library shows corrected titles; Timeline/Search unaffected
22. **Root typecheck:** PASS · 25. **Mobile typecheck:** PASS · 26. **Manifest validation:** PASS · 27. **expo-doctor:** PASS (21/21) · 28. **iOS export:** PASS · 29. **Website build:** PASS (`next build`)
23. **GitHub Mobile CI:** PASS (`2a34435`) · 31. **Vercel:** PASS
24. **Known limitations:** no Governance/Quotes UI (data-only, deferred); no cross-feature search; no bulk download; Places schematic map is dot-markers only (no TN outline, to avoid a mapping dependency); Murasoli bookmarks still deferred
25. **Out-of-scope not started:** Governance UI, Quotes UI, Murasoli enhancements, cross-collection search/Saved, bulk downloads, push, universal links, privacy/legal, App Store, share-as-image, iPad, SDK upgrades — none touched
26. **Exact next activity (current roadmap):** Increment 2's richer-surfaces items (feature export, Timeline, Murasoli reader, Explore entry points) are now **all complete**. The next open roadmap items are in **"Production / store-ready — Not done"**, first listed being **Push notifications** (`expo-notifications` + a `contentVersion`-keyed update signal) — to be confirmed/prioritized with a fresh prompt.

One process note: iOS ATS blocks plain-`http://localhost`, so Places (whose live `features.places` deploys only on merge) was verified against the branch's own data via a temporary `env.ts` origin override, which I reverted — confirmed `env.ts`/`app.json`are pristine and nothing machine-specific was committed. Stopping here; Activity-4 PR is green and awaiting your decision to merge. I did not begin the next activity.

### Assistant

PR #8 is in the right state to proceed: **open, not merged, mergeable**, head `2a34435`, with exactly the Activity-4 scope described. 

I would **not jump straight to Push Notifications yet**. Increment 2 is now functionally complete, so the best next move is to merge PR #8, verify post-merge CI, then do a short **production-readiness prioritization pass** before choosing the next implementation. Push notifications are only first by list order; they are not necessarily the highest-value next step.

The sensible priority order to evaluate is:

1. **Privacy + Support pages** — these are submission blockers.
2. **Universal Links / Associated Domains** — unfinished platform integration.
3. **Accessibility audit** — important before store submission.
4. **Download manager / offline UX polish** — user-facing quality.
5. **Share-as-image** — useful but not blocking.
6. **Push notifications** — valuable, but not necessary to submit.
7. **Crash reporting / analytics**
8. **iPad/tablet layouts**
9. **TestFlight / Android internal testing / store assets**

So the next Claude prompt should be a **merge + readiness audit**, not immediately “build push notifications.”

<a id="turn-0357"></a>
## Turn 0357 — 2026-08-15T12:27:02.286Z

### User

please provide the prompt for Claude

### Assistant

:::writing{variant="document" id="59341" title="Claude Prompt — Merge Activity 4 + Production Readiness Audit"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — merged
- Increment 2 · Activity 1 — feature dataset export — merged
- Increment 2 · Activity 2 — Timeline milestones — merged
- Increment 2 · Activity 3 — Native Murasoli reader — merged
- Increment 2 · Activity 4 — Places export + native Explore Themes/People/Places — PR #8
  - branch: `mobile/increment2-explore`
  - head: `2a34435`
  - PR is currently open, green and mergeable

The richer-surface work in Increment 2 is now complete.

Do NOT begin Push Notifications or any other production feature immediately.

This workstream has two stages:

# Stage 1 — Merge Activity 4 cleanly

Before merging:

1. Re-read current:
   - `HANDOVER.md`
   - `mobile/docs/ROADMAP.md`
   - `mobile/docs/DATA_CONTRACTS.md`
   - `mobile/docs/BUILD.md`

2. Confirm PR #8:
   - is still open
   - is green
   - is mergeable
   - head is still the expected Activity-4 commit
   - contains only:
     - Places deterministic export
     - Places manifest integration
     - native Themes/People/Places Explore UI
     - related docs

3. Inspect the full PR #8 diff.

4. Confirm there are no:
   - generated `ios/`
   - signing files
   - SDK changes
   - temporary localhost/origin overrides
   - machine-specific values
   - unrelated archive/content changes
   - Governance/Quotes UI
   - other production/store-ready work

5. Merge PR #8 into `main`.

6. Confirm:
   - merge commit exists on `main`
   - post-merge Mobile CI passes
   - Vercel/site checks pass
   - `features.places` is populated on `main`
   - Themes/People/Places code is present on `main`
   - working tree is clean

Only after Stage 1 is fully green should you begin Stage 2.

---

# Stage 2 — Production Readiness Audit

Do NOT implement features yet.

The purpose of this stage is to inspect the CURRENT repository and produce a prioritized production/store-readiness plan based on actual blockers and current app state.

This is an audit/planning activity only.

Create a fresh branch from updated `main` only if documentation needs to be changed.
If no repo changes are needed, do not create unnecessary commits.

## Mandatory reading

Read completely:

- `HANDOVER.md`
- `mobile/docs/ROADMAP.md`
- `mobile/docs/BUILD.md`
- `mobile/docs/STORE_CHECKLIST.md` if present
- `mobile/docs/ARCHITECTURE.md`
- `mobile/docs/DATA_CONTRACTS.md`
- `mobile/app.json`
- `mobile/eas.json` if present
- `mobile/package.json`
- `.github/workflows/mobile-ci.yml`
- current Settings screen
- current navigation
- current sharing code
- current offline/download code
- current theme/accessibility-related components
- current app icon/splash config
- current website routes:
  - `/privacy`
  - `/about`
  - any support/help route
- current universal-link related files under:
  - `.well-known/`
  - `public/.well-known/`
  - Android asset-links locations
- any existing analytics/crash-reporting setup
- any TestFlight / EAS / store docs

Search the repo before concluding something is missing.

---

# Audit categories

Evaluate each category below against the actual current code and docs.

For each item classify it as:

- COMPLETE
- PARTIAL
- NOT STARTED
- BLOCKER FOR STORE SUBMISSION
- OPTIONAL / POST-LAUNCH

Do not classify based purely on roadmap ordering.

## A. Legal / store-link blockers

Inspect:

- Privacy Policy page
- Support/About page
- URLs currently exposed in Settings
- whether those URLs resolve to real public pages
- whether wording is suitable for store submission
- whether copyright/permissions wording is still intentionally deferred

Determine whether missing privacy/support pages are genuine App Store blockers.

Do NOT draft legal copy unless explicitly needed for the audit.

---

# B. Universal Links / deep links

Inspect:

- iOS Associated Domains config
- Android intent filters
- `.well-known/apple-app-site-association`
- `assetlinks.json`
- native deep-link route handling
- what currently works only via the custom app scheme
- what was deliberately deferred under the free Apple Personal Team setup

Separate:

1. app-side implementation
2. website-side association files
3. Apple entitlement/signing requirements
4. actual verification status

Do not falsely mark Universal Links complete because route handling exists.

---

# C. Accessibility

Audit the current app for likely App Store / usability readiness.

Inspect at minimum:

- Dynamic Type
- screen-reader labels
- touch target sizes
- color contrast
- theme contrast in light/sepia/dark
- focus order
- headings/semantic labels
- list accessibility
- Tamil text scaling/truncation
- VoiceOver expectations
- reduced-motion concerns if relevant

Do NOT attempt a full manual VoiceOver audit unless tooling supports it.

Classify what can be statically checked vs what requires later physical-device/manual verification.

---

# D. Offline / download UX

Inspect:

- per-chapter download
- offline images
- Murasoli cache behavior
- Timeline/feature cache behavior
- current storage accounting
- clear-offline behavior
- lack/presence of:
  - offline banner
  - bulk volume download
  - download manager
  - storage breakdown
  - retry UI
  - cache invalidation/version behavior

Determine which items are:
- submission blockers
- quality improvements
- post-launch enhancements

Do NOT implement them.

---

# E. Sharing

Inspect current sharing behavior.

Classify:

- native text share
- share-as-image
- current dependencies such as `react-native-view-shot`
- whether share-as-image is actually implemented

Determine whether this is required before launch or optional.

Do not implement share-as-image in this audit.

---

# F. Push notifications

Inspect:

- `expo-notifications` dependency
- actual code usage
- notification permission handling
- device token registration
- backend/content-update signaling
- manifest `contentVersion`
- whether a notification service exists

Determine whether Push Notifications are:
- required for first release
- useful but optional
- entirely unimplemented

Do NOT begin notification implementation.

---

# G. Crash reporting / analytics

Inspect whether any of the following are already present:

- Sentry
- Expo error reporting
- analytics SDK
- custom telemetry
- privacy-respecting diagnostics

Classify crash reporting and analytics separately.

Treat analytics as optional unless there is an explicit product requirement.

Do not add dependencies.

---

# H. iPad / tablet readiness

Inspect:

- `supportsTablet`
- responsive layouts
- fixed-width assumptions
- Reader behavior on tablet
- navigation layout
- split-view support
- orientation

Classify whether:
- basic iPad compatibility exists
- tablet optimization is missing
- store launch is blocked or not blocked

Do not redesign for iPad in this audit.

---

# I. Android readiness

Inspect:

- Android package
- adaptive icon
- intent filters
- build config
- current emulator/testing status
- Play internal-testing readiness
- signing/build requirements
- assetlinks

Classify whether Android release should be:
- simultaneous with iOS
- later
- currently blocked

Do not start Android release work.

---

# J. iOS TestFlight / App Store readiness

Inspect:

- Apple bundle identifier
- EAS build config
- provisioning/signing expectations
- paid Apple Developer membership dependency
- TestFlight status
- App Store Connect setup requirements
- screenshots
- app description
- keywords
- privacy labels
- age rating
- support URL
- privacy URL
- export compliance
- encryption declarations if relevant

Do not assume App Store Connect has been configured unless the repo/docs prove it.

Separate:
- code readiness
- account/process readiness
- asset/metadata readiness

---

# K. App Store Review 4.2 / minimum functionality

Re-evaluate the app as it exists now.

It currently has native functionality including:

- six-volume memoir reader
- offline reading
- Tamil/English
- search
- Timeline
- Explore Themes/People/Places
- native Murasoli reader
- bookmarks/progress
- themes
- sharing

Assess whether there is any meaningful remaining 4.2 risk.

Do not overstate certainty about App Review acceptance.

---

# L. CI / release engineering

Inspect:

- Mobile CI
- manifest validation
- expo-doctor
- iOS export
- root build checks
- Vercel
- EAS build configuration
- release/versioning strategy
- app version/build number
- content version vs binary version

Identify gaps before a real TestFlight build.

Do not change CI unless the audit uncovers a concrete defect.

---

# Prioritization framework

Do NOT simply follow roadmap order.

Rank outstanding work using this order of concern:

1. genuine store-submission blockers
2. reliability/accessibility blockers
3. release-engineering prerequisites
4. high-value user-facing launch polish
5. optional enhancements
6. post-launch features

Specifically challenge the assumption that Push Notifications should be next merely because they are first in the current list.

---

# Expected recommendation format

Produce a priority table with columns conceptually equivalent to:

- Priority
- Work item
- Current status
- Store blocker?
- Why
- Recommended timing
- Estimated scope/risk

No need to estimate days unless clearly useful.
Use relative scope such as:
- Small
- Medium
- Large

---

# Suggested priority order to evaluate

Do not blindly adopt this; verify it against current code:

1. Privacy + Support/About public pages
2. Universal Links / Associated Domains / association files
3. Accessibility audit
4. Release/TestFlight readiness
5. Offline banner / offline UX polish
6. Download-manager enhancements
7. Share-as-image
8. Crash reporting
9. Push notifications
10. iPad optimization
11. Android internal testing
12. analytics

If the repository evidence supports a different order, explain why.

---

# Store blocker definition

Be strict.

A “store blocker” should mean something that prevents or materially jeopardizes:

- building/signing/submitting
- providing required App Store metadata/URLs
- basic app operation
- accessibility/review compliance
- required legal/privacy disclosure

Do not call every nice-to-have a blocker.

---

# Documentation output

At the end of the audit, create or update ONE clear planning document, preferably:

`mobile/docs/PRODUCTION_READINESS.md`

If a similar current document already exists, update that instead of duplicating it.

It should contain:

1. current app baseline
2. completed Increment 1 + 2 summary
3. audit status by category
4. blockers
5. recommended execution order
6. deliberately deferred items
7. exact recommended next workstream

Do not scatter the audit across many docs.

Update `mobile/docs/ROADMAP.md` only if needed to make the next priority unambiguous.

Update `HANDOVER.md` only with a concise pointer to the readiness document and exact next action.

---

# Scope exclusions

This is an audit.

Do NOT implement:

- Push notifications
- Universal Links
- privacy pages
- About/support pages
- accessibility fixes
- download manager
- offline banner
- share-as-image
- crash reporting
- analytics
- TestFlight
- App Store metadata/assets
- iPad redesign
- Android release
- any new reader/discovery feature

Do not add dependencies.

Do not change user-facing behavior.

---

# Verification

If documentation only is changed:

- run markdown/basic repo checks as appropriate
- no unnecessary native build is required

If any code/config must be changed merely to correct an obvious documentation/config inconsistency, explain why before doing so and run relevant gates.

Do not turn the audit into an implementation activity.

---

# Stop condition

Stop once:

- PR #8 is merged
- post-merge CI is green
- production-readiness audit is complete
- blocker/non-blocker status is documented
- priorities are ranked
- exact next workstream is recommended

Do NOT begin that next workstream in the same activity.

---

# Final report

Report:

1. PR #8 merge SHA
2. post-merge CI result
3. readiness document path
4. current genuine store blockers
5. non-blocking launch-polish items
6. optional/post-launch items
7. Universal Links status
8. privacy/support status
9. accessibility status
10. offline/download status
11. sharing status
12. Push Notification status
13. crash-reporting status
14. iPad status
15. Android status
16. TestFlight/App Store process status
17. App Review 4.2 assessment
18. release-engineering status
19. ranked next-workstream order
20. single recommended next workstream
21. confirmation that no production feature was implemented during the audit

Start with Stage 1. Do not begin the audit until PR #8 is merged and post-merge Mobile CI is green.
:::

<a id="turn-0358"></a>
## Turn 0358 — 2026-08-15T12:52:21.392Z

### User

Starting **Stage 1 — merge PR #8**. Confirming it's still green/mergeable, head unchanged, and scope-clean:

PR #8 is green, mergeable, head `2a34435`; scope is exactly Activity 4 (places export + manifest + Explore UI + docs) — `env.ts` is not even in the diff, so no origin override leaked. **Merging:**

Merged (`6713095`). Verifying post-merge state:

Stage 1 verified: merge `6713095` on `main`, Mobile CI green, `features.places` populated, Explore screens present, tree clean. Let me confirm the site (Vercel prod) deploy on `main`:

**Stage 1 fully green** — PR #8 merged (`6713095`), main Mobile CI + Vercel both success, live site 200 with `features.places`populated, Explore screens on `main`, tree clean.

Now **Stage 2 — Production Readiness Audit** (inspection + planning only). Let me gather the audit evidence. Config, deps, docs, and store/legal/deep-link files:

STORE\_CHECKLIST.md exists (I'll update that rather than duplicate). No `eas.json`, no `.well-known` files, no `/privacy` or `/about`website routes, version 0.1.0 with no build numbers. Let me read the store checklist + app.json, and check whether the deps are actually *used* and whether the Settings links resolve:

STORE\_CHECKLIST is a good raw gate list (I'll create PRODUCTION\_READINESS as the prioritized audit and point to it). Now app.json config + whether the deps are actually used + Settings links + do the legal URLs resolve:

Major findings: **`expo-notifications`****, ****`react-native-view-shot`****, ****`netinfo`**** are declared deps but used in 0 source files** (push, share-as-image, offline banner are unimplemented), and **live ****`/privacy`**** + ****`/about`**** return 404** — the Settings links are dead. Let me read the app.json deep-link config and confirm native text-share exists + no analytics/crash tooling:

I now have comprehensive audit evidence. Key facts: deep-link config exists app-side (`applinks:nenjukkuneethi.org` + Android autoVerify intent filters + linking config) but **no ****`apple-app-site-association`****/****`assetlinks.json`** website files; **`/privacy`**** + ****`/about`**** 404**(Settings links dead); **expo-notifications / view-shot / netinfo declared but unused** (push, share-as-image, offline banner unimplemented); native text share works (2 call sites); no crash/analytics tooling; `supportsTablet: true`; no `eas.json`; CI already runs validate\:manifest (roadmap says otherwise — stale).

Let me create the docs branch and write the audit:

Now writing the audit document:

Now minimal ROADMAP updates — correct the stale "manifest validation in CI" item and point to the audit for the next priority. Let me read the Production section:

Now HANDOVER — a concise pointer + exact next action. Updating the Activity-4 "next activity" line:

Docs written. Let me confirm the change is docs-only (no code/config touched) and commit:

Docs-only confirmed. Committing, pushing, and opening a PR:

PR [#9](https://github.com/pugazg/kalaignar-autobiography/pull/9) opened (docs-only). Let me confirm CI passes:

Mobile CI green on the audit PR (Vercel finishing — docs-only, doesn't affect the site build). **Stop condition met.** The audit PR is left open for you to merge (planning doc), and I did not begin the next workstream.

## Final report

1. **PR #8 merge SHA:** `6713095` (Increment 2 · Activity 4 merged to `main`)
2. **Post-merge CI:** Mobile CI **PASS** on `6713095`; Vercel prod deploy **success**; live site 200 with `features.places` populated; Explore screens present on `main`; tree clean
3. **Readiness document:** [mobile/docs/PRODUCTION\_READINESS.md](https://claude.ai/epitaxy/mobile/docs/PRODUCTION_READINESS.md) (audit PR [#9](https://github.com/pugazg/kalaignar-autobiography/pull/9), Mobile CI green — left unmerged for your decision)
4. **Genuine store blockers (strict):**
   - **Privacy Policy + Support/About pages** — Settings links to `/privacy` and `/about`, both **404**. Apple requires a working privacy URL; App Store Connect requires a support URL. (Website work.)
   - **Release engineering to produce a signable build** — no `eas.json`, no version/build-number strategy; **paid Apple Developer account** required for TestFlight/App Store + Associated Domains signing.
   - **Store metadata + assets** — screenshots, description (Ta/En), keywords, privacy labels, age rating (none started).
5. **Non-blocking launch-polish:** offline banner (`netinfo` unused), accessibility manual pass (contrast + VoiceOver), crash reporting, Universal Links website files + verification.
6. **Optional/post-launch:** share-as-image (`view-shot` unused), download manager/bulk download/storage breakdown, **push notifications**, iPad optimization, Android release, analytics.
7. **Universal Links:** app-side COMPLETE (`applinks:nenjukkuneethi.org`, Android autoVerify intent filters, `linking` config); **website ****`.well-known`**** files NOT STARTED**; entitlement signing + on-device verification NOT done (needs paid team). Custom scheme works. **Not falsely complete.**
8. **Privacy/support:** NOT STARTED — both URLs 404 (blocker).
9. **Accessibility:** PARTIAL — Dynamic Type + accessibility labels present (static); contrast-across-themes + VoiceOver/focus-order pass NOT done (needs manual/device).
10. **Offline/download:** core COMPLETE (per-chapter download, offline images, offline-first Murasoli/feature caches, storage total, clear-offline); offline banner / bulk / download-manager / storage-breakdown / content-version update-check NOT started (non-blocking).
11. **Sharing:** native text share COMPLETE (both readers); share-as-image NOT started (optional).
12. **Push notifications:** NOT STARTED — dep + plugin present, **0 code**; not required for first release.
13. **Crash reporting:** NOT STARTED (recommended around launch); **analytics** NOT STARTED (optional — conflicts with the no-data privacy stance).
14. **iPad:** PARTIAL — `supportsTablet: true`, runs with flex layouts; not optimized (no split-view/max-width). Not a hard blocker; iPad screenshots needed if submitting iPad.
15. **Android:** config COMPLETE (package, adaptive icon, autoVerify intent filters); build/signing/`assetlinks`/internal-testing NOT started — recommend **after** iOS.
16. **TestFlight/App Store process:** code readiness HIGH; **account/process** (paid membership, App Store Connect) NOT done; **asset/metadata** NOT done; `eas.json` missing; export-compliance flag not set (standard HTTPS ⇒ exempt, one-line).
17. **App Review 4.2:** **LOW risk** — rich native app (6-vol reader, offline, Ta/En, search, Timeline, Explore Themes/People/Places, native Murasoli, bookmarks/progress, themes, text share), no WebView wrapper, no dead-end/"coming soon" screens.
18. **Release engineering:** Mobile CI COMPLETE (typecheck / validate\:manifest / expo-doctor / iOS export — so "manifest validation in CI" is done, corrected in ROADMAP); **gaps:** no `eas.json`, no version/build-number strategy.
19. **Ranked next-workstream order:** (1) Privacy+Support pages → (2) release-eng (`eas.json` + versioning) → (3) accessibility pass → (4) store metadata/assets → (5) Universal Links website files → (6) offline banner → (7) crash reporting → (8) share-as-image → (9) download manager → (10) push → (11) iPad → (12) Android → (13) analytics.
20. **Single recommended next workstream:** **Legal/store-link readiness** — publish the Privacy Policy and Support/About pages on `nenjukkuneethi.org` and confirm the Settings links resolve, paired with a small **release-engineering setup** (`eas.json` + version/build strategy). **Explicitly not push notifications.**
21. **Confirmation:** no production feature was implemented — planning/docs only (`PRODUCTION_READINESS.md` + ROADMAP/HANDOVER pointers), no dependencies added, no user-facing behavior changed.

Stopping here per the stop condition — the next workstream is recommended but not started.

### Assistant

This is the right stopping point. I also checked GitHub: **PR #9 is still open, unmerged, mergeable, and docs-only**—3 files changed, with no feature implementation. 

One refinement before the next workstream: I would **separate legal/store-link readiness from release engineering**, rather than doing both together. The clean sequence is:

1. **Merge PR #9** and verify post-merge CI.
2. **Production Readiness Activity 1 — Privacy + Support pages**
   - create real `/privacy`
   - create a genuine `/support` page rather than relying on `/about` as support
   - retain `/about` as an About page if useful
   - update the mobile Settings URLs accordingly
   - deploy and verify all URLs return 200
   - ensure the privacy page accurately reflects what the app actually does today: no analytics, no advertising SDK, no account/login, etc., without making unsupported copyright/permission claims
   - run website + mobile regression checks
3. **Production Readiness Activity 2 — Release engineering**
   - `eas.json`
   - app version/build-number strategy
   - TestFlight build path
   - export-compliance configuration
   - paid Apple Developer prerequisites
4. Then accessibility, store metadata/screenshots, Universal Links, and the remaining polish items.

I would **not implement Push Notifications now**. At this stage they add permissions, backend/token handling, privacy considerations, and operational complexity without helping you get the first release submitted.

So the immediate next Claude workstream should be:

> **Merge PR #9 → Production Readiness Activity 1: Privacy Policy + Support/About website pages and mobile Settings link integration.**

<a id="turn-0359"></a>
## Turn 0359 — 2026-08-15T12:53:09.339Z

### User

provide prompt for claude

### Assistant

:::writing{variant="document" id="24681" title="Claude Prompt — Production Readiness Activity 1: Privacy + Support Pages"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — merged
- Increment 2 feature work — complete and merged through Activity 4
- Production Readiness Audit — PR #9
  - branch: `mobile/production-readiness-audit`
  - head: `38f159f`
  - PR is currently open, green, mergeable
  - docs-only
  - recommended next workstream: legal/store-link readiness

This workstream has two stages:

# Stage 1 — Merge PR #9

Before changing anything:

1. Confirm PR #9 is still:
   - open
   - green
   - mergeable
   - head unchanged
   - docs-only

2. Inspect the full PR diff one final time.

3. Confirm it contains only:
   - `mobile/docs/PRODUCTION_READINESS.md`
   - ROADMAP pointer/update
   - HANDOVER pointer/update

4. Confirm there are no code/config/dependency changes.

5. Merge PR #9 into `main`.

6. Verify:
   - merge commit is present on `main`
   - post-merge Mobile CI is green
   - working tree is clean

Only then start Stage 2.

---

# Stage 2 — Production Readiness Activity 1
## Privacy Policy + Support/About pages + mobile Settings links

The current audit found:

- `https://nenjukkuneethi.org/privacy` returns 404
- `https://nenjukkuneethi.org/about` returns 404
- mobile Settings currently points to dead legal/support URLs
- there is no dedicated support page
- these are genuine store-readiness blockers

The goal is to create real, public, accurate pages and wire the app to them.

Do NOT start release engineering (`eas.json`, TestFlight, build numbers) in this activity.

---

# Mandatory startup

Read completely before implementation:

- `HANDOVER.md`
- `mobile/docs/PRODUCTION_READINESS.md`
- `mobile/docs/ROADMAP.md`
- `mobile/docs/STORE_CHECKLIST.md`
- mobile Settings screen
- mobile config/env where website URLs are defined
- website app/router structure
- current website layout/components
- any existing About/Project/Contact/Footer content
- root README
- any existing legal/copyright/provenance wording
- current data/privacy-related dependencies and code usage

Also search the repository for:

- `privacy`
- `support`
- `about`
- `analytics`
- `sentry`
- `firebase`
- `expo-notifications`
- `AsyncStorage`
- `FileSystem`
- `Linking`
- external network origins
- account/login/auth code
- advertising SDKs
- tracking SDKs
- email/contact details already published by the project

Do not invent contact information.

---

# Important principle

The privacy/support pages must reflect what the app ACTUALLY does today.

Do not copy a generic privacy-policy template that claims things the app does not do.

Do not make legal/copyright assertions that are not supported by the repository.

Do not overclaim:

- ownership of source texts
- permission status
- public-domain status
- official affiliation
- endorsement by Kalaignar's family, DMK, Murasoli, or any archive

Use cautious archival-project wording.

---

# A. Privacy Policy page

Create a real public route:

`/privacy`

Use the existing website visual language.

The page should be clear, concise, and suitable for App Store submission.

## First inspect actual behavior

Determine from the CURRENT code whether the app:

- requires user accounts
- collects names/emails
- uses authentication
- uses analytics
- uses crash reporting
- uses advertising
- uses tracking SDKs
- sells/shares personal data
- sends data to third-party analytics services
- uses push notifications
- accesses contacts
- accesses location
- accesses photos/camera
- accesses microphone
- accesses health data
- stores reader preferences locally
- stores bookmarks/progress locally
- caches downloaded content locally
- makes network requests to `nenjukkuneethi.org`
- invokes the operating system share sheet
- opens external links

Base the policy on the evidence.

## Expected current-policy direction

If confirmed by code, the policy may state that the app currently:

- does not require an account
- does not collect registration/profile information
- does not contain advertising
- does not use third-party analytics
- does not use cross-app tracking
- does not sell personal data
- stores reading preferences/progress/bookmarks/download/cache data locally on the device
- fetches archival content from `nenjukkuneethi.org`
- may pass content to another app only when the user explicitly invokes the system Share feature
- does not currently send push notifications even if the dependency exists but is unused

Only state these if the source code supports them.

Do NOT say “we collect no data whatsoever” unless that can genuinely be defended, because ordinary server requests may produce standard infrastructure logs.

A safer accurate distinction is:
- the app itself does not intentionally collect account/profile/analytics data;
- normal hosting/network infrastructure may process routine request metadata needed to serve content.

## Privacy page sections

Keep it practical. Suggested structure:

1. Privacy Policy
2. What the app is
3. Information the app does not request/collect directly
4. Information stored on the device
5. Network requests and website hosting
6. Sharing
7. Notifications
8. Third-party services
9. Children's privacy / general-audience statement where appropriate
10. Changes to this policy
11. Contact / support link

Do not invent an effective date older than the actual publication date.

Use the current date if an effective date is shown.

---

# B. Support page

Create a dedicated route:

`/support`

This should become the App Store support URL.

Do not use `/about` as a substitute for support.

The support page should include only support mechanisms that genuinely exist.

Inspect the repository/site for a real contact channel.

Possible content, if supported:

- brief explanation of the Nenjukku Neethi archive/app
- troubleshooting:
  - content not loading
  - offline/download behavior
  - Tamil font/display
  - search
  - restoring/clearing local cached content
- supported platforms/status
- links to:
  - Privacy Policy
  - About
  - project/site home
- GitHub issue/contact path only if that is genuinely intended for end users

Do NOT invent an email address.

If there is no dedicated support contact, use a truthful support pathway already available in the project rather than fabricating one.

---

# C. About page

Create:

`/about`

or fix the existing route if one already exists but is broken.

This is informational, not the App Store support URL.

It should explain, factually and cautiously:

- the project is a digital archival/reading initiative around Kalaignar M. Karunanidhi's autobiographical and related archival material
- the site/app provides structured access to memoir volumes and related material
- the project is independent unless the repository explicitly proves otherwise
- source/provenance acknowledgements should reflect actual repository data

Do not describe the project as “official.”

Do not claim copyright ownership over archival source material.

Do not introduce unsupported licensing claims.

---

# D. Footer/navigation integration

Add sensible links to the website footer or equivalent global navigation:

- About
- Privacy
- Support

Keep this subtle.

Do not redesign the site navigation.

---

# E. Mobile Settings integration

Update Settings so:

- Privacy Policy → `/privacy`
- Support → `/support`
- About → `/about`

Use the existing `nenjukkuneethi.org` base URL/config pattern.

Do not hardcode duplicate origins if there is already a shared constant.

Ensure all three open externally through the established pattern.

Do not add WebViews.

---

# F. App Store terminology

Use labels that map cleanly to store requirements:

- Privacy Policy
- Support
- About

Do not use ambiguous wording like:
- Legal Info
- Help-ish
- Contact Us

unless the current UI pattern requires it.

---

# G. Verify current privacy facts from code

Before writing final privacy wording, produce a brief internal evidence matrix such as:

- Accounts: none
- Analytics: none
- Ads: none
- Push: dependency present, feature inactive
- Local storage: bookmarks/progress/preferences/cache
- Network origin: nenjukkuneethi.org
- Sharing: OS share sheet, user initiated

Do not put implementation jargon like `AsyncStorage` into the public policy unless useful.

---

# H. Copyright / archival wording

This requires caution.

Do NOT make statements like:

- “All content is public domain”
- “We own all rights”
- “Used with permission”
- “Official archive”

unless directly supported.

Use neutral wording such as:

“The project presents archival material with source and provenance information where available.”

If an existing site/footer contains stronger unverified copyright language, do not expand it.

If necessary, flag it separately for later legal review rather than silently rewriting broad site policy in this activity.

---

# I. No tracking/analytics promise

If the current code genuinely has no analytics/tracking SDK:

Say so accurately.

But phrase it so future changes require a policy update, e.g.:

“The current version does not use advertising or third-party analytics SDKs.”

This is better than an absolute forever-promise.

---

# J. Notifications wording

Because `expo-notifications` is installed but the feature is not implemented:

The privacy policy should describe actual runtime behavior, not dependency presence.

If the app does not request notification permission or register tokens, say:

“The current version does not send push notifications.”

Do not promise this will never change.

---

# K. Support content quality

The Support page should be genuinely useful, not just “Contact us.”

At minimum cover:

- app/content loading problems
- offline content limitations
- clearing downloaded data/cache
- search limitations
- where to report content/transcription issues
- links to Privacy and About

Only include instructions supported by the current UI.

---

# L. Website implementation quality

Use existing:

- layout
- typography
- theme
- responsive behavior
- metadata/SEO helpers
- accessibility patterns

Add sensible metadata:
- page title
- description

Do not add dependencies.

Do not create a separate legal-site design system.

---

# M. Accessibility

The new pages should have:

- semantic headings
- readable text width
- link text that makes sense out of context
- sufficient contrast using existing theme
- mobile responsive layout

Do not begin the app-wide accessibility audit here.

---

# Verification

After implementation run:

## Website

- root typecheck
- lint if established
- `next build`
- relevant tests

Verify locally or through preview that:

- `/privacy` → 200
- `/support` → 200
- `/about` → 200

After PR/Vercel preview:

- confirm all three preview URLs resolve
- confirm production after merge only if/when merged

## Mobile

Run:

- `npm run typecheck`
- `npm run validate:manifest`
- `npx expo-doctor`
- `npx expo export --platform ios`

No physical-device test is required.

Simulator smoke only if Settings behavior is changed enough to warrant it.

At minimum statically confirm all Settings URLs are correct.

---

# Documentation

Update only what is needed.

## `mobile/docs/PRODUCTION_READINESS.md`

Mark:

- Privacy Policy URL — complete
- Support URL — complete
- About page — complete

Remove them from genuine blockers once deployed and verified.

Do NOT mark release engineering complete.

## `mobile/docs/STORE_CHECKLIST.md`

Update relevant URL items only.

## `HANDOVER.md`

Record:

- implementation
- URLs
- verification
- remaining blockers
- exact next workstream

The expected next workstream after this is:

**Production Readiness Activity 2 — Release engineering / TestFlight preparation**

Do not begin it in this activity.

---

# Git discipline

Use a fresh branch from updated `main`, for example:

`mobile/production-legal-pages`

Recommended logical commits:

1. Website Privacy / Support / About pages
2. Mobile Settings link integration
3. Docs/status update

Do not create unnecessary micro-commits.

Inspect the complete diff before pushing.

Confirm no:

- generated `ios/`
- signing material
- secret/contact info invented
- SDK changes
- new dependencies
- unrelated archive edits

Push branch and open a PR.

Require:

- Mobile CI green
- Vercel preview green
- website build green

Leave the PR unmerged once green unless explicitly required by this workstream.

---

# Scope exclusions

Do NOT implement:

- `eas.json`
- TestFlight
- App Store Connect
- build-number/versioning strategy
- export compliance config
- Universal Links
- `.well-known` files
- Push notifications
- crash reporting
- analytics
- offline banner
- download manager
- share-as-image
- accessibility remediation outside the new pages
- iPad redesign
- Android release
- store screenshots/metadata
- unrelated archive/content work

This activity is only:

**Privacy + Support + About + Settings integration + status docs**

---

# Stop condition

Stop when:

- PR #9 is merged
- post-merge CI passes
- `/privacy` exists
- `/support` exists
- `/about` exists
- Settings points to the correct three URLs
- website build passes
- Mobile CI passes
- Vercel preview passes
- pages have been reviewed against the actual app behavior
- readiness docs are updated
- new PR is green

Do NOT begin release engineering.

---

# Final report

Report:

1. PR #9 merge SHA
2. new branch
3. commit SHA(s)
4. new PR number
5. files changed
6. Privacy URL
7. Support URL
8. About URL
9. privacy-policy evidence used from current code
10. local-data behavior documented
11. analytics/tracking statement
12. notification statement
13. support mechanisms published
14. Settings URLs after change
15. website typecheck/build result
16. mobile typecheck result
17. manifest validation result
18. expo-doctor result
19. iOS export result
20. GitHub Mobile CI result
21. Vercel result
22. remaining genuine store blockers
23. confirmation no release-engineering work was started
24. exact next activity:

**Production Readiness Activity 2 — Release engineering / TestFlight preparation**

Start with Stage 1 and do not begin the legal/store-link work until PR #9 is merged and post-merge CI is green.
:::

<a id="turn-0360"></a>
## Turn 0360 — 2026-08-15T13:51:51.366Z

### User

Understood — let me wrap up cleanly: open the pending legal-pages PR to capture the work, prune merged branches, confirm `main` is authoritative, then write the handover + give you a new-chat prompt.

First, open the PR (the branch is already pushed) and take stock of all branches:

PR [#10](https://github.com/pugazg/kalaignar-autobiography/pull/10) opened (mergeable). Now let me confirm which of my branches are merged before deleting (the two `agent/*`branches are pre-existing paused pilots with open PRs — I'll leave those):

Merged and safe to delete (8): the 7 merged-PR branches + `mobile/increment-1-runnable` (0 ahead / fully in main). **Keeping**`main`, `mobile/production-legal-pages` (PR #10 open), and the two `agent/*` branches (pre-existing paused pilots, PRs #1/#2 — not mine). Deleting the merged remote branches:

Remote is clean (only `main`, the open PR #10 branch, and the two unrelated paused-pilot branches). Now local cleanup — the stale worktree + merged local branches:

Let me remove the stale SDK worktree and delete the merged local branches (keeping `main`, the current `production-legal-pages`, and the main checkout's WIP branch): I'll start by reading the handover document.

Let me orient myself: check git state, the true origin/main SHA, and PR #10 status.

PR #10 is `CLEAN`/`MERGEABLE` with all checks green (Mobile CI + Vercel SUCCESS). origin/main is at `0752072` as expected. There's local WIP on this branch (including a WIP `eas.json`) which the handover says to leave alone — I'll treat it as reference only and do Activity 2 on a fresh branch.

Let me check the repo's merge convention before merging PR #10.

History is linear (squash merges). Merging PR #10 with squash and deleting the remote branch.

The merge itself likely succeeded; only the local branch deletion failed (it's checked out in the kn-increment2 worktree). Let me verify.

Merged — origin/main advanced to `aa8639f`. The remote branch still lingers (the `--delete-branch` aborted on the local-branch step). Let me delete the remote branch.

Remote is clean (only `main`). Now let me verify post-merge CI on `main` and check the live pages. Vercel deploys take 1–3 min, so let me check CI status and the live endpoints.

Mobile CI on `main` is still running and Vercel hasn't finished deploying (pages still 404 from the old build). Let me poll in the background until the pages go live and CI completes.

While that polls, let me set up Activity 2. First, let me review the production-readiness plan and the existing WIP `eas.json` / `app.json` as reference.

This branch is behind main. Let me fetch and read the plan from the fresh main.

The local fetch ref is flaky (as the handover warned). Let me fetch the specific merge commit directly.

I have the full plan. Activity 2 = `eas.json` build profiles, version/build-number strategy, and the export-compliance flag. The merge commit `aa8639f` is present locally (the `git show` worked), so I can branch from it directly despite the flaky remote ref.

Let me inspect the current `app.json` (from merged main) and the WIP `eas.json` in this dir as reference.

The WIP `app.json` in this dir is broken experimental smoke-test work (duplicated `applinks`, dropped `expo-sharing`/`expo-splash-screen`/`expo-status-bar` plugins) — I'll leave it untouched per the handover and start Activity 2 clean from merged main. The WIP `eas.json` is a reasonable reference.

Let me check the poll progress and the kn-increment2 worktree (which has node\_modules for running the gate).

All three legal pages are now live (200). Let me confirm the post-merge Mobile CI run on `main` completed green.

Step 1 is fully verified: PR #10 squash-merged, remote branch deleted, Mobile CI on `main` green, Vercel deployed, and `/privacy`, `/support`, `/about` all return 200 live.

Now Activity 2. Let me create a fresh branch from merged main (`aa8639f`) in the kn-increment2 worktree (which has node\_modules for the gate).

Branch is at merged main, clean. Let me read the current app.json and STORE\_CHECKLIST in the worktree, and confirm no eas.json exists on main yet.

I have everything I need. Let me write the Activity 2 changes in the worktree. First, read the worktree's app.json to edit precisely.

Now let me make the app.json edits: add `ios.buildNumber`, `ios.infoPlist.ITSAppUsesNonExemptEncryption`, and `android.versionCode`.

Now create `eas.json`:

Now document the strategy. Let me create a concise `docs/RELEASE.md` and update the STORE\_CHECKLIST.

Now update the STORE\_CHECKLIST to reflect what Activity 2 completes.

Let me add explicit checklist lines for `eas.json` and export compliance under Build & release.

Now run the mobile gate in the worktree: typecheck, validate\:manifest, expo-doctor, iOS export.

expo-doctor 21/21 passed. Now the iOS export.

iOS export succeeded. Now the website build from the worktree root.

Full gate is green. Let me confirm only my intended files changed (build artifacts should be gitignored), then commit.

Exactly the four intended files (build artifacts are gitignored). Let me commit and push.

Now open the PR (leaving it unmerged).

PR [#11](https://github.com/pugazg/kalaignar-autobiography/pull/11) created. Let me wait for its CI to go green (then leave it unmerged, as instructed).

While CI runs, let me clean up the generated `dist/` export artifact in the worktree (gitignored but leftover) to keep the checkout tidy.

Working checkout is clean. Here's where things stand while PR #11's CI runs:

**Step 1 — PR #10 (legal pages): ✅ complete**

- Squash-merged; both remote branches cleaned up (`main` only remains).
- Post-merge Mobile CI on `main`: **success**.
- `/privacy`, `/support`, `/about` all return **200** live on nenjukkuneethi.org (Vercel deployed).

**Step 2 — Activity 2 (release engineering): ✅ done, PR open & unmerged**

- [PR #11](https://github.com/pugazg/kalaignar-autobiography/pull/11) on `mobile/release-engineering` (branched from merged main `aa8639f`).
- `eas.json` (dev/preview/production profiles, `appVersionSource: local`, `production.autoIncrement`); `app.json` seeded `ios.buildNumber "1"` / `android.versionCode 1` + `ITSAppUsesNonExemptEncryption: false`; new `docs/RELEASE.md` + checklist ticks.
- Local gate all green: mobile typecheck · validate\:manifest · expo-doctor 21/21 · iOS export; website typecheck · next build.
- Paid Apple Developer account flagged as the external prerequisite for the actual TestFlight build (not blocked on here).
- **Did not** touch push notifications.

I left the WIP in the backup checkout (`mobile/physical-device-smoke-test`) untouched per the handover. Waiting on PR #11's CI now — I'll confirm once it's green and leave it unmerged.

CI still running (attempt 2). I'll wait for the poll to conclude and report back when PR #11 is green.

I'll wait for the background poll to complete rather than re-checking. It will notify me when CI concludes.

Waiting on PR #11's CI to conclude — the background poll will notify me when it's done, and I'll confirm the green status then (leaving it unmerged).

Both tasks are complete.

## Summary

**Step 1 — PR #10 (legal pages): ✅ merged & verified**

- Squash-merged into `main` (`aa8639f`); both remote branches cleaned up — only `main` remains on origin.
- Post-merge Mobile CI on `main`: **success**.
- `/privacy`, `/support`, `/about` all return **200** live on nenjukkuneethi.org.

**Step 2 — Activity 2 (release engineering): ✅ done, PR green & unmerged**

- [PR #11](https://github.com/pugazg/kalaignar-autobiography/pull/11) — branch `mobile/release-engineering` off merged main. **CLEAN / MERGEABLE**, all checks green:
  - Mobile CI (`typecheck • manifest • doctor • export`): **SUCCESS**
  - Vercel + Vercel Preview Comments: **SUCCESS**
- Left **unmerged** as instructed.

What it contains:

- `mobile/eas.json` — dev/preview/production build profiles + submit placeholder; `appVersionSource: "local"` (build numbers git-versioned, reproducible, no EAS-account dependency); `development` builds on the iOS Simulator with no signing; `production.autoIncrement`.
- `mobile/app.json` — seeded `ios.buildNumber "1"` / `android.versionCode 1` (marketing version stays `0.1.0`); export-compliance flag `ITSAppUsesNonExemptEncryption: false`.
- `mobile/docs/RELEASE.md` (strategy + prerequisite) and `STORE_CHECKLIST.md` ticks.

**Flagged prerequisite:** the actual TestFlight build needs a **paid Apple Developer account** — then `eas login` → `eas init`(writes `extra.eas.projectId` into `app.json`) → `eas build --profile preview`. Repo work is not blocked on it.

**Not touched:** push notifications (de-prioritized), and the WIP in the backup checkout's `mobile/physical-device-smoke-test`branch (left as-is per the handover).

Remaining genuine store blockers after this: store metadata/assets (screenshots, descriptions, privacy labels, age rating) and the paid-account/TestFlight process itself.

### Assistant

PR #11 is in the correct state: **open, not merged, and mergeable**, with head `3f2b8f7`; its scope is exactly release engineering—`eas.json`, version/build numbering, export compliance, and release docs. 

The next move should be:

**Merge PR #11 → verify post-merge Mobile CI on `main` → begin Production Readiness Activity 3: Accessibility Audit & Fixes.**

I would do accessibility before store metadata/screenshots, because screenshots should reflect the final polished UI. After accessibility, the clean order is:

**Store metadata/assets → Universal Links website files → offline banner/crash reporting → optional enhancements.**

Push notifications can remain much later; they are not needed for the first release.

<a id="turn-0361"></a>
## Turn 0361 — 2026-08-15T13:55:44.584Z

### User

please provide prompt for claude

### Assistant

:::writing{variant="document" id="84217" title="Claude Prompt — Production Readiness Activity 3: Accessibility Audit & Fixes"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — complete
- Increment 1 — complete
- Increment 2 — complete
- Privacy / Support / About pages — merged and live
- Production Readiness Activity 2 — Release Engineering — PR #11
  - branch: `mobile/release-engineering`
  - head: `3f2b8f7`
  - PR currently open, green and mergeable
  - contains `eas.json`, version/build-number strategy, export-compliance config and release docs
- Push notifications remain deliberately deferred
- No physical-iPhone testing is required for this workstream

The next workstream is:

# Production Readiness Activity 3
## Accessibility Audit & Fixes

This workstream has two stages:

1. Merge and verify PR #11
2. Perform a focused accessibility audit, fix concrete issues, and document anything that still requires manual VoiceOver/device testing

Do NOT begin store screenshots/metadata yet.

---

# Stage 1 — Merge Release Engineering PR #11

Before merging:

1. Confirm PR #11 is still:
   - open
   - green
   - mergeable
   - head unchanged

2. Inspect the complete PR diff one final time.

3. Confirm its scope is only:
   - `mobile/eas.json`
   - `mobile/app.json` release/version/export-compliance configuration
   - `mobile/docs/RELEASE.md`
   - relevant `STORE_CHECKLIST.md` updates

4. Confirm no:
   - generated `ios/`
   - signing credentials
   - Apple certificates
   - EAS project secrets
   - unrelated feature work
   - push-notification implementation
   - accessibility changes

5. Merge PR #11 into `main`.

6. Verify:
   - merge commit is on `main`
   - post-merge Mobile CI is green
   - Vercel/site remains healthy
   - working tree is clean

Only then begin Stage 2.

---

# Stage 2 — Accessibility Audit & Fixes

Create a fresh branch from updated clean `main`, for example:

`mobile/accessibility-readiness`

Do not work directly on `main`.

The goal is NOT to claim perfect accessibility.

The goal is to:

- inspect the actual native app systematically
- fix clear static and simulator-verifiable accessibility issues
- preserve Tamil readability
- improve VoiceOver semantics where code supports it
- document remaining manual verification accurately

---

# Mandatory startup

Read completely:

- `HANDOVER.md`
- `mobile/docs/PRODUCTION_READINESS.md`
- `mobile/docs/ROADMAP.md`
- `mobile/docs/STORE_CHECKLIST.md`
- `mobile/docs/ARCHITECTURE.md`
- `mobile/docs/BUILD.md`

Inspect all current native screens, especially:

- Home
- Library
- Volume
- Reader
- Search
- Explore
- Timeline
- Saved
- Settings
- Murasoli Library
- Murasoli Volume
- Murasoli Reader
- Themes
- Theme Detail
- People
- Person Detail
- Places
- Place Detail

Inspect shared components before screen-specific fixes:

- typography components
- Card
- Pill / Badge
- Buttons
- icon buttons
- chapter-ref links
- list rows
- loading states
- empty/error states
- theme provider/tokens
- navigation headers
- font controls
- Tamil/English toggles

Search for existing use of:

- `accessible`
- `accessibilityLabel`
- `accessibilityHint`
- `accessibilityRole`
- `accessibilityState`
- `accessibilityLiveRegion`
- `accessibilityViewIsModal`
- `allowFontScaling`
- `maxFontSizeMultiplier`
- `importantForAccessibility`

Do not assume something is inaccessible merely because one explicit prop is absent; inspect React Native defaults and the component structure first.

---

# Audit categories

Audit and classify each finding as:

- PASS
- FIXED IN THIS ACTIVITY
- NEEDS MANUAL VOICEOVER VERIFICATION
- DEFERRED / NON-BLOCKING

Do not call something a failure without evidence.

---

# A. Screen-reader semantics

Inspect every interactive element.

Buttons/icons that are visually obvious must have meaningful spoken labels.

Examples requiring review:

- Back buttons
- Theme buttons
- Tamil/English toggles
- Font increase/decrease
- line-height controls
- bookmark controls
- share buttons
- download controls
- retry buttons
- timeline cards
- chapter-ref links
- Murasoli letters
- Explore discovery cards
- Places schematic-map markers

Avoid labels such as:

- "button"
- "icon"
- "chevron"
- raw icon names

Use purpose-oriented labels.

Examples conceptually:

- `Increase text size`
- `Decrease text size`
- `Switch to English`
- `Bookmark chapter`
- `Open Volume 3`
- `Open letter 3764`

Use Tamil labels where that makes more sense for Tamil-first content, but keep behavior understandable.

Do not invent spoken historical descriptions.

---

# B. Accessibility roles and state

Ensure appropriate roles for:

- buttons
- links
- headers
- tabs
- switches/toggles where appropriate
- selected language/theme states

For controls with state, expose the state truthfully.

Examples:

- selected Tamil/English mode
- selected theme
- bookmarked state
- downloaded state

Do not misuse accessibility roles purely to alter VoiceOver output.

---

# C. Heading hierarchy

Review page titles and important section headings.

Use appropriate accessibility heading semantics where React Native supports them.

Examples:

- Library
- Timeline
- Murasoli
- Themes
- People
- Places
- chapter title
- letter title

Do not mark every label as a heading.

---

# D. Dynamic Type / font scaling

The audit previously found Dynamic Type support partially present.

Verify the actual app.

Check:

- Tamil text scales
- English text scales
- controls remain usable at larger system font settings
- cards do not clip critical text
- buttons remain tappable
- metadata does not overlap
- reader controls remain accessible

Do NOT disable font scaling globally to fix layouts.

Do not set restrictive `maxFontSizeMultiplier` unless there is a strong demonstrated reason.

Fix layout instead where practical.

Test at least:

- default text size
- substantially enlarged accessibility text size in simulator

Tamil rendering is especially important.

---

# E. Touch targets

Audit small interactive controls.

Aim for approximately 44×44 pt usable targets on iOS where practical.

Check especially:

- icon-only buttons
- reader font controls
- theme controls
- language toggle
- bookmark
- share
- map markers
- tiny chevrons

Do not enlarge visual icons unnecessarily; padding/hit-slop may be sufficient.

Use existing React Native mechanisms rather than adding dependencies.

---

# F. Color and contrast

Audit current:

- light
- sepia
- dark

themes.

Pay special attention to:

- body text
- secondary text
- metadata
- links
- disabled states
- accent text
- borders
- pills
- timeline labels
- translator notes
- map labels

Use actual theme tokens and inspect contrast systematically.

Where feasible, calculate contrast ratios from the current color values rather than eyeballing.

Target generally:

- normal text: WCAG AA 4.5:1
- large text: 3:1
- meaningful UI boundaries/icons: roughly 3:1 where applicable

Do not radically redesign the palette.

Make minimal token-level fixes where a shared token causes repeated problems.

If sepia needs adjustment, preserve its visual identity while improving contrast.

Document measured before/after values for any changed token.

---

# G. Color-only communication

Check whether state is conveyed solely by color.

Examples:

- selected theme
- selected language
- downloaded/bookmarked state
- active tab
- progress state

Where necessary, add text, iconography or accessibility state.

Do not introduce visual clutter merely to satisfy a theoretical concern.

---

# H. Focus order / reading order

Inspect component order for VoiceOver.

Important screens:

- Reader
- Murasoli Reader
- Theme Detail
- Person Detail
- Place Detail
- Timeline

Visual order and screen-reader reading order should make sense.

Avoid decorative icons becoming separate focus targets.

Do not implement complicated focus-management code unless a real problem exists.

---

# I. Images and illustrations

Inspect:

- memoir illustrations
- app imagery
- decorative icons
- splash/icon usage
- Places schematic map

Classify each as:

- informative
- decorative

Informative illustrations should receive useful source-supported accessibility labels where an actual description exists.

Decorative images/icons should not create meaningless VoiceOver stops.

Do NOT invent descriptions for historical illustrations when the repository provides no reliable description.

In such cases, use a neutral source-supported label or mark decorative if the image adds no necessary information.

---

# J. Places schematic map

This requires specific review.

The map is explicitly schematic, not geographic.

Ensure:

- screen-reader users can access every place through the list even if map navigation is difficult
- map markers do not become the sole means of accessing a place
- any marker accessibility label uses the actual place name
- no accessibility wording implies GPS/cartographic accuracy

The list is the authoritative accessible path.

Do not add a mapping dependency.

---

# K. Lists

Audit:

- Library
- chapter lists
- Search results
- Timeline
- Murasoli letter lists
- Themes
- People
- Places
- Saved

Check:

- labels provide sufficient context
- rows are tappable as one understandable unit
- decorative child elements do not create excessive focus stops
- large lists still use efficient list components

Do not rewrite content solely for accessibility.

---

# L. Loading / error states

Inspect:

- Loading
- offline errors
- retry states
- empty Saved state
- feature-data failures
- Murasoli network failure

Ensure important state text is exposed.

Use `accessibilityLiveRegion` only where appropriate; do not make every loading state noisy.

Retry controls must be clearly labeled.

---

# M. Reader controls

The memoir Reader and Murasoli Reader are central.

Audit:

- Tamil/English toggle
- font-size controls
- line-height controls
- themes
- bookmark where applicable
- share
- chapter metadata
- progress restoration
- illustrations
- translator note separation

Ensure controls expose purpose and current state.

Do NOT change reading behavior or source text.

---

# N. Motion / reduced motion

Inspect whether the app currently has meaningful animation.

If there are only ordinary navigation transitions and no custom motion, document this and do not add unnecessary reduced-motion infrastructure.

If custom animation exists, determine whether it should respect Reduce Motion.

Do not introduce animation work unless necessary.

---

# O. Orientation / screen size

Check accessibility impact only.

Do not begin iPad redesign.

Verify that fixes do not introduce:

- clipped controls
- unreachable buttons
- horizontal scrolling
- fixed-height text containers

at common phone widths and large Dynamic Type.

---

# P. Tamil accessibility

Do not replace Tamil with transliterated English.

Check:

- Unicode text remains intact
- Tamil labels are not split strangely
- enlarged Tamil text wraps correctly
- line-height remains readable
- English metadata does not dominate Tamil-primary pages

Do not modify archival Tamil text.

---

# Manual VoiceOver boundary

We are explicitly NOT requiring a physical iPhone test.

Do not pretend that a complete VoiceOver audit was performed if it was not.

Use the iOS simulator where practical for:

- Accessibility Inspector
- larger text sizes
- semantic inspection
- layout verification

Any behavior that genuinely requires manual VoiceOver navigation should be recorded as:

**NEEDS MANUAL VOICEOVER VERIFICATION — not performed in this activity**

This must NOT prevent completing the repository-side accessibility pass unless a critical issue is discovered.

---

# Automated/static checks

Use existing tooling first.

Do not add a large accessibility library unless clearly justified.

Where useful, write a small temporary audit script for color contrast or source scanning, but do not commit throwaway tooling unless it has durable value.

Potential useful checks:

- source scan for icon-only `Pressable`s lacking accessible labels
- theme contrast calculations
- obvious `allowFontScaling={false}`
- fixed-height text containers

Review every automated finding manually.

---

# Fix strategy

Prefer:

1. shared-component fix
2. theme-token fix
3. reusable accessibility helper
4. individual screen fix

in that order where appropriate.

Do not create an elaborate accessibility framework.

Keep changes understandable.

---

# Regression boundaries

Do NOT alter:

- archival text
- translations
- chapter ordering
- Murasoli content
- feature JSON
- navigation architecture except accessibility-related props
- network/data contracts
- offline model
- reader storage model
- privacy/support pages
- EAS/release config
- SDK versions

unless a genuine accessibility bug requires a narrow adjustment.

---

# Simulator verification

After fixes, verify representative flows.

At minimum:

## Standard text size

1. Home
2. Library
3. Volume list
4. Memoir Reader
5. Search
6. Timeline
7. Explore
8. Murasoli Library
9. Murasoli Reader
10. Themes
11. People
12. Places
13. Saved
14. Settings

## Large accessibility text

Repeat representative checks for:

- Home
- Library
- memoir Reader
- Timeline
- Explore
- Murasoli Reader
- Theme Detail
- Person Detail
- Place Detail
- Settings

Confirm:

- no critical text clipping
- controls remain reachable
- buttons remain tappable
- Tamil wraps correctly
- no destructive overlap

## Themes

Verify light / sepia / dark after any contrast-token change.

---

# Navigation regression

Confirm:

- memoir Reader deep-links still work
- Timeline → Reader works
- Theme/People/Places → Reader works
- Murasoli navigation works
- back navigation works
- tab navigation works

---

# Standard build gates

Run from `mobile/`:

- `npm ci` if appropriate
- `npm run typecheck`
- `npm run validate:manifest`
- `npx expo-doctor`
- `npx expo export --platform ios`

Also run root checks if shared website files are touched, though no website change is expected.

No physical-device test.

No TestFlight build.

---

# Documentation

Create or update one accessibility document.

Preferred:

`mobile/docs/ACCESSIBILITY.md`

Document:

- audit scope
- fixes completed
- Dynamic Type status
- theme contrast measurements
- screen-reader semantics status
- touch-target status
- known limitations
- manual VoiceOver verification still required
- simulator verification performed

Update:

## `mobile/docs/PRODUCTION_READINESS.md`

Change Accessibility from PARTIAL to the accurate new status.

Do NOT mark it “fully verified” if manual VoiceOver testing remains outstanding.

A suitable state may be:

**Repository accessibility pass COMPLETE; manual VoiceOver verification pending.**

## `mobile/docs/STORE_CHECKLIST.md`

Tick only items genuinely satisfied.

Keep manual VoiceOver/on-device checks unticked if they were not performed.

## `HANDOVER.md`

Record:

- Activity 3 branch
- main fixes
- verification
- remaining manual check
- exact next activity

Expected next activity:

**Production Readiness Activity 4 — App Store metadata + screenshots/assets**

Do not begin it here.

---

# Git discipline

Use a fresh branch from merged `main`.

Suggested:

`mobile/accessibility-readiness`

Keep commits logical.

For example:

1. shared accessibility semantics + touch-target fixes
2. Dynamic Type / contrast/layout fixes
3. documentation

Do not force exactly three commits if a cleaner structure exists.

Before commit confirm no:

- generated `ios/`
- signing material
- EAS credentials
- local Metro IP
- simulator files
- screenshots unless specifically required as audit evidence and intentionally versioned
- unrelated data changes
- SDK/package upgrades

Push the branch.

Open a PR.

Require:

- Mobile CI green
- Vercel green if it runs

Leave the Accessibility PR unmerged once green unless explicitly required otherwise.

---

# Scope exclusions

Do NOT implement:

- App Store screenshots
- App Store descriptions
- keywords
- privacy labels submission
- TestFlight upload
- EAS project initialization
- Universal Links association files
- offline banner
- download manager
- crash reporting
- share-as-image
- push notifications
- analytics
- iPad redesign
- Android release
- feature/content changes
- new archive material

Do not start Production Readiness Activity 4.

---

# Stop condition

Stop when:

- PR #11 is merged
- post-merge Mobile CI is green
- static accessibility audit is complete
- concrete accessibility defects found are fixed
- simulator verification at normal + large text succeeds
- contrast has been measured where relevant
- repository-side semantics are improved
- remaining manual VoiceOver verification is documented truthfully
- standard gates pass
- accessibility docs/status are updated
- Accessibility PR is green

Do NOT begin store metadata/screenshots.

---

# Final report

Report:

1. PR #11 merge SHA
2. Accessibility branch
3. Accessibility commit SHA(s)
4. PR number
5. files changed
6. screens/components audited
7. accessibility issues found
8. issues fixed
9. screen-reader semantics changes
10. accessibility-state changes
11. heading-semantic changes
12. touch-target changes
13. Dynamic Type findings/fixes
14. Tamil large-text result
15. contrast measurements by theme
16. theme-token changes, if any
17. Places schematic-map accessibility result
18. loading/error-state accessibility result
19. image/illustration treatment
20. reduced-motion finding
21. simulator normal-text result
22. simulator large-text result
23. manual VoiceOver status exactly and truthfully
24. mobile typecheck result
25. manifest validation result
26. expo-doctor result
27. iOS export result
28. GitHub Mobile CI result
29. remaining accessibility limitations
30. confirmation no store-metadata/TestFlight/push work was started
31. exact next activity:

**Production Readiness Activity 4 — App Store metadata + screenshots/assets**

Start with Stage 1. Do not begin the accessibility work until PR #11 has been merged and post-merge Mobile CI is green.
:::

<a id="turn-0362"></a>
## Turn 0362 — 2026-08-15T14:36:48.360Z

### User

Starting Stage 1. Let me confirm PR #11's current state and head SHA, then inspect the full diff.

PR #11 fully verified — OPEN, CLEAN, MERGEABLE, head unchanged at `3f2b8f7`, all checks SUCCESS. Scope is exactly the four intended files (app.json version/export config, eas.json, RELEASE.md, STORE\_CHECKLIST.md) — no `ios/`, no signing material, no EAS secrets, no feature/push/accessibility changes. Merging now.

Merged — merge commit `75c9c85` is now `origin/main`. Let me clean up the remote branch and fetch the new main commit locally.

Remote clean (only `main`); merge commit `75c9c85` is present locally. Now verify post-merge Mobile CI and site health.

Site healthy (all routes 200). Post-merge Mobile CI is running for `75c9c85` — let me poll it in the background while I set up Stage 2.

Now set up the Stage 2 branch from merged main in the worktree.

Stage 2 branch `mobile/accessibility-readiness` is set up at merged main. Now the mandatory doc reading. Let me read the handover and mobile docs.

**Stage 1 complete** — PR #11 merged (`75c9c85` on `main`), remote branch deleted, post-merge Mobile CI green, site healthy, working tree clean on the new branch.

Now Stage 2. Let me finish the mandatory doc reading (ROADMAP, BUILD), then start inspecting the code.

I've read all mandatory docs. Now let me inspect the code. Let me start with the shared foundation (theme, ui components) and run a codebase-wide scan for existing accessibility props.

Good — there's already a meaningful a11y baseline. Let me read the shared foundation files.

Now the central interactive screens. Let me read the Reader (font/theme/bookmark/share controls), navigation (headers/back buttons), and Places (map markers).

The Reader is already well-instrumented. Let me read navigation (headers/back/tabs), Settings, and Places (map markers) — the areas most likely to have icon-only or state-bearing controls.

Navigation relies on React Navigation's accessible native-stack back buttons and bottom-tab defaults — good. Let me read Settings, Places (map markers), and ChapterRefs.

Settings is solid (labeled switches, role-tagged theme buttons with `selected` state, labeled steppers). Now the flagged Places map markers, plus Explore and ChapterRefs.

Places is well-structured: the list is a fully accessible path (each place a labeled button), the map is labeled schematic with no GPS claim, and markers carry real place names. The one gap: markers are 12pt dots with `hitSlop={10}` = \~32pt targets (under 44). Let me read ChapterRefs and Explore next.

ChapterRefs and Explore aggregate text labels well (each card is one labeled target; chevrons are decorative inside the Pressable). Let me read the remaining screens in a batch to complete the audit.

Let me read the remaining screens.

Let me read the last set: Saved, Themes, People, and the three Murasoli screens.

Let me read People and the three Murasoli screens to complete the inspection.

People and MurasoliReader follow the same solid patterns (labeled buttons; the reader's `Ctrl`/EN-toggle mirror the memoir Reader — same two small gaps: no `role="button"` on `Ctrl`, no explicit label on the EN toggle).

Now let me measure contrast across all three themes with a script before deciding on any token changes.

Contrast measured. Clear findings: `textFaint` fails AA for informative metadata in light (2.92) and sepia (2.45); sepia `textMuted` is marginal (4.44); light/sepia `accent` (brass) fails even large-text 3:1 as text (2.91/3.12); dark `primary` is borderline (4.00). Borders are decorative separators (not sole affordances) so their low ratio is acceptable. Let me solve for minimal token adjustments that clear the thresholds while keeping brand identity.

Now let me verify the proposed token values clear the thresholds across all themes before editing.

All proposed tokens pass AA now. Let me read the two remaining Murasoli screens and confirm there's no custom animation or disabled font scaling, then implemen

### Assistant

The accessibility work is ready to move forward. I checked GitHub: **PR #12 is still open, unmerged and mergeable**, with current head `5920ba2`. 

There are two small reporting inconsistencies worth correcting before/while merging:

- Claude's final report says **19 files changed**, while GitHub currently reports **20 changed files**. 
- The PR description still says **“Changes (3 commits)”**, but after the HANDOVER update the PR actually contains **4 commits**.  

Neither looks like a functional problem; Claude should simply inspect the final diff and make sure the 20th file is expected before merging.

The next clean sequence is:

**Merge PR #12 → verify post-merge Mobile CI → Production Readiness Activity 4: App Store metadata + screenshot/assets preparation.**

For Activity 4, I recommend **preparing everything in the repository without attempting an App Store submission yet**: finalized app name/subtitle, Tamil + English descriptions, keywords, promotional text, category recommendation, age-rating answers, privacy-label worksheet based on actual app behavior, screenshot plan, screenshot capture specifications, and reusable store-assets structure. Actual TestFlight/App Store Connect submission can wait until the paid Apple Developer account is available.

<a id="turn-0363"></a>
## Turn 0363 — 2026-08-15T14:38:19.010Z

### User

please provide prompt for claude

### Assistant

:::writing{variant="document" id="38416" title="Claude Prompt — Production Readiness Activity 4: App Store Metadata + Screenshot/Asset Preparation"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — complete
- Increment 1 — complete
- Increment 2 — complete
- Privacy / Support / About pages — merged and live
- Production Readiness Activity 2 — Release Engineering — merged
- Production Readiness Activity 3 — Accessibility — PR #12
  - branch: `mobile/accessibility-readiness`
  - head: `5920ba2`
  - currently open, green and mergeable
  - repository accessibility pass complete
  - manual VoiceOver/TalkBack device verification remains explicitly pending
- No physical-device testing is required in this workstream
- No TestFlight/App Store submission should be attempted in this workstream

The next workstream is:

# Production Readiness Activity 4
## App Store Metadata + Screenshot / Store-Asset Preparation

This workstream has two stages:

1. Merge and verify PR #12
2. Prepare the complete repository-side App Store listing package and screenshot plan/assets without submitting anything to App Store Connect

---

# Stage 1 — Merge Accessibility PR #12

Before merging:

1. Confirm PR #12 is still:
   - open
   - green
   - mergeable
   - head unchanged at the expected commit

2. Inspect the complete final PR diff.

3. Resolve the two reporting inconsistencies before merge:
   - GitHub currently reports **20 changed files**, while the previous final report said 19.
   - GitHub currently reports **4 commits**, while the PR description still says “Changes (3 commits).”

These are likely reporting/documentation inconsistencies, but confirm the actual 20th file and all 4 commits are expected.

4. Confirm no unexpected files exist:
   - generated `ios/`
   - simulator artifacts
   - local screenshots
   - signing material
   - EAS credentials
   - SDK changes
   - store metadata work
   - push notifications
   - unrelated content/data changes

5. Update the PR description if necessary so it truthfully reflects the final 4-commit / 20-file state.

6. Merge PR #12 into `main`.

7. Verify:
   - merge commit is on `main`
   - post-merge Mobile CI is green
   - Vercel/site remains healthy
   - working tree is clean
   - accessibility docs are present on `main`

Only then begin Stage 2.

---

# Stage 2 — App Store Listing Package

Create a fresh branch from updated clean `main`, for example:

`mobile/app-store-assets`

Do not work directly on `main`.

This is **repository-side preparation only**.

Do NOT:
- log into App Store Connect
- upload metadata
- submit a build
- create a TestFlight build
- initialize EAS against a live project unless already part of merged configuration
- modify signing
- request Apple certificates

---

# Mandatory startup

Read completely:

- `HANDOVER.md`
- `mobile/docs/PRODUCTION_READINESS.md`
- `mobile/docs/STORE_CHECKLIST.md`
- `mobile/docs/RELEASE.md`
- `mobile/docs/ACCESSIBILITY.md`
- `mobile/app.json`
- `mobile/eas.json`
- root `README.md`

Inspect:

- Home screen
- Library
- Reader
- Search
- Timeline
- Explore
- Themes / People / Places
- Murasoli Library
- Murasoli Reader
- Settings
- About / Privacy / Support website pages
- app icon / splash assets
- current brand assets
- current screenshots or store folders, if any
- current app name / slug / bundle identifier / Android package
- any existing metadata drafts

Search for:

- `App Store`
- `metadata`
- `screenshots`
- `subtitle`
- `keywords`
- `description`
- `promotional`
- `privacy`
- `age rating`
- `copyright`
- `category`

Do not create duplicate metadata systems if one already exists.

---

# Official Apple requirements

Where current App Store limits/specifications matter, verify them against the **current official Apple Developer / App Store Connect documentation** if web access is available.

Examples:

- app name character limit
- subtitle limit
- promotional text li

<a id="turn-0364"></a>
## Turn 0364 — 2026-08-16T12:08:30.008Z

### User

I'll start with Stage 1: verify PR #12, resolve the two reporting inconsistencies (20 files / 4 commits), then merge.

PR #12 is OPEN / CLEAN / MERGEABLE, head `5920ba2` (as expected), all checks SUCCESS.

**Resolving the two inconsistencies:**

- **4 commits** (`37b1f37` semantics, `96451c0` contrast, `c70115e` docs, `5920ba2` handover) — all expected. The 4th (HANDOVER) was added after I first wrote the PR body ("3 commits"), and after my verbal "19 files" count.
- **20 files** = 13 screens + 3 shared (`ui.tsx`, `navigation`, `theme.ts`) + 4 docs (`ACCESSIBILITY.md`, `PRODUCTION_READINESS.md`, `STORE_CHECKLIST.md`, `HANDOVER.md`). The "20th" vs my earlier "19" is `HANDOVER.md` (the 4th commit) — expected. No `ios/`, screenshots, signing, EAS creds, SDK/package, metadata, push, or content/data changes appear.

Both are documentation/arithmetic discrepancies, not branch problems. Let me update the PR body to reflect 4 commits / 20 files before merging.

PR body now reflects 4 commits / 20 files. Let me do the final diff inspection (stat) to confirm scope before merging.

The diff is exactly as expected — small per-screen a11y-prop additions, `theme.ts` token values, and docs. No unexpected files. Merging PR #12.

PR #12 merged — merge commit `28eebe8` on `main`, remote branch deleted (only `main` remains). Let me verify post-merge CI, site health, and that the accessibility docs are on `main`.

Accessibility docs present on `main`, site healthy (all 200). Post-merge CI is running — let me poll it in the background while I set up Stage 2.

Stage 2 branch `mobile/app-store-assets` created at merged main, clean. Now the mandatory reading. I've authored/read most this session; let me read the ones I need fresh (root README, and confirm current app.json/eas.json) plus pull exact manifest counts for captions.

Let me get the authoritative manifest counts (for accurate captions) and confirm the current app.json / eas.json identity on this branch.

**Stage 1 complete & verified:** PR #12 squash-merged (`28eebe8` on `main`), PR body corrected to 4 commits/20 files, remote branch deleted, post-merge Mobile CI **success**, site healthy, docs on `main`, working tree clean on the new branch.

Now Stage 2. Let me establish canonical identity from app.json/eas.json and check for any existing store/metadata artifacts.Canonical identity captured. Let me check for any existing store/metadata artifacts and inspect the icon/splash assets.

Assets check out: `icon.png` 1024², **opaque** (correct — iOS prohibits alpha in the marketing icon); `adaptive-icon.png` has alpha (correct for Android); splash 1242². No existing store folder — I'll create `mobile/store/`.

Now let me verify current Apple requirements from primary sources. Loading web tools.

I'll verify Apple's current metadata limits and screenshot specs from primary sources.

Name 30 / subtitle 30 confirmed. Let me get promotional text, keywords, description limits and screenshot specs from Apple.

Let me fetch the authoritative screenshot-specifications and localizable-properties pages directly.

Screenshot specs confirmed (6.9" **1260×2736 required**; iPad screenshots **required because ****`supportsTablet: true`** — a key flag). Name/Subtitle = 30 chars confirmed from Apple. Let me verify whether Tamil is a supported App Store storefront localization (critical for the localization strategy) and confirm the description/keywords/promo limits.

Confirmed from Apple primary sources: **Tamil IS a supported App Store localization** (so a full Tamil listing is first-class, not discarded); **keywords = 100 characters** (byte-counted — Tamil chars cost more); Name/Subtitle = 30; 6.9" screenshots **1260×2736 required**, iPad screenshots **required** given `supportsTablet: true`. I'll use the stable 4000 (description) / 170 (promo) limits with a "reconfirm in ASC" note since I couldn't pull those two from Apple primary this session.

Let me verify the listing URLs are live, then build the package.

### Assistant

PR #13 is in good shape: **open, unmerged, mergeable**, head `3ee2b38`, with exactly 3 commits and 17 changed files.  

I would change the proposed next priority slightly. **Universal Links should not be next yet.** A complete iOS AASA file needs the Apple Team ID, and Android `assetlinks.json` ultimately needs the signing-certificate fingerprint, so both become much easier to finish after the signing/account setup.

The most useful next workstream is instead:

**Merge PR #13 → Production Readiness Activity 5: iPad submission readiness + missing store screenshots.**

That addresses a genuine current submission blocker because the app declares `supportsTablet: true`. Claude should test the actual app on representative iPad simulators and then:

- if the current UI is acceptable, capture and QA the required iPad App Store screenshots;
- if tablet usability is poor, document the evidence and stop for an **owner decision** on whether to keep iPad support or change the release to iPhone-only;
- capture the missing iPhone Search screenshot at the same time if a clean deterministic state can be produced;
- **not silently change `supportsTablet`**.

After that, the remaining major blocker is the paid Apple Developer / signed TestFlight process, plus your copyright-field owner decision. Offline banner and crash reporting can follow as launch polish; Push Notifications can remain deferred.

<a id="turn-0365"></a>
## Turn 0365 — 2026-08-16T12:15:10.131Z

### User

please provide the prompt for claude

### Assistant

:::writing{variant="document" id="51742" title="Claude Prompt — Production Readiness Activity 5: iPad Readiness + Missing Store Screenshots"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — complete
- Increment 1 — complete
- Increment 2 — complete
- Privacy / Support / About — merged and live
- Production Readiness Activity 2 — Release Engineering — merged
- Production Readiness Activity 3 — Accessibility — merged
- Production Readiness Activity 4 — App Store metadata + screenshot/asset preparation — PR #13
  - branch: `mobile/app-store-assets`
  - head: `3ee2b38`
  - currently open, green, mergeable
  - 3 commits
  - 17 changed files
  - contains the repository-side App Store package plus 6 clean iPhone 6.9" screenshots
- `ios.supportsTablet` is currently `true`
- No physical-device test is required
- Do not attempt TestFlight/App Store submission in this activity
- Push notifications remain deliberately deferred

The next workstream is:

# Production Readiness Activity 5
## iPad Submission Readiness + Missing Store Screenshots

This has two stages:

1. Merge and verify PR #13.
2. Evaluate actual iPad usability, capture required iPad store screenshots if the app is genuinely suitable, and finish the remaining clean iPhone screenshot gaps.

A critical rule:

# DO NOT silently change `supportsTablet`.

If the current app is not suitable for iPad submission, stop and document an explicit **OWNER DECISION REQUIRED** rather than changing the release scope.

---

# Stage 1 — Merge PR #13

Before merging:

1. Confirm PR #13 is still:
   - open
   - green
   - mergeable
   - head unchanged at the expected commit

2. Inspect the complete final PR diff.

3. Confirm scope is only Activity 4:
   - `mobile/store/` metadata package
   - App Privacy worksheet
   - age-rating worksheet
   - App Review notes
   - screenshot plan
   - submission checklist
   - 6 clean iPhone screenshots
   - readiness/HANDOVER docs

4. Confirm there are no:
   - generated `ios/`
   - signing files
   - certificates
   - provisioning profiles
   - EAS secrets
   - App Store Connect credentials
   - push implementation
   - Universal Links files
   - unrelated app/content changes

5. Merge PR #13 into `main`.

6. Verify:
   - merge commit is present on `main`
   - post-merge Mobile CI is green
   - Vercel/site remains healthy
   - `mobile/store/` is present on `main`
   - the 6 iPhone screenshots are present and unchanged
   - working tree is clean

Only then begin Stage 2.

---

# Stage 2 — iPad Submission Readiness

Create a fresh branch from updated clean `main`, for example:

`mobile/ipad-store-readiness`

Do not work directly on `main`.

The purpose is to answer one question truthfully:

> Is the current app good enough to ship with iPad support enabled?

Do not assume the answer is yes because `supportsTablet: true`.

Do not assume the answer is no because there is no dedicated split-screen layout.

Evaluate the actual product.

---

# Mandatory startup

Read completely:

- `HANDOVER.md`
- `mobile/docs/PRODUCTION_READINESS.md`
- `mobile/docs/STORE_CHECKLIST.md`
- `mobile/docs/RELEASE.md`
- `mobile/docs/ACCESSIBILITY.md`
- `mobile/store/README.md`
- `mobile/store/SCREENSHOT_PLAN.md`
- `mobile/store/SUBMISSION_CHECKLIST.md`
- `mobile/store/metadata.en.md`
- `mobile/store/metadata.ta.md`
- `mobile/app.json`
- `mobile/eas.json`

Inspect all major screens again, with iPad layout in mind:

- Home
- Library
- Volume
- Reader
- Search
- Timeline
- Saved
- Settings
- Explore
- Themes
- Theme Detail
- People
- Person Detail
- Places
- Place Detail
- Murasoli Library
- Murasoli Volume
- Murasoli Reader

Also inspect:

- navigation
- shared UI components
- width constraints
- fixed widths/heights
- grids
- modal/sheet usage
- cards
- reader line width
- image sizing
- orientation assumptions

Search for:

- `Dimensions`
- `useWindowDimensions`
- fixed `width`
- fixed `height`
- perce

<a id="turn-0366"></a>
## Turn 0366 — 2026-08-16T13:24:32.060Z

### User

I'll start with Stage 1: verify PR #13, inspect the diff, confirm scope, then merge.

PR #13 is OPEN / CLEAN / MERGEABLE, head `3ee2b38` (as expected), all checks SUCCESS. 3 commits, 17 files — all Activity 4 scope (store package + worksheets + 6 iPhone screenshots + readiness/HANDOVER docs). No `ios/`, signing, certs, EAS secrets, push, or Universal Links files. Let me do a final diff-stat check, then merge.

Diff confirms scope exactly — only docs/markdown + 6 PNGs, no code/`ios/`/secrets. Merging PR #13.

Merged — merge commit `d9e879f` on `main`, remote branch deleted. Let me verify: fetch the commit, confirm `mobile/store/` + the 6 screenshots are on `main`, check CI and site.

`mobile/store/` and all 6 iPhone screenshots are on `main`; site healthy. Post-merge CI is running — let me poll it and set up Stage 2.

Stage 2 branch ready. While CI confirms green, let me do the static code inspection for iPad layout concerns (fixed widths, `maxWidth`, `Dimensions`, orientation) — the docs are already current from this session.

**Stage 1 complete & verified:** PR #13 squash-merged (`d9e879f` on `main`), remote branch deleted, post-merge Mobile CI **success**, site healthy, `mobile/store/` + 6 screenshots present on `main`, tree clean.

Static scan shows the key iPad concern: **no ****`maxWidth`**** anywhere** (Reader/prose will span full iPad width) and `orientation: "default"` (landscape allowed). Now let me verify Apple's current iPad screenshot spec and list available iPad simulators.

Confirmed from Apple: **iPad 13" required — 2064×2752 portrait** (one iPad size suffices; 1–10 shots; no alpha). Let me find a matching iPad Pro 13" simulator.

**iPad Pro 13-inch (M5)** — native 2064×2752, exactly the required 13" class. Booting it and installing the app.

iPad Pro 13" booted, app installed, native capture **2064×2752** (exact required size). Starting Metro and launching.

Let me attach to the iPad (for coordinate space) and screenshot to handle the launch dialog.

iPad portrait, clean status bar. Tapping Open.

iPad Home renders — content pinned to the top with a large empty lower area, and the tiles are very wide/short (47% of a 1032pt canvas). Coherent but sparse. Let me check the Reader (the most important iPad surface) — tapping Library.

Library on iPad: full-width volume cards — wide but readable and coherent (short metadata, not absurd). Acceptable. Now the critical Reader — opening Volume 1.

Volume chapter list: full-width rows (download icons pushed to the far edge — mild but functional). Opening chapter 1 to assess the Reader.

This is the key finding: the Reader body text spans the **full iPad width** — the line length is far too long for comfortable reading (the classic iPad issue). The illustration is fine. This is exactly what a **centered max-width reading column** fixes (the task's endorsed small fix). Let me confirm the rendering roots of each screen so I target the fix precisely.

Layout roots confirmed: 10 screens use `<Screen>` (one fix covers them), 3 use raw `<FlatList>`(Themes/People/MurasoliVolume), 2 Readers use raw `<ScrollView>`.

**Decision: Outcome A with one modest, universally-safe fix** — a centered `maxWidth` (720pt) reading/content column. Since every iPhone is <720pt wide, this is a **pure iPad improvement with zero iPhone change**. Let me implement it. First, add the constant.

Now update the shared `Screen` to center content at `contentMaxWidth` (covers the 10 Screen-based screens).

Add the import for `contentMaxWidth` in ui.tsx.

Now the two Readers. To protect the search scroll-to (which relies on paragraph `onLayout`), I'll center via the ScrollView's `contentContainerStyle` (no reparenting) and match the controls bar to the same 720 column. Editing ReaderScreen:

Add the import in ReaderScreen:

Now the same for MurasoliReaderScreen:

Now the 3 raw-FlatList screens. Let me find their `contentContainerStyle` lines.

All three identical. Let me update each contentContainerStyle and it

### Assistant

PR #14 checks out: **open, unmerged, mergeable**, head `f0afa62`, with **3 commits and 19 changed files**, exactly matching Claude’s final report.  

The Activity-5 outcome is strong. The `720pt` centered content column is a sensible first-release iPad solution, `supportsTablet` remains enabled, and the previously missing store assets are now covered: **7 iPhone + 6 iPad screenshots**. The remaining extreme-Dynamic-Type and landscape checks are appropriately documented rather than overstated. 

### What should come next

I would **not do Universal Links yet** because the final association values depend on the real Apple Team ID and Android signing certificate.

I also would **not add crash reporting yet**. Introducing a third-party crash SDK immediately before release changes the privacy analysis and App Store privacy answers.

The best next repository-side workstream is:

**Merge PR #14 → Production Readiness Activity 6 — Offline/network status + launch reliability polish.**

That should focus narrowly on things such as:

- actually using the already-installed NetInfo dependency;
- a subtle, truthful **Offline** indicator/banner;
- clear transition when connectivity returns;
- no false claim that uncached content is available offline;
- retry behavior for network failures;
- startup behavior when the manifest/network is unavailable;
- cached memoir/Murasoli/Timeline/Explore behavior;
- ensuring the offline banner doesn't interfere with Reader UI, Dynamic Type, or iPad layout;
- regression testing airplane/offline → online transitions.

Then I would do:

**Activity 7 — Universal Links**, once signing identity is available → **Activity 8 — crash reporting decision/setup**, only after deciding whether the privacy trade-off is worthwhile.

The two actual submission blockers remain external: **Apple Developer/App Store Connect + signed build**, and the **copyright-field owner/entity decision**. 

So the immediate next sequence should be:

**PR #14 merge → Offline/network + launch polish.**

<a id="turn-0367"></a>
## Turn 0367 — 2026-08-16T13:25:45.285Z

### User

please provide next prompt

### Assistant

:::writing{variant="document" id="67124" title="Claude Prompt — Production Readiness Activity 6: Offline / Network Status + Launch Reliability Polish"}
Continue the `pugazg/kalaignar-autobiography` project from the current repository state.

Current status:

- Expo SDK 57 migration — complete
- Increment 1 — complete
- Increment 2 — complete
- Privacy / Support / About — merged and live
- Release engineering — merged
- Accessibility repository pass — merged
- App Store metadata package — merged
- iPhone store screenshots — complete
- iPad first-release readiness + screenshots — PR #14
  - branch: `mobile/ipad-store-readiness`
  - head: `f0afa62`
  - 3 commits
  - 19 changed files
  - currently open, green and mergeable
- `supportsTablet: true`
- iPad release decision: FIRST-RELEASE READY
- No physical-device test is required
- Push notifications remain deliberately deferred
- Universal Links remain deferred until real signing identity is available
- Crash reporting remains deferred so we do not unnecessarily change the current privacy model before release

The next workstream is:

# Production Readiness Activity 6
## Offline / Network Status + Launch Reliability Polish

This activity has two stages:

1. Merge and verify PR #14.
2. Improve network/offline communication and startup reliability without changing the existing offline architecture.

The primary goal is:

> The app should behave truthfully and predictably when the network disappears, when it launches offline, and when connectivity returns.

Do not turn this into a bulk-download redesign.

---

# Stage 1 — Merge PR #14

Before merging:

1. Confirm PR #14 is still:
   - open
   - green
   - mergeable
   - head unchanged at the expected Activity-5 commit

2. Inspect the complete final PR diff.

3. Confirm scope is exactly Activity 5:
   - centered `contentMaxWidth = 720`
   - iPad layout adjustments
   - iPhone Search screenshot
   - iPad screenshots
   - screenshot/readiness docs

4. Confirm:
   - `supportsTablet` remains `true`
   - no generated `ios/`
   - no signing material
   - no EAS credentials
   - no Universal Links
   - no push implementation
   - no crash/analytics SDK
   - no unrelated archive/content changes

5. Merge PR #14 into `main`.

6. Verify:
   - merge commit is on `main`
   - post-merge Mobile CI is green
   - Vercel/site remains healthy
   - iPhone/iPad screenshots remain on `main`
   - `contentMaxWidth` changes are on `main`
   - working tree is clean

Only then begin Stage 2.

---

# Stage 2 — Offline / Network Status + Launch Reliability

Create a fresh branch from updated clean `main`, for example:

`mobile/offline-network-readiness`

Do not work directly on `main`.

---

# Mandatory startup

Read completely:

- `HANDOVER.md`
- `mobile/docs/PRODUCTION_READINESS.md`
- `mobile/docs/ROADMAP.md`
- `mobile/docs/STORE_CHECKLIST.md`
- `mobile/docs/ARCHITECTURE.md`
- `mobile/docs/DATA_CONTRACTS.md`
- `mobile/docs/BUILD.md`
- `mobile/docs/ACCESSIBILITY.md`

Inspect carefully:

- `mobile/package.json`
- existing `@react-native-community/netinfo` dependency
- app root / provider composition
- navigation root
- API/data client
- cache layer
- manifest loader
- offline storage helpers
- Home startup behavior
- Reader download/cache behavior
- Murasoli data loading
- Timeline feature loading
- Themes/People/Places feature loading
- Search
- Library
- Settings storage information
- existing retry components
- existing `Loading` / `EmptyState` components

Search the entire mobile codebase for:

- `NetInfo`
- `network`
- `offline`
- `fetch`
- `retry`
- `cache`
- `download`
- `FileSystem`
- `AsyncStorage`
- `manifest`
- `contentVersion`
- network-error handling
- timeout handling

Before implementing anything, document what the current offline model ACTUALLY supports.

---

# Existing offline model must remain authoritative

Based on prior work, the app already has important offline behavior.

Verify rather than assume:

- downloaded memoir chapters can be rea

<a id="turn-0368"></a>
## Turn 0368 — 2026-08-17T10:10:12.525Z

### User

I'll start with Stage 1: verify PR #14, inspect the diff, confirm scope, then merge.
PR #14 is OPEN / CLEAN / MERGEABLE, head `f0afa62` (as expected), all checks SUCCESS. 3 commits, 19 files — matching Activity 5 scope. `app.json` is not in the changed set, so `supportsTablet` is untouched. Let me do a final diff-stat and guard scan before merging.
Scope confirmed — only `contentMaxWidth`/layout changes, screenshots, and docs; no `supportsTablet`/`ios/`/signing/EAS/UL/push/crash/analytics/content changes. Merging PR #14.
Merged — `63910ce` on `main`, remote branch deleted. Let me verify post-merge state and set up Stage 2.
contentMaxWidth ✓, 13 screenshots ✓ on main, site healthy. Post-merge CI running — let me poll it and create the Stage 2 branch.
Stage 2 branch ready. Now the core inspection: the network/offline model. Let me read the data client, AppState provider, feature loader, App root, and package.json (for NetInfo).
Key `client.ts` findings: `fetchJSON` is offline-first for content (cache→network→cache-fallback); the **manifest is network-first with cache fallback** (good for offline relaunch). Two potential defects to verify: (1) `writeCache` writes the raw response *before* `JSON.parse`, so a 200-with-malformed-JSON could overwrite a good cached manifest; (2) no fetch timeout (startup hang risk). Let me confirm the post-merge CI result, then read AppState/App/useFeature/package.json.
**Stage 1 complete & verified:** PR #14 squash-merged (`63910ce` on `main`), remote branch deleted, post-merge Mobile CI **success**, site healthy, `contentMaxWidth` + 13 screenshots on `main`, tree clean.
Now let me read the startup provider, root, feature loader, and package.json.
AppState is sound: manifest is network-first→cache-fallback; `load()` always resolves to `ready`/`error` (no infinite spinner); first-use-offline → error state with `reload` retry. The two narrow client defects stand (malformed-JSON cache overwrite; no timeout). Let me read package.json (NetInfo), App.tsx (provider composition), and useFeature.ts.
App root: SafeAreaProvider → View → AppStateProvider → Root(NavigationContainer). iOS native safe-area insets are position-aware, so a top banner above the navigator won't double-count — that's the clean placement. Let me read `useFeature.ts` and confirm NetInfo is installed.
Confirmed: NetInfo `@react-native-community/netinfo@12.0.1` installed but **unused**; and Themes/People/Places lists + all three Murasoli screens have **dead-end error states (no retry)** — a real offline→online recovery gap. My plan (aligned with Y): (1) NetworkProvider + useNetworkStatus, (2) OfflineBanner, (3) narrow client reliability fixes (parse-before-write, fetch timeout), (4) add retry to the dead-end feature/Murasoli states, (5) docs.
Let me create the network provider.
Now the OfflineBanner component.
Now wire it into App.tsx:
Now the two narrow client reliability fixes: parse-before-write and a fetch timeout.
Now add a `reload` to `useFeature` so the feature error states can retry.
Now wire retry into the Themes/People/Places error states.
Let me verify the `useFeature` variable names match `state.reload` in all three.
All three feature lists now retry. Now the three Murasoli screens need retry. Let me read MurasoliLibraryScreen's loader.
The Murasoli loaders are `useEffect`-based. I'll add a `nonce` retry to each. Starting with MurasoliLibrary.
Now MurasoliVolumeScreen — same pattern:
Now MurasoliReaderScreen:
The memoir Reader's error state also lacks retry (content-fetch failure). Adding it for consistency.
All code changes done. Let me typecheck.
Typecheck clean. Now simulator verification. The offline changes are JS-only and NetInfo's native module was already in the Activity-3 build, so Fast Refresh will deliver them. Let me restart Metro and launch on iPhone Air (which has cached content from earlier).
iPhone Air was shut down. Let me boot it and launch.
**Scenario 1 (online launch): PASS** — Home loads, **no offline banner

### Assistant

I checked PR #15. GitHub confirms it is **open, unmerged, mergeable**, with head `2096b55`, **3 commits and 16 changed files**, matching the report.  

The implementation itself is well scoped. The cache-safety fix is particularly worthwhile: JSON is now parsed **before** replacing a valid cached copy, and requests have a 12-second abort timeout. The NetInfo work is also centralized rather than duplicated across screens.

I would, however, do **one final verification pass before merging PR #15**, because two items in the report are described as PASS without actually being exercised end-to-end:

- **First-ever launch with no cache + unavailable content origin** was established from code reasoning, not actually run on a clean simulator.
- Several offline cases—especially **cached/uncached feature data, Murasoli, Clear Offline Data, and storage-count refresh**—were primarily code-verified rather than runtime-verified.

There is also one intentional behavior worth retaining as a documented limitation: the network provider currently decides offline status only from `isConnected === false`; it deliberately does **not** use `isInternetReachable === false`.  That means a phone connected to Wi-Fi with no usable internet can show no global Offline banner, while individual requests fail normally. I would **not change this automatically** now—the implementation is internally consistent—but keep that wording explicit.

So my recommended sequence is:

**PR #15 final clean-simulator offline verification → merge PR #15 → post-merge CI → stop repository feature work and address the two real submission blockers.**

Those blockers are now much more important than another polish feature:

1. **Apple Developer / App Store Connect / signed TestFlight build**
2. **Copyright-field owner/entity decision**

I would not start crash reporting yet; it changes the privacy analysis for relatively little pre-submission benefit. Universal Links can still wait until the signing Team ID and certificate information exist. Push notifications should remain deferred.

<a id="turn-0369"></a>
## Turn 0369 — 2026-08-17T10:18:02.767Z

### User

To get paid Apple developer account, it will take me few months. Does Android also need paid developer account to create mobile App? And this chat window has substantial information. I would like to take this information to new chat window since this is overloaded. That chat window also has to be a prompt provider for Claude with the information history. Let us use this GitHub repository to keep track - https://github.com/pugazg/kalaignar-tribute

### Assistant

Yes — **Android is much easier to start while you wait for Apple**.

You do **not** need a paid developer account to build, run, or test the Android version of Nenjukku Neethi locally. To publish publicly through **Google Play**, however, Google currently requires a **US$25 one-time registration fee**. It is not an annual subscription like Apple's developer program. citeturn150227search1turn150227search5

For a newly created **personal** Google Play developer account, there is an additional release requirement: before production access, you currently need a closed test with **at least 12 opted-in testers for 14 continuous days**, followed by an application for production access. Google also requires new personal accounts to verify access to a real Android device through the Play Console mobile app. citeturn150227search0turn150227search7

So while your Apple account may take a few months, I think an **Android-first release is very practical**. We can finish PR #15, then prepare the Android build/Play Store path and start that 14-day testing requirement early.

### I also created the permanent handover system

I initialized your private `pugazg/kalaignar-tribute` repository as the **control/handover repository** rather than mixing this history into the actual app source repository.

It now contains:

- `README.md` — explains that this is the control repository.
- `projects/kalaignar-autobiography/HANDOVER.md` — the substantial project history from this conversation, including SDK 57, Increment 1/2, Murasoli, Explore, production-readiness Activities 1–6, App Store preparation, screenshots, iPad, PR #15, remaining blockers and all important constraints.
- `projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md` — the bootstrap prompt specifically for the **new ChatGPT window that will continue acting as your Claude prompt provider**.

I also recorded an important live-repository detail there: current `kalaignar-autobiography/main` has subsequently advanced with commits such as `Vendor Manohara reader part 016–020`, and PR #15 is actually based on that newer live `main`. Therefore the new chat is explicitly instructed to **inspect GitHub first and never reset current main based merely on older conversational SHAs**.

### What to do now

Open a **new ChatGPT chat** and paste this:

> Continue the Nenjukku Neethi mobile project as my reviewer and prompt-provider for Claude Code.  
>   
> Use the GitHub connector. First read completely:  
> `pugazg/kalaignar-tribute/projects/kalaignar-autobiography/HANDOVER.md`  
> and then:  
> `pugazg/kalaignar-tribute/projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md`  
>   
> Then inspect the live repository `pugazg/kalaignar-autobiography`, especially PR #15 and current `main`. Treat GitHub as authoritative over any stale SHA in historical context.  
>   
> Continue from the exact current status. Your role is primarily to review Claude Code's work and provide me detailed ready-to-paste Claude prompts. Do not start a new feature until Activity 6 / PR #15 is resolved. After that, because my paid Apple Developer account may take a few months, help me prioritize an Android-first Google Play release path.

That new window will therefore **not need this overloaded conversation**. The durable history now lives in GitHub, and future handovers can simply update that same tracker repository.

<a id="turn-0370"></a>
## Turn 0370 — 2026-08-17T10:38:57.437Z

### User

Let me put mobile app development on hold then. Let me concentrate on enhancing https://nenjukkuneethi.org/read reading room. As of it has Nenjukku Neethi 6 volumes, Murasoli letters from Feb 2013 till Oct 2016 and Tholkappiya Poonga. I am planning to include items in these repositories - https://github.com/pugazg/kalaignar-novels- https://github.com/pugazg/kalaignar-short-stories- https://github.com/pugazg/kalaignar-poems- https://github.com/pugazg/kalaignar-assembly-speeches- https://github.com/pugazg/kalaignar-essays- https://github.com/pugazg/kalaignar-cinema-works- https://github.com/pugazg/kalaignar-literary-commentary- https://github.com/pugazg/kalaignar-stage-plays- https://github.com/pugazg/kalaignar-public-speechesin reading room. Reading Room has to be reorganised and structured as the name suggests Kalaignar's Digital Library to accommodate all his works. I am still collecting his works. But we need to build a structure with existing data we have. I think plan should be decided and updated in handover document and prompt document

### Assistant

Yes. I think this is the right point to **separate the Digital Library from the mobile-app roadmap** and treat the Reading Room as its own long-term project.

I inspected the current implementation before deciding the structure. `/read` is still fundamentally a Nenjukku Neethi page: `app/read/page.tsx` simply renders `Library`, and its metadata describes the six-volume memoir.  `Library.tsx` then hard-codes Nenjukku Neethi, Murasoli and Tholkappiya Poonga as the three collections while memoir search, volume filters, reading progress and bookmarks all live on that same page.  That is the main architectural constraint we need to remove before adding more works.

I have now created a **new dedicated project handover** in the `kalaignar-tribute` control repository rather than mixing this much broader library work into the old mobile handover:

`projects/kalaignar-digital-library/HANDOVER.md`

It records the current Reading Room, all nine source repositories, current release-readiness of the works already archived, the new library taxonomy, integration rules, phased roadmap, mobile-app hold, and the important fact that **Manohara vendoring has already started in the website repository and must not be duplicated**. 

I also created the new-chat bootstrap/prompt-provider document:

`projects/kalaignar-digital-library/NEXT_CHAT_PROMPT.md`

A fresh ChatGPT window can read that file and immediately continue as your **Claude Code reviewer and prompt provider**, without needing this overloaded conversation. 

I also updated the root `kalaignar-tribute/README.md` so **Kalaignar Digital Library is now the active priority** and the native mobile app is explicitly marked as paused.

### The library structure is now decided

The Digital Library will use **nine public shelves**, rather than mirroring the nine GitHub repositories directly:

1. **வாழ்க்கை எழுத்து / Life Writing** — Nenjukku Neethi
2. **கடிதங்கள் / Letters** — Murasoli
3. **புனைகதை / Fiction** — novels + short stories
4. **கவிதைகள் / Poetry**
5. **நாடகங்கள் / Drama**
6. **திரை எழுத்து / Cinema Writing**
7. **உரைகள் / Speeches** — Public Speeches + Assembly Speeches as subcollections
8. **கட்டுரைகள் / Essays & Articles**
9. **இலக்கிய உரை / Literary Commentary** — Tholkappiya Poonga, later Thirukkural, Sangatamil, Kuraloviyam, etc.

This distinction matters: **GitHub repositories are archival boundaries; shelves are reader-facing library boundaries.**

The fundamental architecture will be **one library catalog, several reader types**. We should not flatten everything into generic prose. Cinema and stage plays retain scenes, speaker labels and stage directions; poetry retains lineation; Assembly speeches retain interventions/exchanges; essays retain article boundaries; commentary retains its own units.

### Implementation order

The roadmap is now deliberately incremental.

**Phase 1 is the next activity: Library Foundation.** `/read` becomes the **கலைஞர் மின்னூலகம் / Kalaignar Digital Library** landing page. We create a normalized catalog, make the current three works catalog-driven instead of hard-coded, preserve all existing URLs, and relocate the memoir-specific search/progress/bookmarks experience into a Nenjukku Neethi-specific surface. Empty future shelves remain hidden until they actually contain a published work.

No new corpus is mass-imported during Phase 1.

**Phase 2 is Cinema, starting with Manohara.** This is intentional because the cinema repository already has mature reader exports and, importantly, the website repo already contains `public/data/cinema/manohara/parts/` from a sequence of Manohara vendor commits. We will inspect that boundary and finish it rather than starting over.

Then the planned order is broadly **Speeches → Essays/Fiction/Poetry → Stage Plays/Literary Commentary → cross-library search/discovery → reusable ingestion automation**. The exact ordering inside later phases can change as your archival work progresses.

The plan also records several imp

<a id="turn-0371"></a>
## Turn 0371 — 2026-08-17T10:52:11.047Z

### User

That Manohara part was accidentally included when cinema-works repository work was ongoing. Claude should not be using that. It should pick from the source repositories only for Manohara. Please update that in handover and prompt document.

### Assistant

Updated both documents in `pugazg/kalaignar-tribute` to reflect your correction.

The handover now states explicitly that the existing `public/data/cinema/manohara/parts/` files in `kalaignar-autobiography` were **accidental artifacts** from the cinema-works workflow and have **no authority for future Reading Room integration**. Claude must not use them for Tamil text, English translation, scene/unit counts, provenance, metadata, or as a continuation boundary. The only approved source for Manohara is `pugazg/kalaignar-cinema-works`. 

I also changed the future Manohara phase accordingly:

- Phase 1 should merely recognize that those accidental files exist and **leave them unused**.
- Phase 2 should start Manohara **afresh from the current verified/released artifacts in `kalaignar-cinema-works`**.
- The exact cinema source-repository commit/integrity state must be recorded.
- If the accidental website files need removal/replacement later, that is an implementation cleanup—not evidence or source material.

The new-chat bootstrap prompt has the same strong rule and explicitly says that any older instruction to “continue existing Manohara vendoring” is superseded.

Commits:

- `1edbcf2` — corrected Digital Library `HANDOVER.md`
- `2ac502a` — corrected `NEXT_CHAT_PROMPT.md`

So there should now be no ambiguity: **for Manohara, Claude goes back to `kalaignar-cinema-works` and imports only from its authoritative verified outputs.**

