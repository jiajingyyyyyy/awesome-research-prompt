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

## Workflow Integration

- **Feeds from:** [Claim-Evidence Linter](claim-evidence-linter.md)
- **Feeds into:** [Rebuttal Strategy Builder](rebuttal-strategy-builder.md) *(if submission is rejected)*
- **Handoff artifact:** The missing ablation from output item 1 + reviewer framing from item 2 → paste as part of `{{reviewer_comments}}` in Rebuttal Strategy Builder if you received this as actual reviewer feedback.
