# Claude Code + open source workflow (Chapka)

This directory is the **human-facing** scaffold for using Claude Code while contributing to open source under **AI-first** norms. It parallels the [`cursor/`](../cursor/) directory but leverages Claude Code's native features.

## Contents

| Item | Purpose |
|------|---------|
| [CLAUDE.md](CLAUDE.md) | Template `CLAUDE.md` to copy to your repo root -- encodes core behavior + attribution rules |
| [CHECKLIST.md](CHECKLIST.md) | Pre-PR checks mapped to common policy themes |
| [SKILLS.md](SKILLS.md) | Index of all skills with ASSESSMENT theme mapping |
| [RESOURCES.md](RESOURCES.md) | Policies, meta-resources, and Claude Code documentation |
| [.claude/commands/](.claude/commands/) | Custom slash commands (see below) |
| [.claude/skills/](.claude/skills/) | Specialized agent skill definitions (see below) |
| [settings.json](settings.json) | Example hooks and permissions for `.claude/settings.json` |
| [templates/pr-body.md](templates/pr-body.md) | Optional PR description scaffold |
| [templates/commit-footer.md](templates/commit-footer.md) | `Assisted-by:` and DCO reminders |

## How Claude Code's features map to the ASSESSMENT themes

Claude Code has a different architecture from Cursor. Here is how each ASSESSMENT consideration is addressed:

### Project context (replaces `.cursor/rules/` + `AGENTS.md`)

Claude Code reads **`CLAUDE.md`** files at the repo root (and in subdirectories). This single file replaces both Cursor's `.mdc` rule files and the `AGENTS.md` manifest. Copy [`CLAUDE.md`](CLAUDE.md) to your repo root and add project-specific details.

**Why one file?** Claude Code loads `CLAUDE.md` automatically on every conversation. There is no need for separate "always apply" rule files. Subdirectory `CLAUDE.md` files can add context for specific parts of the codebase.

### Custom slash commands (replaces Cursor skills)

Files in `.claude/commands/` become slash commands invocable as `/project:<name>`. This scaffold provides three:

| Command | Invocation | What it does |
|---------|-----------|--------------|
| [pre-pr-check](commands/pre-pr-check.md) | `/project:pre-pr-check` | Audits staged changes against the OSS checklist |
| [commit-assisted](commands/commit-assisted.md) | `/project:commit-assisted` | Drafts a commit message with proper `Assisted-by:` trailer |
| [check-upstream-policy](commands/check-upstream-policy.md) | `/project:check-upstream-policy` | Searches the repo for AI contribution policies |

To use these, copy the `commands/` directory into your project's `.claude/commands/`.

### Skills (specialized agent behaviors)

Each skill lives in its own subdirectory as `.claude/skills/{skill-name}/SKILL.md`. This structure allows skills to grow with additional supporting files (examples, templates, configs) alongside their definition. Skills can be used in three ways:

1. **As custom commands**: copy a skill's `SKILL.md` into `.claude/commands/<skill-name>.md` to make it invocable via `/project:<name>`
2. **As CLAUDE.md references**: point to skills from your `CLAUDE.md` to give the agent standing knowledge
3. **Directly**: paste skill content into a conversation when you need that behavior

| Skill | Directory | What it does |
|-------|-----------|--------------|
| Code review | [code-review/](.claude/skills/code-review/) | First-pass review for correctness, style, and AI-specific concerns |
| Test generation | [test-gen/](.claude/skills/test-gen/) | Generates tests matching the project's framework and conventions |
| Documentation sync | [docs-sync/](.claude/skills/docs-sync/) | Drafts doc updates when code changes alter APIs or behavior |
| License audit | [license-audit/](.claude/skills/license-audit/) | Checks AI-generated code for provenance and license compatibility risk |
| Security scan | [security-scan/](.claude/skills/security-scan/) | Audits AI output for common vulnerability patterns |
| Upstream onboarding | [upstream-onboard/](.claude/skills/upstream-onboard/) | Researches a new project's policies, conventions, and good first contributions |
| PR preparation | [pr-prepare/](.claude/skills/pr-prepare/) | Full compliance sweep before opening a pull request |

See [SKILLS.md](SKILLS.md) for the full index and usage details.

### Hooks (mechanical enforcement)

Claude Code supports **hooks** in `settings.json` that run shell commands before or after tool calls. The example [`settings.json`](settings.json) shows:

- A **post-commit reminder** to check for `Assisted-by:` trailers
- **Permission guards** that deny `--force` push and `--no-verify` commits

This is the Claude Code equivalent of git pre-commit hooks but scoped to the agent's actions. Copy relevant sections into your `.claude/settings.json`.

### MCP servers (extended tooling)

Claude Code supports [Model Context Protocol](https://docs.anthropic.com/en/docs/claude-code/mcp-servers) servers for additional capabilities. Relevant for OSS workflows:

- **Code indexing** (e.g., beret) for codebase exploration and architecture understanding
- **CI/CD integration** for checking build status and test results
- **Issue trackers** for understanding context before contributing

Configure these in `.claude/settings.json` or `.claude/settings.local.json`.

## Adopting this in another project

1. Copy `CLAUDE.md` to the repo root. Add project-specific build/test/lint commands and architecture notes.
2. Copy `.claude/commands/` to `.claude/commands/` in the target project for the slash commands.
3. Copy `.claude/skills/` to `.claude/skills/` (or selectively copy the skills you want as commands).
4. Merge relevant hooks and permissions from `settings.json` into `.claude/settings.json`.
5. (Optional) Add MCP server configurations for your tooling.

If the project already has a `CLAUDE.md`, merge the open source rules into the existing file rather than replacing it.

## Why `claude/` vs `.claude/`?

- **`claude/`** (here): onboarding docs, templates, and the `CLAUDE.md` template -- readable in any git host UI.
- **`.claude/`**: Claude Code's config directory (`settings.json`, `settings.local.json`, `commands/`). Files here are consumed by the tool at runtime.

## Background

The rationale and community landscape are documented in **[ASSESSMENT_Claude.md](../ASSESSMENT_Claude.md)** and **[ASSESSMENT_Gemini.md](../ASSESSMENT_Gemini.md)**. A shorter link list lives in **[POLICY_LIST.md](../POLICY_LIST.md)**.
