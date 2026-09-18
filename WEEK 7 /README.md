# HealthConnect Clinic — Week 7: Testing, Refinement & End-to-End Validation

**Programme:** AnalystLab Africa Experience Lab
**Track:** Data Analytics
**Intern:** [Wisdom Chibuike Ukah]
**Week:** 7

---

## What This Week Is About

Week 6 was about building and integrating. Week 7 is about **testing**.

This week I went back through my Week 6 dashboard and proved that every number on it is correct. I recalculated every KPI from the raw CSV, tested every filter, checked whether my key findings held up when the data was segmented, and worked with the Data Science track to confirm our top drivers matched.

The goal was not to build something new. The goal was to prove the existing work is accurate and reliable before Week 8 final integration and presentation.

---

## What I Tested

| # | Test | Method |
|---|------|--------|
| 1 | KPI accuracy | Recalculated each KPI from raw CSV in Python |
| 2 | Distance filter | Applied each distance band, checked KPI cards |
| 3 | Age group filter | Applied each age band, checked no-show values |
| 4 | Reminder channel filter | Applied each channel, checked attendance rates |
| 5 | Appointment type filter | Applied each type, checked no-show rates |
| 6 | Booking lead days filter | Applied each category, checked attendance rates |
| 7 | Highest-risk combination | Filtered Very Far + 2–4 Weeks |
| 8 | Filter reset | Reset all filters, checked KPIs returned to baseline |
| 9 | Channel × distance robustness | Re-ranked channels per distance band |
| 10 | Risk × appointment type robustness | Tested highest-risk combo across all types |
| 11 | Cross-track model re-validation | Worked with Data Science on feature alignment |

---

## Results

**All tests passed. One caveat documented.**

### KPI Validation

| KPI | Dashboard Value | Manual Recalculation | Result |
|-----|----------------|---------------------|--------|
| Attendance Rate | 46.3% | 46.3% | PASS |
| No-Show Rate | 48.5% | 48.5% | PASS |
| Attendance with Reminder | 47.6% | 47.6% | PASS |
| Attendance without Reminder | 42.7% | 42.7% | PASS |
| Reminder Effectiveness Gap | 4.9 pp | 4.9 pp | PASS |

### Filter Testing

All seven sidebar filters tested successfully. Every value matched manual recalculation.

The highest-risk combination (Very Far Distance + 2–4 Weeks) returned **83.3% no-show** as expected.

Resetting all filters returned KPIs to baseline (48.5% / 46.3% / 47.6% / 42.7%) with no leakage.

### Channel Ranking

Aggregate ranking confirmed:

1. SMS — 49.6%
2. Email — 46.5%
3. WhatsApp — 44.6%
4. None — 42.7%

**Caveat:** When re-ranked within distance bands, SMS won 3 of 4 bands. In the Moderate Distance band, Email narrowly outperformed SMS (47.1% vs 46.4%). Documented as a caveat, not a failure.

### Highest-Risk Combination

Very Far Distance + 2–4 Weeks = **83.3% no-show**. This held true across all four appointment types (Diagnostic Test, Follow-up, General Consultation, Specialist Consultation).

---

## Cross-Track Work

**Collaborated with:** Data Science

**What we tested:** Whether the model's top features matched my analytics top drivers.

**Finding:** Both tracks independently identified **Booking Lead Time** and **Distance** as the top two drivers.

**Issue found:** An artefact column named `Unnamed: 0` was present in the raw CSV export.

**Action taken:** Data Science removed the column and re-ran the model.

**Retest result:** Top two features remained unchanged.

**What changed:** Both tracks now use a single cleaned CSV. Dashboard and model are aligned on 5,000 records.

---

## Key Findings (Validated)

- Overall No-Show Rate: **48.5%**
- Reminders improve attendance by **4.9 percentage points**
- Distance is the strongest driver: Very Far = 68.1% vs Close = 46.5%
- Highest-risk segment: Very Far + 2–4 Weeks = **83.3% no-show**
- Best reminder channel: SMS (49.6%), with Moderate Distance caveat

