# HealthConnect Appointment Attendance & No-Show Analysis

## AnalystLab Africa — Week 4 Data Analytics Project

> **Project:** HealthConnect Clinic Experience Lab  
> **Week:** 4 — Problem Understanding & Initial Analysis  
> **Track:** Data Analytics  
> **Project Theme:** Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

---

## 📌 Project Overview

This project is part of the **AnalystLab Africa Experience Lab Internship Programme — Week 4**.

Week 4 marks the beginning of the HealthConnect Experience Lab, where interns contribute to a shared healthcare project from the perspective of their respective professional tracks.

The overall HealthConnect project explores how data, machine learning, and Generative AI can be used to help reduce missed appointments and improve the patient support experience.

As a **Data Analytics intern**, this project focuses specifically on understanding the appointment data and identifying how it can be used to investigate appointment attendance, no-shows, and cancellations.

Week 4 is primarily a **problem understanding, data review, initial analysis, and planning stage**. The purpose is to establish a strong foundation for the deeper analysis and development activities that will follow.

---

# 🎯 Business Problem

HealthConnect Clinic is experiencing several operational and patient-support challenges, including:

- Patients missing scheduled appointments.
- Difficulty understanding factors associated with appointment no-shows.
- Inefficient use of appointment slots when patients fail to attend.
- The need to improve patient engagement and administrative support.

The central project question is:

> **How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?**

For the Data Analytics track, the specific focus is to understand appointment attendance and no-show patterns and identify factors that may be associated with different appointment outcomes.

---

# 👩‍💻 My Role

As a **Data Analytics Intern**, my role within the broader HealthConnect project is to:

- Review and understand the HealthConnect appointment dataset.
- Review the HealthConnect Data Dictionary.
- Assess the quality and consistency of the available data.
- Identify important variables relevant to appointment attendance and no-shows.
- Define relevant business questions.
- Propose meaningful Key Performance Indicators (KPIs).
- Develop an initial analysis approach.
- Identify assumptions, limitations, risks, and dependencies.
- Provide a data-driven foundation for deeper analysis in subsequent weeks.

---

# 🎯 Week 4 Objectives

The main objectives of this stage of the project were to:

1. Understand the HealthConnect business problem.
2. Review the resources relevant to the Data Analytics track.
3. Understand the dataset structure.
4. Conduct an initial data-quality assessment.
5. Identify variables relevant to appointment attendance and no-show behaviour.
6. Define relevant business questions.
7. Identify and justify potential KPIs.
8. Develop an initial analysis approach.
9. Document assumptions, limitations, risks, and dependencies.
10. Establish a foundation for the next phase of the project.

---

# 📚 Project Resources

The HealthConnect Experience Lab provides several project resources.

## HealthConnect Appointment Dataset

**File:** `HealthConnect_Appointment_Data.csv`

The dataset contains fictional and anonymised appointment records covering:

- Patient demographics
- Appointment details
- Booking information
- Previous appointment history
- Previous no-shows
- Reminder information
- Distance to the clinic
- Waiting time
- Appointment outcomes

## HealthConnect Data Dictionary

**File:** `HealthConnect_Data_Dictionary.xlsx`

The Data Dictionary was used to understand:

- Variable definitions
- Data types
- Expected categories
- Business meaning of fields
- Validation rules
- Relationships between certain variables

## HealthConnect Clinic Knowledge Base

**File:** `HealthConnect_Clinic_Knowledge_Base.docx`

The Knowledge Base contains approved fictional information about HealthConnect Clinic, including:

- Clinic information
- Locations and opening hours
- Available services
- Appointment procedures
- Rescheduling and cancellation procedures
- Frequently asked questions
- AI safety rules
- Escalation guidelines

For the Data Analytics track, the main resources used were the **Appointment Dataset** and **Data Dictionary**.

---

# 🛠️ Tools Used

The following tools were used during Week 4:

- **Microsoft Power BI**
- **Power Query**
- **Microsoft Word**
- **GitHub**

Power Query was primarily used for data inspection and quality assessment, while Power BI provides the environment for subsequent analysis and visualisation.

---

# 📊 Dataset Overview

The HealthConnect Appointment Dataset contains:

- **5,000 appointment records**
- **18 variables**

The dataset contains appointment-level information relating to patients, scheduling, previous appointment behaviour, reminders, accessibility, waiting time, and appointment outcomes.

The `appointment_id` field serves as the unique appointment identifier.

The `patient_id` is an anonymised patient identifier and may appear across multiple appointment records.

---

# 🗂️ Dataset Variables

| Variable | Description |
|---|---|
| `appointment_id` | Unique appointment identifier |
| `patient_id` | Anonymised patient identifier |
| `gender` | Recorded gender category |
| `age` | Patient age in years |
| `age_group` | Age band derived from age |
| `appointment_type` | Type of scheduled appointment |
| `booking_date` | Date the appointment was booked |
| `appointment_date` | Scheduled appointment date |
| `appointment_day` | Day of the week of the appointment |
| `appointment_time` | Appointment time period |
| `booking_lead_days` | Number of days between booking and appointment |
| `previous_appointments` | Number of previous appointments |
| `previous_no_shows` | Number of previous missed appointments |
| `reminder_sent` | Whether an appointment reminder was sent |
| `reminder_channel` | Channel used to deliver the reminder |
| `distance_to_clinic_km` | Approximate distance to the clinic |
| `waiting_time_minutes` | Estimated waiting time |
| `appointment_outcome` | Final appointment status |

