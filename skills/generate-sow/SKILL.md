---
description: Generate a Statement of Work (SOW) for a client engagement. Use when the user asks to create, draft, or generate a SOW, scope of work, or project agreement.
---

# Generate SOW

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `legal/templates/sow.md` — the SOW template with all sections and bracketed fields
- `services/pricing.md` — pricing ranges, payment structure rules, and hourly rates
- `services/offerings.md` — service descriptions to help articulate scope and deliverables accurately
- `company/entity.md` — Sprintt's entity details and signatory

These files are the source of truth. Use `services/pricing.md` to guide payment schedule structure and validate that fees are consistent with Sprintt's standard ranges.

## Inputs
Collect the following (you may ask in groups — project context first, then scope, then commercial terms):

**Project context:**
1. Client's full legal name and short name
2. Associated agreement type and date (Consulting Services Agreement or Design Partner Agreement)
3. SOW number (format: SOW-YYYY-###, e.g., SOW-2026-001) — confirm with user or suggest the next sequential number
4. Project name
5. Background — what is the client's situation and what problem are we solving? (2–3 sentences)
6. Objectives — what does success look like? (specific and measurable where possible)
7. Effective date

**Scope:**
8. In-scope deliverables (list each one)
9. Out-of-scope items (what is explicitly excluded)
10. Assumptions (what needs to be true for the project to succeed)
11. Client feedback turnaround time (how many business days the client has to respond to deliverables)

**Timeline:**
12. Project start date
13. Key milestones and target dates
14. Total estimated duration (weeks)

**Commercial:**
15. Service type (refer to `services/offerings.md` for categories)
16. Is this a Design Partner engagement? If yes, what is the discount percentage?
17. Fee structure — line items with amounts, or ask user to describe the scope and suggest pricing based on `services/pricing.md`
18. Payment schedule (derive from `services/pricing.md` rules based on total project fee)
19. Client point of contact name for Section 5

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Collect all inputs above — you may ask in two rounds (project context + scope first, then commercial terms)
3. For pricing: if the user hasn't specified fees, suggest a range based on service type and complexity using `services/pricing.md`, and ask the user to confirm before proceeding
4. Determine payment schedule using the rules in `services/pricing.md`:
   - Under $5,000: 50% upfront, 50% on delivery
   - $5,000–$15,000: 40% upfront, 30% at midpoint, 30% on delivery
   - Over $15,000: 30% upfront, monthly milestones, 20% on delivery
5. Fill in every `[BRACKETED]` field in the SOW template
6. For the additional work rate in Section 4.3: use $225/hr standard; if Design Partner, ask for the agreed partner hourly rate
7. Output the complete, filled-in SOW

## Output
Produce the full SOW as clean, formatted markdown — all brackets replaced, tables filled in, ready to attach to a contract as Exhibit A or send as a standalone document.

End with a one-line note: "Ready to attach as Exhibit A or send standalone. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- SOW number follows the SOW-YYYY-### format
- Fees are consistent with the ranges in `services/pricing.md` — flag if they fall outside the range
- Payment schedule matches the rules in `services/pricing.md` based on total fee
- Standard hourly rate for additional work is $225/hr (or confirmed Design Partner rate)
- Signatory matches `company/entity.md` exactly
- Out-of-scope section explicitly lists at least one exclusion to prevent scope creep
