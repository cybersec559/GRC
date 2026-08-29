# GDPR — Reference Guide for Security & Privacy Professionals

A working reference for building, assessing, or auditing a data protection program against the EU
General Data Protection Regulation (Regulation (EU) 2016/679). Covers scope and key roles, the
core catalog of principles/rights/obligations, an implementation roadmap, and a cross-mapping to
other frameworks commonly run in parallel (ISO/IEC 27001:2022, SOC 2, PCI DSS).

---

## 1. What GDPR Is

- GDPR is an **EU regulation** (not a directive) — it applies directly and uniformly across all
  EU/EEA member states without needing national implementing legislation, in force since
  **25 May 2018**, replacing the 1995 Data Protection Directive.
- **Extraterritorial scope (Art. 3):** GDPR applies to any organization processing the personal
  data of EU/EEA residents where the processing relates to (a) offering goods or services to those
  individuals, or (b) monitoring their behavior — **regardless of where the organization itself is
  established**. A company with no EU office or entity can still be squarely in scope.
- **"Personal data"** is defined broadly: any information relating to an identified or
  identifiable natural person (name, ID number, location data, online identifiers, or factors
  specific to physical/physiological/genetic/mental/economic/cultural/social identity).
- **Enforcement:** independent national supervisory authorities in each member state, coordinated
  by the **European Data Protection Board (EDPB)**. Fines can reach the greater of **€20 million or
  4% of total worldwide annual turnover** for the most serious infringements (lower tier: €10
  million / 2%).
- **One-stop-shop mechanism:** an organization with establishments in multiple member states
  generally deals with a single **lead supervisory authority** (based on its main EU establishment)
  rather than every national authority individually.

## 2. Key Roles

| Role | Definition |
|---|---|
| **Data Subject** | The identified or identifiable natural person whose personal data is processed. |
| **Controller** | The entity that determines the purposes and means of processing personal data. |
| **Processor** | The entity that processes personal data on behalf of, and under the instructions of, a controller. |
| **Sub-processor** | A further processor engaged by a processor to carry out specific processing activities on the controller's behalf; must be authorized and flow down the same contractual protections. |
| **Joint Controllers** | Two or more controllers who jointly determine the purposes and means of processing (Art. 26). |
| **Data Protection Officer (DPO)** | An independent expert role required in specified circumstances to advise on and monitor GDPR compliance (Art. 37-39). |
| **Supervisory Authority** | The independent national public authority responsible for monitoring GDPR application (e.g., investigating complaints, receiving breach notifications). |
| **European Data Protection Board (EDPB)** | EU body ensuring consistent application of GDPR across supervisory authorities; issues guidelines and binding decisions in cross-border cases. |

## 3. Core Catalog

See `controls.csv` for the full 50-entry reference catalog with descriptions. Summarized by
category below.

### 3.1 Data Protection Principles (Art. 5)

| Article | Principle |
|---|---|
| Art. 5(1)(a) | Lawfulness, fairness and transparency |
| Art. 5(1)(b) | Purpose limitation |
| Art. 5(1)(c) | Data minimization |
| Art. 5(1)(d) | Accuracy |
| Art. 5(1)(e) | Storage limitation |
| Art. 5(1)(f) | Integrity and confidentiality |
| Art. 5(2) | Accountability |

### 3.2 Lawful Basis for Processing (Art. 6)

| Article | Basis |
|---|---|
| Art. 6(1)(a) | Consent |
| Art. 6(1)(b) | Contract |
| Art. 6(1)(c) | Legal obligation |
| Art. 6(1)(d) | Vital interests |
| Art. 6(1)(e) | Public task |
| Art. 6(1)(f) | Legitimate interests |

### 3.3 Consent (Art. 7-8)

| Article | Requirement |
|---|---|
| Art. 7(1)-(2) | Conditions for valid consent |
| Art. 7(3) | Right to withdraw consent |
| Art. 8 | Conditions applicable to a child's consent |

### 3.4 Special Category Data (Art. 9-10)

| Article | Requirement |
|---|---|
| Art. 9(1) | Prohibition on processing special categories of data |
| Art. 9(2) | Conditions lifting the prohibition |
| Art. 10 | Processing of criminal conviction and offence data |

### 3.5 Data Subject Rights (Art. 12-22)

| Article | Right |
|---|---|
| Art. 12 | Transparent information and communication |
| Art. 13 | Information to be provided (data collected from the subject) |
| Art. 14 | Information to be provided (data not obtained from the subject) |
| Art. 15 | Right of access |
| Art. 16 | Right to rectification |
| Art. 17 | Right to erasure ("right to be forgotten") |
| Art. 18 | Right to restriction of processing |
| Art. 19 | Notification obligation re: rectification/erasure/restriction |
| Art. 20 | Right to data portability |
| Art. 21 | Right to object |
| Art. 22 | Automated individual decision-making, including profiling |

### 3.6 Controller & Processor Obligations (Art. 24-30)

| Article | Obligation |
|---|---|
| Art. 24 | Responsibility of the controller |
| Art. 25 | Data protection by design and by default |
| Art. 26 | Joint controllers |
| Art. 27 | Representatives not established in the Union |
| Art. 28 | Processor obligations and data processing agreements |
| Art. 29 | Processing under the authority of the controller or processor |
| Art. 30 | Records of processing activities (RoPA) |

### 3.7 Security of Processing (Art. 32)

| Article | Requirement |
|---|---|
| Art. 32 | Security of processing |

### 3.8 Data Breach Notification (Art. 33-34)

| Article | Requirement |
|---|---|
| Art. 33 | Notification to the supervisory authority (within 72 hours where feasible) |
| Art. 34 | Communication to the data subject |

