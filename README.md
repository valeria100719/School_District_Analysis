# School_District_Analysis

The school board has notice that there was evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold the standards of state testing and have turned to you for help. Sh
After assessing the situation with the school superintendent and Maria, you decide the best approach is to:

- Replace the ninth-grade math and reading scores from Thomas High School.
- Keep all other data associated with the ninth-grade students and Thomas High School intact.


##Methods
Using the Pandas method with conditional statements and comparison and logical operators, 
we change all  the ninth-grade reading and math scores for Thomas High School with Nan value. 
In this way we tried to clean the data and have a better understand if the dishonesty will effect the total math and reading score.

Here the results:

BEFORE DATA CLEANUP

Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
79.0, 81.9, 75, 86, 65

AFTER DATA CLEANUP

Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
78.9, 81.9, 74, 85, 64

As we can see there was a light downward change in district averages, so the dishonesty of Thomas High School won't affect too much the final score.

We decide to analysis also if the % of Overall Passing changed or not on the basis of the new analysis, and here the results:

BEFORE CLEANUP: Thomas High School's % Overall Passing = 91, placing second

AFTER CLEANUP: % Overall Passing = 65, placing eighth!

As we can see the Overall ranking order change due to Thomas High School,this school go down of almost 11 position, with the other intervening schools moving up.


Recalculate the high- and low-performing schools.


How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?


OBSERVATION: Relative ranking for THOMAS HS changed from 2ND to 8TH, as it's % OVERALL PASSING number decreased from 91% to 65%.




Recalculate the scores by grade, scores by school spending, scores by school size, and scores by school type.


How does replacing the ninth-grade scores affect the following?


Math and Reading Scores by Grade

Thomas HS 9th grade math & reading scores set to "nan" and equivalent to 0
Totals for passing math & reading across grades are reduced as all of 9th grade scores are equivalent to failing
Average scores calculation not significantly affected by removal of 9th grade scores, seems due to count() function NOT including 9th grade scores = nan
Cacluate number of students with a math grade - use "student_school_math.groupby(["school_name"]).count()""
BEFORE cleanup: Thomas High School       1635
AFTER cleanup: Thomas High School       1174
"%age passing" score is reduced as Total number of students (denominator) remains unchanged, but total passing value (numerator) is reduced by the number of removed 9th grade scores.



Scores by School Spending

Thomas HS is in the spending bucket "$630-644"
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644" as follows
BEFORE: 73, 84, 63
AFTER: 67, 77, 56



Scores by School Size

Thomas HS is in the "Medium (1000-2000)" size bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)" as follows
BEFORE:94, 97, 91
AFTER: 88, 91, 85



Scores by School Type

Thomas HS is in the "CHARTER" type bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER" as follows
BEFORE:94, 97, 90
AFTER: 90	93	87
