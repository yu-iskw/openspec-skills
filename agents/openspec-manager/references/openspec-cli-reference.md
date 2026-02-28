# OpenSpec CLI Reference

Base command: `npx @fission-ai/openspec@latest`

All subcommands support `--help` for usage details.

---

## Subcommands

### `init` — Initialize OpenSpec

```
npx @fission-ai/openspec@latest init [flags]
```

| Flag | Description |
|------|-------------|
| `--tools <list>` | Comma-separated AI tools to configure (e.g., `cursor,claude`) |
| `--force` | Auto-cleanup legacy files |

**Run from the intended project root.** Creates `openspec/` directory and AI instruction files
(e.g., `.cursorrules`, `claude.json`).

---

### `update` — Update Instruction Files

```
npx @fission-ai/openspec@latest update [flags]
```

| Flag | Description |
|------|-------------|
| `--force` | Overwrite even if files are already up-to-date |

Requires OpenSpec to already be initialized (`openspec/` directory must exist).

---

### `list` — List OpenSpec Items

```
npx @fission-ai/openspec@latest list [flags]
```

| Flag | Description |
|------|-------------|
| `--specs` | List specifications instead of active changes |
| `--json` | Output as JSON |
| `--sort name` | Sort by name (default: recent activity) |

---

### `show` — View Item Details

```
npx @fission-ai/openspec@latest show <item-name> [flags]
```

| Flag | Description |
|------|-------------|
| `--type spec` | Treat item as a specification (vs. a change) |
| `--json` | Output as JSON |
| `--requirement <id>` | Extract a specific requirement by ID |
| `--deltas-only` | Show only requirements that differ from the base |

Use `list` first to find the correct `<item-name>`.

---

### `status` — Check Change Progress

```
npx @fission-ai/openspec@latest status --change <change-name> [flags]
```

| Flag | Description |
|------|-------------|
| `--change <name>` | **(Required)** The change to inspect |
| `--json` | Output as JSON |

Shows completion status of: `proposal.md`, `specs/`, `design.md`, `tasks.md`.

---

### `new change` — Create a Change

```
npx @fission-ai/openspec@latest new change <name>
```

Creates `openspec/changes/<name>/` with the standard directory structure. Use slug-style
names (e.g., `add-dark-mode`, `user-auth`).

---

### `instructions` — Get Artifact Instructions

```
npx @fission-ai/openspec@latest instructions <artifact> --change <change-name>
npx @fission-ai/openspec@latest instructions apply --change <change-name>
```

| Artifact | Description |
|----------|-------------|
| `proposal` | Instructions for writing the change proposal |
| `specs` | Instructions for writing specifications |
| `design` | Instructions for writing the technical design |
| `tasks` | Instructions for defining implementation tasks |
| `apply` | Guidance for implementing the tasks |

---

### `validate` — Validate Items

```
npx @fission-ai/openspec@latest validate <item-name> [flags]
```

| Flag | Description |
|------|-------------|
| `--changes` | Validate all changes (no `<item-name>` needed) |
| `--strict` | Enable more rigorous validation checks |

---

### `archive` — Archive a Change

```
npx @fission-ai/openspec@latest archive <change-name> [flags]
```

| Flag | Description |
|------|-------------|
| `-y` | Skip confirmation prompts |
| `--skip-specs` | Archive without updating main specifications |
| `--no-validate` | Skip validation (use only when absolutely necessary) |

**Before archiving:** run `status` and `validate` to confirm the change is complete and valid.

---

## Common Error Patterns

| Error | Cause | Fix |
|-------|-------|-----|
| `command not found` / permission error | npx not available or permissions issue | Verify Node.js and npm are installed |
| `OpenSpec not initialized` | `openspec/` directory missing | Run `init` first |
| `Directory already exists` | Change name collision | Choose a different name or manage existing directory |
| `Validation failed` | Artifact does not match schema | Fix reported issues, then retry |
| `Archive failed: validation error` | Pre-archive validation failed | Fix issues or use `--no-validate` only if necessary |

---

## Typical Lifecycle Order

1. `init` (once per project)
2. `new change <name>` (start work)
3. `instructions proposal --change <name>` → draft proposal
4. `validate <name>` → verify proposal
5. `instructions specs --change <name>` → draft specs
6. `instructions design --change <name>` → draft design
7. `instructions tasks --change <name>` → define tasks
8. `status --change <name>` → confirm all artifacts complete
9. `validate <name> --strict` → final validation
10. `instructions apply --change <name>` → implement tasks
11. `archive <name>` → finalize
