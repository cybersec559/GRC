# HIPAA Security Rule (and Privacy Rule) — Reference Guide for Security Professionals

A working reference for building, assessing, or auditing a HIPAA security and privacy compliance
program against the HHS Security Rule (45 CFR Part 160 and Subparts A/C of Part 164), the
Privacy Rule (Subpart E), and the Breach Notification Rule (Subpart D). Covers the Required vs.
Addressable distinction, the Security Rule's three safeguard categories, an implementation
roadmap, and a cross-mapping to other frameworks commonly run in parallel (ISO/IEC 27001:2022,
SOC 2, PCI DSS).

---

## 1. What HIPAA Is (and Isn't)

- HIPAA (the Health Insurance Portability and Accountability Act of 1996, as amended by HITECH
  in 2009) is a **US federal law**, enforced by the HHS Office for Civil Rights (OCR) — it is
  **not** an industry certification like ISO/IEC 27001, and there is no "HIPAA-certified" badge
  or accredited third-party audit that results in a portable certificate.
- Compliance is a continuous legal obligation, not a point-in-time attestation. OCR enforces
  through complaint investigations, breach reports, and periodic compliance audits, with civil
  penalties tiered by culpability and, for willful neglect, potential criminal referral.
- **Who it applies to:**
  - **Covered Entities** — health plans, health care clearinghouses, and health care providers
    who transmit health information electronically in connection with a HIPAA transaction.
  - **Business Associates** — any person or entity that creates, receives, maintains, or
    transmits PHI on behalf of a covered entity (e.g. cloud hosting providers, billing services,
    IT support vendors, data analytics firms) — HITECH extended direct Security Rule liability
    to business associates, not just covered entities.
  - **Subcontractors of business associates** are, in turn, treated as business associates and
    carry the same obligations down the chain.
- **Scope of the Security Rule:** protects **ePHI** (electronic Protected Health Information) —
  PHI that is created, received, maintained, or transmitted in electronic form. The Privacy Rule
  is broader and covers PHI in any form (electronic, paper, oral).

## 2. Required vs. Addressable — What It Actually Means

Every Security Rule implementation specification is designated **Required** or **Addressable**.
This is a Security Rule–specific concept; it does not apply to the Privacy Rule or Breach
Notification Rule, whose provisions are simply mandatory.

- **Required** — must be implemented as specified. No flexibility.
- **Addressable does NOT mean optional.** For each addressable specification, an organization
  must do one of the following, and document the decision:
  1. **Implement the specification as written**, if reasonable and appropriate given the
     organization's risk analysis; or
  2. **Implement an equivalent alternative measure** that achieves the same protective purpose,
     if the specification itself is not reasonable and appropriate; or
  3. **Document why neither the specification nor an equivalent alternative is reasonable and
     appropriate**, if the corresponding risk is sufficiently low or otherwise mitigated — this
     is the narrowest path and should be rare, well-justified, and revisited as the risk
     analysis is updated.
- What is "reasonable and appropriate" depends on the organization's size, complexity,
  technical infrastructure, costs, and the risk analysis's findings — this is why the Security
  Rule is often called "flexible and scalable" rather than prescriptive.
- **Auditors and OCR investigators will ask for the documentation behind every addressable
  decision** — an addressable specification with no risk analysis, no documented rationale, and
  no compensating control is treated as a gap, not a pass.

## 3. The Security Rule's Safeguard Categories

| Category | 45 CFR Citation | # Rows in `controls.csv` | Focus |
|---|---|---|---|
| Administrative Safeguards | §164.308 | 23 | Risk analysis/management, workforce security, access management, security awareness training, incident procedures, contingency planning, evaluation, business associate oversight |
| Physical Safeguards | §164.310 | 10 | Facility access controls, workstation use/security, device and media controls (disposal, re-use, accountability, backup) |
| Technical Safeguards | §164.312 | 9 | Access control, audit controls, integrity, person/entity authentication, transmission security |
| Organizational Requirements | §164.314 | 3 | Business associate contract terms, group health plan document requirements |
| Policies, Procedures & Documentation | §164.316 | 4 | Written policies, six-year retention, availability, periodic updates |

See `controls.csv` for every individual standard and implementation specification (58 rows total,
including 8 Privacy Rule rows and 1 Breach Notification Rule row — see Section 6).

## 4. Implementation Roadmap

1. **Risk analysis** (§164.308(a)(1)(i)) — the foundational, Required starting point for
   everything else. Identify all systems, applications, and locations that create, receive,
   maintain, or transmit ePHI; identify threats and vulnerabilities; assess likelihood and
   impact. Every other decision in the program (which addressable specs to implement as written,
   which BAs are highest-risk, where to prioritize remediation) traces back to this document.
2. **Gap remediation** — compare current state against every standard and implementation
   specification in `controls.csv`; for Required items, close the gap directly; for Addressable
   items, decide implement / equivalent alternative / documented non-implementation per Section 2.
