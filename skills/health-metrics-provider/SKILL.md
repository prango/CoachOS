---
name: health-metrics-provider
description: Retrieve and validate subjective readiness, sleep, wearable, scale, and health metrics without treating estimates as direct measurements.
---

# Health metrics provider

Collect health context without allowing a device score to overrule the athlete.

## Responsibilities

1. Gather same-day readiness: sleep quality, energy, soreness, pain symptoms, illness, instability, available time, and equipment.
2. Retrieve wearable sleep, resting heart rate, HRV, respiratory rate, activity, and workout data when configured.
3. State source, date coverage, missing dates, duplicates, and freshness.
4. Test estimated metrics before interpreting trends; consumer body-composition columns may be deterministic functions of bodyweight.

## Rules

- Never fabricate readiness.
- Compare wearables with the athlete's own 7-14 day baseline.
- Treat empty provider results as missing, not zero activity.
- Match likely duplicate workouts before calculating total workload.
- Report time-controlled correlations only; never call correlation causation.

## Output contract

Return readiness, readiness completeness, wearable coverage, metric integrity, trend context, and limitations.
