# Palmoria-Group-Analysis
Palmoria Group, a manufacturing company in Nigeria, is under public scrutiny for gender inequality across its three operational regions. Following negative media coverage, the company seeks to address issues such as gender pay gaps and workforce imbalance.
# Case Study 1: Palmora Group HR Analysis
# 1. Project Overview
The Palmoria Group, a manufacturing company based in Nigeria, is embroiled in issues
bordering on gender inequality in its 3 regions. Unfortunately, the media recently
published the news with the headline “Palmoria, the Manufacturing Patriarchy”. This
doesn’t look good for the owners of the business, based on their ambition to scale the
business to other regions and even overseas. Cases like this can only spiral downwards,
revealing other issues like the gender pay gap, amongst other possible issues.
The CEO of Palmoria, Mr Ayodeji Chukwuma, is keen to address these issues before they
get out of hand. The CHRO, Mr Yunus Shofoluwe, has been assigned the task to identify
key areas within the business that could give rise to issues and address them immediately.
Mr Shofoluwe decided to recruit you as an HR Analytics expert to analyse the company’s
HR data and come up with recommendations for management’s attention. “Now, the
future of gender equality in Palmoria lies in your hands” – the exact words of Mr
Shofoluwe before he handed the data to you.
# 2.CASE SCENARIO
● Analyse the company data and generate insights that the Palmoria management
team would need to address
● Your analysis should be visualised using appropriate charts
● Your focus should be on gender-related issues within the organization and its
regions
● The insights required are based on your discretion. However, Mr Gamma, as an
insider, has offered to give you pointers on areas you need to pay attention to
# 3. Required:
● Generally, there are two genders in the organization. However, some employees
refused to disclose their gender. You would need to assign a generic gender status
to these employees
● Some employees are without a salary because they are no longer with the company.
You will need to take those employees out
● Lastly, some departments are indicated as “NULL”. These departments would also
need to be taken out.
# Pointers from Mr Gamma
# Question 1. What is the gender distribution in the organization? Distil to regions and departments.
## Gender Distribution in Palmoria Group
### Tool Used: Excel Pivot Table
### Approach used:
- Cleaned the dataset to remove rows with no salary or department (as instructed).
- Assigned "Not Disclosed" to blank gender entries.
- Created a Pivot Table with:
  - Rows: Gender
  - Columns: Region, Department
  - Values: Count of Employee ID
### Insight:
- Male employees outnumber females in all regions and most departments.
- Some departments have zero female representation.

# Question 2: Show insights on ratings based on gender
## Performance Ratings by Gender
### Tool Used: Power BI
### Approach used:
- Transformed rating categories (Very Poor, Poor, Average, Good, Very Good) into values.
- Built a stacked bar chart showing gender on the x-axis and ratings on the y-axis.
### Insight:
- Male employees received more high ratings, though they are the majority.
- A balanced look at ratings distribution can guide future HR assessments.

# Question 3. Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management
### Tool Used: Excel & SQL
### SQL Query Summary:
```sql
SELECT gender, department, region, AVG(salary) AS avg_salary
FROM palmoria_employees
GROUP BY gender, department, region;
```
### Insight:
- There is a noticeable pay gap in Engineering and Finance departments.
- Northern region has wider disparities in certain roles.

# Question 4. A recent regulation was adopted which requires manufacturing companies to pay
employees a minimum of $90,000
● Does Palmoria meet this requirement?
● Show the pay distribution of employees grouped by a band of $10,000. For example:
● How many employees fall into a band of $10,000 – $20,000, $20,000 – $30,000,
etc.?
● Also visualize this by regions
### Tool Used: Excel Pivot & Power BI
### Approach used:
- Created salary bands (e.g., $10k-$20k, $20k-$30k, ...)
- Filtered employees earning below $90k
- Counted employees in each band by region
### Insight:
- 17% of employees earn below $90,000
- The South-East has the highest number of underpaid employees

# Question 5: Mr Gamma thought to himself that since you were already working on the employee
data, you could help out with allocating the annual bonus pay to employees based on the
performance rating. He handed you another data set that contains rules for making bonus
payments and asked you to:
● Calculate the amount to be paid as a bonus to individual employees
● Calculate the total amount to be paid to individual employees (salary inclusive of
bonus)
● Total amount to be paid out per region and company-wide

### Tool Used: SQL + Excel
### What Was Done:
- Merged employee dataset with bonus rules (based on performance level)
- Calculated bonus = bonus % × salary
- Computed total payout = salary + bonus
### Insight:
- Average bonus per employee is $5,200
- The Engineering department received the highest cumulative bonus
---

## Power BI Report

This `.pbix` file contains the full Palmoria HR Analysis dashboard, including:

- Gender Distribution by Region and Department
- Salary Structure and Pay Gap Analysis
- Performance Ratings vs Bonus Allocation
- Salary Band Compliance Visualization

### Dashboard Preview
!https://github.com/Estellepeters/Palmoria-Group-Analysis/blob/main/Dashboard%201.png

###  Files Included:
- Palmoria_HR_Analysis_Report.pbix – Main Power BI report
- Palmoria Group emp-data.csv – Source employee dataset
- Bonus Rules.xlsx – Performance bonus mapping


