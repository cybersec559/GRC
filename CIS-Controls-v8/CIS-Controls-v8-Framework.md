# CIS Controls v8 — Reference Guide for Security Professionals

A working reference for building, assessing, or maturing a security program against the Center
for Internet Security (CIS) Critical Security Controls, version 8. Covers what CIS Controls is
(and how it differs from ISO/SOC 2/PCI DSS), the Implementation Group (IG) self-selection model,
the 18 Controls and their 153 Safeguards, an implementation roadmap, and a cross-mapping to
ISO/IEC 27001:2022, SOC 2, PCI DSS, and NIST CSF.

---

## 1. What CIS Controls Is (and Isn't)

- CIS Controls is a **prioritized, practitioner-focused set of safeguards** developed and
  maintained by a global community of security practitioners (the CIS Controls Community),
  distilling real-world attack data down to the defensive actions that matter most.
- It is **not a certification and not an attestation** — there is no external auditor issuing a
  CIS Controls report or badge. It is a free, publicly available prioritization framework that an
  organization adopts and self-assesses against, optionally using CIS's own tooling
  (CIS-CAT Pro) or a manual self-assessment.
- Compared to ISO 27001 (management-system-heavy, certification-driven) or PCI DSS (mandated by
  payment brands with formal validation paths), CIS Controls is positioned as **more actionable
  and less bureaucratic** — a flat list of concrete technical and procedural actions rather than
  a management-system standard. This makes it a common choice for smaller security teams with
  limited governance overhead, and a practical **on-ramp** many organizations use to build real
  controls before pursuing a formal certification or attestation later.
- **v8 (current version)** reorganized the prior v7.1 20-Control structure into **18 Controls**
  and shifted from role-based groupings (e.g., "Network," "Application") to activity-based
  groupings, reflecting the move toward cloud-based computing, remote work, and modern
  identity-centric security.

## 2. Implementation Groups — Self-Selecting Your Starting Point

CIS Controls v8 groups its 153 Safeguards into three **Implementation Groups (IGs)**, each
building cumulatively on the last: a Safeguard tagged IG1 also applies to IG2 and IG3; a
Safeguard tagged IG2 also applies to IG3. There is no IG0 — IG1 is the floor every organization
should meet.

| IG | Who it's for | Characteristics |
|---|---|---|
| **IG1** | Small/limited-resource organizations | Basic cyber hygiene. Limited in-house IT/security expertise, primarily off-the-shelf hardware/software, low sensitivity of data handled. ~56 Safeguards. Defends against the most common, opportunistic attacks. |
| **IG2** | Organizations with dedicated IT/security staff | Handles more sensitive data (customer, financial, regulated data) and faces more sophisticated threats. Adds Safeguards supporting more complex infrastructure and multiple departments. Cumulative with IG1: ~130 Safeguards total. |
| **IG3** | Large, mature, or highly regulated organizations | Dedicated security staff specializing in different facets (risk management, application security, incident response). Faces sophisticated/targeted attacks and must defend high-value, highly sensitive data. All 153 Safeguards. |

**Self-selection is based on organization size, risk profile, sensitivity of data handled, and
resources available** — not prescribed externally. An organization determines its own IG, then
treats every Safeguard at that IG (and below) as its baseline control set. See `controls.csv` for
every Safeguard's assigned IG.

## 3. The 18 CIS Controls

| # | Control | Focus |
|---|---|---|
| 1 | Inventory and Control of Enterprise Assets | Know what devices are on your network |
| 2 | Inventory and Control of Software Assets | Know what software runs on those devices |
| 3 | Data Protection | Identify, classify, and protect sensitive data |
| 4 | Secure Configuration of Enterprise Assets and Software | Harden default configurations |
| 5 | Account Management | Manage the lifecycle of user and admin accounts |
| 6 | Access Control Management | Grant, revoke, and enforce access, including MFA |
| 7 | Continuous Vulnerability Management | Find and remediate vulnerabilities on an ongoing basis |
| 8 | Audit Log Management | Collect, retain, and review logs to detect and investigate incidents |
| 9 | Email and Web Browser Protections | Reduce attack surface in the most commonly exploited client software |
| 10 | Malware Defenses | Prevent or control installation/execution of malicious code |
| 11 | Data Recovery | Restore enterprise assets and data to a trusted state after an incident |
| 12 | Network Infrastructure Management | Securely manage routers, switches, firewalls, and other network devices |
| 13 | Network Monitoring and Defense | Detect and respond to threats moving across the network |
| 14 | Security Awareness and Skills Training | Build a security-conscious workforce |
| 15 | Service Provider Management | Manage the risk introduced by third parties |
| 16 | Application Software Security | Manage the security life cycle of in-house-developed and acquired software |
| 17 | Incident Response Management | Establish a program to prepare for, detect, and respond to incidents |
| 18 | Penetration Testing | Test the effectiveness of defenses by simulating an attacker |

See `controls.csv` for all 153 individual Safeguards under these 18 Controls, each with its
description, assigned Implementation Group, asset type, and security function.

