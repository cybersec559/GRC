# PCI DSS v4.0 — Reference Guide for Security Professionals

A working reference for building, assessing, or auditing against PCI DSS v4.0 (Payment Card
Industry Data Security Standard). Covers the 12 requirements across 6 goals, validation paths
(SAQ vs. ROC), an implementation roadmap, and a cross-mapping to ISO/IEC 27001:2022, SOC 2, and
NIST CSF.

---

## 1. What PCI DSS Is

- A **contractual/industry mandate**, not a law — required by the payment card brands (Visa,
  Mastercard, Amex, Discover, JCB) for any entity that stores, processes, or transmits cardholder
  data.
- **Validation path depends on merchant/service provider level:**
  - **SAQ (Self-Assessment Questionnaire)** — smaller merchants self-attest using the SAQ type
    matching their payment channel (e.g., SAQ A for fully outsourced e-commerce, SAQ D for
    everyone else).
  - **ROC (Report on Compliance)** — larger merchants and all Level 1 service providers require
    an on-site (or remote) assessment by a **QSA (Qualified Security Assessor)**.
- **Scope** is defined by the **CDE (Cardholder Data Environment)** — any system that stores,
  processes, or transmits account data, plus any system connected to or that could impact the
  security of the CDE.
- **v4.0 vs. v3.2.1:** v4.0 (effective, with v3.2.1 fully retired) introduced a **customized
  approach** (meet the security objective via an alternative to the defined requirement, validated
  by risk analysis) alongside the traditional **defined approach**, expanded MFA requirements, and
  new requirements around e-commerce/payment page script integrity (11.6.1) and DNS/malware
  detection.

## 2. The 12 Requirements Across 6 Goals

| Goal | Requirements | Focus |
|---|---|---|
| Build and Maintain a Secure Network and Systems | 1-2 | Network security controls, secure configurations |
| Protect Account Data | 3-4 | Data protection at rest and in transit |
| Maintain a Vulnerability Management Program | 5-6 | Anti-malware, secure development |
| Implement Strong Access Control Measures | 7-9 | Logical access, authentication, physical access |
| Regularly Monitor and Test Networks | 10-11 | Logging, vulnerability scanning, penetration testing |
| Maintain an Information Security Policy | 12 | Policy, risk management, awareness, incident response |

See `controls.csv` for all 63 first-level sub-requirements (e.g., 3.1-3.7) with descriptions.
Each sub-requirement in the actual standard expands further into detailed testing procedures —
this catalog stops at the first level, which is the standard granularity for scoping and tracking
purposes; consult the published PCI DSS v4.0 standard for full testing procedure detail.

## 3. Distinctive PCI DSS Requirements Worth Knowing

- **Quarterly external vulnerability scans** (11.3.1) by an **ASV (Approved Scanning Vendor)** —
  not just "periodic," genuinely required every 90 days, with rescans until passing.
- **Annual + change-triggered penetration testing** (11.4) — both internal and external, with
  segmentation testing every 6 months for service providers relying on network segmentation to
  reduce scope.
- **Compensating controls** — when a requirement can't be met exactly as defined due to a
  documented business/technical constraint, an alternative control providing equivalent protection
  can be used, validated via a **Compensating Controls Worksheet** and assessor sign-off (see
  `templates/Compensating_Controls_Worksheet_Template.csv`).
- **SAD (Sensitive Authentication Data) prohibition** — full track data, CVV/CVC, and PIN/PIN
  block must never be stored post-authorization, even encrypted — this is stricter than PAN
  storage rules.

## 4. Implementation Roadmap

1. **Determine scope** — map all systems storing/processing/transmitting account data and
   everything connected to the CDE.
2. **Determine validation path** — merchant/service provider level → SAQ type or ROC via QSA.
3. **Gap assessment** — compare current state against all 63 sub-requirements.
4. **Remediate gaps**, documenting any compensating controls where a requirement can't be met
   directly.
5. **Complete the PCI DSS Compliance Matrix** — track requirement-by-requirement compliance
   status and evidence.
6. **Quarterly ASV scans** — begin the recurring cadence; four consecutive passing scans are
   typically needed before an initial ROC/SAQ D submission is considered complete evidence.
7. **Annual penetration test** (+ semi-annual segmentation test if applicable).
8. **Submit SAQ + Attestation of Compliance**, or complete ROC with QSA.
9. **Annual re-validation** — PCI DSS compliance is an annual cycle, not a one-time certification.

## 5. Cross-Mapping to Other Frameworks

| PCI DSS Requirement | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria | NIST CSF 2.0 Function |
|---|---|---|---|
| 1-2 (Network/Config) | A.8.20-A.8.22, A.8.9 | CC6.6, CC6.1 | Protect |
| 3-4 (Data Protection) | A.8.24, A.5.12 | C1.1, C1.2 | Protect |
| 5-6 (Vuln Mgmt/Secure Dev) | A.8.7, A.8.8, A.8.25-A.8.29 | CC7.1, CC8.1 | Protect, Identify |
| 7-9 (Access Control) | A.5.15-A.5.18, A.7.1-A.7.4 | CC6.1-CC6.5 | Protect |
| 10-11 (Monitoring/Testing) | A.8.15, A.8.16 | CC7.1-CC7.2 | Detect |
| 12 (Policy/Program) | A.5.1, A.5.31, Clause 6.1 | CC1.1-CC3.4 | Govern, Identify |

**Practical use:** an organization running PCI DSS alongside ISO 27001 or SOC 2 can usually satisfy
overlapping evidence requests (access reviews, pen test reports, log review records) once and
reference the same evidence across all three frameworks' trackers.

## 6. Templates in This Folder

See `templates/README.md` — includes the standard GRC template set plus two PCI-specific
artifacts with no ISO/SOC2 equivalent: the **Compensating Controls Worksheet** and the
**Quarterly ASV Scan & Penetration Test Log**.

---
*This is a reference framework, not a substitute for a formal scoping exercise and QSA guidance.
Confirm your actual validation path (SAQ type vs. ROC) and scope before treating any requirement
above as applicable or not.*
