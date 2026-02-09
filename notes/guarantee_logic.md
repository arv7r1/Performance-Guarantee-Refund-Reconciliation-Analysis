# Guarantee Evaluation Logic

This document describes how contractual performance guarantees are evaluated.

## Evaluation Grain
- Site × Month

Each row represents a single contractual evaluation period for one site.

## Breach Determination
A breach occurs when:

actual_energy_kwh < guaranteed_energy_kwh

If this condition is met:
- The site is marked as BREACH
- Energy shortfall is calculated

Otherwise:
- The site is marked as COMPLIANT
- Shortfall is zero

## Shortfall Calculation
shortfall_kwh = max(guaranteed_energy_kwh - actual_energy_kwh, 0)

This ensures:
- No negative shortfalls
- Overperformance does not generate penalties

## Refund Calculation
refund_amount_usd = shortfall_kwh × energy_rate_per_kwh

Refunds apply only to breached periods.

## Aggregation Logic
Refunds and breach counts are aggregated:
- By site (installation-level risk)
- By region (geographic concentration of risk)
- Across the portfolio (total exposure)

This logic mirrors common operational practices for managing performance guarantees in energy portfolios.
