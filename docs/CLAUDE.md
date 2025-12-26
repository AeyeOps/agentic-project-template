# Docs Directory Guidelines

How to use and maintain this documentation structure.

## Directory Purpose

| Directory | Use For | Move Out When |
|-----------|---------|---------------|
| `adr/` | Architecture decision records (immutable) | Never modify; supersede with new ADR |
| `architecture/` | Finalized system design, component specs | Update in place |
| `product/` | PRDs, feature specs, user stories | Superseded by new version |
| `roadmap/` | Milestones, planning, priorities | Completed or abandoned |
| `discovery/` | Research, spikes, exploration | Decision made |
| `archive/` | Superseded or deprecated content | Never |
| `tmp/` | Drafts, WIP, scratch | gitignored |

## Workflow

1. **New ideas** start in `discovery/` for exploration
2. **Decisions** become ADRs in `adr/`, designs go to `architecture/`
3. **Prioritized work** spawns PRDs in `product/` from `roadmap/` items
4. **Superseded content** moves to `archive/` with replacement note

## File Conventions

- Naming: `kebab-case.md` (lowercase, hyphens, no spaces)
- Descriptive names: `auth-flow.md` rather than `design.md`
- Date prefix when time-sensitive: `2025-01-auth-options.md`
- Relative paths for internal links
- Archive header: `> Superseded by: [replacement](../path)`

## Adding Content

Consider whether similar content exists before creating new files. Discovery docs benefit from stating the question upfront. Architecture docs serve as authoritative references. Prefer one concept per file; split large docs by concern.
