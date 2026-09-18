# HealthConnect Clinic Experience Lab — Data Analytics Track

**Programme:** AnalystLab Africa Experience Lab Internship
**Project:** HealthConnect Clinic Experience Lab
**Track:** Data Analytics
**Intern:** [Your Full Name]
**Repository:** [Your GitHub Username]/HealthConnect-Experience-Lab

---

## Project Overview

HealthConnect Clinic is a fictional healthcare provider seeking to reduce missed appointments, improve appointment attendance, make better use of appointment slots, and provide more effective administrative support to patients.

The overall project question is:

> How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

This repository contains the Data Analytics track deliverables produced across the AnalystLab Africa Experience Lab programme (Weeks 4–8).

---

## Weekly Progression

| Week | Stage | Focus |
|------|-------|-------|
| Week 4 | Problem Understanding | Resource review and solution planning |
| Week 5 | Analysis & Development | Initial EDA, KPIs, dashboard, business insights |
| Week 6 | Integration & Advanced Development | Deeper analysis, validated findings, improved dashboard, cross-track integration |
| **Week 7** | **Testing, Refinement & End-to-End Validation** | **Systematic testing, KPI validation, dashboard refinement, cross-track re-validation** |
| Week 8 | Final Integration & Presentation | End-to-end integration and final presentation |

---

## Week 7 — Testing, Refinement & End-to-End Validation

### Objective

Systematically test, refine, and validate the Week 6 dashboard outputs to ensure accuracy, consistency, and readiness for final integration in Week 8.

### What Was Tested

1. **KPI accuracy** — independent recalculation of all dashboard KPIs from the raw CSV
2. **Dashboard filters** — behaviour and correctness of all seven sidebar filters
3. **Channel ranking robustness** — verification that SMS remains the best reminder channel across all distance bands
4. **Highest-risk combination** — validation of the "Very Far Distance + 2–4 Weeks" finding across all appointment types
5. **Cross-track model alignment** — collaboration with the Data Science track to confirm feature importance alignment

### Testing Results Summary

| Test Category | Tests Run | Passed | Failed | Caveats |
|---|---|---|---|---|
| KPI Validation | 5 | 5 | 0 | 0 |
| Dashboard Filters | 7 | 7 | 0 | 0 |
| Robustness Checks | 2 | 2 | 0 | 1 (Moderate distance channel ambiguity) |
| Cross-Track Re-Validation | 1 | 1 | 0 | 0 |
| **Total** | **15** | **15** | **0** | **1** |

**All 15 tests passed. One caveat documented.**

### Key Validated Findings

- **Overall No-Show Rate:** 48.5% (independently recalculated and verified)
- **Overall Attendance Rate:** 46.3% (verified)
- **Reminder Effectiveness Gap:** 4.9 percentage points (47.6% with reminders vs 42.7% without)
- **Distance is the strongest single driver:** Very Far Distance = 68.1% no-show vs Close Distance = 46.5%
- **Highest-risk combination:** Very Far Distance + 2–4 Weeks = **83.3% no-show** (confirmed across all four appointment types)
- **Best reminder channel:** SMS at 49.6% attendance (caveat: Email narrowly outperforms SMS in the Moderate Distance band at 47.1% vs 46.4%)

### Dashboard Refinements Made

1. Added "% of total" labels to the donut chart to prevent Cancelled vs No-Show confusion
2. Reworked the Reminder Channel Performance table to show Total, Attended, and Rate side by side
3. Added a dedicated Highest No-Show Risk Combination chart on Page 3
4. Sharpened chart titles to include the metric being shown
5. Tightened filter interaction so selecting one filter clears stale selections in dependent visuals

### Cross-Track Collaboration

**Track:** Data Science
**Dependency:** Model feature importance validation

The Data Science track's candidate model identified **Booking Lead Time** and **Distance** as the top two predictive features. My analytics work independently identified the same two variables as the strongest drivers of no-show behaviour.

During this collaboration, an artefact column named `Unnamed: 0` was identified in the raw CSV export and removed. The model was re-run, and the top two features remained unchanged. Both tracks now use a single cleaned CSV file, and the dashboard and model are provably aligned on 5,000 records.

**Full collaboration record:** See `Week7_Report.pdf`, Section 2.11.

