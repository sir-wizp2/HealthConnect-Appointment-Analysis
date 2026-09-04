# HealthConnect Appointment Attendance & Patient Experience Analysis

## Project Overview

HealthConnect is a fictional healthcare clinic seeking to improve patient appointment attendance, reduce missed appointments, optimise appointment slots, and enhance the overall patient experience.

This project analyses HealthConnect appointment data to identify patterns associated with appointment attendance, cancellations, no-shows, reminders, waiting times, booking behaviour, and patient characteristics.

The project was completed as part of the **AnalystLab Africa Experience Lab – Data Analytics Track**.

---

## Project Objective

The main objective of this project is to use data analytics and business intelligence to help HealthConnect:

- Understand appointment attendance patterns
- Identify factors associated with missed appointments
- Evaluate the relationship between appointment reminders and attendance
- Understand patient waiting-time patterns
- Identify groups with higher no-show rates
- Generate actionable recommendations for improving appointment attendance and patient experience

### Central Project Question

> **How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?**

---

## Dataset

The analysis uses the **HealthConnect Appointment Dataset**, a fictional and anonymised healthcare appointment dataset provided as part of the AnalystLab Africa Experience Lab.

The dataset contains appointment-level information relating to:

- Patient demographics
- Appointment details
- Booking information
- Previous appointment history
- Previous no-shows
- Appointment reminders
- Distance to the clinic
- Waiting time
- Appointment outcomes

Each row represents an appointment record.

---

## Business Questions

The analysis was designed around the following business questions:

1. What percentage of scheduled appointments are attended, cancelled, or missed?
2. Which factors are most strongly associated with appointment no-shows?
3. Does booking lead time affect appointment attendance?
4. Do appointment reminders affect attendance and no-show rates?
5. Does distance from the clinic influence appointment attendance?
6. Which patient groups have the highest attendance and no-show rates?
7. What is the average patient waiting time?
8. Which appointment types experience higher waiting times or no-show rates?
9. What areas of the appointment process could HealthConnect improve?

---

## Key Performance Indicators

Five core KPIs were identified for the project:

### 1. Appointment Attendance Rate

Percentage of scheduled appointments that were attended.

### 2. Appointment No-Show Rate

Percentage of scheduled appointments where patients did not attend and did not cancel.

### 3. Reminder Effectiveness

Comparison of attendance between patients who received reminders and those who did not.

### 4. Average Waiting Time

Average number of minutes patients wait before receiving service.

### 5. Average Booking Lead Time

Average number of days between booking an appointment and the scheduled appointment date.

These KPIs provide a balanced view of appointment performance, missed appointments, reminder effectiveness, waiting experience, and booking behaviour.

---

## Data Preparation

The data preparation process was carried out using **Power Query in Power BI**.

Key preparation activities included:

- Reviewing column data types
- Checking missing values
- Checking for duplicate records
- Identifying inconsistent values
- Separating relevant components of compound fields where necessary
- Creating meaningful categories for numerical variables
- Categorising waiting-time values
- Preparing fields for analysis and visualisation
- Creating calculated measures using DAX

The original dataset was preserved, while transformed data was used for analysis.

---

## Analysis & Dashboard

The project was developed using **Microsoft Power BI**.

The dashboard focuses on:

### Appointment Performance

- Attendance rate
- No-show rate
- Cancellation patterns
- Overall appointment outcomes

### Reminder Analysis

- No-show rate by reminder sent
- Attendance comparison between patients who received reminders and those who did not
- Reminder channel performance where sufficient data is available

### Patient & Appointment Analysis

- Attendance and no-show patterns across relevant patient groups
- Appointment-type performance
- Booking lead-time patterns

### Waiting-Time Analysis

- Average waiting time
- Waiting-time categories
- Waiting-time patterns across relevant appointment groups

---

## Reminder Analysis

A key part of the analysis evaluates whether appointment reminders are associated with better attendance.

The analysis compares:

### Reminder Sent

- Yes
- No

It also evaluates reminder performance by channel where sufficient data is available, such as:

- SMS
- Email
- Other available channels

The analysis focuses on identifying relationships and patterns rather than claiming that reminders directly cause patients to attend.

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI | Data analysis, DAX measures and dashboard development |
| Power Query | Data cleaning and transformation |
| DAX | KPI and analytical measure development |
| Microsoft Excel | Supporting data inspection and preparation |
| GitHub | Project documentation and version control |

---

## Dashboard

The Power BI dashboard provides an interactive view of HealthConnect appointment performance.

Key dashboard areas include:

- Appointment KPIs
- Attendance analysis
- No-show analysis
- Reminder effectiveness
- Reminder channel comparison
- Waiting-time analysis
- Patient segmentation
- Appointment trends

---

## Key Insights

The analysis is intended to identify:

- The overall scale of appointment attendance and missed appointments
- Whether reminder recipients demonstrate different attendance behaviour
- Which reminder channels perform better where sufficient data exists
- Patient groups associated with higher no-show rates
- Whether longer booking lead times are associated with missed appointments
- Groups experiencing longer waiting times
- Areas where HealthConnect can improve appointment operations and patient experience

> **Note:** Final insights should be updated with the actual numerical findings from the Power BI dashboard.

---

##  Business Recommendations

Based on the analytical findings, HealthConnect can consider:

1. **Strengthening appointment reminder processes** for patients who demonstrate higher no-show behaviour.
2. **Prioritising effective reminder channels** based on observed attendance performance.
3. **Monitoring high-risk patient or appointment groups** and developing targeted engagement strategies.
4. **Reviewing long booking lead times** where they are associated with higher no-show rates.
5. **Investigating long waiting-time categories** to identify operational bottlenecks.
6. **Using dashboard KPIs for continuous monitoring** of attendance and no-show performance.
7. **Combining data analytics with patient-support initiatives** to improve the overall appointment experience.

---

## Assumptions

The analysis is based on the following assumptions:

- Each row represents one appointment record.
- Appointment status accurately represents the outcome of the appointment.
- The available variables are sufficiently representative for exploratory analysis.
- Reminder information accurately reflects the reminder recorded for an appointment.
- Missing values are handled according to the meaning and context of each variable.

---

## Limitations

- The dataset contains missing values, particularly within reminder-related information.
- The dataset may not capture all factors that influence attendance, such as personal circumstances, health conditions, or unexpected events.
- The analysis identifies relationships and patterns but does not establish direct causation.
- The dataset represents a specific period and may not fully represent long-term patient behaviour.
- Reminder-channel comparisons may be affected by differences in the number of records available for each channel.

---

## Future Improvements

Future stages of the project could include:

- Developing a predictive model for appointment no-shows
- Identifying patients at higher risk of missing appointments
- Building automated reminder recommendations
- Expanding the analysis to longer periods of appointment data
- Developing more advanced patient segmentation
- Integrating analytics with an AI-powered patient support solution
- Continuously monitoring appointment KPIs

---

👤 Author

Wisdom Ukah

Aspiring Data Analyst | Computer Science Student
