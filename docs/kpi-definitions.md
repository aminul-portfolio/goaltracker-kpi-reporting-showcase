# GoalTracker KPI Definitions

This document defines the core metrics used in **GoalTracker**.

The purpose of this project is not only to display charts, but to show how KPI logic can be designed, documented, and communicated in a way that is useful to analysts, reporting teams, and managers.

---

## Why These KPI Definitions Matter

GoalTracker is intended to show that strong analytics work is not just about collecting activity data.

It also requires the ability to:

- define the KPI clearly
- explain how it is calculated
- distinguish input data from reporting outputs
- persist summaries at the right reporting level
- present results in a business-interpretable format

That KPI definition and interpretation layer is a core part of what this project is designed to demonstrate.

---

## KPI Calculation Principle

GoalTracker is built around a simple idea:

```
Effective Minutes = Raw Duration × Quality Multiplier
```

This means the project does not treat all logged time as equally valuable. A session completed at higher quality contributes more to performance than the same duration completed at lower quality.

That weighting logic is what differentiates GoalTracker from a basic time logger.

---

## 1. Raw Minutes

**Definition**
Actual logged minutes between `start_at` and `end_at`.

**Purpose**
Acts as the unweighted baseline measure of recorded activity.

**Business interpretation**
Useful for understanding how much time was logged, but not sufficient on its own as a performance KPI.

**Example**
A 90-minute session contributes 90 raw minutes.

---

## 2. Effective Minutes

**Definition**
Quality-weighted minutes derived from session duration and quality multiplier.

```
Effective Minutes = Raw Duration × Quality Multiplier
```

**Purpose**
This is the project's primary KPI.

**Business interpretation**
Models the idea that meaningful output depends on both time invested and the quality of work completed during that time.

**Example**
A 90-minute session with a multiplier of 1.25 contributes 112.5 effective minutes.

---

## 3. Quality Multiplier

**Definition**
A weighting factor applied to a session based on its recorded quality level.

**Purpose**
Allows the reporting model to distinguish between lower-value and higher-value working time.

**Business interpretation**
Makes performance reporting more realistic by reflecting that not all recorded time contributes equally to useful output.

**Example**

| Quality level | Effect |
|---|---|
| Lower-quality session | Smaller contribution to effective minutes |
| Standard-quality session | Baseline contribution |
| Higher-quality session | Larger contribution to effective minutes |

Exact multiplier values can vary by project configuration.

---

## 4. Target Minutes

**Definition**
Configured benchmark representing the intended level of effective minutes across a reporting window.

**Purpose**
Provides the target used for progress and attainment calculations.

**Business interpretation**
Functions as the reference point for determining whether performance is behind, on track, or ahead.

**Example**
If a reporting window target is 600 effective minutes, then all attainment calculations are measured against that benchmark.

---

## 5. Attainment %

**Definition**

```
Attainment % = (Effective Minutes ÷ Target Minutes) × 100
```

**Purpose**
Measures progress against the configured target.

**Business interpretation**
One of the project's main business-facing outputs — it converts activity into a simple, readable performance ratio.

**Example**

| Input | Value |
|---|---|
| Effective minutes | 480 |
| Target minutes | 600 |
| Attainment % | **80%** — currently below target |

---

## 6. Rating

**Definition**
A human-readable performance label stored on snapshots.

**Purpose**
Summarises performance in a way that is easy for a reviewer or manager to interpret quickly.

**Business interpretation**
Converts numeric KPI output into an immediately understandable status signal.

**Example labels**

| Label | Meaning |
|---|---|
| Behind | Below expected pace |
| Good | Meeting baseline expectations |
| Better | Above expected pace |
| Excellent | Significantly ahead of target |

The exact threshold logic depends on the project configuration and reporting rules.

---

## 7. Day Snapshot

**Definition**
A persisted daily reporting summary derived from session activity.

**Purpose**
Stores day-level performance outputs rather than requiring repeated recalculation every time a report is viewed.

**Business interpretation**
Supports recurring daily reporting and historical review.

**Typical contents**

- raw minutes
- effective minutes
- target minutes
- attainment %
- rating
- supporting day-level context

---

## 8. Week Snapshot

**Definition**
A persisted weekly reporting summary built from day-level activity and/or snapshot logic.

**Purpose**
Creates a repeatable weekly reporting layer.

**Business interpretation**
Supports reporting workflows where weekly cadence matters more than raw event detail.

**Typical contents**

- aggregated minutes
- weekly attainment
- summary rating
- weekly trend context

---

## 9. MAE Block

**Definition**
Morning / Afternoon / Evening classification attached to sessions.

**Purpose**
Adds time-of-day structure to the reporting model.

**Business interpretation**
Useful for analysing *when* work tends to happen, not only how much work was completed.

**Example use**
A reviewer may notice that most effective minutes are generated in the morning, or that evening sessions are longer but lower quality.

---

## 10. Reporting Windows

GoalTracker surfaces performance across multiple time windows rather than only at the individual-session level.

| Window | Use |
|---|---|
| **Day** | Short-term performance review and immediate target tracking |
| **Week** | Recurring reporting cadence and broader progress interpretation |
| **Month** | Higher-level trend visibility and period comparison |
| **Goal / sprint window** | Measuring performance against a broader planned objective |

This layered reporting approach demonstrates how the same session-level data can support multiple business-facing views.

---

## 11. Input Data vs Reporting Outputs

One of the main ideas in GoalTracker is the separation between captured activity and reporting output.

**Input data** — the operational records that describe what happened:

| Input element | Description |
|---|---|
| Session record | The underlying work unit being captured |
| Start / end timestamps | The time boundaries of the session |
| Category | Area of work |
| Work item | Specific task or focus |
| Quality level | Self-assessed quality of the session |
| Notes | Supporting context |

**Reporting outputs** — the analytical summaries derived from that activity:

| Output | Description |
|---|---|
| Effective minutes | Quality-weighted time |
| Attainment % | Progress against target |
| Rating | Human-readable performance label |
| Day snapshot | Persisted daily summary |
| Week snapshot | Persisted weekly rollup |

This distinction matters because good reporting systems do not stop at record capture. They transform raw activity into decision-useful outputs.

---

## 12. How a Business User Would Read These KPIs

A manager or analyst reviewing GoalTracker would typically ask:

- Is performance on track against target?
- Are raw minutes and effective minutes materially different?
- Is quality affecting performance output?
- Which days are strongest or weakest?
- Is weekly pace improving or slipping?
- When does the most valuable work tend to happen?
- How should current performance be summarised in a simple rating?

The KPI model is designed to support those questions in a structured and business-readable way.

---

## 13. What This File Proves in the Portfolio

This glossary is part of the portfolio proof itself.

It shows that the project is not only capable of displaying charts or logging activity, but also of:

- defining metrics precisely
- documenting KPI logic clearly
- separating operational data from reporting outputs
- structuring business-facing interpretation

That is why GoalTracker is relevant to **BI Analyst, Data Analyst, Reporting Analyst, and Analytics Engineer** roles.
