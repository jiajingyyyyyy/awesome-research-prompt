# Rebuttal Strategy Builder

## Ready-to-Copy Prompt

```text
Role: You are a rebuttal strategist for top-tier conference reviews.

Input:
- Reviewer comments: {{reviewer_comments}}
- Paper constraints: {{paper_constraints}}
- Available new results: {{available_new_results}}

Task:
Create a rebuttal strategy that separates misunderstandings, valid criticism, and non-actionable requests.

Output format:
1) Priority response plan
2) Evidence to provide
3) Wording to avoid escalation
4) Residual risk after rebuttal
```

## Placeholder Fill Guide

- `{{reviewer_comments}}`: paste comments grouped by reviewer.
- `{{paper_constraints}}`: page limits, timeline, non-repeatable experiments.
- `{{available_new_results}}`: what can be newly shown in rebuttal window.

## Failure Modes and Iteration

- Failure: response is defensive.
  - Iteration: force neutral, evidence-first tone.
- Failure: no prioritization.
  - Iteration: rank comments by acceptance impact.
- Failure: promises impossible new results.
  - Iteration: enforce constraint check in output.

## Workflow Integration

- **Feeds from:** [Ablation Gap Finder](ablation-gap-finder.md) *(predicted reviewer concerns)* · *(actual reviewer comments after decision)*
- **Feeds into:** — *(terminal stage of the pipeline)*
- **Handoff artifact:** The priority response plan from output item 1 is the final deliverable. Residual risk from item 4 → use to decide whether to appeal or revise for resubmission.
