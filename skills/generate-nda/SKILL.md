---
description: Generate a mutual NDA for a new prospect or client. Use when the user asks to create, draft, or generate an NDA or non-disclosure agreement.
---

# Generate NDA

## Context
Before executing, read the `reference.md` file in this skill folder. It contains the NDA template and Sprintt's entity details.

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
1. Confirm all 7 inputs are collected
2. Fill in every `[BRACKETED]` field in the NDA template from `reference.md` using the collected inputs
3. Use today's date for the Effective Date
4. Output the complete, filled-in NDA

## Output
Produce the full NDA as clean, formatted markdown — all brackets replaced, ready to copy into a Google Doc or paste into an e-signature tool (DocuSign, HelloSign, etc.).

End with a one-line note: "Ready to send. Copy into a Google Doc, convert to PDF, and send for e-signature."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Party A is always "Ramirez Digital Ventures LLC d/b/a Sprintt" — never just "Sprintt"
- Signatory is always "Ricardo Ramirez, AR"
- Governing law is State of Florida, Walton County
- Effective Date matches what the user confirmed
