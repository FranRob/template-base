---
description: Git branching and PR workflow — always active
---

## Branch Strategy (Gitflow)

- `main` — production only. Merges from `develop` on deliberate releases.
- `develop` — integration branch. All feature branches merge here.
- Feature branches — short-lived, one per block, branch from `develop`, PR back to `develop`.

## PR Workflow (mandatory)

Every block of work MUST follow this flow — no exceptions:

1. Create a GitHub issue describing the block → add `status:approved` label
2. Create branch from `develop`: `feat/block-XX-description` (or `fix/`, `docs/`, etc.)
3. Work with conventional commits
4. Open PR from branch → `develop`
5. If diff > 400 lines → split into stacked PRs
6. Merge and close the issue

Never accumulate multiple blocks into a single PR.
