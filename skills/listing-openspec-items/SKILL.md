---
name: listing-openspec-items
description: Lists OpenSpec items such as active change proposals and specifications. Use to discover what changes are in progress or what specs exist.
---

# Listing OpenSpec Items

## Purpose

Provides visibility into the current state of OpenSpec artifacts (changes and specs) within the project.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest list --help`.

## 2. Common Workflows

### Workflow: List Active Changes

1.  Run `npx @fission-ai/openspec@latest list` (defaults to changes).
2.  By default, items are sorted by recent activity.

### Workflow: List All Specifications

1.  Run `npx @fission-ai/openspec@latest list --specs`.

### Workflow: Programmatic Listing

1.  Use `--json` for structured output:
    `npx @fission-ai/openspec@latest list --json`

## 3. Examples

### Example: List Specs Sorted by Name

**Command**: `npx @fission-ai/openspec@latest list --specs --sort name`
**Expected Output**: A list of all specifications in alphabetical order.
