# Kalaignar Tribute Series — Archival Workflow

## Purpose

This document defines how the raw conversation archive is converted into useful project knowledge without rewriting the historical record.

For the current processing pass, the reviewed source is `../chronological/part-01.md` through `part-15.md`, covering Turns 0001–0371.

## Two-layer archive

```text
chronological/   immutable source-of-record conversation transcript
processed/       derived navigation, synthesis and methodology
```

The chronological layer records what actually happened, including errors, experiments, abandoned approaches and changes of direction. The processed layer explains that history and makes it navigable.

## Processing workflow

### 1. Establish source coverage

Identify the exact chronological files and turn ranges being processed. Do not imply coverage beyond material actually reviewed.

### 2. Preserve the raw record

Do not edit chronological transcripts merely to correct, shorten or improve them. Historical mistakes and rolled-back approaches are part of the project record.

### 3. Identify meaningful transitions

Extract project-level changes rather than summarizing every turn. In the reviewed range these include:

- tribute collection becoming evidence-based research;
- secondary claims being checked against primary sources;
- temporary research becoming a persistent archive;
- manual source handling becoming reproducible acquisition/extraction tooling;
- downloader and extractor responsibilities being separated;
- visual material and PDFs becoming reusable archival sources;
- canonical digital-library data feeding a native reading client;
- cross-agent prompts becoming structured project handovers.

### 4. Separate kinds of derived knowledge

Use the processed documents for distinct purposes:

- `PROJECT_EVOLUTION_SUMMARY.md` — narrative interpretation;
- `TIMELINE.md` — chronology and source navigation;
- `DECISIONS_AND_RATIONALE.md` — decisions and reasoning;
- `TECHNICAL_WORKLOG.md` — engineering history;
- `INDEX.md` — entry point and coverage map.

Avoid copying the same narrative into every file.

### 5. Maintain provenance

A material statement in the processed layer should be traceable to a chronological part and, where practical, a turn range. `INDEX.md` and `TIMELINE.md` provide the first-level source map.

### 6. Preserve uncertainty and reversals

Do not convert tentative conclusions into facts. Preserve rolled-back implementations and changed architectural decisions in the raw record; explain their significance in the processed layer.

### 7. Distinguish source from interpretation

The chronological transcript answers: **what was discussed?**

The processed layer answers: **what did the project learn, decide or become?**

If the two conflict, the chronological source controls.

### 8. Treat technical handovers as archival evidence

Later conversations contain detailed prompts for continuing work in another agent/context. Preserve their state information—branch, commit, PR, checks, exclusions and next activity—as part of the project's technical history rather than reducing them to generic "development continued" summaries.

### 9. Keep live state separate from historical state

A historical handover records what was believed or true at that point in the conversation. It must not automatically override later repository state. When continuing implementation, verify live GitHub state; when documenting history, preserve the handover as evidence of the state at that time.

## Quality-control pass

Before treating a processed set as complete, check that source coverage agrees across all six documents; dates and turn ranges are consistent; terminology is stable; raw and derived layers are not conflated; reversals are not rewritten as if the abandoned approach never occurred; technical/mobile material is connected to the archival architecture without making the reader client canonical; obsolete next-step statements are removed; and repeated material serves a distinct navigational purpose.

## Current status

For `archive/2026-08-20-conversation-processing-part2`:

- source coverage reviewed: `part-01.md` through `part-15.md`;
- turn coverage: 0001–0371;
- chronological files modified: none;
- processed documents present: six;
- `INDEX.md` and `TIMELINE.md`: extended through Part 15;
- project evolution, technical worklog, decisions and workflow: extended through Part 15;
- remaining quality step: cross-document consistency/diff audit before PR review.

## Reuse

Future conversation-archive batches should repeat this workflow with an explicit source range. Extend processed history only after reviewing the new raw range; do not infer missing history from later handovers or memory.
