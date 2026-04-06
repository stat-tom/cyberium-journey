# Lesson 5 - Nmap - Service Enumeration

## Status
- Planned

## Definition
- Service enumeration is the process of learning more about an exposed service after a port is identified as reachable.
- With Nmap, this usually includes version detection, scripts, protocol behavior, and additional context around what is running.

## Why It Matters
- An open port alone gives limited value.
- Knowing the protocol, product, and likely version helps prioritize relevant vulnerabilities and follow-up tests.
- Enumeration can also reveal weak configurations, anonymous access, or unexpected services.

## Common Enumeration Goals
- Identify the service and probable version.
- Confirm whether default scripts reveal useful metadata.
- Detect certificates, banners, supported methods, or misconfigurations.
- Separate real services from misleading or filtered responses.

## Practical Caution
- Enumeration can generate more noticeable traffic than simple discovery.
- Some scripts are intrusive and must be used only when the scope allows them.
- Results should be confirmed with additional evidence where possible.

## Notes
- Enumeration turns a list of ports into a clearer picture of the exposed stack and its likely weaknesses.