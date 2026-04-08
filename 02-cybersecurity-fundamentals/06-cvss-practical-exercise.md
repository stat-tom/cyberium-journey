# Lesson 6 - CVSS Practical Exercise

## Status
- Completed

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

## Real CVE Example - CVE-2024-45400

### About the Vulnerability
- CVE-2024-45400 affects `ckeditor-plugin-openlink`, a plugin for the CKEditor JavaScript text editor.
- The plugin adds a context-menu option that lets users open a link in a new tab.
- The flaw is a cross-site scripting issue caused by insufficient sanitization of the `href` value.
- An attacker can abuse the link value to execute JavaScript when malicious content is loaded and the link-opening behavior is triggered.

### What Software Is Affected
- Product: `ckeditor-plugin-openlink`
- Ecosystem context: a plugin used with CKEditor
- Weakness: CWE-79, cross-site scripting

### What Versions Are Vulnerable
- Affected versions: earlier than `1.0.7`
- NVD lists the vulnerable range as up to, but excluding, `1.0.7`
- Fixed version: `1.0.7`

### Reading the CVSS 3.1 Vector
- Vector: `CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N`
- `AV:N` means Attack Vector is Network, so exploitation can happen through remotely delivered content.
- `AC:L` means Attack Complexity is Low, so no unusual conditions are required.
- `PR:N` means Privileges Required is None, so the attacker does not need an account in the vulnerable component.
- `UI:R` means User Interaction is Required, so a user must interact with the malicious content.
- `S:C` means Scope is Changed, so exploitation can impact a different security boundary, such as the victim user's browser session or surrounding application context.
- `C:L` means Confidentiality impact is Low.
- `I:L` means Integrity impact is Low.
- `A:N` means Availability impact is None.
- Overall CVSS base score: `6.1 Medium`

### Was It Patched
- Yes. The issue was patched.
- The fix is available starting with version `1.0.7`.
- The patch tightened protocol sanitization so obfuscated `javascript:` values with embedded whitespace are rejected.

### Why This Is a Good CVSS Exercise
- It shows that a vulnerability can still be important even when availability impact is none.
- It is a useful example of how `UI:R` lowers the score compared with a fully self-triggering remote exploit.
- It also shows why reading the full vector matters: the score alone does not explain that the attack depends on malicious content and user action.

## Reflection Questions
- Would the priority change if the service were internal only?
- Would the priority change if a web application firewall already blocked the exploit path?
- Which metric in the example most strongly drives urgency in your environment?

## Notes
- The goal of the exercise is not to memorize one exact score, but to think clearly about exploitability, impact, and business context.
