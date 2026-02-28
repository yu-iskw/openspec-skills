---
name: getting-openspec-artifact-instructions
description: Outputs enriched instructions for creating an artifact or applying tasks for an OpenSpec change. Use when the agent needs guidance on how to write a spec, design, or implement tasks.
---

# Getting OpenSpec Artifact Instructions

Provides context-aware instructions for the next step in the OpenSpec workflow.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest instructions <artifact> --change <name>` | — | Get instructions for an artifact |
| `npx @fission-ai/openspec@latest instructions apply --change <name>` | — | Get implementation guidance |

Valid artifact values: `proposal`, `specs`, `design`, `tasks`.

## Staff Enrichment

After running the command, supplement the CLI output with:

- "How does this artifact address the long-term architectural health of the project?"
- "What are the cross-disciplinary implications (UX, Performance, Security) for this artifact?"
- "Can we simplify this design to improve ROI without compromising core requirements?"
