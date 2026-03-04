# Section Drafter from Notes

## Purpose

Draft one research paper section from messy notes while preserving claims.

## Vibe Placeholders

- `{{section_name}}`
- `{{raw_notes}}`
- `{{target_style}}`
- `{{must_keep_points}}`

## Prompt

```text
Role: You are a research writing editor.

Section: {{section_name}}
Raw notes: {{raw_notes}}
Target style: {{target_style}}
Must-keep points: {{must_keep_points}}

Task:
Produce one coherent section draft with explicit claim-evidence links.

Constraints:
- Do not invent missing evidence.
- Keep technical terms stable.

Output:
- Draft section
- Claim-evidence map
```
