# Record of Processing Activities (ROPA)

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** ropa
**Framework Reference:** GDPR Article 30 / NIST Privacy Framework / OMB Circular A-130
**Document ID:** FHX-PRIV-ROPA-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

GDPR Article 30 requires controllers and processors to maintain a record of processing activities (ROPA). The ROPA is a living document that describes every processing activity involving personal data: what data is processed, for what purpose, on what legal basis, who it is shared with, how long it is retained, and what security measures protect it. For federal systems, the ROPA also informs the Privacy Impact Assessment (PIA) required under OMB Circular A-130.

CloudVault FHX processes personal data of multiple categories across dozens of processing activities. This folder documents all FHX processing activities in GDPR-compliant ROPA format.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| ropa-master.md | Master ROPA: all processing activities in GDPR Art. 30 format | GDPR Art. 30 | Active |
| ropa-phi-processing.md | ROPA entries for PHI processing activities | GDPR Art. 30, HIPAA | Active |
| ropa-payment-processing.md | ROPA entries for payment and financial data processing | GDPR Art. 30, PCI-DSS | Active |
| ropa-analytics-processing.md | ROPA entries for health analytics and reporting activities | GDPR Art. 30 | Active |

---

## ROPA: Selected Processing Activities

The following table documents representative processing activities. The full ROPA contains entries for all 34 identified processing activities.

| Activity ID | Processing Activity | Data Categories | Subjects | Legal Basis | Purpose | Controller | Processor | Retention | Recipients | Security Measures |
|---|---|---|---|---|---|---|---|---|---|---|
| FHX-PA-001 | Patient health record exchange | PHI: name, DOB, MRN, diagnoses, medications, lab results | Federal health program beneficiaries (890,000+) | GDPR Art. 6(1)(e): public task; HIPAA Authorization (where applicable) | Treatment coordination across federal agencies | FHX (federal government) | HealthPay (payment only) | 7 years post-encounter | 47 federal agency partners | AES-256, TLS 1.3, MFA, RBAC |
| FHX-PA-002 | Identity verification and authentication | PII: name, DOB, government ID, email | Federal health program beneficiaries | GDPR Art. 6(1)(e): public task | Verify patient identity before PHI access | FHX | AWS Cognito | Session + 2 years audit log | Internal only | MFA, PIV/CAC, tokenization |
| FHX-PA-003 | Payment processing (copayments) | PCI: PAN (tokenized), billing name; PHI: diagnosis codes for billing | Patients with copayment obligations | GDPR Art. 6(1)(b): contract; Art. 6(1)(e): public task | Process patient copayments for federal health services | FHX | HealthPay Federal Solutions LLC | 7 years | HealthPay (processor), Treasury (recipient) | Tokenization, TLS 1.3, AES-256 |
| FHX-PA-004 | Security monitoring and audit logging | Pseudonymized usage data, IP addresses, user activity | All FHX users | GDPR Art. 6(1)(c): legal obligation; Art. 6(1)(f): legitimate interest | Detect security threats and maintain audit trail (FISMA, FedRAMP) | FHX | AWS (CloudTrail, CloudWatch) | 2 years | ISSO, SOC, AO (on request) | AES-256, access restricted to security personnel |
| FHX-PA-005 | Health analytics and aggregate reporting | De-identified or aggregated health data | Derived from beneficiary data (non-identifiable) | GDPR Art. 9(2)(j): scientific research/statistics (with safeguards) | Federal health program performance analytics | FHX | Apogee Analytics Group | 5 years | Federal agency partners, HHS | De-identification to HIPAA Safe Harbor standard |
| FHX-PA-006 | Employee and contractor data (workforce management) | HR data: name, role, employment terms, training records | FHX workforce (87 individuals) | GDPR Art. 6(1)(b): employment contract; Art. 6(1)(c): legal obligation | HR management, access provisioning, security training tracking | FHX | HR provider | Duration of employment + 7 years | ISSO, HR, managers | Standard HR data controls |
| FHX-PA-007 | Breach and incident records | PHI/PII categories involved in incidents; incident details | Individuals affected by security incidents | GDPR Art. 6(1)(c): legal obligation (GDPR Art. 33 documentation) | Maintain breach notification records as required by GDPR and HIPAA | FHX | None | 6 years | HHS OCR (HIPAA), supervisory authority (GDPR), legal counsel | Access restricted to ISSO and Privacy Officer |

**Total processing activities documented in full ROPA:** 34

---

## Data Categories Inventory

| Data Category | GDPR Classification | Volume | Sensitivity | Encryption |
|---|---|---|---|---|
| Health data (PHI) | Special category (Art. 9) | 890,000+ individuals | Very High | AES-256 at rest, TLS 1.3 in transit |
| Government identifiers (SSN, MRN) | Highly sensitive (national law) | 890,000+ individuals | Very High | AES-256 + tokenization |
| Financial data (payment tokens) | Sensitive | All paying individuals | High | Tokenization, AES-256 |
| Biometric data | Special category (Art. 9) — not collected by FHX | Not applicable | Not applicable | N/A |
| Contact data (email, phone, address) | Standard personal data | 890,000+ individuals | Medium | AES-256 |
| Audit and access logs | Pseudonymized operational data | All users | Low-Medium | AES-256 |
| Aggregated analytics (de-identified) | Non-personal data (post-de-identification) | Derived data | Low | AES-256 |

---

## Related Documents

- [DPIA](../dpia/README.md)
- [Data Subject Rights](../data-subject-rights/README.md)
- [Data Processing Agreements](../dpa-templates/README.md)
- [Breach Notification](../breach-notification/README.md)
- [PHI Inventory](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/phi-inventory/README.md)
- [FedRAMP PT Controls](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
