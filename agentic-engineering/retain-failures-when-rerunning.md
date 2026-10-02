# Retain Failures When Rerunning

A passing rerun should add evidence, not erase the failed attempt. Without the earlier record, a reviewer cannot tell whether the defect was repaired, the environment changed, or the failing path was skipped.

## Keep a linked sequence

For each attempt, retain the source revision, command, relevant environment, outcome, and a reference to the diagnostic evidence. Then record what changed before the next attempt: code, configuration, permissions, test selection, or another relevant condition.

The record should support a sentence such as:

> The first attempt could not launch the test environment. A later attempt ran the intended checks after an environment change. Execution before that change remains unverified.

This is a generic example, not evidence about any particular system.

## Classify the failure at the right level

A runner that cannot start is a failed execution attempt. It does not demonstrate that the application violates a behavioral criterion. Preserve the diagnostic result while marking the unexecuted behavioral claim `UNVERIFIED`.

If an assertion executes and fails, retain that `FAIL` for the tested revision. A passing run after a repair supports the later revision; it does not retroactively make the earlier revision pass. If the rerun omits the failing assertion, the original finding remains unresolved.

Keep raw diagnostics in an appropriately restricted evidence store. A public summary usually needs only the failure class, the relevant change, and the scope of the rerun. Remove sensitive content before sharing; do not overwrite the original evidence to produce the summary.
