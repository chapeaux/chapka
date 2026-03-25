# Chapka

An insulated and opinionated starter kit for participating in the open source software community in an AI-first software development life cycle.

Chapka provides ready-to-copy scaffolding for AI coding agents so that contributors using these tools can navigate disclosure requirements, licensing concerns, community norms, and quality expectations across diverse open source projects.

## The problem

Open source communities are rapidly establishing norms for AI-assisted contributions. Policies range from permissive-with-guardrails (Linux kernel, Fedora) to restrictive (attrs, Gentoo). A contributor using AI tools today must understand attribution formats, licensing risks, DCO/CLA constraints, and anti-spam expectations -- and these vary by project. Getting it wrong wastes maintainer time and damages trust.

Chapka encodes the common ground across these policies into agent-consumable configuration files, so your AI tool behaves responsibly by default.

## What's in the box

```
chapka/
  ASSESSMENT_Claude.md       # Landscape analysis: how communities approach AI contributions
  ASSESSMENT_Gemini.md       # Same analysis, independently synthesized
  POLICY_LIST.md             # Raw link collection of AI policies and discussions
  PROMPT.md                  # The prompt used to generate the assessments

  cursor/                    # Scaffolding for Cursor users
    .cursor/rules/           # .mdc rule files (core behavior + attribution)
    AGENTS.md                # Agent context manifest
    CHECKLIST.md             # Pre-PR checklist
    RESOURCES.md             # Policy links + Cursor docs
    templates/               # PR body and commit footer templates

  claude/                    # Scaffolding for Claude Code users
    CLAUDE.md                # Template project context (copy to repo root)
    .claude/commands/        # Custom slash commands
    .claude/skills/          # Specialized agent skill definitions
    settings.json            # Example hooks and permission guards
    CHECKLIST.md             # Pre-PR checklist
    RESOURCES.md             # Policy links + Claude Code docs
    templates/               # PR body and commit footer templates
```

## Quick start

### For Claude Code users

1. Copy `claude/CLAUDE.md` to the root of the project you're contributing to.
2. Copy `claude/.claude/commands/` to `.claude/commands/` in that project.
3. Copy `claude/.claude/skills/` to `.claude/skills/` (or selectively promote skills to commands).
4. Merge relevant hooks from `claude/settings.json` into `.claude/settings.json`.
5. Add project-specific details (build commands, test paths, architecture) to the `CLAUDE.md` you copied.

Available slash commands:
- `/project:pre-pr-check` -- audit staged changes against the OSS checklist
- `/project:commit-assisted` -- draft a commit with proper `Assisted-by:` trailer
- `/project:check-upstream-policy` -- search the repo for AI contribution policies

Available skills (copy to `.claude/commands/` to use as slash commands):
- **code-review** -- first-pass review for correctness, style, and AI-specific concerns
- **test-gen** -- generate tests matching the project's framework and conventions
- **docs-sync** -- draft doc updates when code changes alter APIs or behavior
- **license-audit** -- check AI-generated code for provenance and license risk
- **security-scan** -- audit AI output for common vulnerability patterns
- **upstream-onboard** -- research a new project's policies and conventions
- **pr-prepare** -- full compliance sweep before opening a pull request

### For Cursor users

1. Copy `cursor/.cursor/rules/` to the target project.
2. Copy `cursor/AGENTS.md` to the project root.
3. Add project-specific context to `AGENTS.md`.

See [`cursor/README.md`](cursor/README.md) for details.

## Core principles

These are consistent across both tool scaffolds and reflect the consensus found in the ASSESSMENT analyses:

- **Humans are accountable.** The contributor owns every line. "An LLM wrote it" is never a defense.
- **AI is not an author.** No `Co-authored-by:` for tools. Use `Assisted-by:` trailers for disclosure.
- **Existing standards apply.** AI-assisted contributions must meet the same quality, licensing, and review bar as any other.
- **Upstream wins.** The target project's policies override Chapka defaults. Always check first.
- **Honest disclosure.** When AI materially shaped the contribution, say so. Trivial assistance (grammar, spelling) is generally exempt.

## What the assessments cover

The ASSESSMENT files synthesize policies from the Linux kernel, Fedora, attrs, Zulip, Pulp, Avocado, Node.js, Django, OpenSSL, and others. They cover:

| Theme | Key question |
|-------|-------------|
| Verification and quality | Can you explain and defend every line? |
| Attribution and disclosure | When and how to declare AI usage? |
| Licensing and copyright | Does AI output risk license contamination? |
| Contributor accountability | Who is legally responsible? |
| Spam and abuse prevention | Is this a valuable, scoped contribution? |
| Enforceability | How do projects actually enforce these norms? |

## Adding support for another tool

Chapka is designed to grow. To add scaffolding for a new AI coding tool:

1. Create a directory named after the tool (e.g., `windsurf/`, `copilot/`).
2. Translate the core principles and attribution rules into that tool's native configuration format.
3. Add a README explaining how the tool's features map to the ASSESSMENT themes.
4. Include a checklist, resource list, and templates following the same structure.

## Related resources

- [CHAOSS WG AI Alignment](https://github.com/chaoss/wg-ai-alignment/tree/main/moderation) -- curated list of 20+ project and foundation AI policies
- [ASF Generative Tooling Guidance](https://www.apache.org/legal/generative-tooling.html)
- [Linux Foundation Generative AI Policy](https://www.linuxfoundation.org/legal/generative-ai)
- [Fedora AI-Assisted Contributions Policy](https://docs.fedoraproject.org/en-US/council/policy/ai-contribution-policy/)

## Part of Chapeaux

Chapka is part of the [Chapeaux](https://github.com/chapeaux) family of projects.

## License

See the project license file for terms.
