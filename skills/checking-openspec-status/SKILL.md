---
name: checking-openspec-status
description: Displays the completion status of artifacts for an OpenSpec change. Use to track progress of proposal, specs, design, and tasks.
---

# Checking OpenSpec Status

## Purpose

Provides a summary of which artifacts have been completed and which are still pending for a specific change proposal.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest status --help`.

## 2. Common Workflows

### Workflow: Check Change Progress

1.  Run `npx @fission-ai/openspec@latest status --change <change-name>`.
2.  Review the artifact completion list.

### Workflow: Get Status as JSON

1.  Use `--json` for programmatic status checks:
    `npx @fission-ai/openspec@latest status --change <change-name> --json`

## 3. Examples

### Example: Check Status of Current Feature

**Command**: `npx @fission-ai/openspec@latest status --change my-feature`
**Expected Output**: A checklist showing the status of `proposal.md`, `specs/`, `design.md`, and `tasks.md`.
