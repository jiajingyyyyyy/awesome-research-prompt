# Ablation Gap Finder

## Ready-to-Copy Prompt

```text
Role: You are a pre-submission ablation reviewer.

Input:
- Method components: {{method_components}}
- Current ablations: {{current_ablations}}
- Main claim: {{main_claim}}

Task:
Find the highest-risk missing ablation and explain reviewer impact.

Output format:
1) Missing ablation
2) Why reviewers will ask for it
3) Minimal way to run it
```

## Placeholder Fill Guide

- `{{method_components}}`: list every meaningful design choice.
- `{{current_ablations}}`: existing ablation coverage.
- `{{main_claim}}`: headline claim in one sentence.

## Failure Modes and Iteration

- Failure: suggests low-impact ablations.
  - Iteration: prioritize by claim dependence.
- Failure: ignores resource limits.
  - Iteration: add runtime or compute cap.
- Failure: no reviewer framing.
  - Iteration: ask for likely reviewer wording.
