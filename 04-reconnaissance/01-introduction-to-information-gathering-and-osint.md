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
- Active reconnaissance: actions that involve direct interaction with the target, such as DNS queries, website requests, port scans, or service checks.
- Enumeration: detailed analysis that uses reconnaissance results as a starting point to identify specific assets, users, and weaknesses.

## What to Collect About an Organization
- Locations and photos: office addresses, branches, maps, and publicly available images of facilities.
- Personnel: executives, IT staff, security teams, public profiles, and job advertisements.
- File metadata: hidden data in documents, presentations, and images that may reveal software versions, directory structures, or author information.
- Contact information: email addresses, phone numbers, fax numbers, social media profiles, and contact forms.
- Business information: corporate details, company registries, tax IDs, financial reports, partnerships, and contractual relationships.

## Metadata and `exiftool`
- `exiftool` is a tool for reading metadata from files such as images, Microsoft Office documents, PDFs, and multimedia files.
- In OSINT, metadata can reveal dates, GPS locations, author names, and application details.
- Example usage: `exiftool filename.jpg`

## Why Reconnaissance Matters
- Good preparation reduces guesswork and helps you understand the real attack surface.
- It identifies technologies, assets, naming patterns, employees, and trust relationships.
- The more accurate the early information, the more efficient later testing becomes.

## Note
Reconnaissance must remain within scope, legality, and ethical boundaries. Public information may be outdated or misleading, so it should be verified in later stages.