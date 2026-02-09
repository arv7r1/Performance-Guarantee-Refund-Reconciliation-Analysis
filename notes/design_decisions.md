# Design Decisions

This document explains key analytical and structural decisions made during the project.

## Use of Excel
Excel was selected as the primary analysis tool because:
- It is commonly used for rapid validation and auditing in energy operations.
- PivotTables and formulas allow fast portfolio-level aggregation.
- Stakeholders can review results without specialized tooling.

## Separation of Actual vs Contract Data
Actual production data and contractual guarantees are maintained in separate tables to:
- Preserve auditability
- Reflect real-world operational data flows
- Avoid circular logic in performance evaluation

## Deterministic Calculations
Randomized values were used only to seed synthetic data and were subsequently frozen to:
- Ensure repeatable results
- Prevent recalculation drift
- Support reliable PivotTable aggregation

## Portfolio-Level Aggregation
PivotTables were used to:
- Summarize refund exposure by site and region
- Rank installations by financial risk
- Enable executive-level decision-making

## Visualization Choices
Only high-signal charts were created:
- Refund exposure by site
- Breach frequency by site
- Refund exposure by region

These visuals prioritize clarity and actionability over visual complexity.
