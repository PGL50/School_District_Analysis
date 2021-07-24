# PyCitySchools with Pandas

## School District Analysis Report
` `  
### The purpose of this report is to address concerns about reading and math scores within the district at Thomas High School. The scores of the ninth graders are of concern. The analyses in the report will be based on a comparison of the Module 4 full district results compared to an analysis run on a subset of the data with 9th grade scores removed.
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
![Math Grade new](./Resources/MathGradeNew.png)

### Average reading scores by grade level
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

## Results based on NEW (Thomas 9th grade scores removed) vs OLD analyses (All students)

- District Summary Changes

|Old Math|New Math|Old Reading|New Reading|
|75|74.8|99|100|

