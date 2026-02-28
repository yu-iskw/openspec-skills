---
name: checking-openspec-status
description: Displays the completion status of artifacts for an OpenSpec change. Use to track progress of proposal, specs, design, and tasks.
---

# Checking OpenSpec Status

Shows which artifacts (`proposal.md`, `specs/`, `design.md`, `tasks.md`) are complete or
pending for a given change.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest status --change <name>` | — | Show artifact completion status |
| `npx @fission-ai/openspec@latest status --change <name>` | `--json` | Output as JSON |
