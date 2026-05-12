# Methodology

## Data Infrastructure

All analyses in this repository are built on a production-grade dbt data warehouse documented in the companion repository: **[People Analytics Data Infrastructure](https://github.com/keenanj-analytics/people-analytics-data-infrastructure)**. The infrastructure includes 25 dbt models across staging, intermediate, and mart layers, deployed to Google BigQuery.

## Source Systems

Five source systems feed the warehouse:

| Source | Records | Update Cadence |
|--------|---------|---------------|
| HRIS (Employee Census) | ~65,000+ rows (monthly snapshots) | Monthly |
| ATS (Recruiting Pipeline) | ~30,000+ rows | Continuous |
| Performance Management | ~15,000+ rows | Semi-annual review cycles |
| Engagement Survey | ~25,000+ rows | Semi-annual |
| Compensation Bands | ~200+ rows | Annual |

## Key Metric Definitions

**Headcount:** Count of active employees at end of month/quarter. An employee is active if their hire date is on or before the month-end and their termination date is null or after the month-start.

**TTM (Trailing Twelve-Month) Attrition Rate:** Total terminations in the prior 12 months divided by the average headcount over the same 12 months. This smooths seasonal variation and provides a structural view of attrition trends.

**R3M Annualized Attrition Rate:** Total terminations in the prior 3 months divided by the average headcount over the same 3 months, multiplied by 4 to project an annual rate. This captures recent acceleration or deceleration in attrition that the TTM rate would smooth out. Because it projects a 3-month pace over 12 months, it can overstate or understate the full-year rate if the pace changes.

**Compa-Ratio:** Employee salary divided by the midpoint of their assigned compensation band. A value of 1.000 means the employee is paid exactly at midpoint. Values below 1.000 indicate below-midpoint pay; above 1.000 indicates above-midpoint pay.

**Below Band / Above Band:** Employees whose compa-ratio falls below the band minimum or above the band maximum. These employees are outside the defined competitive range for their role and level.

**Top Performer:** An employee with a most recent performance rating of 4 or higher (Exceeds Expectations or Significantly Exceeds Expectations) or who has been flagged as critical talent by their manager.

**Regrettable Attrition:** A termination where the departing employee's manager classifies the loss as regrettable. This is a subjective assessment made at time of exit and reflects whether the organization wanted to retain the employee.

**Offer Acceptance Rate:** Offers accepted divided by total offers extended, measured over a rolling window (TTM or R3M).

**Time-to-Fill:** Calendar days from requisition open date to the hired candidate's start date. Internal transfers are excluded from time-to-fill calculations.

**Engagement Score:** Average response on a 1-5 Likert scale within a given theme (e.g., Career Growth, Recognition). Scores are aggregated at the department level; individual responses are anonymized.

**Favorable %:** Proportion of survey responses scoring 4 or 5 on the 1-5 scale. Scores of 1-3 are classified as neutral or unfavorable.

## Reporting Grids and Zero-Fill

All reporting marts use a scaffold (reporting grid) pattern that cross-joins calendar months with every observed dimension combination. This ensures that a month where a given segment has zero terminations, zero hires, or zero headcount still produces a row with a zero value rather than a missing row. Without this pattern, trend lines would break and rolling window calculations would miscalculate averages.

## Rolling Window Calculations

TTM and R3M metrics are computed using SQL window functions partitioned by dimension combination and ordered by month. The TTM window spans 11 preceding rows plus the current row (12 months total). The R3M window spans 2 preceding rows plus the current row (3 months total). Both use SUM for counts and AVG for denominators, ensuring that structural events (like a RIF) are smoothed into the average headcount rather than creating a spike in the rate.

## Data Freshness

All data in this analysis reflects the state as of March 2026 (2026 Q1). Engagement survey data is from the 2025 H2 cycle (the most recent available). Performance ratings are from the 2025 Year-End Review Cycle.

## Limitations

**Synthetic data.** All source data is synthetically generated to model a realistic pre-IPO tech company. Patterns and distributions are designed to reflect plausible workforce dynamics, but no actual employee data is used. Analytical frameworks, metric definitions, and interpretive narratives are original work by the author.

**Point-in-time snapshots.** The HRIS data uses end-of-month snapshots. Events occurring mid-month (transfers, promotions, manager changes) are captured at the next month-end snapshot, not at their exact effective date.

**Engagement anonymization.** Survey data is aggregated at the department level. Individual-level correlations (e.g., "do employees with low engagement scores have higher attrition?") cannot be computed because individual responses are not linked to employee IDs.

**Offer decline reasons.** The recruiting pipeline tracks whether an offer was accepted or declined but does not capture the reason for decline. Recommendations regarding offer competitiveness are inferred from the acceptance rate relative to industry benchmarks, not from direct candidate feedback.
