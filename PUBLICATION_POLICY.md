# Publication Policy

This repository is public. Every new note must pass a privacy and provenance review before publication.

## Publication gate

A note may be published only when all of the following are true:

1. The lesson is useful without knowing the source project.
2. The text does not name or identify a private project, client, collaborator, institution-specific workflow, or internal system.
3. It contains no private code, datasets, file paths, screenshots, credentials, prompts with embedded private context, unpublished scientific results, or operational details that could reconstruct the source work.
4. Numbers, parameter values, task structures, and examples are either generic or independently created for the note.
5. The note states only what the public evidence or the abstracted method supports.
6. If safe anonymization is uncertain, the item is not published.

## Preferred transformation

Turn a private incident into a public note by extracting the invariant:

- private incident -> general failure mode;
- project-specific fix -> reusable review rule;
- internal evidence -> generic evidence checklist;
- concrete implementation -> minimal independent example, if one is needed at all.

Do not merely rename entities while preserving distinctive details. Anonymization must remove the possibility of reconstructing the source project from combinations of requirements, parameters, code structure, or chronology.

## Permanently excluded source material

Some private work is designated as non-publishable source material. For those sources, specific requirements, cases, code, naming, business logic, evaluation criteria, and identifying details must never be reused here. At most, a broadly known engineering principle may be written independently without drawing on those specifics.

## Review standard

When in doubt, omit. A shorter public note is preferable to a detailed note that leaks provenance.
