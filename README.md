# template-base

A Claude Code project template with multi-agent setup, persistent memory via Engram, and auto-loaded rules.

## What's included

```
.claude/
├── settings.json          # Post-compaction hook for Engram memory recovery
├── rules/
│   ├── git-workflow.md    # Gitflow + PR workflow (always active)
│   └── security.md        # Security baseline (always active)
└── agents/
    └── explorer.md        # Sub-agent that maps code without editing it

.engram/config.json        # Locks the project name for Engram persistent memory
CLAUDE.md                  # Project instructions for Claude Code
CLAUDE.local.md.example    # Template for personal overrides (gitignored)
```

## How to use this template

1. Click **Use this template** → Create a new repository
2. Clone your new repo
3. Fill in `CLAUDE.md` with your project's specifics
4. Set your project name in `.engram/config.json`
5. Copy `CLAUDE.local.md.example` → `CLAUDE.local.md` and fill in personal preferences
6. Add stack-specific rules in `.claude/rules/` (e.g. `api-conventions.md`, `testing.md`)
7. Open Claude Code — everything is ready

## What to customize

| File | What to do |
|------|-----------|
| `CLAUDE.md` | Replace all placeholder sections with your project's info |
| `.engram/config.json` | Set `project_name` to your repo name |
| `.claude/rules/` | Add rules specific to your stack with `paths:` frontmatter |
| `.claude/agents/` | Add specialized sub-agents your project needs |

## Rules system

Rules in `.claude/rules/` support `paths:` frontmatter — they only load when Claude is working with matching files. This keeps context lean:

```markdown
---
description: API conventions
paths:
  - "src/modules/**"
---
Your rules here...
```

## Personal overrides

Copy `CLAUDE.local.md.example` to `CLAUDE.local.md` (gitignored). Use it for language preferences, local environment quirks, or personal workflow rules.
