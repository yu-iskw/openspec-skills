---
name: validating-openspec-items
description: Validates OpenSpec changes and specifications against their schemas. Use to ensure artifacts are correctly structured before proceeding or archiving.
---

# Validating OpenSpec Items

Checks that OpenSpec artifacts comply with the required format and contain all necessary
information.

## Commands

| Command | Flags | Notes |
|---------|-------|-------|
| `npx @fission-ai/openspec@latest validate <name>` | — | Validate a specific change |
| `npx @fission-ai/openspec@latest validate` | `--changes` | Validate all changes |
| `npx @fission-ai/openspec@latest validate <name>` | `--strict` | Enable rigorous checks |
