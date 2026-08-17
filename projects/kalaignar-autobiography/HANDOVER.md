# Kalaignar Autobiography / Nenjukku Neethi Mobile — Master Handover

**Last updated:** 2026-08-17

This is the durable cross-chat handover for the Nenjukku Neethi mobile work. A fresh ChatGPT window should read this file first, then inspect live GitHub state before producing the next Claude Code prompt.

## 1. Canonical repositories and site

- **Implementation repository:** `pugazg/kalaignar-autobiography`
- **Tracking / handover repository:** `pugazg/kalaignar-tribute`
- **Production site:** `https://nenjukkuneethi.org`
- **Mobile bundle/package:** `org.nenjukkuneethi.app`
- **Current marketing version:** `0.1.0`

The implementation repository is authoritative for code/data. This tracker repository is authoritative for cross-chat context, workflow history, owner decisions and continuation prompts.

---

## 2. Product baseline

The native Expo/React Native app currently includes:

- 6 Nenjukku Neethi memoir volumes;
- 391 memoir chapters;
- Tamil-first native reading;
- English translations where available;
- local reading progress and recents;
- bookmarks / Saved for memoir content;
- offline memoir chapter/image support;
- local/offline-first search across memoir chapter indexes;
- Timeline with 42 milestones;
- Explore entry points for Themes, People and Places;
- 6 Themes;
- 15 People;
- 10 Places with explicitly **schematic, non-geographic** map coordinates;
- native Murasoli reader;
- 7 Murasoli volumes (48–54), 346 curated letters total;
- Volume 54 is a normal curated **36-letter** volume; do not resurrect the discarded raw-page-browser approach;
- reader themes: light / sepia / dark;
- Dynamic Type support;
- text sharing;
- native iPhone and first-release-ready iPad layouts.

### Important Murasoli details

Total structured letters:

- Vol 48 — 58
- Vol 49 — 53
- Vol 50 — 50
- Vol 51 — 49
- Vol 52 — 50
- Vol 53 — 50
- Vol 54 — 36

Volumes 48–53 have full English coverage in the app data. Volume 54 is treated as Tamil-only in the native reader. Raw OCR/page JSON exists for Vol 54 but is deliberately not exposed as a separate page browser.

Murasoli bookmarks are still deferred because existing Saved/bookmark schema is memoir-specific. Do not casually migrate this schema during unrelated activities.

---

## 3. Native stack / technical baseline

Current mobile baseline after sequential migration:

- **Expo SDK:** 57
- Expo version line previously aligned to `57.0.13`
- React Native: `0.86.2`
- React: `19.2.3`
- Node 22 in CI
- Xcode 26 clean native simulator build previously passed

The SDK-57 upgrade was completed without carrying forward the old fmt/consteval native patch.

Potential minor tech debt from the upgrade era:

- `mobile/.npmrc` may still contain `legacy-peer-deps=true`;
- do not assume `expo-dev-client` exists without checking current `package.json`.

**Physical-device policy:** post-SDK-upgrade physical-device testing was explicitly waived. Do not report a physical SDK-57 test as PASS unless one is actually performed later. Repository/simulator work may proceed without it.

---

## 4. Major completed mobile milestones

### Increment 1 / stability

Important historical commits included:

- offline image binaries / Reader local images / storage counts / retries / truthful offline-search wording;
- Search → Reader find/highlight scrolling;
- race fix using synchronous find index + onLayout scroll;
- mobile CI / handover / README;
- Expo Go / dev-build documentation.

Increment 1 smoke behavior was previously validated; Universal Links were excluded.

### Expo 52 → 57 migration

Sequential SDK upgrades were completed and merged. Current code should be treated as SDK-57 code. Do not restart the migration.

### Increment 2 Activity 1 — feature data export

Completed and merged:

- `timeline.json` — 42
- `governance.json` — 30
- `people.json` — 15
- `themes.json` — 6
- `quotes.json` — 14
- later `places.json` — 10

The exporter is deterministic for feature JSON. Do **not** claim the whole manifest build is byte-identical because the app manifest has generated metadata such as `generatedAt`.

### Activity 2 — Timeline

Completed and merged:

- native timeline screen;
- existing feature loader / offline-first data client;
- source-era ordering preserved;
- deep-links to real memoir Reader refs;
- fallback to old volume-era Timeline if feature data is missing/malformed.

### Memoir volume-title correction

Merged separately: volumes 2–6 received proper Tamil part titles instead of generic `Volume N` fallbacks.

### Activity 3 — Native Murasoli

Merged. Native route chain:

`Explore → MurasoliLibrary → MurasoliVolume → MurasoliReader`

