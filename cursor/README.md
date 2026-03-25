# Cursor + open source workflow (Chapka)

This directory is the **human-facing** scaffold for using Cursor while contributing to open source under **AI-first** norms. Cursor loads **project rules** from [`.cursor/rules/`](../.cursor/rules/) and reads **[`AGENTS.md`](../AGENTS.md)** at the repo root; those encode the same ideas in machine-oriented form.

## Contents

| Item | Purpose |
|------|---------|
| [CHECKLIST.md](CHECKLIST.md) | Pre-PR checks mapped to common policy themes |
| [RESOURCES.md](RESOURCES.md) | Policies, meta-resources, and Cursor documentation |
| [templates/pr-body.md](templates/pr-body.md) | Optional PR description scaffold |
| [templates/commit-footer.md](templates/commit-footer.md) | `Assisted-by:` and DCO reminders |

## Why both `cursor/` and `.cursor/`?

- **`cursor/`** (here): onboarding, checklists, and templates you can read in any git host UI.
- **`.cursor/rules/`**: `.mdc` rule files that Cursor injects into the agent. Rules live there by convention.

## Background

The rationale and community landscape are documented in **[`ASSESSMENT.md`](../ASSESSMENT.md)**. A shorter link list lives in **[`POLICY_LIST.md`](../POLICY_LIST.md)**.

## Adopting this in another project

Copy `.cursor/rules/`, `AGENTS.md`, and the `cursor/` tree (or merge their content into existing files). Then add stack-specific instructions to `AGENTS.md` or additional rules for your languages and tools.
