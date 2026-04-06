# Lesson 4 - Nmap - Techniques and Scan Types

## Status
- Planned

## Overview
- Nmap is a widely used network scanning tool for host discovery, port scanning, service detection, and basic scripting.
- Different scan types provide different visibility depending on firewalls, privileges, and target behavior.

## Common Scan Types
- TCP connect scans complete the full connection and work without raw packet privileges.
- SYN scans are often faster and more stealthy because they do not complete the full TCP handshake.
- UDP scans are useful for services such as DNS or SNMP but are often slower and harder to interpret.
- Ping and discovery options help determine whether hosts appear alive before deeper scans begin.

## Choosing a Technique
- Use lighter discovery when you first need to identify live systems.
- Use port scans when you need to understand exposed services.
- Adjust timing and source assumptions carefully to reduce false conclusions.

## Interpreting Results
- `open` suggests a reachable service is listening.
- `closed` suggests the host is reachable but nothing is listening on that port.
- `filtered` suggests a firewall or packet filtering is preventing a clear answer.

## Notes
- Nmap is powerful because it combines many controlled probing methods, but results still require context and validation.