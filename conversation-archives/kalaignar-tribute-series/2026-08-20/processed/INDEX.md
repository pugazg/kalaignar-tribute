# Kalaignar Tribute Series — Processed Archive Index

## Purpose

This directory is the curated knowledge layer derived from `../chronological/`.

The chronological transcript is preserved as the source of record. Files here are navigation, synthesis and methodology documents; they do not replace the raw conversation.

## Reviewed source coverage

| Source file | Turns | Starting date | Principal subject |
| --- | ---: | --- | --- |
| `../chronological/part-01.md` | 0001–0025 | 2026-06-03 | Birthday tribute series; personal recollections |
| `../chronological/part-02.md` | 0026–0050 | 2026-06-03 | Institutional/development claims and verification |
| `../chronological/part-03.md` | 0051–0075 | 2026-06-04 | Assembly records; industrial-policy research |
| `../chronological/part-04.md` | 0076–0100 | 2026-06-10 | Constitutional and political thought |
| `../chronological/part-05.md` | 0101–0125 | 2026-06-16 | Deep document reading and source-led synthesis |
| `../chronological/part-06.md` | 0126–0150 | 2026-06-26 | Transition to building the digital archive |
| `../chronological/part-07.md` | 0151–0175 | 2026-06-27 | Downloader/configuration architecture |
| `../chronological/part-08.md` | 0176–0200 | 2026-06-27 | Downloader implementation and acquisition layers |
| `../chronological/part-09.md` | 0201–0225 | 2026-07-04 | Tamil source extraction and HTML debugging |
| `../chronological/part-10.md` | 0226–0250 | 2026-07-04 | Pipeline consolidation |

**Reviewed coverage:** Turns 0001–0250.

## Curated documents

| File | Use it for |
| --- | --- |
| `PROJECT_EVOLUTION_SUMMARY.md` | Understanding how the original tribute activity evolved into a digital archival project |
| `TIMELINE.md` | Following the project chronologically and locating the corresponding raw turn ranges |
| `DECISIONS_AND_RATIONALE.md` | Understanding major archival/research decisions and why they were made |
| `TECHNICAL_WORKLOG.md` | Following the engineering evolution of acquisition, storage and extraction |
| `ARCHIVAL_WORKFLOW.md` | Reusing the source-first archival methodology in later work |
| `INDEX.md` | Entering and navigating this processed archive |

## Recommended reading paths

For a quick historical understanding:

`PROJECT_EVOLUTION_SUMMARY.md` → `TIMELINE.md`

For archival/research work:

`ARCHIVAL_WORKFLOW.md` → `DECISIONS_AND_RATIONALE.md` → relevant chronological part

For engineering work:

`TECHNICAL_WORKLOG.md` → `TIMELINE.md` Phases 6–10 → relevant chronological part

## Provenance model

The archive has two layers:

```text
chronological/   source-of-record conversation transcript
processed/       derived navigation, synthesis and methodology
```

A processed statement should be capable of being traced back to a chronological part and turn range. If interpretation and source conflict, the chronological source controls.

## Preservation rule

Do not rewrite the chronological files merely to make the history cleaner. Errors, abandoned approaches and changes of direction are themselves part of the project history. Correct or reinterpret them in the processed layer while preserving the original record.

## Processing status

- Raw source files reviewed: `part-01.md` through `part-10.md`
- Turn coverage reviewed: 0001–0250
- Curated document set: complete for this reviewed range
- Next quality step: cross-document consistency and duplication audit before merge/PR review
