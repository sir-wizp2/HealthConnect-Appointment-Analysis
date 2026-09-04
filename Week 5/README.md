# HealthConnect Appointment Analysis
## AnalystLab Africa Week 5 Experience Lab

---

## Project Overview

This project is part of the **AnalystLab Africa Week 5 Experience Lab Assignment**.

The project focuses on analysing HealthConnect appointment data to understand patient appointment behaviour, identify factors associated with missed appointments, evaluate the effectiveness of appointment reminders, and assess aspects of the overall patient experience.

The analysis is designed to provide HealthConnect with data-driven insights that can support better appointment management, reduce no-shows, improve waiting times, and enhance the patient experience.

---

## Business Objective

The main objective of this project is to understand patterns in appointment attendance and identify factors that may influence patient behaviour.

The analysis aims to answer questions such as:

- What percentage of appointments are attended, cancelled, or missed?
- Which factors are associated with appointment no-shows?
- Does booking lead time affect appointment attendance?
- How does the use of appointment reminders affect attendance?
- Does distance to the clinic influence no-show behaviour?
- Which patient groups have the highest attendance and no-show rates?
- What is the average patient waiting time?
- Which appointment types experience higher waiting times or no-show rates?
- What areas of the appointment process can HealthConnect improve?

---

## Dataset

The HealthConnect Appointment dataset contains:

- **5,000 appointment records**
- **18 columns**

The dataset contains a combination of:

- Appointment information
- Patient demographic information
- Appointment status
- Reminder information
- Booking lead time
- Distance to clinic
- Waiting time
- Other appointment-related variables

---

## Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| Microsoft Power BI | Data visualization and dashboard creation |
| Power Query | Data cleaning and transformation |

---

## Data Quality Assessment

An initial data quality assessment was conducted before analysis.

### Key Findings

| Quality Check | Result |
|---------------|--------|
| Total Records | 5,000 |
| Total Columns | 18 |
| Duplicate Records | None found |

### Missing Values Handling

| Column | Missing Count | Handling Strategy |
|--------|---------------|-------------------|
| reminder_channel | 1,366 | Left as missing (represents "No Reminder Sent") |
| distance_to_clinic_km | 90 | Replaced with "Not Specified" |
| waiting_time_minutes | 60 | Replaced with "Not Specified" |

The missing values in **reminder_channel** required particular attention because a blank value may indicate that no reminder was sent rather than that the information was missing. These values were therefore left as missing to preserve their business meaning.

---

## Key Performance Indicators (KPIs)

The following KPIs were calculated for the analysis:

| # | KPI | Value |
|---|-----|-------|
| 1 | **Appointment Attendance Rate** | 46.3% |
| 2 | **Appointment No-Show Rate** | 48.5% |
| 3 | **Attendance Rate (With Reminder)** | 47.6% |
| 4 | **Attendance Rate (Without Reminder)** | 46.3% |
| 5 | **Reminder Effectiveness** | +1.3% |
| 6 | **Average Waiting Time** | 24.2 minutes |
| 7 | **Average Booking Lead Time** | 24.2 days |

### KPI Definitions

**1. Appointment Attendance Rate (%)**
Measures the percentage of scheduled appointments that patients attended.

**2. Appointment No-Show Rate (%)**
Measures the percentage of scheduled appointments where patients did not attend and did not cancel.

**3. Attendance Rate (With Reminder)**
Measures the percentage of patients who attended after receiving a reminder.

**4. Attendance Rate (Without Reminder)**
Measures the percentage of patients who attended without receiving a reminder.

**5. Reminder Effectiveness (%)**
Compares attendance among patients who received reminders with those who did not.

**6. Average Waiting Time (Minutes)**
Measures the average amount of time patients wait before receiving service.

**7. Average Booking Lead Time (Days)**
Measures the average number of days between booking an appointment and the scheduled appointment date.

---

## Exploratory Data Analysis (EDA)

