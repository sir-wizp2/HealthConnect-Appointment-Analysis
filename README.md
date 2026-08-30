# HealthConnect-Appointment-Analysis
Analysis of HealthConnect appointment data to identify factors influencing patient attendance, no-shows, waiting times, and reminder effectiveness

## Project Overview

This project is part of the **AnalystLab Africa Week 4 Experience Lab Assignment**.

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

## 🔍 Data Quality Assessment

An initial data quality assessment was conducted before analysis.

### Key findings

- **5,000 records** were identified.
- **18 columns** are available.
- **No duplicate records** were identified.
- Missing values were identified in three main columns:
- reminder_channel – 1,366 missing values
- distance_to_clinic_km – 90 missing values
- waiting_time_minutes – 60 missing values

The missing values in reminder_channel require particular attention because a blank value may indicate that no reminder was sent rather than that the information was missing.

Missing values will therefore be investigated and handled based on the business meaning of each field rather than automatically replacing them with zero.

---

## Proposed KPIs

The following KPIs were proposed for the analysis:

### 1. Appointment Attendance Rate (%)

Measures the percentage of scheduled appointments that patients attended.

### 2. Appointment No-Show Rate (%)

Measures the percentage of scheduled appointments where patients did not attend and did not cancel.

### 3. Reminder Effectiveness (%)

Compares attendance among patients who received reminders with those who did not.

### 4. Average Waiting Time (Minutes)

Measures the average amount of time patients wait before receiving service.

### 5. Average Booking Lead Time (Days)

Measures the average number of days between booking an appointment and the scheduled appointment date.

---

## Initial Analysis Approach

The analysis will follow these stages:

1. **Data Cleaning**
   - Review data types
   - Identify missing values
   - Check for duplicates
   - Investigate inconsistent entries

2. **Descriptive Analysis**
   - Calculate attendance rate
   - Calculate no-show rate
   - Calculate average waiting time
   - Calculate average booking lead time

3. **Segmentation**
   - Analyse appointment outcomes by patient demographics
   - Compare different reminder channels
   - Group booking lead time
   - Group distance to clinic

4. **Comparative Analysis**
   - Compare reminder recipients with non-recipients
   - Compare attendance across booking lead-time groups
   - Examine the relationship between distance and attendance
   - Compare waiting times across appointment types

5. **Insight Generation**
   - Identify important trends and patterns
   - Highlight potential operational issues
   - Develop practical recommendations for Health Connect

---

## Assumptions and Limitations

### Assumptions

- Each row represents one appointment record.
- Appointment status accurately represents the outcome of an appointment.
- The available variables are sufficient to identify major patterns in appointment attendance.
- Missing reminder information requires investigation before interpretation.

### Limitations

- Some fields contain missing values.
- The dataset may not capture every factor that influences patient attendance.
- The analysis identifies relationships and patterns but does not establish causation.
- The dataset represents a specific period and may not reflect long-term behavior.

---

## Expected Business Value

The analysis is expected to help Health Connect:

- Reduce appointment no-shows
- Improve appointment attendance
- Evaluate reminder strategies
- Identify patient groups requiring additional attention
- Understand factors associated with missed appointments
- Identify causes of longer waiting times
- Improve appointment scheduling and management
- Enhance the overall patient experience

---

## 🛠️ Tools & Technologies

The project will use data analysis and visualization tools to clean, analyze, and communicate insights from the Health Connect appointment dataset.

**Tools:**

- Microsoft Excel
- Power BI
- Power Query

---
Status: Initial Analysis / In Progress

The business understanding, data quality assessment, business questions, proposed KPIs, assumptions, limitations, and initial analysis approach have been established. The next stage is to perform the detailed analysis and develop the required visualizations and insights.

👤 Author

Wisdom Ukah

Data Analyst | Computer Science Student

Analyst Lab Africa – Week 4 Experience Lab
