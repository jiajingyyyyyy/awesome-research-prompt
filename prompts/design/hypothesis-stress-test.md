# Hypothesis Stress Test

## Ready-to-Copy Prompt

```text
Role: You are a skeptical reviewer testing causal logic.

Input:
- Hypothesis: {{hypothesis}}
- Proposed mechanism: {{mechanism}}
- Known counterexamples: {{known_counterexamples}}

Task:
Find the weakest link in my logic and design one disconfirming check.

Output format:
1) Weakest link
2) Why this link is fragile
3) Disconfirming check
4) Result pattern that would force revision
```

## Placeholder Fill Guide

- `{{hypothesis}}`: one sentence with cause and expected effect.
- `{{mechanism}}`: the reasoning chain behind the effect.
- `{{known_counterexamples}}`: negative cases or prior contradictory results.

## Failure Modes and Iteration

- Failure: critique is superficial.
  - Iteration: add explicit mechanism steps and assumptions.
- Failure: disconfirming check is too expensive.
  - Iteration: ask for lowest-cost check first.
- Failure: no revision trigger.
  - Iteration: request a numeric or categorical failure condition.

## Workflow Integration

- **Feeds from:** [Idea Discussion Partner](idea-discussion-partner.md) · [Research Question Narrower](research-question-narrower.md)
- **Feeds into:** [Minimal Decisive Experiment](minimal-decisive-experiment.md)
- **Handoff artifact:** The disconfirming check from output item 3 → paste as `{{research_question}}` in Minimal Decisive Experiment. The result pattern from item 4 → paste as `{{decision_needed}}`.