### 3.9 Data Protection Impact Assessment (Art. 35-36)

| Article | Requirement |
|---|---|
| Art. 35 | DPIA requirement |
| Art. 36 | Prior consultation |

### 3.10 Data Protection Officer (Art. 37-39)

| Article | Requirement |
|---|---|
| Art. 37 | Designation of the DPO |
| Art. 38 | Position of the DPO |
| Art. 39 | Tasks of the DPO |

### 3.11 International Data Transfers (Art. 44-49)

| Article | Mechanism |
|---|---|
| Art. 44 | General principle for transfers |
| Art. 45 | Adequacy decisions |
| Art. 46 | Appropriate safeguards (e.g. Standard Contractual Clauses) |
| Art. 47 | Binding Corporate Rules (BCRs) |
| Art. 49 | Derogations for specific situations |

## 4. Implementation Roadmap

1. **Data mapping / Records of Processing Activities (RoPA)** (Art. 30) — inventory every
   processing activity: purpose, categories of data subjects and data, recipients, transfers,
   retention, and security measures. This is the foundation everything else builds on.
2. **Lawful basis assessment** (Art. 6, Art. 9) — for each processing activity in the RoPA,
   identify and document the applicable lawful basis, and separately confirm any special category
   data has a valid Art. 9(2) condition.
3. **DPIA where required** (Art. 35) — screen each high-risk processing activity (large-scale
   special category processing, systematic monitoring, new technology, etc.) and complete a DPIA;
   consult the supervisory authority (Art. 36) if residual risk remains high.
4. **Policies & consent mechanisms** — publish privacy notices (Art. 12-14), implement a
   compliant consent mechanism where consent is the lawful basis (Art. 7-8), and stand up
   procedures for handling data subject rights requests (Art. 15-22).
5. **Breach response plan** (Art. 33-34) — build and rehearse a plan capable of meeting the
   72-hour supervisory authority notification clock and assessing whether data subject
   notification is separately required.
6. **DPO appointment if required** (Art. 37) — determine whether designation is mandatory
   (public authority, large-scale systematic monitoring, or large-scale special category
   processing) and appoint accordingly; even where not mandatory, many organizations appoint a
   privacy lead voluntarily.
7. **Ongoing monitoring** — maintain the RoPA and Compliance Matrix as processing changes, run
   periodic internal audits/readiness reviews, track international transfers and sub-processor
   changes, and bring status into a recurring compliance review.

## 5. Cross-Mapping to Other Frameworks

Useful when an organization runs GDPR alongside ISO 27001, SOC 2, or PCI DSS — avoid duplicating
evidence collection where obligations genuinely overlap.

| GDPR Category/Article | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria | PCI DSS |
|---|---|---|---|
| Data Protection Principles (Art. 5) | A.5.34 (Privacy and protection of PII), A.8.11 (Data masking) | Privacy criteria (if in scope — confirm current set with your auditor) | Req. 3-4 where cardholder data overlaps with personal data |
| Lawful Basis / Consent (Art. 6-8) | A.5.31 (Legal, statutory, regulatory and contractual requirements) | CC1.1, Privacy criteria | Req. 12.1 (information security policy) |
| Special Category Data (Art. 9-10) | A.5.12 (Classification of information), A.8.11 (Data masking) | C1.1 (Confidential information identification) | Req. 3.1-3.7 (account data protection) |
| Data Subject Rights (Art. 12-22) | A.5.34 | Privacy criteria (if in scope) | Limited overlap — cardholder data is not typically subject to portability/erasure requests |
| Controller & Processor Obligations (Art. 24-30) | A.5.19-A.5.22 (Supplier relationships) | CC9.2 (Vendor and business partner risk) | Req. 12.8-12.9 (TPSP management) |
| Security of Processing (Art. 32) | A.8.24 (Cryptography), Technological controls broadly | CC6.1-CC6.8 (Access controls) | Req. 3-4, 7-9 |
| Data Breach Notification (Art. 33-34) | A.5.24-A.5.28 (Incident management) | CC7.3-CC7.5 (Incident response/recovery) | Req. 12.10 |
| DPIA (Art. 35-36) | Clause 6.1 (Risk assessment), A.5.8 | CC3.1-CC3.4 (Risk assessment) | Req. 12.3 |
| Data Protection Officer (Art. 37-39) | A.5.2 (Roles and responsibilities) | CC1.3 (Structure and reporting lines) | Req. 12.4-12.5 |
| International Data Transfers (Art. 44-49) | A.5.14 (Information transfer), A.5.19-A.5.21 | CC9.2 (Vendor and business partner risk) | Req. 12.8 |

**Practical use:** when responding to a data subject request or an auditor request under any one
framework, check this table for adjacent controls/criteria — often the same evidence (a DPIA, an
access review, a vendor security questionnaire, a breach postmortem) satisfies multiple frameworks'
requests simultaneously.

## 6. Templates in This Folder

See `templates/README.md` for the full set — 18 fillable templates covering the GDPR compliance
lifecycle, including four GDPR-specific artifacts with no direct ISO/SOC2/PCI equivalent: the
**Records of Processing Activities Template**, the **Data Protection Impact Assessment Template**,
the **Data Subject Request Log**, and the **International Transfer Register**.

---
*This is a reference framework, not legal advice and not a substitute for a formal gap assessment
against your organization's actual processing activities. GDPR compliance obligations depend
heavily on the specifics of what data you process, for whom, and where — consult qualified privacy
counsel before relying on any control above as a complete or accurate statement of your legal
obligations.*
