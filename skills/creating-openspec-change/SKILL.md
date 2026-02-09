---
name: creating-openspec-change
description: Creates a new OpenSpec change directory and initial structure. Use when starting a new feature, bugfix, or refactor.
---

# Creating OpenSpec Change

## Purpose

Initializes a new change proposal directory with the standard OpenSpec structure, enabling spec-driven development for a new task.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest new change --help`.
2.  **Naming**: Use a slug-style name (e.g., `add-dark-mode`).

## 2. Common Workflows

### Workflow: Start a New Change

1.  Run `npx @fission-ai/openspec@latest new change <name>`.
2.  This creates a directory under `openspec/changes/<name>/`.

## 3. Error Handling

- If the directory already exists: Choose a different name or manually manage the existing directory.

## 4. Examples

### Example: Create a New Feature Proposal

**Command**: `npx @fission-ai/openspec@latest new change user-auth`
**Expected Output**: A new directory `openspec/changes/user-auth/` is created with initial template files.
