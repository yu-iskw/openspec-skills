---
name: updating-openspec-instructions
description: Updates OpenSpec instruction files in a project. Use when OpenSpec is already initialized but instructions need refreshing or the CLI was updated.
---

# Updating OpenSpec Instructions

Refreshes AI instruction files (e.g., `.cursorrules`, `claude.json`) with the latest OpenSpec
standards. Requires `initializing-openspec` to have been run first.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest update` | — | Refresh instruction files |
| `npx @fission-ai/openspec@latest update` | `--force` | Overwrite even if up-to-date |
