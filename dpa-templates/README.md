# Data Processing Agreements (DPA) Templates

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** dpa-templates
**Framework Reference:** GDPR Article 28 / HIPAA BAA (45 CFR 164.308(b)) / Privacy Act 1974
**Document ID:** FHX-PRIV-DPA-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

GDPR Article 28 requires that when a controller engages a processor to process personal data on its behalf, the processing must be governed by a binding Data Processing Agreement (DPA). The DPA establishes the processor's obligations regarding data protection, the scope of authorized processing, data security requirements, breach notification obligations, and sub-processor management.

For CloudVault FHX, DPAs run in parallel with HIPAA Business Associate Agreements (BAAs) for processors who handle both PHI and personal data under GDPR. This folder contains the FHX DPA template library and the executed DPA register.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| dpa-template-standard.md | Standard DPA template for cloud service providers and technology vendors | GDPR Art. 28 | Active |
| dpa-template-fedramp.md | DPA template adapted for FedRAMP-authorized cloud service providers | GDPR Art. 28 | Active |
| dpa-template-agency.md | Inter-agency data sharing agreement template with GDPR and Privacy Act provisions | GDPR Art. 28, Privacy Act | Active |
| dpa-executed-register.md | Register of all executed DPAs with parties, scope, effective date, and renewal | GDPR Art. 28 | Active |
| dpa-eu-scc.md | EU Standard Contractual Clauses addendum for any transfers to non-EU recipients | GDPR Art. 46(2)(c) | Active |

---

## DPA Core Requirements (GDPR Art. 28(3))

Every DPA executed by CloudVault FHX must address the following mandatory elements per GDPR Article 28(3):

| Required Element | Description | Included in FHX DPA Template |
|---|---|---|
| Subject matter and duration | Specific processing activities, data types, and agreement term | Yes |
| Nature and purpose of processing | How and why data is processed by the processor | Yes |
| Type of personal data and categories of subjects | PHI, PII, and other data categories; patients, workforce, partners | Yes |
| Controller's obligations and rights | Instructions the processor must follow; controller's audit rights | Yes |
| Processor must act only on documented instructions | Processor cannot process data beyond the scope of controller's instructions | Yes |
| Confidentiality obligations | Personnel authorized to process data must be bound by confidentiality | Yes |
| Security measures (Art. 32) | Appropriate technical and organizational measures proportionate to the risk | Yes |
| Sub-processor management | Prior written authorization required; same obligations passed down | Yes |
| Data subject rights assistance | Processor must assist controller in fulfilling DSRs | Yes |
| Deletion or return at end of service | All personal data deleted or returned upon termination | Yes |
| Audit rights | Controller may audit processor compliance | Yes |
| Evidence of GDPR compliance | Processor must provide necessary information to demonstrate compliance | Yes |

---

## Executed DPA Register (Representative Entries)

FHX maintains executed DPAs with all processors who handle personal data under GDPR and CCPA in addition to HIPAA BAAs. The DPA and BAA are maintained as a combined agreement where processing includes both PHI and non-health personal data.

| DPA ID | Processor | Data Categories Processed | Effective Date | Type | Status |
|---|---|---|---|---|---|
| FHX-DPA-001 | Amazon Web Services (AWS GovCloud) | All FHX personal data (hosting) | March 15, 2022 | DPA + BAA combined | Active |
| FHX-DPA-002 | HealthPay Federal Solutions LLC | Payment data, billing identifiers | January 1, 2023 | DPA + BAA combined | Active |
| FHX-DPA-003 | Apogee Analytics Group | Aggregated, de-identified health data | June 1, 2024 | DPA | Active |
| FHX-DPA-004 | ClearPath Security Assessors LLC | Incidental access during assessment | February 1, 2025 | DPA + BAA combined | Active |
| FHX-DPA-005 | MedCom Federal Solutions | PHI (HL7 FHIR integration services) | April 1, 2023 | DPA + BAA combined | Active |
| FHX-DPA-006 | Cornerstone OnDemand (LMS) | Workforce training records | July 1, 2022 | DPA | Active |

**Total executed DPAs:** 23 (18 vendor DPAs + 5 inter-agency data sharing agreements)

---

## EU Standard Contractual Clauses

Where FHX shares personal data with processors or recipients outside the EU/EEA, EU Standard Contractual Clauses (SCCs) are used as the legal transfer mechanism per GDPR Article 46(2)(c). As a US federal government entity, FHX uses the Controller-to-Processor SCCs (Module 2) or Controller-to-Controller SCCs (Module 1) as applicable. The current SCCs (adopted June 4, 2021 by the European Commission) are incorporated as an addendum to all relevant DPAs.

As of April 2025, all FHX DPAs with processors that may involve EU data subjects include the current EU SCCs addendum.

---

## Related Documents

- [ROPA](../ropa/README.md)
- [DPIA](../dpia/README.md)
- [Breach Notification](../breach-notification/README.md)
- [HIPAA BAA Templates](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/baa-templates/README.md)
- [FedRAMP Third-Party Risk](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
