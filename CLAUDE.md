# Sprintt Plugin — Context

This is the Claude Cowork plugin for Sprintt, an AI consulting firm owned by Ricardo Ramirez (Ramirez Digital Ventures LLC d/b/a Sprintt).

## What This Repo Is

A standalone Claude Cowork plugin installed via:
```
/plugin install sprinttai/sprintt-plugin
```

Each skill in `skills/` packages instructions (`SKILL.md`) and bundled KB context (`reference.md`) so it works self-contained when installed in Cowork.

## Knowledge Base Location

The Sprintt knowledge base (source of truth for all business context) lives at:
```
/Users/ricardoramirez/Documents/Projects/knowledge-base/
```

**Before building or updating any skill, read the relevant KB files from that path.** Key files by skill type:

| Skill | KB Files to Read |
|-------|-----------------|
| `generate-nda` | `legal/templates/nda.md`, `company/entity.md` |
| `generate-contract` | `legal/templates/consulting-agreement.md`, `legal/templates/design-partner-agreement.md`, `company/entity.md` |
| `generate-sow` | `legal/templates/sow.md`, `services/pricing.md`, `services/offerings.md` |
| `generate-proposal` | `legal/templates/proposal.md`, `services/offerings.md`, `services/pricing.md`, `services/ideal-client.md`, `company/overview.md`, `brand/guidelines.md` |
| `generate-invoice` | `company/entity.md`, `company/finances.md` |
| `discovery-prep` | `operations/discovery-call.md`, `services/offerings.md`, `services/ideal-client.md` |
| `write-linkedin-post` | `marketing/strategy.md`, `brand/guidelines.md`, `company/overview.md` |
| `write-blog-post` | `marketing/strategy.md`, `brand/guidelines.md`, `services/offerings.md` |
| `write-newsletter` | `marketing/strategy.md`, `brand/guidelines.md` |
| `client-onboarding` | `operations/client-onboarding.md`, `operations/workflows.md` |
| `financial-review` | `company/finances.md`, `business-plan/plan.md` |
| `checklist-update` | `business-plan/checklist.md` |

## How to Build a Skill

1. Read the relevant KB files listed above
2. Create `skills/[skill-name]/SKILL.md` — instructions for Claude
3. Create `skills/[skill-name]/reference.md` — paste the relevant KB content the skill needs at runtime (this is what gets bundled into the installed plugin)
4. Follow the skill template in the KB at `plugin/skills-roadmap.md`
5. Commit and push — the plugin updates for all users on next `/plugin install`

## Skill Invocation

Skills are invoked in Cowork as `/sprintt:[skill-name]` (e.g., `/sprintt:generate-nda`).

## Build Order

Follow the wave priority in `/Users/ricardoramirez/Documents/Projects/knowledge-base/plugin/skills-roadmap.md`:
- **Wave 1 (Get Paid):** generate-nda ✅, generate-contract, generate-sow, generate-invoice
- **Wave 2 (Win Deals):** generate-proposal, discovery-prep
- **Wave 3 (Grow Pipeline):** write-linkedin-post, write-blog-post, write-newsletter
- **Wave 4 (Run the Business):** client-onboarding, financial-review, checklist-update

## Rules

- Never hardcode rates or entity details in SKILL.md — pull them from the KB and put them in `reference.md`
- Every client-facing skill must include entity name ("Ramirez Digital Ventures LLC d/b/a Sprintt") in its `reference.md`
- Bump the version in `.claude-plugin/plugin.json` when skills change (MAJOR.MINOR.PATCH)
