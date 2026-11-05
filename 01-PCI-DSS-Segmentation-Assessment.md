# HealthTrail Hospital
## PCI DSS - Network Segmentation and CDE Scoping Assessment

**Prepared by:** Concord Ekwonna  
**Framework:** PCI DSS v4.0.1  

---

## 1. Executive Summary

HealthTrail Hospital operates one main hospital and two outpatient clinics, providing healthcare services supported by electronic health records, payment terminals, an online patient portal, and third-party payment processing services.

The hospital's payment systems are connected to its wider corporate network. However, the Cardholder Data Environment (CDE) has not been formally defined, and network segmentation has not been reviewed.

These weaknesses create uncertainty regarding which systems fall within PCI DSS scope and whether unnecessary network connections could expose payment systems to security threats.

This assessment identifies potential payment security risks and proposes a network segmentation approach to strengthen protection of the payment environment and support PCI DSS compliance.

## 2. Assessment Scope

The preliminary assessment considers:

- Reception payment terminals.
- Online patient payment portal.
- Third-party payment processor connections.
- Network infrastructure supporting payment transactions.
- Corporate systems, employee devices, EHR infrastructure, and guest Wi-Fi that may connect to or affect the payment environment.

**Scope limitation:** The actual transmission paths, storage locations, payment processing architecture, and security configurations have not been independently verified.

## 3. Current-State Assessment

| Observation | Potential Security Risk |
|---|---|
| The CDE has not been formally defined. | Systems that store, process, transmit, or could affect the security of cardholder data may be omitted from PCI DSS scope. |
| Payment systems are connected to the wider hospital network. | Unnecessary connectivity could increase exposure to threats originating from other network segments. |
| Network segmentation has not been reviewed. | Existing restrictions may not adequately isolate payment systems. |
| Employee devices and EHR systems operate within the wider network. | Compromised internal systems could potentially affect payment systems where connectivity is insufficiently restricted. |
| Guest Wi-Fi provides internet access, but access to internal systems has not been formally reviewed. | Unverified network boundaries may permit unintended connectivity. |
| A third-party payment processor handles transactions. | Responsibility for payment security controls and the hospital's remaining PCI DSS obligations may be unclear. |

## 4. Proposed CDE Scoping Approach

The hospital should identify and document all systems that store, process, or transmit cardholder data, along with connected systems and security-impacting components.

The following components require further investigation:

| System / Component | Preliminary Scoping Consideration |
|---|---|
| Reception payment terminals | Determine whether terminals store, process, or transmit cardholder data and identify their connectivity. |
| Online patient portal | Determine whether cardholder data passes through hospital-controlled systems or is handled through processor-hosted payment functionality. |
| Third-party payment processor | Document payment flows, provider responsibilities, and relevant security dependencies. |
| Network devices and security infrastructure | Identify components that connect to, segment, or protect the CDE. |
| Corporate and employee systems | Evaluate connectivity and whether these systems could affect CDE security. |
| EHR environment | Review network dependencies and potential paths to payment systems. |
| Guest Wi-Fi | Verify isolation from payment systems and other sensitive internal environments. |

**Important:** Inclusion in this table does not automatically establish that a system is in PCI DSS scope. Final classification depends on verified data flows, connectivity, system functions, and applicable PCI DSS scoping guidance.

## 5. Recommended Network Segmentation Design

A proposed network architecture should establish controlled boundaries between the payment environment and other hospital networks.

**Recommended security zones:**

- **Payment Zone:** In-scope payment systems and supporting components.
- **Clinical Zone:** EHR systems and clinical applications.
- **Corporate Zone:** Administrative systems and employee devices.
- **Guest Zone:** Patient and visitor internet access.
- **Management Zone:** Authorized infrastructure administration and security monitoring systems.

Traffic between zones should be restricted through appropriately configured firewalls or equivalent network security controls.

### Proposed Segmentation Principles

1. Deny inter-zone traffic by default unless explicitly authorized.
2. Permit only documented business-required connections to payment systems.
3. Restrict administrative access to approved personnel and management paths.
4. Isolate guest Wi-Fi from internal and payment networks.
5. Log and review security-relevant network activity.
6. Validate segmentation effectiveness through appropriate testing.

**Design Note:** These are proposed logical zones, not evidence of an existing or implemented network architecture. VLANs alone should not be assumed to provide effective PCI DSS segmentation.

## 6. PCI DSS Requirements and Control Recommendations

| PCI DSS v4.0.1 Requirement | Relevance to HealthTrail | Recommended Action |
|---|---|---|
| Requirement 1 - Install and Maintain Network Security Controls | Restricts unnecessary network connectivity to payment systems. | Establish documented network security rules and controlled payment environment boundaries. |
| Requirement 2 - Apply Secure Configurations to All System Components | Supports secure configuration of relevant systems and network devices. | Establish approved configuration standards for in-scope systems. |
| Requirement 7 - Restrict Access to System Components and Cardholder Data by Business Need to Know | Limits access to payment systems and sensitive information. | Apply role-based authorization and least-privilege access. |
| Requirement 8 - Identify Users and Authenticate Access to System Components | Supports accountability and secure authentication. | Apply appropriate authentication and access management requirements. |
| Requirement 11 - Test Security of Systems and Networks Regularly | Supports validation of segmentation and identification of weaknesses. | Conduct applicable segmentation penetration testing and review test results. |
| Requirement 12 - Support Information Security with Organizational Policies and Programs | Establishes security governance, responsibilities, and documented processes. | Maintain payment security policies, responsibilities, and scope documentation. |

## 7. Recommended Remediation Priorities

| Priority | Corrective Action | Expected Evidence |
|---|---|---|
| 1 | Document payment data flows and determine the CDE boundary. | Payment data-flow diagrams, system inventory, and approved scoping documentation. |
| 2 | Review network connectivity between payment systems and other hospital environments. | Network diagrams, firewall configurations, and connectivity review records. |
| 3 | Implement appropriate segmentation and access restrictions. | Approved network security rules, change records, and configuration evidence. |
| 4 | Define payment security responsibilities with third-party providers. | Responsibility matrix, service agreements, and provider compliance documentation. |
| 5 | Validate segmentation effectiveness and address identified weaknesses. | Segmentation test results, remediation records, and follow-up verification evidence. |

Priorities are proposed sequencing recommendations rather than formal risk ratings.

## 8. Verification and Closure Criteria

The hospital should verify that:

- CDE boundaries and payment data flows are documented and approved.
- Network connections into the payment environment are identified and justified.
- Unauthorized connectivity is blocked by appropriate security controls.
- Relevant third-party responsibilities are documented.
- Segmentation testing is performed where applicable and weaknesses are remediated.

A finding should not be closed solely because a control has been proposed or configured. Supporting evidence and appropriate validation should demonstrate that the identified weakness has been addressed.

## 9. Conclusion

HealthTrail's undefined CDE boundaries and unreviewed network segmentation create uncertainty regarding payment security exposure and PCI DSS scope.

A structured scoping exercise, supported by documented payment data flows, controlled network boundaries, appropriate security configurations, and segmentation validation, would strengthen the hospital's payment security posture.
