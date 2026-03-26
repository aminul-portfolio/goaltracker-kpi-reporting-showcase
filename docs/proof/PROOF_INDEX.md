# GoalTracker — Proof Index

> A fast review path through the strongest public proof surfaces in the **GoalTracker — KPI Tracking & BI Reporting** showcase.

---

## Purpose

This document exists to:

- reduce reviewer effort
- highlight the highest-signal assets first
- show what the project proves without requiring access to the private codebase

---

## Quick Review — Start Here

If you only have a few minutes, review these in order:

| # | Asset | Path |
|---|---|---|
| 1 | **KPI Dashboard** | `screenshots/goaltracker_01_kpi_dashboard.png` |
| 2 | **Snapshot History** | `screenshots/goaltracker_03_snapshot_history.png` |
| 3 | **Export Hub** | `screenshots/goaltracker_05_exports_hub.png` |
| 4 | **Power BI Dashboard** | `screenshots/goaltracker_06_powerbi_dashboard.png` |
| 5 | **KPI Definitions** | [`../kpi-definitions.md`](../kpi-definitions.md) |

This order moves from headline KPI proof → persisted reporting logic → export and BI proof → metric-definition clarity.

---

## What This Project Proves

GoalTracker is the portfolio's main proof asset for:

| Capability | What it demonstrates |
|---|---|
| **KPI modelling** | Quality-weighted effective minutes, not just raw time logging |
| **Snapshot reporting** | Persisted day and week summaries designed for recurring review |
| **Target vs actual analysis** | Attainment % and rating surfaced at the day and sprint level |
| **Business-facing interpretation** | Outputs designed for analysts, reporting teams, and managers |
| **BI-oriented export design** | Structured dataset delivery for downstream spreadsheet and BI use |
| **End-to-end proof** | From session capture through KPI logic to reporting and BI-facing outputs |

This is what makes it different from a simple productivity tracker or time logger.

---

## Recommended Review Path

### 1 — KPI Dashboard
`screenshots/goaltracker_01_kpi_dashboard.png`

**What to look for**

- target vs actual progress
- raw vs effective minutes
- category contribution
- pace and summary visibility
- business-facing reporting layout

**What it proves**

> The project has a true KPI layer. The reporting surface is designed for interpretation, not just record display.

---

### 2 — Daily Tracking Workflow
`screenshots/goaltracker_02_today_tracking.png`

**What to look for**

- operational capture workflow
- quality-level input
- timer/session structure
- source layer feeding the KPI model

**What it proves**

> The analytics outputs are grounded in a structured operational input flow. The KPI model is not disconnected from how data is captured.

---

### 3 — Snapshot History
`screenshots/goaltracker_03_snapshot_history.png`

**What to look for**

- persisted reporting history
- daily and weekly review surfaces
- trend visibility across time
- performance cadence beyond single-day reporting

**What it proves**

> The project stores reporting outputs at the snapshot level. Reporting is designed for repeatable historical review, not only live recalculation.

---

### 4 — Day Snapshot Detail
`screenshots/goaltracker_04_day_snapshot_detail.png`

**What to look for**

- day-level attainment
- rating
- supporting session evidence
- how performance is explained, not only measured

**What it proves**

> The project connects summary KPIs back to supporting operational detail. Daily reporting is interpretable, not just numeric.

---

### 5 — Export Hub
`screenshots/goaltracker_05_exports_hub.png`

**What to look for**

- reporting-oriented export surfaces
- legacy CSV outputs for direct review
- BI-oriented export structure
- evidence of downstream dataset thinking

**What it proves**

> The project goes beyond dashboards. Outputs are designed for downstream spreadsheet and BI use. Reporting delivery is part of the product story.

---

### 6 — Power BI Dashboard
`screenshots/goaltracker_06_powerbi_dashboard.png`

**What to look for**

- downstream reporting consumption
- KPI visibility outside the Django interface
- BI-facing presentation of exported data

**What it proves**

> The export dataset supports reporting beyond the source application. The project has credible BI/reporting positioning, not only in-app charts.

---

## Supporting Document — KPI Glossary

**File:** [`../kpi-definitions.md`](../kpi-definitions.md)

This is one of the strongest supporting documents in the showcase. It proves that the KPI model is defined clearly, not just displayed visually.

Use it to review:

| Metric | What it covers |
|---|---|
| Raw Minutes | Unweighted baseline measure |
| Effective Minutes | Quality-weighted primary KPI |
| Quality Multiplier | Weighting logic applied to sessions |
| Target Minutes | Configured performance benchmark |
| Attainment % | Progress against target |
| Rating | Business-readable performance label |
| Day Snapshot | Persisted daily reporting summary |
| Week Snapshot | Persisted weekly reporting rollup |
| MAE Block | Morning / Afternoon / Evening distribution |
| Reporting windows | Day / week / month / sprint-level logic |

---

## Role Fit

| Role | Strongest proof areas |
|---|---|
| **BI Analyst** | KPI definitions, snapshot reporting, export design, Power BI output |
| **Data Analyst** | Target vs actual, category breakdowns, weighted performance modelling |
| **Reporting Analyst** | Recurring summaries, export delivery, manager-facing interpretation |
| **Analytics Engineer** | Structured metric logic, persisted snapshot layer, dataset design |

Secondary fit: **Python / Django data-product roles**

---

## Why This Project Is Distinct in the Portfolio

GoalTracker is the portfolio project that most directly proves KPI logic, snapshot design, reporting cadence, and BI-oriented outputs.

It complements the other portfolio projects by focusing on **internal performance data and reporting design** — rather than event ETL, external/API ingestion, or transactional commerce analytics.

| Project | Data category |
|---|---|
| CineScope Analytics | Event / activity data |
| DataBridge Market API | External / API-driven data |
| PureLaka Commerce Platform | Transactional business data |
| **GoalTracker** | Internal performance data |

That distinction rounds out the broader portfolio story across four different data categories.

---

## Public vs Private Review

This repository is a **public showcase version** providing screenshots, KPI definitions, proof-oriented documentation, and reviewer guidance.

The full implementation is maintained privately. The public review focuses on:

- what the project proves
- how the KPI and reporting logic is framed
- what outputs a reviewer can inspect directly

rather than full code-level implementation details.

---

## Three Things to Remember

If you remember only three things about GoalTracker, they should be:

| # | What to remember |
|---|---|
| 1 | GoalTracker is a **KPI-first analytics and BI/reporting project** — not a habit tracker |
| 2 | Its strongest proof areas are **effective-minutes logic, snapshot reporting, and BI-oriented exports** |
| 3 | It is the portfolio project that best demonstrates **business-facing performance interpretation** |
