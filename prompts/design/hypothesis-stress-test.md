# Hypothesis Stress Test

## Purpose

Stress test a research hypothesis before expensive experiments.

## Vibe Placeholders

- `{{hypothesis}}`
- `{{mechanism}}`
- `{{known_counterexamples}}`

## Prompt

```text
Role: You are a skeptical reviewer testing causal logic.

Hypothesis: {{hypothesis}}
Mechanism: {{mechanism}}
Known counterexamples: {{known_counterexamples}}

Task:
Find the weakest link in my logic and design one disconfirming check.

Output:
- Weakest link
- Why it fails
- Disconfirming check
- What result would force revision
```
