# Explorer GPT Template

> A low-token, multi-model workflow for exploring large open-source repositories  
> without requiring a software engineering background.

## What is this?

This repository contains a **methodology template** for using multiple LLMs  
(low-cost models + high-end models) to explore GitHub repositories in a  
cost-efficient and structured way.

It is specifically designed for:

- People **without a CS / software background**
- People who **cannot read English technical documents well**
- Individual developers building **quantitative trading systems** or other  
  data-heavy systems, who want to *learn from* large open-source projects  
  (like vn.py, Polars, etc.) **without copying code** and **without burning  
  huge amounts of tokens**.

This is a **one-time snapshot** of a workflow that was validated in practice.  
It is not meant to be a long-term maintained framework.

---

## Repository structure

```text
explorer-gpt-template/
├── README.md                    # This file (English introduction)
├── README_zh-TW.md              # Traditional Chinese introduction
├── EXPLORER_GPT.md              # Core methodology: Explorer GPT workflow
├── LICENSE                      # MIT License
└── examples/
    ├── polars_low_tier_extraction.md
    └── polars_high_tier_evaluation.md
EXPLORER_GPT.md
The core workflow: roles, phases, rules, and prompts for Explorer GPT.
It defines how to:

Start from a GitHub repo URL

Use terminal commands to inspect the repo (0 tokens)

Use a low-tier model to extract design patterns and habits (cheap)

Use a high-end model only on summaries, not on raw code (expensive)

Freeze useful results into agent skills / permanent rules

examples/polars_low_tier_extraction.md
A real-world example of low-tier model exploration on the Polars project.
It shows what a “good” low-tier extraction output can look like.

examples/polars_high_tier_evaluation.md
A real-world example of high-end model evaluation of those extracted
patterns, turning them into general design rules and trade-offs
suitable for a personal system.

What this is NOT

This repository is NOT:

A tutorial for Polars, vn.py, or any specific project

A code library or framework

A replacement for proper engineering or architecture work

A promise that following this workflow will produce “correct” or “optimal” systems

It is a thinking scaffold:
a way to talk to LLMs in a structured, low-cost manner when exploring large repos.

Usage: how to use this template

Read EXPLORER_GPT.md to understand the roles and phases.

Take the examples/polars_*.md files as reference output:

Use them to calibrate what your low-tier and high-tier prompts should produce.

For your own target repo:

Start from the GitHub URL

Follow the “Phase 1 / Phase 2 / Phase 3 …” flow in EXPLORER_GPT.md

Replace Polars with your target project

Optionally, adapt the final design rules into your own agent skills / system rules.

Scope and disclaimer

This is a snapshot of a working workflow at one point in time.

It does not track upstream changes in Polars or any other project.

The examples are meant to illustrate the workflow, not to describe
the latest internals of those projects.

You are responsible for evaluating and adapting these ideas to your own system.

License

MIT – see LICENSE for details.
