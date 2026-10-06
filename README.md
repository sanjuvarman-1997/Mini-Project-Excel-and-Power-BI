[HR_Analytics_Employee_Master_README.md](https://github.com/user-attachments/files/33085217/HR_Analytics_Employee_Master_README.md)
# HR Analytics Employee Master

> **Tools:** Power BI | Excel | DAX | Power Query | Data Modeling  
> **Domain:** Human Resources / Workforce Analytics

## 📌 Project Overview

The **HR Analytics Employee Master** project analyzes employee workforce data to understand headcount, employee status, salary distribution, performance ratings, department-level workforce patterns, job-role structure, gender distribution, and employee termination trends.

The project uses **Microsoft Excel** for data preparation and **Power BI** for data modeling, KPI creation, visualization, filtering, and interactive dashboard development.

The final solution provides a consolidated view of the workforce and helps HR teams identify areas that may require attention, such as departments with higher termination rates, salary differences across departments and roles, and performance patterns across employee groups.

## 🎯 Project Objectives

- Analyze overall employee headcount and workforce status.
- Compare **Active** and **Terminated** employees.
- Understand salary distribution across departments, genders, and job titles.
- Analyze employee performance ratings and identify department-level patterns.
- Compare employee distribution across departments and job roles.
- Analyze termination patterns and identify departments with relatively higher turnover.
- Build an interactive Power BI dashboard with KPIs, charts, tables, slicers, and employee-status analysis.
- Convert cleaned employee data into business-ready HR insights.

## 📊 Dataset

The source dataset contains **500 employee records** with **12 fields**.

| Column | Description |
|---|---|
| `EmployeeID` | Unique identifier assigned to each employee |
| `FullName` | Employee full name |
| `Department` | Department in which the employee works |
| `JobTitle` | Employee job role/title |
| `Email` | Employee email address |
| `Gender` | Gender category recorded for the employee |
| `HireDate` | Employee joining date |
| `TerminationDate` | Employee termination date, where available |
| `Salary` | Employee salary value |
| `ManagerID` | Identifier of the employee's manager |
| `PerformanceRating` | Employee performance rating |
| `Status` | Current recorded employee status such as Active or Terminated |

### Dataset Summary

| Metric | Value |
|---|---:|
| Total Employees | **500** |
| Active Employees | **436** |
| Terminated Employees | **64** |
| Active Rate | **87.20%** |
| Termination Rate | **12.80%** |
| Average Salary | **93,181.34** |
| Median Salary | **76,425.50** |
| Minimum Salary | **55,020** |
| Maximum Salary | **179,979** |
| Average Performance Rating | **3.49** |
| Departments | **9** |
| Job Titles | **25** |

## 🔍 Problem Statement

The HR team needs a clear view of its employee master data to answer the following business questions:

1. How many employees are currently active versus terminated?
2. Which departments have the highest and lowest employee headcount?
3. Which departments have the highest and lowest average salary?
4. Which departments show higher termination rates?
5. How is employee performance distributed across the workforce?
6. Which job titles have the highest average salary?
7. How does salary vary across gender groups?
8. How are employees distributed by gender and employment status?
9. What hiring and termination date patterns are present in the dataset?
10. How can HR use these insights to improve workforce planning and retention?

## 📈 Dashboard Features

The Power BI file includes a multi-page report with the following analysis pages:

- **Dashboard** – Main HR overview with KPI cards and multiple workforce visuals.
- **Column Chart** – Department and gender-based employee status analysis.
- **Bar Chart** – Department-wise salary analysis.
- **Donut Chart** – Employee distribution by gender and status.
- **Pie Chart** – Department/status-based employee distribution.
- **KPI** – Key employee and performance indicators.
- **Slicer** – Interactive filters for Department, Gender, Status, and Performance Rating.

### Main Dashboard Visuals

The primary dashboard includes:

- KPI Cards for **Total Employees**, **Active Employees**, **Terminated Employees**, **Average Performance**, and **Total Salary**.
- Department-wise employee count.
- Department-wise average salary.
- Performance rating analysis by gender.
- Employee status summary table.
- Salary distribution by gender.
- Active employees by department.
- Terminated employee analysis using a matrix.
- Interactive filtering using HR-related slicers.

## 🛠️ Tools & Technologies

- **Power BI** – Dashboard development, data visualization, interactive reporting.
- **Power Query** – Data cleaning and transformation.
- **DAX** – Measures and KPI calculations.
- **Microsoft Excel** – Source data preparation, employee master creation, and supporting analysis.
- **Data Modeling** – Structuring employee data for Power BI reporting.

## 🧹 Data Cleaning & Preparation

The project included data preparation steps before analysis:

- Reviewed the employee master dataset for missing values.
- Checked employee IDs for duplicate records.
- Standardized the employee master structure for Power BI.
- Prepared salary and performance fields for aggregation.
- Prepared employee status for Active/Terminated analysis.
- Reviewed date fields for hire and termination trend analysis.
- Created a dedicated `Employee_Master` sheet for reporting.
- Built supporting pivot analysis in Excel.

### Data Quality Note

The source `Raw Data` contains **436 blank TerminationDate values**, which mainly correspond to employees recorded as Active. It also contains **135 blank ManagerID values**.

In the Excel `Employee_Master` output, active employees' blank termination dates are represented as **31-12-1899**. This value should be treated as a placeholder rather than a real termination date. For a production HR system, it is better to retain a true blank/null value and use the `Status` field for active/terminated logic.

The `Employee_Master` sheet also contains an additional average-salary formula row below the 500 employee records; this summary row should not be counted as an employee record in Power BI.

## 📌 Key Analysis Areas

### 1. Workforce Overview

The dataset contains **500 employees**, of which **436 are Active** and **64 are Terminated**. This results in an **87.20% active rate** and a **12.80% termination rate**.

### 2. Department Analysis

**IT Support** has the highest employee count with **61 employees**, followed by **Quality Control with 60**.

**Human Resources** has the smallest headcount with **50 employees**.

Department-level salary and performance patterns show meaningful differences across teams:

| Department | Employees | Avg Salary | Avg Performance | Termination Rate |
|---|---:|---:|---:|---:|
| Sales | 57 | 128,985.93 | 3.60 | 12.28% |
| Quality Control | 60 | 111,427.93 | 3.58 | 11.67% |
| IT Support | 61 | 105,249.90 | 3.56 | 14.75% |
| Production | 55 | 97,626.07 | 3.51 | **20.00%** |
| Marketing | 55 | 90,088.80 | 3.45 | **7.27%** |
| Research & Development | 55 | 88,910.95 | 3.58 | 9.09% |
| Finance | 56 | 70,226.30 | 3.11 | 16.07% |
| Logistics | 51 | 69,931.12 | **3.75** | 11.76% |
| Human Resources | 50 | **68,379.42** | 3.24 | 12.00% |

### 3. Salary Analysis

The overall average salary is **93,181.34**, while the median salary is **76,425.50**.

- **Sales** has the highest department-level average salary at **128,985.93**.
- **Human Resources** has the lowest department-level average salary at **68,379.42**.
- The highest average salary among job titles is for **Regional Sales Manager: 153,967.64**.
- Other highly paid roles include **IT Manager: 152,334.62** and **Operations Manager: 151,622.84**.

### 4. Performance Analysis

The overall average performance rating is **3.49**.

| Performance Rating | Employees |
|---:|---:|
| 2 | 130 |
| 3 | 113 |
| 4 | **140** |
| 5 | 117 |

A rating of **4** is the most common performance level in the dataset.

At department level:

- **Logistics** has the highest average performance rating at **3.75**.
- **Finance** has the lowest average performance rating at **3.11**.

### 5. Gender Analysis

The workforce is distributed as follows:

| Gender | Employees | Avg Salary | Avg Performance | Termination Rate |
|---|---:|---:|---:|---:|
| Male | 194 | 89,237.26 | 3.45 | 11.86% |
| Non-binary | 177 | **97,893.15** | **3.55** | 14.12% |
| Female | 129 | 92,647.69 | 3.45 | 12.40% |

The **Male** group has the largest employee count, while the **Non-binary** group has the highest average salary and average performance rating in this dataset.

### 6. Termination Analysis

The dataset contains **64 terminated employees**.

By department:

- **Production** has the highest termination rate at **20.00%**.
- **Finance** follows at **16.07%**.
- **IT Support** has a termination rate of **14.75%**.
- **Marketing** has the lowest termination rate at **7.27%**.

This suggests that Production and Finance may deserve closer review for retention, workload, role structure, compensation alignment, or other workforce factors.

### 7. Hiring & Termination Date Analysis

Hiring records are concentrated in:

- **2025 – 308 hires**
- **2026 – 192 hires**

The termination records in the dataset span **2026 to 2031**. Because several termination dates are future-dated relative to a normal current HR snapshot, these dates should be validated before using them for real-world attrition or tenure reporting.

## 💡 Business Insights

The dashboard and supporting Excel analysis highlight the following key observations:

- The workforce is predominantly active, with an **87.20% active rate**.
- **IT Support** is the largest department by headcount.
- **Sales** has the strongest average salary among departments.
- **Production** has the highest termination rate and should be prioritized for retention investigation.
- **Marketing** has the lowest termination rate, making it useful as a benchmark for workforce stability.
- **Logistics** has the highest average performance rating despite having one of the lower department salary averages.
- **Finance** has the lowest average performance rating and a relatively high termination rate, indicating an area for management review.
- Higher-paid managerial roles dominate the top salary averages.
- The dashboard can help HR compare employee status, department, gender, and performance dynamically.

## 🎯 Recommendations

Based on the analysis, the following HR actions can be considered:

1. **Investigate Production turnover**  
   Review workload, role expectations, manager structure, compensation, and employee feedback in Production.

2. **Review Finance workforce performance**  
   Study training needs, role fit, performance management, and retention drivers in Finance.

3. **Benchmark compensation by role and department**  
   Compare similar job titles across departments to identify salary gaps and maintain internal consistency.

4. **Use performance and status together**  
   Evaluate whether terminated employees show different performance patterns from active employees before making retention decisions.

5. **Improve date-field quality**  
   Keep missing termination dates as null/blank instead of using a placeholder date such as 31-12-1899.

6. **Extend the dashboard for future HR planning**  
   Add tenure, attrition rate by year/month, age analysis, manager-level analysis, and compensation bands when those fields become available.

## 📈 Dashboard Preview

> **Add your Power BI Dashboard screenshot here when uploading the project to GitHub.**
>
> Suggested GitHub image path:
>
> `images/hr-analytics-dashboard.png`

## 📁 Suggested Project Structure

```text
HR-Analytics-Employee-Master/
│
├── README.md
├── HR_Analytics_Employee_Master.pbix
├── HR_Analytics_Employee_Master.xlsx
└── images/
    └── hr-analytics-dashboard.png
```

## 🚀 Project Outcome

This project demonstrates an end-to-end **HR analytics workflow** using Excel and Power BI.

The solution transforms employee master data into an interactive reporting layer that covers:

- Workforce size and status
- Department performance
- Salary distribution
- Job-role salary patterns
- Performance ratings
- Gender distribution
- Termination patterns
- Interactive HR filtering

The final dashboard provides a single view of important workforce metrics and supports more data-driven HR decision-making.

## 📌 Conclusion

The **HR Analytics Employee Master** project provides a structured view of employee workforce information using Power BI, Power Query, DAX, Excel, and data modeling.

The analysis identifies differences in department headcount, salary, performance, and termination rates. In particular, **Production shows the highest termination rate**, **Sales shows the highest average salary**, **Logistics records the highest average performance**, and **Finance requires attention due to its lower average performance and higher termination rate**.

Overall, the project demonstrates how HR master data can be transformed into practical workforce insights through data cleaning, KPI analysis, visualization, and interactive reporting.

## 👤 Author

**Sanjuvarman G**  
Data Analytics Learner | Excel | Power BI | SQL | Python

## 🏷️ Tags

`Power BI` `HR Analytics` `Employee Analytics` `Human Resources` `Workforce Analytics` `Employee Master` `Power Query` `DAX` `Excel` `Data Modeling` `Data Visualization` `Dashboard` `Performance Analysis` `Salary Analysis` `Attrition Analysis`

---

⭐ **Portfolio Project:** HR Analytics Employee Master
