# Project-Two
---

### Project 2 Topic: Palmoria Group HR Analysis
----

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

### Code Used
---
An analysis of comparation on both Top 10 Customers and 10 Bottom customers activities were dawn, for the KMS to increase the revenue from the 10 Bottom Customers this following points are what contributed to the revenue increasement in Top Customers, which must be put into:

'''  SQL
  Avg Female Salary = CALCULATE(AVERAGE('Sheet1'[Salary]
'''

Avg Male Salary = CALCULATE(AVERAGE('Sheet1'[Salary]))
Gender Count = COUNTROWS('Sheet1' )
GenderPayGap = [AvgM.Salary]-[AvgF.Salary]
BelowMinimumPay = CALCULATE(COUNTROWS('EmployeeData'),'EmployeeData'[Salary] < 90000)
SalaryBand = VAR SALARYAMOUNT= 'EmployeeData'[Salary] VAR Bandsize = 10000 VAR LowerBound = INT('EmployeeData'[Salary]/ Bandsize) *Bandsize VAR UpperBound = LowerBound + Bandsize RETURN "$" & FORMAT (LowerBound, "#,0")& "-$"& FORMAT(UpperBound, "#,0")
 BonusPercentage = LOOKUPVALUE(BonusRules[BonusPercentage],BonusRules[Rating], EmployeeData[Rating], BonusRules[Department], EmployeeData[Department])
 BonusAmount = EmployeeData[Salary]*[BonusPercentage]
TotalCompany Payout = Sum(EmployeeData[BonusAmount])
New Salary = EmployeeData[Salary]+EmployeeData[BonusAmount]

