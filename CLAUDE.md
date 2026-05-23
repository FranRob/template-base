# [project-name]

[One-line description of the project and its main tech stack.]

## Commands

[Fill in the main commands to run, build, test, and deploy the project.]

```bash
# example
npm run dev     # Start dev server
npm run build   # Build for production
npm test        # Run tests
```

## Architecture

[Describe the folder structure and entry points. Keep it brief — focus on what's non-obvious.]

```
src/
├── [entry-point]    # [what it does]
└── [key folder]/    # [what it contains]
```

## Data Model

[List the core entities and their relationships. Only include what Claude needs to understand the domain.]

## Environment

[List required environment variables and where to put them.]

```
VARIABLE=value   # what it's for
```

## Priorities

1. **Order** — clean branches, one PR per block, linked issues
2. **Security** — auth, input validation, secrets
3. **Everything else**

## Workflow Rules

- **Never commit** unless the user explicitly confirms the feature works end-to-end
- **Full diagnosis before any fix** — identify ALL root causes first, state them, get confirmation, then code
- **No speculative improvements** — only change what was asked

## Rules (auto-loaded by Claude)

| File | When active |
|------|-------------|
| `.claude/rules/git-workflow.md` | Always |
| `.claude/rules/security.md` | Always |
| `.claude/rules/[stack].md` | When editing `src/**` — add your own |

## Available Agents

- `explorer` — maps codebase structure, never edits code
