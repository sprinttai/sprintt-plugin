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
6. **Contractor involved?** — is an SDLC contractor on this engagement? (yes/no)
7. **Current phase** — starting from scratch (pre-kickoff) or mid-engagement? If mid-engagement, which steps are already complete?

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process

### Step 1 — Contractor Setup (if applicable)
If a contractor is involved, address these before any other onboarding steps:
- Has Sprintt's NDA been executed with the contractor? (separate from the client NDA)
- Has the contractor reviewed the SOW and confirmed their availability for the full timeline?
- Has the contractor's rate been agreed and documented?
- Does the contractor know what's in scope and out of scope — and that all client communication goes through Ricardo?
- Are system access invitations for the contractor queued (to be sent after client grants access)?

Flag any of these that are outstanding before proceeding. The contractor must be aligned before kickoff.

### Step 2 — Walk Each Phase
Present each phase of the checklist from `operations/client-onboarding.md` in order. Cover all phases:

- **Pre-Kickoff** (must complete within 48 hours of signed agreement)
- **Kickoff Meeting**
- **Post-Kickoff** (within first week)
- **Ongoing Throughout Engagement**
- **Closeout**

For each phase, present the items as a scannable checklist. Ask the user to confirm which are done and which are outstanding. Flag any time-sensitive items based on the signed date.

### Step 3 — Invoice Reminder Schedule
Using the SOW payment schedule provided, calculate each invoice milestone and output a calendar reminder schedule:

- Calculate the exact dollar amount for each milestone
- Assign a target invoice date for each (based on signed date, project timeline, or milestone delivery)
- Output as a list the user can use to set calendar reminders

### Step 4 — Summarize Outstanding Actions
After all phases, output a prioritized list of everything still outstanding, ordered by urgency.

## Output

**Onboarding Tracker: [CLIENT NAME] — [PROJECT NAME]**
- Engagement type: [TYPE]
- Signed: [DATE]
- Contractor: [YES — [NAME/ROLE] / NO]

---

**Contractor Setup** *(if applicable)*
- [ ] NDA executed with contractor
- [ ] Contractor confirmed availability for full timeline
- [ ] Rate agreed and documented
- [ ] Scope briefing complete — contractor knows what's in/out and that all client comms go through Ricardo
- [ ] System access invitations queued

---

**[Phase Name]**
- [x] Completed item
- [ ] Outstanding item — [note or deadline]

*(Repeat for each phase)*

---

**Invoice Reminder Schedule**
| Milestone | Amount | Target Invoice Date | Set Reminder For |
|-----------|--------|--------------------|--------------------|
| Upfront deposit | $[X] | [DATE] | Day of signing |
| Midpoint | $[X] | [DATE] | [X days before milestone] |
| Final delivery | $[X] | [DATE] | [X days before delivery] |

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
- Google Drive folder: `Clients/[ClientName]/[ProjectName]` — save SOW here
- Professional liability (E&O) insurance: not yet in place — low risk now, revisit as engagements grow
- Weekly status updates to client are required even when nothing major happened

## Quality Checks
- Contractor setup is checked before any other phase if a contractor is on the engagement
- Pre-kickoff items (payment, communication channel) are confirmed before kickoff proceeds
- Kickoff deadline is flagged if more than 3 days have passed since signing
- Invoice schedule math matches the SOW total and payment percentages exactly
- Design Partner closeout includes case study initiation and referral conversation
- No phase is skipped — all five phases are presented even if the user is starting mid-engagement
