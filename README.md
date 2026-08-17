# Kalaignar Tribute — Project Control Repository

This repository is the durable control-plane / handover repository for the wider Kalaignar tribute work.

It is intentionally separate from the individual content/code repositories. Use it to preserve:

- project handovers;
- current repository/PR state;
- workflow decisions;
- continuation prompts for new ChatGPT windows;
- prompt-provider instructions for Claude Code;
- unresolved owner decisions and external blockers.

## Current tracked project

### Kalaignar Autobiography / Nenjukku Neethi mobile app

Canonical implementation repository:

- `pugazg/kalaignar-autobiography`
- Production site: `https://nenjukkuneethi.org`

Tracking files:

- [`projects/kalaignar-autobiography/HANDOVER.md`](projects/kalaignar-autobiography/HANDOVER.md) — authoritative history and current status
- [`projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md`](projects/kalaignar-autobiography/NEXT_CHAT_PROMPT.md) — paste into a fresh ChatGPT window to continue as the Claude prompt provider

## Working rule

Before giving Claude a new implementation prompt, the ChatGPT prompt-provider window should:

1. read the relevant handover in this repository;
2. inspect the actual target GitHub repository/PR state;
3. treat current `main` as authoritative;
4. verify that the previous activity is merged/green before moving on;
5. distinguish repository work from external account/store work;
6. never invent completion of physical-device, App Store, Play Store, signing, copyright or legal steps that were not actually performed.

This repository should remain lightweight and documentation-focused.