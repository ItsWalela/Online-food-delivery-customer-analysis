# Online-food-delivery-customer-analysis

## Table of Content
- [Description](#description)
- [Project Aim](#project-aim)
- [Business questions](#business-questions)
- [Aim of the analysis](#aim-of-the-analysis)
- [Processes](#processes)
- [Insights](#insights)
- [Recommendations](#recommendations)
- [How to use the dashboard](#how-to-use-the-dashboard)

## Description
This project offers an opportunity to gain hands-on experience in analyzing data using Excel, including data cleaning, exploratory data analysis (EDA), PivotTables, KPI development, and dashboard creation. I used an online food delivery customer survey dataset to explore patterns in demographics, income, and satisfaction that are associated with a customer's likelihood to reorder.

Source: [Online Food Delivery Preferences Dataset](https://www.kaggle.com/datasets/benroshan/online-food-delivery-preferencesbangalore-region)

**ONLINE FOOD DELIVERY CUSTOMER DASHBOARD**
| Total Respondents | Would Reorder | Reorder Rate |
|---|---|---|
| 388 | 301 | 77.6% |

## Description of the added metric
A custom **Customer Segment** column was engineered by combining two existing fields — `Output` (would reorder: Yes/No) and `Feedback` (Positive/Negative) — into four segments: **Loyal Customer**, **At Risk**, **Lost Potential**, and **Churned & Unhappy**. This turns two weak individual signals into one strong, business-usable classification.

## Project Aim
The aim of this project is to analyze customer survey data and identify the demographic and behavioral characteristics associated with customer loyalty versus churn risk. The objective of this project is to answer the following question:
- Which customer characteristics (occupation, income, education, customer type) are associated with being a Loyal Customer versus being At Risk or Churned?

## Business questions
I identified several pressing challenges related to customer retention, presented in bullet points for clarity:
- Unclear loyalty drivers: No clear view of which customer types are most likely to keep ordering
- Limited satisfaction insight: Lack of actionable insight into which segments report negative feedback
- Undifferentiated marketing: Difficulty identifying which occupation/income groups to prioritize for retention efforts

## Aim of the analysis
The primary objectives of this analysis are as follows:
- Clean and prepare survey data for analysis
- Engineer a Customer Segment classification from reorder intent and feedback
- Data analysis: analyze reorder intent and feedback across occupation, income, age, education, and customer type
- Build an interactive Excel dashboard for business decision-making

## Processes
**Step 1: Data Preparation & Cleaning**
Tools: Microsoft Excel — Power Query, Tables, Formulas

Activities:
- Reviewed the dataset structure and variables (14 fields, 388 respondents)
- Checked for duplicate respondent records
- Checked for blank/missing values across key fields (Output, Feedback, Occupation, Monthly Income)
- Checked categorical variables (Marital Status, Customer Type, Feedback) for consistency and standardization
- Added the **Customer Segment** calculated column using nested `IF(AND(...))` logic on Output and Feedback
- Confirmed the cleaned dataset contained no remaining duplicates or blanks requiring correction

**Step 2: Exploratory Data Analysis (EDA)**
Tools: Microsoft Excel — PivotTables, Formulas

Activities:
- Created PivotTables to examine Customer Segment, Output, and Feedback across occupation, income bracket, age group, gender, education, and customer type
- Corrected an early aggregation error: switched Family Size analysis from **Sum** to **Average**, since summing conflates group size with household size
- Compared reorder rate and satisfaction across categories to identify patterns and at-risk segments
- Designed an Excel dashboard with slicers connected across all PivotTables to bring the key findings together

## Insights
- **Overall Loyalty:** 77.6% of respondents indicated they would reorder (`Output = Yes`), suggesting strong overall repeat-usage intent across the customer base.
- **Occupation and Segment:** Students are overwhelmingly Loyal Customers (174 of 207 students, ~84%) — the strongest loyalty rate of any occupation group. Employees show the highest Churned & Unhappy share (33 of 118, ~28%), making them the segment most worth investigating for service issues.
- **Income and Reorder Rate:** Respondents with No Income have the highest reorder rate (164 of 187, ~88%) — largely overlapping with the student population — while the mid-tier "25,001–50,000" income bracket has the weakest reorder rate (~61%), a counterintuitive dip worth investigating further.
- **Customer Type and Feedback:** Regular and Frequent customers report similarly high positive feedback (~82% each), while New customers report the lowest positive feedback share (~75%), pointing to a possible first-experience or onboarding gap.
- **Household Size:** Correcting the Family Size metric from Sum to Average revealed genuine differences in typical household size by occupation, rather than results driven purely by group size.

## Recommendations
- **Prioritize Employee Retention:** Since Employees have the highest Churned & Unhappy rate, the business could investigate delivery time, pricing, or service quality specifically for working professionals, who likely value speed and reliability differently than students.
- **Investigate the Mid-Income Dip:** The 25,001–50,000 income bracket underperforms neighboring brackets on reorder rate — worth a targeted survey or promotion test to understand why.
- **Strengthen the New Customer Experience:** With New customers reporting the lowest positive feedback, the business could introduce a first-order guarantee, onboarding discount, or proactive follow-up after a customer's first order.
- **Protect the Student Segment:** Students are the most loyal segment — the business could introduce student-specific loyalty perks to defend this segment against competitors.
- **Segment Marketing Spend:** Use the Customer Segment classification (Loyal/At Risk/Lost Potential/Churned) to route marketing budget — retention offers toward At Risk, win-back campaigns toward Lost Potential, and referral incentives toward Loyal Customers.

## How to use the dashboard
**Step 1: Download the dashboard**
- Download the `online_food_delivery_analysis_.xlsx` file from this repository

**Step 2: Open the dashboard**
- Open the `.xlsx` file using Microsoft Excel

**Step 3: Enable editing**
- If prompted, select Enable Editing

**Step 4: Explore the dashboard**
- Use the available filters/slicers to explore Customer Segment, Output, and Feedback across occupation, income, age group, gender, education, and customer type

**Step 5: Review the results**
- Use the KPIs, charts, and visualizations on the "Report" sheet to understand the key loyalty and satisfaction patterns identified in the analysis
