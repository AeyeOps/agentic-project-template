# Modus Operandi

Operational patterns for agents working on this project.

## Session Start

Start by reading `./CLAUDE.md` for project context. Check `./STATUS.md` if present for current state. Review relevant subdirectory CLAUDE.md files for local conventions. Consider whether available skills apply (`/help` or skill listings).

## Decision Authority

### Proceed Without Asking
- File organization within established directories
- Code formatting and style consistency
- Routine documentation updates
- Creating files in `tmp/` or `scripts/`
- Git commits (when user requests)

### Confirm First
- New top-level directories
- Architectural changes or new patterns
- Adding external dependencies
- Deleting or archiving existing content
- Changes affecting multiple subsystems

## Session Handoff

When work spans sessions or may be continued later, update or create `STATUS.md`:

```markdown
## Current Focus
Active work in progress.

## Blockers
What's waiting on external input or decision.

## Next Steps
Prioritized list of what should happen next.

## Context
Key information the next session needs.
```

## Verification

Before considering work complete, confirm:
- Changes align with existing patterns — check similar files for conventions
- No obvious regressions introduced
- Documentation updated if behavior changed
- `make check` or equivalent run if available

## Avoid

- Modifying ADRs — they're immutable records; create a new one that supersedes
- Creating parallel structures — extend existing patterns when possible
- Over-engineering — solve the immediate requirement, not hypothetical futures
- Committing without git user configured — commits need valid attribution
- Using `/tmp/` or OS temp locations — project's `./tmp/` keeps artifacts discoverable for cleanup
- AI attribution in commits — keep commit history neutral

## CLAUDE.md Hierarchy

When multiple CLAUDE.md files exist, read in this order because each layer adds specificity:

1. `./CLAUDE.md` — project root, read first for overall context
2. `./MODUS-OPERANDI.md` — operational patterns (this file)
3. Subdirectory CLAUDE.md — local conventions for that area

Later files add context; they refine rather than override earlier guidance.

## Working Memory

| Need | Location |
|------|----------|
| Scratch work, experiments | `./tmp/` (gitignored) |
| Draft documentation | `./docs/tmp/` (gitignored) |
| Persistent working notes | `./docs/discovery/` with WIP prefix |
| Reusable scripts | `./scripts/` |

## Communication Style

- Lead with the answer, then explain if needed
- State uncertainty directly rather than hedging
- Disagree when there's good reason
- Concise responses; expand when asked
