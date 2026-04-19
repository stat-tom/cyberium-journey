# Lesson 6.1 - Introduction to Information Gathering and OSINT

## Status
- Planned

## Introduction
In this lesson, you will learn the basics of reconnaissance and OSINT: collecting information from publicly available sources. You will discover how to build a profile of an organization that is the target of a penetration test.

## Learning Objectives
- Distinguish reconnaissance types: passive, active, and enumeration.
- Gather information about an organization: locations, personnel, metadata, contact details, and business data.
- Use `exiftool` to read file metadata as part of OSINT.

## Reconnaissance Types
- Passive reconnaissance: collecting information without direct interaction with the target. Examples include search engines, public records, certificates, social media, and open data.
- Active reconnaissance: actions that involve direct interaction with the target, such as DNS queries, website requests, port scans, login attempts, or service checks. This includes sending requests and receiving responses to verify reachable hosts and exposed services.
- Enumeration: a more detailed, active technique that uses reconnaissance results to analyze services, machines, and applications. It often includes iterating through user names or other identifiers to identify valid accounts and accessible resources.

## Active Reconnaissance Examples
- Login attempts: testing authentication pages and protocols to identify valid accounts, response behavior, and possible weak credentials.
- Port scanning: using tools like `nmap`, `Nessus`, and `Nikto` to discover open ports, services, and web application issues.

## Enumeration Examples
- Services, machines, and applications: enumerating specific targets, checking service banners, versions, and configurations.
- User identification by iteration: attempting username lists, common account names, or patterns to determine which accounts exist.
- Active technique: enumeration is usually an active process that builds on reconnaissance findings and provides higher-resolution detail about the target environment.

## What to Collect About an Organization
- Locations: office addresses, branches, maps, geographic footprint, and facility details.
- Exterior and interior photos: publicly available images of buildings, entrances, parking, and workspace areas.
- Physical security: camera placement, window protections, fences, gates, and visible access controls.
- Personnel: executives, IT staff, security teams, public profiles, and job advertisements.
- File metadata: hidden data in documents, presentations, and images that may reveal software versions, directory structures, or author information.
- Contact information: email addresses, phone numbers, fax numbers, social media profiles, and contact forms.
- Business information: corporate details, company registries, tax IDs, financial reports, partnerships, and contractual relationships.

## Metadata and `exiftool`
- `exiftool` is a platform-independent command-line application and Perl library for reading, writing, and editing metadata in a wide variety of file types.
- It supports many metadata formats, including EXIF, GPS, IPTC, XMP, JFIF, GeoTIFF, ICC Profile, Photoshop, FlashPix, ID3, and more.
- Beyond images, `exiftool` can read metadata from PDFs, Office documents, videos, audio files, RAW camera files, archives, and other document formats.
- OSINT analysts use it to extract hidden timestamps, GPS coordinates, author names, camera models, software versions, and other contextual clues from files.
- `exiftool` is available as a Windows executable package, a MacOS package, and as a Perl script for Unix-like systems. It works on Windows, macOS, and Linux.
- Example usage:
  - `exiftool filename.jpg` – show all metadata for one file.
  - `exiftool -r directory/` – recursively read metadata from a directory tree.
  - `exiftool -json file.jpg > metadata.json` – export metadata in JSON format.
  - `exiftool -tagsFromFile source.jpg -all:all dest.jpg` – copy metadata from one file to another.
- Useful `exiftool` options for OSINT:
  - `-gps:all` to filter GPS-related tags.
  - `-CreateDate -ModifyDate -DateTimeOriginal` to show timestamps.
  - `-s -G` to display raw tag names with group information.
  - `-diff file1.jpg file2.jpg` to compare metadata differences between files.
- When metadata reveals the program or tool used to generate a file, that software becomes a valuable intelligence lead. Knowing the application or library used can help you search for known vulnerabilities, version-specific bugs, and misconfiguration issues related to that software.
- Example: if metadata indicates a document was created with WPS Office, you can search for "WPS Office vulnerabilities 2026" to identify recent CVEs and security advisories affecting that software.

## OSINT Techniques
- Collecting information about the organization: public profiles, leadership, locations, and corporate structure.
- Gathering infrastructure information: domains, hosts, network architecture, exposed services, and technology stacks.
- Collecting other data: documents, leaked credentials, social engineering clues, and external relationships.

## Why Reconnaissance Matters
- Good preparation reduces guesswork and helps you understand the real attack surface.
- It identifies technologies, assets, naming patterns, employees, and trust relationships.
- The more accurate the early information, the more efficient later testing becomes.

## Note
Reconnaissance must remain within scope, legality, and ethical boundaries. Public information may be outdated or misleading, so it should be verified in later stages.