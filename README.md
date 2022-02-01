## Overview of the school district analysis: Explain the purpose of this analysis.

The researchers would like to know the  15 schools of math and reading performance of the high school students. The schools have different budgets and are located in different districts. 
However, the previous data analysis showed evidence of academic dishonesty, which came from Thomas High School; specifically, reading and math grades for Thomas High School ninth-graders appear to have been altered. 
Now school boarding asked the clients to recalculate all school data without calculating nine-grade students from Thomas High School. Since Thomas High school had a ninth-grade problem, it will not include the ninth grade in all data analysis. 
We expected some changes to the original data, not only the whole school's performance but also Thomas high school's performance on math and reading. In the following section, we will calculated math and reading without nine-grade Thomas high school students.

### Basic strategies of reculculations:

First step, replace the math and reading performance from the nine-grade students from thomas High school as NAN using np.nan and loc functions.
Second step, repeat all analysis as previosu steps where Thomas High is considered as normal performance.
Third step, replace teh new grades percentages to the old one by keeping data format same.

## Deliverable 1: Replace ninth-grade reading and math scores

Using the following code replace 9-grade students' reading and math performance for NAN as using np.nan from Numpy.
code: student_data_df.loc[((student_data_df["school_name"]=="Thomas High School") & (student_data_df["grade"]=="9th")),"math_score"]=np.nan
student_data_df.head(10)
student_data_df.tail(10)


After replaing NAN we checked the Thoams High School info : it is as below: <class 'pandas.core.frame.DataFrame'> Int64Index: 461 entries, 37537 to 39167 Data columns (total 7 columns): Column Non-Null Count Dtype

0 Student ID 461 non-null int64
1 student_name 461 non-null object 2 gender 461 non-null object 3 grade 461 non-null object 4 school_name 461 non-null object 5 reading_score 0 non-null float64 6 math_score 0 non-null float64 dtypes: float64(2), int64(1), object(4) memory usage: 28.8+ KB

Therefore, total 461 student's grades from math and reading are not effective in this data anlysis

## Deliverable 2 : Repeat the school district analysis¶

### District Summary

#### Results

#### How is the district summary affected?

the reading, math performance in percentage and average are slightly dropped compared to the old one in which Thomas High school data was complete. Withough any statistic test it is hard to tell the differences were significant or not.

![Alt text](new_district_summary_df.png) 
![Alt text](ols_district_summary_df.png)

#### How is the school summary affected?

There are huge differences of students performance in math and reading in terms of school. Since Thomas High school nine-grades data was removed from the whole analysis. This total number of the students did not change therefore when we calculated the average, all average score dropped becasue of lacking data for nine-grades.

![Alt text](new_per_school_summary.png)
![Alt text](old_per_school_summary.png)

#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Thomas high school, before the finding dishonesty, was one of the top High school in terms of overall passing percentages. After recalculations,  the passing math percentage  was dropped from original 93.27% to 66.91%, and same as passing reading percentages from 97.3% to 69.66%, and overall passing percentages from 90% to 65 %. However, the average math and reading did not change much from the original data with considering nie-grades of from Thomas High School. 


#### How does replacing the ninth-grade scores affect the following:


##### Math and reading scores by grade


There were no significant differences in terms of math grading among schools-anylisis with Thomas high nine grade and without it. However, in post analysis which is the analysis of without considering Thomas High nine-grades,only difference was Thomas High nine-grade as NAN for average math. (no grade is claculated) The statement is same for reading score, which means only Thomas High School nine-grade performances of math and reading as NAN.


##### Scores by school spending

Replacing ninth_grade was only affacted on the spending range of per students on the range where Thomas high school involved.

![Alt text](old_spending_summary.png)
![Alt text](new_spending_rage.png)

##### Scores by school size

Replacing ninth_grade was only affacted on the school_size where Thomas high school involved.Over all passing dropped from 90% to 85% in new data analysis.
![Alt text](new_school_size.png)

#### Scores by school type

Replacing ninth_grade was only affacted on the school_type where Thomas high school involved.Over all passing dropped from 90% to 87% in new data analysis.

## Summary

After replacing math and reading scores from ninth_grade students in Thomas High School, the average math and reading scores did not change signficnatly; however, overall passing, passing  math and reading percentages dramatically changed in Thomas high school and over all results as well, where Thomas High School was involved. School spending, school type and school size had been changed where Thomas High Data was considered. As usual, the medium or small school sizes are related to higher overall passing, and interestingly, the school spending  is not positively related to overall passing in which less spending ranges seemed to have higher overall passing. 


```python

```
