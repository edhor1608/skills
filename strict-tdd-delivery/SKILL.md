---
name: strict-tdd-delivery
description: Enforce strict test-first delivery with layered tests, milestone commits, and runnable checkpoints. Use when the user requests TDD, comprehensive tests before implementation, or high-confidence incremental delivery.
---

# Strict TDD Delivery

Drive implementation with tests as the primary control surface.

## Workflow

1. Translate the request into explicit behavior requirements.
2. Write failing tests first.
3. Confirm failures are real and specific.
4. Implement the minimum code to pass tests.
5. Add regression coverage for discovered edge cases.
6. Run fast checks first, then broader suites.
7. Commit only when all required checks pass.

## Test Layers

- Unit tests for local logic
- Integration tests for boundaries
- Snapshot tests only where stable and useful
- End-to-end checks for critical flows

## Guardrails

- Do not write tests that mirror current implementation details.
- Do not ship partial steps that are not runnable.
- Keep each milestone independently verifiable.

## Output Format

- Behavior under test
- Failing test evidence
- Minimal implementation summary
- Passing test evidence
- Remaining risk and next test target
