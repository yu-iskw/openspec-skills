---
name: viewing-openspec-item-details
description: Displays detailed information about a specific OpenSpec change or specification. Use when you need to read the content of a proposal or spec.
---

# Viewing OpenSpec Item Details

## Purpose

Retrieves the full content or specific parts of an OpenSpec change proposal or specification.

## 1. Safety & Verification

1.  **Check Help**: Run `npx @fission-ai/openspec@latest show --help`.
2.  **Verify Item Existence**: Use `listing-openspec-items` to find the correct name/ID.

## 2. Common Workflows

### Workflow: Show Change Content

1.  Run `npx @fission-ai/openspec@latest show <change-name>`.

### Workflow: Show Spec Content

1.  Run `npx @fission-ai/openspec@latest show --type spec <spec-id>`.

### Workflow: Extract Specific Requirements (JSON)

1.  Use `--json` and `--requirement <id>` to get a specific requirement:
    `npx @fission-ai/openspec@latest show <item-name> --json --requirement 1`

## 3. Examples

### Example: View Only Deltas of a Change

**Command**: `npx @fission-ai/openspec@latest show my-feature --deltas-only`
**Expected Output**: The requirements and scenarios that are changing in the proposal.
