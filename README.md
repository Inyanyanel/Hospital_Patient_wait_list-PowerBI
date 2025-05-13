# Hospital_Patient_wait_list-PowerBI

## Table Of Contents
---

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools used](#tools-used)
- [Data preparation](#data-preparation)
- [Explanatory analysis](#explanatory-analysis)
- [Data Analysis]($data-analysis)
- [Functions](#functions)
- [Findings and results]($findings-and-results)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview
---

This data analysis project aims to provide insights on the patients waiting times of a certain hospital. We are seeking to identify various patients categories trends, gain a deeper understanding of the underlying causes and make recommendations on how to improve on the current metrics.

### Data Sources
---

Patients Data: The primary dataset used for this analysis was downloaded from a youtube tutorial with the link attached. [Check Here](https://pivotalstats.com/wp-content/uploads/2024/09/Data-Mapping-Bg.zip).

### Tools used
---

- Microsoft Power BI - Used to clean, transform, analyse and visualisation.

### Data preparation
---

- Data loading and merging using power query.
- Used replace function to remove duplicate values.
- Used transform tool to change dates from text to date format.
- Used data modelling tool to create the tables relationships and interactivity.

### Explanatory analysis
---
- What was the current year wait times as compared to previous year?
- What were the average/median wait times for various categories?
- What was the waiting time when categorised by patients agesets?
- What were the top 5 patients specialty wait times?
- What were the monthly trending analysis for inpatient, oupatient and day case categories?

### Data Analysis
---
We predominantly used Power BI visuals and DAX formulas as demonstrated below;
- Current and previous month wait list (DAX)
```DAX
Latest month wait list = CALCULATE(SUM('All Data'[Total]),'All Data'[Archive_Date] = MAX('All Data'[Archive_Date])) + 0
PY month wait list = CALCULATE(SUM('All Data'[Total]),'All Data'[Archive_Date] = EDATE(MAX('All Data'[Archive_Date]),-12)) + 0
```

- Average and median wait times for various categories.
```DAX
Average wait list = AVERAGE('All Data'[Total])
Median wait list = MEDIAN('All Data'[Total])
```
- Waiting time by age.
Used a Stacked column chart with Average/Median waiting times on the Y-axis and Time bands on the x-axis supported by the Age profiles on the legend sections.

- Top 5 patients specialty wait times.
Used a multi row card containing Average/Median waiting times and Specialty names.

- Monthly trending analysis for patient categories.
Used a line chart having Total waiting time on the Y-axis and Archive dates on the X-axis.

---

#### Findings and results
---
  - There was a 16% increase in patient waiting time in the current year from the previous one.
  - The average waiting time was 54 while median was 13.
  - The average and median waiting times gradually decreased as age sets went higher.
  - The company experienced boom in sales fo the first quarter then sales dwindeled in the latter quarters.
  - Foods and beverage was the top selling category during the year.
  - Branch sales were evenly distributed during the year.
  - Payment modes of cash, credit card and e-wallet were evenly used across the period.
  - Alexandria branch dominated on food and beverage sales (47%), Giza on home & lifestyle (43%), Cairo on health & beauty (39%).

#### Recommendations
---
Based on the highlighted observations, we recommend the following courses of actions.
  - Invest in marketing promotions to boost sales in the latter three quarters.
  - Incentives should be offered on food and beverage category to boost sales.
  - Each branch need to adopt its top selling category into a respective flagship outlet to bost sales.
  - Profit margin need to be slightly slashed to 4% to reduce the price in order to try boost sales in the last three quarters.

#### Limitations
---
  - Inpatient and outpatient datasets were not uniform structurewise (i.e they had diferent number of columns and columns titles).

#### References
---
  - Excel advanced skills for business [Check here](https://coursera.org/share/4282d5f46dce95bf970f7084e2200d72)
  - Excel fundamentals for data analysis [Check here](https://coursera.org/share/3644ab5effb80789d6d71f61816530ef)



