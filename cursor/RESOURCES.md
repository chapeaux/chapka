# Resources — policies, tooling, Cursor

Curated for Chapka’s [ASSESSMENT.md](../ASSESSMENT.md) themes. Use these to calibrate behavior when contributing upstream.

## Meta and moderation

- [CHAOSS WG AI Alignment — moderation resources](https://github.com/chaoss/wg-ai-alignment/tree/main/moderation) — index of project policies, foundation guidance, detection ideas, and examples of problematic patterns.

## Formal policies (examples across the spectrum)

- [Linux kernel — tool-generated content](https://docs.kernel.org/process/generated-content.html)
- [Linux kernel — coding assistants](https://docs.kernel.org/process/coding-assistants.html)
- [Fedora — AI-assisted contributions](https://docs.fedoraproject.org/en-US/council/policy/ai-contribution-policy/)
- [Zulip — AI use](https://zulip.readthedocs.io/en/latest/contributing/contributing.html#ai-use-policy-and-guidelines)
- [attrs — AI policy](https://github.com/python-attrs/attrs/blob/main/.github/AI_POLICY.md)
- [Pulp — AI-generated / assisted coding](https://github.com/pulp#pulp-project-policy-on-ai-generated-content--ai-assisted-coding)
- [Avocado — AI policy](https://avocado-framework.readthedocs.io/en/latest/guides/contributor/chapters/ai_policy.html)
- [vLLM — AI-assisted contributions](https://docs.vllm.ai/en/latest/governance/process/#ai-assisted-contributions)

## Active discussions (as of ASSESSMENT synthesis)

- [Django — AI/LLM contribution policy proposal](https://forum.djangoproject.com/t/proposal-add-an-ai-llm-contribution-policy-to-django/44298)
- [Node.js — AI guidelines PR](https://github.com/nodejs/node/pull/62105)
- [OpenSSL communities — AI policy thread](https://openssl-communities.org/d/FS9r6Vyl/ai-policy-)

## CI and trust tooling (optional adoption)

Projects sometimes add PR templates with disclosure fields, checks for trailers when AI is declared, or experimental detection/trust actions. CHAOSS’s moderation repo links to examples; there is no single standard — adopt what fits your governance.

## Cursor product documentation

- [Cursor — Rules](https://docs.cursor.com/context/rules) — how `.cursor/rules` and `.mdc` frontmatter work.
- [Cursor — AGENTS.md](https://docs.cursor.com/context/agents) — agent context at the repo root.

## Personal skills (optional)

For repeated workflows (e.g. formatting commits with `Assisted-by:`), consider a **user-level** Cursor skill so the agent follows your preferred trailer format. Project rules in `.cursor/rules/` already encode Chapka’s baseline.
