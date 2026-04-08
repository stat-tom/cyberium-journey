# Lesson 7 - Threats and Threat Modeling

## Status
- Completed

## What Is a Threat?
- A threat is any potential cause of harm to a system, process, user, or organization.
- Threats can come from external attackers, malicious insiders, accidents, supply chain failures, or natural events.

![Definition of a threat](./assets/threat-definition.svg)

- A threat can also be described as a potential event in which a vulnerability may be exploited to cause damage.
- Common examples include unauthorized access, data theft, DDoS attacks, and malware infections.
- Threats may originate from both outside and inside the organization.

## Threat Categories
- Human threats: cybercriminals, hacktivists, state actors, competitors, insiders.
- Technical threats: malware, exploitation of vulnerabilities, denial-of-service attacks.
- Process threats: weak approvals, missing backups, poor offboarding, insecure change management.
- Environmental threats: fire, flood, power failure, hardware failure.

## External Threats

![External threats examples](./assets/threat-external-examples.svg)

- Hacking attempts may target confidential data, credentials, or exposed services.
- DDoS attacks try to make websites or online services unavailable.
- Competitors or hostile third parties may fund or commission malicious activity.

## Internal Threats

![Internal threats examples](./assets/threat-internal-examples.svg)

- Disgruntled employees may intentionally delete data or alter important code and settings.
- Unaware users can accidentally install malware or expose sensitive information.
- Coworkers, administrators, and contractors already have legitimate access, which increases the potential impact of misuse.

## What Threat Modeling Is
- Threat modeling is a structured method for identifying what could go wrong in a system and deciding which controls are needed.
- It is most effective early in design, but it also provides value when reviewing existing systems.

![Introduction to threat modeling](./assets/threat-modeling-intro.svg)

- It starts with understanding likely threats and weak points in the system.
- It continues with risk assessment so the organization can estimate business impact.
- The result should be proactive defensive actions rather than reacting only after incidents occur.

## The Attacker's Perspective

