# School District Analysis

## Overview of Project

### Purpose

For this project, we are working with Maria, the chief data scientist for a city school district, to prepare standardized test data for analysis, reporting, and presentation to provide insights about performance trends and patterns.

Analysis of the provided data will assist the school board and superintendent in making decisions regarding the school budgets and prioritites.

### Process

Two CSV files were provided containing the following information:

(1) schools_complete.csv
- School name
- School type (District vs. Charter school)
- School population size
- School budget

(2) students_complete.csv
- Student name
- Student gender
- Student grade level
- Student's school of attendance
- Student's reading score
- Student's math score

Python, Jupyter Notebook, and Pandas libraries were used for data anaylsis.

The data had to first be prepared for use by cleaning incorrect student names.

Following cleaning of the data, the data from the two independent CSV files were merged into one working DataFrame. The following was delivered for analysis by the school district:

- A high-level snapshot of the district's key metrics, presented in a table format
- An overview of the key metrics for each school, presented in a table format
- Tables presenting each of the following metrics:
  - Top 5 and bottom 5 performing schools, based on the overall passing rate
  - The average math score received by students in each grade level at each school
  - The average reading score received by students in each grade level at each school
  - School performance based on the budget per student
  - School performance based on the school size 
  - School performance based on the type of school

Following a report that the reading and math scores for Thomas High School ninth graders were altered, the potentially fraudulent scores were discarded (replaced with NaN) and analysis was repeated with the new dataset.

## Analysis

The following was delivered for analysis by the school district:

### A high-level snapshot of the district's key metrics, presented in a table format

![Deliverable_2_-_district_summary_df](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20district%20summary%20df.png)

### An overview of the key metrics for each school, presented in a table format

### Tables presenting each of the following metrics:

#### Top 5 and bottom 5 performing schools, based on the overall passing rate

![Deliverable_2_-_top_5_schools](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20top%205%20schools.png)
![Deliverable_2_-_bottom_5_schools](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20bottom%205%20schools.png)

#### The average math score received by students in each grade level at each school

#### The average reading score received by students in each grade level at each school

#### School performance based on the budget per student

#### School performance based on the school size 

#### School performance based on the type of school

- Overview of the school district analysis, the purpose of this analysis is well defined

### Results
- There is a bulleted list that addresses how each of the seven school district metrics was affected by the changes in the data

### Summary

- There is a statement summarizing four changes to the school district analysis after reading and math scores have been replaced
