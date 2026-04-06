# Lesson 2 Lab - Enumerating Subdomains (vhosts)

## Status
- Planned

## Objective
- Practice identifying subdomains and virtual hosts that may expose additional applications or environments.

## Lab Setup
- Use a legal lab target or a training environment you control.
- Prepare basic recon tools such as `nslookup`, `dig`, `host`, or a dedicated subdomain enumeration tool.
- If virtual host fuzzing is part of the lab, ensure you have an IP address or host that resolves and accepts HTTP requests.

## Tasks
- Task 1:
	- Identify the main domain and review any obvious subdomains linked from the site.
	- Check certificate transparency results or other public sources for additional hostnames.
- Task 2:
	- Attempt passive enumeration and record candidate subdomains.
	- Resolve each finding to determine which names are live.
- Task 3:
	- If the lab supports vhost discovery, send requests with different `Host` headers and note which responses change.
	- Separate default responses from meaningful application responses.

## Expected Output
- A list of confirmed subdomains or virtual hosts.
- Notes about which hosts resolved, which responded over HTTP or HTTPS, and which appeared inactive.
- A short conclusion about which targets deserve deeper review.

## Notes
- Virtual host enumeration can reveal hidden applications behind a shared IP address.
- False positives are common, so response comparison matters.