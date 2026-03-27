---
description: Review the Sprintt business launch checklist, surface what's been completed, and identify the next 3-5 priorities to tackle. Use for a periodic business health check or when you're not sure what to focus on next.
---

# Checklist Update

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `business-plan/checklist.md` — the master Sprintt launch checklist organized by phase

This file is the source of truth. Do not invent or assume any checklist items. Work only with what is in the file.

## Inputs
Collect the following:

1. **What's changed since the last review?** — Ask the user what they've accomplished recently that might need to be marked complete. They may also mention blockers on specific items.
2. **Has revenue or client work started?** — Ask explicitly. This determines whether recurring monthly/quarterly tasks should be surfaced as active obligations or future ones.
3. **Any specific phase to focus on?** — Optional. If the user wants to focus on a particular area, note it.

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read `business-plan/checklist.md` from the KB
2. Scan the checklist for two things before presenting anything:
   - **Deadline language** — any item containing a date, deadline, due date, or time reference. Calculate urgency from today's date and flag these items prominently, regardless of which phase they're in.
   - **Inconsistencies** — any unchecked item whose checklist text suggests it should be complete given the state of other items (e.g., a prerequisite is unchecked but a dependent item is checked). Surface these as warnings, not assumptions.
3. Present a summary of completion status by phase — how many items are done vs. total in each phase
4. Ask the user to confirm any newly completed items based on what they shared
5. Identify all outstanding items across all phases
6. Prioritize the next 3-5 actions using this logic:
   - **Deadline-driven items first** — anything with a date or deadline in the checklist text, ordered by urgency
   - **Blocking items second** — anything that prevents other work from happening
   - **Revenue-impact items third** — anything that directly affects ability to get paid or win clients
   - **Quick wins fourth** — items that are low-effort and would meaningfully advance the checklist
7. Surface recurring tasks (monthly/quarterly) from the checklist only if the user confirmed revenue or client work has started — otherwise note them as upcoming obligations to be aware of

## Output

**Checklist Review — [DATE]**

**⚠️ Time-Sensitive Items** *(surfaced before anything else if found)*
- [Item with deadline language] — [calculated urgency from today's date]

**⚠️ Inconsistencies Detected** *(if any)*
- [Item that appears inconsistent given the state of other items in the checklist]

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

**Recurring Tasks** *(shown only if revenue or client work has started)*
- [Monthly/quarterly tasks from the checklist that are now active obligations]

**To update the checklist:** Mark items complete in `business-plan/checklist.md` in your knowledge-base repo.

## Quality Checks
- Deadline language scanned from checklist text — urgency calculated from today's actual date, not estimated
- Inconsistencies flagged based on checklist state only — no assumptions about items not in the file
- Phase completion counts are accurate — count actual checkboxes, don't estimate
- Recurring tasks surfaced only if user confirmed revenue or client work has started
- Priorities are actionable today, not vague goals
- No checklist items invented — all output derives from what is in `business-plan/checklist.md`
