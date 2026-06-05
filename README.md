<h1 align="center">🏥 Healthcare Appointment & Patient Analytics Dashboard</h1>

<p align="center">
  <b>An end-to-end Power BI dashboard analyzing 50,000 patient appointments across Jan 2024 – Dec 2025</b><br/>
  <i>Covering chronic disease patterns, attendance behaviour, satisfaction scores & demographic insights</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Domain-Healthcare%20Analytics-blue?style=for-the-badge&logo=health&logoColor=white"/>
  <img src="https://img.shields.io/badge/Records-50%2C000%2B-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Period-Jan%202024%20–%20Dec%202025-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
</p>

---

## 📸 Dashboard Preview

<img width="1307" height="727" alt="Screenshot 2026-06-05 133051" src="https://github.com/user-attachments/assets/241a6516-efe6-4b39-9955-1901812fc1d0" />


> *Interactive Power BI dashboard with slicers for Gender, Marital Status, and Month-level filtering*

---

## 📌 Project Overview

This **Healthcare Analytics Dashboard** was built to give hospital administrators, clinic managers, and health policy analysts a single-pane-of-glass view of patient appointment data. It transforms raw appointment records into actionable visual insights — from tracking no-show rates and chronic disease prevalence to understanding how income level correlates with hypertension.

### 🎯 Business Problem Solved
Healthcare facilities struggle to:
- Monitor **patient no-show rates** and attendance patterns over time
- Understand which **demographics** are most affected by chronic diseases
- Identify **high-risk patient segments** across age groups, employment status, and income levels
- Measure **patient satisfaction** across different insurance types

This dashboard answers all of these questions in one place.

---

## 📊 Key KPIs at a Glance

| KPI | Value | Insight |
|---|---|---|
| 🗓️ **Total Appointments** | 50,000 | Full 2-year dataset |
| 🩺 **Diabetes Patients** | 10,795 | 21.6% of total patients |
| 💊 **Chronic Disease Patients** | 19,084 | 38.2% chronic disease prevalence |
| ✅ **Attendance Rate** | 91.7% | Strong overall attendance |
| ❌ **No Show Rate** | 8.3% | Key area for operational improvement |

---

## 🧩 Dashboard Sections Explained

### 1. 🏙️ Top 5 Cities by Alcoholism
Identifies geographic hotspots for alcohol-related cases to guide targeted health interventions.

| City | Cases |
|---|---|
| Amsterdam | 786 |
| Rotterdam | 715 |
| The Hague | 604 |
| Utrecht | 563 |
| Eindhoven | 526 |

---

### 2. 📈 Diabetes Patients by Age Group
Bar chart showing diabetes distribution across 5 age brackets.

| Age Group | Patients |
|---|---|
| 0–18 | 1,127 |
| 19–30 | 1,251 |
| 31–45 | 2,095 |
| **46–60** | **3,491 ← Peak** |
| 60+ | 2,831 |

> 💡 **Insight:** The 46–60 age group has the highest diabetes prevalence — a clear signal for proactive screening programs targeting middle-aged patients.

---

### 3. 🍺 Alcoholism by Clinic Type
Compares alcoholism cases across 4 facility types.

- **Public Hospital** leads with 1,935 cases — likely due to higher patient volume and accessibility
- **Specialty Clinics** show the lowest at 685 — suggesting selective referral patterns

---

### 4. 📅 Total Appointments by Month
Line chart tracking monthly appointment volumes across the full 2-year period.

> 💡 **Insight:** Appointments peak in **May (4,359)** and decline steadily toward **February (3,857)**, suggesting seasonal health-seeking behaviour — actionable for staff scheduling and resource planning.

---

### 5. 💼 Employment Status by Chronic Disease
Horizontal bar chart showing chronic disease burden across employment categories.

| Status | Patients |
|---|---|
| **Employed** | **8,794** |
| Retired | 3,400 |
| Unemployed | 2,673 |
| Student | 2,324 |
| Self-employed | 1,893 |

> 💡 **Insight:** Employed individuals account for the largest chronic disease group — highlighting the need for **workplace wellness programs**.

---

### 6. ⭐ Satisfaction Score by Insurance Type
| Insurance | Score |
|---|---|
| **Public** | **183.35K** |
| Private | 90.96K |
| Uninsured | 41.98K |
| Mixed | 34.62K |

