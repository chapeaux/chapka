# Pre-pull request checklist (OSS + AI-assisted work)

Use this before opening or marking ready for review. **Upstream wins**: if the target project has its own AI or contribution policy, follow that first.

Run `/project:pre-pr-check` in Claude Code to have the agent audit your changes against this list.

## 1. Verification and quality

- [ ] I have **read** every changed line and can explain what it does and why.
- [ ] I **ran** relevant tests or manual checks; the change is not raw untested model output.
- [ ] I **verified** any claim about behavior or APIs against this repo's source, tests, or official docs -- not only against the model's answer.

## 2. Attribution and disclosure

- [ ] If a **significant** portion came from an AI tool with minimal editing, I **disclosed** that in the PR (and in commits if the project expects it). Trivial grammar/spelling-only help can stay implicit unless upstream says otherwise.
- [ ] I used **`Assisted-by:`** (or the project's required trailer) where appropriate; I did **not** list a tool as **`Co-authored-by:`**.

## 3. Licensing and copyright

- [ ] I did **not** add **`Signed-off-by`** or other DCO/CLA certification unless **I** am the human making that attestation (agents must not sign for the contributor).
- [ ] Nothing in the change looks like **copied** or **license-incompatible** material; if something was flagged by similarity tools, I **rewrote** or confirmed compatibility.

## 4. Contributor accountability

- [ ] I am prepared to **discuss and revise** from my own understanding in review -- not only by re-prompting and resubmitting.

## 5. Spam and community norms

- [ ] The PR is **scoped** and valuable; it is not a drive-by mass refactor or unrelated churn.
- [ ] PR and issue text is **my voice**, succinct, and focused on what needs human judgment; I am not pasting LLM walls into development channels where policies forbid it.
- [ ] I am not posting **LLM-generated review comments** on other people's work.

## 6. Enforceability and honesty

- [ ] I am relying on **honest disclosure** and substance; detection tooling is imperfect, but maintainers rely on trust and review.
