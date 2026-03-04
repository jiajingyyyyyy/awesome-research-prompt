# Research Prompt Toolkit

A practical toolkit for researchers: ready-to-use prompt templates plus a composable method to build new prompts for new research scenarios.

## Start Here

- Direct use: open [prompts/catalog.md](prompts/catalog.md)
- Adapt use: edit placeholders inside each prompt file
- Build new: read [docs/how-to-vibe.md](docs/how-to-vibe.md)

## Prompt Coverage by Research Stage

| Stage | Representative Prompts |
|---|---|
| Idea | Idea Discussion Partner, Research Question Narrower |
| Reading | Paper Dissection for My Research, Paper-to-Project Transfer |
| Design | Hypothesis Stress Test, Minimal Decisive Experiment |
| Writing | Section Drafter from Notes, Claim-Evidence Linter |
| Revision | Ablation Gap Finder, Rebuttal Strategy Builder |

## Repository Structure

```text
prompts/
  catalog.md                      # stage index and quick entry
  idea/                           # problem framing and narrowing
  reading/                        # paper analysis and transfer
  design/                         # hypothesis and experiment design
  writing/                        # drafting and claim-evidence checks
  revision/                       # ablation and rebuttal support

docs/
  how-to-vibe.md                  # composition method when no template fits
  vibe-placeholder-skills.md      # placeholder reference (summary)
  vibeable-research-map.md        # stage map (short reference)
```

## Why This Toolkit Exists

Most researchers ask one question first: "I need help now, which prompt should I use?"
This repo answers that first, then gives a composition method for cases not covered by existing prompts.

## Contributing

A prompt contribution should include:

1. Placeholder set used
2. Output contract
3. Failure modes
4. One reproducible example

## Acknowledgements

This project is inspired by open prompt-sharing efforts in the research community, especially:

- https://github.com/Leey21/awesome-ai-research-writing

## License

MIT is recommended unless you need another license.
