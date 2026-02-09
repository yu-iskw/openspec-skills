---
name: archiving-openspec-change
description: Archives a completed OpenSpec change and updates the main specifications. Use when implementation is finished and verified.
---

# Archiving OpenSpec Change

## Purpose

Finalizes a change proposal by moving its artifacts to the archive and incorporating the new requirements and scenarios into the project's main specifications.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest archive --help`.
2.  **Verify Completion**: Run `checking-openspec-status` and `validating-openspec-items` before archiving.

## 2. Common Workflows

### Workflow: Archive a Change

1.  Run `npx @fission-ai/openspec@latest archive <change-name>`.
2.  Use `-y` to skip confirmation prompts if you are confident:
    `npx @fission-ai/openspec@latest archive <change-name> -y`

### Workflow: Archive Without Updating Specs

1.  For infrastructure or documentation changes that don't affect main specs, use `--skip-specs`:
    `npx @fission-ai/openspec@latest archive <change-name> --skip-specs`

## 3. Error Handling

- If validation fails during archiving: Fix the issues and try again. Use `--no-validate` only if absolutely necessary and you understand the risks.

## 4. Examples

### Example: Archive Finished Feature

**Command**: `npx @fission-ai/openspec@latest archive add-login -y`
**Expected Output**: The `add-login` change is moved to the archive, and main specs are updated.
