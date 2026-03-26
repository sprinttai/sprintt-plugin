---
description: Prepare for a discovery call with a prospect. Use when the user has an upcoming discovery call and wants to prepare questions, assess fit, and have a follow-up email ready.
---

# Discovery Prep

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `operations/discovery-call.md` — call structure, questions, red flags, and follow-up template
- `services/offerings.md` — service descriptions to identify likely fit
- `services/ideal-client.md` — ICP profiles to assess prospect fit and spot anti-patterns

These files are the source of truth. The goal of this skill is to walk into the call prepared — not to sell, but to assess fit and listen well.

## Inputs
Collect the following:

1. Prospect's name and company
2. Company size and industry (if known)
3. How did they find Sprintt? (referral, LinkedIn, website, inbound, etc.)
4. What problem or goal did they mention when they reached out? (even if vague)
5. Date and time of the call (to confirm the follow-up email deadline — within 24 hours)
6. Is there any prior context? (mutual connections, past interactions, their website or LinkedIn)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read all KB files listed in Context above
2. Map the prospect to the most likely ICP from `services/ideal-client.md` based on what's known — note if they match any anti-patterns and flag them clearly
3. Identify the 1–2 most likely service fits from `services/offerings.md` based on their stated problem
4. Pull the call structure from `operations/discovery-call.md` and tailor it to this specific prospect
5. Generate tailored discovery questions based on what's already known — build on the core questions from the KB, don't just repeat them
6. Pre-fill the follow-up email template from `operations/discovery-call.md` with everything already known, leaving placeholders for what will be learned on the call
7. Output the full prep package

## Output
Produce a structured prep package with the following sections:

---

**Prospect:** [NAME] — [COMPANY]
**Call:** [DATE & TIME]
**Follow-up due by:** [24 hours after call]

---

### ICP Assessment
- Most likely ICP: [ICP name from ideal-client.md]
- Budget range to expect: [from ICP profile]
- Decision-maker on the call: [confirmed / unknown — flag if unknown]
- ⚠️ Anti-patterns to watch for: [any flags based on what's known, or "none identified yet"]

### Likely Service Fit
- Primary fit: [service name + 1-sentence reason]
- Secondary fit (if applicable): [service name + 1-sentence reason]

### Tailored Discovery Questions
Questions to ask during "Their World" and "Assess Fit" — in addition to the standard framework:
1. [Tailored question based on their industry/problem]
2. [Tailored question based on their company stage]
3. [Tailored question to surface budget readiness]
4. [Tailored question to identify the real decision-maker]

### Red Flags to Watch For on This Call
[Based on what's already known — pull relevant red flags from discovery-call.md and add any specific to this prospect]

### Pricing Anchors
If they ask about investment on the call, use these ranges (don't commit to specifics):
- [Service fit 1]: "[price range from services/pricing.md]"
- [Service fit 2 if applicable]: "[price range]"

### Follow-Up Email (Pre-filled)
Ready to send within 24 hours of the call — fill in the [BLANKS] after the call:

> Hi [NAME],
>
> Great talking today. Here's a quick recap of what I took away:
>
> **The situation:** [FILL IN AFTER CALL — 1–2 sentences on their problem]
>
> **What I'd propose:** [FILL IN AFTER CALL — 1 sentence on service type / scope]
>
> **Next step:** [FILL IN AFTER CALL — proposal by X date / follow-up call / etc.]
>
> Let me know if I missed anything. Otherwise I'll be in touch by [DATE].
>
> Ricardo

---

End with: "You're ready. Remember: the goal is fit assessment, not selling. Let them talk."

## Quality Checks
- ICP match is explicit — not left as "unclear" if enough info is available
- At least one anti-pattern check is included even if none are flagged
- Tailored questions are specific to this prospect — not generic copies of the KB questions
- Pricing anchors reference actual ranges from `services/pricing.md`
- Follow-up email is pre-filled with everything already known and deadline is set to 24 hours after the call
