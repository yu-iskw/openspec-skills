---
name: initializing-openspec
description: Initializes OpenSpec in a project directory. Use when starting a new project or adding OpenSpec to an existing one.
---

# Initializing OpenSpec

## Purpose

Standardizes the initialization of OpenSpec in a project to ensure proper configuration and tool integration.

## 1. Safety & Verification

Before initialization:

1.  **Check Help**: Run `npx @fission-ai/openspec@latest init --help` to verify the latest initialization options.
2.  **Verify Context**: Ensure you are in the intended project root.

## 2. Common Workflows

### Workflow: Basic Initialization

1.  Run `npx @fission-ai/openspec@latest init`.
2.  Follow interactive prompts (if applicable) or provide flags for non-interactive use.

### Workflow: Non-Interactive Tool Setup

1.  Specify AI tools to configure:
    `npx @fission-ai/openspec@latest init --tools cursor,claude`
2.  Use `--force` to auto-cleanup legacy files if necessary.

## 3. Error Handling

- If `command not found` occurs: Ensure Node.js is installed and use `npx`.
- If permission errors occur: Check file system permissions in the target directory.

## 4. Examples

### Example: Initialize with Cursor and Claude

**Command**: `npx @fission-ai/openspec@latest init --tools cursor,claude`
**Expected Output**: OpenSpec configuration files and instruction files (e.g., `.cursorrules`) are created.
