# skills
Reusable skills for autonomous delivery loops, strict TDD, PR triage, project status snapshots, Obsidian sync, project bootstrapping, and document-to-plan conversion.

## Included Skills

- `overnight-pr-loop`: Run chained improve-review-deliver cycles with small PRs.
- `strict-tdd-delivery`: Enforce test-first implementation with runnable milestones.
- `pr-review-triage`: Process PR feedback and push minimal validated fixes.
- `project-status-snapshot`: Generate compact branch/PR/check/blocker status.
- `obsidian-project-sync`: Sync project knowledge into structured Obsidian docs.
- `project-bootstrap-brand-pack`: Generate name, phonetic, license, README, and GitHub copy.
- `doc-ingest-to-plan`: Convert long documents into milestones, tasks, and decisions.

## Usage

In Codex prompts, invoke skills with:

```text
Use $strict-tdd-delivery to implement this change with failing tests first.
```

## Install As Global Skills

This repo is meant to be versioned in Git while being active in global Codex scope (`~/.codex/skills`).

### 1) Clone repo

```bash
git clone <your-github-url> /Users/jonas/repos/codex-skills
```

### 2) Create symlinks into global skills dir

```bash
for s in overnight-pr-loop strict-tdd-delivery pr-review-triage project-status-snapshot obsidian-project-sync project-bootstrap-brand-pack doc-ingest-to-plan; do
  ln -sfn "/Users/jonas/repos/codex-skills/$s" "/Users/jonas/.codex/skills/$s"
done
```

### 3) Verify links

```bash
for s in overnight-pr-loop strict-tdd-delivery pr-review-triage project-status-snapshot obsidian-project-sync project-bootstrap-brand-pack doc-ingest-to-plan; do
  ls -ld "/Users/jonas/.codex/skills/$s"
done
```

## Structure

Each skill follows:

```text
<skill-name>/
  SKILL.md
  agents/openai.yaml
```

## Notes

- Keep `name` in `SKILL.md` equal to the folder name.
- Keep `agents/openai.yaml` `default_prompt` referencing `$<skill-name>`.
- Do not version `/Users/jonas/.codex/skills/.system` in this repo.

<!-- status:start -->
## Status
- State: active
- Summary: Define current milestone.
- Next: Define next concrete step.
- Updated: 2026-02-21
- Branch: `main`
- Working Tree: dirty (2 files)
- Last Commit: 714aa52 (2026-02-21) Add 7 reusable agent skills for Codex and Claude
<!-- status:end -->
