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

Following a report that the reading and math scores for Thomas High School ninth graders were altered, the potentially fraudulent scores were discarded (replaced with NaN) and analysis was repeated with the new dataset. The corrected data is available below.

## The following was delivered for analysis by the school district:

### District-level metrics

A high-level snapshot describing the following for the district as a whole: total number of schools in the district, total number of students in the district, total budget for the district, average math score for all students in the district, average reading score for all students in the district, percent of district students with passing scores (70 or above) on the math test, percent of district students with passing scores (70 or above) on the reading test, and percent of district students with both math and reading scores passing (70 or above).

![Deliverable_2_-_district_summary_df](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20district%20summary%20df.png)

### School-level metrics

The same metrics as above, broken down by data for each school in the district. Additionally, each school is described by its budget per student and its student population size compared to other district schools.

![Deliverable_2_-_per_school_summary_df](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20per%20school%20summary%20df.png)

### Futher break-down of the following six metrics:

#### (1) Top and bottom performing schools in the district

Based on overall passing rate for each school, the top 5 performing schools in the district are (from best to worst): Cabrera HS, Thomas HS, Griffin HS, Wilson HS, Pena HS. The top performing school in the district is Cabrera HS. Cabrera HS is a medium-sized charter school with a budget of <$586/student. All 5 top schools are charter schools. 

![Deliverable_2_-_top_5_schools](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20top%205%20schools.png)

Based on overall passing rate for each school, the bottom 5 performing schools in the district are (from best to worst): Rodriguez HS, Figueroa HS, Huang HS, Hernandez HS, Johnson HS. The worst performing school in the district is Johnson HS. Johnson HS is a large-sized district school with a budget range of $646-675/student. All 5 bottom schools are district schools. 

![Deliverable_2_-_bottom_5_schools](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20bottom%205%20schools.png)

#### (2) The average math score received by students in each grade level at each school

The 9th grade scores for Thomas HS are marked NaN because of potentially fraudulent scores-- these scores were disgarded.

![Deliverable_2_-_math_scores_by_grade](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20math%20scores%20by%20grade.png)

#### (3) The average reading score received by students in each grade level at each school

The 9th grade scores for Thomas HS are marked NaN because of potentially fraudulent scores-- these scores were disgarded.

![Deliverable_2_-_reading_scores_by_grade](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/Deliverable%202%20-%20reading%20scores%20by%20grade.png)

#### (4) School performance based on the budget per student

![deliverable_2_-_spending_summary](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/deliverable%202%20-%20spending%20summary.png)

#### (5) School performance based on the school size 

![deliverable_2_-_size_summary](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/deliverable%202%20-%20size%20summary.png)

#### (6) School performance based on the type of school

![deliverable_2_-_school_type_summary](https://github.com/cewarkentin/School_District_Analysis/blob/main/Images/deliverable%202%20-%20school%20type%20summary.png)

- Overview of the school district analysis, the purpose of this analysis is well defined

### Results

Following discarding the potentially fraudulent 9th grade test scores for Thomas HS, the school district analysis changed in the following ways:
 - The total number of students in the district did not change following discarding the Thomas HS 9th grade test scores.
 - The total budget for the district did not change following discarding the Thomas HS 9th grade test scores.
 - The district's average math score changed from 79.0 to 78.9 following discarding the Thomas HS 9th grade test scores.
 - The district's average reading score did not change following discarding the Thomas HS 9th grade test scores.
 - The percent of students in the district with passing math scores changed from 75.0% to 74.8% following discarding the Thomas HS 9th grade test scores.
 - The percent of students in the district with passing reading scores changed from 86.0% to 85.7% following discarding the Thomas HS 9th grade test scores.
 - The percent of students in the district with overall passing exam scores changed from 65.0% to 64.9% following discarding the Thomas HS 9th grade test scores.

Disregarding the 461 9th grade students at Thomas HS, the population of students included in calculating the average district scores decreased from 39,170 to 38,709. Because the 9th grade population of Thomas HS is small compared to the total number of students in the district, it makes sense that disregarding this data had a small affect on the overall district metrics (if any affect at all).

Additionally, because it is most likely that the fraudulent scores were altered to be better than the real data, it makes sense that disregarding this data caused, if any change at all, a change to decrease the district metrics. This explanation can be confirmed by comparison of Thomas HS scores before and after discarding the potentially altered 9th grade data-- the original data set had a higher average math score, average reading score, % passing math, % passing reading, and % overall passing compared to the data set without the 9th grade data. For example, the original Thomas HS data set including the 9th graders has a 90.9% overall pass rate, while the adjusted data with the 9th graders excluded has a 65.1% overall pass rate. This illustrates that the fraudulent data improved the scores for Thomas HS.

### Summary

Following discarding the potentially fraudulent 9th grade test scores for Thomas HS, the school district analysis changed in the following ways:
 - (1)
 - (2)
 - (3) 
 - (4) 
