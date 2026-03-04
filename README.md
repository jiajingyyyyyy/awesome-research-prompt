# Vibe Skill
> Make AI Research Better for Everyone

## Core Insight

As AI gets stronger, researchers get better at improvising prompts.
A fixed template is often weaker than a prompt that is composed for the exact context.

This project treats prompting as a skill system.
The contribution is a reusable library of visible **Vibe Placeholder Skills** plus a complete list of research prompts built from that system.

## Two Kinds of Placeholders in This Repo

### 1) Prompt-Composition Placeholders
These are placeholders used to generate high-quality prompts.
Examples: `{{task_goal}}`, `{{quality_criteria}}`, `{{hard_constraints}}`.

### 2) Research-Scope Placeholders
These define which parts of research work are suitable for prompt-vibing.
Examples: `{{research_stage}}`, `{{artifact_type}}`, `{{decision_risk}}`.

See:
- [Vibe Placeholder Skills](docs/vibe-placeholder-skills.md)
- [Vibeable Research Map](docs/vibeable-research-map.md)

## Complete Prompt List

This repository includes a full prompt catalog organized by research workflow.

- [Prompt Catalog](prompts/catalog.md)
- Mandatory prompts requested by this project direction:
  - [Idea Discussion Partner](prompts/idea/idea-discussion-partner.md)
  - [Paper Dissection for My Research](prompts/reading/paper-dissection.md)

## What Makes This Repo Different

- Placeholder-first instead of template-first
- Workflow-aware instead of isolated prompts
- Built for adaptation across models and domains
- Includes required prompts for paper reading and idea discussion

## Quick Start

1. Choose a research task from [Prompt Catalog](prompts/catalog.md).
2. Fill the placeholders for your own context.
3. Run one pass.
4. Use the failure-mode notes to iterate.

## Repository Layout

```text
prompts/
  catalog.md
  idea/
  reading/
  design/
  writing/
  revision/

docs/
  vibe-placeholder-skills.md
  vibeable-research-map.md
```

## Contributing

To contribute a new prompt, include:
1. Placeholder set
2. Output contract
3. Failure modes
4. One reproducible example

## License

MIT is recommended unless you need another license.
