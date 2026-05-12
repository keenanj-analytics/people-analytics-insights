# 4. Compensation

**Question:** Are we paying equitably within peer cohorts? Where are compa-ratio outliers?

---

## Key Findings

**JustKaizen's compensation structure appears healthy at the org level but masks department-level compression and a meaningful equity gap for Non-Binary employees.** The org-wide average compa-ratio is 1.000 (exactly at band midpoint), and the average salary is $145,191. However, Engineering (0.992) and Executive (0.986) are both below midpoint, and Non-Binary employees have a compa-ratio of 0.989 vs. 1.000 for Men and Women. Across the organization, 85 employees (7%) sit below their compensation band -- a manageable number for targeted correction, but one that grows more urgent when cross-referenced with the departments experiencing the highest attrition.

---

## Org-Wide Compensation

| Metric | Value |
|--------|-------|
| Average Salary | $145,191 |
| Average Compa-Ratio | 1.000 |
| Employees Below Band | 85 (7%) |
| Employees Above Band | 87 (7%) |

A compa-ratio of 1.000 means the average employee is paid exactly at the midpoint of their compensation band. The near-symmetric distribution of below-band (85) and above-band (87) employees suggests the band structure is well-calibrated to current pay levels. This is a positive signal for the compensation framework itself.

---

## Department Compa-Ratios

| Department | Avg Compa-Ratio | Below Band | Above Band | Employees |
|-----------|----------------|------------|------------|-----------|
| Sales | 1.008 | 11 (6%) | 15 (8%) | 200 |
| G&A | 1.008 | 3 (3%) | 12 (11%) | 110 |
| People | 1.007 | 8 (10%) | 7 (9%) | 80 |
| Product | 1.003 | 9 (9%) | 10 (10%) | 100 |
| Data & Analytics | 1.002 | 3 (5%) | 6 (11%) | 55 |
| Marketing | 1.000 | 9 (9%) | 9 (9%) | 100 |
| Customer Success | 0.996 | 12 (9%) | 10 (8%) | 130 |
| Engineering | 0.992 | 30 (7%) | 24 (6%) | 410 |
| Executive | 0.986 | 0 (0%) | 1 (7%) | 15 |

### Engineering Compression

Engineering has the second-lowest compa-ratio at 0.992 and the largest absolute count of below-band employees (30). For a department of 410 people experiencing 36% annualized attrition with Career Opportunities as the dominant departure reason, below-midpoint compensation is a contributing factor. The 30 below-band engineers represent immediate flight risk -- these are employees whose pay is demonstrably below the company's own defined competitive range.

### Customer Success Underpayment

Customer Success at 0.996 has 12 employees below band (9% of the department). Combined with the 42% annualized attrition rate and Compensation as the #2 departure reason at 20%, this department's pay structure is directly fueling attrition.

---

## Pay Equity: Gender

| Gender | Avg Compa-Ratio | Employees |
|--------|----------------|-----------|
| Men | 1.000 | 615 |
| Women | 1.000 | 541 |
| Non-Binary | 0.989 | 44 |

Men and Women have identical average compa-ratios at 1.000. Non-Binary employees average 0.989, a gap of 1.1 percentage points. While the Non-Binary population is small (44 employees, 3.7% of the workforce), a persistent gap of this magnitude warrants investigation. A compa-ratio of 0.989 means Non-Binary employees are, on average, paid 1.1% below band midpoint -- roughly $1,600 below the midpoint for an employee at the average salary level. This is a correctable gap.

---

## Cross-Referencing Compensation with Attrition

The compensation data becomes most valuable when layered with the attrition findings from [Section 2](02_attrition.md):

**Engineering:** 0.992 compa-ratio + 36% attrition + 50% offer acceptance + "Career Opportunities" as top departure reason. This is a coherent signal: engineers are underpaid relative to band, leaving for better opportunities, and the company cannot close competing candidates. Compensation is a primary lever.

**Customer Success:** 0.996 compa-ratio + 42% attrition + Compensation as #2 reason (20%). The CSM role specifically has 64% annualized attrition. If CSMs are clustered at the bottom of their bands, a targeted adjustment could directly reduce the departure rate.

**Sales:** 1.008 compa-ratio. Sales is the one high-attrition department where compensation does *not* appear to be a factor. The 37% attrition rate in Sales is driven by Manager Relationship (26%) and Career Opportunities (21%), not pay. This confirms that the Sales retention problem requires a different intervention (see [Section 2](02_attrition.md) recommendations).

---

## Recommended Actions

1. **Immediately review and adjust compensation for the 30 below-band engineers.** These employees are below the company's own defined competitive range in the department with the highest absolute attrition volume. This is the single highest-ROI compensation action available.

2. **Investigate the Non-Binary compa-ratio gap.** Determine whether the 0.989 average is driven by level mix (Non-Binary employees concentrated in lower-paid roles) or by within-role pay differences. If within-role, correct immediately. If level mix, address through promotion pipeline analysis.

3. **Conduct a targeted comp review for CSMs and Customer Education roles.** These sub-departments have the highest attrition in Customer Success, and Compensation is the #2 departure reason. Bringing below-band employees to midpoint in these roles is a retention investment with a clear, measurable return.

4. **Do not pursue a broad-based compensation increase.** The org-wide compa-ratio of 1.000 indicates the band structure is sound. The problem is localized to specific departments and roles. Broad increases would spend budget where it is not needed and underinvest where it is.

---

*Data source: fct_compensation_reporting, fct_employee_roster. Compa-ratio = employee salary / compensation band midpoint. Below band = compa-ratio below the defined band minimum. Above band = compa-ratio above the defined band maximum. All figures reflect active, full-time employees as of Q1 2026.*
