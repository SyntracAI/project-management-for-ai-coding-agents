---
name: task-breakdown
description: Decompose a feature or objective into small, independently shippable tasks, each with explicit acceptance criteria, size, and dependencies. Use at the start of a feature, when a ticket is too big to estimate, or before sprint planning.
license: MIT
metadata:
  author: SyntracAI
  version: '1.0.0'
---

# Task breakdown

Turn a feature or objective into a set of small, well-scoped tasks an AI coding agent (or a human) can pick up and finish in about a day.

## When to use
- A ticket or feature is too large or vague to estimate or start.
- Before sprint planning or grooming.
- When work keeps spilling over because tasks are too big.

## Inputs
- The feature / objective (one or two sentences).
- Known constraints (deadline, tech, dependencies).
- Optional: the relevant part of the codebase the agent can read.

## Steps
1. **Restate the goal and the definition of done** in one sentence each. If you can't, ask for clarification before continuing.
2. **Find the vertical slices.** Split by user-visible outcome, not by layer — each slice should be independently testable and, ideally, shippable behind a flag.
3. **Write each task** with:
   - an imperative title ("Add …", "Migrate …") — if the title needs "and", split it;
   - **Scope**: what's explicitly in and out;
   - **Acceptance criteria**: a short checklist or Given/When/Then; no task ships without these;
   - **Dependencies**: tasks or facts it needs first;
   - **Size**: S (<½ day), M (~1 day), L (split it).
4. **Sequence** by dependency, and put the riskiest or most uncertain task first to de-risk early.
5. **List open questions** that block estimating or starting.

## Output format
```
Goal: <one sentence>
Definition of done: <one sentence>

| # | Task | Size | Depends on | Acceptance criteria |
|---|------|------|-----------|---------------------|
| 1 | ...  | M    | —         | - [ ] ...           |

Open questions:
- ...
```

## Guardrails
- No task larger than ~1 day; split anything bigger.
- Every task has acceptance criteria.
- Prefer thin end-to-end slices over horizontal "do all the backend" tasks.
