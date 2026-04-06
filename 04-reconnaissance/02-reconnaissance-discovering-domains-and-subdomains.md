# Lesson 2 - Reconnaissance - Discovering Domains and Subdomains

## Status
- Planned

## Objective
- Build a clearer map of the target's external presence by identifying domains, subdomains, and related infrastructure.

## Why It Matters
- Organizations often expose many more assets than their main website suggests.
- Subdomains can reveal staging systems, admin panels, forgotten services, APIs, and third-party integrations.
- Naming patterns can hint at internal structures, environments, and technology choices.

## Common Discovery Methods
- Review the target website, certificates, and publicly visible links.
- Query DNS records and inspect certificate transparency logs.
- Use search engines and specialized recon tools to find references to related hosts.
- Check public code repositories, configuration files, and archived web content for leaked hostnames.

## What to Look For
- Internet-facing applications such as portals, APIs, VPN gateways, and mail services.
- Environment markers such as `dev`, `test`, `staging`, `admin`, or region-specific labels.
- Hosts that appear misconfigured, outdated, or disconnected from the main security controls.

## Good Practice
- Validate findings instead of trusting every discovered hostname.
- Separate confirmed live assets from passive leads that still need verification.
- Track the source of each finding so results remain reproducible.

## Notes
- Domain and subdomain discovery is one of the highest-value reconnaissance activities because it expands visibility before any deeper testing begins.