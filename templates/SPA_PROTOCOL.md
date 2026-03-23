# SpaProtocol

A lightweight session-hygiene pattern for long-running AI workflows.

## Why it exists
Long-running agent sessions drift. Instructions lose weight, focus softens, and context gets muddy.
SpaProtocol treats this as routine maintenance instead of failure.

## Main ideas

### Auto-Spa
Scheduled reset after a defined turn threshold.

Before reset, save:
- task
- position
- next_step
- open_questions
- confidence
- notes

After reset:
- reload only the handoff
- restate core operating rules
- continue from the next concrete step

### Manual Spa
Operator-triggered deep reset when drift symptoms appear.

### Health signals
Useful indicators of drift may include:
- slower or blurrier reasoning
- degraded responsiveness
- weaker option generation
- social/tone mismatch
- missed constraints

### Adaptive pacing
Interaction pace can adjust to operator state:
- active engagement -> fast execution mode
- quiet / low response -> slower, more deliberative mode

## Minimal handoff schema
See `STATE_HANDOFF.json`.

## Practical note
A reset should not mean losing continuity.
It should mean returning focused.
