# Reference — Generate SOW

## legal/templates/sow.md

# STATEMENT OF WORK

**SOW Number:** [SOW-YYYY-### — e.g., SOW-2026-001 for the first SOW of 2026]
**Effective Date:** [DATE]
**Associated Agreement:** Consulting Services Agreement dated [MSA DATE] / Design Partner Agreement dated [DPA DATE]

---

**Consultant:** Ramirez Digital Ventures LLC d/b/a Sprintt
**Client:** [CLIENT LEGAL NAME] ("[CLIENT SHORT NAME]")

---

> **Usage note:** This template covers two engagement types. Use **Sections 1–6** for project-based engagements (fixed scope, one-time deliverables). For retainer engagements (Advisor, Builder, or Partner tier), use **Sections 1 and 7** instead — Sections 2–6 do not apply to retainers.
>
> **Pricing note:** All `[PLACEHOLDER]` values referencing rates, amounts, or thresholds must be sourced from `services/pricing.md` at generation time. Do not hardcode any rates or dollar amounts — use the current values from pricing.md.

---

## 1. PROJECT OVERVIEW

### 1.1 Project Name
[PROJECT NAME]

### 1.2 Engagement Type
☐ Project-based (fixed scope — use Sections 2–6)
☐ Retainer (monthly recurring — use Section 7)

### 1.3 Background
[Brief description of the client's situation, the problem being solved, or the opportunity being pursued. 2-3 sentences.]

### 1.4 Objectives
[What success looks like. Be specific and measurable where possible.]

- Objective 1: [e.g., "Reduce manual data entry time by 50% through AI-powered automation"]
- Objective 2: [e.g., "Deploy a customer support AI agent handling Tier 1 inquiries"]
- Objective 3: [e.g., "Train the operations team on AI workflow management"]

### 1.5 Data and Systems Access
The following client data, systems, or tools will be accessed by Sprintt in the course of this engagement:

| System / Dataset | Data Type | Purpose |
|-----------------|-----------|---------|
| [e.g., CRM — Salesforce] | [e.g., Customer records] | [e.g., Build training dataset for lead scoring model] |
| [e.g., Internal Slack workspace] | [e.g., Message history] | [e.g., Analyze communication patterns] |

All data accessed under this SOW is governed by the data handling obligations in the associated agreement. [CLIENT SHORT NAME] warrants that it has the right to share this data with Sprintt for the purposes stated above.

---

## 2. SCOPE OF WORK *(Project-based only — skip for retainers)*

### 2.1 In Scope
[Detailed list of what Sprintt will deliver]

- [ ] Deliverable 1: [Description]
- [ ] Deliverable 2: [Description]
- [ ] Deliverable 3: [Description]

### 2.2 Out of Scope
[Explicitly state what is NOT included to prevent scope creep]

- [e.g., "Ongoing maintenance and support after delivery"]
- [e.g., "Integration with systems not listed in Section 2.1"]
- [e.g., "Data migration from legacy systems"]

### 2.3 Assumptions
[What needs to be true for this project to succeed]

- Client will provide access to required systems, data, and documentation within [X] business days of project start
- Client will designate a single point of contact for approvals and feedback
- Client feedback on deliverables will be provided within [X] business days of submission
- [Any technical assumptions about the client's environment or tooling]
- [Any dependency on third-party vendors or services outside Sprintt's control]

---

## 3. TIMELINE AND MILESTONES *(Project-based only — skip for retainers)*

| Milestone | Description | Target Date | Deliverable |
|-----------|-------------|-------------|-------------|
| Kickoff | Project kickoff meeting | [DATE] | Kickoff notes, refined plan |
| Phase 1 | [Description] | [DATE] | [Deliverable] |
| Phase 2 | [Description] | [DATE] | [Deliverable] |
| Review | Client review and feedback | [DATE] | Feedback incorporated |
| Delivery | Final delivery | [DATE] | All deliverables complete |

**Total estimated duration:** [X] weeks

**Note:** Timeline assumes timely client responses per Section 2.3. Delays in client feedback or access will extend the timeline accordingly. Sprintt will communicate proactively if a delay arises.

---

## 4. FEES AND PAYMENT *(Project-based only — skip for retainers)*

### 4.1 Project Fee

| Item | Amount |
|------|--------|
| [Service/Deliverable 1] | $[AMOUNT] |
| [Service/Deliverable 2] | $[AMOUNT] |
| [Service/Deliverable 3] | $[AMOUNT] |
| **Total Project Fee** | **$[TOTAL]** |

[If Design Partner: "This reflects a [XX]% Design Partner discount off standard rates of $[STANDARD TOTAL]."]

### 4.2 Payment Schedule

Select the appropriate structure based on total project fee and delete the others:

**Under [PAYMENT_TIER_1_MAX] (reference `services/pricing.md`):**

| Payment | Amount | Due |
|---------|--------|-----|
| Deposit | $[AMOUNT] (50%) | Upon SOW execution |
| Final | $[AMOUNT] (50%) | Upon final delivery |
| **Total** | **$[TOTAL]** | |

**[PAYMENT_TIER_1_MAX]–[PAYMENT_TIER_2_MAX] (reference `services/pricing.md`):**

| Payment | Amount | Due |
|---------|--------|-----|
| Deposit | $[AMOUNT] (40%) | Upon SOW execution |
| Midpoint | $[AMOUNT] (30%) | Upon [MILESTONE] completion |
| Final | $[AMOUNT] (30%) | Upon final delivery |
| **Total** | **$[TOTAL]** | |

**Over [PAYMENT_TIER_2_MAX] (reference `services/pricing.md`):**

| Payment | Amount | Due |
|---------|--------|-----|
| Deposit | $[AMOUNT] (30%) | Upon SOW execution |
| Monthly | $[AMOUNT]/mo | 1st of each month |
| Final | $[AMOUNT] (20%) | Upon final delivery |
| **Total** | **$[TOTAL]** | |

### 4.3 Additional Work
Work outside the scope defined in Section 2 will be quoted separately. If the client requests additional work during the engagement, Sprintt will provide a written estimate before proceeding. Additional work will be billed at:
- **Standard rate:** [STANDARD_HOURLY_RATE] (reference `services/pricing.md` for current rate)
- **Design Partner rate:** [DESIGN_PARTNER_HOURLY_RATE] (reference `services/pricing.md` for current Design Partner rate)

### 4.4 Expenses
Out-of-pocket expenses incurred by Sprintt on behalf of [CLIENT SHORT NAME] (API credits, software licenses, travel, etc.) are reimbursed at cost with no markup. Expenses exceeding [EXPENSE_APPROVAL_THRESHOLD] require prior written approval from [CLIENT SHORT NAME] before being incurred. Expenses are invoiced separately from project fees.

---

## 5. CLIENT RESPONSIBILITIES *(Project-based only — skip for retainers)*

[CLIENT SHORT NAME] shall:

- Designate [CLIENT CONTACT NAME] as the primary point of contact for all project communication and approvals
- Provide access to necessary systems, data, and documentation as specified in Section 1.5
- Provide training data, sample documents, or historical records required for AI model development or testing
- Grant API access or credentials for any third-party systems listed in Section 1.5 within [X] business days of project start
- Make relevant subject matter experts (SMEs) available for input sessions, interviews, or UAT participation as needed
- Participate in user acceptance testing (UAT) for AI outputs before final delivery, providing specific written feedback within the review window
- Respond to requests for information or feedback within [X] business days
- Participate in scheduled meetings and review sessions
- Provide final written approval of all deliverables

---

## 6. ACCEPTANCE *(Project-based only — skip for retainers)*

### 6.1 Delivery
Upon delivery of each milestone, Client shall have **[REVIEW_ACCEPTANCE_WINDOW_DAYS]** to review and either accept or provide specific, written feedback. This window is the default per `legal/defaults.md` and is adjustable per engagement cadence — confirm with client at kickoff.

### 6.2 Revisions
Sprintt will make up to **[REVISION_ROUNDS] rounds of revisions** per deliverable based on Client feedback. Additional revision rounds will be billed at the applicable hourly rate.

### 6.3 Deemed Acceptance
If Client does not respond within the review period in Section 6.1, the deliverable shall be deemed accepted. This clause protects against indefinitely stalled approvals — both Parties acknowledge and agree to this mechanism.

---

## 7. RETAINER ENGAGEMENT *(Use this section instead of Sections 2–6 for retainer engagements)*

### 7.1 Retainer Tier

☐ **Advisor** — 5 hrs/mo at [ADVISOR_MONTHLY_RATE] ([ADVISOR_EFFECTIVE_RATE] effective)
☐ **Builder** — 15 hrs/mo at [BUILDER_MONTHLY_RATE] ([BUILDER_EFFECTIVE_RATE] effective)
☐ **Partner** — 30 hrs/mo at [PARTNER_MONTHLY_RATE] ([PARTNER_EFFECTIVE_RATE] effective)

Selected tier: **[TIER NAME]**
Monthly committed hours: **[X] hrs/mo**
Monthly rate: **$[AMOUNT]/mo**

[If Design Partner: "This reflects a [XX]% Design Partner discount off the standard [TIER] rate of $[STANDARD RATE]/mo."]

### 7.2 Included Monthly Deliverables

*Fill in the deliverables for the selected tier from `services/pricing.md`. Do not leave blank.*

**Advisor (5 hrs/mo):**
- One 60-minute strategy session per month
- Up to 3 hours of async support (email/Slack) — responses within one business day
- One written output per month (roadmap review, vendor evaluation, recommendation brief, or similar)
- Session notes and follow-up action items after every call

**Builder (15 hrs/mo):**
- Two 60-minute working sessions per month
- Active development or advisory work between sessions (~11 hrs)
- Async support with same-day response during business hours
- Monthly progress summary and updated priorities

**Partner (30 hrs/mo):**
- Weekly working sessions (four 60-minute calls per month)
- Embedded availability for prioritization, unblocking, and decision support (~26 hrs)
- Async support with same-day response during business hours
- Attends relevant team meetings as needed
- Monthly roadmap review and stakeholder-ready status update

### 7.3 Commitment Period
Initial commitment: **3 months** (Months 1–3: [START DATE] through [END DATE])

After the initial 3-month period, this retainer continues month-to-month until terminated by either Party with **30 days' written notice**.

Month-to-month rate after initial term: **$[AMOUNT + MONTH_TO_MONTH_PREMIUM]/mo** ([MONTH_TO_MONTH_PREMIUM_RATE] premium applies per pricing policy — reference `services/pricing.md`)

### 7.4 Billing
Monthly retainer fees are billed **in advance** on the 1st of each month. First invoice is due upon execution of this SOW before work begins.

### 7.5 Hours and Overages
Committed monthly hours do not roll over to the following month. Hours used beyond the monthly commitment are billed at **[STANDARD_HOURLY_RATE]** (standard rate — reference `services/pricing.md`), invoiced at the end of the month.

### 7.6 Pausing
No pausing during the initial 3-month commitment period. After the initial term, [CLIENT SHORT NAME] may pause the retainer once per 12-month period for up to 1 month with 30 days written notice. Hours do not roll over during a pause.

### 7.7 Expenses
Out-of-pocket expenses incurred by Sprintt on behalf of [CLIENT SHORT NAME] are reimbursed at cost with no markup. Expenses exceeding [EXPENSE_APPROVAL_THRESHOLD] require prior written approval. Expenses are invoiced separately from monthly retainer fees.

### 7.8 Focus Areas *(optional — use to align on priorities for the engagement)*
During this retainer, Sprintt's work will focus on the following areas, subject to adjustment by mutual agreement:

- [Focus area 1 — e.g., "AI roadmap development and prioritization"]
- [Focus area 2 — e.g., "Workflow automation for [DEPARTMENT]"]
- [Focus area 3 — e.g., "Team enablement and prompt engineering guidance"]

---

## 8. SIGNATURES

This Statement of Work is governed by the terms of the [Consulting Services Agreement / Design Partner Agreement] between the Parties dated [AGREEMENT DATE].

**Ramirez Digital Ventures LLC d/b/a Sprintt**

Signature: ________________________________
Name: Ricardo Ramirez
Title: AR (Authorized Representative)
Date: ________________________________

**[CLIENT LEGAL NAME]**

Signature: ________________________________
Name: [CLIENT CONTACT NAME]
Title: [CLIENT TITLE]
Date: ________________________________

---

## legal/defaults.md

# Legal Defaults

> **Source of truth for all structural contractual terms used across Sprintt's legal templates.**
>
> When generating any legal document, read this file and substitute the placeholder values below into the corresponding `[PLACEHOLDER]` fields in the template. Do not hardcode these values in templates — change them here and all documents pick up the update automatically.
>
> For pricing-related terms (hourly rates, payment tiers, retainer rates, expense thresholds, payment terms, late payment rates), see `services/pricing.md`.

---

## Termination

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[MSA_TERMINATION_NOTICE_DAYS]` | 30 days | Consulting Services Agreement — termination for convenience |
| `[DPA_TERMINATION_NOTICE_DAYS]` | 15 days | Design Partner Agreement — termination for convenience |
| `[CURE_PERIOD_DAYS]` | 15 days | Both agreements — cure period before termination for cause |
| `[NDA_TERMINATION_NOTICE_DAYS]` | 30 days | NDA — early termination notice period |

> **Note on termination notice inconsistency:** The MSA uses 30 days and the DPA uses 15 days. This is intentional — the DPA covers shorter, more defined engagements. If you want to standardize these, update both values here and both templates pick up the change.

---

## Confidentiality

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[CONFIDENTIALITY_SURVIVAL_YEARS]` | 2 years | Consulting Agreement (§4.4), Design Partner Agreement (§5.5), NDA (§5) |
| `[NDA_TERM_YEARS]` | 2 years | NDA — duration of the agreement itself |
| `[NDA_SURVIVAL_YEARS]` | 2 years | NDA — confidentiality obligations post-termination |

---

## Data Handling

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[DATA_RETURN_DAYS]` | 30 days | Consulting Agreement (§8.4), Design Partner Agreement (§6.1) — window to return or destroy client data after termination |
| `[NDA_RETURN_DESTROY_DAYS]` | 10 business days | NDA (§6) — window to return or destroy confidential materials upon request |

---

## Non-Solicitation

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[NON_SOLICITATION_MONTHS]` | 12 months | Consulting Agreement (§10), Design Partner Agreement (§12) |

---

## Force Majeure

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[FORCE_MAJEURE_NOTIFICATION_DAYS]` | 5 business days | Consulting Agreement (§12), Design Partner Agreement (§13) — notice window after a force majeure event |
| `[FORCE_MAJEURE_EXIT_DAYS]` | 30 days | Consulting Agreement (§12), Design Partner Agreement (§13) — duration after which either party may exit |

---

## Delivery and Acceptance (SOW)

| Placeholder | Current Value | Applies To |
|---|---|---|
| `[REVIEW_ACCEPTANCE_WINDOW_DAYS]` | 5 business days | SOW (§6.1) — default client review window before deemed acceptance |
| `[REVISION_ROUNDS]` | 2 | SOW (§6.2) — default revision rounds included per deliverable |

> **Note:** Both of these are defaults — they should be confirmed with the client at kickoff and can be adjusted per engagement in the SOW.

---

## services/pricing.md

# Pricing Strategy

## Philosophy

Price based on value delivered, not hours spent. The right pricing model depends on the type of work:

- **Strategy & advisory** — priced by scope and complexity
- **Workshops & training** — priced by session type and team size (more people = more prep, facilitation, and follow-up)
- **Operational efficiency** — priced by how many teams/workflows are in scope
- **Technical builds** — priced by scope and complexity; a contractor may be brought in for larger initiatives
- **Retainers** — priced on Ricardo's committed time per month

---

## Ricardo's Rate

- **Standard:** $225/hr
- **Design partner:** $125–$150/hr
- **Minimum engagement:** 5 hours

All project and retainer pricing below is derived from this rate. Hourly billing is available but project-based quotes are preferred — clients get predictability, and the work is priced on value rather than clock time.

---

## Contractor Pricing Model

When one or more contractors are involved in delivery, use this model to build the project price floor before applying value-based pricing on top.

### Formula

```
Project price floor = (Ricardo's hours × $225) + (Contractor hours × contractor rate)
                      ÷ (1 − target gross margin)
```

**Target gross margin:**
- Ricardo-only engagements: 85–90%
- 1 contractor: 60–65%
- 2+ contractors: 55–60% (management overhead increases)

**Example — medium complexity AI Agent Build with 1 contractor:**
- Ricardo: 25 hrs × $225 = $5,625
- Contractor: 50 hrs × $100 = $5,000
- Total cost: $10,625
- At 62% gross margin: $10,625 ÷ 0.38 = **~$27,960 price floor**
- Then apply value-based pricing — if the deliverable is worth more, charge more

### Contractor Rate Assumptions

| Contractor Type | Estimated Rate |
|----------------|---------------|
| SDLC engineer (mid-level) | $75–$100/hr |
| SDLC engineer (senior) | $100–$125/hr |

Always confirm contractor rate before quoting a project. Never quote a project with contractor involvement without knowing the actual rate first.

### Scaling Beyond 1 Contractor

Each additional contractor adds capacity but also adds Ricardo's coordination and QA overhead (~10–15% of the contractor's hours billed at Ricardo's rate). Factor this in:

```
Additional overhead = contractor hours × 12.5% × $225/hr
```

For large clients requiring 2+ contractors, the existing price range ceilings may not apply — quote based on the formula and actual scope, not the standard table. The standard ranges are calibrated for Ricardo + 0–1 contractors.

---

## Strategy & Advisory

_Priced by scope and complexity. Team size is not a primary driver._

| Service | Standard | Design Partner | Duration |
|---------|----------|----------------|----------|
| AI Readiness Assessment | $3,000–$6,000 | $1,800–$3,500 | 1–2 weeks |
| Strategy Workshop (half-day) | $2,500 | $1,500 | 4 hours |
| Strategy Workshop (full-day) | $4,500 | $2,500 | 8 hours |

---

## Workshops & Team Training

_Priced by session type and team size. The number of participants directly affects preparation, facilitation complexity, and follow-up support._

| Service | Up to 10 | 11–25 | 26–50 | 50+ |
|---------|----------|-------|-------|-----|
| Prompt Engineering (half-day) | $2,000 | $3,000 | $4,500 | Custom |
| Prompt Engineering (full-day) | $3,500 | $5,000 | $7,500 | Custom |
| AI Tools & Workflow Training (half-day) | $2,000 | $3,000 | $4,500 | Custom |
| AI Tools & Workflow Training (full-day) | $3,500 | $5,000 | $7,500 | Custom |
| Developer Tooling Workshop (half-day) | $2,500 | $3,500 | $5,000 | Custom |
| Developer Tooling Workshop (full-day) | $4,500 | $6,500 | $9,000 | Custom |

**Add-ons (quoted separately):**
- Custom playbook tailored to org's workflows: $2,500–$6,000
- Post-workshop office hours (2 sessions): $750

### AI Champions Program

_A standalone ongoing program — not an add-on. Priced by program scope, not team size._

| Scope | Standard | Design Partner | Duration |
|-------|----------|----------------|----------|
| 1–3 champions, 4 sessions | $4,000–$5,500 | $2,500–$3,500 | 4 weeks |
| 1–3 champions, 8 sessions | $7,000–$9,000 | $4,500–$6,000 | 8 weeks |

Includes structured sessions, follow-up coaching between sessions, and a resource library tailored to the organization's tools and workflows. Goal is self-sufficient internal AI capability — not ongoing dependency on Sprintt.

---

## Operational Efficiency

_Priced by how many teams or workflows are in scope. A single-team engagement is very different from an org-wide rollout._

| Scope | Standard | Design Partner | Duration |
|-------|----------|----------------|----------|
| Single team or workflow | $3,000–$6,000 | $1,800–$4,000 | 1–3 weeks |
| Department (2–5 teams) | $7,500–$15,000 | $4,500–$10,000 | 3–6 weeks |
| Organization-wide | Custom | Custom | 6–12 weeks |

---

## Technical Builds

_Priced by scope and complexity. For larger initiatives, Ricardo may bring in one SDLC contractor to support implementation — this is accounted for in the project quote, not billed separately to the client._

**Service distinction:**
- **AI Agent Build** — The deliverable is an autonomous AI system that makes decisions and takes actions (e.g., customer support agent, lead qualification bot, code review agent). The agent IS the product.
- **Workflow Automation** — The deliverable is an intelligent pipeline that connects existing tools and reduces manual work (e.g., automated reporting, CRM-to-email routing, document processing). The automation runs in the background.

| Service | Standard | Design Partner | Duration |
|---------|----------|----------------|----------|
| Proof of Concept | $4,000–$9,000 | $2,500–$6,000 | 1–2 weeks |
| AI Agent Build | $6,500–$30,000 | $4,000–$18,000 | 2–6 weeks |
| Workflow Automation | $4,000–$18,000 | $2,500–$12,000 | 1–4 weeks |
| System Integration | $9,000–$35,000 | $6,000–$22,000 | 3–8 weeks |
| AI Product Development (full) | $15,000–$60,000 | $10,000–$40,000 | 4–12 weeks |

**Complexity guide — use this to land on a number within the range:**

| Complexity | Signals | Price (within range) |
|------------|---------|----------------------|
| Low | Single-purpose scope, standard APIs, well-defined requirements, minimal custom logic | Bottom 25% of range |
| Medium | Multiple integrations, custom logic, some ambiguity in requirements, moderate data complexity | Middle 50% of range |
| High | Multi-system or multi-agent, enterprise integrations, sensitive data, tight timeline, or significant unknowns | Top 25% of range |

When in doubt, scope the PoC first to reduce unknowns before committing to a full build price.

**On contractor support:** For larger or longer builds, Ricardo may bring in one SDLC engineer for implementation. Ricardo scaffolds the project and sets up agent context, and the contractor works within that system. All client-facing leadership and accountability remains Ricardo's. Contractor cost is factored into the quoted price — clients are not billed separately for it.

---

## Retainers

_Monthly recurring engagements, priced on Ricardo's committed hours. **Minimum commitment: 3 months** for all tiers. Month-to-month available after the initial term at a 10% premium._

| Tier | Hours/Month | Monthly Rate | Effective Hourly | Best For |
|------|------------|-------------|-----------------|----------|
| Advisor | 5 hrs | $1,000/mo | $200/hr | Strategic guidance, lightweight ongoing support |
| Builder | 15 hrs | $2,750/mo | $183/hr | Ongoing development + advisory |
| Partner | 30 hrs | $5,000/mo | $167/hr | Embedded fractional AI lead / CPO |

**What each tier includes:**

**Advisor (5 hrs/mo)**
- One 60-minute strategy session per month
- Up to 3 hours of async support (email/Slack) — responses within one business day
- One written output per month (roadmap review, vendor evaluation, recommendation brief, or similar)
- Session notes and follow-up action items after every call

**Builder (15 hrs/mo)**
- Two 60-minute working sessions per month
- Active development or advisory work between sessions (~11 hrs)
- Async support with same-day response during business hours
- Monthly progress summary and updated priorities

**Partner (30 hrs/mo)**
- Weekly working sessions (four 60-minute calls)
- Embedded availability for prioritization, unblocking, and decision support (~26 hrs)
- Async support with same-day response during business hours
- Attends relevant team meetings as needed
- Monthly roadmap review and stakeholder-ready status update

---

## Pricing Rules

1. **Always quote project-based** before offering hourly. Clients get predictability; value is captured more accurately.
2. **Never go below $125/hr effective rate**, even for design partners.
3. **Scope creep:** Every project has a defined scope in the SOW. Out-of-scope work is billed at the standard hourly rate.
4. **Payment structure:**
   - Under $5,000: 50% upfront, 50% on delivery
   - $5,000–$15,000: 40% upfront, 30% at midpoint, 30% on delivery
   - Over $15,000: 30% upfront, monthly milestones, 20% on delivery
   - Retainers: Billed monthly in advance
5. **Payment terms:** Net 15, ACH or wire via Mercury
6. **Late payment:** 1.5% per month after 15 days
7. **Retainer overages:** Hours used beyond the monthly commitment are billed at the standard rate ($225/hr), invoiced at the end of the month. Unused hours do not roll over.
8. **Retainer pausing:** No pausing during the initial 3-month commitment. After that, clients may pause once per 12-month period for up to 1 month with 30 days written notice. Hours do not roll over during a pause.
9. **Expense reimbursement:** Out-of-pocket costs incurred on behalf of a client (API credits, third-party tool licenses, travel, etc.) are passed through at cost with no markup. Expenses over $100 require prior written approval from the client.

---

## When to Adjust Pricing

**Charge more when:**
- Client is enterprise (>500 employees) or well-funded startup
- Tight timelines or weekend work required
- Project involves sensitive data or elevated security requirements
- Work will generate significant, quantifiable ROI
- Fractional CPO scope involves ongoing decision-making authority

**Offer discounts when:**
- Client agrees to case study + testimonial (10–15%)
- Multi-project commitment (10–20%)
- Referral from an existing client (10% on first project)
- Non-profit or social impact organization (evaluate case by case)

**Maximum combined discount: 25%.** Apply the highest-value discount first, then layer others up to the cap. Discounts beyond 25% should use the Design Partner program instead — it exists for a reason.

---

## Unlisted Services Pricing

> Not for public promotion. Referral and conversation basis only. Do not include in standard proposals or marketing materials.

### Small Business Website Creation

| Service | Price | Duration |
|---------|-------|----------|
| Standard website (5–10 pages) | $2,500–$5,000 | 2–4 weeks |
| AI-powered website (site + 1 AI feature) | $4,500–$8,000 | 3–5 weeks |
| AI landing page | $1,500–$3,000 | 1–2 weeks |
| Monthly maintenance | $150–$300/mo | Ongoing |

**Pricing notes:**
- AI features (chatbot, lead capture, booking automation, content personalization) add $1,500–$3,000 to the base website price
- Contractor cost is factored into project pricing — not billed separately
- Same payment structure as standard projects (50/50 split for under $5,000; milestone-based above)
- Always look for an upsell path to AI consulting or operational efficiency work after delivery

---

## Market Reference Points

| Tier | Rate |
|------|------|
| Big consultancies (McKinsey, Deloitte) | $300–$600/hr |
| Boutique AI firms | $200–$350/hr |
| Independent AI consultants | $150–$250/hr |
| Offshore / junior consultants | $50–$100/hr |

Sprintt sits in the **independent-to-boutique** range. $225/hr reflects full SDLC coverage, Fractional CPO seniority, and deep GenAI tooling expertise — well below boutique firm rates, and clearly above the generalist freelancer tier.

---

## services/offerings.md

# Service Offerings

## 1. AI Strategy & Roadmapping

**Who it's for:** Business owners and executives who have an AI initiative that isn't moving — or don't know where to start.

### Services

- **AI Readiness Assessment** — Audit current workflows, tech stack, and team capabilities to identify the highest-impact AI opportunities. Deliverable: prioritized roadmap with ROI estimates.

- **AI Strategy Workshop** — Half-day or full-day facilitated session with leadership. Map business goals to specific AI use cases. Walk away with a concrete 90-day action plan.

- **Ongoing Advisory** — Monthly retainer for fractional AI strategic guidance. Regular check-ins, vendor evaluation, implementation oversight.

### Ideal for
- Companies with 10–500 employees exploring AI seriously for the first time
- Executives overwhelmed by AI options and vendor noise
- Organizations that have an AI roadmap that hasn't shipped anything

---

## 2. AI Product Development

**Who it's for:** Companies ready to build an AI-powered product or feature and need a senior operator to lead it end-to-end.

### Services

- **AI Agent Development** — Custom-built AI agents that handle specific business functions: customer support, data analysis, content generation, lead qualification, internal Q&A, developer tooling, and more.

- **AI-Native Product Builds** — Full product design, development, and launch. Ricardo leads strategy and delivery; a contracted SDLC engineer handles implementation within a scaffolded, agent-ready project structure.

- **Workflow Automation** — Connect existing tools with AI-powered automation. Reduce manual work, eliminate bottlenecks, and create intelligent pipelines.

- **System Integration** — Embed AI capabilities into existing software, CRMs, ERPs, or internal tools. API development, RAG systems, custom model fine-tuning recommendations.

- **Proof of Concept (PoC)** — Rapid prototyping to validate an AI use case before committing to a full build. Delivered in 1–2 weeks.

### Delivery Model
Ricardo leads every engagement. For development-heavy projects, one SDLC contractor is brought in for implementation. Ricardo sets up the project scaffolding and AI agent context so the contractor ships fast within a well-defined system. All client-facing work runs through Ricardo.

### Ideal for
- Startups building an AI-native product who need a hands-on technical leader
- Companies with a specific problem and budget to solve it
- Teams that tried to build in-house and got stuck

---

## 3. AI Operational Efficiency

**Who it's for:** Teams that want AI working in their day-to-day operations — not someday, now.

### Services

- **Process Audit & AI Workflow Design** — Map existing workflows, identify manual bottlenecks, and design AI-augmented replacements. Deliverable: documented workflow redesign with implementation plan.

- **Developer Tooling & SDLC Acceleration** — Set up AI tooling across the development lifecycle: context engineering for agents, automated documentation, release note generation, and more. Model-agnostic — tools are selected based on what's right for the client's stack. Ricardo has direct experience achieving 70% reduction in bug-fix effort and 90% faster technical documentation.

- **Team Enablement & Prompt Engineering** *(one-time)* — A half-day or full-day hands-on workshop for teams. Focused on getting dramatically better results from AI tools they're already paying for. Includes a custom playbook tailored to the team's actual workflows. Best for organizations that want a fast, concrete win.

- **AI Champions Program** *(ongoing)* — A multi-session program that trains 1–3 internal "AI champions" who then scale adoption across the organization. Includes structured sessions over 4–8 weeks, follow-up coaching, and a resource library. Best for organizations that want sustainable, long-term AI capability built internally — not permanent dependency on a consultant.

### Ideal for
- Engineering teams losing time to manual SDLC tasks
- Companies that bought AI tools but adoption is low
- Organizations that want internal AI capability, not permanent dependency on consultants

---

## 4. Fractional CPO / AI Advisor

**Who it's for:** Companies that need senior product leadership embedded part-time — not a consultant dropping off a deck, but an operator who sits inside the work.

### Services

- **Roadmap Development & Prioritization** — Build or overhaul the product roadmap with clear prioritization frameworks tied to business outcomes, not just engineering capacity.

- **AI Integration Strategy** — Define where and how AI fits into the existing product — build vs. buy decisions, model selection, architecture guidance, and phased rollout planning.

- **Team Structure & Process Design** — Evaluate current team structure, identify gaps, and design lightweight processes that let the team ship faster without adding overhead.

- **Stakeholder Alignment** — Own the product narrative with founders, boards, and engineering leads. Translate strategy into language that moves decisions forward.

- **Ongoing Strategic Advisory** — Regular cadence of working sessions (weekly or biweekly) to stay embedded in prioritization, unblock decisions, and keep the roadmap moving.

### Delivery Model
Engagement runs on a monthly retainer. Ricardo attends key meetings, works directly with founders and engineering leads, and is accessible between sessions for async input. Scope scales up or down based on company stage and need. See `services/pricing.md` for retainer tiers.

### Ideal for
- Early-stage startups (0-to-1) that need product operations without a full-time CPO hire
- Series A/B companies adding AI to an existing product
- Organizations where the technical founder needs a strategic product counterpart

---

## Unlisted Services

> These services are not advertised publicly or on sprintt.ai. They are available on a referral or conversation basis only. Do not include in proposals, marketing materials, or client-facing documents unless the client has specifically asked about them.

### Small Business Website Creation

**Who it's for:** Small and local businesses (Freeport/Destin area and beyond) that need a professional web presence, ideally with AI-powered features built in from the start.

**Why it's unlisted:** Website creation is outside Sprintt's core AI consulting positioning. Advertising it publicly risks diluting the brand and attracting low-budget clients who aren't a fit for the primary services.

**When to offer it:**
- Local small business referrals where there's a natural conversation opening
- As a foot-in-the-door that could lead to AI consulting or automation work
- When the client needs both a website and AI features (chatbot, lead capture, booking automation) — bundle and price accordingly

**Services:**
- **Standard website** — 5–10 page professional site, mobile-optimized, built on a modern stack
- **AI-powered website** — same as above, plus at least one AI feature: chatbot, lead capture automation, booking assistant, or content personalization
- **AI landing page** — single high-converting page with AI-driven lead capture or qualification
- **Monthly maintenance** — hosting management, updates, and minor content changes

**Delivery model:** Ricardo scopes and leads. SDLC contractor handles build. Ricardo QAs and delivers.

See `services/pricing.md` for rates.

---

## Design Partner Program

**Special offering for early clients (Q1–Q2 2026)**

Design partners get Sprintt's full capabilities at a significantly reduced rate in exchange for:

1. Honest, detailed feedback on the engagement process
2. A published case study on sprintt.ai upon successful completion (reviewed and approved by the client before publication)
3. A written testimonial cleared for use in proposals and marketing materials
4. A LinkedIn post at project completion — written by the client, tagging Sprintt
5. Permission to display their logo on sprintt.ai
6. A 60-second video testimonial (Loom or equivalent; optional but strongly encouraged)
7. 2–3 warm introductions to contacts in their network who could benefit from Sprintt's services
8. Willingness to take reference calls from prospective clients (up to 3 per year)
9. Flexibility as Sprintt refines its delivery processes

**What design partners receive:**
- 30–50% discount off standard rates
- Direct access to Ricardo (no account managers or handoffs)
- Priority scheduling
- Input on how Sprintt's services evolve

**Limit:** 3 design partners maximum during launch phase.

---

## company/entity.md

# Legal Entity Details

## Business Structure

- **Legal name:** Ramirez Digital Ventures LLC
- **DBA / Trade name:** Sprintt
- **Entity type:** Limited Liability Company (LLC)
- **State of formation:** Florida
- **Status:** Active

## Registered Information

- **Business address:** 57 Riverwalk Cir, Freeport, FL 32439
- **Registered agent:** Ricardo Ramirez, 57 Riverwalk Cir, Freeport, FL 32439
- **EIN:** 41-4857465
- **Florida registration number:** L26000126861

## Ownership

- **Sole Member:** Ricardo Ramirez (100%)
- **Title:** AR (Authorized Representative)

## Contact & Booking

- **Email:** ricardo@sprintt.ai
- **Website:** sprintt.ai
- **Calendly:** https://calendly.com/accounts-sprintt

## How to Use in Documents

When drafting contracts, invoices, NDAs, or any legal document:

- **Full contracting name:** Ramirez Digital Ventures LLC d/b/a Sprintt
- **Short form (after first reference):** "Sprintt" or "the Company"
- **Governing law:** State of Florida
- **Jurisdiction for disputes:** Walton County, Florida (or as negotiated)
- **Signatory:** Ricardo Ramirez, AR

## Tax Information

- **Tax classification:** Single-member LLC, taxed as sole proprietor (disregarded entity — reported on Schedule C of personal return)
- **Fiscal year:** Calendar year (January 1 – December 31)
- **Sales tax:** Florida does not impose sales tax on consulting/professional services. No sales tax collection required unless selling tangible goods or taxable digital products.

## Insurance

- **General liability:** Not yet obtained — PRIORITY: get before first client engagement
- **Professional liability (E&O):** Not yet obtained — PRIORITY: strongly recommended before consulting work begins
- **Cyber liability:** Not yet obtained — evaluate once handling client data or AI systems

## Annual Requirements

- Florida annual report filing (due by May 1 each year via SunBiz — **first filing due May 1, 2027**, not required in year of formation)
- Federal tax return
- Florida does not have a state income tax
- Mercury account maintenance and reconciliation
