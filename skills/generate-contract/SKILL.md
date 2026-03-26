---
description: Generate a consulting contract for a new client. Use when the user asks to create, draft, or generate a contract, consulting agreement, services agreement, or design partner agreement.
---

# Generate Contract

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `legal/templates/consulting-agreement.md` — standard Consulting Services Agreement (MSA)
- `legal/templates/design-partner-agreement.md` — Design Partner Agreement for early/discounted clients
- `company/entity.md` — Sprintt's entity details, address, and signatory

These files are the source of truth. Do not invent or assume any entity details.

## Inputs
First, ask the user which contract type they need if not specified via $ARGUMENTS:

1. **Standard Consulting Services Agreement** — for paying clients at standard rates
2. **Design Partner Agreement** — for early clients receiving discounted rates in exchange for feedback, testimonials, and referrals

Then collect the following (ask all at once):

**For both contract types:**
1. Client's full legal name (e.g., "Acme Corp LLC")
2. Client's short name (e.g., "Acme")
3. Client's business address
4. Client's point of contact name and title
5. Client's email address
6. Effective date (or confirm today's date)
7. Whether a signed NDA already exists, and if so, the NDA date

**Additional inputs for Design Partner Agreement only:**
8. Discount percentage off standard rates (e.g., "40%")

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Confirm contract type and all required inputs are collected
3. Fill in every `[BRACKETED]` field using the collected inputs and entity details from the KB
4. For the Design Partner Agreement, fill in the `[XX]%` discount placeholder with the confirmed percentage
5. For the NDA reference in the Design Partner Agreement (Section 5.1): if an NDA date was provided, insert it; if no NDA exists, replace the sentence with: "No separate NDA has been executed; the confidentiality provisions of this Section shall govern."
6. Output the complete, filled-in contract

## Output
Produce the full contract as clean, formatted markdown — all brackets replaced, ready to copy into a Google Doc or paste into an e-signature tool.

End with a one-line note: "Ready to send. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Consultant/Party A entity name matches exactly what is in `company/entity.md` — never abbreviate
- Signatory, governing law, and jurisdiction match `company/entity.md` exactly
- For Design Partner Agreement: discount percentage is filled in and the SOW exhibit reference is noted
- Effective Date matches what the user confirmed
