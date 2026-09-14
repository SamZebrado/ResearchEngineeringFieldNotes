# Review the Evidence, Not the Agent

AI coding agents can produce fluent explanations of what they changed, why the change is correct, and why the test suite should be sufficient. That explanation is useful context, but it is not evidence.

A reliable review starts from artifacts that can be checked independently:

- the exact revision under review;
- the diff or changed files;
- executable tests and their outputs;
- logs or generated artifacts tied to that revision;
- explicit assumptions and acceptance criteria.

## A useful review order

1. **Identify the exact candidate.** A review without a fixed revision can become invalid while it is being performed.
2. **Read the change itself.** Do not infer implementation from the agent's summary.
3. **Map claims to evidence.** For each important claim, ask what artifact demonstrates it.
4. **Look for missing negative evidence.** Passing tests say little about paths that were never exercised.
5. **Classify the result.** Use `PASS` only when the relevant claim is actually supported; otherwise prefer `UNVERIFIED` or a specific blocker.

## Why this matters

Agent output compresses uncertainty. A confident summary may combine observed facts, inferred behavior, and intended behavior into one paragraph. Review should separate those categories again.

The same principle applies to human-authored work: confidence is metadata; evidence is the authority.
