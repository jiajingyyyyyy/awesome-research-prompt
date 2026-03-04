# How to Vibe a Prompt

This is the method document for composing prompts when `prompts/catalog.md` does not contain an exact match.

## What "vibe" means in this repository

"Vibe" is a verb: compose a context-aware prompt quickly with structured placeholders.
It is not a style label and not a replacement for evidence.

## Composition Workflow

## Step 1: Pin the research stage

Set:
- `{{research_stage}}` = idea / reading / design / writing / revision

This controls prompt intent and output contract.

## Step 2: Define the task boundary

Set:
- `{{task_goal}}`
- `{{input_scope}}`
- `{{output_depth}}`

Rule:
If the task cannot be written in one sentence, the scope is too broad.

## Step 3: Define quality target

Set:
- `{{quality_criteria}}`
- `{{acceptance_checks}}`

Rule:
Quality criteria must be observable in the output.

## Step 4: Define hard constraints

Set:
- `{{hard_constraints}}`
- `{{forbidden_patterns}}`

Rule:
Hard constraints protect against hallucination and scope drift.

## Step 5: Define workflow handoff

Set:
- `{{current_stage}}`
- `{{next_stage}}`
- `{{handoff_artifact}}`

Rule:
Every prompt should produce an artifact that can be used by the next stage.

## Canonical Composition Template

```text
Role: {{role}}
Task: {{task_goal}}
Input Scope: {{input_scope}}
Quality Criteria: {{quality_criteria}}
Hard Constraints: {{hard_constraints}}
Output Contract: {{output_contract}}
Current Stage: {{current_stage}}
Next Stage: {{next_stage}}
Handoff Artifact: {{handoff_artifact}}
```

## Fast Adaptation Patterns

- If output is generic: tighten `{{input_scope}}` and `{{quality_criteria}}`.
- If output is unstable: strengthen `{{output_contract}}` and add examples.
- If output drifts from facts: add stricter `{{hard_constraints}}`.
- If output is too verbose: lower `{{output_depth}}`.

## Non-Negotiable Rule

Prompt vibing may change framing and structure.
It must not change factual evidence.

## Relationship to Other Docs

- Use `prompts/catalog.md` to find an existing prompt first.
- Use this doc only when you need to compose or heavily adapt one.
