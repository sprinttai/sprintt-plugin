---
description: Conduct a monthly financial review — input actuals, compare to targets, surface concerns, and identify next financial actions. Use at the end of each month or whenever you need a clear picture of business health.
---

# Financial Review

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
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
6. **Contractor costs paid this month** — payments already sent to contractors
7. **Contractor payments due but not yet paid** — any contractor invoices received but not yet paid (affects true cash position)
8. **New or one-time expenses** — anything beyond the standard recurring overhead in `finances.md`

**Section 3 — Business Health**
9. **Active clients, revenue per client, and contractor hours used per project** — needed for both client concentration and gross margin checks
10. **Pipeline** — proposals out (with estimated values), discovery calls scheduled, deals close to closing

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process

Work through this skill conversationally, section by section. Present calculations and assessments after each section, ask if anything looks off, then move on. Do not output everything at once.

### Step 1 — Cash Position & Runway
After collecting Section 1 and 2 inputs:

- Pull monthly overhead from `finances.md` (do not guess)
- Calculate **true cash position:** Mercury balance - contractor payments due but not yet paid
- Calculate **runway:** true cash position ÷ monthly overhead = months of runway if revenue stopped today
- Calculate **net received this month:** revenue received - monthly overhead - contractor costs paid
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
- Total all expenses: standard overhead + contractor costs paid + new/one-time expenses
- Check for budget rule violations (e.g., monthly overhead exceeding the target ceiling)
- Check tool renewal dates from `finances.md` — flag any tools renewing in the next 60 days

**Gross margin check (if contractor was used this month):**
- Pull gross margin targets from `business-plan/plan.md` (varies by engagement type — Ricardo-only vs. with contractor)
- For each active project with a contractor: calculate effective gross margin using `(project revenue - contractor cost) ÷ project revenue`
- Compare to the target margin for that engagement type
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
9. Revenue tracking update (log this month in `finances.md`)

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
- Runway: [X] months at current overhead
- Revenue received this month: $[AMOUNT]
- Contractor costs paid: $[AMOUNT]
- Additional expenses: $[AMOUNT]
- Standard overhead: $[AMOUNT from finances.md]
- Net this month: $[AMOUNT]

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

**Bottom Line**
[2-3 sentence plain-English summary with the single most important action]

## Quality Checks
- Mercury reconciliation confirmed before any numbers collected
- True cash position accounts for contractor payments due but not yet sent
- Runway uses true cash position, not raw Mercury balance
- All overhead figures pulled from `finances.md` — not guessed
- Contractor costs paid and contractor costs owed tracked separately
- Outstanding invoices split into current vs. overdue — overdue flagged for immediate action
- Gross margin checked against targets from `business-plan/plan.md` for any project with contractor involvement
- Tax set-aside calculated as a specific dollar amount, not a vague reminder
- Estimated tax payment reminder only surfaced when YTD revenue suggests $1,000+ tax liability
- Client concentration calculated if multiple clients active — 40% rule from business plan applied
- Tool renewals in next 60 days checked against `finances.md` renewal dates
- Quarterly target sourced from `business-plan/plan.md`
- Skill worked conversationally — sections presented one at a time
- Revenue tracking update flagged as an action item every month
