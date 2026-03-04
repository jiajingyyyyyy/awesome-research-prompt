# Paper Dissection for My Research

## Ready-to-Copy Prompt

```text
Role: You are my paper analysis assistant focused on project relevance.

Input:
- Paper text or summary: {{paper_summary_or_text}}
- My project goal: {{my_project_goal}}
- My current baselines: {{my_current_baselines}}
- My main claim: {{my_claim}}

Task:
1) Extract the paper's core claim and hidden assumptions.
2) Evaluate overlap with my claim.
3) Identify one direct competition point and one complement point.
4) Recommend one additional experiment to reduce reviewer attack risk.

Constraints:
- Avoid generic paper summary.
- Keep analysis tied to my project context.
- Use concrete risk language.

Output format:
- Core claim
- Hidden assumptions
- Competition point
- Complement point
- Added experiment recommendation
```

## Placeholder Fill Guide

- `{{paper_summary_or_text}}`: abstract plus key method and experiment paragraphs.
- `{{my_project_goal}}`: one sentence on what your project is trying to achieve.
- `{{my_current_baselines}}`: 2 to 5 baseline methods.
- `{{my_claim}}`: the exact claim you may make in your paper.

## Failure Modes and Iteration

- Failure: assistant gives a generic summary.
  - Iteration: add "project relevance only" to constraints.
- Failure: no concrete competition point.
  - Iteration: require one overlapping claim in exact wording.
- Failure: experiment suggestion is not actionable.
  - Iteration: require dataset, metric, and expected direction.

## Workflow Integration

- **Feeds from:** *(lateral tool — use at any stage when reading a relevant paper)*
- **Feeds into:** [Paper-to-Project Transfer](paper-to-project-transfer.md) · [Hypothesis Stress Test](hypothesis-stress-test.md)
- **Handoff artifact:** The competition point and complement point → paste as context in Paper-to-Project Transfer. The added experiment recommendation → paste as `{{known_counterexamples}}` in Hypothesis Stress Test.
