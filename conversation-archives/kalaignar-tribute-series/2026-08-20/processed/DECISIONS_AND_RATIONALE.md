# Kalaignar Tribute Series — Decisions and Rationale

## Purpose

This document records the important methodological and project decisions visible in the chronological conversation archive, together with the reasoning behind them.

## 1. Preserve the raw conversation archive unchanged

### Decision

The files under `../chronological/` are treated as the source-of-record conversation archive and are not rewritten into cleaner prose.

### Rationale

Conversation history contains context, failed approaches, corrections, uncertainties and changes in direction that would disappear in a polished summary. Preserving it protects the provenance of later project decisions.

## 2. Create a separate processed layer

### Decision

Human-readable summaries, timelines, decisions and workflows live under `processed/` instead of replacing the chronological files.

### Rationale

Raw preservation and interpretation serve different purposes. Keeping them separate allows the archive to retain historical fidelity while still becoming understandable and useful.

## 3. Move beyond tribute rhetoric toward evidence

### Decision

Claims about Kalaignar's achievements, institutions, policies or historical significance should not be accepted merely because they appear in commemorative or political material.

### Rationale

The project increasingly encountered infographics, institutional claims and policy narratives. Reliable archival work requires distinguishing a claim from its evidence.

## 4. Prefer primary and contemporaneous sources

### Decision

Assembly records, government documents, policy texts and original publications should be preferred where available.

### Rationale

Contemporaneous evidence reduces dependence on later retellings and makes it possible to verify dates, wording, institutional context and policy intent.

## 5. Preserve unresolved questions

### Decision

When a source cannot support a definite conclusion, record the uncertainty rather than forcing a clean answer.

### Rationale

An archive becomes less trustworthy if uncertainty is silently converted into certainty. Unresolved items are themselves useful research metadata.

## 6. Separate acquisition, extraction and publication

### Decision

The technical archive should distinguish between obtaining a source, extracting its content, validating it and publishing a readable representation.

### Rationale

Each stage introduces different failure modes. A downloader can succeed while an extractor fails; extraction can succeed while text fidelity remains poor. Layering makes errors easier to locate and correct.

## 7. Do not run modified pipelines before code and configuration agree

### Decision

Configuration changes alone are not sufficient reason to run an existing downloader or extraction engine.

### Rationale

The archived technical discussions explicitly show caution around running `download.py` after changing `config.yaml`. The implementation must actually understand the new configuration contract before execution.

## 8. Treat source preservation as more important than convenience

### Decision

Raw HTML, scans, transcripts or page-level source material should be retained even when cleaned text is easier to work with.

### Rationale

Later verification may require returning to the original representation. A cleaned derivative cannot always reconstruct what was removed.

## 9. Build reusable workflows rather than one-off fixes

### Decision

When a recurring source or archive pattern appears, generalize the process into scripts, structure and documentation.

### Rationale

The project expanded beyond one tribute or one book. A reusable workflow reduces repeated manual work and creates consistency across the larger Kalaignar digital archive.

## 10. Keep the public narrative downstream of verification

### Decision

Public-facing summaries, reading experiences or tribute material should be generated after source verification, not before it.

### Rationale

The archive is intended to preserve historical and cultural material. Presentation should not outrun evidence.

## Decision Hierarchy

When two project goals conflict, the conversations imply the following priority order:

1. source fidelity;
2. provenance and traceability;
3. factual verification;
4. preservation of uncertainty;
5. reusable structure;
6. publication convenience;
7. presentation polish.

## Relationship to the Raw Archive

This document is a curated interpretation of the conversations. The chronological transcript remains authoritative for the exact wording, sequence and context of individual decisions.
