# Project management skills for AI coding agents

A small set of project-management skills packaged for the open [agent skills ecosystem](https://github.com/vercel-labs/skills). Each skill is a `SKILL.md` you can install into Claude Code, Cursor, Codex, and 50+ other agents — or just read and paste.

## Install

```bash
# Install all skills (auto-detects the agents you have)
npx skills add SyntracAI/project-management-for-ai-coding-agents

# List what's available without installing
npx skills add SyntracAI/project-management-for-ai-coding-agents --list

# Install one skill to a specific agent
npx skills add SyntracAI/project-management-for-ai-coding-agents --skill task-breakdown -a claude-code
```

## The skills

| Skill | Use it to |
|---|---|
| [task-breakdown](./task-breakdown/SKILL.md) | Turn a feature or objective into scoped tasks with acceptance criteria |
| [sprint-planning](./sprint-planning/SKILL.md) | Turn a prioritized backlog + capacity into a realistic iteration plan |
| [backlog-grooming](./backlog-grooming/SKILL.md) | Clarify, split, estimate, and prioritize backlog items |
| [standup](./standup/SKILL.md) | Generate a concise status update from recent commits, PRs, and tasks |

## Use without the CLI

Every skill is a plain `SKILL.md`. You can also:
- **Paste** a skill's body into any chat agent (ChatGPT, Claude, …) and add your inputs.
- **Copy** a skill folder into your agent's skills directory manually (e.g. `.claude/skills/`).

## With an MCP-connected board

If your agent is connected to a project-management tool over MCP (see the [comparison guide](../README.md)), these skills read and update real tasks through your MCP tools instead of just printing Markdown.

## Contributing

Skills follow the [vercel-labs/skills](https://github.com/vercel-labs/skills) format: a directory containing a `SKILL.md` with `name` and `description` frontmatter. PRs adding more skills welcome.
