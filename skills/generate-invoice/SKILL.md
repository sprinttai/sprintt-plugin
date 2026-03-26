---
description: Generate a professional invoice for a client. Use when the user asks to create, draft, or generate an invoice or bill.
---

# Generate Invoice

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `company/entity.md` — Sprintt's legal name, address, EIN, and signatory
- `company/finances.md` — banking details, payment methods, and default payment terms

These files are the source of truth for all Sprintt-side invoice details. Do not invent or assume banking or entity information.

## Inputs
Collect the following (ask all at once):

1. Invoice number — suggest the next sequential number if the user doesn't specify (format: INV-YYYY-###, e.g., INV-2026-001)
2. Invoice date (default to today's date — confirm with user)
3. Client's full legal name
4. Client's billing address
5. Client's point of contact name and email
6. Associated project or SOW name/number (for reference line)
7. Line items — for each:
   - Description of service
   - Quantity or hours (if hourly)
   - Rate (if hourly) or flat amount
   - Line total
8. Any previously paid deposits or retainer credits to apply
9. Payment due date (default: Net 15 from invoice date — confirm if different)
10. Any notes to include (e.g., "Per SOW-2026-001", "Final payment upon delivery")

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Confirm all inputs are collected
3. Calculate subtotal, apply any credits/deposits, and calculate the amount due
4. Pull payment instructions from `company/finances.md` (bank name, payment methods accepted, account details if present)
5. Output the complete invoice

## Output
Produce the invoice as clean, formatted markdown using this structure:

```
# INVOICE

**Invoice #:** INV-YYYY-###
**Date:** [DATE]
**Due Date:** [DATE] (Net 15)

---

**From:**
Ramirez Digital Ventures LLC d/b/a Sprintt
[Address from entity.md]
[Email from entity.md]
EIN: [EIN from entity.md]

**To:**
[CLIENT LEGAL NAME]
[CLIENT ADDRESS]
Attn: [CLIENT CONTACT NAME]
[CLIENT EMAIL]

**Re:** [PROJECT/SOW REFERENCE]

---

## Services

| Description | Qty/Hrs | Rate | Amount |
|-------------|---------|------|--------|
| [line items] |

**Subtotal:** $X,XXX.00
**Less Deposit Paid:** ($X,XXX.00)  ← only if applicable
**Amount Due:** $X,XXX.00

---

## Payment Instructions

[Payment details from finances.md]

**Payment Due:** [DATE]

[Any notes]
```

End with: "Invoice ready. Send to [CLIENT EMAIL] and log in Mercury."

## Quality Checks
- Invoice number follows INV-YYYY-### format
- All entity details (name, address, EIN) match `company/entity.md` exactly
- Payment terms match `company/finances.md` (Net 15 unless otherwise agreed)
- Amount Due correctly reflects subtotal minus any deposits
- Payment instructions are pulled from `company/finances.md` — never invented
