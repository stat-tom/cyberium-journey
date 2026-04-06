# Lesson 2 - CIA Triad

## Status
- Not completed

## Overview
- The CIA triad is a foundational model used to describe three core information security objectives: confidentiality, integrity, and availability.

## Confidentiality
- Confidentiality ensures that information is accessible only to authorized users, systems, and processes.
- Typical controls include encryption, strong authentication, access control lists, network segmentation, and data classification.
- Example risk: a leaked customer database exposes personal data.

## Integrity
- Integrity ensures that information remains accurate, complete, and trustworthy.
- Typical controls include hashing, digital signatures, input validation, version control, and change approval processes.
- Example risk: an attacker modifies a payment recipient account number.

## Availability
- Availability ensures that systems, services, and data are accessible when required.
- Typical controls include redundancy, backups, patching, monitoring, failover design, and denial-of-service protection.
- Example risk: ransomware prevents staff from accessing business systems.

## Additional CIA-Related Attributes
- Authentication and authorization: verify user identity and ensure each user has the correct level of access.
- Non-repudiation: prevent users or systems from denying actions they performed, usually through logging, signatures, and audit trails.
- Resilience: maintain operations during disruption and recover quickly after failures or attacks.
- Compliance: meet legal, regulatory, contractual, and policy requirements.
- Privacy: protect personal data and the privacy rights of users.

## Tradeoffs
- Security decisions often improve one part of the triad while adding cost or complexity elsewhere.
- Example: stronger access controls improve confidentiality but may slow down legitimate workflows if implemented poorly.

## Examples by Goal
- Confidentiality: database encryption, VPN access, role-based access control.
- Integrity: code signing, audit logs, file integrity monitoring.
- Availability: load balancing, backup power, disaster recovery plans.

## Practical Use
- The CIA triad helps security teams map threats to business impact.
- It also helps prioritize which controls are most important for a specific system.

## Notes
- A single incident can affect more than one pillar. Ransomware, for example, can damage availability and integrity at the same time.