3. **Policies and procedures** (§164.316(a)) — formalize the safeguards chosen above into written
   policy, sized to organizational complexity; assign an Assigned Security Responsibility owner
   (§164.308(a)(2)) and, in practice, a Privacy Officer for Privacy Rule obligations.
4. **Workforce training** (§164.308(a)(5)(i)) — security awareness training and periodic
   reminders for all workforce members with ePHI access, plus role-specific training for
   privacy-facing roles (minimum necessary, individual rights processes).
5. **Business Associate Agreements** (§164.308(b)(1), §164.314(a)(1)) — inventory every business
   associate and subcontractor with ePHI access; execute a BAA before any ePHI flows; track
   renewal/review dates (see `templates/Business_Associate_Agreement_Register.csv`).
6. **Ongoing evaluation** (§164.308(a)(8)) — periodic technical and nontechnical evaluation,
   re-triggered by environmental or operational changes (new systems, new regulations, incidents,
   mergers); feed findings back into the risk analysis, closing the loop.

Layered throughout: **security incident procedures** (§164.308(a)(6)(i)) and the **Breach
Notification Rule's 60-day clock** (§164.400-414) for any breach of unsecured PHI, and
**contingency planning** (§164.308(a)(7)) so ePHI availability survives disruptions.

## 5. Cross-Mapping to Other Frameworks

Useful when an organization runs HIPAA alongside ISO 27001, SOC 2, or PCI DSS — avoid rebuilding
evidence collection per framework where controls genuinely overlap. (Note: HIPAA's ePHI scope and
PCI DSS's cardholder data scope are legally distinct — an organization handling both payment card
data and ePHI needs both programs; the mapping below is about reusable evidence, not substitution.)

| HIPAA Safeguard Category | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria | PCI DSS Requirement |
|---|---|---|---|
| Administrative — Risk Analysis/Management (164.308(a)(1)) | Clause 6.1, A.5.7 | CC3.1-CC3.4 | Req. 12.3 |
| Administrative — Workforce Security/Sanctions (164.308(a)(3), (a)(1)(iii)) | A.6.1, A.6.4, A.6.5 | CC1.4, CC1.5 | Req. 12.7 |
| Administrative — Security Awareness Training (164.308(a)(5)) | A.6.3 | CC1.4 | Req. 12.6 |
| Administrative — Security Incident Procedures (164.308(a)(6)) | A.5.24-A.5.28 | CC7.3-CC7.5 | Req. 12.10 |
| Administrative — Contingency Plan (164.308(a)(7)) | A.5.29, A.5.30 | CC9.1, A1.2, A1.3 | Req. 12.10 (supporting) |
| Administrative — BA/Vendor Oversight (164.308(b), 164.314(a)) | A.5.19-A.5.22 | CC9.2 | Req. 12.8, 12.9 |
| Physical — Facility/Workstation/Media Controls (164.310) | A.7.1-A.7.14 | CC6.4 | Req. 9 |
| Technical — Access Control (164.312(a)) | A.5.15-A.5.18, A.8.2-A.8.3 | CC6.1-CC6.3 | Req. 7-8 |
| Technical — Audit Controls (164.312(b)) | A.8.15, A.8.16 | CC7.1-CC7.2 | Req. 10 |
| Technical — Transmission Security/Encryption (164.312(e)) | A.8.24 | C1.1 | Req. 4 |
| Organizational — Policies & Documentation (164.316) | Clause 7.5, A.5.1, A.5.37 | CC5.3 | Req. 12.1 |
| Privacy Rule — Minimum Necessary, NPP, Individual Rights | A.5.34 | C1.1, C1.2 | — |
| Breach Notification Rule (164.400-414) | A.5.24-A.5.28 | CC7.4-CC7.5 | Req. 12.10 |

**Practical use:** an access review, a workforce security awareness session, or an incident
response record often satisfies the equivalent request under two or three frameworks at once —
check this table before re-collecting evidence you already have.

## 6. Templates in This Folder

See `templates/README.md` — 18 fillable templates adapted to HIPAA's terminology, including two
HIPAA-specific artifacts with no direct ISO/SOC2/PCI equivalent: a **Business Associate Agreement
Register** (tracking BAA execution/renewal per business associate, replacing the generic
vendor risk register given HIPAA's specific legal BAA requirement) and a **Contingency Plan Test
Log** using HIPAA's own terms (Data Backup Plan, Disaster Recovery Plan, Emergency Mode Operation
Plan). The Incident Management Tracker also carries fields for breach determination and the
60-day notification clock.

---
*This is a reference framework, not a substitute for a formal risk analysis against your actual
systems, workforce, and business associate relationships, or for qualified legal counsel on
HIPAA applicability and breach determinations. Validate every Required/Addressable decision
above against your organization's own risk analysis before treating any item as satisfied,
not applicable, or safely deferred.*
