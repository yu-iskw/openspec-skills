---
name: updating-openspec-instructions
description: Updates OpenSpec instruction files in a project. Use when OpenSpec is already initialized but instructions need refreshing or the CLI was updated.
---

# Updating OpenSpec Instructions

## Purpose

Ensures that the AI agent's instruction files (e.g., `.cursorrules`, `claude.json`) are up-to-date with the latest OpenSpec standards and project configuration.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest update --help`.
2.  **Verify Initialization**: Ensure OpenSpec has already been initialized in the project (check for `openspec/` directory).

## 2. Common Workflows

### Workflow: Refresh Instructions

1.  Run `npx @fission-ai/openspec@latest update`.
2.  Use `--force` to overwrite existing instructions even if they appear up-to-date.

## 3. Error Handling

- If the command fails because OpenSpec is not initialized: Run `initializing-openspec` first.

## 4. Examples

### Example: Force Update Instructions

**Command**: `npx @fission-ai/openspec@latest update --force`
**Expected Output**: Updated instruction files in the project root or `.cursor/` directory.
