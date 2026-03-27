---
description: Generate an NDA for a new prospect or client — mutual or one-way. Use when the user asks to create, draft, or generate an NDA or non-disclosure agreement.
---

# Generate NDA

## Context
Before executing, locate the knowledge-base by running `find /sessions -maxdepth 4 -name "knowledge-base" -type d 2>/dev/null | head -1`, then read the following files from that path:
- `legal/templates/nda.md` — the NDA template (mutual by default)
- `legal/defaults.md` — standard contractual terms (NDA term, survival period, termination notice, return/destroy window)
- `company/entity.md` — Sprintt's entity details, address, and signatory

These files are the source of truth. Do not invent or assume any entity details. All `[PLACEHOLDER]` values in the NDA template that reference durations or notice periods must be sourced from `legal/defaults.md`.

## Inputs
Ask the user for the following if not already provided (you can ask all at once):

1. NDA type — **mutual** (both parties share confidential information) or **one-way** (only one party discloses)
   - If one-way: which direction? (a) client discloses to Sprintt, or (b) Sprintt discloses to client
2. Client's full legal name (e.g., "Acme Corp LLC")
3. Client's short name / what to call them in the document (e.g., "Acme")
4. Client's business address
5. Client's point of contact name and title
6. Client's email address
7. Brief description of the purpose (e.g., "AI consulting and workflow automation services")
8. Today's date (or confirm today's date with the user)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Confirm all inputs are collected
3. Fill in every `[BRACKETED]` field using the collected inputs and entity details from the KB
4. Use today's date for the Effective Date
5. If **mutual**: use the template as-is
6. If **one-way**: adapt the template as follows:
   - Change title to "NON-DISCLOSURE AGREEMENT"
   - Identify the Disclosing Party and Receiving Party based on the direction specified
   - Section 1: Replace "each Party may disclose certain confidential and proprietary information to the other Party" with "the Disclosing Party will disclose certain confidential and proprietary information to the Receiving Party"
   - Section 4 Obligations: Change "Each Party agrees to" to "The Receiving Party agrees to" and remove any language implying mutual obligations
   - All other sections remain the same
7. Output the complete, filled-in NDA

## Output
Produce the full NDA as clean, formatted markdown — all brackets replaced, ready to copy into a Google Doc or paste into an e-signature tool (DocuSign, HelloSign, etc.).

End with a one-line note: "Ready to send. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Party A entity name matches exactly what is in `company/entity.md` — never abbreviate
- Signatory, governing law, and jurisdiction match `company/entity.md` exactly
- Effective Date matches what the user confirmed
- All duration and notice period placeholders sourced from `legal/defaults.md` — not hardcoded
- For one-way NDAs: title says "NON-DISCLOSURE AGREEMENT" (not "MUTUAL"), and obligations apply only to the Receiving Party
