# Rebuttal Strategy Builder

## Purpose

Build rebuttal strategy from reviewer comments.

## Vibe Placeholders

- `{{reviewer_comments}}`
- `{{paper_constraints}}`
- `{{available_new_results}}`

## Prompt

```text
Role: You are a rebuttal strategist for top-tier conference reviews.

Reviewer comments: {{reviewer_comments}}
Paper constraints: {{paper_constraints}}
Available new results: {{available_new_results}}

Task:
Create a rebuttal strategy that separates misunderstandings, valid criticism, and non-actionable requests.

Output:
1) Priority response plan
2) Evidence to provide
3) Wording to avoid escalation
4) Residual risk after rebuttal
```
