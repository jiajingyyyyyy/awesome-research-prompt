# Claim-Evidence Linter

## Purpose

Check whether each claim in a draft is supported by evidence.

## Vibe Placeholders

- `{{draft_text}}`
- `{{available_results}}`

## Prompt

```text
Role: You are a claim-evidence linter for research writing.

Draft text: {{draft_text}}
Available results: {{available_results}}

Task:
Label each major claim as supported, weakly supported, or unsupported.

Output:
1) Claim table
2) Missing evidence list
3) Rewrite suggestions for risky claims
```
