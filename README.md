# Remote Work Productivity Analysis

## Team Project

A data analysis project focused on exploring remote work productivity and identifying patterns related to work arrangement, department, region, company size, and job level.

## Dataset

**Dataset:** Remote Work Productivity 2026  
**Source:** Kaggle  
**Records:** 10,000  
**Columns:** 21

## Team Members

- Istabraq Sherif
- Gehad Yasser

## Project Objective

The main objective of this project is to clean, transform, analyze, and visualize remote-work survey data to identify patterns and relationships between work conditions, employee well-being, and productivity-related measures.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SQLite
- Jupyter Notebook

## Project Workflow

### 1. Data Extraction
- Loaded the dataset using Pandas.
- Examined the dataset structure, data types, and statistical summary.
- Checked missing values and duplicate records.
- Validated categorical and numerical values.

### 2. Data Cleaning & Transformation
- Converted `Survey_Date` to datetime format.
- Standardized categorical values.
- Created additional date features such as:
  - Survey Year
  - Survey Month
  - Survey Weekday
  - Survey Quarter
- Created analytical groups for:
  - Meeting Intensity
  - Focus Hours
  - Work Arrangement
- Created a High Burnout flag based on the project-defined threshold.

### 3. Exploratory Data Analysis

The analysis focused on:

- Comparing Focus, Collaboration, Work-Life Balance, and Satisfaction across work arrangements.
- Comparing Satisfaction, Burnout, and Tasks Completed across departments and job levels.
- Analyzing differences across regions and company sizes.
- Examining monthly trends in satisfaction, burnout, focus, and task completion.
- Exploring correlations between meetings, focus, burnout, commute, work-life balance, satisfaction, and task completion.
- Comparing high-burnout rates across work arrangements.
- Analyzing Work Arrangement × Job Level combinations.
- Comparing communication and project tools based on collaboration, response time, and task completion.

### 4. Data Visualization

Created visualizations to communicate the main findings, including comparisons of:

- Work Arrangement
- Department
- Job Level
- Region
- Company Size
- Burnout Risk
- Satisfaction
- Focus
- Response Time
- Task Completion

### 5. Data Modeling & Database

Created a fact table:

`cleaned_survey_responses`

with `Employee_ID` as the primary key.

Created summary tables for:

- Work Arrangement
- Department
- Region
- Month
- Company Size & Job Level

The processed data and summary tables were loaded into a SQLite database named:

`remote_work.db`

### 6. ETL Process

The project follows an ETL workflow:

**Extract → Transform → Analyze → Load → Validate**

The final outputs include:

- Cleaned dataset in CSV format
- Summary tables in CSV format
- SQLite database
- ETL log

## Key Findings

- Work arrangement was the clearest differentiating factor in the dataset, particularly for burnout risk, focus, and response time.
- Office employees showed a substantially higher high-burnout rate compared with Hybrid and Remote employees.
- Remote employees showed stronger average focus.
- Office employees showed the shortest average response time.
- Differences between departments, regions, and company sizes were relatively small for average satisfaction and burnout.
- Correlation analysis helped identify relationships between meeting time, commute, focus, work-life balance, satisfaction, burnout, and task completion.

## Recommendations

- Consider flexible or hybrid work arrangements where job requirements allow.
- Investigate factors contributing to higher burnout among Office employees.
- Review meeting practices and their relationship with focus and burnout.
- Consider communication expectations separately from employee well-being.

## Limitations

- The dataset is cross-sectional and does not track the same employees over time.
- Several measures are self-reported.
- The sampling method and represented population are not documented in the supplied dataset.
- Some analytical thresholds were defined specifically for this project.
- The dataset covers six months, limiting long-term trend analysis.
- Correlation and group comparisons do not establish causation.

## Conclusion

This project demonstrates an end-to-end data analysis workflow, from data extraction and cleaning to exploratory analysis, visualization, data modeling, SQLite database loading, and final validation.

The analysis highlights work arrangement as an important differentiating factor in employee well-being and productivity-related measures.
