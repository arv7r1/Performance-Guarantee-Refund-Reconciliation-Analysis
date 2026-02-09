# Assumptions

This analysis is based on the following assumptions to reflect realistic energy operations and contractual evaluation scenarios:

## Operational Assumptions
- Energy production is evaluated on a monthly basis per site.
- Each site has a single contractual energy guarantee per month.
- Actual energy production is sourced from metered system data.
- Energy shortfall is calculated only when actual production is below guaranteed levels.

## Contractual Assumptions
- Guaranteed energy values are fixed for the evaluation period and do not change based on actual performance.
- Refunds apply only to the energy shortfall (overperformance does not generate credits).
- Energy rates are fixed per site-period and defined contractually.

## Financial Assumptions
- Refund exposure is calculated as:
  
  shortfall_kwh × energy_rate_per_kwh

- All refund amounts are expressed in USD.
- Rounding is applied to currency values for reporting clarity.

## Data Assumptions
- Synthetic data is used to simulate realistic fleet behavior.
- Values are frozen to ensure repeatability and auditability.

These assumptions are intentionally conservative and designed to mirror common industry practices for performance guarantee evaluation.
