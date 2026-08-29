# NIST Cybersecurity Framework (CSF) 2.0 — Reference Guide for Security Professionals

A working reference for building, assessing, or maturing a cybersecurity risk management program
against the NIST Cybersecurity Framework 2.0 (NIST CSWP 29, released February 2024). Covers the
six Functions and their Categories/Subcategories, the Profile/Tier model, an implementation
roadmap, and a cross-mapping to other frameworks commonly run in parallel (ISO/IEC 27001:2022,
SOC 2, PCI DSS).

---

## 1. What NIST CSF 2.0 Is (and Isn't)

- CSF is a **voluntary framework**, not a certification and not a checklist of mandatory controls.
  There is no "CSF certified" status and no accredited external audit — organizations use it to
  organize, communicate, and improve their own cybersecurity risk management.
- CSF 2.0 (Feb 2024) is the first major revision since CSF 1.1 (2018). The headline change is the
  addition of a sixth Function, **GOVERN**, which elevates cybersecurity governance,
  risk-management strategy, roles, policy, oversight, and supply chain risk management to the same
  level as the original five Functions. CSF 2.0 also broadened its scope beyond critical
  infrastructure to organizations of any size, sector, or maturity level.
- Two organization-specific artifacts sit at the center of using CSF:
  - **Current Profile** — where the organization's cybersecurity outcomes actually stand today,
    subcategory by subcategory.
  - **Target Profile** — where the organization wants those outcomes to be, based on its risk
    tolerance, mission, legal/regulatory obligations, and resources.
  - The gap between the two Profiles drives a prioritized action plan.
- **Implementation Tiers** describe the rigor of an organization's cybersecurity risk governance
  and management practices — they are a maturity descriptor, not a scoring of individual controls,
  and not a prerequisite for using the Framework. Tiers apply organization-wide or per Function,
  at the organization's discretion.

| Tier | Name | Characteristics |
|---|---|---|
| 1 | Partial | Risk management practices are informal and applied ad hoc, often reactively. Limited awareness of organizational cybersecurity risk. |
| 2 | Risk-Informed | Risk management practices are approved by management but not established as organization-wide policy. Prioritization is risk-informed but not consistently formalized. |
| 3 | Repeatable | Organization-wide risk management practices are formally approved, expressed as policy, and regularly updated. Consistent methods are in place to respond to changes in risk. |
| 4 | Adaptive | The organization adapts its cybersecurity practices in near-real-time based on lessons learned and predictive indicators, using continuous improvement that incorporates advanced technologies and practices. |

## 2. The Six Functions

Functions are the highest level of organization in CSF 2.0 — they organize cybersecurity outcomes
at their most basic level and are not intended to be a sequential path; in practice, an
organization performs activities from all six concurrently.

| Function | Code | Focus | Example Categories |
|---|---|---|---|
| GOVERN | GV | Establish, communicate, and monitor the organization's cybersecurity risk management strategy, expectations, and policy. | Organizational Context, Risk Management Strategy, Roles/Responsibilities/Authorities, Policy, Oversight, Cybersecurity Supply Chain Risk Management |
| IDENTIFY | ID | Understand the organization's current cybersecurity risk to systems, assets, data, and capabilities. | Asset Management, Risk Assessment, Improvement |
| PROTECT | PR | Use safeguards to manage cybersecurity risk and prevent or lower the likelihood/impact of adverse events. | Identity Management/Authentication/Access Control, Awareness and Training, Data Security, Platform Security, Technology Infrastructure Resilience |
| DETECT | DE | Find and analyze possible cybersecurity attacks and compromises. | Continuous Monitoring, Adverse Event Analysis |
| RESPOND | RS | Take action once a cybersecurity incident is detected. | Incident Management, Incident Analysis, Incident Response Reporting and Communication, Incident Mitigation |
| RECOVER | RC | Restore assets and operations affected by a cybersecurity incident. | Incident Recovery Plan Execution, Incident Recovery Communication |

See `controls.csv` for all 22 Categories and 106 Subcategories with full descriptions — GOVERN
carries the largest share (31 subcategories across 6 categories), reflecting the 2.0 emphasis on
governance as a precondition for effective risk management in the other five Functions.

## 3. GOVERN's Six Categories (New in 2.0)

| Category | Code | Focus |
|---|---|---|
| Organizational Context | GV.OC | Mission, stakeholder needs, legal/regulatory/contractual obligations, critical dependencies |
| Risk Management Strategy | GV.RM | Risk appetite/tolerance, enterprise risk integration, prioritization method |
| Roles, Responsibilities, and Authorities | GV.RR | Leadership accountability, resourcing, HR integration |
| Policy | GV.PO | Cybersecurity policy establishment and maintenance |
| Oversight | GV.OV | Strategy review, performance evaluation, adjustment |
| Cybersecurity Supply Chain Risk Management | GV.SC | Supplier risk program, contracts, due diligence, monitoring, offboarding |

