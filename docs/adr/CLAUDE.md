# Architecture Decision Records

Immutable decision log. Record significant technical choices here.

## Format

```markdown
# ADR-NNN: Short Title

Status: proposed | accepted | superseded | rejected
Date: YYYY-MM-DD
Supersedes: ADR-XXX (if applicable)

## Context
What prompted this decision.

## Decision
What we chose and why.

## Consequences
Trade-offs accepted, follow-on work required.
```

## Conventions

- Naming: `adr-NNN-short-title.md` (zero-padded number)
- Status values: proposed, accepted, superseded, rejected
- To change a decision: create new ADR that supersedes the original
- Link from `architecture/` docs back to relevant ADRs for context

## Why Immutable

ADRs capture the decision moment with its context. Modifying them loses historical reasoning. When circumstances change, a new ADR explains the evolution.
