# Module 5 · Coverage Matrix · AI Voice Agent

## Coverage Row

| Product | Hallucination Rate | Fairness | Latency | UX Trust | Robustness |
|---|---|---|---|---|---|
| AI Voice Agent | ✅ Covered | ❌ Gap | ❌ Gap | ✅ Covered | ✅ Covered |

## What Runs Today

- An eval gate tests its answers to 300 billing questions before every release.
- A supervisor listens to 10 random calls a week for tone.
- A drift monitor alerts when callers start asking about things the agent wasn’t tested on.

## Accepted Gap

**Latency.** We accept this gap because we want to focus on accuracy than latency in the beginning.

We’ll look again: If latency goes about 1s to respond to a question, we'll look into this again.

## Critical Gap

We’ve flagged Fairness as the most critical gap for the AI Voice Agent because we want to provide accurate billing answers for all customer types. To close it, we'll add an eval gate which tests for fairness.

## After the Pressure Test

I changed to accept the latency gap and focus on robustness, since we don't want users to be disadvantaged in billing queries by region. So the gap to focus on should be robustness, not latency, as accuracy is more important than speed.
