# School District Analysis
School District Analysis using `Anaconda`, `Jupyter Notebook`, `Pandas` &amp; `Python`

## Overview of Project
Here is the list of deliverables for the analysis of the school district: 

* A high-level snapshot of the district's key metrics, presented in a table format
* An overview of the key metrics for each school, presented in a table format
* Tables presenting each of the following metrics:
    * Top 5 and bottom 5 performing schools, based on the overall passing rate
    * The average math score received by students in each grade level at each school
    * The average reading score received by students in each grade level at each school
    * School performance based on the budget per student
    * School performance based on the school size 
    * School performance based on the type of school
Before we can begin these tasks, we need to import the datasets into Jupyter Notebook using Python.

## Background Analysis and Challenges
The school board has notified Maria and her supervisor that the `students_complete.csv` file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. She has asked you to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once you’ve replaced the math and reading scores, Maria would like you to repeat the school district analysis that you did in this module and write up a report to describe how these changes affected the overall analysis.

## Deliverable 1: Replace Ninth-Grade Reading and Math Scores
**Instructions**: Using the Pandas `loc` method with conditional statements and comparison and logical operators, select the ninth-grade reading and math scores for Thomas High School. Then, use the Pandas NumPy module to change the reading and math scores to NaN.

### Deliverable 1 Requirements:

* The `loc` method is used to select all the reading and math scores from the ninth grade at Thomas High School. Inside the `loc` method, the following are completed:

    * A comparison operator is used to retrieve all the rows with Thomas High School in the **"school_name"** column of the `student_data_df`.
    * A comparison operator is used to retrieve all the rows with the ninth grade in the **"grade"** column of the `student_data_df`.
    * Logical and comparison operators are used to retrieve all the rows with the **"reading_score"** column for Thomas High School ninth graders from the `student_data_df`.
    * Logical and comparison operators are used to retrieve all the rows with the **"math_score"** column for Thomas High School ninth graders from the `student_data_df`.
    * The reading and math scores for the ninth graders in **Thomas High school** are replaced with **NaNs**.
 
### Deliverable 1 Results:

![name-of-you-image](https://github.com/DataJew/School_District_Analysis/blob/main/School_District_Analysis/Resources/Deliverable1.png)

## Deliverable 2: Repeat the School District Analysis
**Instructions**: Repeat the school district analysis you did in this module, and recreate the following metrics:

* The district summary 
* The school summary
* The top 5 and bottom 5 performing schools, based on the overall passing rate
* The average math score for each grade level from each school
* The average reading score for each grade level from each school
* The scores by school spending per student, by school size, and by school type

### Deliverable 2 Requirements:

repeating the school district analysis and updating the following required metrics in the `PyCitySchools_Challenge.ipynb` file:

* The district summary DataFrame.
* The school summary DataFrame.
* The top 5 performing schools, based on the overall passing rate.
* The bottom 5 performing schools, based on the overall passing rate.
* The average math score for each grade level from each school.
* The average reading score for each grade level from each school.
* The scores by school spending per student.
* The scores by school size.
* The scores by school type.
 
### Deliverable 2 Results:

(https://github.com/DataJew/School_District_Analysis/blob/main/School_District_Analysis/PyCitySchools_Challenge.ipynb)

## Deliverable 3: A Written Report for the School District Analysis
**Instructions**: For this part of the Challenge, write a report that summarizes your updated analysis and compares it with the results from the module.

The analysis should contain the following:

1. **Overview of the school district analysis** 

2. **Results** 

3. **Summary**

### How is the district summary affected?

**OBSERVATION:** Slight change in Math Score, including % Passing district averages, Comparing the two dataframes above, the average show the difference when the 9th grade student Math and Reading scores from Thomas High Schools were excluded from the District Summary.


### How is the school summary affected?

**OBSERVATION:** Overall order change due to Thomas High School cleanup


### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

**OBSERVATION:** Replacing ninth graders’ math and reading scores affect Thomas High School’s performance between the other schools, Relative ranking for Thomas High School changed from 2nd place to 8th (see images above). 


### How does replacing the ninth-grade scores affect the following:
- 
    * Math and reading scores by grade
        - Math and Reading Scores from Thomas High School 9th Grade set to "nan" and equivalent to 0.
        - Math and Reading Scores from Thomas High School 9th Grade means all of them failed (set to fail for analysis).
        - Doing that, the only significantly score affected was minimal in a very small in quantity. 
        - Student count() Before THS Cleanup was: 1635
        - Student count() After THS Cleanup was: 1174

    * Scores by school spending
        - Thomas HS is in the spending bucket "$630-644"
        - Math and Reading Scores from Thomas High School 9th Grade means all of them failed (set to fail for analysis).
        - Doing that, the only significantly score affected was minimal in a very small in quantity. 
        - Student count() Before THS Cleanup was: 1635
        - Student count() After THS Cleanup was: 1174

    * Scores by school size
        - Removing Thomas High School 9th Grade reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket.

    * Scores by school type
        - Thomas High School is in the "CHARTER" type
        - Removing Thomas High School 9th Grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing"
    

**Summary:** (4) changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs:
   1. Average Math & Reading scores
   2. % Passing Math and Reading scores
   3. Overall Passing marks changes
   4. Changes that are reflected in the funding for each student (Difference each students funding is ~ $200)
