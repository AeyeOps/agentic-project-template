# Discovery Docs

Research, spikes, and exploration.

## Conventions

- Start with the question being answered
- Document options considered and trade-offs
- End with recommendation or decision
- Date prefix helps track currency: `2025-01-auth-options.md`

## Structure

```markdown
# Discovery: [Topic]

## Question
What we're trying to understand or decide.

## Options Considered
1. Option A - pros, cons
2. Option B - pros, cons

## Recommendation
What we suggest and why.

## Next Steps
Actions to take based on findings.
```

## Lifecycle

Discovery concludes when a decision is made. At that point:
- Create an ADR in `adr/` capturing the decision
- Update or create docs in `architecture/` with the design
- Archive the discovery doc or leave in place for context