Supply chain risk management (GV.SC) is the single largest category in CSF 2.0 (10 subcategories),
reflecting how much weight the 2.0 revision places on third-party and supplier risk relative to
CSF 1.1.

## 4. Implementation Roadmap

1. **Scope the effort** — define which business units, systems, and data are in scope for the
   Profile; identify the organizational mission and priorities that will shape risk tolerance
   (GV.OC).
2. **Build the Current Profile** — for each of the 106 subcategories, assess what is actually
   implemented today. Use `templates/Current_Target_Profile_Template.csv` to record status per
   subcategory.
3. **Assess the Current Tier** — evaluate the rigor and repeatability of risk governance
   practices, organization-wide or per Function, against the four Tier definitions in Section 1.
4. **Build the Target Profile** — for each subcategory, define the desired outcome based on risk
   tolerance, legal/regulatory requirements, mission objectives, and available resources.
5. **Gap analysis** — compare Current Profile to Target Profile subcategory by subcategory; every
   material gap becomes a row in `templates/Nonconformity_Gap_Register.csv` with an owner and
   target date.
6. **Prioritize and build the action plan** — sequence gap closure by risk exposure, cost, and
   dependency; align resourcing (GV.RR-03) to the plan.
7. **Implement** — build or mature the actual controls, processes, and technology the Target
   Profile commits to.
8. **Tier re-assessment** — periodically re-evaluate Tier maturity as governance practices mature
   from ad hoc (Partial) toward integrated and adaptive.
9. **Review and iterate** — bring Profile status, Tier assessment, gap register changes, and
   security objective progress into a recurring leadership **Profile Review**
   (`templates/Profile_Review_Agenda_Template.md`). CSF explicitly frames this as a continuous
   cycle, not a one-time certification event.

## 5. Cross-Mapping to Other Frameworks

Useful when an organization runs NIST CSF alongside ISO 27001, SOC 2, or PCI DSS — avoid
duplicating evidence collection where outcomes genuinely overlap.

| CSF 2.0 Function | ISO/IEC 27001:2022 Annex A theme | SOC 2 Common Criteria series | PCI DSS v4.0 goal |
|---|---|---|---|
| GOVERN | Organizational (A.5.1-A.5.8, A.5.31) | CC1 (Control Environment), CC2 (Communication), CC5 (Control Activities) | Build and Maintain a Secure Network and Systems; Maintain an Information Security Policy (Req. 12) |
| IDENTIFY | Organizational (A.5.9-A.5.13, A.5.19-A.5.22) | CC3 (Risk Assessment), CC9 (Risk Mitigation) | Maintain a Vulnerability Management Program (Req. 5-6) |
| PROTECT | Technological (A.8.1-A.8.5, A.8.24), People (A.6), Physical (A.7) | CC6 (Logical and Physical Access Controls), CC8 (Change Management) | Protect Account Data (Req. 3-4); Implement Strong Access Control Measures (Req. 7-9) |
| DETECT | Technological (A.8.15, A.8.16) | CC7 (System Operations, detection portion) | Regularly Monitor and Test Networks (Req. 10-11) |
| RESPOND | Organizational (A.5.24-A.5.27) | CC7 (System Operations, response portion) | Maintain an Information Security Policy — incident response (Req. 12.10) |
| RECOVER | Organizational (A.5.29-A.5.30) | CC9 (Risk Mitigation), A1 (Availability, if in scope) | Maintain an Information Security Policy — recovery/continuity (Req. 12.10.1) |

**Practical use:** when responding to an evidence request under any one framework, check this
table for the adjacent CSF Function — the same access review, vulnerability scan, or incident
report often satisfies multiple frameworks' requests at once.

## 6. Templates in This Folder

See `templates/README.md` for the full set — adapted from the generic ISMS/SOC 2/PCI templates to
CSF's own terminology (e.g. a Current/Target Profile in place of a Statement of Applicability, a
"Gap Register" in place of a nonconformity or exception register, and Tier-based maturity fields
rather than pass/fail conformance fields).

---
*This is a reference framework, not a substitute for a formal risk assessment against your actual
organizational mission, risk tolerance, and legal/regulatory obligations. Validate Target Profile
selections and Tier ratings against your organization's own risk management strategy before
treating any subcategory above as mandatory or complete.*