### Appointment Status Breakdown

| Status | Count | Percentage |
|--------|-------|------------|
| No-Show | 2,423 | 48.5% |
| Attended | 2,314 | 46.3% |
| Cancelled | 263 | 5.3% |

### Attendance Rate by Reminder Status

| Reminder Status | Attendance Rate |
|-----------------|-----------------|
| With Reminder | 47.6% |
| Without Reminder | 46.3% |
| **Difference** | **+1.3%** |

### No-Show Rate by Reminder Status

| Reminder Status | No-Show Rate |
|-----------------|--------------|
| With Reminder | 47.4% |
| Without Reminder | 48.5% |

### Attendance Rate by Booking Lead Time

| Booking Lead Time Category | Attendance Rate |
|----------------------------|-----------------|
| Short Term (0-7 days) | 66.6% |
| 1-2 Weeks | 61.8% |
| 2-4 Weeks | 51.7% |
| 1-2 Months | 34.1% |

### No-Show Rate by Distance

| Distance Category | No-Show Rate |
|-------------------|--------------|
| Very Far Distance | 68.1% |
| Far Distance | 55.5% |
| Not Specified | 52.2% |
| Moderate Distance | 49.4% |
| Close Distance | 46.5% |

### Average Waiting Time by Appointment Time

| Appointment Time | Average Wait (Minutes) |
|------------------|------------------------|
| Evening | 29.6 |
| Morning | 24.1 |
| Afternoon | 23.9 |

### No-Show Rate by Age Group

| Age Group | No-Show Rate |
|-----------|--------------|
| 18-24 | Higher |
| 25-34 | Moderate |
| 35-44 | Moderate |
| 45-54 | Moderate |
| 55-64 | Lower |
| 65+ | Lowest |

### No-Show Rate by Appointment Type

| Appointment Type | No-Show Rate |
|------------------|--------------|
| General Consultation | Moderate |
| Specialist Consultation | Higher |
| Follow-up | Moderate |
| Diagnostic Test | Moderate |

---

## Key Insights

### Insight 1: The No-Show Crisis

**Finding:** 48.5% of all appointments result in no-shows, with an additional 5.3% cancelled.

**Implication:** This represents significant revenue loss for HealthConnect. For a 5,000-appointment dataset, this means 2,423 appointments were missed without prior cancellation.

**Action:** Immediate implementation of a multi-channel reminder system and a no-show reduction strategy is required.

---

### Insight 2: Current Reminders Are Not Working Effectively

**Finding:** Reminders improve attendance by only 1.3% (47.6% vs 46.3%).

**Implication:** The current reminder system is not very effective. The small improvement suggests that the reminder channel (likely SMS) or timing may not be optimal.

**Action:**
- Switch to WhatsApp as the primary reminder channel
- Implement a multi-step reminder system (7-day, 3-day, 1-day)
- Track reminder effectiveness by channel

---

### Insight 3: Booking Lead Time is a Critical Predictor

**Finding:** Attendance drops from 66.6% for Short Term bookings (0-7 days) to 34.1% for 1-2 Months bookings.

**Implication:** Patients who book appointments far in advance are nearly twice as likely to no-show compared to those who book closer to the appointment date.

**Action:**
- Implement weekly touchpoints for bookings >14 days
- Offer easier rescheduling options
- Consider a "last-minute" slot service

---

### Insight 4: Distance is a Major Access Barrier

**Finding:** Very Far Distance patients have a 68.1% no-show rate vs. 46.5% for Close Distance patients.

**Implication:** Geographic access is a significant determinant of appointment attendance.

**Action:**
- Explore telemedicine options for patients in Very Far Distance areas
- Consider transport partnerships or support
- Implement a "Distance Risk" flag for proactive outreach

---

### Insight 5: Age Group Segmentation Matters

**Finding:** Younger patients (18-24) have the highest no-show rates; older patients (65+) have the lowest.

