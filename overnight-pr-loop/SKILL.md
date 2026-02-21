---
name: overnight-pr-loop
description: Run autonomous multi-cycle implementation loops that repeatedly process review comments, create chained branches, open focused PRs, and continue until blocked. Use when the user asks for overnight runs, continuous momentum, chained PR creation, or looped improve-review-continue execution.
---

# Overnight PR Loop

Execute a continuous delivery loop with strict iteration boundaries.

## Inputs

- Goal for this run
- Base branch
- PR size limit
- Stop condition

## Loop

1. Pull latest state and verify clean working tree.
2. Read latest PR feedback for current branch.
3. Apply only valid review comments.
4. Run required checks/tests and fix failures.
5. Create a new child branch from current branch.
6. Implement one focused improvement batch.
7. Re-run checks/tests.
8. Commit with a concise scope label.
9. Push branch and open a non-draft PR.
10. Record what changed, what is next, and known risks.
11. Repeat until stop condition is met.

## Guardrails

- Keep each PR small and reviewable.
- Never bundle unrelated work.
- Stop if checks cannot pass without major scope changes.
- Preserve a chain of branches to keep review history linear.

## Output Format

- Cycle number
- Branch and PR URL
- Completed items
- Deferred items
- Next cycle target
