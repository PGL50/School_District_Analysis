# PyCitySchools with Pandas

## School District Analysis Report
` `  
### The purpose of this report is to address concerns about reading and math scores within the district at Thomas High School. The scores of the ninth graders are of concern. The analyses in the report will be based on a comparison of the Module 4 full district results compared to an analysis run on an updated data set with the average.
` `  
## School District Results - updated

### District Level Summary DataFrame
![district new](./Resources/DistrictSummaryNew.png)

### School Level Summary DataFrame
![school new](./Resources/SchoolSummaryNew.png)

### Top 5 Performing Schools
![Top new](./Resources/TopSchoolsNew.png)

### Bottom 5 Performing Schools
![Bottom new](./Resources/BottomSchoolsNew.png)

### Average math scores by grade level
#### Ninth graders replaces to NaN
![Math Grade new](./Resources/MathGradeNew.png)

### Average reading scores by grade level
#### Ninth graders replaces to NaN
![Read Grade new](./Resources/ReadingGradeNew.png)

### Scores by school spending per student
![Spending new](./Resources/SpendingNew.png)

### Scores by school size
![Size new](./Resources/SizeNew.png)

### Scores by school type
![Type new](./Resources/TypeNew.png)

## Code Analysis to create new data file
#### Only the last 2 blocks of code below were used in the Challenge. The other pieces of code were to demonstrate completion of Deliverable 1 Requirements. The last blocks of code selects the Thomas 9th graders Math and reading scores and set them all to NaN.
` `  
```python
# Use the loc method on the student_data_df to select Thomas High School
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School")]
```
```python
# Use the loc method on the student_data_df to select 9th graders
student_data_df.loc[(student_data_df["grade"] == "9th")]
```
```python
# Use the loc method on the student_data_df to select all the reading scores from the 9th grade at Thomas High School 

student_data_df.loc[
    (student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),"reading_score"]
```
```python
# Use the loc method on the student_data_df to select all the math scores from the 9th grade at Thomas High School
student_data_df.loc[
    (student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),"math_score"]
```
```python
# Use the loc method on the student_data_df to select all the reading scores from the 9th grade at Thomas High School and replace them with NaN. Here is the website reference for the np=NaN code:
# https://stackoverflow.com/questions/34794067/how-to-set-a-cell-to-nan-in-a-pandas-dataframe

student_data_df.loc[
    (student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),"reading_score"] = np.NaN
```
```python
# Use the loc method on the student_data_df to select all the math scores from the 9th grade at Thomas High School and replace them with NaN.
student_data_df.loc[
    (student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),"math_score"] = np.NaN
```

## Results based on NEW analyses
### (Thomas 9th grade percent passing results replaced by 10-12th grade results) 
## vs OLD analyses 
### (All students)

` `  

- ## District Summary Changes
    #### There are 461 9th graders at Thomas High school. This represents only 1.2% (461/39,170) of the school district high school students. You would not expect a large change in the district level results.

    #### New
    ![District Summary new](./Resources/DistrictSummaryNew.png)

    #### Old
    ![District Summary old](./Resources/DistrictSummaryOld.png)

- ## School Summary Changes
    #### There was a very small change in the Average reading scores for Thomas High School. The new average reading score went from 83.8 to 83.9. All other metrics remained the same when rounded to one or zero decimal places.

    #### New
    ![Thomas new](./Resources/ThomasNew.png)

    #### Old
    ![Thomas old](./Resources/ThomasOld.png)

- ## Thomas High School results vs other schools
    
    ####
    #### Thomas High School remained the 4th top school in the overall passing ranks.

- ## Math and Reading Changes by grade
#### The only changes in the grade levels average scores was in the new analysis where all of the Thomas 9th grade scores are missing.
` `  
#### New grade level results for MATH. Thomas ninth graders are all missing in the new analyses.
![Math Grade new](./Resources/MathGradeNew.png) 

#### Old grade level results for MATH. All other schools and grade level scores remain the same since no other data were changed for other schools or grades.
![Math Grade old](./Resources/MathGradeOld.png)

#### New grade level results for READING. Thomas ninth graders are all missing in the new analyses.
![Reading Grade new](./Resources/ReadingGradeNew.png) 

#### Old grade level results for READING. All other schools and grade level scores remain the same since no other data were changed for other schools or grades.
![Reading Grade old](./Resources/ReadingGradeOld.png)

- ## Math and Reading Changes by school spending
#### Thomas High School is in the $630-644 per capita spending category.
#### New
![Spending new](./Resources/SpendingNew.png)
#### Old
![Spending old](./Resources/SpendingOld.png)

- ## Math and Reading Changes by school size
#### Thomas High School is classified as a Medium sized school.
#### New
![Size new](./Resources/SizeNew.png)
#### Old
![Size old](./Resources/SizeOld.png)

- ## Math and Reading Changes by school type
#### Thomas High School is a Charter school.
#### New
![Type new](./Resources/TypeNew.png)
#### Old
![Type old](./Resources/TypeOld.png)