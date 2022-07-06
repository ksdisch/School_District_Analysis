# School District Analysis

## Project Overview

### Purpose

#### Initial Analysis
The purpose of this project was to assist Maria, the Chief Data Scientist for City School District, in analyzing data on student funding and student'ss standardized test scores. Specifically, my task was to aggregate the data and showcase trends in school performance. This will assist the school board and superintendent in making decisions regarding school budgets and priorities. 

#### Updated Analysis
After completing the initial analysis, the school board informed Maria and her supervisor that the stuents_complete.csv file showed evidence of academic dishonesty. The dishonest data included the math and reading scores for ninth graderes at Thomas High School. To uphold state-testing standards, Maria tasked me with replacing the dishonest scores with null values, while keeping the rest of the data intact. Once this was complete, I repeated the full school district analysis and examined how the changes affected the results overall. 

### Resources
- Data Source(s): schools_complete.csv, students_complete.csv, missing_grades.csv
- Python3.7 anaconda4.13

## Results

### Effects of Removing Thomas High School Ninth Grade Scores
The list bulleted below reflects how different aspects of the initial analysis were affected by replacing the math and reading scores of ninth graders at Thomas High School with null values. Items with one or no images were not affected by the replacement values.

- District Summary: Slight reductions in average math score, average reading score, percentage passing math, percentage passing reading, and percentage passing overall.
  - Original ![Original district summary](/Resources/district_summary_old.png?raw=true "Title")
 
  - Updated ![Updated district summary](/Resources/district_summary_new.png?raw=true "Title")
 
- School Summary: 
  - Original ![Original school summary](/Resources/school_summary_old.png?raw=true "Title")
 
  - Updated ![Updated school summary](/Resources/school_summary_new.png?raw=true "Title")
 
- Thomas High School's Performance Relative to Other Schools: 
![Updated top 5 schools summary](/Resources/top_schools_new.png?raw=true "Title")

- Math Scores by Grade: This dataframe was unaffected because we summarized the scores by grade for each school. As a result, the only change was the value for ninth grade at Thomas High School was NaN in the dataframe versus 83.6 originally.

- Reading Scores by Grade: This dataframe was unaffected because we summarized the scores by grade for each school. As a result, the only change was the value for ninth grade at Thomas High School was NaN in the dataframe versus 83.7 originally.

- Scores by School Spending: This dataframe was unaffected after rounding to 1 decimal place.
- Scores by School Size: This dataframe was unaffected after rounding to 1 decimal place.
- Scores by School Type: This dataframe was unaffected after rounding to 1 decimal place.


## Summary

### District Summary
The metrics for the district were worse, but only slightly. There reductions in average math score (-0.054838), average reading score (-0.022044), percentage of students passing math (-0.220461), percentage passing reading (-0.145797), and percentage of students passing overall (-0.316608).

### Top Performing Schools
Thomas High School was the second highest performing school both before and after removing their ninth grade scores. The only differences were slight reductions in average math score, average reading score, percentage passing math, percentage passing reading, and percentage passing overall. The differences were slight enough that they would not shown up if this dataframe were rounded to one decimal place.
