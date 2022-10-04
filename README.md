# School District Analysis

## Project Overview

### Purpose

#### Initial Analysis
The purpose of this project was to assist Maria, the Chief Data Scientist for City School District, in analyzing data on student funding and student's standardized test scores. Specifically, my task was to aggregate the data and showcase trends in school performance. This will assist the school board and superintendent in making decisions regarding school budgets and priorities. 

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


## Summary of Relevant Changes After Updating the Analysis

### Decreased Percentage of Students in the District Passing Overall
The greatest reduction in the district summary was the percentage of students passing both math and reading in the school district. This makes sense given that it is the most restrictive criteria, and it would make sense foracademic dishonesty to result in inflated performance in the most difficult measure.

### Increased Average Reading Score for Thomas High School
Interestingly, the average reading score at THS increased (0.047152).The fact average reading score increased despite percentage of students passing decreased suggests there may have been a few very low reading score outliers dragging the average down.

### Decreased Average Reading Score in the District
The average reading score was the least affected in the district summary, only decreasing by (0.022044) after removing the Thomas High School ninth grade scores. This makes sense for this to be the least affected metric if it is true that there were a few exceedingly low reading score outliers in the ninth grade at Thomas High School.

### Top Performing Schools
Thomas High School was the second highest performing school both before and after removing their ninth grade scores. Interestingly, the average reading score at THS increased (0.047152). The other differences were slight reductions in average math score (-0.067412), percentage passing math (-0.086481), percentage passing reading (-0.290130), and percentage passing overall (-0.317688). The differences were slight enough that they would not shown up if this dataframe were rounded to one decimal place. The fact average reading score increased despite percentage of students passing decreased suggests there may have been a few very low reading score outliers dragging the average down. The fact that Thomas High School was still the second highest performing school even after removing the scores makes the scandal seem pointless. 