Important constraint: Vol 54 is the 36 curated letters, not a scan-page browser.

### Activity 4 — native Explore + Places export

Merged:

- `places.json` generated from authoritative `data/places.ts`;
- Explore → Themes / People / Places / Murasoli;
- source refs deep-link to memoir Reader;
- Places coordinates remain schematic (viewBox 1640×2032), never geocoded;
- no heavy map dependency;
- Governance and Quotes remained data-only.

---

## 5. Production-readiness work completed

### Activity 1 — Privacy / Support / About

Merged and live:

- `https://nenjukkuneethi.org/privacy`
- `https://nenjukkuneethi.org/support`
- `https://nenjukkuneethi.org/about`

The privacy position was based on actual current app behavior, not a generic template.

### Activity 2 — release engineering

Merged:

- `mobile/eas.json` with development / preview / production profiles;
- local app-version source strategy;
- iOS build number seeded at `1`;
- Android versionCode seeded at `1`;
- `ITSAppUsesNonExemptEncryption=false`;
- `mobile/docs/RELEASE.md`.

A paid Apple Developer account is still required for the real App Store/TestFlight path. The user expects obtaining this may take **a few months**.

### Activity 3 — accessibility repository pass

Merged:

- screen-reader labels/roles/state improvements;
- primary heading semantics;
- touch-target improvements;
- measured contrast fixes across light/sepia/dark;
- Dynamic Type verification;
- `mobile/docs/ACCESSIBILITY.md`.

Truthful remaining boundary:

- manual VoiceOver/TalkBack on-device verification has **not** been performed;
- Home/Explore dashboard clipping at the very largest accessibility text sizes remains documented;
- do not claim those are fully solved.

### Activity 4 — App Store metadata package

Merged:

- English + Tamil listing copy;
- privacy-label worksheet;
- age-rating worksheet;
- review notes;
- screenshot plan;
- submission checklist;
- store screenshots.

Current store asset package is under `mobile/store/`.

Canonical app name remains **Nenjukku Neethi**.

Current category recommendation:

- Primary: Books
- Secondary: Reference

Current privacy worksheet conclusion was **Data Not Collected**, based on current code and with routine hosting/network metadata nuance documented. Do not add analytics/crash SDKs without re-evaluating this.

### Activity 5 — iPad readiness + missing screenshots

Merged before Activity 6 branch creation.

Key code change:

- centered `contentMaxWidth = 720` reading/content column;
- applied to shared Screen, memoir/Murasoli readers and raw FlatList surfaces;
- no-op on iPhone widths;
- `supportsTablet` remains **true**.

Result: **FIRST-RELEASE READY** on iPad, not "fully tablet-optimized".

Screenshot package now includes:

- **7 iPhone 6.9-inch screenshots** at 1260×2736;
- **6 iPad 13-inch screenshots** at 2064×2752;
- alpha stripped;
- clean marketing status bar;
- Tamil Search screenshot uses query `தமிழ்` and returned 215 results at capture time.

Known manual follow-up: iPad landscape was not actually exercised in the simulator session; do not report it as tested.

---

## 6. CURRENT ACTIVE WORK — Production Readiness Activity 6

### PR #15

Implementation repo:

`pugazg/kalaignar-autobiography`

PR:

`https://github.com/pugazg/kalaignar-autobiography/pull/15`

Current verified state at handover time:

- **OPEN**
- **not merged**
- **mergeable**
- head: `2096b559517298e5f65ada8b9a35f223a8f892bd`
- branch: `mobile/offline-network-readiness`
- 3 commits
- 16 changed files
- Mobile CI run #33: SUCCESS
- Vercel status: SUCCESS

Do not assume it has been merged in a future chat. Inspect GitHub first.

### Activity 6 contents

PR #15 adds:

1. **Central NetInfo architecture**
   - `NetworkProvider`
   - `useNetworkStatus()`
   - `unknown | online | offline`
   - only `isConnected === false` means globally offline
   - connectivity state remains local; no analytics/privacy change

2. **Global offline banner**
   - wording: `Offline — downloaded & cached content is available`
   - shown only for known offline state
   - below status bar
   - does not cover Reader controls
   - works with iPad 720pt column
   - accessibility announcement behavior included

3. **Client reliability fixes**
   - 12-second request timeout
   - parse JSON before writing to cache
   - failed/malformed network refresh cannot overwrite a known-good cached copy

4. **Retry improvements**
   - Themes / People / Places
   - Murasoli Library / Volume / Reader
   - memoir Reader

5. `mobile/docs/OFFLINE_NETWORK.md` and readiness docs.

### Important verification caveat before merging PR #15

