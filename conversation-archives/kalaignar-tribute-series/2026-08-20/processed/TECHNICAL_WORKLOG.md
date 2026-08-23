# Kalaignar Tribute Series — Technical Worklog

## Purpose

This document summarizes the technical evolution visible in the chronological conversation archive. It is not a replacement for command history or source code; it records the major engineering directions, recurring issues and architectural lessons.

## 1. From Content Collection to Archive Construction

The early conversations were primarily editorial and research-oriented. By late June 2026, the work had shifted toward building a durable archive capable of storing and processing source material at scale.

The technical objective became broader than downloading files. The emerging system needed to preserve provenance, support repeatable extraction and remain usable for future digital-library work.

## 2. Configuration-Driven Acquisition

The archive discussions introduced a configuration-driven approach to downloading source material.

Key idea:

- source definitions belong in configuration;
- downloader behavior should follow a stable schema;
- changing configuration without updating the downloader contract is unsafe.

A notable discussion explicitly cautioned against running `download.py` immediately after changing `config.yaml`, because the existing downloader still expected the older configuration shape.

### Lesson

Configuration and implementation must evolve together. A configuration file is an interface, not merely a collection of parameters.

## 3. Downloader Engine Refactoring

Later conversations moved into modifying the downloader engine itself.

The intended direction was to make acquisition reusable across different Kalaignar source collections rather than hard-code behavior for a single book or site.

Important concerns included:

- deterministic output locations;
- repeatability;
- retaining the original fetched material;
- avoiding silent overwrites;
- making later extraction independent of network access where possible.

## 4. Raw HTML Preservation

The archive captured raw page HTML before extraction.

This was technically important because the source pages contained structure such as:

- `prp-page-content`;
- `mw-parser-output`;
- page-quality metadata;
- running headers;
- MediaWiki/ProofreadPage markup.

Keeping the HTML allowed later inspection when extraction behavior was uncertain.

### Lesson

The raw acquisition layer should survive even if parsing logic changes later.

## 5. Extraction Pipeline Investigation

The conversations show hands-on debugging of `scripts/extract.py` using shell inspection and HTML structure checks.

Examples of the debugging pattern included:

- stopping a long-running extraction process;
- grepping downloaded HTML for structural markers;
- locating the actual page-content container;
- distinguishing page-quality/header markup from textual body content.

This marked a transition from speculative parsing to evidence-driven parser development.

## 6. Avoiding Premature Engine Expansion

At one point, after a request for more code, the response explicitly questioned whether another engine should be added immediately.

This reflects an important architectural principle: adding new processing stages is not automatically progress. Existing acquisition and extraction layers should first be understood and stabilized.

## 7. Layered Technical Model

The conversations collectively point toward the following architecture:

```text
Source discovery
      ↓
Configuration
      ↓
Downloader / acquisition
      ↓
Raw preserved source
      ↓
Extraction
      ↓
Validation / fidelity checks
      ↓
Structured canonical data
      ↓
Reader / publication layer
```

Each layer should be independently inspectable.

## 8. Failure Modes Identified

The archive surfaces several recurring technical risks:

### Configuration drift

A new config schema can break an old downloader even when the YAML itself is valid.

### Parser assumptions

A parser that looks for the wrong HTML container can return incomplete or misleading text.

### Long-running scripts

Extraction routines may appear stalled or require targeted debugging rather than blind reruns.

### Source-cleaning loss

Removing markup too early can destroy information needed for later validation.

### Over-engineering

Introducing new engines before stabilizing existing stages makes debugging harder and obscures the source of errors.

## 9. Engineering Practices Emerging from the Conversations

The technical discussions support the following reusable practices:

1. download once, preserve raw source;
2. make extraction rerunnable offline;
3. inspect actual source structure before changing parser logic;
4. keep configuration contracts explicit;
5. separate acquisition errors from extraction errors;
6. validate output before treating it as canonical;
7. document architecture decisions as the system evolves;
8. prefer incremental stabilization over adding unnecessary layers.

## 10. Relationship to Later Digital Library Work

These archive-engineering conversations are significant because they form the technical precursor to the later Kalaignar Digital Library / Reading Room approach.

The same principles recur there:

- source-first processing;
- canonical data separated from presentation;
- reproducible import pipelines;
- preservation of archival evidence;
- validation before public release.

## Relationship to the Raw Archive

This worklog summarizes themes and lessons from the chronological transcripts. Exact commands, code fragments, errors and conversation context remain in `../chronological/` and should be consulted whenever precise reconstruction is required.
