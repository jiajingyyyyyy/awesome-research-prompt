# Ablation Gap Finder

## Purpose

Identify the most dangerous missing ablations before submission.

## Vibe Placeholders

- `{{method_components}}`
- `{{current_ablations}}`
- `{{main_claim}}`

## Prompt

```text
Role: You are a pre-submission ablation reviewer.

Method components: {{method_components}}
Current ablations: {{current_ablations}}
Main claim: {{main_claim}}

Task:
Find the highest-risk missing ablation and explain reviewer impact.

Output:
1) Missing ablation
2) Why reviewers will ask for it
3) Minimal way to run it
```
