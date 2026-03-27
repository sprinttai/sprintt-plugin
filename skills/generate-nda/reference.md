# Reference — Generate NDA

## legal/templates/nda.md

# MUTUAL NON-DISCLOSURE AGREEMENT

**Effective Date:** [DATE]

This Mutual Non-Disclosure Agreement ("Agreement") is entered into by and between:

**Party A:** Ramirez Digital Ventures LLC d/b/a Sprintt ("Sprintt")
- Address: 57 Riverwalk Cir, Freeport, FL 32439
- Contact: Ricardo Ramirez, AR
- Email: ricardo@sprintt.ai

**Party B:** [CLIENT LEGAL NAME] ("[CLIENT SHORT NAME]")
- Address: [CLIENT ADDRESS]
- Contact: [CLIENT CONTACT NAME], [TITLE]
- Email: [CLIENT EMAIL]

Collectively referred to as the "Parties" and individually as a "Party."

---

## 1. PURPOSE

The Parties wish to explore a potential business relationship related to [BRIEF DESCRIPTION OF PURPOSE, e.g., "AI consulting and technology implementation services"] (the "Purpose"). In connection with this Purpose, each Party may disclose certain confidential and proprietary information to the other Party.

## 2. DEFINITION OF CONFIDENTIAL INFORMATION

"Confidential Information" means any and all non-public information disclosed by either Party to the other Party, whether orally, in writing, electronically, or by any other means, including but not limited to:

(a) Business plans, strategies, forecasts, and financial information;
(b) Customer and client lists, data, and relationships;
(c) Technical data, trade secrets, know-how, inventions, and processes;
(d) Software, code, algorithms, models, and system architectures;
(e) Marketing strategies, pricing information, and proposals;
(f) Employee and contractor information;
(g) Any information marked as "confidential," "proprietary," or with a similar designation. Unmarked information shared in a context that reasonably implies confidentiality is also covered.

## 3. EXCLUSIONS

Confidential Information does not include information that:

(a) Is or becomes publicly available without breach of this Agreement;
(b) Was known to the receiving Party prior to disclosure, as demonstrated by written records;
(c) Is independently developed by the receiving Party without use of the disclosing Party's Confidential Information;
(d) Is lawfully obtained from a third party without restriction on disclosure;
(e) Is required to be disclosed by law, regulation, or court order, provided the receiving Party gives prompt written notice to the disclosing Party and cooperates in seeking protective treatment.

## 4. OBLIGATIONS

Each Party agrees to:

(a) Hold the other Party's Confidential Information in strict confidence;
(b) Not disclose Confidential Information to any third party without prior written consent of the disclosing Party;
(c) Use Confidential Information solely for the Purpose described in Section 1;
(d) Limit access to Confidential Information to those employees, contractors, or advisors who need to know and who are bound by obligations of confidentiality at least as protective as this Agreement;
(e) Protect Confidential Information with at least the same degree of care used to protect its own confidential information, but in no event less than reasonable care.

## 5. TERM AND TERMINATION

This Agreement shall remain in effect for a period of **[NDA_TERM_YEARS]** from the Effective Date, unless terminated earlier by either Party with [NDA_TERMINATION_NOTICE_DAYS]' written notice. The obligations of confidentiality shall survive termination for a period of **[NDA_SURVIVAL_YEARS]** from the date of termination.

## 6. RETURN OR DESTRUCTION OF MATERIALS

Upon termination of this Agreement or upon written request by the disclosing Party, the receiving Party shall promptly return or destroy all Confidential Information and any copies thereof, and shall confirm such return or destruction in writing within [NDA_RETURN_DESTROY_DAYS].

## 7. RESIDUAL KNOWLEDGE

Nothing in this Agreement prevents either Party from using general knowledge, skills, experience, ideas, concepts, techniques, or know-how retained in unaided memory that is incidentally acquired through the relationship contemplated by this Agreement, provided such use does not constitute a disclosure of the other Party's Confidential Information and does not involve copying or using any specific materials, documents, or data belonging to the disclosing Party.

## 8. NO LICENSE OR OBLIGATION

Nothing in this Agreement grants either Party any rights to the other Party's Confidential Information except as expressly stated herein. This Agreement does not obligate either Party to enter into any further agreement or business relationship.

## 9. REMEDIES

Each Party acknowledges that a breach of this Agreement may cause irreparable harm for which monetary damages would be insufficient. The disclosing Party shall be entitled to seek equitable relief, including injunction and specific performance, in addition to any other remedies available at law or in equity.

## 10. GOVERNING LAW AND JURISDICTION

This Agreement shall be governed by and construed in accordance with the laws of the **State of Florida**, without regard to its conflict of laws principles. Any disputes arising under this Agreement shall be resolved in the courts of **Walton County, Florida**, and each Party consents to the personal jurisdiction of such courts. The prevailing Party in any litigation arising under this Agreement shall be entitled to recover reasonable attorneys' fees and costs.

## 11. MISCELLANEOUS

(a) **Entire Agreement:** This Agreement constitutes the entire agreement between the Parties regarding the subject matter hereof and supersedes all prior negotiations, representations, or agreements.
(b) **Amendments:** This Agreement may only be modified by written agreement signed by both Parties.
(c) **Assignment:** Neither Party may assign this Agreement without the prior written consent of the other Party, except that Sprintt may assign this Agreement in connection with a merger, acquisition, or sale of substantially all of its assets. Any attempted assignment in violation of this Section is void.
(d) **Severability:** If any provision of this Agreement is held to be unenforceable, the remaining provisions shall remain in full force and effect.
(e) **Counterparts:** This Agreement may be executed in counterparts, including electronic signatures, each of which shall be deemed an original.
(f) **Notices:** Written notices shall be sent to the addresses listed above, or as updated in writing by either Party. Email is acceptable for routine communications; material notices (termination, breach) require written confirmation.
(g) **Waiver:** Failure by either Party to enforce any provision of this Agreement on one occasion shall not constitute a waiver of that Party's right to enforce such provision on any future occasion.

---

## SIGNATURES

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
