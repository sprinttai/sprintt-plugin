---
description: Conduct a monthly financial review — input actuals, compare to targets, surface concerns, and identify next financial actions. Use at the end of each month or whenever you need a clear picture of business health.
---

# Financial Review

## Context
Before executing, read the following files directly from the **knowledge-base** directory (it is mounted and accessible — use the Read tool):
- `company/finances.md` — operating costs, revenue tracking, financial goals, budget rules, tool renewal dates, and tax notes
- `business-plan/plan.md` — financial projections, quarterly targets, success metrics, client concentration rules, and gross margin targets

Read both files before collecting any inputs. Pull all overhead figures, targets, margins, and rules directly from the KB — do not assume or hardcode any numbers.

## Inputs
Collect conversationally, one section at a time. Start with the numbers, then move to assessment.

**Before collecting any numbers — confirm Mercury is reconciled:**
Ask the user: has the Mercury account been reconciled this month? If no, prompt them to reconcile before proceeding. The accuracy of every calculation in this review depends on the Mercury balance and transaction history being current. Do not proceed with unreconciled numbers.

**Section 1 — Cash & Revenue**
1. **Month and year** being reviewed
2. **Mercury account balance** — the actual current balance after reconciliation
3. **Revenue received this month** — payments that actually landed in Mercury, not invoices sent
4. **Outstanding invoices** — for each outstanding invoice: client name, amount, invoice date, and due date (to distinguish current vs. overdue)
5. **YTD revenue** — total received since January 1 (or business start if mid-year)

**Section 2 — Expenses**
6. **Contractor costs paid this month** — total dollar amount already paid to contractors this month
7. **Contractor payments due but not yet paid** — any contractor invoices received but not yet paid, with amounts
8. **New or one-time expenses this month** — anything beyond the standard recurring overhead in `finances.md`, with amounts

**Section 3 — Business Health**
9. **Active projects with contractors** — for each project using a contractor this month: project name, total project revenue, and total contractor cost for that project (dollar amount, not hours — needed for gross margin calculation)
10. **Active clients and revenue per client** — needed for client concentration check
11. **Pipeline** — proposals out (with estimated values), discovery calls scheduled, deals close to closing

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process

Work through this skill conversationally, section by section. Present calculations and assessments after each section, ask if anything looks off, then move on. Do not output everything at once.

### Step 1 — Cash Position & Runway
After collecting Section 1 and 2 inputs:

- Pull monthly fixed overhead from `finances.md` (do not guess)
- Calculate **total monthly burn:** fixed overhead + contractor costs paid this month + additional expenses this month
- Calculate **true cash position:** Mercury balance - contractor payments due but not yet paid
- Calculate two runway figures:
  - **Fixed-cost runway:** Mercury balance ÷ fixed overhead — how long the business survives on subscriptions/tools alone if everything stopped
  - **Current burn runway:** true cash position ÷ total monthly burn — realistic runway at this month's actual spending rate. Only show this if total monthly burn exceeds fixed overhead; otherwise the two figures are the same.
- Calculate **net this month:** revenue received - fixed overhead - contractor costs paid - additional expenses
- Flag any outstanding invoices that are past their due date as **overdue** — these need immediate follow-up action, not just a note
- Present a clean cash summary and ask the user to confirm before proceeding

### Step 2 — Tax Set-Aside Check
After confirming cash position:

- Pull the tax set-aside guidance from `finances.md` (25-30% of revenue for taxes, including self-employment tax)
- Calculate the recommended set-aside amount based on revenue received this month: `revenue received × 0.275` (midpoint of 25-30%)
- Ask the user: has this amount been moved to a separate savings account or earmarked for taxes?
- If revenue has started coming in and no set-aside system is in place, flag this as high priority — self-employment tax (15.3% on net earnings) plus income tax is the most common financial surprise for new solo business owners
- **Estimated tax payment guidance:** Only surface quarterly estimated tax payment reminders once cumulative YTD revenue suggests Ricardo will owe $1,000+ in taxes for the year. Until that threshold is approaching, note that estimated payments are not yet required — but flag when they will be. Quarterly due dates: April 15, June 16, September 15, January 15.

### Step 3 — Revenue vs. Targets
- Pull the quarterly revenue target for the current period from `business-plan/plan.md`
- Calculate how much has been received this quarter vs. the target
- Assess pace: on track, behind, or ahead — and how much is needed in remaining weeks to hit the quarter
- Check YTD against the annual target

### Step 4 — Expense Review & Gross Margin Check
- Pull budget rules and gross margin targets from `finances.md` and `business-plan/plan.md`
- Total all expenses: fixed overhead + contractor costs paid + new/one-time expenses
- Check for budget rule violations (e.g., monthly overhead exceeding the target ceiling)
- Check tool renewal dates from `finances.md` — flag any tools renewing in the next 60 days

**Gross margin check (if contractor was used this month):**
- Pull gross margin targets from `business-plan/plan.md` (varies by engagement type — Ricardo-only vs. with contractor)
- For each active project with a contractor, use the contractor cost (dollar amount) provided in Section 3:
  - Calculate effective gross margin: `(project revenue - contractor cost) ÷ project revenue`
  - Compare to the target margin for that engagement type from `business-plan/plan.md`
  - Flag any project where actual margin is falling below target — this means contractor costs are eating more than expected and project pricing may need to be revisited

