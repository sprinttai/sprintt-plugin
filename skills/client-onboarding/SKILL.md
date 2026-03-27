---
description: Walk through the full client onboarding lifecycle — pre-kickoff through closeout — with contractor steps, invoice reminders, and phase-by-phase checklists. Use when a new client has signed or at any point during an active engagement.
---

# Client Onboarding

## Context
Before executing, locate the knowledge-base by running `find /sessions -maxdepth 4 -name "knowledge-base" -type d 2>/dev/null | head -1`, then read the following files from that path:
- `operations/client-onboarding.md` — the full onboarding checklist by phase
- `operations/workflows.md` — the lead-to-client pipeline and delivery standards
- `company/entity.md` — Sprintt's legal name and contact info for any client-facing documents
- `legal/defaults.md` — standard contractual terms (deliverable acceptance window, revision rounds)
- `services/pricing.md` — payment structure rules, retainer terms, expense reimbursement policy, and out-of-scope billing rates

Read all five files before proceeding. Pull all rates, thresholds, and payment terms directly from `services/pricing.md`. Pull the deliverable acceptance window and revision round defaults from `legal/defaults.md` — do not hardcode or assume any numbers.

## Inputs
Collect the following — ask conversationally, one at a time if not provided upfront:

1. **Client name** — the company or individual being onboarded
2. **Project name** — the engagement name or SOW title
3. **Engagement type** — Design Partner, Standard Client, or Retainer (Advisor / Builder / Partner tier)
4. **Signed date** — when was the agreement fully executed?
5. **SOW payment schedule** — the milestone breakdown and total fee (e.g., "$10,000 total: 40% upfront, 30% at midpoint, 30% on delivery"). For retainers: monthly rate and tier.
6. **Contractor involved?** — is an SDLC contractor on this engagement? (yes/no — if yes, ask for their name/role and agreed hourly rate)
7. **Current phase** — starting from scratch (pre-kickoff) or mid-engagement? If mid-engagement, which phase are you currently in?

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process

Work through this skill conversationally and section by section. Present one section, get confirmation or input from the user, then move to the next. Do not output everything at once.

### Step 1 — Contractor Setup (if applicable)
If a contractor is involved, address these before any other onboarding steps. Present as a checklist and ask the user to confirm each:

**Agreements & compliance:**
- Has Sprintt's NDA been executed with the contractor? (separate from the client NDA)
- Has the contractor provided their W-9? (required to file a 1099-NEC if they earn $600+ this year — collect it now, before work begins)
- Has the contractor's rate and payment terms been agreed and documented? (when do you pay them — per milestone, net 30, upon client payment? — get this in writing)

**Alignment:**
- Has the contractor reviewed the SOW and confirmed their availability for the full timeline?
- Does the contractor know what's in scope and out of scope?
- Does the contractor understand that all client communication goes through Ricardo — they do not contact the client directly?
- Are system access invitations for the contractor queued (to be sent after client grants access)?

Flag any outstanding items before proceeding. Ask the user to confirm they are ready to move on before continuing to Step 2.

### Step 2 — Capture All Client Contacts
Before kickoff, confirm three distinct contacts on the client side. Ask the user for each:

- **Primary POC** — day-to-day communication (name, email, phone)
- **Billing contact** — who approves and processes invoices (often a different person, especially at companies). If same as POC, confirm explicitly.
- **Escalation contact** — who to go to if the primary POC is unresponsive and something is blocking delivery

Explain: missing the billing contact is the most common reason invoices get delayed. Once captured, confirm with the user before moving on.

### Step 3 — Walk Each Phase
Present each phase of the checklist from `operations/client-onboarding.md` one at a time. After presenting each phase, ask the user which items are done and which are outstanding before moving to the next phase.

Cover all five phases in order. Apply phase-aware filtering:
- If the user is starting fresh (pre-kickoff), present all phases and surface time-sensitive deadlines based on the signed date
- If the user is mid-engagement, skip phases already completed and start from the current phase — do not surface pre-kickoff reminders if kickoff has already happened
- Mark Ongoing items explicitly as a weekly recurring cadence to set up, not a one-time checklist

Phases to cover:
1. **Pre-Kickoff** (must complete within 48 hours of signed agreement)
2. **Kickoff Meeting** — include the additions from Step 4
3. **Post-Kickoff** (within first week) — include the access list from Step 5
4. **Ongoing Throughout Engagement** — weekly recurring, not one-time
5. **Closeout**

### Step 4 — Kickoff Meeting Additions
When presenting the Kickoff Meeting phase, add these items to the standard checklist. Pull all rates and thresholds from `services/pricing.md` — do not state specific numbers from memory:

**Scope change process:**
Explicitly communicate to the client: all scope changes must be documented in writing and approved before work begins. No verbal change orders. Out-of-scope work is billed at the standard hourly rate (read from `services/pricing.md`) — the client needs to hear this number at kickoff, not when they see it on an invoice.

**Deliverable approval process:**
Walk the client through how approvals work. Per the SOW:
- Deliverables are submitted for review with a clear acceptance window (default is [REVIEW_ACCEPTANCE_WINDOW_DAYS] per `legal/defaults.md` — confirm against the actual SOW if already executed)
- If no feedback is received within that window, the deliverable is deemed accepted
- Feedback must be consolidated — default is [REVISION_ROUNDS] rounds of revisions per deliverable per `legal/defaults.md`, unless additional rounds were scoped

