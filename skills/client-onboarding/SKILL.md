---
description: Walk through the full client onboarding lifecycle — pre-kickoff through closeout — with contractor steps, invoice reminders, and phase-by-phase checklists. Use when a new client has signed or at any point during an active engagement.
---

# Client Onboarding

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `operations/client-onboarding.md` — the full onboarding checklist by phase
- `operations/workflows.md` — the lead-to-client pipeline and delivery standards
- `company/entity.md` — Sprintt's legal name and contact info for any client-facing documents
- `services/pricing.md` — payment structure rules, retainer terms, expense reimbursement policy, and out-of-scope billing rates

These files are the source of truth. Do not invent or assume any onboarding steps or billing rules.

## Inputs
Collect the following:

1. **Client name** — the company or individual being onboarded
2. **Project name** — the engagement name or SOW title
3. **Engagement type** — Design Partner, Standard Client, or Retainer (Advisor / Builder / Partner tier)
4. **Signed date** — when was the agreement fully executed?
5. **SOW payment schedule** — the milestone breakdown and total fee (e.g., "$10,000 total: 40% upfront, 30% at midpoint, 30% on delivery"). For retainers: monthly rate and tier.
6. **Contractor involved?** — is an SDLC contractor on this engagement? (yes/no — if yes, ask for their name/role and agreed hourly rate)
7. **Current phase** — starting from scratch (pre-kickoff) or mid-engagement? If mid-engagement, which steps are already complete?

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process

### Step 1 — Contractor Setup (if applicable)
If a contractor is involved, address these before any other onboarding steps:

**Agreements & compliance:**
- Has Sprintt's NDA been executed with the contractor? (separate from the client NDA)
- Has the contractor provided their W-9? (required to file a 1099-NEC if they earn $600+ this year — collect it now, before work begins)
- Has the contractor's rate and payment terms been agreed and documented? (when do you pay them — per milestone, net 30, upon client payment? — get this in writing)

**Alignment:**
- Has the contractor reviewed the SOW and confirmed their availability for the full timeline?
- Does the contractor know what's in scope and out of scope?
- Does the contractor understand that all client communication goes through Ricardo — they do not contact the client directly?
- Are system access invitations for the contractor queued (to be sent after client grants access)?

Flag any outstanding items before proceeding. The contractor must be fully aligned and documented before kickoff.

### Step 2 — Capture All Client Contacts
Before kickoff, confirm three distinct contacts on the client side:

- **Primary POC** — day-to-day communication (name, email, phone)
- **Billing contact** — who approves and processes invoices (often a different person, especially at companies). If same as POC, confirm explicitly.
- **Escalation contact** — who to go to if the primary POC is unresponsive and something is blocking delivery

Missing the billing contact is the most common reason invoices get delayed. Capture all three upfront.

### Step 3 — Walk Each Phase
Present each phase of the checklist from `operations/client-onboarding.md` in order. Cover all phases:

- **Pre-Kickoff** (must complete within 48 hours of signed agreement)
- **Kickoff Meeting** — see Step 4 for items to add beyond the standard checklist
- **Post-Kickoff** (within first week) — see Step 5 for access tracking
- **Ongoing Throughout Engagement** — these are weekly recurring actions for the life of the engagement, not a one-time checklist. Present them as a cadence to set up, not items to check off once.
- **Closeout**

For each phase, present the items as a scannable checklist. Ask the user to confirm which are done and which are outstanding. Flag any time-sensitive items based on the signed date.

### Step 4 — Kickoff Meeting Additions
In addition to the standard kickoff checklist items, confirm the following are covered during the kickoff meeting:

**Scope change process:**
Explicitly communicate to the client: all scope changes must be documented in writing and approved before work begins. No verbal change orders. Out-of-scope work is billed at the standard hourly rate ($225/hr) — the client needs to hear this number at kickoff, not when they see it on an invoice.

**Deliverable approval process:**
Walk the client through how approvals work. Per the SOW:
- Deliverables are submitted for review with a clear acceptance window (typically 5–7 business days — confirm the specific timeframe in the SOW)
- If no feedback is received within that window, the deliverable is deemed accepted
- Feedback must be consolidated — one round of revisions per deliverable unless additional rounds are scoped

