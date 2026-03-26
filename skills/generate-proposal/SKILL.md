---
description: Generate a client proposal for a consulting engagement. Use when the user asks to create, draft, or generate a proposal, quote, or engagement overview for a prospect or client.
---

# Generate Proposal

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `legal/templates/proposal.md` — the proposal template
- `services/offerings.md` — service descriptions and delivery model
- `services/pricing.md` — pricing ranges, payment structures, and rate rules
- `services/ideal-client.md` — ICP profiles to assess prospect fit
- `company/overview.md` — Sprintt's mission, differentiators, and proof points
- `company/entity.md` — Calendly booking link and contact details
- `brand/guidelines.md` — voice and tone guidance for client-facing copy

These files are the source of truth. Every proposal must sound like Sprintt — confident, direct, and specific to what the prospect actually said.

## Inputs
Collect the following (ask in two rounds — prospect context first, then engagement details):

**Prospect context:**
1. Client company name and contact name
2. How did they find Sprintt? (referral, LinkedIn, website, etc.)
3. What problem or goal did they describe? (use their words where possible)
4. Company size and industry (to assess ICP fit)
5. Are they a Design Partner candidate? (yes / no / unsure)
6. Today's date (for proposal date and 30-day validity window)

**Engagement details:**
7. Service type — which offering best fits their need? (refer to `services/offerings.md`)
8. Key deliverables — what will the client have at the end?
9. What's explicitly out of scope?
10. Estimated timeline (phases and duration)
11. Will contractors be involved? If yes, get hours and rate to calculate price floor per `services/pricing.md`
12. Proposed fee — confirm against ranges in `services/pricing.md` before proceeding
13. Any relevant client case studies or outcomes to highlight for this specific client (optional — if none, skill will use proof points from `company/overview.md`)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read all KB files listed in Context above
2. Assess ICP fit using `services/ideal-client.md` — flag if the prospect matches an anti-pattern before proceeding
3. Collect inputs in two rounds as described above
4. For pricing: validate the proposed fee against `services/pricing.md` ranges. If contractors are involved, calculate the price floor first. Flag if the fee falls outside the expected range.
5. Determine the correct payment schedule based on total fee per `services/pricing.md` rules
6. Write the proposal using the template from `legal/templates/proposal.md`, applying Sprintt's voice and tone from `brand/guidelines.md`:
   - Be specific and concrete — use the client's language from discovery
   - Lead with their goal, not Sprintt's capabilities
   - For the "Why Sprintt" proof point: if the user has a relevant client case study or outcome to share, use it. If not — which is expected early on — use the most relevant metric from `company/overview.md` (e.g., "Discovery cycles: 3 months → 1 week", "Bug-fix effort: 70% reduction", "Technical docs: 90% faster") matched to what matters most to this specific client. Never leave this placeholder blank or fabricate a client story.
   - If contractor is involved, include the contractor delivery note in "How This Works"
   - If Design Partner: note the discount and reference the Design Partner Agreement
7. Output the complete, filled-in proposal

## Output
Produce the full proposal as clean, formatted markdown — all brackets replaced, ready to copy into the Google Docs branded template and send as a PDF.

After the proposal, ask:

---
"Ready to move forward? If the client accepts, you'll need a contract and SOW before work starts. Want me to generate the contract now?

- **Yes** — I'll continue using the client details I already have
- **No** — Run `/sprintt:generate-contract` when ready"

---

If the user says **yes**, proceed directly into contract generation using all client details already collected. Follow the full process from the `generate-contract` skill — confirm contract type, then generate the contract and offer to continue into SOW generation inline.

If the user says **no**, end with: "Run `/sprintt:generate-contract` when the client is ready to proceed."

## Quality Checks
- Every `[BRACKETED]` field is filled in — none left blank
- Proposal uses client's own language in "The Opportunity" section — not generic
- Fee is consistent with `services/pricing.md` ranges — flagged if outside
- Payment schedule matches the correct tier from `services/pricing.md`
- Out-of-scope section includes at least one explicit exclusion
- Proof points from `company/overview.md` are included in "Why Sprintt"
- Voice matches `brand/guidelines.md` — confident, direct, no hedging language
- Proposal validity date is 30 days from today
- Calendly link in Next Steps is pulled from `company/entity.md` — never hardcoded
- Entity footer reads: "Ramirez Digital Ventures LLC d/b/a Sprintt · ricardo@sprintt.ai · sprintt.ai"
