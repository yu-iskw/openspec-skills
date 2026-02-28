---
name: viewing-openspec-item-details
description: Displays detailed information about a specific OpenSpec change or specification. Use when you need to read the content of a proposal or spec.
---

# Viewing OpenSpec Item Details

Retrieves the full content or specific parts of a change proposal or specification. Use
`listing-openspec-items` first to find the correct name or ID.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest show <name>` | — | Show change content |
| `npx @fission-ai/openspec@latest show <name>` | `--type spec` | Show a specification |
| `npx @fission-ai/openspec@latest show <name>` | `--json --requirement <id>` | Extract a specific requirement |
| `npx @fission-ai/openspec@latest show <name>` | `--deltas-only` | Show only differing requirements |
