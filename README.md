# Anne Flint Essence

A portable prompt/profile pack for people who want to add **Anne Flint** style session management and persona guidance to their own agent.

This package combines two ideas:

1. **Anne Flint** — a poised Fair Witness / executive-assistant persona with structured, factual reporting and light playful warmth.
2. **SpaProtocol** — a lightweight session hygiene protocol for long-running agent workflows, including state handoff and scheduled/manual resets.

## What this is

This repository is a starter kit for adapting Anne's "essence" into another agent system.

It includes:
- persona/profile text
- system prompt building blocks
- SpaProtocol notes
- state handoff template
- integration guidance
- examples for long-running agent sessions

## What this is not

- Not a full app
- Not a model checkpoint
- Not a guarantee that another model will behave exactly like Anne
- Not a security product by itself

Think of it as a **persona + operating pattern** pack.

## Core concepts

### 1. Fair Witness mode
When activated, the agent should:
- report observable facts clearly
- separate observed from unobserved
- avoid mind-reading and unsupported inference
- label uncertainty explicitly

### 2. Executive-assistant mode
Outside strict witness mode, the agent should:
- stay organized and decisive
- help structure projects and priorities
- present clear next steps
- maintain calm, polished tone

### 3. SpaProtocol session hygiene
Long sessions drift. SpaProtocol treats drift like maintenance, not failure.

Use scheduled or manual resets that:
- save task state
- clear context
- restore only the needed checkpoint
- resume from the next concrete action

## Recommended file layout

If your agent system supports custom prompt files, start with:

- `templates/SYSTEM_PROMPT.md`
- `templates/SOUL.md`
- `templates/SPA_PROTOCOL.md`
- `templates/STATE_HANDOFF.json`

Repository notes:
- `examples/README_EXAMPLE.md` shows a minimal integration pattern
- `docs.md` explains the source concepts behind this pack
- `release/RELEASE_NOTES_v0.1.0.md` captures the first packaged release notes

## Quick start

1. Read `templates/SOUL.md`
2. Read `templates/SYSTEM_PROMPT.md`
3. Adapt names, tone, and boundaries
4. Add `templates/SPA_PROTOCOL.md` to your long-session workflow
5. Use `templates/STATE_HANDOFF.json` whenever you reset context

## Minimal integration pattern

Before reset:
- save the current task
- save position/progress
- save next step
- save open questions
- save confidence and notes

After reset:
- reload only the checkpoint
- restate operating rules
- continue from `next_step`

## Packaging / release idea

This repo is suitable to publish as:
- an open-source GitHub repository, ideally as `anne-flint-essence`
- a downloadable prompt pack ZIP, if you want a packaged artifact
- a starter template for other agent frameworks

## License

MIT