A prior review found the implementation good, but recommended one final verification pass because some report items were inferred from code rather than fully exercised end-to-end:

- first-ever launch with **no cache** + unavailable content origin;
- cached/uncached feature data runtime paths;
- cached/uncached Murasoli runtime paths;
- Clear Offline Data runtime behavior;
- storage-count refresh runtime behavior.

These do not necessarily indicate defects. They are verification gaps. Before merging #15, the prompt-provider should ask Claude to perform the highest-value clean-simulator/runtime checks that are practical, update claims so they distinguish **runtime-verified** from **code-verified**, then merge only if clean.

The current provider intentionally uses `isConnected`, not `isInternetReachable`. Therefore Wi-Fi with no usable Internet may not trigger the global banner; individual request errors still surface. Preserve this as a deliberate documented limitation unless there is evidence to change it.

---

## 7. Important current-main caution

At handover time, a live GitHub inspection showed `pugazg/kalaignar-autobiography` current `main` at:

`9535f306c41683e9461b7e9da7677a331d6254c7`

with recent commits titled e.g.:

- `Vendor Manohara reader part 016`
- `Vendor Manohara reader part 017`
- `Vendor Manohara reader part 018`
- `Vendor Manohara reader part 019`
- `Vendor Manohara reader part 020`

PR #15's GitHub base SHA is also `9535f306...`.

These commits arrived after the Activity-5 merge lineage described conversationally. **Do not reset, rewrite or delete them merely because they look unrelated.** Treat current `main` as authoritative, inspect their relationship if it matters, and merge/rebase PR #15 only against the actual live repository state.

This is exactly why every new chat must inspect GitHub instead of trusting old SHA narratives blindly.

---

## 8. Remaining store / release blockers and decisions

### Apple

The user expects a paid Apple Developer account may take a few months.

Until it exists, do not pretend to complete:

- App Store Connect app record;
- signing/provisioning;
- TestFlight production path;
- real Apple Team ID-dependent association setup;
- actual App Store submission.

### Android / Google Play

Android development itself is not blocked by a paid account. Public Google Play distribution requires a Google Play/Android full-distribution developer account. See the prompt-provider's current web verification when planning this path; rules can change.

Because Apple may be delayed, an **Android-first release path is now a useful candidate workstream** after PR #15 is finalized.

Do not start it automatically: first inspect current Android config/build readiness, current Google Play requirements, and whether the user wants public Play Store distribution now.

### Copyright field

Still unresolved:

**OWNER DECISION REQUIRED**

Do not invent the copyright owner/entity. Do not use DMK, Murasoli, Kalaignar family, a trust/foundation or any other entity without the user's explicit instruction and supporting basis.

### Universal Links

Still deferred because final association values depend on real signing identity:

- Apple Team ID for AASA / Associated Domains validation;
- Android signing certificate fingerprint for `assetlinks.json`.

Do not build fake final association files with guessed identifiers.

### Crash reporting

Not installed. Treat this as a privacy/product decision, not an automatic pre-launch dependency. Adding a third-party SDK may require revisiting privacy disclosures.

### Push notifications

Deliberately deferred. `expo-notifications` may be present as a dependency/plugin, but no actual notification implementation should be assumed.

---

## 9. Claude Code prompt-provider rules

The new ChatGPT window is primarily a **reviewer + prompt provider for Claude Code**.

For every Claude execution report:

1. inspect the relevant GitHub PR/repository independently;
2. compare reported head SHA, changed-file count, commit count and scope;
3. inspect high-risk patches when needed;
4. verify CI/workflow state;
5. identify any overclaims (runtime vs code verification, simulator vs physical device, etc.);
6. recommend merge only when scope and gates are clean;
7. then provide the next complete ready-to-paste Claude prompt when the user asks.

Prompt style:

- explicit staged workflow;
- mandatory startup docs;
- source-of-truth constraints;
- exact scope exclusions;
- verification matrix;
- Git discipline;
- stop condition;
- structured final report;
- never silently begin the next activity.

Do not ask the user to repeat prior project context if this handover plus live GitHub state can resolve it.

---

## 10. Recommended immediate continuation

A fresh ChatGPT window should begin by:

1. reading this handover;
2. inspecting PR #15 live;
3. confirming whether PR #15 is still open/green/mergeable or has since changed;
4. if still open, preparing a **final Activity-6 verification + merge prompt** for Claude rather than starting another feature;
5. once #15 is merged and post-merge CI is green, discuss whether to pursue an **Android-first Google Play release track while Apple account access is delayed**;
6. keep copyright owner/entity as an explicit unresolved owner decision.

Do not start Universal Links, crash reporting or push notifications automatically.
