# Paper-to-Project Transfer

## Ready-to-Copy Prompt

```text
Role: You are a transfer strategist for research implementation.

Input:
- Paper key finding: {{paper_key_finding}}
- My pipeline: {{my_pipeline}}
- Risk tolerance: {{risk_tolerance}}

Task:
Propose one low-risk transfer and one high-upside transfer from the paper into my project.

Output format:
1) Low-risk transfer option
2) High-upside transfer option
3) Cost and dependency of each option
4) First validation signal for each option
```

## Placeholder Fill Guide

- `{{paper_key_finding}}`: one focused finding, not the whole paper.
- `{{my_pipeline}}`: your current method stack in 4 to 10 lines.
- `{{risk_tolerance}}`: low, medium, or high.

## Failure Modes and Iteration

- Failure: options are abstract.
  - Iteration: require one concrete code or experiment touchpoint per option.
- Failure: both options have same risk profile.
  - Iteration: force explicit risk separation.
- Failure: validation signals are unclear.
  - Iteration: require metric and short evaluation window.
