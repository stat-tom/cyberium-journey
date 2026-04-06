# Lesson 2 - Penetration Testing Methodology

## Status
- Planned

## Overview
- A penetration test should follow a repeatable process so testing is effective, safe, and useful to the client.
- The exact workflow varies by engagement, but most tests follow the same high-level phases.

## 1. Scoping and Rules of Engagement
- Define the target systems, allowed techniques, testing window, contacts, and success criteria.
- Agree on legal authorization, data handling rules, and whether exploitation of sensitive systems is limited.
- Clarify what is in scope and out of scope to avoid unsafe or unauthorized activity.

## 2. Reconnaissance
- Gather information about the target from public sources and direct observation.
- Identify domains, IP ranges, technologies, users, exposed services, repositories, and metadata.
- Good reconnaissance often determines the quality of the rest of the engagement.

## 3. Enumeration and Scanning
- Identify open ports, running services, versions, technologies, directories, endpoints, and exposed functionality.
- Verify what is actually reachable and how the attack surface is structured.
- Distinguish between noisy automated results and findings worth manual follow-up.

## 4. Vulnerability Analysis
- Review discovered assets for weak configurations, missing patches, insecure logic, and exploitable trust relationships.
- Correlate technical findings with likely attack paths and business impact.
- Avoid treating every scanner output as a confirmed vulnerability.

## 5. Exploitation
- Attempt controlled exploitation only where it is permitted by the rules of engagement.
- Prove the weakness exists while minimizing disruption to production systems.
- Record exact steps, payloads, and evidence so the issue can be reproduced and fixed.

## 6. Post-Exploitation and Impact Validation
- Assess what access was gained and what an attacker could do next.
- Evaluate privilege escalation, lateral movement, access to sensitive data, and persistence risks if these are allowed in scope.
- Focus on the realistic business effect, not only the technical exploit.

## 7. Reporting and Retesting
- Document findings clearly, including risk, affected assets, evidence, attack narrative, and remediation advice.
- Prioritize issues so the client knows what to fix first.
- Retest remediated findings when needed to confirm the fixes actually work.

## Notes
- Strong methodology matters because a penetration test is valuable only when the results are trustworthy, reproducible, and safe.