# Lesson 3 - Discovering Hosts in Networks

## Status
- Planned

## Objective
- Identify which IP addresses in a given scope are alive and worth deeper testing.

## Common Techniques
- ICMP echo requests to detect responsive hosts.
- ARP-based discovery on local networks.
- TCP or UDP probes to ports that commonly respond.
- Passive observation where network visibility is available and authorized.

## Why Host Discovery Is Not Simple
- Some hosts block ICMP but respond on TCP services.
- Firewalls and rate limits can hide live systems.
- Cloud and segmented environments may behave differently from flat local networks.

## Good Practice
- Use more than one discovery method when results matter.
- Keep careful notes about which technique produced each result.
- Distinguish between no response and confirmed absence.

## Notes
- Host discovery is the bridge between raw scope and targeted enumeration.