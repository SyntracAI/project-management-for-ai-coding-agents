---
name: standup
description: Generate a concise daily standup update (Yesterday / Today / Blockers) from recent activity — git commits, merged or open PRs, and task-board changes. Use for an individual or to summarize a whole team's day.
license: MIT
metadata:
  author: SyntracAI
  version: '1.0.0'
---

# Standup

Produce a tight standup update from what actually happened, instead of trying to remember it.

## When to use
- Daily async or live standup.
- A quick status update for a stakeholder.

## Inputs (use whatever is available)
- Recent **git history**: `git log --since="yesterday" --author="<you>" --oneline`, plus merges and PRs.
- The **task board** state if your agent is connected over MCP (in-progress, done, blocked).
- Anything you remember that isn't in the tools (decisions, conversations).

## Steps
1. **Gather** yesterday's done work from commits and PRs, and any tasks moved to Done.
2. **Yesterday** — list what was completed, as outcomes not activity ("shipped X", not "worked on X").
3. **Today** — the 1–3 things you'll actually finish, tied to the current goal or sprint.
4. **Blockers** — anything waiting on a person, decision, or dependency. Be specific and name who or what would unblock it. "None" is a valid answer.
5. Keep it to a few bullets per section. A standup is a signal, not a report.

## Output format
```
**<name> — <date>**
Yesterday:
- ...
Today:
- ...
Blockers:
- ... (or "none")
```

## Guardrails
- Outcomes, not activity logs.
- Surface blockers loudly — that's the point of a standup.
- If you have nothing for "Today" that ties to the goal, that's itself worth raising.
