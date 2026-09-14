# Bind Reviews to an Exact Revision

A technical review is only meaningful if everyone knows exactly what was reviewed.

For code, record the commit SHA. For generated evidence, record the source revision and enough provenance to connect outputs back to that source. For a patch-only review, record both the base and candidate revisions.

## Minimal contract

A review request should answer four questions:

- What exact revision is the candidate?
- What revision or state is it being compared against?
- What scope is in review?
- What evidence was generated from that candidate?

This prevents a common failure mode: a reviewer approves one state while later edits silently become associated with the approval.

## Narrow delta reviews

When only a small correction is requested, keep the scope narrow. Re-review the changed behavior and any dependencies that can invalidate the earlier conclusion. Do not casually reopen unrelated settled areas, but also do not assume an earlier result still holds if the new change touches its premises.

A useful review record is therefore not simply `PASS`; it is closer to:

`PASS for revision X, within scope Y, supported by evidence Z.`

That sentence remains interpretable months later.
