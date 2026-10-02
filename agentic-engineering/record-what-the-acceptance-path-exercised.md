# Record What the Acceptance Path Exercised

A successful command is useful evidence only if the intended checks actually ran. A test can exist in the repository while being omitted from the command people use to accept a change.

## Inspect discovery before interpreting success

Read the documented entry point and trace which suites it invokes. Compare the expected suites with the observed execution. A zero exit status does not establish coverage for an omitted suite, and a missing remote check is neither a passing test nor a demonstrated defect.

Use a small acceptance record:

| Question | Evidence to record |
|---|---|
| What ran? | Entry point, discovered suites, and result |
| What behavior was checked? | Assertions and the paths they exercise |
| Where did it run? | Relevant runtime and test environment |
| What remains open? | Missing execution, device checks, and human decisions |

Do not infer behavioral coverage from a test name or count. Read the assertions. A test that only observes startup cannot support a claim about saving data.

## Keep environment and authority visible

A browser fixture with invented input can verify its asserted behavior in that environment. It does not establish physical-device behavior, operating-system integration, or handling of representative real input. Record those claims as `UNVERIFIED` until appropriate evidence exists; record a demonstrated unmet criterion as `FAIL`.

Security scans and deployment checks answer their own questions. Their success does not replace application tests. Likewise, automated checks cannot supply consent or a designated human approval. Keep each human gate open until the authorized person decides it.

Before accepting the change, map each claim to the execution, assertion, or decision that supports it. This makes missing evidence visible without converting uncertainty into either success or failure.
