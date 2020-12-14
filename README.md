# School District Analysis

## Overview
We are tasked with analyzing the standardized test scores of a city school district. In order to perform this school district analysis we will create a high-level snapshot of the districts key metrics and an overview of these key metrics broken down by school.
We will then break things down further by creating the following tables:
* Top 5 and bottom 5 performing schools based on the overall passing rate
* The average math score received by students in each grade level at each school
* The average reading score received by students in each grade level at each school
* School performance based on the budget per student
* School performance based on the school size 
* School performance based on the type of school

Due to the School Board's concerns of academic dishonesty, Thomas High School's ninth grade results are in question. We will exclude Thomas High School ninth grade results in English and Math, while leaving all other data intact. After replacing these scores with NaN's we will repeat our school district analysis and look for any changes.


## Resources
Jupyter Notebook,  Anaconda 4.8.3

Data: [school_complete.csv](Resources/schools_complete.csv) &
[students_complete.csv](Resources/students_complete.csv)
## Results
[Challenge code ](PyCitySchools_Challenge.ipynb)

### District Overview 
Combining the data from the schools_complete.csv and students_complete.csv allows us to get an overview of the district.

Original district summary:
![District Sumary](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/Distict_Summary.png)

District summary with the Thomas High School's ninth grade results set as NaN:
![Altered District Summary](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/District_Summary_Altered.png)

Comparing the metrics on the two tables we can observe.

* "Average Math Score" has decreased by 0.1
* "% Passing Math",  has decreased by 0.1
* "% Passing Reading" has decreased by 0.1
* "% Overall Passing" has decreased by 0.1
* "Average Reading Score" remains unchanged
* "Total Students" remains the same as only the scores of the Thomas High 9th grade are removed, not the students completely.  
* "Total Budget" is unaffected.    
### Per School Summary

We broke the data down further to allow us to view it by school.


Original per school summary:

![Per School Summary](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/Per_school_summary.png)

Per school summary with Thomas High ninth grade results set to NaN:

![Altered Per School Summary](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/Per_school_summary_altered.png)
Comparing these charts we can see small differences in Thomas High School:
* Decrease in "Average Math Score" less 0.1
* Decrease in "% Passing Math" less than 0.1
* Decrease in "% Overall Passing" 0.3
* Decrease in "% Passing Reading" 0.3
* Slight increase "Average Reading Score" 0.05 
            

### Schools Ranked by Performance 
Looking at the highest and lowest performing schools we can see that Thomas High is the second highest performing school.

Top 5 schools.
![Top five schools](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/top_schools.png)
Top 5 schools with THS ninth grade scores removed.
![Altered Top Five Schools](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/top_schools_altered.png)

* Although Thomas High's "% Overall Passing" has decreased by 0.3 it still remains the second highest ranked school.

### Math and reading scores by grade 


We further broke down the test scores by grade level.

Math score by grade:

![Math Scores by grade](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/math_scores_by_grade.png)

* Looking at the Math scores we can see that Thomas High's ninth grade were the schools highest performers but only by 0.1%.

![Altered Math Scores by grade](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/math_scores_by_grade_altered.png)

Reading score by grade:

![Reading Score by grade](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/reading_scores_by_grade.png)

* Looking at the reading scores we can see that Thomas High's ninth grade was not scoring as high as it's tenth or telfth grade.

![Altered Reading Score by grade](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/reading_scores_by_grade_altered.png) 
* The adjusted tables show NaN in place of Thomas High ninth grade.

### Scores by school spending

The data also allowed us to look at schools budgets, and calculate a per student spending. We then split the schools into spending bins to compare spending and results.

![Results by spending](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/spending_summary.png)
* We can see an inverse relationsip between district spending and "% Overall Passing". The schools spending least being most sucessful.

![Altered results by spending](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/spending_summary_altered.png)
* Removing Thomas High's ninth grade has not had a noticable effect on these tables.

### Scores by school size
The data also allowed us to create bins that grouped schools by size and compare results.

![Results by size](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/size_summary.png)
* Smaller and Medium schools have a much higher % Overall Passing than large schools.
* Large schools fare worse in all categories. 
* Difference is more pronounced in Math than reading.
* Smaller and Medium schools have a much higher % Overall Passing than large schools.

![Altered Results by size](https://github.com/RussellShelley/Imagefiles/blob/main/size_summary_altered.png?raw=true)
* Removing the Thomas High ninth grade results did not change anything.


### Scores by type
The district has both charter and district schools. We compared the results by type.
![Results by school type](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/type_summary.png)
* Charter beats out district in all metrics. 
* Much more Sucessful in "% Overall passing" (90% v 54 %) 

![Altered results by type](https://raw.githubusercontent.com/RussellShelley/Imagefiles/main/type_summary_altered.png)

* Thomas High ninth grade results did not change this table.


## Summary
In summary after replacing Thomas High Schools ninth grade scores with NaNs. We can see the following. 
   *  Per the Distrct Summary. We can see that the overall district's scores suffered without the ninth graders from the high performing Thomas High School. "Average Math Score", "% Passing Math", "% Passing Reading" and "% Overall Passing" have all decreased by 0.1%.
   * Per the school summary we can see that without the ninth grade Thomas High School "% overall passing" fell by 0.3. 
   * Although Thomas High's "% Overall Passing" has decreased by 0.3 it still remains the second highest ranked school.
   * Looking at the breakdown by grade, we can see that Thomas High's ninth grader have high scores in math. They were the schools highest performers, but only by 0.1%. In Reading they are third out of the four grades. 
