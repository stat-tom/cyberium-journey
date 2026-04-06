# Lesson 6 - CVSS Practical Exercise

## Status
- Not completed

## Objective
- Practice reading a vulnerability and translating it into CVSS thinking.

## Example Scenario
- A web application contains an authenticated file upload flaw that allows an attacker to upload and execute a malicious script on the server.
- The vulnerable application is internet-facing and used by employees.

## Step 1 - Identify the Attack Path
- Attack Vector: network, because the attacker can reach the application remotely.
- Attack Complexity: low, if no unusual conditions are required.
- Privileges Required: low, because a normal authenticated user account is enough.
- User Interaction: none, if the attacker can trigger exploitation directly after login.

## Step 2 - Estimate Impact
- Confidentiality impact may be high if the attacker can read server-side data.
- Integrity impact may be high if files or application logic can be modified.
- Availability impact may be high if the attacker can disrupt the application or host.

## Step 3 - Consider Scope
- Scope may be changed if exploitation of the application lets the attacker affect other components outside the original security boundary.

## Step 4 - Prioritize in Context
- The vulnerability deserves urgent attention because it is internet-facing, exploitable through normal user access, and may lead to server compromise.
- If exploit code is public or active attacks are reported, the urgency increases further.

## Practical Workflow
- Confirm that the vulnerable version exists in your environment.
- Check whether the service is reachable by attackers.
- Review vendor advisories and available patches or mitigations.
- Assign technical severity with CVSS.
- Combine that score with business context and exposure.
- Patch, mitigate, retest, and document the outcome.

## Reflection Questions
- Would the priority change if the service were internal only?
- Would the priority change if a web application firewall already blocked the exploit path?
- Which metric in the example most strongly drives urgency in your environment?

## Notes
- The goal of the exercise is not to memorize one exact score, but to think clearly about exploitability, impact, and business context.