---

# 🧹 Data Quality Assessment

An initial data-quality assessment was performed using **Power Query**.

The assessment focused on:

- Duplicate records
- Unique identifiers
- Missing values
- Data types
- Valid categories
- Logical relationships between variables
- Consistency with the Data Dictionary

---

## 1. Appointment ID Uniqueness

The `appointment_id` column was checked using Power Query's column distribution.

Results:

- **5,000 distinct values**
- **5,000 unique values**

This indicates that all appointment IDs are unique and no duplicate appointment IDs were identified.

**Status: ✅ Valid**

---

## 2. Missing Values

Column quality was reviewed across the dataset.

Limited empty values were identified in:

| Variable | Missing/Empty Values |
|---|---:|
| `distance_to_clinic_km` | Approximately 2% |
| `waiting_time_minutes` | Approximately 1% |

These variables will require appropriate consideration when they are used during subsequent analysis.

The `reminder_channel` value `None` is treated as a valid category because it represents appointments where no reminder was sent.

**Status: ⚠️ Minor missing-data consideration**

---

## 3. Data Types

The dataset's variables were reviewed against the Data Dictionary.

The appropriate data types were identified for:

- Text fields
- Integer fields
- Decimal fields
- Date fields

**Status: ✅ Valid**

---

## 4. Appointment Outcome Validation

The `appointment_outcome` field contains:

- Attended
- No-Show
- Cancelled

These are the expected appointment outcome categories.

**Status: ✅ Valid**

---

## 5. Age Validation

The recorded age range was:

**18–80 years**

This is consistent with the dataset specification for adult patients.

**Status: ✅ Valid**

---

## 6. Age Group Validation

The age groups identified were:

- 18–24
- 25–34
- 35–44
- 45–54
- 55–64
- 65+

**Status: ✅ Valid**

---

## 7. Appointment Type Validation

The appointment types identified were:

- Diagnostic Test
- Follow-up
- General Consultation
- Specialist Consultation

**Status: ✅ Valid**

---

## 8. Gender Validation

The gender categories identified were:

- Female
- Male
- Prefer not to say

**Status: ✅ Valid**

---

## 9. Reminder Sent Validation

The `reminder_sent` field contains:

- Yes
- No

**Status: ✅ Valid**

---

## 10. Reminder Channel Validation

The reminder channels identified were:

- Email
- SMS
- WhatsApp
- None

`None` represents appointments where no reminder was sent.

A logical consistency check between reminder status and reminder channel returned **Valid**.

**Status: ✅ Valid**

---

## 11. Appointment Day Validation

All seven days of the week were represented:

- Monday
- Tuesday
- Wednesday
- Thursday
- Friday
- Saturday
- Sunday

**Status: ✅ Valid**

---

## 12. Appointment Time Validation

The appointment time periods identified were:

- Morning
- Afternoon
- Evening

**Status: ✅ Valid**

---

## 13. Booking Lead Days Validation

The recorded `booking_lead_days` value was independently compared with the difference between:

`appointment_date - booking_date`

The validation returned **Match**.

This indicates that the recorded booking lead time is consistent with the underlying booking and appointment dates.

**Status: ✅ Valid**

---

## 14. Previous Appointment History Validation

A logical check was performed to ensure:

`previous_no_shows <= previous_appointments`

The validation returned **Valid**.

This means that previous no-shows did not exceed the total number of previous appointments.

**Status: ✅ Valid**

---

## 15. Booking and Appointment Date Validation

A logical check was performed to ensure:

`booking_date <= appointment_date`

The validation returned **Valid**.

No logical inconsistency was identified where a booking date occurred after the scheduled appointment date.

**Status: ✅ Valid**

---

# 📋 Overall Data Quality Summary

| Data Quality Area | Finding | Status |
|---|---|---|
| Total records | 5,000 | ✅ |
| Total variables | 18 | ✅ |
| Distinct appointment IDs | 5,000 | ✅ |
| Unique appointment IDs | 5,000 | ✅ |
| Duplicate appointment IDs | None identified | ✅ |
| Age range | 18–80 | ✅ |
| Missing distance values | Approximately 2% | ⚠️ |
| Missing waiting-time values | Approximately 1% | ⚠️ |
| Appointment outcomes | Valid categories | ✅ |
| Age groups | Valid categories | ✅ |
| Appointment types | Valid categories | ✅ |
| Gender | Valid categories | ✅ |
| Reminder status | Valid | ✅ |
| Reminder channels | Valid | ✅ |
| Appointment days | Valid | ✅ |
| Appointment times | Valid | ✅ |
| Booking lead days | Match | ✅ |
| Previous no-shows relationship | Valid | ✅ |
| Booking/appointment dates | Valid | ✅ |
| Reminder consistency | Valid | ✅ |

---

