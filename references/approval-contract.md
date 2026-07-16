# Approval Contract

The skill is a policy layer. A hard stop before an external or irreversible action exists only when the host validates an approval request before calling the write tool.

## Decision Record

Use [DecisionRecord](../contracts/decision-record.schema.json) to capture the agent's task classification, evidence checked, question-gate result, assumptions, and approval boundary. It makes an agent's decision process reviewable without storing raw private context.

## Approval Request

Use [ApprovalRequest](../contracts/approval-request.schema.json) before a write action such as an email send, publication, payment, permission change, delete, deployment, or data mutation.

An approval is valid only for the recorded action, parameters, target, and expiry. A host should reject a request that is missing, rejected, expired, or changed after approval.

## Minimal Host Rule

1. The agent proposes a staged action and creates an ApprovalRequest.
2. The user approves, rejects, or edits the exact request.
3. The host validates the approved request immediately before the write tool call.
4. The host records the resulting effect or refusal.

Do not represent a conversational phrase such as "go ahead" as blanket authority for unrelated, future, or altered actions.
