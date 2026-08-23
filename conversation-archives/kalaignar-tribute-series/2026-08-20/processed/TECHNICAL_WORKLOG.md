# Kalaignar Tribute Series — Technical Worklog

## Purpose

This document summarizes the technical evolution visible in `../chronological/part-01.md` through `part-15.md` (Turns 0001–0371). It is not a replacement for command history or source code; it records major engineering directions, recurring issues and architectural lessons.

## 1. From Content Collection to Archive Construction

The early conversations were primarily editorial and research-oriented. By late June 2026, the work had shifted toward building a durable archive capable of storing and processing source material at scale. The technical objective became broader than downloading files: preserve provenance, support repeatable extraction and make source material usable by future reading products.

## 2. Configuration-Driven Acquisition

The archive discussions introduced a configuration-driven approach. Source definitions belong in configuration, downloader behavior should follow a stable schema, and changing configuration without updating the downloader contract is unsafe.

**Lesson:** configuration is an interface, not merely a collection of parameters.

## 3. Downloader Engine Refactoring

The downloader was progressively generalized for different Kalaignar source collections. Important concerns included deterministic output locations, repeatability, retention of original fetched material, avoiding silent overwrites and allowing later extraction without renewed network access.

## 4. Raw HTML Preservation

Raw page HTML was retained before extraction. This preserved structural information such as ProofreadPage containers, parser output, page-quality metadata, headers and MediaWiki markup.

**Lesson:** the raw acquisition layer should survive even if parsing logic changes later.

## 5. Extraction Pipeline Investigation

The conversations show hands-on debugging of extraction using shell inspection and actual HTML structure. Instead of assuming a simplified DOM, the workflow located real content containers and distinguished body content from quality/header markup.

This marked the transition from speculative parsing to evidence-driven parser development.

## 6. Downloader and Extractor Responsibility Boundary

At Turn 0251 the user reported rolling back a downloader change. The resulting architectural decision was explicit: the downloader should remain an archival acquisition engine; HTML understanding belongs in the extractor.

This separation reduces coupling. Acquisition can preserve source material even when extraction logic changes, while extractor revisions do not require reacquiring the source.

## 7. Embedded Image Extraction

The next range examined photographs embedded within scanned pages. The source HTML exposed thumbnail containers, image elements, crop offsets, dimensions and captions.

The resulting conceptual pipeline was:

```text
full page scan
      ↓
thumbnail/crop metadata
      ↓
coordinate-aware crop
      ↓
individual image derivative
      ↓
caption/page provenance
```

This extended the archive beyond plain text and full-page scans toward structured visual assets.

## 8. PDF-Backed Rendering

Local volume PDFs became an additional source for page rendering. Rather than add redundant configuration, PDF paths could be derived from the established output hierarchy (`volume1.pdf`, `volume2.pdf`, etc.).

This introduced useful source redundancy: derivatives can be regenerated from preserved PDFs even when remote source behavior changes.

## 9. Avoiding Premature Engine Expansion

Across the downloader/extractor work, the archive repeatedly favors stabilizing existing stages before adding another engine. New layers are justified by a distinct responsibility, not simply because another feature is possible.

## 10. Layered Technical Model

By the end of the extraction work, the architecture can be summarized as:

```text
Source discovery
      ↓
Configuration
      ↓
Downloader / acquisition
      ↓
Raw HTML / scans / PDFs
      ↓
Extraction (text + visual metadata)
      ↓
Validation / fidelity checks
      ↓
Structured canonical data
      ↓
Web / native reader
```

Each layer should remain independently inspectable.

## 11. Native Mobile Development

Part 14 records the transition into Expo/iOS development for the Kalaignar Digital Library. Simulator/Expo connectivity problems were treated separately from application-code failures: a timed-out `simctl openurl` meant the native app had not necessarily executed yet.

This is consistent with the earlier layered debugging approach: identify which layer failed before changing downstream code.

## 12. Feature Data Contracts

By Part 15, mobile work is consuming generated feature datasets such as timeline, governance, people, themes and quotes through an application data layer. The handoff records manifest integration, deterministic reruns and validation/typecheck/export checks.

This demonstrates the payoff of keeping canonical/archive data separate from presentation: the native application can consume generated data without becoming the authority for the archival source.

## 13. Branch, PR and Verification Discipline

The later workflow is deliberately staged:

1. complete a narrowly scoped activity;
2. verify generated datasets and checks;
3. inspect the PR for unrelated changes;
4. merge to clean `main`;
5. verify post-merge state;
6. create a fresh branch for the next activity.

Scope exclusions are written into the handoff itself—for example, not exporting an adjacent `places` dataset merely because the source exists, and not starting unrelated UI work during the Timeline activity.

## 14. Multi-Agent Handoff as Engineering Infrastructure

The project begins using detailed prompts to transfer state to Claude. These prompts carry branch/commit/PR identifiers, completed artifacts, checks, exclusions and the exact next activity.

For a long-running project, this is effectively part of the technical infrastructure. It reduces state loss and prevents a new agent from redoing completed work or widening scope based on incomplete context.

## 15. Failure Modes Identified

Recurring risks across the reviewed range include configuration drift, parser assumptions, long-running scripts, source-cleaning loss, over-engineering, confusing simulator/tooling failure with application failure, derivative data drifting from canonical data, and handoff state becoming stale.

## 16. Engineering Practices Emerging from the Conversations

1. download once and preserve raw source;
2. make extraction rerunnable offline;
3. inspect actual source structure before changing parser logic;
4. keep configuration contracts explicit;
5. separate downloader and extractor responsibilities;
6. retain crop/caption metadata for visual derivatives;
7. keep preserved PDFs usable as regeneration sources;
8. validate output before treating it as canonical;
9. separate canonical data from reader applications;
10. debug the failing layer rather than changing downstream code blindly;
11. use deterministic generation and validation checks;
12. merge completed scope before beginning adjacent scope;
13. encode state and exclusions in cross-agent handovers.

## Relationship to the Raw Archive

Exact commands, code fragments, errors and conversation context remain in `../chronological/`. Consult the relevant source part whenever precise reconstruction is required.
