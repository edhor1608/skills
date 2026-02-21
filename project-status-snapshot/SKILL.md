---
name: project-status-snapshot
description: Generate a concise, actionable project status snapshot with branch, PR, checks, blockers, drift, and next actions. Use when the user asks to check status, check again, summarize state, or report current execution progress.
---

# Project Status Snapshot

Produce a fast, decision-ready status report.

## Data Collection

1. Current branch and upstream sync state.
2. Working tree cleanliness and uncommitted changes.
3. Open PRs for current branch scope.
4. Latest CI/check results.
5. Active blockers and dependencies.
6. Drift against stated plan.

## Output Sections

- Current state
- What changed since last snapshot
- Blockers
- Risk level
- Next 1 to 3 actions

## Guardrails

- Prefer facts over interpretations.
- Separate confirmed state from assumptions.
- Flag missing data explicitly.
