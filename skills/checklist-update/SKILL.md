---
description: Review the Sprintt business launch checklist, surface what's been completed, and identify the next 3-5 priorities to tackle. Use for a periodic business health check or when you're not sure what to focus on next.
---

# Checklist Update

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `business-plan/checklist.md` — the master Sprintt launch checklist organized by phase

This file is the source of truth. Do not invent or assume any checklist items.

## Inputs
Collect the following:

1. **What's changed since the last review?** — Ask the user what they've accomplished recently that might need to be marked complete. They may also mention blockers on specific items.
2. **Any specific phase to focus on?** — Optional. If the user wants to focus on marketing, legal, or a specific area, note it.
3. **Current date** — Use today's date to assess time-sensitive items (e.g., Florida Annual Report due May 1, 2027).

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read `business-plan/checklist.md` from the KB
2. Present a summary of completion status by phase — how many items are done vs. total in each phase
3. Ask the user to confirm any newly completed items based on what they shared
4. Identify all outstanding items across all phases
5. Prioritize the next 3-5 actions using this logic:
   - **Blocking items first** — anything that prevents other work from happening
   - **Revenue-impact items second** — anything that directly affects ability to get paid or win clients
   - **Time-sensitive items third** — anything with a real deadline approaching
   - **Quick wins fourth** — items that are low-effort and would meaningfully advance the checklist
6. Flag any items that are time-sensitive based on today's date
7. Note any recurring tasks (monthly/quarterly) that are due

## Output

**Checklist Review — [DATE]**

**Progress by Phase**
| Phase | Done | Total | Status |
|-------|------|-------|--------|
| Phase 1: Legal & Entity | X | X | [Complete / In Progress / Not Started] |
| Phase 2: Brand & Digital | X | X | ... |
| Phase 3: Service & Ops | X | X | ... |
| Phase 4: KB & Automation | X | X | ... |
| Phase 5: Marketing & Outreach | X | X | ... |
| Phase 6: First Clients | X | X | ... |
| Phase 7: Growth | X | X | ... |

**Newly Completed (this session)**
- [Item just marked complete based on user input]

**Your Next 3-5 Priorities**
1. [Highest priority item] — [why it's first]
2. [Next item] — [brief rationale]
3. ...

**Time-Sensitive Flags**
- [Any deadline-driven items, e.g., "Florida Annual Report due May 1, 2027 — 13 months away"]

**Recurring Tasks Due**
- [Any monthly/quarterly tasks that should be running by now]

**To update the checklist:** Mark items complete in `business-plan/checklist.md` in your knowledge-base repo.

## Quality Checks
- Phase completion counts are accurate — count actual checkboxes, don't estimate
- Priorities are actionable today, not vague goals
- Blocking items (e.g., insurance before first client delivery) are surfaced before convenience items
- Time-sensitive dates are calculated from today's actual date
- Recurring tasks are surfaced if any revenue or client activity has started