> 💡 **Insight:** Public insurance patients report significantly higher satisfaction — potentially linked to greater accessibility and coverage breadth.

---

### 7. 🩸 Hypertension by Income Level
Donut chart revealing income-based hypertension distribution.

| Income Level | Share |
|---|---|
| Middle | 33.89% |
| Lower-Middle | 24.33% |
| Low | 18.14% |
| Upper-Middle | 17.95% |
| High | 5.69% |

> 💡 **Insight:** Over **76% of hypertension cases** fall in Middle or below income segments — strongly suggesting a socioeconomic link with hypertension risk.

---

## 🛠️ Tools & Technologies

```
Power BI Desktop    →  Dashboard design, visuals, and publishing
DAX                 →  KPI measures, calculated columns, time intelligence
Power Query (M)     →  Data cleaning, transformation, and shaping
Excel / CSV         →  Source data format
```

---

## 🔑 DAX Measures Used

```dax
-- Attendance Rate
Attendance Rate % = DIVIDE(COUNTROWS(FILTER(Appointments, Appointments[Status] = "Attended")),
                    COUNTROWS(Appointments), 0) * 100

-- No Show Rate
No Show Rate % = DIVIDE(COUNTROWS(FILTER(Appointments, Appointments[Status] = "No Show")),
                 COUNTROWS(Appointments), 0) * 100

-- Chronic Disease Patients
Chronic Patients = CALCULATE(COUNTROWS(Patients), Patients[Chronic_Disease] = "Yes")

-- Diabetes Count
Diabetes Patients = CALCULATE(COUNTROWS(Patients), Patients[Diabetes] = "Yes")

-- Satisfaction Total
Total Satisfaction = SUM(Appointments[Satisfaction_Score])
```

---

## 🎛️ Interactive Filters (Slicers)

The dashboard includes **3 dynamic slicers** that update all visuals simultaneously:

- **Gender** — Filter by Male / Female / All
- **Marital Status** — Single / Married / Divorced / All
- **Month** — Drill into any specific month across the 2-year period

---

## 💡 Key Business Insights

1. **8.3% no-show rate** = ~4,150 missed appointments — significant revenue and resource loss for clinics
2. **46–60 age group** is the highest-risk segment for diabetes — early screening campaigns would deliver high ROI
3. **February** consistently shows the lowest appointments — an opportunity for promotional health check campaigns
4. **76%+ of hypertension patients** are from middle and lower-income groups — suggests need for subsidised care pathways
5. **Public hospitals** handle the most alcoholism cases — resource allocation should prioritise these facilities

---

## 📁 Project Structure

```
📦 healthcare-appointment-analytics/
 ┣ 📊 Healthcare_Dashboard.pbix     ← Power BI file
 ┣ 📄 README.md                     ← You are here
 ┣ 🖼️ dashboard_preview.png         ← Dashboard screenshot
 ┗ 📂 data/
    ┗ 📄 appointments_data.csv      ← Source dataset
```

---

## 🚀 How to Open This Project

```bash
# Requirements: Power BI Desktop (Free)
# Download: https://powerbi.microsoft.com/desktop

# Steps:
1. Clone or download this repository
2. Open Power BI Desktop
3. File → Open → Select Healthcare_Dashboard.pbix
4. Refresh data source if prompted
5. Explore the dashboard with slicers!
```

---

## 👤 Author

**Manish Bisht** — Data Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/dataanalyst-manish)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?style=flat-square&logo=github)](https://github.com/bisht5431-source)

---

## 📂 More Projects by Manish

| Project | Tools | Description |
|---|---|---|
| 🏥 Healthcare Analytics Dashboard | Power BI · DAX | This project |
| 🍕 Pizza Sales Dashboard | Power BI · SQL · DAX | Revenue KPIs on 48K+ transactions |
| 💳 Credit Card Portfolio Dashboard | Power BI · DAX · SQL | Transaction & portfolio behaviour |
| 🛒 E-Commerce SQL Analytics | MySQL · SQL | 20 real-world interview queries |

---

<p align="center">
  ⭐ <b>If this project helped you, please star the repository!</b> ⭐<br/>
  <i>It motivates me to keep building more real-world analytics projects.</i>
</p>
