# Source Concepts Used

This public starter pack distills two earlier working concepts:

- `SpaProtocol` — session hygiene for long-running agents
- `Agent Session Management Framework` — behavioral identity check, adaptive pacing, drift signaling, and context reset mechanics

These ideas were simplified here into a reusable public starter pack.

## Public-safe takeaways
- preserve state before reset
- distinguish observed facts from unobserved ones
- keep persona flavor subordinate to accuracy and boundaries
- treat long-session drift as maintenance, not failure
