# cloudvault-privacy

![Framework](https://img.shields.io/badge/Framework-GDPR%20%7C%20CCPA-blue)
![Privacy](https://img.shields.io/badge/Privacy-FedRAMP%20High-red)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Cert](https://img.shields.io/badge/Cert-CGRC-green)
![Data](https://img.shields.io/badge/Data-PHI%20%7C%20PII%20%7C%20CUI-orange)

## System Overview

**System Name:** CloudVault Federal Health Exchange (FHX)
**System Owner:** Dr. Patricia Owens
**ISSO / ISSM:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Privacy Officer:** Sandra Voss
**AO:** Deputy Director Henry Kline
**CISO:** Angela Torres
**Classification:** UNCLASSIFIED // CUI
**Impact Level:** HIGH (FIPS 199) | FedRAMP High (421 controls)
**Cloud Platform:** AWS GovCloud (US-West)
**Last Updated:** April 2025

---

## Purpose

CloudVault FHX processes personal data — including PHI, PII, and CUI — for 47 federal agencies and 890,000+ patients. While primarily a federal system subject to FISMA and HIPAA, FHX also maintains compliance with GDPR (for data involving EU-affiliated individuals accessing the US federal health system) and CCPA (for California residents whose data is processed by FHX).

This repository documents the CloudVault FHX privacy compliance program: the Record of Processing Activities (ROPA), Data Protection Impact Assessments (DPIA), data subject rights procedures, data processing agreements (DPA), breach notification procedures, and CCPA-specific compliance documentation.

---

## Repository Structure

```
cloudvault-privacy/
├── ropa/                   # Record of Processing Activities
├── dpia/                   # Data Protection Impact Assessments
├── data-subject-rights/    # Data subject rights procedures (access, deletion, portability)
├── dpa-templates/          # Data Processing Agreement templates
├── breach-notification/    # Privacy breach notification procedures
├── ccpa/                   # CCPA compliance documentation
├── diagrams/               # Privacy data flow diagrams
└── README.md               # This file
```

---

## Deliverables

| Document | Folder | Framework Reference | Status |
|---|---|---|---|
| Record of Processing Activities (ROPA) | ropa/ | GDPR Art. 30 | In Progress |
| Data Protection Impact Assessment | dpia/ | GDPR Art. 35 | In Progress |
| Data Subject Rights Procedures | data-subject-rights/ | GDPR Art. 15-22 | In Progress |
| Data Processing Agreement Templates | dpa-templates/ | GDPR Art. 28 | In Progress |
| Privacy Breach Notification Procedures | breach-notification/ | GDPR Art. 33-34 / CCPA | In Progress |
| CCPA Compliance Program | ccpa/ | Cal. Civ. Code 1798.100 | In Progress |
| Privacy Data Flow Diagrams | diagrams/ | GDPR Art. 30 | In Progress |

---

## Privacy Framework Coverage

| Framework | Applicability | FHX Implementation |
|---|---|---|
| GDPR (EU 2016/679) | EU-affiliated individuals in FHX dataset; EU-funded research programs | Full GDPR compliance program; DPO function fulfilled by Privacy Officer (Sandra Voss) |
| CCPA / CPRA (Cal. Civ. Code 1798.100+) | California residents in FHX dataset (estimated 142,000 individuals) | CCPA privacy notice, opt-out mechanisms, data subject request procedures |
| HIPAA Privacy Rule (45 CFR 164.500+) | All PHI processed by FHX | Integrated with HIPAA compliance program; see cloudvault-hipaa repository |
| Privacy Act of 1974 (5 U.S.C. 552a) | All PII collected and maintained by federal agencies | System of Records Notice (SORN) maintained; FHX-001 SORN published in Federal Register |
| OMB Circular A-130 | Federal information resources management | Privacy Impact Assessment (PIA) maintained and updated annually |
| NIST Privacy Framework v1.0 | Privacy program structure | FHX privacy program structured around NIST Privacy Framework core functions |
| NIST SP 800-53 Rev 5 (PT family) | Privacy controls in federal systems | All 8 PT control families implemented in FHX FedRAMP baseline |

---

## Laws, Regulations, and Standards

| Law / Standard | Scope | Status |
|---|---|---|
| GDPR Art. 30 (ROPA) | Record all processing activities | Complete |
| GDPR Art. 35 (DPIA) | Impact assessments for high-risk processing | Complete |
| GDPR Art. 15-22 (DSR) | Data subject rights: access, erasure, portability, objection | In Progress |
| GDPR Art. 28 (DPA) | Data processor agreements | Complete |
| GDPR Art. 33-34 (Breach) | 72-hour breach notification to supervisory authority | Complete |
| CCPA 1798.100-1798.199 | California consumer rights | In Progress |
| Privacy Act 1974 | Federal PII management | Complete (SORN published) |
| OMB A-130 | Federal privacy program | Complete (PIA current) |

---

## Certifications

| Certification | Holder | Relevance |
|---|---|---|
| CGRC (Certified in Governance, Risk, and Compliance) | Enechi P.C. Njeze | Privacy program governance and federal privacy requirements |
| CISA (Certified Information Systems Auditor) | Enechi P.C. Njeze | Privacy control assessment and audit |
| CISM (Certified Information Security Manager) | Enechi P.C. Njeze | Privacy-security integration |
| PMP (Project Management Professional) | Enechi P.C. Njeze | Privacy program management |
| PMI-RMP (Risk Management Professional) | Enechi P.C. Njeze | Privacy risk assessment |
| CompTIA Security+ SY0-701 | Enechi P.C. Njeze | Technical privacy control implementation |
| CHP (Certified HIPAA Professional) | Enechi P.C. Njeze | HIPAA privacy rule compliance |
| CSCS (Certified Security Compliance Specialist) | Enechi P.C. Njeze | Multi-framework privacy compliance |
| CISSP (in progress) | Enechi P.C. Njeze | Broad privacy and security architecture |

---

## Related Repositories

- [cloudvault-fedramp-ato](https://github.com/enechi-njeze/cloudvault-fedramp-ato): FedRAMP ATO (PT controls)
- [cloudvault-hipaa](https://github.com/enechi-njeze/cloudvault-hipaa): HIPAA compliance (PHI)
- [cloudvault-nist-rmf](https://github.com/enechi-njeze/cloudvault-nist-rmf): NIST RMF (privacy-integrated)
- [cloudvault-risk-governance](https://github.com/enechi-njeze/cloudvault-risk-governance): Enterprise risk governance
- [cloudvault-master-controls](https://github.com/enechi-njeze/cloudvault-master-controls): Unified cross-framework controls

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