## 4. Implementation Roadmap

1. **Determine your Implementation Group** — assess organization size, data sensitivity, threat
   exposure, and available resources (Section 2). Most organizations starting fresh should target
   IG1 first regardless of ultimate ambition — it is explicitly designed as the achievable floor.
2. **Implement Safeguards in priority order** — start with the foundational Controls
   (1, 2, and 4 — knowing what you have and hardening it) before layering on detection- and
   response-oriented Controls (8, 13, 17). CIS's own guidance and community resources
   (Community Defense Model) reinforce that Controls 1-6 defend against the largest share of
   real-world attack techniques.
3. **Use CIS-CAT Pro or a documented self-assessment process** — CIS provides a free
   self-assessment tool (CIS-CAT Lite) and a licensed version (CIS-CAT Pro) that scores systems
   against CIS Benchmarks (the configuration-level counterpart to the Controls). Absent tooling,
   use the `Internal_Audit_Checklist_Template.csv` and `CIS_Controls_Implementation_Matrix_Template.csv`
   in `templates/` to track status manually.
4. **Track and mature toward the next IG over time** — treat IG1 as a floor, not a ceiling.
   Reassess annually (or after significant organizational change) whether growth in data
   sensitivity, headcount, or threat exposure justifies adopting IG2 or IG3 Safeguards.

## 5. Cross-Mapping to Other Frameworks

CIS publishes its own detailed mappings between the Controls/Safeguards and other major
frameworks; the table below summarizes the general correspondence at the Control level. Useful
when an organization runs CIS Controls alongside ISO 27001, SOC 2, PCI DSS, or NIST CSF — avoid
rebuilding evidence collection per framework where the underlying control genuinely overlaps.

| CIS Control | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria | PCI DSS Requirement | NIST CSF 2.0 Function |
|---|---|---|---|---|
| 1-2 (Asset/Software Inventory) | A.5.9, A.8.19 | CC6.1 | 2, 6.3 | Identify |
| 3 (Data Protection) | A.5.12, A.8.10-A.8.12, A.8.24 | C1.1, C1.2 | 3, 4 | Protect |
| 4 (Secure Configuration) | A.8.9 | CC6.1 | 1, 2 | Protect |
| 5-6 (Account & Access Control Management) | A.5.15-A.5.18, A.8.2-A.8.5 | CC6.1-CC6.3 | 7, 8 | Protect |
| 7 (Vulnerability Management) | A.8.8 | CC7.1 | 6.3, 11.3 | Identify, Protect |
| 8 (Audit Log Management) | A.8.15-A.8.17 | CC7.1-CC7.2 | 10 | Detect |
| 9 (Email/Browser Protections) | A.8.7, A.8.23 | CC6.6 | 5, 6 | Protect |
| 10 (Malware Defenses) | A.8.7 | CC6.8 | 5 | Protect |
| 11 (Data Recovery) | A.8.13, A.5.30 | A1.2, A1.3 | 12.10 (supporting) | Recover |
| 12-13 (Network Management & Monitoring) | A.8.20-A.8.22 | CC6.6, CC7.1-CC7.2 | 1, 10, 11 | Protect, Detect |
| 14 (Awareness & Training) | A.6.3 | CC1.4 | 12.6 | Govern, Protect |
| 15 (Service Provider Management) | A.5.19-A.5.22 | CC9.2 | 12.8-12.9 | Identify |
| 16 (Application Software Security) | A.8.25-A.8.29 | PI1.1-PI1.5 | 6 | Protect |
| 17 (Incident Response Management) | A.5.24-A.5.28 | CC7.3-CC7.5 | 12.10 | Respond, Recover |
| 18 (Penetration Testing) | A.8.8 (supporting) | CC4.1 (supporting) | 11.4 | Identify |

**Practical use:** when responding to an evidence request under any one framework, check this
table for the adjacent CIS Control — the same asset inventory, access review, pen test report, or
log review record often satisfies multiple frameworks' requests at once.

## 6. Templates Every Security Professional Should Have on Hand

- **Implementation Matrix** — spreadsheet: Safeguard ID | Control Title | Safeguard Title |
  Implementation Group | Applicable to Our IG (Y/N) | Implementation status | Evidence reference |
  Owner | Last review date.
- **Risk register** — Asset | Threat | Vulnerability | Likelihood | Impact | Inherent risk score |
  Treatment decision | Residual risk score | Related Safeguards | Owner | Review date.
- **Internal audit / self-assessment checklist** — one row per Safeguard, with fields for
  evidence reviewed, conformance finding, and corrective action reference.
- **Implementation Group Review agenda** — standing template covering Safeguard implementation
  progress, self-assessment/CIS-CAT results, risk register changes, and a periodic decision on
  whether to progress toward the next IG.

See `templates/README.md` for the full 19-template set adapted to CIS Controls terminology.

---
*This is a reference framework, not a substitute for a formal Implementation Group determination
and gap assessment against your organization's actual environment. Validate Safeguard
applicability against your own risk assessment before treating any Safeguard above as mandatory
or non-applicable.*
