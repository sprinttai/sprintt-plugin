---
description: Guide the user through billing a client in Mercury based on their SOW and pricing rules. Use when the user asks how to invoice a client, what to bill, or how to create an invoice in Mercury.
---

# Invoicing Guide

## Context
Before executing, locate the knowledge-base by running `find /sessions -maxdepth 4 -name "knowledge-base" -type d 2>/dev/null | head -1`, then read the following files from that path:
- `company/entity.md` — Sprintt's legal name, address, and EIN
- `company/finances.md` — banking details, payment methods, and default payment terms
- `services/pricing.md` — payment structure rules and late payment terms

These files are the source of truth. Do not invent or assume any billing details.

## Inputs
Collect the following:

1. Client name
2. SOW number and total project fee (e.g., SOW-2026-001, $10,000)
3. Payment schedule from the SOW (e.g., "40% upfront, 30% at midpoint, 30% on delivery")
4. Which milestone is being billed (e.g., "upfront deposit", "midpoint", "final delivery")
5. Is this the first invoice to this client? (yes/no)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read the KB files listed in Context above
2. Calculate the exact amount due for the current milestone based on the payment schedule and total fee
3. Determine the due date using the payment terms from `services/pricing.md` and `company/finances.md` unless otherwise agreed in the SOW
4. Walk the user through entering the invoice in Mercury step by step
5. Flag any reminders relevant to this invoice

## Output
Produce a clear billing summary followed by Mercury instructions:

**Billing Summary**
- Client: [CLIENT NAME]
- SOW: [SOW NUMBER]
- Milestone: [MILESTONE NAME]
- Amount to bill: $[AMOUNT]
- Due date: [DATE] ([payment terms from services/pricing.md] from today)
- Line item description to use: [DESCRIPTION]

**How to enter in Mercury**
1. Go to mercury.com → **Invoices** → **New Invoice**
2. Set the invoice date to today
3. Set the due date to [DATE]
4. Add recipient: [CLIENT NAME]
5. Line item description: [DESCRIPTION matching the SOW milestone]
6. Amount: $[AMOUNT]
7. In the invoice notes, add: "Payment terms: [payment terms from services/pricing.md]. Invoices unpaid after [term] days accrue interest at [late payment rate from services/pricing.md] per the consulting agreement."
8. Send to: [CLIENT EMAIL]

**Reminders**
- [ ] If this is the first invoice to this client, send them your W-9 alongside it
- [ ] Log the invoice in your revenue tracking in `company/finances.md` once sent
- [ ] If payment isn't received by the due date, follow up the next business day

## Quality Checks
- Amount matches the correct milestone percentage of the SOW total — double-check the math
- Due date uses payment terms from `services/pricing.md` unless SOW specifies otherwise
- Late payment language is included in the Mercury invoice notes — terms and interest rate sourced from `services/pricing.md`
- W-9 reminder is surfaced for first invoices to a new client
