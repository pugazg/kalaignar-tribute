# Kalaignar Tribute Series — Decisions and Rationale

## Purpose

This document records important methodological and project decisions visible in `../chronological/part-01.md` through `part-15.md` (Turns 0001–0371), together with the reasoning behind them.

## 1. Preserve the raw conversation archive unchanged

**Decision:** treat `../chronological/` as the source-of-record and do not rewrite it into cleaner prose.

**Rationale:** conversation history preserves context, failed approaches, corrections, uncertainty and changes in direction that a polished summary would erase.

## 2. Create a separate processed layer

**Decision:** summaries, timelines, decisions and workflows live under `processed/`.

**Rationale:** raw preservation and interpretation serve different purposes and should remain independently inspectable.

## 3. Move beyond tribute rhetoric toward evidence

**Decision:** claims about achievements, institutions, policies or historical significance require evidence rather than acceptance because they appear in commemorative or political material.

**Rationale:** a reliable archive must distinguish a claim from its documentary support.

## 4. Prefer primary and contemporaneous sources

**Decision:** prefer Assembly records, government documents, policy texts and original publications where available.

**Rationale:** contemporaneous evidence makes dates, wording, institutional context and policy intent independently checkable.

## 5. Preserve unresolved questions

**Decision:** when a source cannot support a definite conclusion, retain the uncertainty.

**Rationale:** silently converting uncertainty into certainty weakens the archive.

## 6. Separate acquisition, extraction and publication

**Decision:** obtaining a source, interpreting/extracting it, validating it and presenting it are different stages.

**Rationale:** each stage has different failure modes and should be independently repeatable.

## 7. Keep HTML interpretation out of the downloader

**Decision:** after an attempted change was rolled back, keep the downloader focused on archival acquisition and place HTML understanding in the extractor.

**Rationale:** source acquisition should not depend on current parser assumptions. The same preserved source may need to be reinterpreted later with improved extraction logic.

## 8. Do not run modified pipelines before code and configuration agree

**Decision:** configuration changes alone are not sufficient reason to execute an old downloader/extractor.

**Rationale:** configuration is an interface contract; implementation must understand the changed schema first.

## 9. Preserve visual evidence, not only text

**Decision:** where source pages expose embedded photographs, crop coordinates and captions, treat them as archival information rather than discard them after text extraction.

**Rationale:** visual content can carry historical evidence that is not represented in OCR/transcription. Derived crops should remain traceable to the full page scan.

## 10. Keep preserved PDFs usable as regeneration sources

**Decision:** use locally preserved PDFs as stable page-rendering inputs where useful, deriving their paths from existing structure rather than proliferating redundant configuration.

**Rationale:** this reduces dependence on live websites and makes derivative regeneration reproducible.

## 11. Build reusable workflows rather than one-off fixes

**Decision:** recurring source/archive patterns should become scripts, structure and documentation.

**Rationale:** the project spans many works and formats; repeatable processes create consistency and reduce manual drift.

## 12. Keep canonical data independent from presentation clients

**Decision:** generated/validated archive data should feed web or native readers rather than letting those clients become the canonical source.

**Rationale:** presentation technology will change faster than archival evidence. A stable data layer allows multiple reading experiences without rewriting source truth.

## 13. Diagnose infrastructure failure before application failure

**Decision:** when Expo/iOS failed to open a simulator URL, treat the connection/tooling layer as the first problem rather than immediately changing app code.

**Rationale:** layered debugging avoids introducing code changes for failures that occur before the application is reached.

## 14. Complete and verify one feature scope before starting another

**Decision:** later mobile work is divided into narrow activities. A completed activity is checked, merged and post-merge verified before a fresh branch begins the next feature.

**Rationale:** this keeps diffs reviewable, makes regressions easier to locate and prevents roadmap scope from expanding opportunistically.

## 15. Explicitly record exclusions

**Decision:** handoffs state what must *not* be done as well as what should be done—for example, not adding `places` merely because a source file exists, and not starting unrelated UI work during the Timeline activity.

**Rationale:** in long-running projects, adjacent possibilities are a major source of scope drift. Explicit exclusions preserve the intended phase boundary.

## 16. Treat cross-agent handovers as project records

**Decision:** when work moves to Claude or another fresh context, provide repository state, branch/commit/PR identifiers, completed artifacts, checks, exclusions and the exact next activity.

**Rationale:** a precise handover reduces rework and prevents stale conversational memory from overriding live repository state.

## 17. Keep the public narrative downstream of verification

**Decision:** public summaries and reading experiences should follow source verification rather than outrun it.

**Rationale:** presentation convenience must not become more authoritative than evidence.

## Decision Hierarchy

When goals conflict, the reviewed conversations support this priority order:

1. source fidelity;
2. provenance and traceability;
3. factual verification;
4. preservation of uncertainty;
5. stable canonical data;
6. reproducible processing;
7. controlled scope and handoff state;
8. publication convenience;
9. presentation polish.

## Relationship to the Raw Archive

This document is a curated interpretation. The chronological transcript remains authoritative for exact wording, sequence and context.
