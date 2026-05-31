---
name: backlog-grooming
description: Clarify, split, estimate, and prioritize raw backlog items so they are ready to plan. Produces a groomed, ordered backlog with acceptance criteria and a value/effort priority. Use before sprint planning or whenever the backlog gets messy.
license: MIT
metadata:
  author: SyntracAI
  version: '1.0.0'
---

# Backlog grooming

Take a messy backlog and make it plannable: each item clear, appropriately sized, estimated, and prioritized.

## When to use
- The backlog has vague, oversized, or duplicate items.
- Before sprint planning.
- On a recurring cadence (for example, weekly).

## Inputs
- The raw backlog (titles, notes, tickets).
- Optional: product goals to prioritize against.

## Steps
For **each item**:
1. **Clarify** the value in one sentence: "As <who>, I want <what>, so that <why>." Drop or merge anything with no clear value.
2. **Split** anything larger than ~1 day or with multiple distinct outcomes (use `task-breakdown`).
3. **Write acceptance criteria** — a short checklist of what "done" means.
4. **Estimate** relatively (S/M/L or points). Flag anything you can't estimate as **Not ready** with the open question attached.
5. **Prioritize** by value versus effort. A simple score is `priority = value / effort`; for more nuance use RICE-lite (Reach × Impact × Confidence ÷ Effort).
6. Mark each item **Ready** or **Not ready**.

Then **sort** the backlog by priority, Ready items on top.

## Output format
```
| Rank | Item | Value | Effort | Priority | Ready? | Acceptance criteria |
|------|------|-------|--------|----------|--------|---------------------|

Needs decisions:
- <item> — <open question>
```

## Guardrails
- No item is "Ready" without acceptance criteria and an estimate.
- Split before you estimate — don't estimate a blob.
- Re-groom regularly; a stale backlog rots.
