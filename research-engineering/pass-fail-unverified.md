# PASS, FAIL, and UNVERIFIED Are Different Outcomes

A binary pass/fail label is often too coarse for research engineering.

`PASS` means the stated criterion was tested with appropriate evidence and succeeded.

`FAIL` means the criterion was tested and the evidence shows that it was not satisfied.

`UNVERIFIED` means the available evidence does not justify either conclusion.

The third state matters because missing evidence is common in complex pipelines. Treating `UNVERIFIED` as `PASS` rewards gaps in coverage. Treating it as `FAIL` confuses uncertainty with a demonstrated defect.

## Examples

- A unit test passes, but the production path was never exercised: the unit-level claim may pass; production parity is unverified.
- A model-fitting job completes, but parameter recovery was not assessed: execution passes; identifiability or recovery remains unverified.
- A generated figure matches expected dimensions, but its source data were not traced: rendering may pass; source provenance is unverified.

## Practical rule

State the claim at the same level as the evidence. Avoid promoting a narrow success into a broader conclusion.

This is especially important when AI agents generate both the implementation and the explanation of its correctness. Independent review should preserve the boundary between what was demonstrated and what was merely asserted.
