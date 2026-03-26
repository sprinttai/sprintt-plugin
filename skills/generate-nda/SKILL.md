---
description: Generate a mutual NDA for a new prospect or client. Use when the user asks to create, draft, or generate an NDA or non-disclosure agreement.
---

# Generate NDA

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `legal/templates/nda.md` — the NDA template
- `company/entity.md` — Sprintt's entity details, address, and signatory

These files are the source of truth. Do not invent or assume any entity details.

## Inputs
Ask the user for the following if not already provided (you can ask all at once):

1. Client's full legal name (e.g., "Acme Corp LLC")
2. Client's short name / what to call them in the document (e.g., "Acme")
3. Client's business address
4. Client's point of contact name and title
5. Client's email address
6. Brief description of the purpose (e.g., "AI consulting and workflow automation services")
7. Today's date (or confirm today's date with the user)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Confirm all 7 inputs are collected
3. Fill in every `[BRACKETED]` field in the NDA template using the collected inputs and entity details from the KB
4. Use today's date for the Effective Date
5. Output the complete, filled-in NDA

## Output
Produce the full NDA as clean, formatted markdown — all brackets replaced, ready to copy into a Google Doc or paste into an e-signature tool (DocuSign, HelloSign, etc.).

End with a one-line note: "Ready to send. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Party A entity name matches exactly what is in `company/entity.md` — never abbreviate
- Signatory, governing law, and jurisdiction match `company/entity.md` exactly
- Effective Date matches what the user confirmed
