# ISO/IEC 27001:2022 Framework — Reference Guide for Security Professionals

A working reference for building, assessing, or auditing an Information Security Management System
(ISMS) against ISO/IEC 27001:2022. Covers the management-system clauses, the restructured Annex A
control set (93 controls across 4 themes, down from 114 in the 2013 edition), an implementation
roadmap, and a cross-mapping to other frameworks commonly run in parallel (NIST CSF, SOC 2, PCI DSS).

---

## 1. What changed in the 2022 revision

- Annex A reorganized from **14 clauses / 114 controls** (2013) into **4 themes / 93 controls**.
- **11 new controls** introduced (e.g. Threat Intelligence, Cloud Security, Data Masking, Data Leakage
  Prevention, ICT Readiness for Business Continuity, Physical Security Monitoring, Configuration
  Management, Information Deletion, Web Filtering, Secure Coding, Monitoring Activities).
- Each control now carries **five attributes** for flexible filtering/reporting: Control type
  (Preventive/Detective/Corrective), Information security properties (CIA), Cybersecurity concepts
  (Identify/Protect/Detect/Respond/Recover — aligned to NIST CSF language), Operational capabilities
  (e.g. Governance, Asset Management, Physical Security), and Security domains (Governance &
  Ecosystem, Protection, Defence, Resilience).
- Organizations certified under 2013 have a transition deadline; new certifications are issued only
  against 2022.

## 2. Management System Clauses (4–10) — mandatory, auditable

These are the ISMS "operating system" — non-negotiable for certification, distinct from Annex A
(which is the control catalog you select from based on risk).

| Clause | Title | What it requires |
|---|---|---|
| 4 | Context of the Organization | Determine internal/external issues, interested parties and their requirements, ISMS scope (documented), and how the ISMS integrates with other business processes. |
| 5 | Leadership | Top management commitment, information security policy, and assignment of roles/responsibilities/authorities. |
| 6 | Planning | Risk assessment methodology, risk treatment plan, **Statement of Applicability (SoA)**, and information security objectives with a plan to achieve them. |
| 7 | Support | Resources, competence, awareness, communication, and documented information (control of records/policies). |
| 8 | Operation | Operational planning and control, risk assessment execution, and risk treatment plan execution. |
| 9 | Performance Evaluation | Monitoring/measurement/analysis/evaluation, internal audit program, and management review. |
| 10 | Improvement | Nonconformity and corrective action, continual improvement. |

**The Statement of Applicability (SoA)** is the single most important artifact connecting Clause 6
to Annex A: for each of the 93 controls, it records whether the control is applicable, why/why not,
and its current implementation status. Auditors will ask for this first.

## 3. Annex A — 93 Controls Across 4 Themes

### 3.1 Organizational Controls (A.5.1 – A.5.37) — 37 controls

| ID | Control |
|---|---|
| A.5.1 | Policies for information security |
| A.5.2 | Information security roles and responsibilities |
| A.5.3 | Segregation of duties |
| A.5.4 | Management responsibilities |
| A.5.5 | Contact with authorities |
| A.5.6 | Contact with special interest groups |
| A.5.7 | Threat intelligence *(new)* |
| A.5.8 | Information security in project management |
| A.5.9 | Inventory of information and other associated assets |
| A.5.10 | Acceptable use of information and other associated assets |
| A.5.11 | Return of assets |
| A.5.12 | Classification of information |
| A.5.13 | Labelling of information |
| A.5.14 | Information transfer |
| A.5.15 | Access control |
| A.5.16 | Identity management |
| A.5.17 | Authentication information |
| A.5.18 | Access rights |
| A.5.19 | Information security in supplier relationships |
| A.5.20 | Addressing information security within supplier agreements |
| A.5.21 | Managing information security in the ICT supply chain |
| A.5.22 | Monitoring, review and change management of supplier services |
| A.5.23 | Information security for use of cloud services *(new)* |
| A.5.24 | Information security incident management planning and preparation |
| A.5.25 | Assessment and decision on information security events |
| A.5.26 | Response to information security incidents |
| A.5.27 | Learning from information security incidents |
| A.5.28 | Collection of evidence |
| A.5.29 | Information security during disruption |
| A.5.30 | ICT readiness for business continuity *(new)* |
| A.5.31 | Legal, statutory, regulatory and contractual requirements |
| A.5.32 | Intellectual property rights |
| A.5.33 | Protection of records |
| A.5.34 | Privacy and protection of PII |
| A.5.35 | Independent review of information security |
| A.5.36 | Compliance with policies, rules and standards for information security |
| A.5.37 | Documented operating procedures |

### 3.2 People Controls (A.6.1 – A.6.8) — 8 controls

| ID | Control |
|---|---|
| A.6.1 | Screening |
| A.6.2 | Terms and conditions of employment |
| A.6.3 | Information security awareness, education and training |
| A.6.4 | Disciplinary process |
| A.6.5 | Responsibilities after termination or change of employment |
| A.6.6 | Confidentiality or non-disclosure agreements |
| A.6.7 | Remote working |
| A.6.8 | Information security event reporting |

### 3.3 Physical Controls (A.7.1 – A.7.14) — 14 controls

| ID | Control |
|---|---|
| A.7.1 | Physical security perimeters |
| A.7.2 | Physical entry |
| A.7.3 | Securing offices, rooms and facilities |
| A.7.4 | Physical security monitoring *(new)* |
| A.7.5 | Protecting against physical and environmental threats |
| A.7.6 | Working in secure areas |
| A.7.7 | Clear desk and clear screen |
| A.7.8 | Equipment siting and protection |
| A.7.9 | Security of assets off-premises |
| A.7.10 | Storage media |
| A.7.11 | Supporting utilities |
| A.7.12 | Cabling security |
| A.7.13 | Equipment maintenance |
| A.7.14 | Secure disposal or re-use of equipment |

