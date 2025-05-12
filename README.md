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
- What was the total sales and profits trend?
-  What were the top selling categories and invoices?
-  What were most preferred payments over the year?
-  What were the top branches and why?

### Data Analysis
---
We predominantly used excel functions and formulas as demonstrated below;
#### Formulas
  - Sum-used to get total sales, cost of goods sold and profits.
  - Count-used to get total number of transactions.
##### Functions
---
  - Sumifs-used to get total sales and profits per category and salesper branch.
  - Countifs-used to get total transactions and payment modes per category.
  - Xlookup-used to get sales and units quantity per invoice during the year.

#### Findings and results
---
  - January was the top selling month with Kshs. 75,160.51 while April the lowest at Kshs. 2,870.46.
  - Top sales order was invoice no. 860-79-0874 selling as Kshs. 1,042.65.
  - The profits were predetermined at a margin of 5%.
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



