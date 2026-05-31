# Project management skills for AI coding agents

A small set of copy-pasteable, agent-agnostic project-management skills you can run with Claude Code, Cursor, Codex, ChatGPT, or any MCP-connected assistant. Each skill is a single Markdown file with a clear procedure and an output format — no install required.

## The skills

| Skill | Use it to |
|---|---|
| [task-breakdown](./task-breakdown.md) | Turn a feature or objective into scoped tasks with acceptance criteria |
| [sprint-planning](./sprint-planning.md) | Turn a prioritized backlog + capacity into a realistic iteration plan |
| [backlog-grooming](./backlog-grooming.md) | Clarify, split, estimate, and prioritize backlog items |
| [standup](./standup.md) | Generate a concise status update from recent commits, PRs, and tasks |

## How to use them

**Any chat agent (ChatGPT, Claude, …)** — paste the body of a skill, then add your inputs (the feature, the backlog, etc.).

**Claude Code** — drop a skill into `.claude/skills/<name>/SKILL.md` (each file already has `name`/`description` frontmatter), then invoke it by name. Or paste the body as a prompt.

**Cursor / Codex** — add the skill body to your rules/instructions file, or paste it inline.

**With an MCP-connected board** — if your agent is connected to a project-management tool over MCP (see the [comparison guide](../README.md)), these skills read and update real tasks through your MCP tools instead of just printing Markdown.

## Notes

These are deliberately tool-agnostic — they work with a plain-text backlog, a git history, or a live board. Tweak the output formats to match your team. PRs adding more skills are welcome.
