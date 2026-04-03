# Playwright Security Tests

Automated security tests written with [Playwright](https://playwright.dev/).

## Purpose

Use Playwright to automate browser-based security checks such as:
- Verifying security headers (CSP, HSTS, X-Frame-Options, etc.)
- Testing authentication flows for common vulnerabilities
- Detecting exposed sensitive information in HTTP responses

## Getting Started

```bash
npm install
npx playwright test
```

## Structure

```
playwright-security-tests/
├── tests/          # Test files
├── playwright.config.ts
└── package.json
```