# 📌 Data Quality Conclusion

The initial assessment indicates that the HealthConnect Appointment Dataset is generally well structured and suitable for further exploratory analysis.

The dataset contains unique appointment identifiers, appropriate data types, valid categorical values, and logically consistent relationships between important variables.

The main data-quality considerations are the limited missing values in:

- `distance_to_clinic_km`
- `waiting_time_minutes`

These will need to be considered when these variables are used in subsequent analysis.

---

# 🔎 Important Variables for Analysis

The following variables were identified as particularly relevant to appointment attendance and no-show behaviour.

## Appointment Outcome

`appointment_outcome`

This is the primary outcome variable because it records whether an appointment was attended, missed, or cancelled.

## Demographic Variables

- `age`
- `age_group`
- `gender`

These variables can help determine whether appointment outcomes differ across demographic groups.

## Appointment Variables

- `appointment_type`
- `appointment_day`
- `appointment_time`

These variables can help identify whether specific appointment characteristics are associated with attendance or no-shows.

## Booking and Timing Variables

- `booking_date`
- `appointment_date`
- `booking_lead_days`

These variables allow investigation of scheduling and the amount of time between booking and appointment.

## Historical Behaviour Variables

- `previous_appointments`
- `previous_no_shows`

These variables are important for examining whether previous appointment behaviour is associated with future attendance.

## Reminder Variables

- `reminder_sent`
- `reminder_channel`

These variables can be used to investigate reminder coverage and differences between reminder channels.

## Operational Variables

- `distance_to_clinic_km`
- `waiting_time_minutes`

These variables provide additional accessibility and operational context.

---

# ❓ Business Questions

The following business questions were defined to guide the subsequent analysis.

### Question 1

**What is the overall pattern of attended, no-show, and cancelled appointments at HealthConnect Clinic?**

### Question 2

**Which patient characteristics are associated with differences in appointment attendance and no-show behaviour?**

### Question 3

**How do appointment characteristics and booking timing relate to appointment attendance?**

### Question 4

**Is previous appointment behaviour associated with the likelihood of a patient missing an appointment?**

### Question 5

**How are appointment reminders and reminder channels associated with appointment attendance?**

---

# 📈 Potential KPIs

Five potential KPIs were identified.

| KPI | Purpose | Related Business Question |
|---|---|---|
| **Attendance Rate** | Measures the percentage of appointments attended | Q1 |
| **No-Show Rate** | Measures the percentage of appointments resulting in a no-show | Q1 |
| **Cancellation Rate** | Measures the percentage of appointments cancelled | Q1 |
| **Reminder Coverage Rate** | Measures the percentage of appointments receiving reminders | Q5 |
| **Repeat No-Show Rate** | Examines repeated no-show behaviour | Q4 |

## KPI Justification

### Attendance Rate

Provides an overall measure of successful appointment attendance.

### No-Show Rate

Measures the scale of the missed-appointment problem.

### Cancellation Rate

Separates cancellations from no-shows so that the two behaviours are not treated as the same outcome.

### Reminder Coverage Rate

Measures the extent to which appointments receive reminders.

### Repeat No-Show Rate

Helps examine whether previous no-show behaviour is relevant to future appointment attendance.

> **Important:** The Week 4 brief requires these KPIs to be identified and their relevance justified. KPI calculation, analysis, and visualisation are not required at this stage.

---

# 🔬 Initial Analysis Approach

The proposed analysis will follow a structured process.

## Step 1 — Validate the Data

Confirm that the data is sufficiently accurate, consistent, and suitable for analysis.

## Step 2 — Examine Appointment Outcomes

Analyse the distribution of:

- Attended
- No-Show
- Cancelled

## Step 3 — Analyse Demographic Patterns

Compare appointment outcomes across:

- Age groups
- Gender

## Step 4 — Analyse Appointment Characteristics

Compare outcomes across:

- Appointment types
- Appointment days
- Appointment times

## Step 5 — Analyse Booking Timing

Investigate whether `booking_lead_days` is associated with different appointment outcomes.

## Step 6 — Analyse Previous Behaviour

Examine:

- Previous appointments
- Previous no-shows

to determine whether historical behaviour is associated with future attendance.

## Step 7 — Analyse Reminders

Compare appointment outcomes according to:

- Whether a reminder was sent
- Reminder channel

## Step 8 — Analyse Operational Factors

Explore:

- Distance to clinic
- Waiting time

while accounting for their limited missing values.

## Step 9 — Calculate and Analyse KPIs

The selected KPIs will be calculated and analysed during the appropriate subsequent stage.

## Step 10 — Develop Insights and Recommendations

The analysis will be used to identify meaningful patterns and develop evidence-based recommendations.

---

# 🔄 Proposed Analytical Workflow

```text
Data Validation
       ↓
Exploratory Analysis
       ↓
Appointment Outcome Analysis
       ↓
Demographic Analysis
       ↓
Appointment & Timing Analysis
       ↓
Historical Behaviour Analysis
       ↓
Reminder Analysis
       ↓
Operational Factor Analysis
       ↓
KPI Analysis
       ↓
Insights
       ↓
Recommendations
