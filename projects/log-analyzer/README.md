# Log Analyzer

A tool for parsing and analyzing security-relevant log files.

## Purpose

Automate detection of suspicious patterns in logs, such as:
- Brute-force login attempts
- Unusual access times or IP addresses
- Error spikes indicating scanning activity

## Getting Started

```bash
python log_analyzer.py --file /var/log/auth.log
```

## Structure

```
log-analyzer/
├── log_analyzer.py   # Main script
├── patterns/         # Detection rules / regex patterns
└── samples/          # Sample log files for testing
```
