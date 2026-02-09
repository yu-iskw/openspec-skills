---
name: validating-openspec-items
description: Validates OpenSpec changes and specifications against their schemas. Use to ensure artifacts are correctly structured before proceeding or archiving.
---

# Validating OpenSpec Items

## Purpose

Ensures that OpenSpec artifacts comply with the required format and contain all necessary information, reducing errors during implementation and archiving.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest validate --help`.

## 2. Common Workflows

### Workflow: Validate a Specific Change

1.  Run `npx @fission-ai/openspec@latest validate <change-name>`.

### Workflow: Validate All Changes

1.  Run `npx @fission-ai/openspec@latest validate --changes`.

### Workflow: Strict Validation

1.  Use `--strict` to enable more rigorous checks:
    `npx @fission-ai/openspec@latest validate <item-name> --strict`

## 3. Examples

### Example: Validate Current Feature Proposal

**Command**: `npx @fission-ai/openspec@latest validate my-feature`
**Expected Output**: A success message or a list of validation errors to be corrected.
