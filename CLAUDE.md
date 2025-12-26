# Agent Guidelines

Guidance for AI agents working with this codebase.

**Read [MODUS-OPERANDI.md](MODUS-OPERANDI.md) for operational patterns**: decision authority, session handoff, verification, and anti-patterns.

## Project Overview

<!-- Replace this section with project-specific context -->

Describe what this project does, its core components, and key technologies.

## Directory Structure

```
docs/
  adr/            # Architecture decision records (immutable)
  architecture/   # System design, component diagrams, integration specs
  product/        # PRDs, feature specs, user stories
  roadmap/        # Milestones, planning, prioritization
  discovery/      # Research, spikes, technical exploration
  archive/        # Deprecated or superseded content
  tmp/            # Work in progress, drafts (not committed)
scripts/          # Reusable scripts, makefile commands
tmp/              # Transient work product (gitignored)
```

## Working Conventions

### General
- Use the current system date (`date`) for timestamps, not training knowledge cutoff dates
- Place temp files, scratch scripts, and transient work in `./tmp/` (not `/tmp/` or other OS locations) for easier cleanup
- Promote reusable scripts from `./tmp/` to `./scripts/` when they prove valuable

### Documentation
- Place research and exploration in `discovery/`
- Finalized designs go in `architecture/`
- Move superseded content to `archive/` with a note on what replaced it
- Use `tmp/` for drafts; clean up before committing

## Git Conventions

- Commit messages: concise, imperative mood, no attribution
- No author references, co-authors, or AI attribution in commits
- Before committing, verify git user is configured (`git config user.name` and `user.email`). If not configured, stop and ask the user to set it up.

## Skills

Before starting work, consider whether available skills apply to the task. Check `/help` or skill listings for relevant capabilities (documentation, architecture, code patterns, etc.).

## Key Decisions

<!-- Replace this section with project-specific architectural decisions -->

Document significant technical choices here, or reference ADRs in `docs/adr/`.
