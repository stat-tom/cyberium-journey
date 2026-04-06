# Lesson 9 - Risk Metrics - What Are They and How to Calculate Them?

## Status
- Not completed

## Why Metrics Matter
- Risk metrics turn security concerns into values that can be tracked, compared, and discussed with decision-makers.
- Good metrics help answer whether risk is increasing, decreasing, or being ignored.

## Qualitative Metrics
- Use labels such as low, medium, and high.
- Useful when precise numbers are unavailable.
- Example: likelihood is high because the system is internet-facing and unpatched.

## Quantitative Metrics
- Use numeric estimates to compare potential losses and control benefits.
- Common inputs include asset value, expected loss, frequency of incidents, and time to detect or respond.

## Common Formulas
- Single Loss Expectancy (SLE) = asset value x exposure factor.
- Annualized Rate of Occurrence (ARO) = expected number of incidents per year.
- Annualized Loss Expectancy (ALE) = SLE x ARO.

## Example Calculation
- Asset value: 100,000 USD.
- Exposure factor: 0.25, meaning one incident is expected to cause a 25 percent loss.
- SLE = 25,000 USD.
- ARO = 0.4, meaning the event is expected once every 2.5 years.
- ALE = 10,000 USD per year.

## Operational Security Metrics
- Mean time to detect incidents.
- Mean time to respond or contain.
- Patch latency for critical vulnerabilities.
- Number of high-risk findings over time.
- Percentage of systems with multi-factor authentication enabled.
- Backup restoration success rate.

## Limitations
- Metrics are only as good as the assumptions and data behind them.
- Overly precise numbers can create false confidence.
- Metrics should support decisions, not replace expert judgment.

## Notes
- The best metrics are consistent, understandable, tied to business impact, and reviewed regularly.
