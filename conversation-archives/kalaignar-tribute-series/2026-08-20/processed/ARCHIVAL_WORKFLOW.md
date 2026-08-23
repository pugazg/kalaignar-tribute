# Kalaignar Tribute Series — Archival Workflow

## Purpose

This document defines how the raw conversation archive is converted into useful project knowledge without rewriting the historical record.

For the current processing pass, the reviewed source is `../chronological/part-01.md` through `part-10.md`, covering Turns 0001–0250.

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

Do not edit chronological transcripts merely to correct, shorten or improve them. Historical mistakes should remain visible in the source record.

### 3. Identify meaningful transitions

Extract project-level changes rather than summarizing every conversational turn. Examples include:

- tribute collection becoming evidence-based research;
- secondary claims being checked against primary sources;
- temporary research becoming a persistent archive;
- manual source handling becoming reproducible acquisition/extraction tooling.

### 4. Separate kinds of derived knowledge

Use the processed documents for distinct purposes:

- `PROJECT_EVOLUTION_SUMMARY.md` — narrative interpretation;
- `TIMELINE.md` — chronology and source navigation;
- `DECISIONS_AND_RATIONALE.md` — decisions and their reasoning;
- `TECHNICAL_WORKLOG.md` — engineering history;
- `INDEX.md` — entry point and coverage map.

Avoid copying the same narrative into every file.

### 5. Maintain provenance

A material statement in the processed layer should be traceable to a chronological part and, where practical, a turn range. The timeline and index provide the first-level mapping for the current archive.

### 6. Preserve uncertainty

Do not convert tentative conversation conclusions into established facts. Unverified claims, unresolved readings and provisional technical assumptions should remain identifiable as such.

### 7. Distinguish source from interpretation

The chronological transcript answers: **what was discussed?**

The processed layer answers: **what did the project learn, decide or become?**

If the two conflict, the chronological source controls.

## Quality-control pass

Before treating a processed set as complete, check:

- source coverage agrees across documents;
- dates and turn ranges are consistent;
- terminology is stable;
- raw and derived layers are not conflated;
- no document claims that unfinished processing is complete;
- obsolete next-step statements are removed;
- repeated material serves a distinct navigational purpose rather than accidental duplication.

## Current status

For the 2026-08-20 archive processing branch:

- source coverage reviewed: Turns 0001–0250;
- chronological files modified: none;
- processed documents present: six;
- timeline/source map: complete for the reviewed range;
- cross-document consistency pass: completed;
- remaining repository action: review branch diff and prepare the change for merge through the repository's normal review process.

## Reuse

Future conversation-archive batches should repeat this workflow with an explicit source range. Extend the existing processed history only after reviewing the new raw range; do not infer missing history from later handovers or memory.
