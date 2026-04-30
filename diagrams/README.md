# Privacy Diagrams and Visual Documentation

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** diagrams
**Framework Reference:** GDPR Art. 30 / NIST Privacy Framework / OMB Circular A-130
**Document ID:** FHX-PRIV-DIA-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

Privacy diagrams communicate complex data flows, processing boundaries, and privacy control coverage to auditors, supervisory authorities, and executive stakeholders. For CloudVault FHX, which processes personal data across multiple legal frameworks and 47 federal agency partners, visual documentation is essential for demonstrating compliance and identifying privacy risks.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| personal-data-flow-diagram.md | Personal data flow from collection through processing, sharing, and deletion | GDPR Art. 30, NIST PF | Active |
| privacy-rights-process-diagram.md | Process flow for handling data subject rights requests | GDPR Art. 12, CCPA | Active |
| breach-notification-flowchart.md | Multi-framework breach notification decision flowchart | GDPR Art. 33-34, HIPAA, CCPA | Active |
| privacy-controls-landscape.md | Visual map of FHX privacy controls across GDPR, CCPA, HIPAA, and Privacy Act | Multi-framework | Active |

---

## Personal Data Flow Description

CloudVault FHX personal data flows through the following stages:

**Collection:** Personal data is collected from three sources: (1) federal agency EHR systems (patient PHI via FHIR API), (2) the FHX patient portal (patient-provided contact and demographics data), and (3) HR processes (workforce personal data). Collection notice is provided at each collection point per GDPR Art. 13 and CCPA 1798.130(a)(5).

**Processing:** Collected personal data is validated, de-duplicated, and enriched by the FHX processing layer. Health data is processed under GDPR Art. 9(2)(h) (health care management) and the HIPAA Treatment/Payment/Operations (TPO) framework. Contact and non-health data is processed under GDPR Art. 6(1)(e) (public task).

**Storage:** All personal data is stored in encrypted form (AES-256) within the FHX AWS GovCloud environment. Retention periods are enforced automatically: 7 years for PHI (HIPAA/federal records), 2 years for audit logs, with shorter periods for operational data.

**Sharing:** PHI is shared with 47 federal agency partners under executed BAAs and DPAs, and limited by FHIR scoping to only the PHI each agency is authorized to receive. Non-PHI personal data is not shared with third parties except under the CCPA service provider framework.

**Archival and Deletion:** At end of retention, personal data is deleted using NIST SP 800-88 procedures. Deletion records are maintained for audit purposes. De-identified analytics data is retained for statistical purposes per GDPR Art. 9(2)(j).

---

## Privacy Controls Landscape

| Privacy Control Area | GDPR | CCPA | HIPAA | Privacy Act | FHX Implementation |
|---|---|---|---|---|---|
| Lawful basis for processing | Art. 6, 9 | N/A | 45 CFR 164.502 | 5 U.S.C. 552a(e)(1) | Public task + HIPAA TPO + Privacy Act authority |
| Privacy notice | Art. 13-14 | 1798.130(a)(5) | 45 CFR 164.520 | 5 U.S.C. 552a(e)(3) | Unified privacy notice at collection for all applicable laws |
| Data minimization | Art. 5(1)(c) | Not explicit | Minimum necessary (164.514) | 5 U.S.C. 552a(e)(1) | Minimum necessary applied; FHIR scope limiting |
| Storage limitation | Art. 5(1)(e) | Not explicit | 6-year retention (164.530) | Records schedules | Automated retention enforcement; 7 years PHI |
| Security | Art. 32 | 1798.150 | 164.308-164.312 | 5 U.S.C. 552a(e)(10) | AES-256, TLS 1.3, MFA, RBAC, FedRAMP High |
| Data subject rights | Art. 15-22 | 1798.100-1798.135 | Limited (HIPAA access) | 552a(d) | Unified DSR portal and procedure |
| Breach notification | Art. 33-34 | 1798.82 | 164.400-414 | N/A | Unified breach response procedure |
| Third-party management | Art. 28 | Service provider | 164.308(b) BAA | N/A | DPA + BAA combined agreements |

---

## Related Documents

- [ROPA](../ropa/README.md)
- [DPIA](../dpia/README.md)
- [Data Subject Rights](../data-subject-rights/README.md)
- [Breach Notification](../breach-notification/README.md)
- [CCPA Compliance](../ccpa/README.md)
- [HIPAA PHI Data Flow](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/diagrams/README.md)
- [FedRAMP Data Flow](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/att-02-data-flow/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
