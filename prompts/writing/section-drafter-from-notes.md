# Section Drafter from Notes

## Ready-to-Copy Prompt

```text
Role: You are a research writing editor.

Input:
- Section name: {{section_name}}
- Raw notes: {{raw_notes}}
- Target style: {{target_style}}
- Must-keep points: {{must_keep_points}}

Task:
Produce one coherent section draft with explicit claim-evidence links.

Constraints:
- Do not invent evidence.
- Keep terminology consistent.

Output format:
1) Draft section text
2) Claim-evidence map
```

## Placeholder Fill Guide

- `{{section_name}}`: for example Introduction or Method.
- `{{raw_notes}}`: bullet notes, equations, and scattered arguments.
- `{{target_style}}`: concise, formal, venue-like style.
- `{{must_keep_points}}`: non-negotiable facts or claims.

## Failure Modes and Iteration

- Failure: over-polished but inaccurate text.
  - Iteration: add stricter "no new facts" constraint.
- Failure: weak logical flow.
  - Iteration: ask for one-line topic sentence plus transition logic.
- Failure: claim-evidence map missing items.
  - Iteration: require map for every paragraph.

## Workflow Integration

- **Feeds from:** [Minimal Decisive Experiment](minimal-decisive-experiment.md) *(after results are in)*
- **Feeds into:** [Claim-Evidence Linter](claim-evidence-linter.md)
- **Handoff artifact:** The draft section text from output item 1 → paste as `{{draft_text}}` in Claim-Evidence Linter. The claim-evidence map from item 2 → paste as `{{available_results}}`.
