# Separate Implementation Success from Scientific Validity

Research software often has at least two different questions:

1. Did the implementation execute as intended?
2. Does the implementation support the scientific claim being made?

These questions overlap, but they are not interchangeable.

A pipeline can be technically correct and scientifically inappropriate. A model can fit without being identifiable. A cross-validation procedure can run without testing the intended generalization. A figure can be reproducibly generated from code while still summarizing the wrong quantity.

## Review both layers

For implementation, inspect items such as:

- code path and configuration;
- data flow;
- stopping and failure conditions;
- tests and regression coverage;
- reproducibility of generated outputs.

For scientific validity, inspect items such as:

- whether the estimator matches the research question;
- whether training and evaluation are separated correctly;
- whether transformations preserve the intended meaning;
- whether model comparison is fair;
- whether the conclusion is narrower than or equal to the evidence.

## Useful consequence

Keep technical acceptance and scientific acceptance separately reportable. A result such as `implementation PASS / scientific interpretation UNVERIFIED` is often more informative than one global status.

This separation is especially useful in AI-assisted work, where an agent may be excellent at satisfying an implementation contract while having no authority to redefine the scientific contract itself.
