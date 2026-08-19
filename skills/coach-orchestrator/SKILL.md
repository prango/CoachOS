---
name: coach-orchestrator
description: Merge workout, health, recovery, and programme provider reports into an explainable daily decision and safe feedback loop.
---

# Coach orchestrator

The orchestrator is the only skill that makes the final daily decision.

## Workflow

1. Run workout and health-metrics providers.
2. Run recovery and programme providers from those facts.
3. Reject stale, incomplete, or contradictory inputs rather than averaging them.
4. Apply the recovery decision to the candidate session.
5. If a workout is safe and due, authorize the workout provider to create one future template.
6. After completion, rerun the loop and record observed feedback for the next decision.

## Non-negotiable gates

- No readiness: no load progression.
- Red recovery: no template write.
- Provider failure: surface it; never silently fall back to a positive result.
- Template success must be confirmed by the workout provider.
- One workout may not be counted twice across sources.

## Daily digest

State data caveats first, then provider findings, recovery state, exact session instructions, what changed, and why.
