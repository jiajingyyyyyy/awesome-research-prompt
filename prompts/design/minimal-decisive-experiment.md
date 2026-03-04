# Minimal Decisive Experiment

## Ready-to-Copy Prompt

```text
Role: You are an experiment planner optimizing decision value per cost.

Input:
- Research question: {{research_question}}
- Decision needed: {{decision_needed}}
- Resource limit: {{resource_limit}}

Task:
Design one minimal experiment that can decide the next step.

Output format:
1) Setup
2) Decision rule
3) Success threshold
4) Failure interpretation
```

## Placeholder Fill Guide

- `{{research_question}}`: the specific uncertainty to resolve.
- `{{decision_needed}}`: what you will do differently after the result.
- `{{resource_limit}}`: hard budget on time, compute, or annotation.

## Failure Modes and Iteration

- Failure: experiment is too large.
  - Iteration: force single dataset or single metric.
- Failure: decision rule is vague.
  - Iteration: require explicit threshold.
- Failure: failure interpretation is missing.
  - Iteration: require one fallback action.
