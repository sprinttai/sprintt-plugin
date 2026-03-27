---
description: Conduct a monthly financial review — input actuals, compare to targets, surface concerns, and identify next financial actions. Use at the end of each month or whenever you need a clear picture of business health.
---

# Financial Review

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `company/finances.md` — operating costs, revenue tracking, financial goals, and budget rules
- `business-plan/plan.md` — financial projections, quarterly targets, and success metrics

These files are the source of truth for targets and overhead. Do not invent or assume any numbers.

## Inputs
Collect the following:

1. **Month and year** being reviewed (e.g., March 2026)
2. **Revenue received** — total payments received in Mercury this month (not invoiced, received)
3. **Outstanding invoices** — any invoices sent but not yet paid, and their amounts
4. **New expenses this month** — any one-time or new recurring costs beyond the standard overhead
5. **Active clients** — how many active engagements are currently in progress?
6. **Pipeline** — any proposals out, discovery calls scheduled, or deals close to closing?

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Pull the current monthly overhead from `finances.md` (do not guess — read it)
3. Pull the quarterly revenue target for the current period from `business-plan/plan.md`
4. Calculate:
   - Net revenue this month (received - overhead)
   - Year-to-date revenue (ask user for YTD if not provided)
   - Monthly run rate vs. quarterly target pace
   - Months of runway at current burn if revenue were zero (overhead ÷ 1)
5. Assess financial health across three dimensions:
   - **Revenue:** On track, behind, or ahead of quarterly target?
   - **Expenses:** Any budget rule violations or new subscriptions to evaluate?
   - **Pipeline:** Is there enough in the pipeline to hit next quarter's target?
6. Surface any tax reminders relevant to the current period (quarterly estimated payments, etc.)

## Output

**Financial Review — [MONTH YEAR]**

**Revenue**
- Received this month: $[AMOUNT]
- Outstanding invoices: $[AMOUNT] (due [dates])
- YTD revenue: $[AMOUNT]
- Quarterly target pace: [on track / behind / ahead] — need $[X] more by [end of quarter]

**Expenses**
- Standard monthly overhead: $[AMOUNT from finances.md]
- Additional expenses this month: $[AMOUNT] — [description]
- Total expenses: $[AMOUNT]
- Net this month: $[AMOUNT]

**Pipeline Health**
- Active clients: [NUMBER]
- Proposals out: [NUMBER] — estimated value $[AMOUNT]
- Upcoming opportunities: [brief summary]
- Pipeline assessment: [strong / adequate / thin]

**Flags & Actions**
- [ ] [Any budget rule violations, approaching limits, or concerns]
- [ ] [Tax reminders — quarterly payment due? Set-aside check?]
- [ ] [Revenue tracking update — log this month in finances.md]
- [ ] [Any tools up for renewal this month?]

**Bottom Line**
[2-3 sentence plain-English summary of business health and the most important thing to do this month]

## Quality Checks
- Revenue figure is payments received, not invoices sent
- Overhead pulled from `finances.md` — not guessed
- Quarterly target sourced from `business-plan/plan.md`
- Tax reminders are surfaced if it's a quarterly payment month (April, June, September, January)
- Flags are specific and actionable, not vague observations
