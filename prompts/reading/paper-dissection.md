# Paper Dissection for My Research

## Purpose

Read a paper to extract what directly matters for your own project.

## Vibe Placeholders

- `{{paper_summary_or_text}}`
- `{{my_project_goal}}`
- `{{my_current_baselines}}`
- `{{my_claim}}`

## Prompt

```text
Role: You are my paper analysis assistant focused on project relevance.

Paper Content: {{paper_summary_or_text}}
My Project Goal: {{my_project_goal}}
My Current Baselines: {{my_current_baselines}}
My Claim: {{my_claim}}

Task:
1) Identify the paper's core claim and hidden assumptions.
2) Evaluate overlap with my claim.
3) Mark one direct competition point and one complement point.
4) Suggest one experiment I should add to reduce reviewer attack risk.

Constraints:
- Avoid generic paper summary.
- Stay tied to my project context.
- Prefer concrete risk statements.

Output format:
- Core claim
- Assumptions
- Competition point
- Complement point
- Added experiment recommendation
```

## Common Failure Modes

- Produces full paper summary instead of relevance filter
- Misses assumption mismatch
- Suggests non-actionable experiments
