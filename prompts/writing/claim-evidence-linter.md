# Claim-Evidence Linter

## Ready-to-Copy Prompt

```text
Role: You are a claim-evidence linter for research writing.

Input:
- Draft text: {{draft_text}}
- Available results: {{available_results}}

Task:
Label each major claim as supported, weakly supported, or unsupported.

Output format:
1) Claim table with support label
2) Missing evidence list
3) Rewrite suggestions for risky claims
```

## Placeholder Fill Guide

- `{{draft_text}}`: one section or multiple paragraphs.
- `{{available_results}}`: tables, figures, metrics, and ablation outcomes.

## Failure Modes and Iteration

- Failure: labels are too lenient.
  - Iteration: ask for strict reviewer standard.
- Failure: missing evidence list is generic.
  - Iteration: require evidence item per claim.
- Failure: rewrite suggestions change meaning.
  - Iteration: require semantic preservation.
