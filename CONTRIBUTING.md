# Contributing

The fastest way to improve AskUp is to contribute a de-identified case that exposes a real decision boundary.

## Useful Contributions

- A request where the policy asked an unnecessary question.
- A request where the policy should have asked but did not.
- A safe assumption that caused avoidable rework.
- An approval boundary that was too broad, too narrow, or unclear.
- A host adapter that validates the published contracts before a write action.

## Contribution Format

Include the minimal prompt, available context, observed response, intended decision boundary, and a proposed evaluation criterion. Remove names, emails, customer details, credentials, tokens, proprietary documents, and private message content.

## Before Opening a Pull Request

1. Keep runtime instructions in `SKILL.md` and detailed rationale in `references/`.
2. Add or update an example or evaluation case for behavioral changes.
3. Preserve the explicit distinction between policy guidance and tool-level enforcement.
