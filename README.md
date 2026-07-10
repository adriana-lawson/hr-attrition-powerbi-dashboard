# Employee Attrition Analysis: Power BI Dashboard

For this project, I built an interactive Power BI dashboard analyzing employee attrition using IBM's publicly available HR analytics dataset, covering 1,470 employees. The goal was to identify where attrition is highest and what factors seem to be driving it, in a format someone could actually explore rather than just read.

## The Questions I Set Out to Answer

1. What is the overall attrition rate, and how does average income compare across the company?
2. Which departments and job roles have the highest attrition?
3. Does working overtime relate to whether an employee leaves?
4. Can a user filter and explore these patterns interactively by department and gender?

## What I Found

The overall attrition rate across the company is 16.12%, with an average monthly income of roughly $6,500. Breaking this down further revealed some clear patterns. Sales and Human Resources both show noticeably higher attrition than Research & Development. Looking at job role specifically told an even sharper story: Sales Representatives have by far the highest attrition rate of any role, at close to 40%, more than double the next-highest roles. This level of detail wasn't visible from the department view alone, which is part of why I built both.

I also looked at whether working overtime relates to attrition, and found a clear pattern: employees who work overtime leave at a substantially higher rate than those who don't, suggesting workload may be a meaningful factor in retention.

## Data Cleaning and Setup

Before building any visuals, I cleaned the dataset in Power Query. I removed three columns (EmployeeCount, StandardHours, Over18) that had the same single value across every employee and added nothing analytically. I also checked EmployeeNumber against the full dataset, not just a sample, to confirm there were no duplicate employee records before building anything on top of it.

## Dashboard Features

- Two KPI cards showing overall attrition rate and average monthly income
- Three comparative bar charts breaking down attrition by department, job role, and overtime status
- Two interactive slicers (department and gender) that let a user filter the entire dashboard at once, with all visuals updating together

## Tools & Skills Demonstrated

- **Power BI:** Power Query for data cleaning, DAX measures for custom calculations, interactive slicers for filtering
- **DAX:** Wrote custom measures using DIVIDE, CALCULATE, COUNTROWS, and AVERAGE to calculate attrition rate and average income dynamically
- **Data quality investigation:** identifying and removing constant-value columns, verifying no duplicate records existed
- **Dashboard design:** building a cohesive, interactive layout rather than a static report

## Project Structure

```
hr-attrition-powerbi-dashboard/
├── data/               # IBM HR Analytics Employee Attrition dataset
├── screenshots/        # Dashboard preview image
├── hr_attrition_dashboard1.pbix
└── README.md
```

## Data Source

IBM HR Analytics Employee Attrition & Performance dataset, a publicly available synthetic dataset of 1,470 employees, commonly used for HR analytics practice.

## What I'd Do Next

I'd like to add a second dashboard page focused specifically on the Sales department, since it showed both the highest department-level attrition and the highest-attrition individual role, to explore what else might be contributing to turnover there specifically.
