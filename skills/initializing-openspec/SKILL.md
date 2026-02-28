---
name: initializing-openspec
description: Initializes OpenSpec in a project directory. Use when starting a new project or adding OpenSpec to an existing one.
---

# Initializing OpenSpec

Sets up the `openspec/` directory and AI instruction files in the project. Must be run from
the intended project root.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest init` | — | Basic init |
| `npx @fission-ai/openspec@latest init` | `--tools cursor,claude` | Configure specific AI tools |
| `npx @fission-ai/openspec@latest init` | `--force` | Auto-cleanup legacy files |