**Implication:** Different age groups respond to different communication styles and have different barriers to attendance.

**Action:**
- Tailor communication strategies by age group
- For younger patients: Use WhatsApp with SMS back-up
- For older patients: Consider phone call reminders in addition to digital reminders

---

### Insight 6: Evening Appointments Have Longest Wait Times

**Finding:** Evening appointments average 29.6 minutes waiting time vs. 23.9 minutes in the afternoon and 24.1 minutes in the morning.

**Implication:** Patient dissatisfaction may be higher for evening appointments due to longer waits.

**Action:**
- Review evening appointment scheduling capacity
- Consider adding additional evening staff
- Implement a "Wait Time Feedback" system

---

### Insight 7: Specialist Consultations Show Higher No-Show Rates

**Finding:** Specialist consultations have the highest no-show rates among all appointment types.

**Implication:** Specialist appointments often involve longer wait times to schedule and may be perceived as lower priority.

**Action:**
- Implement targeted reminders for specialist consultations
- Provide pre-appointment education to reduce patient anxiety
- Offer a "Specialist Consultation" confirmation call 48 hours prior

---

## Business Recommendations

### Recommendation 1: Implement a Multi-Channel Reminder System

| Item | Details |
|------|---------|
| **Priority** | High |
| **Timeline** | Immediate (0-3 months) |
| **Expected Impact** | 10-15% reduction in no-shows |

**Implementation Plan:**
1. **Primary Reminder (7 Days Prior):** WhatsApp message with appointment confirmation
2. **Secondary Reminder (3 Days Prior):** WhatsApp/SMS reminder
3. **Tertiary Reminder (1 Day Prior):** WhatsApp "Final Reminder" with preparation instructions
4. **Escalation:** If no confirmation, follow with SMS or phone call

---

### Recommendation 2: Optimise Booking Lead Time Strategy

| Item | Details |
|------|---------|
| **Priority** | High |
| **Timeline** | Short-term (0-6 months) |
| **Expected Impact** | 8-12% improvement |

**Implementation Plan:**
1. Bookings >14 days: Automated weekly reminder touchpoint
2. Bookings >30 days: Targeted outreach to confirm attendance
3. Waitlist Management: Create a waitlist system to fill cancelled slots
4. Messaging: Reinforce appointment value in all communications

---

### Recommendation 3: Address Distance Barriers

| Item | Details |
|------|---------|
| **Priority** | Medium-High |
| **Timeline** | Medium-term (3-9 months) |
| **Expected Impact** | 5-10% improvement |

**Implementation Plan:**
1. Flag System: Identify Very Far Distance and Far Distance patients
2. Proactive Outreach: Contact these patients 48 hours before appointments
3. Telemedicine: Explore options for teleconsultations
4. Transport Partnerships: Consider ride-sharing or community transport

---

### Recommendation 4: Age-Tailored Communication Strategies

| Item | Details |
|------|---------|
| **Priority** | Medium |
| **Timeline** | Medium-term (3-6 months) |
| **Expected Impact** | 5-8% improvement |

**Implementation Plan:**
1. **18-34 Age Group:** WhatsApp/Email primary, easy rescheduling, evening/weekend availability
2. **35-54 Age Group:** Mixed approach (SMS, Email, WhatsApp), flexible scheduling
3. **55+ Age Group:** Phone calls + digital, transportation assistance, early appointments

---

### Recommendation 5: Improve Appointment Type Management

| Item | Details |
|------|---------|
| **Priority** | Medium-High |
| **Timeline** | Short-term (0-3 months) |
| **Expected Impact** | 5-10% reduction |

**Implementation Plan:**
1. **Specialist Consultation:** Dedicated reminder protocol, pre-appointment education, confirmation call 48 hours prior
2. **Follow-up Appointments:** Book at time of service, provide written details, WhatsApp confirmation

---

### Recommendation 6: Optimise Appointment Timing

