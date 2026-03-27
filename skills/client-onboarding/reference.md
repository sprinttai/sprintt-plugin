# Reference — Client Onboarding

## operations/client-onboarding.md

# Client Onboarding Checklist

Use this checklist for every new client engagement.

## Pre-Kickoff (within 48 hours of signed agreement)

- [ ] Agreement fully executed (both parties signed)
- [ ] First payment received in Mercury
- [ ] NDA executed (if separate from main agreement)
- [ ] Client point of contact confirmed (name, email, phone)
- [ ] Communication channel established (email, Slack Connect, or client's preferred tool)
- [ ] Kickoff meeting scheduled (within 1 week of signed agreement)
- [ ] Internal project folder created (Google Drive: Clients/[ClientName]/[ProjectName])
- [ ] SOW saved to project folder
- [ ] Client added to revenue tracking in `company/finances.md`

## Kickoff Meeting

- [ ] Introductions and roles confirmed
- [ ] SOW reviewed — scope, milestones, and timeline confirmed
- [ ] Access requirements identified (systems, data, tools)
- [ ] Communication cadence agreed upon (weekly calls, async updates, etc.)
- [ ] Feedback and approval process confirmed
- [ ] Questions and concerns addressed
- [ ] Meeting notes sent within 24 hours

## Post-Kickoff (within first week)

- [ ] All access credentials / system invitations received
- [ ] Initial data or documentation received from client
- [ ] Project timeline with milestones shared with client
- [ ] First status update sent
- [ ] Any blockers identified and communicated

## Ongoing Throughout Engagement

- [ ] Weekly status updates sent (even if brief)
- [ ] Milestone deliverables submitted on schedule
- [ ] Scope changes documented and approved in writing
- [ ] Invoices sent per payment schedule in SOW
- [ ] Payments received and confirmed

## Closeout

- [ ] All deliverables accepted by client
- [ ] Final invoice sent and paid
- [ ] Handoff documentation provided (if applicable)
- [ ] Testimonial requested
- [ ] Case study discussion initiated (design partners)
- [ ] Referral conversation had
- [ ] 30-day follow-up check-in scheduled
- [ ] Project archived in Google Drive
- [ ] Lessons learned noted for internal improvement

---

## operations/workflows.md

# Operational Workflows

## Lead-to-Client Pipeline

### Stage 1: Awareness
- Prospect discovers Sprintt via LinkedIn, website, referral, or local event
- **Action:** Content marketing, networking, referral partnerships

### Stage 2: Discovery
- Prospect reaches out (email, website form, DM, or referral introduction)
- **Action within 24 hours:**
  - Acknowledge receipt
  - Send calendar link for a 30-minute discovery call
  - Brief review of their business/website before the call

### Stage 3: Discovery Call (30 min)
- Understand their business, challenges, and what they've tried
- Assess fit (do they match an ICP? do they have budget?)
- Explain how Sprintt works — no hard selling
- If good fit: propose next step (assessment, workshop, or scoping session)
- If not a fit: recommend a resource or alternative and part graciously
- **Deliverable:** Brief follow-up email summarizing the conversation and proposed next steps

### Stage 4: Proposal
- Draft a proposal based on discovery call findings
- Include: project overview, scope, timeline, investment, and terms
- Reference `services/pricing.md` for rate card
- For design partners: include Design Partner Agreement
- For standard clients: include Consulting Agreement + SOW
- **Send within 3 business days** of the discovery call

### Stage 5: Negotiation & Close
- Address questions, adjust scope/pricing if needed
- Get signatures on agreement(s) — use e-signature (DocuSign free tier or similar)
- Collect first payment per SOW terms
- **Handoff to onboarding**

### Stage 6: Onboarding
- Follow `operations/client-onboarding.md` checklist
- Set up project communication channel
- Schedule kickoff meeting

### Stage 7: Delivery
- Execute per SOW milestones
- Regular check-ins (weekly minimum)
- Milestone reviews and approvals
- Track scope changes

### Stage 8: Closeout
- Final deliverable review and sign-off
- Collect final payment
- Request testimonial and case study participation
- Ask for referrals
- Schedule 30-day follow-up check-in

---

## Project Delivery Standards

- **Response time:** Respond to client messages within 4 business hours
- **Meeting prep:** Always have an agenda, always send notes after
- **Deliverable format:** Clean, documented, and accompanied by a brief explanation
- **Scope changes:** Always documented in writing before work begins
- **Status updates:** Weekly at minimum, more frequently for active build phases

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
