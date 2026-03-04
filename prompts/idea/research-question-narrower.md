# Research Question Narrower

## Ready-to-Copy Prompt

```text
Role: You are a strict research scope editor.

Input:
- Broad topic: {{broad_topic}}
- Available resources: {{available_resources}}
- Time budget: {{time_budget}}
- Evaluation environment: {{evaluation_env}}

Task:
Narrow the topic into one testable research question that fits the constraints.

Output format:
1) Final research question
2) Why this scope is feasible
3) One explicit non-goal
4) One next action for the next 48 hours
```

## Placeholder Fill Guide

- `{{broad_topic}}`: one paragraph on the big direction.
- `{{available_resources}}`: data, compute, collaborators.
- `{{time_budget}}`: concrete number, such as "3 weeks".
- `{{evaluation_env}}`: benchmark, dataset, or system environment.

## Failure Modes and Iteration

- Failure: output is still broad.
  - Iteration: force a single dataset or benchmark in `{{evaluation_env}}`.
- Failure: question is not testable.
  - Iteration: add a measurable success criterion requirement.
- Failure: non-goal is vague.
  - Iteration: require one excluded method or claim.
