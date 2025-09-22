🏋️‍♂️ Fitness Analytics Dashboard (Power BI)

A Power BI dashboard designed to analyze gym business performance, memberships, and client fitness insights. 
It combines business KPIs and health metrics into an interactive, data-driven solution for fitness centers.


📌 Features

  1. Business Performance

       - Total clients & trainers

        - Total revenue, expenses, and profit

        - Quick insights into financial performance
  

  2. Monthly Tracking

       - New members acquired each month

      - Monthly revenue, expenses, and profit trends

      - Side-by-side revenue vs. expenses comparison
  

  3. Membership Analysis

     - Active vs. expired memberships by tier (Platinum, Gold, Silver)

      - Individual client membership status

       - Custom SVG progress bar for membership completion
  

  4. Health & Fitness Calculations

     - BMI with categories (Underweight, Normal, Overweight, Obese)

     - BMR (Basal Metabolic Rate)

      - TDEE (Total Daily Energy Expenditure)

     - Calorie intake recommendations
  

  5. Member Profile Page

      - Personal details (Name, Age, Gender, Contact, Address)

      - Membership info (Tier, Start, Expiry, Status)

      - Health metrics and progress tracking

  

📊 Dataset & Tables

  - Users – Member information
 
   - Payments – Revenue details

  - Expenses – Operational costs

   - Calendar – Date table for time intelligence

   - Additional slicers: Weight, Height, Age, Gender, Activity
     
     
  

⚙️ Key DAX Measures

  Some measures used:

  - Users_Count = DISTINCTCOUNT(Users[UserID])

  - Revenue = SUM(Payments[Amount])

   - Expenses = SUM(Expenses[Amount])

   - Profit = [Revenue] - [Expenses]

   - ProgressPercent = DIVIDE([Complete_Days],[Total_Days],0)*100

   - BMI = ROUND(Weight / (HeightMeters * HeightMeters),1)

  - BMR = (10 * Weight) + (6.25 * Height) - (5 * Age) + Gender_Adjustment
  
  - TDEE = [BMR] * ActivityFactor

👉 Full list of measures included in the file Business Solution.


🚀 Learnings & Outcomes

  - Built data model with multiple tables & relationships

  -  Applied advanced DAX for KPIs & fitness metrics

  - Designed custom SVG visuals in Power BI

  - Delivered an end-to-end fitness + business analysis solution
    
    

📷 Dashboard Preview
    - Home Page Only
    <img width="1426" height="798" alt="image" src="https://github.com/user-attachments/assets/7ac1090a-1a6e-4190-9144-833d4b7080d5" />

  - For whole Dashboard visit pdf file " Fitness Analytics Board "




🛠️ Tech Stack

  - Power BI
  - Ms Excel (Dataset)
  - DAX

