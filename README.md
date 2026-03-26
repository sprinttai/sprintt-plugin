# Sprintt Plugin for Claude Cowork

The Sprintt business OS — a Claude Cowork plugin that handles proposals, contracts, content, and operations for an AI consulting firm.

## Installation

```
/plugin install sprinttai/sprintt-plugin
```

## Skills

Skills are invoked in Cowork as `/sprintt:[skill-name]`.

### Wave 1 — Get Paid

| Skill | Invocation | Description |
|-------|-----------|-------------|
| Generate NDA | `/sprintt:generate-nda` | Draft a mutual NDA for a new prospect or client |
| Generate Contract | `/sprintt:generate-contract` | Generate a Consulting Services Agreement or Design Partner Agreement |
| Generate SOW | `/sprintt:generate-sow` | Build a Statement of Work with scope, timeline, and fees |
| Invoicing Guide | `/sprintt:invoicing-guide` | Walk through billing a client milestone in Mercury |

### Coming Soon

- **Wave 2 — Win Deals:** `generate-proposal`, `discovery-prep`
- **Wave 3 — Grow Pipeline:** `write-linkedin-post`, `write-blog-post`, `write-newsletter`
- **Wave 4 — Run the Business:** `client-onboarding`, `financial-review`, `checklist-update`

## How It Works

Each skill reads live business context from a private knowledge base repository at runtime via the GitHub connector — no sensitive data is stored in this repo. The plugin contains only skill instructions; all entity details, templates, pricing, and brand data live in the connected private repo.

**Required:** The GitHub connector must be enabled in Cowork and connected to the private `knowledge-base` repository for skills to function.

## Structure

```
skills/
└── [skill-name]/
    ├── SKILL.md      ← Instructions for Claude
    └── reference.md  ← KB dependency manifest (no business data)
.claude-plugin/
└── plugin.json       ← Plugin metadata
```

## Contributing

This plugin is maintained by [Ricardo Ramirez](https://sprintt.ai). To suggest a skill or report an issue, open a GitHub issue.
