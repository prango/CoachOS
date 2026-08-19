---
name: workout-provider
description: Read and normalize workout history, record completed sessions, and create future workout templates only after orchestrator authorization.
---

# Workout provider

Provide trustworthy workout facts to the coaching loop.

## Responsibilities

1. Sync and normalize workout history.
2. Separate completed, confirmed sessions from planned or unconfirmed sessions.
3. Return exercises, working sets, reps, load, duration, timestamps, and only truly logged RIR or rest data.
4. Identify the newest completed session and overlapping muscles with the next candidate workout.
5. Write at most one future template per local day, only with explicit orchestrator authorization.

## Rules

- Never alter completed history.
- Never invent weights, RIR, rest, duration, or completion status.
- Treat missing data as missing, not zero.
- Validate exercises against configured constraints before writing.
- Return the provider write result, not an assumed success.

## Output contract

Return status, data coverage, completed-session facts, planned-session facts, integrity warnings, and a write result of not-attempted, created, or failed.
