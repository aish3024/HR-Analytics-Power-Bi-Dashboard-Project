1. Data Import & Preprocessing:
Import Dataset: Loaded the HR Analytics dataset, which includes various employee attributes such as age, salary, job role, and attrition status.
Missing Values Handling: Checked for missing values using the Column Quality view and filled them using the nearest value (down-fill).
Data Cleaning: Replaced values in the BusinessTravel column (e.g., "Travel_rarely" was corrected to "TravelRarely").
2. Feature Engineering:
New Calculated Field: Created a new column Attrition_count using a conditional formula:
if(HR_Analytics[Attrition]=='Yes', 1, 0), which flags employees who left the company.
Attrition Rate Calculation: Added a new measure Attrition_rate using:
sum([HR_Analytics[Attrition_count]])/sum(HR_Analytics[EmployeeCount]).
3. Dashboard 1: HR Analytics Overview:
Employee Metrics: Displayed various employee metrics including:
Employee Count: Total employees.
Attrition Count: Sum of employees who left.
Attrition Rate: Percentage of employees who left.
Average Age, Salary, and Years: Showed averages for age, salary, and years at the company.
Attrition Analysis:
By Gender, Education, Age Group, and Job Roles.
Job Roles with Attrition Count: Used a matrix to highlight job satisfaction and total attrition.
Salary Slab and Years at Company: Attrition trends based on salary slabs and tenure.
4. Dashboard 2: HR Analytics Attrition by Travel:
Business Travel Attrition: Showed count of attrition based on business travel frequency (e.g., No Travel, Travel Rarely, Travel Frequently).
Root Cause Analysis: Identified root causes of attrition by combining Business Travel and Job Role.
5. Data Visualization:
Used slicers for Department and other key features to filter the data.
Various charts and graphs helped visualize the attrition patterns based on demographics, job roles, and travel frequency.
6. Final Analysis:
Explored key insights and patterns regarding employee attrition, factors such as job satisfaction, salary, and work-life balance, and their influence on turnover.
