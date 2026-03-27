---
description: Generate a consulting contract for a new client. Use when the user asks to create, draft, or generate a contract, consulting agreement, services agreement, or design partner agreement.
---

# Generate Contract

## Context
Before executing, read the following files directly from the **knowledge-base** directory (it is mounted and accessible — use the Read tool):
- `legal/templates/consulting-agreement.md` — standard Consulting Services Agreement (MSA)
- `legal/templates/design-partner-agreement.md` — Design Partner Agreement for early/discounted clients
- `legal/templates/sow.md` — SOW template (needed if user proceeds to SOW generation)
- `legal/defaults.md` — standard contractual terms (termination notice, cure period, confidentiality survival, non-solicitation, data return, force majeure thresholds)
- `company/entity.md` — Sprintt's entity details, address, and signatory
- `services/pricing.md` — pricing rules and rate floor (needed for discount validation and SOW fees)
- `services/offerings.md` — service descriptions (needed if user proceeds to SOW generation)

These files are the source of truth. Do not invent or assume any entity details. All `[PLACEHOLDER]` values referencing durations, notice periods, or survival windows must be sourced from `legal/defaults.md`.

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
3. For Design Partner Agreement: validate that the discount percentage does not push the effective hourly rate below the minimum rate floor defined in `services/pricing.md`. Apply the discount to the standard hourly rate from `services/pricing.md` and confirm the result meets or exceeds that floor. If the entered discount would breach it, flag this and ask the user to confirm or adjust before proceeding.
4. Fill in every `[BRACKETED]` field using the collected inputs and entity details from the KB
5. For the Design Partner Agreement, fill in the `[XX]%` discount placeholder with the confirmed percentage
6. For the NDA reference in the Design Partner Agreement (Section 5.1): if an NDA date was provided, insert it; if no NDA exists, replace the sentence with: "No separate NDA has been executed; the confidentiality provisions of this Section shall govern."
7. Output the complete, filled-in contract

## Output
Produce the full contract as clean, formatted markdown — all brackets replaced, ready to copy into a Google Doc or paste into an e-signature tool.

After the contract, ask:

---
"The contract references a Statement of Work (SOW) as Exhibit A — both need to be ready before you send anything for signature. Do you want to generate the SOW now?

- **Yes** — I'll continue here using the client details I already have
- **No** — You can run `/sprintt:generate-sow` separately when ready"

---

If the user says **yes**, proceed directly into SOW generation using all client details already collected (name, short name, address, contact, email, effective date, contract type and date). Follow the full process from the `generate-sow` skill — collect scope, timeline, and commercial inputs, then output the complete SOW. Label it as Exhibit A.

If the user says **no**, end with: "Ready when you are. Run `/sprintt:generate-sow` to generate the SOW separately before sending."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Consultant/Party A entity name matches exactly what is in `company/entity.md` — never abbreviate
- Signatory, governing law, and jurisdiction match `company/entity.md` exactly
- All duration and notice period placeholders sourced from `legal/defaults.md` — not hardcoded
- For Design Partner Agreement: discount percentage is filled in, effective rate is at or above the minimum floor from `services/pricing.md`, and SOW exhibit reference is noted
- Effective Date matches what the user confirmed
- User is always prompted about the SOW before the skill ends
