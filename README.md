# Project-Two
---

### Project 2 Topic: Palmoria Group HR Analysis
----
[Project Overview](#project-overview)

[Data Source](#data-source)

[Tools Used](#tools-used)

[Data Cleasing and Preparation](#Data-cleasing-and-preparation)

[Explotory Data Analysis](#explotory-data-analysis)

[Data Analysis](#data-analysis)

[Key Insights](#key-insights)

[Dashboard Features](#ddatshboard-features)

### Project Overview
---
Palmora Group, a manufacturing company based in Nigeria, embroiled in issues bordering on gender inequality in its 3 regions. Recently, the company was published as "Palmoria, the Manufacturing Patriachy"' and because of their ambition to scale the business to other regions and even overseas, they decided to find solution issues like the gender gap pay, amongst other issues. Two excel files were shared gnerate insight that can addressed the company issues in the area of gender-related within the company & regions to be  analysed and visualised with appropriate charts.

### Data Source
---
The primary source of that used here are Palmoria Grop Employee.ulsx and Palmoria Grop Bonus Rules.ulsx, which was extracted, transformed and loaded for analysis and visuliation purposes.

### Tools Used
---
- Power BI for creating report [Download Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
- Clt G was used to assign generic name into the blank fields, remove of past employees and NULL department
- Data Cleasing and Preparation
- Unpivot command was used
- Relationship was created beweet two tables
- The datasets were given, is a well struture data, transformed, thereafter downloaded into Power Bi
- DAX and Power Query

### Explotory Data Analysis.
---
EDA was exploring to generate answer the following question in respect of available datasets:

### Pointers from Mr. Gamma, an insider of Palmoria Group
---
- What is the gender distribution in the organisation? Distil to regions and departments
- Show insights on ratings based on gender?
- Analse the company's salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management?
- A recent regulation was adopted which regquires manufacturing companies employees a minimum of $90,000
  - Does Palmoria meet this requirement?
  - Show the pay distribution of employees grouped by a band of $10,000. For example:
  - WHow many employees fall into a band of $10,000 - $20,000, $20,000 - $30,000, etc.?
  - Also visualize this by regions
- Which consumer was the most profitable one?
- Which customer returned items, and what segment do they belomng to?
- If the delivery truck is the most economical but the slowest shipping methond and Express Air, is the fastest but the most expensive one, do you think the company appropriately spent shipping costs based on the Order Priority? Explain your answer

### Data Analysis
---
This is where some basic functions/outline were used such as:
- Extraction of Dataset from csv files, transformed and loaded
- Creation of Measure and Columm for the following:
  - Average Female Salary
  - Average Male Salary
  - BelowMinimumPay
  - Bonusamount
  - BonusPecentage
  - GenderCount
  - GenderPayGap
  - New Salary
  - TotalCompany Payout

## 🎯 Key Insight
---
👥 Gender Distribution by Department
* Gender balance varies by department.

* Some departments have a higher male or female presence, with others showing equal or unspecified distributions.
  
🌍 Gender Distribution by Region
* Employees are located across Abuja, Kaduna, and Lagos.

* Each region shows different trends in gender representation.

### ✅ Gender Pay Gap
---
- The **Engineering** department at **kaduna** & **Lagos** shows a reverse gender pay gap favoring women by **52.07%** & **11.05%** respectively.
- The **Human Resources** department at **Abuja** has the highest gender pay gap at **25.14%** in favor of men.
- 
### ✅ Salary Distribution
---
- Distribution is shown in **$10,000** salary bands.
- The majority of employees earn between **$60,000 – $90,000**.
- **654 employees** earn less than **$90,000** annually.

### ✅ Employee Ratings
---
- Female and male employees have similar rating distributions.
- A significant number of employees remain **"Not Rated"**, indicating room for improved evaluation practices.

### ✅ Bonus Payouts
---
- Bonus payouts vary across regions with **Lagos** receiving the highest at **$825.91K**.
- Individual bonuses and updated salaries are tracked per employee.Department], EmployeeData[Department])

## Dashboard Features📂 
---

- 📌 Gender-based salary & bonus analysis
- 📌 Department-level insights
- 📌 Ratings distribution by gender
- 📌 Regional breakdowns for total pay and bonuses
- 📌 Visual drill-through for individual employee analysis



