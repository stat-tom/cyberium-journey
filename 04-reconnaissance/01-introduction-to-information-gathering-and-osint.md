# Lesson 1 - Introduction to Information Gathering and OSINT

## Status
- Planned

## Overview
- Reconnaissance is the process of collecting information about a target before active testing begins.
- OSINT, or Open Source Intelligence, focuses on information gathered from publicly available sources.

## Why Reconnaissance Matters
- Good reconnaissance helps reduce guesswork and reveals the real attack surface.
- It identifies technologies, exposed assets, naming patterns, employees, third-party services, and potential trust relationships.
- The more accurate the early information, the more efficient later testing becomes.

## Passive and Active Reconnaissance
- Passive reconnaissance gathers information without directly interacting with the target systems, for example by using search engines, public certificates, or breach datasets.
- Active reconnaissance touches the target more directly, for example through DNS queries, web requests, or service probing.
- Passive methods are usually quieter, while active methods can reveal more detail but create more detectable traffic.

## Common OSINT Sources
- Search engines, company websites, blogs, job postings, and public documentation.
- DNS records, certificate transparency logs, and WHOIS-related data.
- Code repositories, package registries, and exposed configuration files.
- Social media, professional profiles, and public presentations.
- Public breach data and leak monitoring platforms where legally permitted.

## Typical Outcomes
- A list of domains, subdomains, IP addresses, email patterns, technologies, and exposed applications.
- Better hypotheses about where valuable targets or weak points may exist.
- Input for later stages such as crawling, scanning, and validation.

## Notes
- Reconnaissance should stay tied to scope, legality, and evidence quality. Public information can still be inaccurate or outdated.