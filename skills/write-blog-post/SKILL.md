---
description: Write a blog post for sprintt.ai. Use when the user asks to write, draft, or generate a blog post, article, or written content for the website.
---

# Write Blog Post

## Context
Before executing, use the GitHub connector to read the following files from the **knowledge-base** repository:
- `marketing/strategy.md` — blog content strategy, SEO approach, and content goals
- `brand/guidelines.md` — voice, tone, and copy rules
- `services/offerings.md` — service descriptions to accurately represent what Sprintt does
- `company/overview.md` — proof points and differentiators

These files are the source of truth. Every post should teach something useful or demonstrate a real result — not be a generic AI think-piece.

## Inputs
Collect the following:

1. **Topic or title idea** — what is this post about?
2. **Target reader** — which ICP is this written for? (SMB owner, growth-stage startup, mid-market ops leader, technical founder — or general)
3. **Target keyword** — what would someone Google to find this? (e.g., "how to automate [X] with AI", "AI consulting for [industry]")
4. **Key points to cover** — what should the reader walk away knowing or being able to do?
5. **Any specific outcomes, data, or examples to include** (optional — if none, draw from `company/overview.md`)
6. **Approximate length** — short (500–800 words), medium (800–1,200 words), or long (1,200–2,000 words)

If the user provides any of this via $ARGUMENTS, use it and only ask for what's missing.

## Process
1. Read all KB files listed in Context above
2. Confirm all inputs
3. Write the blog post following these rules:
   - Answer one specific question a potential client might Google — per `marketing/strategy.md`
   - Lead with the problem or insight, not with Sprintt
   - Use Ricardo's voice — practical, direct, no buzzwords, personality-forward
   - Each section should leave the reader with something actionable
   - Include a CTA at the end (book a call, Calendly link from entity.md if read, or "reply to this post")
   - SEO: use the target keyword naturally in the title, first paragraph, and 2–3 headings
4. Format the output as a complete MDX file with proper frontmatter — ready to drop into `content/blog/` in the sprintt repo

## Output
Produce the complete MDX file content:

~~~
---
title: "[POST TITLE]"
date: "[YYYY-MM-DD]"
description: "[1–2 sentence description for SEO meta and blog listing — include target keyword]"
tags: ["[tag1]", "[tag2]", "[tag3]"]
readingTime: "[X min read]"
---

[Full post content in markdown]
~~~

After the MDX content, provide:

**Filename:** `[slug].mdx` (URL-friendly slug matching the title)

**To publish:**
1. Create the file at `content/blog/[slug].mdx` in the sprintt repo
2. Commit and push to main (or your working branch)
3. Vercel will auto-deploy — post will be live at `sprintt.ai/blog/[slug]`

## Quality Checks
- Frontmatter is complete — all fields filled in
- Target keyword appears in title, first paragraph, and at least 2 headings
- Post answers a specific question — not a generic overview
- At least one actionable takeaway per major section
- CTA at the end is clear and specific
- Voice matches `brand/guidelines.md` — practical, direct, Ricardo's perspective
- Reading time estimate is accurate (roughly 200–250 words per minute)
- Slug is URL-friendly (lowercase, hyphens, no special characters)
