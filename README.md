# Hospital-Analytics-Dashboard
> **Tools:** Power BI | Excel | DAX | Power Query | Data Modeling  

---

## 📘 Introduction

Healthcare organizations increasingly rely on data analytics to monitor patient flow, optimize operational efficiency, control costs, and improve quality of care. Hospitals collect large volumes of patient, treatment, and billing information, but without proper analysis, these insights remain untapped.
This Power BI project transforms raw hospital data into an interactive analytics dashboard that supports strategic decision-making across patient engagement, financial performance, claim processing, and geographical distribution of services.

---

## 📌 Project Objective

The main objectives of this project are:
1.	To create a unified Power BI dashboard for patient, claim, and revenue insights.
2.	To analyse operational efficiency through encounter types, weekly patient flow, and gender trends.
3.	To evaluate financial performance using cost distribution, charge decomposition, and revenue indicators.
4.	To provide location-based insights using geographic mapping and city-wise ranking.
5.	To empower decision-makers with interactive slicers (Ethnicity, Weekday, City, Country, Patient Type, Charges).

---

## 📂 Data Sources

**Sources:**
- 📅 (https://mavenanalytics.io/data-playground/hospital-patient-records)

---

## ❓ Problem Statement
 
 Hospitals often struggle with:
 - Limited visibility into daily/weekly patient volumes
 - Difficulty tracking gender-wise trends and encounter types
 - Weak understanding of charge distribution across cities
 - Lack of clarity in claim status allocations (high/medium/low cost)
 - Inefficient monitoring of revenue performance vs targets
 - No consolidated system that connects patients, geography, and financials into a single source of truth.

---

## 🧾 Attribute Details

| **Attribute Name** | **Data Type** | **Description** |
|--------------------|---------------|-----------------|
| PATIENT_ID | Text | Unique identifier for each patient in the dataset |
| BIRTH_DATE | Date | Birth date (Year/Month/Day) of the Patient |
| MARITAL | Text | The patient’s marital status |
| CATEGORY | Text | Represents the patient’s race or demographic category|
| ETHNICITY | Text | Specifies the ethnic background of the patient |
| GENDER |Text | Gender of the patient |
| CITY | Text | City where the patient resides |
| STATE| Text | State of residence |
| COUNTRY | Text | Country name for high-level geographical segmentation |
| STATE ID | Integer | Numeric identifier for the state |
| FULL NAME | Text | Patient’s full legal name |
| ADMISSION DATE | Date | Hospital admission or visit date |
| ENCOUNTERCLASS | Text | Type of clinical encounter |
| BASE_ENCOUNTER_COST | Currency | Cost before insurance claim |
| CLAIM_COST| Currency | Total claimed amount |
| BALANCE_CLAIMCOST| Currency | Pending or unpaid claim amount |
| CLAIM_STATUS| Text | Classification of claim (Low/Medium/High) |

---

## 🧹 Data Preprocessing Steps

1. **Data Collection:**  
   Gathered data of https://mavenanalytics.io/data-playground/hospital-patient-records from Maven Analytics Portal  

2. **Data Consolidation:**  
   Combined monthly Excel sheets, removed subtotals and redundant rows.  

3. **Automation (Macros):**  
   Automated repetitive formatting tasks like column alignment and styling.  

4. **Data Cleaning (Power Query):**  
   Filled missing values, standardized text formats, corrected data types.  

5. **Data Transformation:**  
   Added calculated flag columns and harmonized field names.  

6. **Data Integration:**  
   Appended cleaned datasets into a unified dataset of https://mavenanalytics.io/data-playground/hospital-patient-records from Maven Analytics Portal)for visualization.

---

## Calculated Measures

- Total Patients 
- Total Claimcost 
- Total Cities 
- Total Charges 
- Total BaseCost 
- Total BaseCost 
- Avg Cost per Day 
- Average Claimcost
- Average Charges 
- AVERAGE BASE COST

---

## Calculated Tables

### Calendar Table:
- The Calendar table provides a complete date structure with Year, Quarter, Month, and Date fields. It enables accurate time intelligence (YTD, MTD, QTD) and ensures all measures work consistently across time.
### Measures Tables:
- The Measure Values table stores all DAX measures used in the dashboard, such as totals, averages, revenues, and ranking metrics. It keeps all calculations organized in one place, making the data model cleaner, easier to manage, and more efficient.

---

## Calculated Columns

- CLAIM_STATUS 
- BALANCE_CLAIMCOST 

---

## 📍 Patient & Claim Dashboard Insights

### Weekly Patients Analysis
- Highest patients recorded on Friday (500 patients)
- Strong upward trend after midweek
- Monday & Tuesday show lower patient inflow
- Helps plan staffing and appointment availability
  
### Patients by Encounter Class
- Ambulatory accounts for the highest share (≈ 46%)
- Outpatient is the second-most used class (≈ 24%)
- Indicates high demand for walk-in treatments and non-admission services
  
### Male vs Female Trend (Monthly)
- March shows the highest patient count
- Female and male trends follow a similar decline toward May
- Indicates seasonal fluctuations or campaign-driven traffic
  
### Claim Status Breakdown
- Majority of claims lie in Low Cost (88%)
- Medium (8.8%) & High Cost (3%) claims are significantly lower
- Indicates efficient cost management and fewer expensive treatments

### City Map by Charges
- Higher billing clusters observed in areas like Boston, Chelsea, and Cambridge
- Geographic visualization helps monitor region-wise service consumption
- Useful for planning hospital outreach or expansion
  
### KPI Summary
- Total Patients: 500
- Total Base Cost: ₹54.54K
- Total Claim Cost: ₹1.53M
- Target Revenue: 2M

---

## 📍 Revenue & City Performance Dashboard Insights

### Revenue Measures
- Target Revenue: 2M
- Future Revenue: 3M
- Total Charges: 1M
Indicates progress toward goals and forecasting potential

### Decomposition Tree
Breakdown by Country and then by specific cities:
- Suffolk Country: Highest contributor
- Boston
- Chelsea
- Norfolk Country
- Middlesex Country
This helps identify high-value zones and underperforming areas

### City-wise Rank by Charges
Top-performing cities:
1.	Lynnfield
2.	Melrose
3.	Norwell
4.	Cohasset
5.	Everett
Provides clear insight into geographical revenue hierarchy

### Charges by Month
- evenue fluctuations across Jan–May
- Peaks during March, dips in May
- Helps forecast and allocate resources seasonally

### Cost Distribution Across Cities
- Boston leads with ₹6,21,097
- Cambridge and Brookline follow
- Supports financial and operational decision-making

---

## 📊 HOSPITAL ANALYTICS DASHBOARD

### Patient & Claim Dashboard

<img width="984" height="553" alt="image" src="https://github.com/user-attachments/assets/8cf65ca4-bef5-47fe-9b68-c718c6f373e8" />

---

### Revenue & City Performance Dashboard

<img width="989" height="558" alt="image" src="https://github.com/user-attachments/assets/5727e9bc-7417-4b5a-9ecd-5d96b5b18dac" />

---

## 📜 Key Insights & Summary

### Operational Insights
- Friday is the busiest day; staffing should align accordingly.
- Ambulatory and outpatient services are most in demand.
- Gender distribution is consistent across months.
### Financial Insights
- Low-cost claims dominate, reducing financial risk.
- Major revenue is concentrated in a handful of cities.
- Total charges (1M) lag behind future revenue targets (3M).
### Geographical Insights
- Boston metro region shows highest charges.
- Several smaller towns still generate meaningful contributions.

---


## 📘 Conclusion

This Power BI analytics solution provides hospital administrators with a comprehensive, interactive, and data-driven view of patient activity, cost structures, claim status, and revenue performance.
By combining operational, financial, and geographical insights into a single dashboard, decision-makers can:
- Improve resource planning
- Optimize revenue strategy
- Strengthen patient engagement
- Monitor claim cost efficiency
- Prioritize high-performing cities
The result is a scalable, professional BI system that enhances transparency and supports evidence-based decision-making.

---
## 📎 Repository Contents

-   Power BI .pbix file
-   Dataset (Excel / CSV)
-   README.md
-   Dashboard screenshots
-   Insights documentation

---

## 🚀 How to Use

1.  Download the `.pbix` file
2.  Open in Power BI Desktop
3.  Apply filters to explore trends
4.  Compare banks and channels

---

## 👩‍💻 Author

**Swadhika K**  
*Data Analyst | Power BI Developer*  

- 🌐 GitHub:  https://github.com/SwadhikaK/
- 💼 LinkedIn:https://www.linkedin.com/in/swadhikak/
- 📧 Email: swadhika1994@gmail.com


## 📚 Tags
`#PowerBI` `#DataAnalysis` `#MutualFunds` `#FinanceAnalytics`  
`#DAX` `#DataVisualization` `#ExcelPowerQuery`


## 🤝 Contributions

Contributions are welcome --- submit issues or pull requests.

## ⭐ Support

If this project helped you, give the repo a **star ⭐**!
