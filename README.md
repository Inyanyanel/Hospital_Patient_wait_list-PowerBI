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
- Current and previous year patients number (DAX)
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
  - There was a 16% increase in patients in the current year from the previous one.
  - The average waiting time was 54 while median was 13.
  - The average and median waiting times gradually decreased as age sets went higher.
  - Accidents cases led on both average and median waiting times, paediatric categories dominated average waiting times while elderly issues dominated median waiting times.
  - Inpatient wait times remained relatively constant, Day cases experienced a slight dip then rise while outpatient cases suffered an gradual rise (of 26%) over time.

#### Recommendations
---
Based on the highlighted observations, we recommend the following courses of actions.
  - Invest in more efficient handling facilities and personel to handle the increasing patient population.
  - 
  - More efficient facilities and staff addressing higher age sets should be increased so as to reduce the average/median waiting time.
  - Specialised facilities addressing fast attendance of accidents, paediatric and elderly cases that require quick attention need to be expanded.
  - Facilities handling oupatients should be expanded on a timely basis to match an always increasing putpatient number over the years.

#### Limitations
---
  - Inpatient and outpatient datasets were not uniform structurewise (i.e they had diferent number of columns and columns titles).
  - A large disparity between Average and median patients waiting time.



