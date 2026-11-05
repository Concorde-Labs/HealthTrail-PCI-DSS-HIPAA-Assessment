# HealthTrail Hospital
## HIPAA Security Rule - Access Control and ePHI Protection Assessment

**Prepared by:** Concord Ekwonna  
**Framework:** HIPAA Security Rule (45 CFR Part 164, Subpart C)  

---

## 1. Executive Summary

HealthTrail Hospital operates a main hospital and two outpatient clinics, supported by an Electronic Health Record (EHR) system containing sensitive patient information, including medical histories, diagnoses, treatment records, and laboratory results.

The assessment identified weaknesses in employee access governance. Some administrative and billing employees can access clinical information beyond their job responsibilities, employee access is not consistently reviewed following role changes, and periodic EHR access reviews are not consistently performed.

These weaknesses increase the potential for inappropriate access to electronic protected health information (ePHI), unauthorized disclosure, and inadequate oversight of workforce access privileges.

This assessment evaluates the identified gaps against relevant HIPAA Security Rule requirements and recommends corrective actions to strengthen access governance and patient information protection.

## 2. Assessment Scope and Approach

The assessment focuses on workforce access to HealthTrail's EHR environment, including:

- Employee access authorization.
- Role-based access restrictions.
- Access changes following employee role transitions.
- Periodic user access reviews.
- Audit logging and monitoring of ePHI access.

Findings are based on the supplied organizational scenario. No EHR configurations, employee permissions, audit logs, or internal policies were independently examined.

## 3. HIPAA Access Control Gap Analysis

| ID | Identified Gap | Relevant HIPAA Security Rule Requirement | Associated Risk | Recommended Corrective Action |
|---|---|---|---|---|
| H-01 | Billing and administrative employees can access clinical information beyond their job responsibilities. | **45 CFR §164.312(a)(1)** - Access Control; **§164.308(a)(4)** - Information Access Management | Workforce members may access ePHI beyond authorized job functions. | Define role-based permissions, review existing EHR access, and restrict unnecessary privileges. |
| H-02 | Employee access rights are not consistently reviewed following role changes. | **§164.308(a)(3)(ii)(C)** - Termination Procedures; **§164.308(a)(4)(ii)(C)** - Access Establishment and Modification | Employees may retain access that is no longer appropriate for their current responsibilities. | Implement a formal joiner-mover-leaver process with documented approval and timely access changes. |
| H-03 | Periodic reviews of EHR access are not consistently performed. | **§164.308(a)(1)(ii)(D)** - Information System Activity Review; **§164.312(b)** - Audit Controls | Inappropriate access activity may remain undetected or insufficiently investigated. | Establish scheduled access entitlement reviews and risk-based audit log monitoring. |

**Regulatory Mapping Note:** Access entitlement reviews and system activity reviews are related but distinct activities. HIPAA's Information System Activity Review requirement specifically addresses regular review of system activity records, while access authorization and modification requirements support workforce entitlement management.

## 4. Recommended Access Governance Model

HealthTrail should establish an access management process based on documented job responsibilities and authorized use of ePHI.

| Workforce Role | Proposed Access Principle |
|---|---|
| Physicians and authorized clinical staff | Access to clinical information necessary for assigned treatment and professional responsibilities. |
| Nursing staff | Access appropriate to assigned clinical duties and patient care responsibilities. |
| Billing personnel | Access to payment, billing, and related information required for authorized functions; detailed clinical access only where justified. |
| Administrative staff | Access limited to information necessary for assigned administrative duties. |
| IT support personnel | Privileged technical access only where authorized, justified, and appropriately monitored. |

Access should be based on documented responsibilities rather than unrestricted departmental access.

**Important:** HIPAA's minimum necessary standard generally does not apply to disclosures to, or requests by, healthcare providers for treatment purposes. The proposed access model should accommodate legitimate clinical workflows and emergency access requirements.

## 5. Remediation and Verification Plan

| Finding | Proposed Owner | Target Timeline* | Expected Evidence | Verification Method |
|---|---|---|---|---|
| H-01 | Privacy Officer / EHR Administrator | 0–30 days | Approved role-permission matrix, access approvals, and updated EHR permissions | Sample user permissions against approved job responsibilities. |
| H-02 | HR / IT Access Management | 0–30 days | Role-change notifications, access modification tickets, and approval records | Sample employee role changes and verify timely access adjustments. |
| H-03 | Information Security / Privacy Officer | 30–60 days | Access review reports, audit log review procedures, and investigation records | Review completed entitlement reviews and sampled EHR activity monitoring records. |

*Timelines and accountable functions are proposed recommendations, not confirmed organizational arrangements.

## 6. Monitoring and Control Effectiveness

HealthTrail should establish measurable indicators to monitor access governance.

| Indicator | Proposed Measurement |
|---|---|
| Role-Based Access Compliance | Percentage of sampled users whose permissions align with approved roles |
| Role-Change Access Updates | Percentage of required access changes completed within the approved timeframe |
| Access Review Completion | Percentage of scheduled entitlement reviews completed and documented |
| Audit Log Review Completion | Percentage of scheduled EHR activity reviews completed |
| Unauthorized Access Findings | Number of confirmed inappropriate access incidents identified and investigated |

Management should establish targets based on operational requirements, risk exposure, and approved policies.

**Closure Criteria:** Findings should be closed only after access restrictions are implemented, supporting evidence is reviewed, and verification confirms that the identified weaknesses have been adequately addressed.

## 7. Conclusion

HealthTrail's current access management weaknesses create risks to the confidentiality of patient information and the effectiveness of workforce access governance.

Implementing documented role-based permissions, timely access modifications, periodic entitlement reviews, and appropriate EHR activity monitoring would strengthen the organization's ability to protect ePHI and support HIPAA Security Rule compliance.



