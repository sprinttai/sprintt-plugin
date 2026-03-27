---
description: Prepare for a discovery call with a prospect. Use when the user has an upcoming discovery call and wants to prepare questions, assess fit, and have a follow-up email ready.
---

# Discovery Prep

## Context
Before executing, read the following files directly from the **knowledge-base** directory (it is mounted and accessible — use the Read tool):
- `operations/discovery-call.md` — call structure, questions, red flags, and follow-up template
- `services/offerings.md` — service descriptions to identify likely fit
- `services/ideal-client.md` — ICP profiles to assess prospect fit and spot anti-patterns

These files are the source of truth. The goal of this skill is to walk into the call prepared — not to sell, but to assess fit and listen well.

## Inputs
Collect the following:

1. Prospect's name and company name
2. Company website URL (if known)
3. Prospect's LinkedIn URL (if known)
4. How did they find Sprintt? (referral, LinkedIn, website, inbound, etc.)
5. What problem or goal did they mention when they reached out? (even if vague)
6. Date and time of the call (to confirm the follow-up email deadline — within 24 hours)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read all KB files listed in Context above
2. **Research the prospect** using web search:
   - Visit their website — note what the company does, their size signals, their industry, and anything they're publicly working on or promoting
   - Search for the prospect's LinkedIn profile — note their title, tenure, background, and any recent posts or activity
   - Search for any recent news, funding announcements, or notable company events
   - Note any mutual context (how they found Sprintt, any shared connections)
3. Map the prospect to the most likely ICP from `services/ideal-client.md` using both what the user provided and what research revealed — note if they match any anti-patterns and flag them clearly
4. Identify the 1–2 most likely service fits from `services/offerings.md` based on their stated problem and what research revealed about their situation
5. Pull the call structure from `operations/discovery-call.md` and tailor it to this specific prospect
6. Generate tailored discovery questions based on research findings — build on the core questions from the KB using specific details found during research
7. Pre-fill the follow-up email template from `operations/discovery-call.md` with everything already known, leaving placeholders for what will be learned on the call
8. Output the full prep package

## Output
Produce a structured prep package with the following sections:

---

**Prospect:** [NAME] — [COMPANY]
**Call:** [DATE & TIME]
**Follow-up due by:** [24 hours after call]

---

### Research Summary
What was found before the call — use this to open the conversation with context:
- **What they do:** [1–2 sentences from website]
- **Company size signals:** [headcount, funding stage, or other signals found]
- **Prospect's role:** [title, tenure, background from LinkedIn]
- **Recent activity:** [funding, product launches, news, or LinkedIn posts worth referencing]
- **How they found Sprintt:** [referral / LinkedIn / website / inbound]
- **Anything notable:** [mutual connections, shared context, or anything that helps open warmly]

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

If they push for a specific number before you have enough context:
> *"I don't want to give you a number I'll have to walk back once I understand the details better. Let me put together a proper proposal — you'll have it in [X] days."*

### How to End the Call — Three Scenarios

**If it's a strong fit:**
> *"I'd like to put together a proposal based on what we've discussed. I'll have it to you within 3 business days. Any additional context I should have before I start?"*
Then run `/sprintt:generate-proposal`.

**If you need more information before scoping:**
> *"I want to make sure I scope this correctly. Can we schedule a 30-minute working session with [person with more context / the technical lead / your team]?"*
Then schedule the follow-up and run `/sprintt:discovery-prep` again before that call.

**If they need time to think:**
> *"Totally makes sense. I'll send you a brief recap of what we discussed with some initial thinking. If it resonates, we can go from there."*
Then send the follow-up email below.

### If It's Not a Fit
Don't force it. Say so clearly and helpfully — this protects your time and leaves the relationship intact:
> *"Honestly, I don't think I'm the right fit for this one — [specific reason]. But I'd recommend [alternative resource or type of provider]. Happy to make an intro if that's helpful."*

[If anti-patterns were flagged in research, note the specific reason to use here]

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
- Research summary is populated from actual web search results — never skipped
- ICP match is explicit — not left as "unclear" if enough info is available
- At least one anti-pattern check is included even if none are flagged
- Tailored questions are specific to this prospect — not generic copies of the KB questions
- Pricing anchors reference actual ranges from `services/pricing.md`
- All three next-step scenarios are included — strong fit, needs more discovery, needs to think
- If anti-patterns were flagged, the "not a fit" exit language includes the specific reason
- Follow-up email is pre-filled with everything already known and deadline is set to 24 hours after the call
