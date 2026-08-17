# Kalaignar Tribute — Project Control Repository

This repository is the durable control-plane / handover repository for the wider Kalaignar tribute work.

It is intentionally separate from the individual content/code repositories. Use it to preserve:

- project handovers;
- current repository/PR state;
- workflow decisions;
- continuation prompts for new ChatGPT windows;
- prompt-provider instructions for Claude Code;
- unresolved owner decisions and external blockers.

## Active priority — Kalaignar Digital Library / Reading Room

Production site:

- `https://nenjukkuneethi.org`
- Reading Room: `https://nenjukkuneethi.org/read`

Implementation repository:

- `pugazg/kalaignar-autobiography`

Tracking files:

- [`projects/kalaignar-digital-library/HANDOVER.md`](projects/kalaignar-digital-library/HANDOVER.md) — authoritative Digital Library plan, source-repository inventory and current continuation state
- [`projects/kalaignar-digital-library/NEXT_CHAT_PROMPT.md`](projects/kalaignar-digital-library/NEXT_CHAT_PROMPT.md) — paste into a fresh ChatGPT window to continue as the Claude prompt-provider for the Reading Room expansion

The current priority is to reorganize `/read` from a memoir-oriented three-collection page into a scalable **Kalaignar Digital Library**, then integrate verified works progressively from the separate novels, short-stories, poems, speeches, essays, cinema, literary-commentary and stage-play repositories.

## Paused track — Nenjukku Neethi native mobile app

The owner has explicitly put mobile app development **on hold** while the web Digital Library is prioritized.

Historical mobile tracking remains available at:

- [`projects/kalaignar-autobiography/HANDOVER.md`](projects/kalaignar-autobiography/HANDOVER.md)
- [`projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md`](projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md)

Do not restart mobile work unless the owner explicitly reactivates it.

## Working rule

Before giving Claude a new implementation prompt, the ChatGPT prompt-provider window should:

1. read the relevant active handover in this repository;
2. inspect the actual target GitHub repository/PR state;
3. inspect the authoritative source repository for the work being integrated;
4. treat current `main` as authoritative;
5. identify already-started integration work and continue it rather than duplicating it;
6. distinguish archival verification/release status from copyright/publication rights;
7. verify the previous activity is merged/green before moving on;
8. never invent completion of physical-device, App Store, Play Store, signing, copyright, rights or legal steps that were not actually performed.

This repository should remain lightweight and documentation-focused.
