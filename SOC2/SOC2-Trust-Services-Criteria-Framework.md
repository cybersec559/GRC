# SOC 2 Trust Services Criteria — Reference Guide for Security Professionals

A working reference for building, assessing, or preparing for a SOC 2 audit against the AICPA
Trust Services Criteria (TSC, 2017 framework with 2022 points-of-focus revisions). Covers report
types, the Common Criteria (Security) plus the four optional Trust Service Categories, an
implementation roadmap, and a cross-mapping to ISO/IEC 27001:2022, NIST CSF, and PCI DSS.

---

## 1. What SOC 2 Is (and Isn't)

- SOC 2 is an **attestation** report issued by a licensed CPA firm, not a certification like
  ISO 27001. There's no "SOC 2 certified" badge — you receive a report describing your controls
  and the auditor's opinion on them.
- **Type I** — a point-in-time assessment: are controls suitably designed as of a specific date?
- **Type II** — an assessment over a period (typically 3–12 months): were controls designed
  *and operating effectively* throughout that period? Type II is what most enterprise customers
  actually require in vendor due diligence.
- **Trust Service Categories** — five possible categories; **Security is mandatory** for every
  SOC 2 report (also called the "Common Criteria," CC-series). The other four
  (Availability, Processing Integrity, Confidentiality, Privacy) are optional and selected based
  on what your service commits to customers. Most SaaS companies scope Security + Availability
  at minimum.
- **Privacy criteria note:** the AICPA's 2022 update separated Privacy from the core TSC package
  — if Privacy is in scope, confirm with your auditor which current privacy criteria set applies
  rather than assuming the older P-series criteria still governs unchanged.

## 2. Common Criteria (Security) — Mandatory, 33 Points of Focus Across 9 Series

Modeled on the COSO Internal Control Framework's five components.

| Series | COSO Component | # Controls | Focus |
|---|---|---|---|
| CC1 | Control Environment | 5 | Tone at the top, org structure, competence, accountability |
| CC2 | Communication and Information | 3 | Internal/external communication of control-relevant info |
| CC3 | Risk Assessment | 4 | Objective-setting, risk identification, fraud consideration |
| CC4 | Monitoring Activities | 2 | Ongoing/separate control evaluations, deficiency reporting |
| CC5 | Control Activities | 3 | Selecting/deploying controls, technology general controls |
| CC6 | Logical and Physical Access Controls | 8 | Access provisioning, boundary protection, malware, disposal |
| CC7 | System Operations | 5 | Vulnerability/anomaly detection, incident response, recovery |
| CC8 | Change Management | 1 | Authorized, tested, approved changes |
| CC9 | Risk Mitigation | 2 | Business disruption planning, vendor/partner risk management |

See `controls.csv` for every individual criterion (CC1.1–CC9.2) with its full description.

## 3. Additional (Optional) Trust Service Categories

| Category | Code | # Controls | Focus |
|---|---|---|---|
| Availability | A1 | 3 | Capacity management, environmental/backup/recovery infrastructure, recovery testing |
| Confidentiality | C1 | 2 | Identifying and disposing of confidential information |
| Processing Integrity | PI1 | 5 | Complete, accurate, timely, authorized system input/processing/output/storage |

Scope these in only if your service actually makes commitments in these areas (e.g., an uptime
SLA justifies Availability; a payments platform almost always needs Processing Integrity).

## 4. Implementation Roadmap

1. **Scope the report** — which systems/services are in scope, and which Trust Service
   Categories beyond mandatory Security.
2. **Readiness assessment** — gap analysis against the applicable criteria; identify missing
   policies, controls, and evidence.
3. **Remediate gaps** — implement missing controls (access reviews, logging, change management,
   vendor risk process, etc.).
4. **Build the controls matrix** — map each in-scope criterion to your actual control
   implementation and evidence source (see `templates/TSC_Controls_Matrix_Template.csv`).
5. **Type I audit** (optional but common first step) — auditor evaluates control design as of a
   point in time.
6. **Observation period** — typically 3–12 months of operating the controls with evidence
   generated continuously (not backfilled).
7. **Type II audit** — auditor samples evidence across the observation period and tests
   operating effectiveness.
8. **Report delivery** — SOC 2 report issued (restricted-use, shared under NDA with
   customers/prospects, not published publicly).
9. **Annual renewal** — most organizations run a new Type II observation period every 12 months,
   overlapping with the prior period's end.

## 5. Cross-Mapping to Other Frameworks

Useful when an organization runs SOC 2 alongside ISO 27001, PCI DSS, or NIST CSF — avoid
duplicating evidence collection where criteria genuinely overlap.

| SOC 2 Series | ISO/IEC 27001:2022 Annex A theme | NIST CSF 2.0 function | Overlaps heavily with |
|---|---|---|---|
| CC1 (Control Environment) | Organizational (A.5.1-A.5.5) | Govern | PCI DSS Req. 12 |
| CC2 (Communication) | Organizational (A.5.1, A.5.36) | Govern | PCI DSS Req. 12.6 |
| CC3 (Risk Assessment) | Organizational (A.5.7, Clause 6.1) | Identify | PCI DSS Req. 12.3 |
| CC4 (Monitoring) | Organizational (A.5.35, A.5.36) | Detect | PCI DSS Req. 12.10 |
| CC5 (Control Activities) | Organizational (A.5.1, A.5.37) | Govern, Protect | — |
| CC6 (Access Controls) | Technological (A.8.1-A.8.5), Physical (A.7.1-A.7.4) | Protect | PCI DSS Req. 7-8-9 |
| CC7 (System Operations) | Technological (A.8.15, A.8.16), Organizational (A.5.24-A.5.28) | Detect, Respond, Recover | PCI DSS Req. 10, 12.10 |
| CC8 (Change Management) | Technological (A.8.32) | Protect | PCI DSS Req. 6 |
| CC9 (Risk Mitigation) | Organizational (A.5.19-A.5.22, A.5.29-A.5.30) | Identify, Recover | PCI DSS Req. 12.8-12.9 |
| A1 (Availability) | Technological (A.8.14), Organizational (A.5.29-A.5.30) | Recover | PCI DSS Req. 12.10.1 |
| C1 (Confidentiality) | Organizational (A.5.12, A.5.34), Technological (A.8.10) | Protect | PCI DSS Req. 3-4 |
| PI1 (Processing Integrity) | Technological (A.8.25-A.8.29) | Protect | PCI DSS Req. 6 |

**Practical use:** when responding to an evidence request under any one framework, check this
table for the adjacent SOC 2 criterion — the same access review, pen test report, or change
ticket often satisfies multiple frameworks' requests at once.

## 6. Templates in This Folder

See `templates/README.md` for the full set — adapted from the generic ISMS templates to SOC 2's
own terminology (e.g. "control exceptions" rather than ISO's "nonconformities," a Trust Services
Criteria controls matrix rather than a Statement of Applicability).

---
*This is a reference framework, not a substitute for a formal readiness assessment against your
actual in-scope systems and Trust Service Category selections. Confirm criteria applicability with
your auditor before treating any control above as mandatory or non-applicable.*
