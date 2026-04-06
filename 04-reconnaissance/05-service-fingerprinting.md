# Lesson 4 - Service Fingerprinting

## Status
- Planned

## Definition
- Service fingerprinting is the process of identifying what software, protocol, version, or framework is running on a target service.
- It helps determine what technology is exposed and which vulnerabilities or misconfigurations may apply.

## Common Targets
- Web servers and reverse proxies.
- Application frameworks and content management systems.
- SSH, FTP, SMTP, DNS, and other network services.
- APIs that reveal framework behavior through headers, error messages, or response formats.

## Ways Fingerprinting Happens
- Reading banners, headers, certificates, and default error pages.
- Comparing response behavior across different requests.
- Looking for static files, metadata, routes, or version-specific features.
- Using controlled probing tools during authorized active reconnaissance.

## Why It Matters
- Identifying the exact stack helps prioritize known weaknesses and relevant tests.
- Version clues can show whether software is outdated or poorly maintained.
- Fingerprinting also helps defenders understand what information their systems leak unnecessarily.

## Defensive Perspective
- Reduce unnecessary banners and verbose error messages.
- Keep versions patched and monitor internet-facing assets for unexpected exposure.
- Assume motivated attackers will combine many small signals to identify the stack.

## Notes
- Fingerprinting is rarely based on one perfect clue. It usually comes from multiple weak signals combined into a confident conclusion.