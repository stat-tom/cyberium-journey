# Lesson 2 - Network Scanning - Introduction

## Status
- Planned

## Overview
- Network scanning is the process of probing hosts and services to learn what systems are reachable and what they expose.
- It is one of the main ways to turn a vague target range into a concrete set of assets for testing.

## Core Goals
- Discover which systems are online.
- Identify open, closed, or filtered ports.
- Learn which services and protocols are reachable.
- Support later fingerprinting, enumeration, and validation.

## Main Tradeoffs
- Faster scans cover more ground but create more noise and may miss detail.
- Careful scans provide richer information but take longer and may still be detected.
- The right balance depends on scope, rules of engagement, and target sensitivity.

## Key Considerations
- Respect authorization and timing constraints.
- Understand whether firewalls, NAT, IDS, or rate limits may affect the results.
- Treat scan output as evidence to validate, not as final truth.

## Notes
- Good scanning is deliberate. It is not about launching the loudest command, but about collecting useful information with controlled risk.