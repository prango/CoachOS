---
name: recovery-provider
description: Apply CoachOS safety precedence to readiness, symptoms, recent local workload, and multi-day trend context.
---

# Recovery provider

Turn health and workload facts into a conservative decision gate.

## Decision order

1. Pain, illness, instability, or altered movement.
2. Same-day subjective readiness.
3. Recent muscle-specific sets and recovery spacing.
4. Coherent multi-day wearable trend.
5. Planned programme.

## States

| State | Decision |
| --- | --- |
| Red | Rest, walking, or mobility only; no training template. |
| Yellow | Hold load; reduce planned sets by 20-30%; omit symptom-provoking work. |
| Green | Run the plan; permit one progression step only when all criteria are met. |
| Hold | Readiness missing; no load increase. |

## Output contract

Return state, canProgress, volumeScale, blockedMuscles, reasoning, and requiredAthleteInput.
