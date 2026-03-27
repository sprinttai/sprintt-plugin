---
description: Write a LinkedIn post for Sprintt. Use when the user asks to write, draft, or generate a LinkedIn post, social post, or content for LinkedIn.
---

# Write LinkedIn Post

## Context
Before executing, locate the knowledge-base by running `find /sessions -maxdepth 4 -name "knowledge-base" -type d 2>/dev/null | head -1`, then read the following files from that path:
- `marketing/strategy.md` — LinkedIn content types, cadence, and goals
- `brand/guidelines.md` — voice, tone, and copy rules
- `company/overview.md` — proof points and differentiators to draw from

These files are the source of truth. Every post must sound like Ricardo — a practitioner who builds real things, not a thought leader who just talks about them.

## Inputs
Collect the following:

1. **Topic or angle** — what is this post about? (can be a rough idea or a specific insight)
2. **Content type** — which format fits best? (suggest one based on the topic if the user isn't sure)
   - *"Here's what I built"* — show real work, real results
   - *"Most businesses get this wrong"* — contrarian take with substance
   - *Breakdown* — how a specific AI tool solves a specific business problem
   - *Quick tip* — something actionable the reader can use today
   - *Design partner update* — building in public (only if there's a real update to share)
3. **Any specific data, outcomes, or details to include** (optional — if none, draw from `company/overview.md`)
4. **Generate an X/Twitter adaptation?** (yes/no — shorter, punchier version of the same post)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read all KB files listed in Context above
2. Confirm topic and content type
3. Write the LinkedIn post following these rules from `brand/guidelines.md`:
   - Lead with a hook — first line must stop the scroll
   - Use short paragraphs (1–3 lines max) — LinkedIn rewards white space
   - Be specific and concrete — vague posts get ignored
   - Show, don't tell — results and specifics beat adjectives
   - End with one clear CTA or question — not multiple asks
   - No em dashes in every line, no corporate buzzwords, no hedging language
   - Active voice, strong verbs, forward momentum
4. If X/Twitter adaptation requested: shorten to under 280 characters or create a thread opener if the topic warrants it
5. Output the post(s)

## Output

**LinkedIn Post:**
[Full post, ready to copy-paste — include line breaks as they should appear]

**Character count:** [X characters] — note if it's ideal for LinkedIn (under 1,300 characters before "see more" cutoff) or long-form

**Suggested hashtags (3 max):** #[tag] #[tag] #[tag]

**Best time to post:** Reference `marketing/strategy.md` content calendar for the day this fits best (Monday teaching moment, Wednesday "what I'm building", Friday contrarian take, etc.)

If X/Twitter adaptation was requested:

**X/Twitter:**
[Adapted post — punchy, direct, under 280 characters or first tweet of a thread]

End with: "Copy into LinkedIn, review once, post. Don't overthink it."

## Quality Checks
- First line works as a standalone hook — would you stop scrolling?
- No hedging language ("we believe", "we think", "perhaps", "might")
- Specific and concrete — at least one real detail, number, or outcome
- Single CTA at the end — not multiple asks
- Voice matches `brand/guidelines.md` — Ricardo's voice, not a corporation's
- Under 3,000 characters total (LinkedIn limit)
