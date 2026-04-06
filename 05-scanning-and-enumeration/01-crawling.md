# Lesson 1 - Crawling

## Status
- Planned

## Definition
- Crawling is the process of systematically following links and collecting content from a web application to map its reachable structure.
- It helps identify pages, parameters, directories, APIs, forms, and static resources that may deserve closer testing.

## Why Crawling Matters
- Applications are often larger than the visible navigation suggests.
- Hidden routes, archived content, and forgotten endpoints may expose sensitive functionality.
- A better application map improves later testing for authentication, authorization, and input handling flaws.

## Typical Targets
- Public pages, linked assets, and JavaScript files.
- Forms, query parameters, and API endpoints.
- Directories, backups, admin paths, and references in client-side code.

## Manual and Automated Approaches
- Manual browsing helps understand workflows and business logic.
- Automated crawling finds breadth quickly and helps collect large sets of URLs.
- The best results usually come from combining both methods.

## Notes
- Crawling is more useful when findings are organized into routes, parameters, roles, and trust boundaries rather than just a long list of URLs.