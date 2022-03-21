# School District Analysis

## Overview
In a previous analysis, school performance based on math and reading scores were evaluated for 15 high schools in the school district. However, the school board suspects that the grades for Thomas High School ninth graders were altered, and requested that the analysis be re-run ignoring the grades in question. To accomplish this, math and reading grades for Thomas High School ninth graders were set to NaNs in the data.

The analysis consists of the following:
1. Overall average scores, passing rates, school statistics for the district 
2. Average scores, passing rates, school statistics for each school
3. The top 5 and bottom 5 performing schools, based on the overall passing rate
4. The average math score for each grade level from each school
5. The average reading score for each grade level from each school
6. The scores by school spending per student, by school size, and by school type

## Resources
Data Source: 

schools_complete.csv
https://github.com/kristindong/School_District_Analysis/blob/ac6d7f1f7040e63f716088a5d304443bf3a4360f/Resources/schools_complete.csv

students_complete.csv
https://github.com/kristindong/School_District_Analysis/blob/ac6d7f1f7040e63f716088a5d304443bf3a4360f/Resources/students_complete.csv



## Results
Replacing the Thomas High School 9th grade scores had the following impacts:

* District summary - average scores and passing rates all decreased compared to the original analysis

  Before change:
  
  ![District_Summary_old](District_Summary_old.png)
  
  After change:
  
  ![District_Summary_new](District_Summary_new.png)
  
  
* School summary - Thomas High School's average reading score increased while math sccoe and all passing rates decreased

  Before change:
  
  ![THS_old](THS_old.png)
  
  After change:
  
  ![THS_new](THS_new.png)
  
* School ranking - the change did not impact Thomas High School's ranking. It's still ranked 2nd based on overall passing percentage.


* Math and reading scores by grade - the change set Thomas High School's 9th grade scores to NaN. It did not impact the School's average math and reading     scores for 10th, 11th, and 12th grades.

After change 
  ![ByGrade_reading_new](ByGrade_reading_new.png)

* Scores by school spending

* Scores by school size

* Scores by school type


A sample of the script and results displayed in Visual Studio Code:

![VSCode_screenshot](VSCode_screenshot.png)

The text file containing the audit results is saved here:
https://github.com/kristindong/Election_Analysis/blob/50a03a50484d6af8364f489912598d382ab73a71/analysis/election_analysis.txt


## Summary
With some modifications, the Python script used for this election audit can be used for any election, provided that the data is stored in csv format and contain county and candidate name for each vote cast. 

1. The name and path of the election results csv file and election analysis text file may need to be modified if the file name and location are not the same as those used in the code.

![Code_Modification_1](Code_Modification_1.png)


2. If county and candidate name are not in columns 2 and 3, respectively, the the index values in the code below will need to be adjusted to reflect the columns they are stored in the data file. 

![Code_Modification_2](Code_Modification_2.png)