| Item | Details |
|------|---------|
| **Priority** | Medium |
| **Timeline** | Short-term (0-3 months) |
| **Expected Impact** | 3-5% improvement |

**Implementation Plan:**
1. **Evening Appointments:** Review capacity and staffing, monitor wait times
2. **Morning Appointments:** Prioritise high-risk patients earlier in the day
3. **Afternoon Appointments:** Maintain current performance, optimise for maximum attendance

---

### Recommendation 7: Develop a No-Show Prevention Dashboard

| Item | Details |
|------|---------|
| **Priority** | High |
| **Timeline** | Short-term (0-3 months) |
| **Expected Impact** | Ongoing improvement |

**Implementation Plan:**
1. **Key Metrics to Track:** Daily no-show rate by appointment type, reminder status, distance, lead time, age group
2. **Real-time Monitoring:** Identify high-risk appointments, proactive outreach
3. **Monthly Review:** Evaluate effectiveness, adjust strategies, report to management

---

## Dashboard Visualisation Summary

The Power BI dashboard developed for this analysis includes:

### Tab 1: Appointment & Patient Insights
- Booking Lead Days Category and No-Show Rate
- Distance to Clinic Group and No-Show Rate
- Appointment Day and Cancellation/Attendance Breakdown
- Appointment Type and Distance Category Analysis
- Reminder Channel and Attendance Performance
- Attendance Rate by Reminder Status
- No-Show Rate by Reminder Status
- No-Show Rate by Booking Lead Time
- No-Show Rate by Appointment Type

### Tab 2: Patient Experience & Process Improvement
- Average Waiting Time by Appointment Time
- Attendance Rate by Booking Lead Days
- Attendance Rate by Distance
- Average Waiting Time by Appointment Type
- Demographic Breakdowns by Age Group

---

## Limitations

### Data Limitations

| Limitation | Description |
|------------|-------------|
| Missing Values | reminder_channel contains 1,366 missing values (27.3% of records) |
| Data Period | Represents a specific time period only |
| No Causal Inference | Identifies correlations but cannot establish causation |
| Self-Reported Data | Appointment outcomes may contain recording errors |

### Analytical Limitations

| Limitation | Description |
|------------|-------------|
| Segmentation Granularity | Pre-defined categories may hide other patterns |
| External Factors | Socioeconomic status, weather, etc. not captured |
| Generalisability | May not apply to other clinic settings |

---

## Next Steps

### Immediate Actions (0-3 Months)
- Implement Multi-Channel Reminder System
- Flag High-Risk Patients
- Proactive Outreach to High-Risk Patients
- Establish KPI Monitoring

### Short-Term Actions (3-6 Months)
- Evaluate Telemedicine Options
- Age-Tailored Communication
- Specialist Consultation Improvement
- Waiting Time Optimisation

### Medium-Term Actions (6-12 Months)
- Regional Clinics for Far-Distance Patients
- Predictive Modelling for High-Risk Identification
- Patient Feedback System
- Continuous Improvement Reviews

---

## Expected Business Value

The analysis is expected to help HealthConnect:

- Reduce appointment no-shows
- Improve appointment attendance
- Evaluate reminder strategies
- Identify patient groups requiring additional attention
- Understand factors associated with missed appointments
- Identify causes of longer waiting times
- Improve appointment scheduling and management
- Enhance the overall patient experience

---

## Project Status

**Status:** Completed

The business understanding, data quality assessment, business questions, KPIs, assumptions, limitations, and initial analysis approach were established in Week 4. The detailed analysis, dashboard development, and business recommendations were completed in Week 5.

### Week 5 Deliverables:
- Cleaned and prepared dataset
- 7 KPIs calculated
- 2-page Power BI dashboard
- 7 key insights identified
- 7 practical recommendations
- Comprehensive analytics report

---

## Author

**Wisdom Chibuike Ukah**

Data Analyst | Computer Science Student

AnalystLab Africa – Week 5 Experience Lab
