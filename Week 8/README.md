# HealthConnect Clinic — Appointment Attendance & No-Show Analysis

**AnalystLab Africa Week 8 — Data Analytics Track**
**Intern:** Wisdom Chibuike Ukah

## Project Overview
HealthConnect Clinic faces a 48.5% no-show rate across 5,000 appointments. This project builds and validates a Power BI dashboard that identifies the strongest drivers of no-shows and provides actionable recommendations.

## Key Findings
- No-Show Rate: 48.5% (validated)
- Reminder Effectiveness: +4.9 pp (47.6% vs 42.7%)
- Distance: Very Far = 68.1% vs Close = 46.5%
- Highest-Risk Combo: Very Far + 2–4 Weeks = 83.3%
- Best Channel: SMS (49.6%), with Email caveat in Moderate Distance

## Tools Used
- Excel - Data Cleaning and Preparation
- Power BI — Dashboard visualization
- Jupyter Notebook — Analysis, testing and KPI validation

## Validation
All KPIs independently recalculated from raw CSV with zero variance.
All seven filter tests passed. Cross-track alignment with Data Science confirmed.

## Cross-Track Collaboration
- Partner: Dorsilla Kemunto (Data Science)
- Shared: KPIs, distance finding, channel ranking, risk combo
- Received: Top 2 model features (Booking Lead Time, Distance)
- Result: Dashboard and model aligned on 5,000 records

## Limitations
- Moderate Distance channel ambiguity (SMS vs Email within 0.7 pp)
- "Not specified" distance group (52.2% no-show) may hide a driver
- Mobile filter testing not yet done

## Recommendations
1. Target Very Far + 2–4 Weeks with intensive reminders/transport
2. Default SMS; A/B test Email in Moderate Distance band
3. Encourage shorter booking lead times
4. Offer telehealth for Very Far patients
5. Age-tailored messaging for 18–24 and 55–64
