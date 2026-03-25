Review the staged and unstaged changes in this repository against the open source AI contribution checklist. For each item, report pass/fail/not-applicable with a one-line explanation.

## Checklist

1. **Verification**: Have all changed files been read and understood? Are there untested code paths?
2. **Attribution**: Do commits that materially used AI assistance have an `Assisted-by:` trailer? Is anything incorrectly using `Co-authored-by:` for a tool?
3. **Licensing**: Is there a `Signed-off-by` added by an agent instead of the human? Does any generated code look like it was copied from a specific known source with an incompatible license?
4. **Accountability**: Is the PR description written in the contributor's voice (not a diff narration)? Does it explain *why*?
5. **Scope**: Is the change atomic and focused, or does it bundle unrelated refactors?
6. **Community norms**: Are there any LLM-generated review comments or verbose AI prose in issue/PR text?

If an upstream project's CONTRIBUTING or AI policy is present, also check compliance against those specific requirements.

Summarize findings and flag anything that should be fixed before opening the PR.