**Expense reimbursement:**
Remind the client (even though it's in the contract) that out-of-pocket costs incurred on their behalf — API credits, third-party tool licenses, travel — are passed through at cost. Any single expense over $100 requires prior written approval. Establishing this verbally at kickoff prevents surprise invoice line items later.

**Retainer-specific (if applicable):**
If this is a retainer engagement, walk the client through:
- Billing is monthly in advance
- Unused hours do not roll over
- Overages beyond the monthly commitment are billed at $225/hr at end of month
- Pausing is not available during the initial 3-month commitment; after that, one pause per 12 months with 30 days written notice

### Step 5 — Document Access Requirements
At kickoff, the "Access requirements identified" checklist item must produce an explicit list — not just a conversation. For each system, dataset, or tool Ricardo needs:

- What is it? (e.g., GitHub repo, Salesforce sandbox, Google Analytics)
- Who on the client side is responsible for granting access?
- What is the expected turnaround?

Output this as a named access list. Post-kickoff can then be checked against it item by item. Without a list, "all access received" has no definition.

### Step 6 — Invoice Reminder Schedule
Using the SOW payment schedule provided, calculate each invoice milestone and output a calendar reminder schedule.

**For project engagements:**
- Calculate the exact dollar amount for each milestone
- Assign a target invoice date for each
- If a milestone invoice goes unpaid past Net 15, work pauses until payment is received

**For retainer engagements:**
- First invoice is due before the engagement begins (billed in advance)
- Set a recurring monthly reminder to invoice on the same day each month
- Flag the overage billing reminder: review hours used at end of each month and invoice any overages separately

Output as a table the user can use to set calendar reminders.

### Step 7 — Late Payment Protocol
Surface the late payment process so it's understood before it's needed:

- Invoice due date: Net 15 from invoice date (unless otherwise agreed in the SOW)
- Day 16: Follow up with a polite but direct email if unpaid
- Day 21+: Work pauses. Notify the client in writing that work is on hold pending payment per the consulting agreement
- Day 30+: Late payment interest begins accruing at 1.5% per month per the contract
- Do not absorb late payments silently — the contract gives you the right to pause and charge interest. Use it.

### Step 8 — Summarize Outstanding Actions
After all phases, output a prioritized list of everything still outstanding, ordered by urgency.

## Output

**Onboarding Tracker: [CLIENT NAME] — [PROJECT NAME]**
- Engagement type: [TYPE]
- Signed: [DATE]
- Contractor: [YES — [NAME/ROLE] / NO]

---

**Contractor Setup** *(if applicable)*
- [ ] NDA executed with contractor
- [ ] W-9 collected from contractor
- [ ] Payment terms agreed and documented — [terms]
- [ ] Contractor confirmed availability for full timeline
- [ ] Rate agreed: $[RATE]/hr
- [ ] Scope briefing complete — contractor knows what's in/out and that all client comms go through Ricardo
- [ ] System access invitations queued

---

**Client Contacts**
- Primary POC: [NAME] — [EMAIL] — [PHONE]
- Billing contact: [NAME] — [EMAIL] *(confirm separately from POC)*
- Escalation contact: [NAME] — [EMAIL]

---

**[Phase Name]**
- [x] Completed item
- [ ] Outstanding item — [note or deadline]

*(Repeat for all five phases — mark Ongoing items as weekly recurring, not one-time)*

---

**Kickoff Agenda Additions**
- [ ] Scope change process communicated — client understands all changes require written approval; out-of-scope work billed at $225/hr
- [ ] Deliverable approval process communicated — client understands the acceptance window and deemed acceptance clause
- [ ] Expense reimbursement communicated — pass-through at cost, expenses over $100 require prior written approval
- [ ] Retainer terms communicated *(if applicable)* — billing in advance, no rollover, overage rate, pause policy

---

**Access Requirements** *(produced at kickoff)*
| System / Tool | Owner on Client Side | Expected Turnaround | Received? |
|---------------|---------------------|--------------------:|-----------|
| [e.g., GitHub repo] | [NAME] | [DATE] | [ ] |
| [e.g., Salesforce sandbox] | [NAME] | [DATE] | [ ] |

---

**Invoice Reminder Schedule**
| Milestone | Amount | Target Invoice Date | Follow-Up If Unpaid |
|-----------|--------|---------------------|---------------------|
| Upfront deposit | $[X] | [DATE] | N/A — collect before kickoff |
| Midpoint | $[X] | [DATE] | [DATE + 16 days] |
| Final delivery | $[X] | [DATE] | [DATE + 16 days] |

*(For retainers: recurring monthly invoice on [DAY] + end-of-month overage check)*

**Late payment protocol:** Day 16 — follow up. Day 21 — pause work, notify in writing. Day 30 — interest accrues at 1.5%/mo.

---

**Your Next Actions (in order):**
1. [Most urgent outstanding item]
2. [Next item]
3. ...

---

**Standing Reminders**
- First payment must be confirmed in Mercury before kickoff
- Kickoff meeting must be scheduled within 1 week of signing
- Add client to revenue tracking in `company/finances.md`
- Save signed agreement AND SOW to Google Drive: `Clients/[ClientName]/[ProjectName]`
- Professional liability (E&O) insurance: not yet in place — low risk now, revisit as engagements grow
- Weekly status updates are a recurring commitment — set a recurring calendar reminder

## Quality Checks
- All three client contacts captured (primary POC, billing, escalation)
- Contractor W-9 and payment terms flagged if a contractor is involved — do not skip
- Ongoing phase items presented as a weekly recurring cadence, not a one-time checklist
- Scope change process, out-of-scope rate ($225/hr), deliverable approval, and expense reimbursement all included in kickoff agenda
- Retainer-specific billing terms covered at kickoff if engagement type is retainer
- Access requirements documented as a named list at kickoff — not a general conversation
- Invoice schedule reflects project or retainer billing correctly
- Late payment protocol always included — not optional
- Design Partner closeout includes case study initiation and referral conversation
- No phase is skipped — all five phases presented even if starting mid-engagement
