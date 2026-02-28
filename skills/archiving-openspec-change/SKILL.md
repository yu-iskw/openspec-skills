---
name: archiving-openspec-change
description: Archives a completed OpenSpec change and updates the main specifications. Use when implementation is finished and verified.
---

# Archiving OpenSpec Change

Finalizes a change by moving its artifacts to the archive and incorporating requirements into
the project's main specifications. Before archiving, run `checking-openspec-status` and
`validating-openspec-items` to confirm the change is complete and valid.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest archive <name>` | — | Archive a completed change |
| `npx @fission-ai/openspec@latest archive <name>` | `-y` | Skip confirmation prompts |
| `npx @fission-ai/openspec@latest archive <name>` | `--skip-specs` | Archive without updating main specs |
| `npx @fission-ai/openspec@latest archive <name>` | `--no-validate` | Skip validation (use only if necessary) |