![The attacker's perspective in threat modeling](./assets/threat-attacker-perspective.svg)

- System decomposition helps break the application into components, data flows, and trust boundaries that can be analyzed for weak points.
- Brainstorming encourages the team to discuss realistic abuse cases and attack paths.
- Threat modeling is valuable because it deliberately looks at the system from the attacker's point of view rather than only from the defender's checklist.

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

## Using STRIDE to Analyze a User Interface

![STRIDE analysis for a user interface](./assets/threat-stride-ui-overview.svg)

- STRIDE is useful when reviewing user interfaces because many attack paths start with forms, workflows, exposed actions, or visible data.
- A UI-focused STRIDE review asks how a user-facing feature could be impersonated, manipulated, denied, abused, overloaded, or used to gain extra privileges.
- This does not replace server-side analysis, but it helps the team spot risky entry points earlier.

### Spoofing in the User Interface

![Spoofing in a user interface](./assets/threat-stride-ui-spoofing.svg)

- Ask whether an attacker can pretend to be another user through the interface.
- Weak authentication, weak session handling, or poor identity checks can make spoofing easier.
- Login, password reset, and account recovery flows deserve special attention.

### Tampering in the User Interface

![Tampering in a user interface](./assets/threat-stride-ui-tampering.svg)

- Ask whether values submitted through the interface can be modified in unintended ways.
- Server-side validation is critical because client-side controls alone do not stop tampering.
- Sensitive actions should also verify integrity, allowed state transitions, and authorization.

### Repudiation in the User Interface

![Repudiation in a user interface](./assets/threat-stride-ui-repudiation.svg)

- Ask whether a user can deny performing an action because the system cannot prove what happened.
- Missing logs, weak audit trails, or poor event attribution make repudiation harder to investigate.
- Important operations should record who acted, what changed, and when it happened.

### Information Disclosure in the User Interface

![Information disclosure in a user interface](./assets/threat-stride-ui-information-disclosure.svg)

- Ask whether the interface exposes sensitive data to the wrong people.
- Poorly handled errors, excessive detail in the UI, or weak transport protection can leak information.
- Review what the page reveals before login, after login, and during failure cases.

### Denial of Service in the User Interface

![Denial of service in a user interface](./assets/threat-stride-ui-denial-of-service.svg)

- Ask whether visible UI actions can be abused to overwhelm the system.
- Missing rate limits, expensive searches, or unbounded upload and form processing can enable denial-of-service conditions.
- Controls such as throttling, quotas, caching, and graceful degradation reduce this risk.

### Elevation of Privilege in the User Interface

![Elevation of privilege in a user interface](./assets/threat-stride-ui-elevation-of-privilege.svg)

- Ask whether a lower-privileged user can reach actions or data meant for higher-privileged roles.
- Broken authorization, unsafe admin flows, and client-controlled role checks are common causes.
- Every privileged action should be enforced on the server, even if the UI hides the control.

## Strengths of STRIDE

![Strengths of STRIDE](./assets/threat-stride-strengths.svg)

- STRIDE gives teams a systematic way to review common categories of threats.
- Its structured approach reduces the chance that important areas are skipped during analysis.
- It is especially useful for workshops because it gives people a shared vocabulary for discussing risk.

## Limitations of STRIDE

![Limitations of STRIDE](./assets/threat-stride-limitations.svg)

- STRIDE is a general model, so it does not automatically provide deep, technology-specific guidance.
- Teams still need technical knowledge of the application, platform, and architecture to use it well.
- It works best as a framework for thinking, not as a substitute for secure design review, testing, or operational context.

## Four Key Questions

![Four key questions in threat modeling](./assets/threat-four-key-questions.svg)

- What are we building?
- What can go wrong?
- What are we going to do about it?
- Did we do a good enough job?

## Step 1: What Are We Building?

![Step 1 in threat modeling](./assets/threat-step-1-what-are-we-building.svg)

- Start by decomposing the application into smaller parts that are easier to reason about.
- Build a clear understanding of components, functions, data flows, and trust boundaries.
- Review each component separately so the team understands the system before listing threats.

## Step 2: What Can Go Wrong?

![Step 2 in threat modeling](./assets/threat-step-2-what-can-go-wrong.svg)

- Identify threats for each part of the system instead of thinking only at a high level.
- Use a framework such as STRIDE to avoid missing common categories of abuse.
- Discuss the threats as a team so different people can challenge assumptions and add scenarios.

## Step 3: What Are We Going to Do About It?

![Step 3 in threat modeling](./assets/threat-step-3-what-are-we-going-to-do-about-it.svg)

- Choose mitigations that reduce risk to an acceptable level rather than aiming for perfect elimination.
- Some threats require architectural changes, while others are better handled with security features or process improvements.
- The output of this step should be a clear set of actions, owners, and priorities.

## Step 4: Did We Do a Good Enough Job?

![Step 4 in threat modeling](./assets/threat-step-4-did-we-do-a-good-enough-job.svg)

- Review whether the selected controls actually address the identified threats.
- Check whether the changes introduced new weaknesses or unexpected side effects.
- Treat threat modeling as a repeatable process that should be revisited as the system evolves.

## Summary of the Four Questions

![Summary of the four questions](./assets/threat-four-questions-summary.svg)

- First understand the system.
- Then identify what could go wrong.
- Next decide what actions to take.
- Finally verify whether the result is good enough.

## Practical References

![OWASP cheat sheets](./assets/threat-owasp-cheat-sheets.svg)

- OWASP Cheat Sheets provide short, practical guidance for common security problems.
- They are useful during threat modeling when the team needs mitigation ideas, secure design reminders, or implementation guidance.

## Outputs of Threat Modeling
- Better system diagrams and trust-boundary awareness.
- A prioritized list of security requirements.
- Early detection of design weaknesses before implementation costs increase.
- A shared understanding between developers, architects, and security teams.

## Team Participation

![Team involvement in threat modeling](./assets/threat-team-involvement.svg)

- Invite people from different roles when the system or business process is complex.
- Broader participation improves coverage because each role sees different risks and assumptions.
- When time is limited, a focused session with the core engineering team is usually better than a large unfocused meeting.

## Attacker Goals and Motivation

![Attacker goals and motivation](./assets/threat-attacker-goals.svg)

- Understanding attacker goals helps explain what the adversary is trying to achieve.
- Motivation analysis helps identify why a person or group might launch an attack.
- Asset protection improves when we identify which resources are most attractive to attackers.

## Threat Modeling vs Vulnerability Assessment

![Threat modeling versus vulnerability assessment](./assets/threat-modeling-vs-vuln-assessment.svg)

- Vulnerability assessment focuses on finding known weaknesses in systems and software.
- Threat modeling focuses on how attackers might misuse the design, architecture, data flows, or trust relationships.
- A useful rule of thumb is that vulnerability assessment is more defender-centric, while threat modeling deliberately studies the attacker's perspective.

## Notes
- Threat modeling is not about predicting every attack. It is about systematically reducing blind spots.