### 3.4 Technological Controls (A.8.1 – A.8.34) — 34 controls

| ID | Control |
|---|---|
| A.8.1 | User endpoint devices |
| A.8.2 | Privileged access rights |
| A.8.3 | Information access restriction |
| A.8.4 | Access to source code |
| A.8.5 | Secure authentication |
| A.8.6 | Capacity management |
| A.8.7 | Protection against malware |
| A.8.8 | Management of technical vulnerabilities |
| A.8.9 | Configuration management *(new)* |
| A.8.10 | Information deletion *(new)* |
| A.8.11 | Data masking *(new)* |
| A.8.12 | Data leakage prevention *(new)* |
| A.8.13 | Information backup |
| A.8.14 | Redundancy of information processing facilities |
| A.8.15 | Logging |
| A.8.16 | Monitoring activities *(new)* |
| A.8.17 | Clock synchronization |
| A.8.18 | Use of privileged utility programs |
| A.8.19 | Installation of software on operational systems |
| A.8.20 | Networks security |
| A.8.21 | Security of network services |
| A.8.22 | Segregation of networks |
| A.8.23 | Web filtering *(new)* |
| A.8.24 | Use of cryptography |
| A.8.25 | Secure development life cycle |
| A.8.26 | Application security requirements |
| A.8.27 | Secure system architecture and engineering principles |
| A.8.28 | Secure coding *(new)* |
| A.8.29 | Security testing in development and acceptance |
| A.8.30 | Outsourced development |
| A.8.31 | Separation of development, test and production environments |
| A.8.32 | Change management |
| A.8.33 | Test information |
| A.8.34 | Protection of information systems during audit testing |

## 4. Implementation Roadmap (Plan–Do–Check–Act)

1. **Scope the ISMS** (Clause 4.3) — define boundaries: business units, locations, systems, data
   types in scope. Get this in writing and approved by leadership before anything else.
2. **Risk assessment** (Clause 6.1) — identify assets, threats, vulnerabilities; score
   likelihood × impact; produce a risk register.
3. **Risk treatment** (Clause 6.1.3) — for each risk: treat, transfer, avoid, or accept. Selected
   treatments map to Annex A controls.
4. **Draft the Statement of Applicability** — for all 93 controls, mark Applicable/Not Applicable
   with justification, and current implementation status.
5. **Implement/operate controls** (Clause 8) — build the actual policies, technical controls, and
   procedures the SoA commits to.
6. **Internal audit** (Clause 9.2) — independent (internal or third-party) review of ISMS
   conformance before external audit.
7. **Management review** (Clause 9.3) — leadership formally reviews ISMS performance, audit
   findings, risk register changes, and improvement actions.
8. **Corrective action** (Clause 10) — track nonconformities to closure.
9. **Stage 1 external audit** — documentation review (scope, SoA, policies, risk assessment).
10. **Stage 2 external audit** — evidence of operating effectiveness; interviews, sampling, system
    walkthroughs.
11. **Certification** (3-year cycle) — annual surveillance audits, recertification at year 3.

## 5. Cross-Mapping to Other Frameworks

Useful when an org (like this one) runs SOC 2, PCI DSS, and NIST CSF in parallel — avoid rebuilding
evidence collection per framework where controls genuinely overlap.

| ISO 27001:2022 Annex A theme | NIST CSF 2.0 function | Overlaps heavily with |
|---|---|---|
| Organizational (A.5) | Govern, Identify | SOC 2 CC1 (Control Environment), CC2 (Communication), PCI DSS Req. 12 |
| People (A.6) | Govern, Protect | SOC 2 CC1.4, PCI DSS Req. 12.6 (awareness training) |
| Physical (A.7) | Protect | SOC 2 CC6.4, PCI DSS Req. 9 |
| Technological — Access (A.8.1-A.8.5) | Protect | SOC 2 CC6.1-CC6.3, PCI DSS Req. 7-8 |
| Technological — Detection/Monitoring (A.8.15-A.8.16) | Detect | SOC 2 CC7.1-CC7.2, PCI DSS Req. 10 |
| Technological — Cryptography/Dev (A.8.24-A.8.34) | Protect | SOC 2 CC8.1, PCI DSS Req. 3-4, 6 |
| Incident Management (A.5.24-A.5.28) | Respond, Recover | SOC 2 CC7.3-CC7.5, PCI DSS Req. 12.10 |

**Practical use:** when responding to an auditor request under any one framework, check this table
for adjacent ISO controls — often the same evidence (e.g. an access review, a pen test report, a
change management ticket) satisfies multiple frameworks' requests simultaneously.

## 6. Templates Every Security Professional Should Have on Hand

- **Statement of Applicability (SoA)** — spreadsheet: Control ID | Title | Applicable (Y/N) |
  Justification | Implementation status | Evidence link | Owner.
- **Risk register** — Asset | Threat | Vulnerability | Likelihood | Impact | Inherent risk score |
  Treatment decision | Residual risk score | Owner | Review date.
- **Internal audit checklist** — one row per Annex A control + management clause, with fields for
  evidence reviewed, conformance finding, and corrective action reference.
- **Management review agenda** — standing template covering: audit results, risk register changes,
  nonconformities/corrective actions, security objective progress, external issue changes
  (regulatory, threat landscape), resource needs.

---
*This is a reference framework, not a substitute for a formal gap assessment against your actual
ISMS scope. Validate control applicability against your organization's actual risk assessment
before treating any control above as mandatory or non-applicable.*
