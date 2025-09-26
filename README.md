# 🏋️‍♂️ Fitness Analytics 



A **Power BI dashboard** designed to analyze gym business performance, memberships, and client fitness insights. It combines business KPIs and health metrics into an interactive, data-driven solution for fitness centers, providing a holistic view of both financial health and member engagement.

---

## 📷 Dashboard Preview

### Home Page Only 
*For a view of the complete dashboard, including the Member Profile page, please refer to the PDF file: "Fitness Analytics Board."*
<img width="1197" height="653" alt="image" src="https://github.com/user-attachments/assets/fb0ccb6f-e549-47a3-b884-66ec343f9007" />




## 📌 Features

This dashboard is divided into key analytical areas to provide comprehensive insights:

### 1. Business Performance (KPIs)
* **Total clients & trainers** at a glance.
* Tracking **Total Revenue, Expenses, and Profit**.
* **Quick insights** into overall financial health.

### 2. Monthly Tracking & Trends
* Analysis of **new members acquired** each month.
* Visualization of **monthly revenue, expenses, and profit trends**.
* **Side-by-side revenue vs. expenses comparison** to quickly identify margins.

### 3. Membership Analysis
* Detailed view of **active vs. expired memberships** broken down by tier (**Platinum, Gold, Silver**).
* Tracking **individual client membership status**.
* Implementation of a **custom SVG progress bar** for visual membership completion tracking.

### 4. Health & Fitness Calculations
* Calculations for **BMI (Body Mass Index)** with distinct categories (Underweight, Normal, Overweight, Obese).
* Calculation of **BMR (Basal Metabolic Rate)**.
* Calculation of **TDEE (Total Daily Energy Expenditure)**.
* Generation of **calorie intake recommendations** based on metrics.

### 5. Member Profile Page
* A dedicated page for personal details (**Name, Age, Gender, Contact, Address**).
* Display of membership info (**Tier, Start, Expiry, Status**).
* Visualization of **health metrics and progress tracking**.

---

## 📊 Dataset & Data Model

The analysis is powered by a relational data model consisting of the following tables:

| Table | Description |
| :--- | :--- |
| **Users** | Core information about gym members. |
| **Payments** | Detailed records of all revenue transactions. |
| **Expenses** | Records of all operational and business costs. |
| **Calendar** | A standard date table for robust time intelligence analysis. |

**Additional Slicers/Filters:** `Weight`, `Height`, `Age`, `Gender`, and `Activity Level` are available for granular filtering.

---

## ⚙️ Key DAX Measures

Advanced **DAX (Data Analysis Expressions)** were utilized to transform raw data into meaningful KPIs and complex fitness metrics.

| Measure | Formula Description |
| :--- | :--- |
| `Users_Count` | `DISTINCTCOUNT(Users[UserID])` |
| `Revenue` | `SUM(Payments[Amount])` |
| `Expenses` | `SUM(Expenses[Amount])` |
| `Profit` | `[Revenue] - [Expenses]` |
| `ProgressPercent` | `DIVIDE([Complete_Days],[Total_Days],0)*100` (Used for membership completion) |
| `BMI` | `ROUND(Weight / (HeightMeters * HeightMeters),1)` |
| `BMR` | `(10 * Weight) + (6.25 * Height) - (5 * Age) + Gender_Adjustment` |
| `TDEE` | `[BMR] * ActivityFactor` |

👉 **Full List:** A complete list of all DAX measures is included in the provided file `Business Solution` (not in this README).

---

## 🚀 Learnings & Outcomes

This project served as a comprehensive exercise in business intelligence development, demonstrating mastery in several key areas:

* Successfully built a **robust data model** with multiple tables and defined relationships.
* Applied **advanced DAX** for calculating both financial KPIs and complex physiological fitness metrics.
* Designed and implemented **custom SVG visuals** within Power BI to create unique elements like the membership progress bar.
* Delivered an **end-to-end fitness + business analysis solution**.

---

## 🛠️ Tech Stack

* **Primary Tool:** **Power BI**
* **Data Source:** **Ms Excel** (for the initial dataset)
* **Language:** **DAX** (Data Analysis Expressions)

---






