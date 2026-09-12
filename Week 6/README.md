# HealthConnect — Patient Attendance & No-Show Analysis

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Week](https://img.shields.io/badge/week-6-blue)
![Tracks](https://img.shields.io/badge/tracks-Analytics%20%7C%20Data%20Science-purple)

A cross-track analytics project analyzing **5,000 patient appointments** to identify the drivers of no-shows and improve attendance through better reminder strategy and targeted interventions.

---

## 📌 Project Overview

HealthConnect is a healthcare appointment dataset used to answer one core question:

> **Why do patients miss appointments, and what can we do about it?**

This repository contains the full analytical pipeline — from KPI validation to deep segmentation, cross-track ML validation, and dashboard delivery.

| Attribute | Detail |
|---|---|
| **Dataset size** | 5,000 appointments |
| **Target variable** | `no_show` |
| **Analyst** | [Wisdom Chibuike Ukah] — Data Analytics |
| **Collaborator** | [Dorsilla Kemunto ] — Data Science |
| **Tools** | Power BI · Python (pandas, scikit-learn) |
| **Current phase** | Week 6 — Deep dive + cross-track integration |

---

## 📊 Key Metrics (Validated — Week 6)

| KPI | Value |
|---|---|
| Total Appointments | 5,000 |
| Attended Appointments | 2,314 |
| **No-Show Rate** | **48.5%** |
| **Overall Attendance Rate** | **46.3%** |
| Attendance Rate — With Reminder | 47.6% |
| Attendance Rate — Without Reminder | 42.7% |

> The **4.9 pp gap** between reminded and non-reminded appointments confirms reminders help — but even reminded patients attend less than half the time.

---

## 📈 Analysis Timeline

### Week 5 — Baseline Analysis
- ✅ KPI validation (no-show rate, attendance rate)
- ✅ No-show rate by reminder channel
- ✅ Initial ML-ready dataset created (4 features)
- 📌 Finding: WhatsApp had the lowest no-show rate (49.8%)

### Week 6 — Deep Dive + Cross-Track Integration
- ✅ Attendance rate by reminder channel (SMS = 49.6%)
- ✅ No-show rate by distance × age group
- ✅ Highest-risk combinations (distance × lead time)
- ✅ Attendance rate by booking lead time × appointment type
- ✅ Cross-track integration with Data Science (Random Forest validation)
- ✅ Cross-Track Validation Card added to dashboard

---

## 🎯 Key Findings (Week 6)

### 1. Reminder Channel — Attendance Rate

| Channel | Total | Attended | Rate |
|---|---|---|---|
| **SMS** | 2,000 | 992 | **49.6%** |
| Email | 533 | 248 | 46.5% |
| WhatsApp | 1,101 | 491 | 44.6% |
| None | 1,366 | 583 | 42.7% |

> ⚠️ **Metric note:** Week 5 no-show rate ranked WhatsApp best (49.8% no-show). Week 6 attendance rate ranks SMS best (49.6% attendance). **These are different metrics and are not contradictory** — no-show + attendance ≠ 100% because cancellations and reschedules sit between them.

### 2. Booking Lead Time × Appointment Type

| Appointment Type | 1–2 Months | 1–2 Weeks | 2–4 Weeks | Short Term |
|---|---|---|---|---|
| Diagnostic Test | 35.7% | 63.9% | 49.0% | 68.8% |
| **Follow-up** | **29.6%** | 59.6% | 51.7% | 62.7% |
| General Consultation | 36.5% | 60.9% | 52.8% | **72.2%** |
| Specialist Consultation | 34.8% | 66.0% | 50.8% | 60.5% |

- **Lowest:** Follow-up + 1–2 Months = **29.6%**
- **Highest:** General Consultation + Short Term = **72.2%**

### 3. Distance × Age Group

- **Highest no-show:** 18–24 Very Far & 55–64 Very Far = **83.3%**
- **Very Far** distance elevates no-show across all age groups (53–83%)
- **Close** distance stays stable (43–49%) regardless of age

### 4. Highest-Risk Combinations

| Distance | Lead Time | No-Show Rate |
|---|---|---|
| Very Far | 2–4 Weeks | **83.3%** |
| Very Far | Short Term | **80.0%** |
| Far | 1–2 Months | 71.8% |
| Not Specified | 1–2 Months | 64.3% |
| Moderate | 1–2 Months | 60.3% |
| Very Far | 1–2 Months | 60.0% |

---

## 🔗 Cross-Track Integration (Analytics × Data Science)

The Data Science track trained a **Random Forest model** to predict `no_show`. My manual segmentation and their feature importance ranking converged on the same drivers.

| Insight Source | Top Driver 1 | Top Driver 2 |
|---|---|---|
| Manual Analytics (Week 6) | Booking Lead Time | Distance to Clinic |
| ML Feature Importance | `numeric_booking_lead_days` | `numeric_distance_to_clinic_km` |

✅ **Two independent methods converged on the same top drivers.**

### Model Error Distribution

| Type | Count | % |
|---|---|---|
| True Negative | 259 | 27.32% |
| True Positive | 243 | 25.63% |
| False Negative | 242 | 25.53% |
| False Positive | 204 | 21.52% |

**Concerns flagged to Data Science track:**
- ⚠️ `Unnamed: 0` used as feature (index leak) — should be dropped
- ⚠️ Only 4 features in Week 5 ML-ready set — needs enrichment with Week 6 dimensions
- ⚠️ False Negatives ≈ True Positives — optimize **recall**, not accuracy
- ⚠️ Overall accuracy ~53%

📄 Full details: [`reports/cross_track_integration_report.md`](reports/cross_track_integration_report.md)

---

## 🛠️ Dashboard Structure

**Top Row — KPI Cards:**

| Card | Value |
|---|---|
| No-Show Rate | 48.5% |
| Attendance Rate | 46.3% |
| With Reminder | 47.6% |
| Without Reminder | 42.7% |

**Visuals:**

1. No-Show Rate by Distance × Age Group (heatmap)
2. Highest No-Show Risk Combinations (bar)
3. Attendance Rate by Lead Time × Appointment Type (matrix)
4. Reminder Channel Performance (table — volume + rate)
5. **Cross-Track Validation Card** ← *Week 6 new*

---

## 💡 Recommendations

1. **Continue SMS** as a primary reminder channel (highest attendance + highest volume)
2. **Investigate WhatsApp** no-show vs. attendance gap (cancellations? reschedules?)
3. **Staged reminders** for bookings >2 weeks out (booking → mid-point → 48h)
4. **Targeted outreach** for Very Far distance patients (transport / telehealth)
5. **Priority flagging** for Follow-up + 1–2 Month bookings (lowest attendance segment)
6. **Enrich ML feature set** with Week 6 dimensions and drop the index column

---

## 📅 Roadmap

- [x] **Week 5** — Baseline analysis + ML-ready dataset
- [x] **Week 6** — Deep dive + cross-track integration
- [ ] **Week 7** — Intervention design + model iteration
- [ ] **Week 8** — Final presentation + handoff

---

## 📎 Reports

| Report | Link |
|---|---|
| Week 5 Report | [`reports/week5_report.md`](reports/week5_report.md) |
| Week 6 Report | [`reports/week6_report.md`](reports/week6_report.md) |
| Cross-Track Integration Report | [`reports/cross_track_integration_report.md`](reports/cross_track_integration_report.md) |

---

## 👥 Contributors

| Name | Track | Contribution |
|---|---|---|
| [Your Name] | Data Analytics | Segmentation, dashboards, cross-track triangulation |
| [DS Name] | Data Science | Random Forest model, feature importance, error analysis |

---

## 📄 License

This project is for educational and internal analysis purposes.

---

*Last updated: Week 6*
