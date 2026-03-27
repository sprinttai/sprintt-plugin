---
description: Walk through the client onboarding checklist for a new engagement — pre-kickoff, kickoff, and post-kickoff steps with clear next actions. Use when a new client has signed and you need to make sure nothing gets missed.
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
5. **Current phase** — are you starting from scratch (pre-kickoff) or mid-onboarding? If mid-onboarding, which steps are already done?

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Determine the current phase based on the signed date and user input
3. Walk through each phase of the checklist in order:
   - **Pre-Kickoff** (must complete within 48 hours of signed agreement)
   - **Kickoff Meeting**
   - **Post-Kickoff** (within first week)
4. For each phase, present the checklist items as a scannable list
5. Ask the user to confirm which items are done and which are outstanding
6. Flag any items that are time-sensitive based on the signed date (e.g., kickoff must be within 1 week)
7. Summarize outstanding items as a prioritized action list

## Output

**Onboarding Status: [CLIENT NAME] — [PROJECT NAME]**
- Engagement type: [TYPE]
- Signed: [DATE]
- Current phase: [PHASE]

**[Phase Name]**
- [x] Completed item
- [ ] Outstanding item — [any relevant note or deadline]

(Repeat for each phase)

**Your Next Actions (in order):**
1. [Most urgent outstanding item]
2. [Next item]
3. ...

**Reminders**
- Kickoff meeting must be scheduled within 1 week of signed agreement
- First payment must be confirmed in Mercury before kickoff
- Add client to revenue tracking in `company/finances.md`
- Internal Google Drive folder: `Clients/[ClientName]/[ProjectName]`

## Quality Checks
- Pre-kickoff items are checked first — payment and communication setup must be confirmed before kickoff
- Kickoff deadline is surfaced if more than 3 days have passed since signing
- Design Partner clients get closeout reminders for case study and referral conversation
- No steps are skipped or assumed complete without user confirmation
