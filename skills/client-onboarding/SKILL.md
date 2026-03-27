---
description: Walk through the full client onboarding lifecycle — pre-kickoff through closeout — with contractor steps, invoice reminders, and phase-by-phase checklists. Use when a new client has signed or at any point during an active engagement.
---

# Client Onboarding

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `operations/client-onboarding.md` — the full onboarding checklist by phase
- `operations/workflows.md` — the lead-to-client pipeline and delivery standards
- `company/entity.md` — Sprintt's legal name and contact info for any client-facing documents

These files are the source of truth. Do not invent or assume any onboarding steps.

## Inputs
Collect the following:

1. **Client name** — the company or individual being onboarded
2. **Project name** — the engagement name or SOW title
3. **Engagement type** — Design Partner or Standard Client (affects closeout steps)
4. **Signed date** — when was the agreement fully executed?
5. **SOW payment schedule** — the milestone breakdown and total fee (e.g., "$10,000 total: 40% upfront, 30% at midpoint, 30% on delivery")
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

### Step 2 — Walk Each Phase
Present each phase of the checklist from `operations/client-onboarding.md` in order. Cover all phases:

- **Pre-Kickoff** (must complete within 48 hours of signed agreement)
- **Kickoff Meeting** — see Step 3 for items to add beyond the standard checklist
- **Post-Kickoff** (within first week)
- **Ongoing Throughout Engagement** — these are weekly recurring actions for the life of the engagement, not a one-time checklist. Present them as a cadence to set up, not items to check off once.
- **Closeout**

For each phase, present the items as a scannable checklist. Ask the user to confirm which are done and which are outstanding. Flag any time-sensitive items based on the signed date.

### Step 3 — Kickoff Meeting Additions
In addition to the standard kickoff checklist items, confirm the following are covered during the kickoff meeting:

**Scope change process:**
Explicitly communicate to the client: all scope changes must be documented in writing and approved before work begins. No verbal change orders. This protects both parties and must be stated clearly at kickoff — not enforced for the first time when a dispute arises.

**Deliverable approval process:**
Walk the client through how approvals work. Per the SOW:
- Deliverables are submitted for review with a clear acceptance window (typically 5–7 business days — confirm the specific timeframe in the SOW)
- If no feedback is received within that window, the deliverable is deemed accepted
- Feedback must be consolidated — one round of revisions per deliverable unless additional rounds are scoped

Make sure the client understands and agrees to this process at kickoff. It prevents scope creep and protects you at closeout.

### Step 4 — Invoice Reminder Schedule
Using the SOW payment schedule provided, calculate each invoice milestone and output a calendar reminder schedule:

- Calculate the exact dollar amount for each milestone
- Assign a target invoice date for each (based on signed date, project timeline, or milestone delivery)
- Note: if a milestone invoice goes unpaid past Net 15, work pauses until payment is received per the consulting agreement — remind the user to follow up the next business day after the due date if unpaid

Output as a table the user can use to set calendar reminders.

### Step 5 — Late Payment Protocol
Surface the late payment process so it's understood before it's needed:

- Invoice due date: Net 15 from invoice date (unless otherwise agreed in the SOW)
- Day 16: Follow up with a polite but direct email if unpaid
- Day 21+: Work pauses. Notify the client in writing that work is on hold pending payment per the consulting agreement
- Day 30+: Late payment interest begins accruing at 1.5% per month per the contract
- Do not absorb late payments silently — the contract gives you the right to pause and charge interest. Use it.

### Step 6 — Summarize Outstanding Actions
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

**[Phase Name]**
- [x] Completed item
- [ ] Outstanding item — [note or deadline]

*(Repeat for all five phases — mark Ongoing items as weekly recurring, not one-time)*

---

**Kickoff Agenda Additions**
- [ ] Scope change process communicated — client understands all changes require written approval before work begins
- [ ] Deliverable approval process communicated — client understands the acceptance window and deemed acceptance clause

---

**Invoice Reminder Schedule**
| Milestone | Amount | Target Invoice Date | Follow-Up If Unpaid |
|-----------|--------|---------------------|---------------------|
| Upfront deposit | $[X] | [DATE] | N/A — collect before kickoff |
| Midpoint | $[X] | [DATE] | [DATE + 16 days] |
| Final delivery | $[X] | [DATE] | [DATE + 16 days] |

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
- Contractor W-9 and payment terms are flagged if a contractor is involved — do not skip
- Ongoing phase items are presented as a weekly recurring cadence, not a one-time checklist
- Scope change and deliverable approval processes are explicitly in the kickoff additions
- Invoice schedule math matches the SOW total and payment percentages exactly
- Late payment protocol is always included in the invoice section — not optional
- Design Partner closeout includes case study initiation and referral conversation
- No phase is skipped — all five phases are presented even if the user is starting mid-engagement
