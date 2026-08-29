# CCPA/CPRA — Reference Guide for Security/Privacy Professionals

A working reference for building, assessing, or auditing a privacy program against the California
Consumer Privacy Act as amended by the California Privacy Rights Act (CCPA/CPRA, California Civil
Code § 1798.100 et seq.). Covers applicability, key roles, the core obligations/rights catalog, an
implementation roadmap, and a cross-mapping to other frameworks commonly run in parallel (GDPR,
ISO/IEC 27001:2022, SOC 2).

---

## 1. What CCPA/CPRA Is

- A **California state law** — not a federal statute, and not an industry mandate like PCI DSS.
  The CPRA (effective January 1, 2023) substantially amended the original 2018 CCPA, adding new
  consumer rights, a new "Sensitive Personal Information" category, and a dedicated regulator (the
  CPPA).
- **Applicability is threshold-based, not location-based.** Like GDPR's extraterritorial reach, a
  business does not need to be headquartered or incorporated in California to be covered — it only
  needs to do business in California, collect California residents' personal information, and meet
  at least one of three thresholds: (1) over $25M in annual gross revenue, (2) annually buys, sells,
  or shares the personal information of 100,000+ California consumers or households, or (3) derives
  50%+ of annual revenue from selling or sharing personal information. Any organization meeting a
  threshold is in scope regardless of where its servers, staff, or headquarters are located.
