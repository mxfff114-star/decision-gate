# AskUp Specification

## Intent

AskUp is the decision layer between a natural-language request and an agent's action. Its job is to reduce unnecessary questions without silently expanding authority.

## User Jobs

1. Act immediately on fully specified, low-risk, reversible requests.
2. Investigate facts that can be learned without interrupting the user.
3. Ask only when an answer can materially change the decision and belongs to the user.
4. Present material choices as an approval-ready Decision Card.
5. Keep confirmed preferences separate from temporary or volatile context.
6. Stage an exact approval request before a high-impact write action.

## Non-Goals

- Replacing legal, financial, security, or domain review.
- Claiming tool-level enforcement without a host adapter.
- Building a hidden profile of users or retaining sensitive information.

## Evidence Model

The public evaluation record must include de-identified traces, failures, revisions, model and host context, and the scoring method. See [EVALS.md](EVALS.md).

## Compatibility

The runtime policy follows the Agent Skills format. Contracts are plain JSON Schema so adapters can use them without a framework dependency.

## Maintenance Rule

A behavioral change requires an updated example or evaluation case. A new preference rule must state its source, scope, recheck condition, and user-control path.
