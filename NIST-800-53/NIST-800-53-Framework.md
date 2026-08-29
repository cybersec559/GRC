# NIST SP 800-53 Rev 5 — Reference Guide for Security Professionals

A working reference for building, assessing, or authorizing an information system's control
implementation against NIST SP 800-53 Revision 5 (Security and Privacy Controls for Information
Systems and Organizations). Covers the control catalog structure, impact baselines, the Risk
Management Framework (RMF) implementation roadmap, and a cross-mapping to ISO/IEC 27001:2022,
SOC 2, and PCI DSS.

---

## 1. What NIST SP 800-53 Is

- A **comprehensive federal control catalog** published by NIST, providing security and privacy
  controls for federal information systems and organizations — but widely adopted well beyond
  government as a general-purpose control catalog.
- **Foundational to other frameworks and programs:** FedRAMP (cloud service authorization for U.S.
  federal agencies), FISMA (the statutory basis requiring federal systems to be secured), and
  CMMC (Cybersecurity Maturity Model Certification, for the Defense Industrial Base) all build
  their control requirements directly on top of 800-53.
- Organized into **20 control families**, each identified by a two-letter prefix (e.g. `AC` for
  Access Control), with individual controls numbered within each family (e.g. `AC-1`, `AC-2`, …).
- Controls are selected for a given system via **impact baselines** — Low, Moderate, or High —
  based on the system's security categorization under **FIPS 199** (Standards for Security
  Categorization of Federal Information and Information Systems) and implementation guidance in
  **FIPS 200**. A Low-impact system implements a smaller set of controls; a High-impact system
  implements the full baseline plus additional control enhancements.
- Rev 5 (the current revision) made the catalog **outcome-based and platform-independent** —
  controls are written to apply regardless of the type of system, technology, or sector, and
  privacy controls are now fully integrated alongside security controls rather than in a separate
  appendix.

## 2. Scope Note: This Catalog Is Base-Control-Level Only

NIST SP 800-53 Rev 5 is significantly larger in scope than ISO 27001, SOC 2, or PCI DSS: beyond
its roughly 300 **base controls**, the full standard defines **well over a thousand individual
control enhancements** — sub-parts of a base control that add more stringent or specific
requirements (e.g. `AC-2(1)`, `AC-2(2)`, … `AC-2(13)` are all enhancements of the single base
control `AC-2`, Account Management).

To keep this reference suite consistent in scale with its ISO 27001 / SOC 2 / PCI DSS siblings
(which catalog at a comparable single level of granularity), **`controls.csv` in this folder
catalogs only the 302 base controls across all 20 families — it does not itemize control
enhancements.** When a system's baseline requires specific enhancements (Moderate and High
baselines pull in progressively more), consult the published NIST SP 800-53 Rev 5 catalog
(free from NIST) or NIST SP 800-53B (Control Baselines for Information Systems and Organizations)
for the enhancement-level detail.

## 3. The 20 Control Families

| Prefix | Family |
|---|---|
| AC | Access Control |
| AT | Awareness and Training |
| AU | Audit and Accountability |
| CA | Assessment, Authorization, and Monitoring |
| CM | Configuration Management |
| CP | Contingency Planning |
| IA | Identification and Authentication |
| IR | Incident Response |
| MA | Maintenance |
| MP | Media Protection |
| PE | Physical and Environmental Protection |
| PL | Planning |
| PM | Program Management |
| PS | Personnel Security |
| PT | PII Processing and Transparency |
| RA | Risk Assessment |
| SA | System and Services Acquisition |
| SC | System and Communications Protection |
| SI | System and Information Integrity |
| SR | Supply Chain Risk Management |

See `controls.csv` for every base control (Control ID, Family, Title, Description) within each
family.

## 4. Impact Baselines

| Baseline | Applies When | General Characteristic |
|---|---|---|
| Low | Loss of confidentiality, integrity, or availability would have a limited adverse effect | Smallest control set; foundational safeguards |
| Moderate | Loss would have a serious adverse effect | Most common baseline for typical business/mission systems; adds substantially more controls and enhancements |
| High | Loss would have a severe or catastrophic adverse effect | Largest control set; adds the most stringent enhancements, especially around access, audit, and contingency |

A system's baseline is determined by its **FIPS 199 security categorization** — the "high-water
mark" of the confidentiality, integrity, and availability impact ratings across all information
types the system processes, stores, or transmits. The baseline can then be **tailored** (controls
added, scoped, or in limited cases removed with documented justification) to fit the system's
actual risk profile.

## 5. Implementation Roadmap — The Risk Management Framework (RMF)

NIST's RMF (detailed in NIST SP 800-37) is the standard process for applying this catalog to a
real system, end to end:

1. **Prepare** — establish organization-wide risk management roles, a risk management strategy,
   and a common control baseline before working system-by-system.
2. **Categorize** the system — determine the FIPS 199 impact level (Low/Moderate/High) for
   confidentiality, integrity, and availability based on the information types it handles.
