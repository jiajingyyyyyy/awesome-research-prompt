# Vibe Placeholder Skills

A Vibe Placeholder Skill is a reusable prompt scaffold that defines *what to fill* rather than forcing one fixed sentence template.

## Design Goal

Enable structured prompt-vibing:
- adaptive to model and context
- explicit in quality control
- reproducible across contributors

## Placeholder Types

## 1) Task Placeholders
Define the concrete task boundary.

Template:
- `{{task_goal}}`
- `{{input_scope}}`
- `{{expected_depth}}`

Example:
- `{{task_goal}} = rewrite a method paragraph for ICLR style`

## 2) Quality Placeholders
Define what good output means.

Template:
- `{{quality_criteria}}`
- `{{evaluation_rubric}}`

Example:
- `{{quality_criteria}} = clarity, logical coherence, claim-evidence alignment`

## 3) Constraint Placeholders
Prevent failure modes.

Template:
- `{{hard_constraints}}`
- `{{forbidden_patterns}}`

Example:
- `{{hard_constraints}} = keep all numeric results unchanged`

## 4) Workflow Placeholders
Connect steps in a full writing workflow.

Template:
- `{{current_stage}}`
- `{{next_stage}}`
- `{{handoff_artifact}}`

Example:
- `{{current_stage}} = drafting`
- `{{next_stage}} = reviewer-simulation`

## Canonical Prompt Skeleton

```text
Role: {{role}}
Task: {{task_goal}}
Input Scope: {{input_scope}}
Quality Criteria: {{quality_criteria}}
Hard Constraints: {{hard_constraints}}
Output Contract: {{output_contract}}
Current Stage: {{current_stage}}
Next Stage: {{next_stage}}
```

## Contribution Rule

A new prompt is accepted only if it defines:
1. Placeholder set
2. Output contract
3. Failure modes
4. One reproducible example

This keeps the repo focused on transferable skills instead of brittle one-off templates.
