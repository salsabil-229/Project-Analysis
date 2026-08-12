# Data Job Market Analysis: Skills, Salaries & Regional Trends

## Overview

This project is a deep-dive analysis of the 2023 data job market, built entirely in Excel to demonstrate advanced data analytics capabilities: **Power Query (ETL), Power Pivot (data modeling), DAX (calculated measures), PivotTables, and advanced PivotCharts.**

As a job seeker myself, I wanted real answers to the questions that actually matter when deciding what to learn and where to look for work: which skills are worth my time, what pay I should expect, and how location changes the picture. Rather than relying on generic advice, I built a full analytical workflow - from raw data to decision-ready visuals - to answer these questions with data.

This repo documents that workflow model by model: what I built, how I built it, what it showed, and what someone could actually do with it.

### The Dataset

I worked with a real-world dataset of 2023 data science job postings, containing job titles, salaries, locations, and the skills listed on each posting. *(Dataset sourced via Luke Barousse's Excel for Data Analytics course.)*

### Questions I Set Out to Answer

1. **Do more skills get you better pay?**
2. **What's the salary for data jobs in different regions?**
3. **What are the top skills of data professionals?**
4. **What's the pay for the top 10 skills?**

### Skills Demonstrated in This Project

- :mag: **Power Query** - Extracting, cleaning, and transforming raw data (ETL)
- :muscle: **Power Pivot** - Building a relational data model across multiple tables
- :abacus: **DAX** - Writing calculated measures for dynamic aggregation
- :bar_chart: **PivotTables** - Summarizing and slicing large datasets
- :chart_with_upwards_trend: **PivotCharts** - Building combo/dual-axis visuals for comparative analysis


## Model 1: Do More Skills Get You Better Pay?

### Skill Displayed:
**Power Query (ETL)**

### Creation Process
I used Power Query to build a proper ETL pipeline rather than working with the raw file directly:

- **Extract:** Pulled in the source workbook (`data_salary_all.xlsx`) and split it into two separate queries - one holding the full job postings data, and one listing every skill tied to each job ID.
- **Transform:** Cleaned both queries by correcting column data types, dropping unnecessary columns, stripping unwanted text, and trimming whitespace so the data would join and aggregate correctly downstream.
- **Load:** Loaded both cleaned queries into the workbook as the foundation for every model that follows.

`data_jobs_all` query after transformation and load:

![Data jobs query](power_query_data_jobs_all.png)

`data_jobs_skills` query after transformation and load:

![Data job skills query](power_query_data_jobs_skills.png)


### Insights/Results
- There's a clear positive correlation between the number of skills listed on a job posting and its median salary - most visible in roles like Senior Data Engineer and Data Scientist.
- Roles requiring fewer skills, like Business Analyst, consistently land at the lower end of the pay scale.

<div align="center"><img src="power_query_skills_vs_salary.png"></div>

### Conclusion
For job seekers, stacking complementary skills is better for increasing earning potential, more so than going deep on a single tool. For employers, this is a useful benchmark; if a role's skill requirements have crept up over time, compensation should be tracking with it, or the posting risks under-pricing the position relative to market.