- **Consumer** means a natural person who is a California resident — the law protects individuals,
  not organizations, and (since CPRA) covers both consumer-facing and employee/B2B personal
  information (the original CCPA's temporary employee/B2B exemptions expired January 1, 2023).

## 2. Key Roles

| Role | Definition | Practical Distinction |
|---|---|---|
| **Business** | For-profit entity that determines the purposes and means of processing and meets an applicability threshold. | The accountable party — owns notice, rights-handling, and contract obligations. |
| **Service Provider** | Processes personal information on the business's behalf, under contract, for a business purpose; barred from using data for its own purposes. | Classic "processor" analog — collects/receives data *on behalf of* the business. |
| **Contractor** (CPRA-added) | Receives personal information *made available by* the business under contract, subject to similar use restrictions as a Service Provider. | Distinguished by data flow direction, not by risk profile — contract terms are nearly identical to a Service Provider's. |
| **Third Party** | Any recipient of personal information that is not the business, a Service Provider, or a Contractor. | Receiving data as a Third Party (for consideration, or for cross-context behavioral advertising) is what triggers "sale" or "sharing" classification and opt-out rights. |
| **Consumer** | A natural person who is a California resident. | The rights-holder — not "data subject" (GDPR's term), but the same underlying concept. |

## 3. Core Obligations and Consumer Rights Catalog

See `controls.csv` for the full flat reference catalog (37 entries: Ref, Category, Title,
Description), organized into these categories:

| Category | Covers |
|---|---|
| Consumer Rights | Right to know/access, delete, correct, opt-out of sale/sharing, limit use of sensitive PI, non-discrimination, data portability. |
| Business Obligations | Notice at collection, privacy policy, "Do Not Sell or Share" link, opt-out preference signal honoring, verification of requests, 45-day response timelines, designated request methods. |
| Roles & Definitions | Business, Service Provider, Contractor, Third Party, Sale, Sharing, exemptions. |
| Sensitive Personal Information | The CPRA-added SPI category and the associated use-limitation notice. |
| Data Minimization | Purpose limitation and retention-period requirements (CPRA-added principles). |
| Service Provider / Contractor / Third Party Contracts | Required contract terms distinguishing each role. |
| Risk Assessment & Cybersecurity Audits (CPRA) | Annual independent cybersecurity audits and periodic risk assessments for high-risk processing, plus emerging ADMT (automated decision-making technology) rulemaking. |
| Enforcement | Private right of action for data breaches, CPPA/AG administrative enforcement, preemption, waiver prohibition. |

## 4. Implementation Roadmap

1. **Applicability threshold check** — determine whether the organization meets any of the three
   CCPA/CPRA thresholds (revenue, data volume, or data-sale revenue share). Do this before anything
   else; a large share of "do we need to comply" confusion traces back to skipping this step.
2. **Data mapping** — inventory categories of personal information collected, sources, purposes,
   retention periods, and downstream recipients (see `templates/Personal_Information_Inventory_Template.csv`).
3. **Privacy policy and notice-at-collection updates** — align public-facing disclosures with the
   data map; confirm the privacy policy is reviewed/republished at least every 12 months.
4. **Opt-out mechanism implementation** — implement the "Do Not Sell or Share My Personal
   Information" (or "Your Privacy Choices") link and honor recognized opt-out preference signals
   (e.g., Global Privacy Control) as a valid opt-out request.
5. **Vendor contract updates** — classify each recipient as Service Provider, Contractor, or Third
   Party, and confirm contracts contain the role-appropriate required terms.
6. **Consumer request handling process** — stand up intake, identity verification, and the 45-day
   (extendable to 90-day) response workflow (see `templates/Consumer_Request_Log.csv`).
7. **Risk assessment / cybersecurity audit program** — if processing presents significant risk to
   consumer privacy or security under CPPA regulations, stand up the recurring independent
   cybersecurity audit and risk assessment cadence (see
   `templates/Cybersecurity_Audit_and_Risk_Assessment_Log.csv`).

## 5. Cross-Mapping to Other Frameworks

Useful when an organization runs CCPA/CPRA alongside GDPR, ISO 27001, or SOC 2 — many concepts
overlap conceptually but differ in legal mechanics, so evidence can often be reused even where the
underlying legal test is not identical.

| CCPA/CPRA Concept | GDPR Analog | Key Mechanical Difference |
|---|---|---|
| Business | Controller | GDPR has no revenue/volume threshold; CCPA/CPRA applicability is threshold-gated. |
| Service Provider / Contractor | Processor | GDPR uses one processor concept; CCPA/CPRA splits it into two roles based on data flow direction. |
| Third Party (sale/sharing) | Third-party recipient / further transfer | GDPR's controller-to-controller transfer concept doesn't map cleanly to "sale" or "sharing," which are CCPA/CPRA-specific triggers. |
| Right to know/access, delete, correct, portability | Right of access, erasure, rectification, portability | Broadly equivalent consumer/data-subject rights, but response windows differ (45 days vs. GDPR's 1 month, each independently extendable). |
| Right to opt-out of sale/sharing | Right to object / withdraw consent | CCPA/CPRA's opt-out model is closer to an always-available objection right than to GDPR's consent-withdrawal model. |
| Sensitive Personal Information | Special category data | Category lists overlap heavily but are not identical (e.g., CCPA/CPRA includes precise geolocation and financial account credentials explicitly). |
| Risk assessments / cybersecurity audits (CPRA) | Data Protection Impact Assessment (DPIA) | Conceptually similar risk-based assessment obligation; CPRA additionally requires a periodic independent cybersecurity audit with no direct GDPR equivalent. |
| CPPA | Supervisory Authority (e.g., a national DPA) | Both are dedicated privacy regulators, but the CPPA is state-level (California only) while GDPR supervisory authorities operate under an EU-wide cooperation mechanism. |

| CCPA/CPRA Category | ISO/IEC 27001:2022 | SOC 2 |
|---|---|---|
| All privacy obligations, broadly | A.5.34 (Privacy and protection of PII) | Privacy (optional Trust Service Category, separated from the core TSC package in the AICPA's 2022 update — confirm with your auditor which current criteria set applies if Privacy is in scope). |
| Data minimization / retention | A.8.10 (Information deletion), A.5.12 (Classification) | C1.1-C1.2 (Confidentiality) |
| Vendor/contract requirements | A.5.19-A.5.22 (Supplier relationships) | CC9.2 (Risk Mitigation) |
| Cybersecurity audits / risk assessments | Clause 6.1 (Risk assessment), A.5.35 (Independent review) | CC3.1-CC3.4 (Risk Assessment) |
| Data breach handling | A.5.24-A.5.28 (Incident management) | CC7.3-CC7.5 (System Operations) |

**Practical use:** an organization running CCPA/CPRA alongside ISO 27001 or SOC 2 can often reuse
the same access reviews, incident response records, and vendor risk assessments to support both an
information-security framework's evidence requests and a CCPA/CPRA compliance file — but the legal
tests (e.g., "sale," "sharing," applicability thresholds) still need independent evaluation; they
are not satisfied merely by having a mapped security control in place.

## 6. Templates in This Folder

See `templates/README.md` for the full set, including two CCPA-specific artifacts with no direct
ISO/SOC2/PCI equivalent: the **Personal Information Inventory** (replacing a generic asset
inventory) and the **Consumer Request Log** (tracking the 45-day statutory response clock), plus a
CPRA-specific **Cybersecurity Audit and Risk Assessment Log**.

---
*This is a reference framework, not legal advice. CCPA/CPRA applicability, exemptions, and
obligations depend on specific facts (the categories of personal information involved, the
organization's revenue and data-processing volume, and evolving CPPA regulations). Consult
qualified privacy counsel before treating any item above as determinative for your organization.*