**Expense reimbursement:**
Remind the client that out-of-pocket costs incurred on their behalf — API credits, third-party tool licenses, travel — are passed through at cost. The approval threshold for individual expenses (read from `services/pricing.md`) requires prior written approval. Establishing this verbally at kickoff prevents surprise invoice line items later.

**Retainer-specific (if applicable):**
If this is a retainer engagement, walk the client through the retainer terms as documented in `services/pricing.md`: billing cadence, rollover policy, overage rate, and pause policy.

### Step 5 — Document Access Requirements
When presenting the Post-Kickoff phase, produce an explicit access requirements list — not just a general conversation. For each system, dataset, or tool Ricardo needs:
- What is it?
- Who on the client side is responsible for granting access?
- What is the expected turnaround?

This list becomes the checklist for "All access credentials received" in post-kickoff. Without it, that item has no definition.

### Step 6 — Invoice Reminder Schedule
After completing the phase walkthrough, produce a calendar reminder schedule based on the payment terms from `services/pricing.md` and the SOW schedule provided.

**For project engagements:**
- Calculate the exact dollar amount for each milestone from the SOW
- Assign a target invoice date for each milestone
- Apply payment terms from `services/pricing.md` (Net 15 unless otherwise specified in the SOW)
- Calculate the follow-up date for each invoice if unpaid

**For retainer engagements:**
- First invoice is due before the engagement begins (billed in advance)
- Set a recurring monthly invoice reminder on the same day each month
- Include an end-of-month overage check reminder

### Step 7 — Late Payment Protocol
After the invoice schedule, surface the late payment process so it's understood before it's needed. Pull all thresholds, terms, and interest rates from `services/pricing.md` and the applicable agreement — do not hardcode or state specific figures from memory:

- **Day 1 through Net term (from pricing.md):** Payment window — no action needed
- **Day [Net term + 1]:** Follow up with a polite but direct email if unpaid
- **Day [suspension threshold from pricing.md]:** Work pauses. Notify the client in writing that work is on hold pending payment per the signed agreement. Read the exact suspension threshold from `services/pricing.md` — do not assume a number.
- **Ongoing while unpaid:** Late payment interest accrues per the rate in `services/pricing.md`. Read the rate — do not state it from memory.
- Do not absorb late payments silently — the contract gives Ricardo the right to pause and charge interest. Use it.

### Step 8 — Summarize Outstanding Actions
After all sections, output a consolidated prioritized list of everything still outstanding across all phases and setup steps, ordered by urgency.

## Output

Work through each section interactively. Final output after all sections:

---

**Onboarding Tracker: [CLIENT NAME] — [PROJECT NAME]**
- Engagement type: [TYPE]
- Signed: [DATE]
- Contractor: [YES — [NAME/ROLE] / NO]
- Current phase: [PHASE]

---

**Contractor Setup** *(if applicable)*
- [x] / [ ] NDA executed with contractor
- [x] / [ ] W-9 collected from contractor
- [x] / [ ] Payment terms agreed and documented — [terms]
- [x] / [ ] Contractor confirmed availability for full timeline
- [x] / [ ] Rate agreed: $[RATE]/hr
- [x] / [ ] Scope briefing complete
- [x] / [ ] System access invitations queued

---

**Client Contacts**
- Primary POC: [NAME] — [EMAIL] — [PHONE]
- Billing contact: [NAME] — [EMAIL]
- Escalation contact: [NAME] — [EMAIL]

---

**Phase Checklists**
*(Each phase presented and confirmed individually — final status shown here)*

[Phase 1 through 5 with confirmed status per item]

---

**Access Requirements**
| System / Tool | Owner on Client Side | Expected Turnaround | Received? |
|---------------|---------------------|---------------------|-----------|
| [SYSTEM] | [NAME] | [DATE] | [ ] |

---

**Invoice Reminder Schedule**
| Milestone | Amount | Invoice Date | Follow-Up If Unpaid |
|-----------|--------|--------------|---------------------|
| [MILESTONE] | $[X] | [DATE] | [DATE] |

Late payment protocol: [pulled from services/pricing.md and consulting agreement]

---

**Your Next Actions (in order):**
1. [Most urgent outstanding item]
2. [Next item]
3. ...

---

**Standing Reminders** *(shown only for pre-kickoff and kickoff phases)*
- First payment must be confirmed in Mercury before kickoff
- Kickoff meeting must be scheduled within 1 week of signing
- Add client to revenue tracking in `company/finances.md`
- Save signed agreement AND SOW to Google Drive: `Clients/[ClientName]/[ProjectName]`
- Professional liability (E&O) insurance: not yet in place — low risk now, revisit as engagements grow
- Weekly status updates are a recurring commitment — set a recurring calendar reminder

## Quality Checks
- All rates, thresholds, and payment terms read from `services/pricing.md` — none hardcoded
- All three client contacts captured (primary POC, billing, escalation)
- Contractor W-9 and payment terms flagged if a contractor is involved — do not skip
- Skill worked conversationally — sections presented one at a time, user confirmed before proceeding
- Standing reminders suppressed if current phase is post-kickoff or later
- Ongoing phase items presented as weekly recurring cadence, not one-time checklist
- Access requirements documented as a named list, not a general conversation
- Invoice schedule math matches SOW total and payment percentages exactly
- Late payment protocol always included and sourced from KB — not stated from memory
- Design Partner closeout includes case study initiation and referral conversation
- No phase skipped — all five phases presented even if starting mid-engagement