### Step 5 — Client Concentration Check
- Pull the client concentration rule from `business-plan/plan.md` (no single client should exceed 40% of revenue)
- If multiple clients are active: calculate each client's share of YTD revenue
- Flag any client approaching or exceeding the 40% threshold
- If only one client is active: note this as a concentration risk and flag building the pipeline as a priority

### Step 6 — Pipeline Assessment
- Review pipeline inputs against next quarter's target from `business-plan/plan.md`
- Assess whether the current pipeline is sufficient to hit next quarter's numbers
- Flag if pipeline is thin relative to the gap between current YTD and annual target

### Step 7 — Flags & Actions
Consolidate all flags from previous steps into a prioritized action list. Order by urgency:
1. Overdue invoices (immediate)
2. Contractor payments due but not yet sent (cash management)
3. Tax set-aside gap (immediate if revenue is coming in)
4. Gross margin below target on active projects
5. Budget rule violations
6. Tool renewals in next 30 days
7. Client concentration warnings
8. Pipeline gaps
9. Revenue tracking update — output the exact row to add to `finances.md` (see Output section)

### Step 8 — Bottom Line
Close with a 2-3 sentence plain-English summary: current financial health, the single most important action this month, and whether the business is on track for the quarter.

## Output

Present each step interactively. Final consolidated output:

---

**Financial Review — [MONTH YEAR]**

**Cash Position**
- Mercury balance (reconciled): $[AMOUNT]
- Contractor payments due but unpaid: -$[AMOUNT]
- True cash position: $[AMOUNT]
- Fixed overhead: $[AMOUNT from finances.md]
- Contractor costs paid: $[AMOUNT]
- Additional expenses: $[AMOUNT]
- Total burn this month: $[fixed overhead + contractor costs paid + additional expenses]
- Net this month: $[revenue received - fixed overhead - contractor costs paid - additional expenses]
- Fixed-cost runway: [X] months (Mercury balance ÷ fixed overhead)
- Current burn runway: [X] months (true cash position ÷ total burn) *(shown only if burn exceeds fixed overhead)*

**Invoices**
- Current (within terms): $[AMOUNT] — [CLIENT, DUE DATE]
- ⚠️ Overdue: $[AMOUNT] — [CLIENT, DAYS OVERDUE] — follow up immediately

**Tax Set-Aside**
- Recommended reserve this month: $[revenue × 0.275]
- Set aside: [YES / NO / PARTIAL — $AMOUNT]
- Estimated tax payment: [not yet required / due DATE — estimated $AMOUNT]

**Revenue vs. Targets**
- This quarter received: $[AMOUNT] of $[TARGET] — [X]% complete
- Remaining to hit quarter: $[AMOUNT] in [X] weeks
- YTD: $[AMOUNT] of $[ANNUAL TARGET]

**Gross Margin** *(if contractor involved)*
- [PROJECT]: [X]% actual margin vs. [Y]% target [⚠️ below target if applicable]

**Client Concentration**
- [CLIENT]: [X]% of YTD revenue [⚠️ approaching/exceeding 40% limit if applicable]

**Pipeline**
- Proposals out: [NUMBER] — estimated value $[AMOUNT]
- Discovery calls scheduled: [NUMBER]
- Pipeline assessment: [strong / adequate / thin]
- Gap to next quarter target: $[AMOUNT]

**Flags & Actions**
- [ ] [Prioritized action items]

**Revenue Tracking — Add to `finances.md`**
```
| [Month Year] | $[revenue received] | [client name(s)] | [brief note] |
```

**Bottom Line**
[2-3 sentence plain-English summary with the single most important action]

## Quality Checks
- Mercury reconciliation confirmed before any numbers collected
- Total monthly burn calculated correctly: fixed overhead + contractor costs paid + additional expenses
- Net this month includes all expense categories: fixed overhead + contractor costs paid + additional expenses
- Two runway figures shown when contractor burn is active; single figure when burn equals fixed overhead only
- True cash position accounts for contractor payments due but not yet sent
- Current burn runway uses true cash position ÷ total monthly burn — not fixed overhead alone
- All overhead figures pulled from `finances.md` — not guessed
- Contractor costs captured as dollar amounts per project — not hours — enabling accurate margin calculation
- Gross margin formula uses contractor cost (dollars): (project revenue - contractor cost) ÷ project revenue
- Outstanding invoices split into current vs. overdue — overdue flagged for immediate action
- Tax set-aside calculated as a specific dollar amount, not a vague reminder
- Estimated tax payment reminder only surfaced when YTD revenue suggests $1,000+ tax liability
- Client concentration calculated if multiple clients active — 40% rule from business plan applied
- Tool renewals in next 60 days checked against `finances.md` renewal dates
- Quarterly target sourced from `business-plan/plan.md`
- Revenue tracking row outputted in correct table format ready to paste into `finances.md`
- Skill worked conversationally — sections presented one at a time
