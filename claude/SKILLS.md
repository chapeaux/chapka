# Skills index

These skill files define specialized agent behaviors for open source contribution workflows. Each skill is a structured prompt that can be referenced from `CLAUDE.md`, used as the basis for a custom command, or invoked directly by pasting into a conversation.

## How to use

**As custom commands:** Copy any skill's `SKILL.md` into `.claude/commands/<skill-name>.md` and invoke it with `/project:<skill-name>`.

**As CLAUDE.md references:** Point to these from your project's `CLAUDE.md` to give the agent standing knowledge of how to perform these tasks.

**Directly:** Paste the skill content into a Claude Code conversation when you need that behavior.

## Skill catalog

| Skill | File | ASSESSMENT theme | Use when... |
|-------|------|-----------------|-------------|
| Code review | [code-review/SKILL.md](.claude/skills/code-review/SKILL.md) | Verification, quality | You want a first-pass review before human reviewers see it |
| Test generation | [test-gen/SKILL.md](.claude/skills/test-gen/SKILL.md) | Verification, quality | You need tests for changed code, especially edge cases |
| Documentation sync | [docs-sync/SKILL.md](.claude/skills/docs-sync/SKILL.md) | Documentation agents | Code changes altered APIs, configs, or behavior |
| License audit | [license-audit/SKILL.md](.claude/skills/license-audit/SKILL.md) | Licensing, copyright | You want to check AI-generated code for provenance risk |
| Security scan | [security-scan/SKILL.md](.claude/skills/security-scan/SKILL.md) | LLM evaluation, security | You want to audit AI output for vulnerabilities |
| Upstream onboarding | [upstream-onboard/SKILL.md](.claude/skills/upstream-onboard/SKILL.md) | Context management, community norms | You're contributing to an unfamiliar project for the first time |
| PR preparation | [pr-prepare/SKILL.md](.claude/skills/pr-prepare/SKILL.md) | Attribution, accountability, spam prevention | You're ready to open a PR and want a full compliance sweep |
