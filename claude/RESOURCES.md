# Resources -- policies, tooling, Claude Code

Curated for Chapka's ASSESSMENT themes. Use these to calibrate behavior when contributing upstream.

## Meta and moderation

- [CHAOSS WG AI Alignment -- moderation resources](https://github.com/chaoss/wg-ai-alignment/tree/main/moderation) -- index of project policies, foundation guidance, detection ideas, and examples of problematic patterns.

## Formal policies (examples across the spectrum)

- [Linux kernel -- tool-generated content](https://docs.kernel.org/process/generated-content.html)
- [Linux kernel -- coding assistants](https://docs.kernel.org/process/coding-assistants.html)
- [Fedora -- AI-assisted contributions](https://docs.fedoraproject.org/en-US/council/policy/ai-contribution-policy/)
- [Zulip -- AI use](https://zulip.readthedocs.io/en/latest/contributing/contributing.html#ai-use-policy-and-guidelines)
- [attrs -- AI policy](https://github.com/python-attrs/attrs/blob/main/.github/AI_POLICY.md)
- [Pulp -- AI-generated / assisted coding](https://github.com/pulp#pulp-project-policy-on-ai-generated-content--ai-assisted-coding)
- [Avocado -- AI policy](https://avocado-framework.readthedocs.io/en/latest/guides/contributor/chapters/ai_policy.html)
- [vLLM -- AI-assisted contributions](https://docs.vllm.ai/en/latest/governance/process/#ai-assisted-contributions)

## Active discussions (as of ASSESSMENT synthesis)

- [Django -- AI/LLM contribution policy proposal](https://forum.djangoproject.com/t/proposal-add-an-ai-llm-contribution-policy-to-django/44298)
- [Node.js -- AI guidelines PR](https://github.com/nodejs/node/pull/62105)
- [OpenSSL communities -- AI policy thread](https://openssl-communities.org/d/FS9r6Vyl/ai-policy-)

## CI and trust tooling (optional adoption)

Projects sometimes add PR templates with disclosure fields, checks for trailers when AI is declared, or experimental detection/trust actions. CHAOSS's moderation repo links to examples; there is no single standard -- adopt what fits your governance.

## Claude Code documentation

- [Claude Code overview](https://docs.anthropic.com/en/docs/claude-code/overview) -- capabilities, installation, getting started.
- [CLAUDE.md (project memory)](https://docs.anthropic.com/en/docs/claude-code/memory) -- how CLAUDE.md files work, hierarchy, and best practices.
- [Custom slash commands](https://docs.anthropic.com/en/docs/claude-code/slash-commands) -- creating project and user commands in `.claude/commands/`.
- [Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) -- pre/post tool-call hooks in `settings.json` for automated enforcement.
- [Settings and permissions](https://docs.anthropic.com/en/docs/claude-code/settings) -- `settings.json`, `settings.local.json`, and permission modes.
- [MCP servers](https://docs.anthropic.com/en/docs/claude-code/mcp-servers) -- extending Claude Code with Model Context Protocol servers.
- [GitHub integration](https://docs.anthropic.com/en/docs/claude-code/github) -- using Claude Code for PR workflows, code review, and issue triage.

## Additional recommended resources

### For maintainers adopting AI policies

- [ASF Generative Tooling Guidance](https://www.apache.org/legal/generative-tooling.html) -- Apache's license category framework (A/B/X) for evaluating AI output compatibility.
- [Linux Foundation Generative AI Policy](https://www.linuxfoundation.org/legal/generative-ai) -- foundation-level guidance on AI tool safety features and provenance.
- [OpenInfra Foundation AI Policy](https://openinfra.org/legal/ai-policy/) -- human-in-the-loop requirements and governance constraints.

### For contributors using Claude Code

- [Claude Code CLI reference](https://docs.anthropic.com/en/docs/claude-code/cli-usage) -- flags, environment variables, and non-interactive mode for CI.
- [Claude Code IDE extensions](https://docs.anthropic.com/en/docs/claude-code/ide-integrations) -- VS Code and JetBrains integration.
