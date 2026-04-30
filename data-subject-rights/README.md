# Data Subject Rights Procedures

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** data-subject-rights
**Framework Reference:** GDPR Articles 15-22 / CCPA Cal. Civ. Code 1798.100-1798.199 / Privacy Act 1974
**Document ID:** FHX-PRIV-DSR-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

Individuals whose personal data is processed by CloudVault FHX have rights under GDPR (Articles 15-22), CCPA (Cal. Civ. Code 1798.100-1798.199), and the Privacy Act of 1974 (5 U.S.C. 552a). This folder documents the FHX procedures for receiving, verifying, and fulfilling data subject requests (DSRs) within the time limits mandated by each applicable law.

For a federal health exchange processing data across multiple legal regimes simultaneously, DSR management requires careful analysis: a request to delete health records may conflict with HIPAA record retention requirements, the Privacy Act, or federal records management law. This folder addresses these intersections explicitly.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| dsr-procedure.md | Master DSR intake, verification, and fulfillment procedure | GDPR Art. 12, CCPA 1798.105 | Active |
| right-of-access.md | Procedure for GDPR Art. 15 and CCPA access requests | GDPR Art. 15, CCPA 1798.110 | Active |
| right-to-erasure.md | Procedure for GDPR Art. 17 erasure requests (right to be forgotten) | GDPR Art. 17 | Active |
| right-to-portability.md | Procedure for GDPR Art. 20 data portability requests | GDPR Art. 20 | Active |
| right-to-object.md | Procedure for GDPR Art. 21 and CCPA opt-out requests | GDPR Art. 21, CCPA 1798.120 | Active |
| dsr-request-log.md | Log of all DSRs received, response status, and closure dates | GDPR Art. 12(1) | Active |

---

## Data Subject Rights Matrix

The following table maps each applicable right to the relevant legal provisions, FHX applicability, and any limitations.

| Right | GDPR Article | CCPA Provision | Privacy Act Section | FHX Applicability | Limitations |
|---|---|---|---|---|---|
| Right of Access | Art. 15 | 1798.110 | 552a(d)(1) | Yes: individuals may request a copy of their personal data held by FHX | May be limited where disclosure would harm another individual's rights or security |
| Right to Rectification | Art. 16 | N/A (CCPA does not include) | 552a(d)(2) | Yes: individuals may correct inaccurate or incomplete personal data | Data shared with agency partners may require coordination |
| Right to Erasure | Art. 17 | 1798.105 | N/A (Privacy Act does not include) | Limited: HIPAA and federal records retention requirements may override erasure rights | HIPAA requires 6-year retention; federal records law may require longer |
| Right to Restriction | Art. 18 | N/A | N/A | Yes: individuals may request restriction of processing pending accuracy dispute resolution | |
| Right to Portability | Art. 20 | 1798.110 | N/A | Yes: health data can be exported in FHIR R4 format | Applies only to data provided by the individual and processed by automated means |
| Right to Object | Art. 21 | 1798.120 (opt-out of sale) | N/A | Yes for analytics and research processing; No for treatment and legal obligation processing | FHX does not sell personal data; CCPA opt-out mechanism not applicable to treatment data |
| Right to Not be Subject to Automated Decision-Making | Art. 22 | N/A | N/A | Limited: FHX uses automated record matching with human review available | Automated matching flags are reviewed by clinical staff before treatment decisions |

---

## DSR Response Timelines

| Request Type | GDPR Deadline | CCPA Deadline | Privacy Act Deadline | FHX Target |
|---|---|---|---|---|
| Access request | 1 month (Art. 12(3)) | 45 days (1798.130(a)(2)) | 30 days (552a(d)(1)) | 25 days |
| Rectification request | 1 month | N/A | 30 days | 20 days |
| Erasure request | 1 month | 45 days | N/A | 30 days (with retention conflict analysis) |
| Portability request | 1 month | 45 days | N/A | 25 days |
| Objection request | Without undue delay | 15 days (opt-out) | N/A | 10 days |

---

## DSR Intake and Verification Process

**Step 1: Request Receipt.** DSRs may be submitted through: (1) the FHX patient portal DSR form (authenticated users only), (2) written request to the FHX Privacy Officer (Sandra Voss, privacy@fhx.gov), or (3) in-person at the FHX Privacy Office.

**Step 2: Identity Verification.** All requestors must verify their identity before FHX processes a DSR. For authenticated portal users, identity is confirmed by existing MFA session. For external requests, a government-issued photo ID and supporting documentation (MRN, date of birth) are required. Identity verification is documented in the DSR log.

**Step 3: Request Assessment.** The Privacy Officer reviews the request to determine: (1) applicable legal rights, (2) any exemptions or limitations (e.g., HIPAA retention override for erasure), (3) any third parties affected by the response, and (4) the feasibility of fulfilling the request within the applicable timeline.

**Step 4: Fulfillment.** Approved requests are fulfilled by the Privacy Officer in coordination with the ISSO (for technical access or deletion) and the DevOps Lead (for data retrieval or deletion from technical systems). All fulfillment actions are documented in the DSR log.

**Step 5: Response.** A written response is sent to the requestor within the applicable deadline confirming the action taken, any limitations applied, and the requestor's right to appeal to the relevant supervisory authority if unsatisfied.

---

## FY2025 DSR Log Summary (Q1)

| Request Type | Received | Fulfilled | Denied | Pending | Average Response Time |
|---|---|---|---|---|---|
| Access (GDPR Art. 15) | 12 | 12 | 0 | 0 | 18 days |
| Rectification (GDPR Art. 16) | 8 | 8 | 0 | 0 | 14 days |
| Erasure (GDPR Art. 17) | 3 | 1 (full) | 2 (partial: HIPAA retention applies) | 0 | 28 days |
| Portability (GDPR Art. 20) | 5 | 5 | 0 | 0 | 22 days |
| Objection to analytics (GDPR Art. 21) | 2 | 2 | 0 | 0 | 8 days |
| CCPA Access | 7 | 7 | 0 | 0 | 22 days |
| CCPA Deletion | 3 | 1 | 2 (HIPAA retention) | 0 | 30 days |
| Privacy Act Access | 15 | 15 | 0 | 0 | 20 days |
| **Total** | **55** | **51** | **4** | **0** | **20 days avg** |

---

## Related Documents

- [ROPA](../ropa/README.md)
- [DPIA](../dpia/README.md)
- [Breach Notification](../breach-notification/README.md)
- [CCPA Compliance](../ccpa/README.md)
- [HIPAA PHI Inventory](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/phi-inventory/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
