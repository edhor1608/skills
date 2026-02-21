---
name: pr-review-triage
description: Process PR feedback efficiently by validating comments, applying justified fixes, and pushing clean follow-up commits without scope creep. Use when handling PR reviews, Coderabbit feedback, multi-PR queues, or branch-by-branch comment processing.
---

# PR Review Triage

Process review feedback in a deterministic, auditable pass.

## Workflow

1. List open PRs in priority order.
2. For each PR, collect unresolved comments.
3. Classify each comment: valid, invalid, already addressed, or blocked.
4. Apply only valid comments with minimal diffs.
5. Run project checks for touched areas.
6. Commit and push with a review-linked message.
7. Post resolution summary per PR.

## Decision Rules

- Valid: behavior risk or correctness issue with clear evidence.
- Invalid: stylistic preference that conflicts with project standards.
- Blocked: requires product decision or cross-PR dependency.

## Guardrails

- Do not merge unless explicitly requested.
- Do not refactor unrelated files.
- Keep one concern per commit where possible.

## Output Format

- PR identifier
- Accepted comments and fixes
- Rejected comments with reason
- Blocked comments and required decision
- Verification results
