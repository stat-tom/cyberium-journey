# Lesson 7 - Threats and Threat Modeling

## Status
- Not completed

## What Is a Threat?
- A threat is any potential cause of harm to a system, process, user, or organization.
- Threats can come from external attackers, malicious insiders, accidents, supply chain failures, or natural events.

## Threat Categories
- Human threats: cybercriminals, hacktivists, state actors, competitors, insiders.
- Technical threats: malware, exploitation of vulnerabilities, denial-of-service attacks.
- Process threats: weak approvals, missing backups, poor offboarding, insecure change management.
- Environmental threats: fire, flood, power failure, hardware failure.

## What Threat Modeling Is
- Threat modeling is a structured method for identifying what could go wrong in a system and deciding which controls are needed.
- It is most effective early in design, but it also provides value when reviewing existing systems.

## Typical Threat Modeling Steps
- Define the scope and business purpose of the system.
- Identify assets such as data, credentials, APIs, and privileged functions.
- Map components, trust boundaries, data flows, and external dependencies.
- List possible threats against each component and flow.
- Rate the threats by likelihood and impact.
- Select mitigations and track the remaining risk.

## Common Frameworks
- STRIDE: spoofing, tampering, repudiation, information disclosure, denial of service, elevation of privilege.
- Attack trees: visual breakdowns of how an attacker might achieve a goal.
- Abuse cases: scenarios that describe how a feature can be misused.

## Outputs of Threat Modeling
- Better system diagrams and trust-boundary awareness.
- A prioritized list of security requirements.
- Early detection of design weaknesses before implementation costs increase.
- A shared understanding between developers, architects, and security teams.

## Notes
- Threat modeling is not about predicting every attack. It is about systematically reducing blind spots.
