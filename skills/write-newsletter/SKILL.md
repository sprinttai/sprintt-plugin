---
description: Draft an "AI in Practice" newsletter issue — one real use case, one tool, one actionable tip — in Sprintt's voice, ready to paste into any platform.
---

# Write Newsletter

## Context

Before executing, read the following KB files:
- `marketing/strategy.md` — newsletter format, cadence, goals, and channel strategy
- `brand/guidelines.md` — voice, tone, and copy rules

## Inputs

Ask the user for the following before drafting:

1. **Main topic / use case** — What real AI use case or result is this issue about? (e.g., "how I used Claude to cut discovery time from 3 months to 1 week")
2. **Tool spotlight** — Is there a specific tool to feature this issue? (optional — skip if not relevant)
3. **Actionable tip** — What's the one thing a reader can do today? (can suggest one based on the topic if the user doesn't have one)
4. **Any personal anecdote or data point?** — Real stories and numbers make the newsletter land. Share anything relevant.
5. **Tone this issue** — Energetic, reflective, or matter-of-fact? (default: confident and direct per brand guidelines)

## Process

1. Draft the newsletter in the "AI in Practice" format:
   - **Subject line** — Direct, specific, and curiosity-driving. No clickbait. No emojis unless user requests. Max 60 characters.
   - **Preview text** — 1 sentence that complements (not repeats) the subject line. Max 90 characters.
   - **Opening hook** — 1-3 sentences. Start with the real-world result or observation, not a preamble.
   - **The Use Case** — What was the problem, what was built or tried, what was the result. Specific > vague. Numbers when available.
   - **The Tool** (optional) — One tool, one paragraph. What it does, why it's useful, one limitation to be honest.
   - **The Tip** — One actionable thing the reader can do this week. Concrete, specific, doable in under an hour.
   - **Closing** — 1-2 sentences in Ricardo's voice. Can be an invitation to reply, a question, or a forward look.
   - **CTA** — One call to action max. Default: book a strategy call. Adapt if the issue has a more natural CTA.

2. Apply brand voice throughout:
   - Confident, not arrogant
   - Direct and specific — cut filler words
   - Technical but accessible — no unexplained jargon
   - Personality-forward — this is Ricardo's voice, not a corporate newsletter

3. After drafting, output:
   - Subject line
   - Preview text
   - Full newsletter body (plain text, no platform-specific formatting)
   - Word count
   - Suggested send day (based on strategy.md content calendar — Thursday is newsletter day)

## Output Format

Output as clean plain text that can be pasted into any email platform. Use simple formatting cues only:
- Section breaks with a blank line
- Bold text indicated with **asterisks** if the user's platform supports markdown, otherwise plain
- No HTML, no platform-specific blocks

Note to user: once you've chosen a newsletter platform (Buttondown, Substack, ConvertKit, etc.), future issues can be formatted specifically for it.

## Quality Checks

- Subject line is specific — could it only be written by someone who actually did the thing? If not, sharpen it.
- Use case includes a real result or number, not just a description of what was done
- Tip is actionable this week, not a vague suggestion
- No filler phrases: "in today's fast-paced world," "AI is transforming," "leverage synergies"
- Reads like Ricardo wrote it, not like a newsletter generator wrote it
- Word count target: 300–500 words (short enough to read in 3 minutes)
