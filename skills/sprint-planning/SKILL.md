---
name: sprint-planning
description: Turn a prioritized backlog and a known team capacity into a realistic, committed iteration plan with a single goal, a dependency-ordered task list, and a buffer. Use at the start of a sprint or iteration.
license: MIT
metadata:
  author: SyntracAI
  version: '1.0.0'
---

# Sprint planning

Convert a prioritized backlog plus capacity into an honest iteration commitment — what the team will actually finish, not a wish list.

## When to use
- Start of a sprint or iteration.
- Re-planning mid-cycle after scope changes.

## Inputs
- A **prioritized** backlog (if it isn't prioritized and ready, run `backlog-grooming` first).
- Team **capacity** for the iteration (person-days, or velocity in points).
- Iteration length and any fixed dates.

## Steps
1. **Write one sprint goal** — a single sentence describing the outcome. If you need "and", the sprint is unfocused; pick the most valuable thread.
2. **Check readiness.** Each candidate item must have clear acceptance criteria and no blocking unknowns. Send unready items back to grooming — do not commit them.
3. **Fill to ~80% of capacity**, top of the backlog first. Leave a buffer for review, bugs, and interruptions.
4. **Order by dependency** and pull risky or uncertain work earlier.
5. **Name the risks** and pick one **stretch** item to pull in only if you finish early.

## Output format
```
Sprint goal: <one sentence>
Capacity: <X person-days>  Committed: <~80%>  Buffer: <~20%>

| # | Item | Size | Owner | Ready? | Notes |
|---|------|------|-------|--------|-------|

Risks:
- ...
Stretch (only if ahead):
- ...
Deferred / not ready:
- ...
```

## Guardrails
- Never commit to 100% of capacity.
- Every committed item is Ready (has acceptance criteria, no blocking unknowns).
- One goal per sprint.