3. **Select** the control baseline corresponding to that categorization, and **tailor** it
   (`PL-10`, `PL-11`) — add, scope, or justify removal of controls based on the system's actual
   risk profile.
4. **Implement** the selected controls, documenting the design and deployment of each in the
   **System Security Plan (SSP)**.
5. **Assess** control implementation via a Security Control Assessment (`CA-2`) — an independent
   reviewer (Security Control Assessor) determines whether each control is implemented correctly,
   operating as intended, and producing the desired outcome.
6. **Authorize** — the Authorizing Official reviews the assessment results, the risk register, and
   any open Plan of Action and Milestones (POA&M) items, then issues (or denies) an Authorization
   to Operate (ATO) based on the residual risk (`CA-6`).
7. **Monitor** continuously — ongoing vulnerability scanning, audit log review, configuration
   drift detection, access recertification, and control reassessment keep the authorization
   current rather than treating it as a one-time event (`CA-7`).

Steps 2-4 roughly track "build," step 5 is independent verification, and steps 6-7 are the
authorization decision and its ongoing maintenance — this is why RMF is often described as a
continuous lifecycle rather than a linear project.

## 6. Cross-Mapping to Other Frameworks

Useful when an organization runs NIST 800-53 alongside ISO 27001, SOC 2, or PCI DSS — avoid
rebuilding evidence collection per framework where controls genuinely overlap.

| NIST 800-53 Family | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria | PCI DSS Requirement |
|---|---|---|---|
| AC (Access Control) | A.5.15-A.5.18, A.8.1-A.8.5 | CC6.1-CC6.3 | Req. 7-8 |
| AT (Awareness and Training) | A.6.3 | CC1.4 | Req. 12.6 |
| AU (Audit and Accountability) | A.8.15-A.8.17 | CC7.1-CC7.2 | Req. 10 |
| CA (Assessment, Authorization, and Monitoring) | Clause 9.1-9.2 | CC4.1-CC4.2 | Req. 12.4, 11.4 |
| CM (Configuration Management) | A.8.9, A.8.32 | CC8.1 | Req. 1, 2, 6 |
| CP (Contingency Planning) | A.5.29-A.5.30 | A1.2-A1.3 | Req. 12.10 |
| IA (Identification and Authentication) | A.5.16-A.5.17, A.8.5 | CC6.1 | Req. 8 |
| IR (Incident Response) | A.5.24-A.5.28 | CC7.3-CC7.5 | Req. 12.10 |
| MA (Maintenance) | A.7.13 | CC6.8 | Req. 9.2 |
| MP (Media Protection) | A.7.10 | CC6.5 | Req. 9.4 |
| PE (Physical and Environmental Protection) | A.7.1-A.7.9 | CC6.4 | Req. 9 |
| PL (Planning) | Clause 6, A.5.1 | CC5.1-CC5.3 | Req. 12.1 |
| PM (Program Management) | Clause 5, Clause 9.3 | CC1.1-CC1.5 | Req. 12.4 |
| PS (Personnel Security) | A.6.1-A.6.8 | CC1.4 | Req. 12.7 |
| PT (PII Processing and Transparency) | A.5.34 | P-series (Privacy) | N/A |
| RA (Risk Assessment) | Clause 6.1, A.5.7 | CC3.1-CC3.4 | Req. 12.3 |
| SA (System and Services Acquisition) | A.5.19-A.5.22, A.8.25-A.8.31 | CC8.1 | Req. 6 |
| SC (System and Communications Protection) | A.8.20-A.8.24 | CC6.6-CC6.7 | Req. 1, 3, 4 |
| SI (System and Information Integrity) | A.8.7-A.8.8, A.8.16 | CC7.1-CC7.2 | Req. 5, 6, 11 |
| SR (Supply Chain Risk Management) | A.5.19-A.5.22 | CC9.2 | Req. 12.8-12.9 |

**Practical use:** when responding to an evidence request under any one framework, check this
table for the adjacent NIST 800-53 family — an access review, a penetration test report, or a
change management ticket produced for one framework often satisfies overlapping requests across
all four.

## 7. Templates in This Folder

See `templates/README.md` — the standard GRC template set adapted to RMF terminology, plus two
NIST-specific artifacts with no ISO/SOC2/PCI equivalent: the **Control Implementation Summary**
(NIST's actual pre-authorization tracking document, analogous to but distinct from an ISO
Statement of Applicability) and the **Plan of Action and Milestones (POA&M)**, the formally
required RMF artifact for tracking control weaknesses through remediation.

---
*This is a reference catalog, not a substitute for a formal RMF categorization and tailoring
exercise against your actual system boundary and information types. It itemizes base controls
only — consult the full NIST SP 800-53 Rev 5 standard (available free from NIST) for control
enhancements and complete implementation guidance before treating any control above as sufficient
on its own for a Moderate or High baseline.*
