# OpenSpec Agent Skills

## Overview

This repository provides a collection of specialized **Agent Skills** and **Subagents** designed to automate the Spec-Driven Development (SDD) workflow using **OpenSpec**. These skills empower AI agents to initialize projects, manage change proposals, track artifact status, and archive completed features while maintaining high-quality specifications.

## Key Features

- **Spec-Driven Development**: Standardizes the workflow from proposal to implementation and archiving.
- **Workflow Automation**: Automates common OpenSpec CLI tasks like listing, showing, and validating changes.
- **Agent Orchestration**: Includes the `openspec-manager` subagent to guide the entire SDD process.
- **Extensible Architecture**: Built as primitive skills that can be combined or used independently.

## Agents

- **[openspec-manager](agents/openspec-manager/)**: Orchestrates the Spec-Driven Development (SDD) workflow using OpenSpec. Proactively guides the agent through proposal creation, specification, design, implementation, and archiving.

## Agent Skills

### OpenSpec Skills

- **[initializing-openspec](skills/initializing-openspec/)**: Initializes OpenSpec in a project directory.
- **[updating-openspec-instructions](skills/updating-openspec-instructions/)**: Updates OpenSpec instruction files in a project.
- **[listing-openspec-items](skills/listing-openspec-items/)**: Lists OpenSpec items such as active change proposals and specifications.
- **[viewing-openspec-item-details](skills/viewing-openspec-item-details/)**: Displays detailed information about a specific OpenSpec change or specification.
- **[checking-openspec-status](skills/checking-openspec-status/)**: Displays the completion status of artifacts for an OpenSpec change.
- **[creating-openspec-change](skills/creating-openspec-change/)**: Creates a new OpenSpec change directory and initial structure.
- **[getting-openspec-artifact-instructions](skills/getting-openspec-artifact-instructions/)**: Outputs enriched instructions for creating an artifact or applying tasks for an OpenSpec change.
- **[validating-openspec-items](skills/validating-openspec-items/)**: Validates OpenSpec changes and specifications against their schemas.
- **[archiving-openspec-change](skills/archiving-openspec-change/)**: Archives a completed OpenSpec change and updates the main specifications.

### Internal Agent Skills

- **[implementing-agent-skills](.cursor/skills/implementing-agent-skills/)**: Implements new Agent Skills for the project, ensuring specification compliance.
- **[lint-and-fix](.cursor/skills/lint-and-fix/)**: Autonomous loop to format the codebase, run linters, and fix violations.

## Development

This project uses `uv` for dependency management and `trunk` for linting and formatting.

### Useful Commands

- `make format`: Format the codebase using `trunk fmt`.
- `make lint`: Check for linting issues using `trunk check`.
- `make validate`: Validate all agent skills using `scripts/validate_agent_skills.sh`.
