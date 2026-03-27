---
description: Generate a Statement of Work (SOW) for a client engagement. Use when the user asks to create, draft, or generate a SOW, scope of work, or project agreement.
---

# Generate SOW

## Context
Before executing, locate the knowledge-base by running `find /sessions -maxdepth 4 -name "knowledge-base" -type d 2>/dev/null | head -1`, then read the following files from that path:
- `legal/templates/sow.md` — the SOW template (covers both project-based and retainer engagements)
- `legal/defaults.md` — standard contractual terms (review acceptance window, revision rounds)
- `services/pricing.md` — pricing ranges, payment structure rules, hourly rates, and retainer tier details
- `services/offerings.md` — service descriptions to help articulate scope and deliverables accurately
- `company/entity.md` — Sprintt's entity details and signatory

These files are the source of truth. Use `services/pricing.md` to guide payment structure and validate that fees are consistent with Sprintt's standard ranges. Use `legal/defaults.md` for acceptance window and revision round defaults.

## Inputs

First, determine engagement type — this controls which sections of the SOW are used:

**Step 0 — Engagement type:**
Ask: "Is this a project-based engagement (fixed scope and deliverables) or a retainer (Advisor, Builder, or Partner tier)?"

Then collect inputs based on the answer.

---

### Project-Based Engagement Inputs

**Project context:**
1. Client's full legal name and short name
2. Associated agreement type and date (Consulting Services Agreement or Design Partner Agreement)
3. SOW number (format: SOW-YYYY-###) — confirm with user or suggest the next sequential number
4. Project name
5. Background — client's situation and problem (2–3 sentences)
6. Objectives — what does success look like? (specific and measurable)
7. Effective date
8. Data and systems access — what client data or systems will Sprintt access? (list each with data type and purpose for Section 1.5)

**Scope:**
9. In-scope deliverables (list each one)
10. Out-of-scope items (what is explicitly excluded)
11. Assumptions (access timeline, feedback window, POC, technical dependencies)
12. Client feedback turnaround time (business days — used in Section 5 and 6.1)
13. Revision rounds per deliverable (default: 2 — confirm with user)
14. Deemed acceptance window (default: 5 business days — confirm with user; explain this clause protects against indefinitely stalled approvals)

**Timeline:**
15. Project start date
16. Key milestones and target dates
17. Total estimated duration (weeks)

**Commercial:**
18. Service type (refer to `services/offerings.md`)
19. Is this a Design Partner engagement? If yes, discount percentage
20. Will SDLC contractors be involved? If yes: contractor hours and rate — use contractor pricing formula from `services/pricing.md` to calculate price floor before quoting
21. Fee structure — line items with amounts, or ask user to describe scope and suggest pricing based on `services/pricing.md`
22. Payment schedule (derive from `services/pricing.md` rules based on total fee — present all three tiers and confirm the correct one)
23. Client point of contact name

---

### Retainer Engagement Inputs

**Retainer context:**
1. Client's full legal name and short name
2. Associated agreement type and date (Consulting Services Agreement or Design Partner Agreement)
3. SOW number (format: SOW-YYYY-###) — confirm with user or suggest the next sequential number
4. Project / engagement name
5. Background — why is the client engaging on a retainer basis? (2–3 sentences)
6. Objectives — what outcomes is the retainer focused on?
7. Effective date
8. Data and systems access — what client data or systems will Sprintt access? (list each for Section 1.5)

**Retainer terms:**
9. Tier selection — Advisor (5 hrs/mo), Builder (15 hrs/mo), or Partner (30 hrs/mo)? Read tier descriptions and rates from `services/pricing.md` before asking
10. Is this a Design Partner engagement? If yes, discount percentage off standard tier rate
11. Start date and initial 3-month commitment end date
12. Focus areas for the engagement (optional — 2–3 priorities to align on)
13. Client point of contact name

---

## Process

### For Project-Based SOWs:
1. Read all KB files listed in Context above
2. Confirm engagement type is project-based
3. Collect project context, scope, timeline, and commercial inputs
4. For contractor engagements: calculate price floor using formula in `services/pricing.md` before suggesting a fee
5. For pricing: if the user hasn't specified fees, suggest a range based on service type and complexity; confirm before proceeding
6. Determine payment schedule using the rules in `services/pricing.md` — present the correct tier based on total fee; confirm with user
7. Confirm revision rounds and deemed acceptance window with user — explain that Section 6.3 (deemed acceptance) means the client's silence after the review window constitutes approval; this is one of the strongest protections against stalled projects
8. Fill in every `[BRACKETED]` field in Sections 1–6 and Section 8 of the SOW template
9. Output the complete SOW

### For Retainer SOWs:
1. Read all KB files listed in Context above
2. Confirm engagement type is retainer
3. Collect retainer context inputs
4. Read retainer tier details from `services/pricing.md` — confirm selected tier, monthly rate, and included deliverables with user before proceeding
5. Calculate month-to-month rate (standard tier rate + 10%) for post-initial-term
6. If Design Partner: calculate discounted monthly rate
7. Confirm focus areas with user — these are optional but recommended
8. Fill in every `[BRACKETED]` field in Sections 1 and 7 and Section 8 of the SOW template. Sections 2–6 are not used for retainers — omit them from the output entirely
9. Output the complete SOW

## Output
Produce the full SOW as clean, formatted markdown — all brackets replaced, tables filled in, ready to attach to a contract as Exhibit A or send as a standalone document.

For **project-based** SOWs: include Sections 1–6 and Section 8. Omit Section 7.
For **retainer** SOWs: include Sections 1 and 7 and Section 8. Omit Sections 2–6.

End with: "Ready to attach as Exhibit A or send standalone. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Engagement type checkbox in Section 1.2 is checked
- SOW number follows the SOW-YYYY-### format
- Section 1.5 data access table is filled in — not left blank
- **Project-based:** Fees consistent with `services/pricing.md` ranges; payment schedule matches correct tier; revision rounds and deemed acceptance window confirmed by user; out-of-scope has at least one explicit exclusion
- **Retainer:** Tier, monthly rate, and included deliverables sourced from `services/pricing.md`; month-to-month rate is standard rate + 10%; initial 3-month commitment end date is correct; Section 7.6 pause policy matches `services/pricing.md`
- Sections not applicable to the engagement type are omitted from output entirely
- Standard hourly rate for additional/overage work sourced from `services/pricing.md` — not hardcoded
- Review acceptance window and revision rounds sourced from `legal/defaults.md` — not hardcoded
- Signatory matches `company/entity.md` exactly (Ricardo Ramirez, AR — Authorized Representative)
