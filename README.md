# JustKaizen AI: People Analytics Insights

Workforce insights and executive reporting for **JustKaizen AI**, a pre-IPO enterprise AI company (1,200 employees, remote-first). This repository translates raw workforce data into findings, recommendations, and action plans that inform People team and executive decision-making.

Built on the data infrastructure published in the companion repository: **[People Analytics Data Infrastructure](https://github.com/keenanj-analytics/people-analytics-data-infrastructure)**

---

## Executive Summary

JustKaizen AI's workforce is under pressure. After three years of hypergrowth (133 to 1,235 employees, 110% CAGR from 2021 to 2023), a reduction in force in early 2024, and a recovery year in 2025, the company entered 2026 with a target of 3% headcount growth. Instead, headcount declined 1.7% in Q1 2026, dropping from 1,221 to 1,200.

The root cause is attrition outpacing hiring. The 3-month annualized attrition rate hit 33.4% in Q1 2026, more than triple the 9.9% rate from a year prior. The 12-month trailing rate stands at 22.2%, confirming this is a sustained acceleration and not a single-quarter spike. Over half of departures (52%) are regrettable, and 26% involve top performers. The highest-attrition departments -- Customer Success (42%), Sales (37%), and Engineering (36%) -- are also the company's three largest revenue-generating functions.

On the hiring side, JustKaizen is closing only 56% of offers extended (TTM), well below the SHRM benchmark of 90%. Engineering, the largest department and the one losing the most people, has a 50% offer acceptance rate. The company is bleeding talent it cannot replace at current offer competitiveness.

Engagement survey data reinforces the pattern. Sales has the lowest overall engagement score (3.49/5.00), and the three weakest themes org-wide -- Recognition (3.53), Career Growth (3.56), and Communication (3.57) -- align directly with the top voluntary termination reasons: Career Opportunities (36%), Work-Life Balance (18%), and Compensation (15%).

Compensation appears structurally sound at the org level (average compa-ratio of 1.00), but this masks department-level compression in Engineering (0.992) and Executive (0.986), and a meaningful gap for Non-Binary employees (0.989 vs. 1.000 for Men and Women).

The sections below present findings by domain, each structured as: what the data shows, why it matters, and what action to take.

---

## Table of Contents

| # | Domain | Key Question | Status |
|---|--------|-------------|--------|
| 1 | [Workforce Composition](docs/01_workforce_composition.md) | Is the organization growing at a healthy rate? Where is growth concentrated? | Complete |
| 2 | [Attrition](docs/02_attrition.md) | Are we losing people faster than we should be? Are we losing the right or wrong people? | Complete |
| 3 | [Hiring Pipeline](docs/03_hiring.md) | Are we filling roles fast enough? Where is the pipeline breaking down? | Complete |
| 4 | [Compensation](docs/04_compensation.md) | Are we paying equitably within peer cohorts? Where are compa-ratio outliers? | Complete |
| 5 | [Engagement](docs/05_engagement.md) | Which teams are engaged and which are disengaging? What themes are driving the gap? | Complete |
| 6 | [Performance](docs/06_performance.md) | Is our rating distribution healthy or inflated? Where is top talent concentrated? | Complete |
| 7 | [Cross-Domain Insights](docs/07_cross_domain_insights.md) | Where do workforce signals compound across domains? | Complete |

Supporting documentation: [Methodology](methodology.md)

---

## Dashboards

Interactive Tableau dashboards supporting these findings are available at: **[Tableau Public](https://public.tableau.com/)** (Coming Soon)

Dashboard screenshots are stored in the [`dashboards/`](dashboards/) directory.

---

## About

Analysis by **[Keenan Artis](https://www.linkedin.com/in/keenanjeffreyartis/)**, an analytics engineer with 7+ years across forensics analytics (PwC) and people analytics. This analysis is modeled after executive workforce reviews delivered to CHROs and VPs of People at a 1,200-person tech company, adapted for portfolio presentation. All data is synthetic; all analytical frameworks, business logic, and interpretive narratives are original work by the author.
