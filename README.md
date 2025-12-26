# Agentic Project Template

A project structure optimized for AI coding agent collaboration. Provides conventions for documentation, architecture decisions, and session continuity that help agents understand context quickly and work effectively across sessions.

## About

This template is an [AeyeOps](https://github.com/AeyeOps) initiative, distilling patterns we've found effective when working with AI coding agents. It represents accumulated learnings from real-world usage and serves as a living baseline we'll continue refining.

**Current state:** The conventions here evolved primarily through Claude Code usage, so some patterns reflect that tool's strengths. As the agentic coding landscape matures—with tools like OpenAI Codex emerging as strong contenders—we aim to generalize these patterns for broader applicability.

Contributions and feedback from teams using other agents are welcome.

## Usage

### Create a New Project

**Via GitHub UI:**
1. Click the green "Use this template" button above
2. Choose "Create a new repository"
3. Name your project and select visibility

> **Note:** GitHub may briefly show a 404 after redirect. Refresh if needed—the repo is being provisioned.

**Via CLI:**
```bash
gh repo create my-project --template AeyeOps/agentic-project-template --public
cd my-project
```

**Manual clone (without GitHub):**
```bash
git clone --depth 1 https://github.com/AeyeOps/agentic-project-template.git my-project
cd my-project
rm -rf .git
git init
```

### After Creating

1. Update `CLAUDE.md` with your project overview and key decisions
2. Rename `CLAUDE.md` files if your tooling uses different conventions
3. Start adding content to the appropriate directories

## Structure

```
CLAUDE.md             # Agent guidelines (customize for your project)
MODUS-OPERANDI.md     # Operational patterns (use as-is or adapt)
docs/
  adr/                # Architecture decision records (immutable)
  architecture/       # System design specifications
  product/            # PRDs and feature specs
  roadmap/            # Planning and milestones
  discovery/          # Research and exploration
  archive/            # Superseded content
scripts/              # Reusable automation
tmp/                  # Transient work (gitignored)
```

## Key Files

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Project context and conventions for agents |
| `MODUS-OPERANDI.md` | Operational patterns: decision authority, session handoff, verification |
| `docs/*/CLAUDE.md` | Directory-specific guidance |
| `STATUS.md` | Session continuity (created as needed) |

## Design Principles

- **Progressive disclosure** — CLAUDE.md hierarchy layers context from general to specific
- **Clear decision authority** — Explicit boundaries on autonomous vs. confirm-first actions
- **Session continuity** — STATUS.md convention enables effective handoff between sessions
- **Immutable decisions** — ADRs capture context at decision time; supersession pattern for changes
- **Minimal structure** — Just enough convention to be useful without over-engineering

## Adapting for Other Agents

The `CLAUDE.md` naming convention works with Claude Code's automatic context loading. Other tools may use different patterns:

- **Codex**: Consider `AGENTS.md` or tool-specific conventions as they emerge
- **Cursor/Windsurf**: May recognize different instruction file patterns
- **Generic**: Rename to `AGENT.md` or `AI.md` and configure your tool accordingly

The content and structure matter more than the filename—adapt as needed for your toolchain.

## Contributing

This is a living template. If you've found patterns that work well with agentic workflows—regardless of which tool you use—we'd welcome contributions:

- Open an issue to discuss structural changes
- Submit PRs for documentation improvements
- Share what works (or doesn't) with different AI coding tools

## License

Apache 2.0 — see [LICENSE](LICENSE)

---

Part of the [AeyeOps](https://github.com/AeyeOps) project family.
