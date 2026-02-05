# MIS-311
## Data Analysis and Insight
### 1.Data Overview
<img width="361" height="528" alt="image" src="https://github.com/user-attachments/assets/0e15b5fb-e498-45c6-aabf-fb2191ee62fe" />

The ***Student Performance*** dataset provides detailed information on students’ demographic backgrounds and their academic achievements across three subjects: math, reading, and writing. It contains **202 rows** and **8 columns**, where each row represents an individual student.

**Data Column Descriptions**
* race_ethnicity  (object): Different racial groups  
* parental_level_of_education (object): The educational background of the student's family  
* math_score (float): Performance in math  
* reading_score (float): Performance in reading  
* writing_score (float): Performance in writing skills
* total_score (float): The sum of math, reading, and writing scores
* average_score (float): The mean of the three subject scores

The dataset is designed to explore how factors such as gender, race ethnicity, and parental education influence student performance. It serves as a representative sample for analyzing educational outcomes and evaluating factors affecting student success.

### 2.Data cleaning
<img width="575" height="341" alt="image" src="https://github.com/user-attachments/assets/942bba49-2474-4d67-ad4d-ab39c00037fe" />

The ***parental_level_of_education*** column has **3** missing values.  
The ***average_score*** column has **4** missing values.  
The remaining columns has no missing values.

The ***parental_level_of_education*** column I will fill "**not updated**" in the missing blank by using `fillna()` funtion.   

The ***average_score*** column is missing some spaces so I will calculate and fill in the blanks using the `fillna()` function

<img width="918" height="136" alt="image" src="https://github.com/user-attachments/assets/cf2252bd-dbed-4ddf-ab8c-eccb47930bdb" />

We will re-check with `info()` function.


<img width="638" height="341" alt="image" src="https://github.com/user-attachments/assets/52a7edcc-5f31-4dd6-a4c4-d1adae29a70c" />

Missing values are solved, all columns have 202 rows

We use `.duplicated()` to identify duplicate rows and `.drop_duplicates()` to remove them if any exist.

<img width="1021" height="760" alt="image" src="https://github.com/user-attachments/assets/ec3e0880-576a-43e8-b62a-33a211c90911" />

Following the data cleaning process, the dataset consists of 199 rows and 8 columns after removing three duplicate records, ensuring greater accuracy for subsequent descriptive and analytical procedures.

### 3.Descriptive Statistics

We can quickly do *the descriptive statistic* by using `describe()` fuction.

<img width="1241" height="485" alt="image" src="https://github.com/user-attachments/assets/1df6c6bc-7460-45c2-9099-3e90ad1409d4" />

This table shows descriptive statistics for students' scores in math, reading, writing, total score, and average score. On average, students scored between 64 and 67 points in each subject. Students score around 64.22 in math, 67.63 in reading, and 66.37 in writing, showing slightly stronger performance in reading. The minimum score is quite low, while the maximum score is 100, indicating a wide range of scores. The standard deviation (about 15-16) shows some variation in performance among students. Overall, the data shows average performance with some individual variation in achievement levels.

**_Insight 1_**

<img width="1185" height="527" alt="image" src="https://github.com/user-attachments/assets/e3c60e67-913a-41a1-bca4-356d09d4fce7" />
<img width="1039" height="604" alt="image" src="https://github.com/user-attachments/assets/9335708a-4e5c-4629-8c67-2870804d5327" />


The results showed that students whose parents had higher levels of education, such as bachelor’s or master’s degrees, tended to have higher average scores than other students. This suggests that parental education has a significant impact on children’s academic achievement. Understanding this can help schools and families provide appropriate support to help students from different backgrounds perform better in their studies.

**_Insight 2_**

<img width="968" height="400" alt="image" src="https://github.com/user-attachments/assets/df9ff7e9-2236-4530-b7e1-e5253ee837bb" />
<img width="1001" height="612" alt="image" src="https://github.com/user-attachments/assets/a8840f34-fb9b-4050-a03b-4edc422f29f7" />

The table shows that average scores vary across different race ethnicity groups. Group A has the lowest average score at 58.11, while Group E has the highest at 70.27. There is a clear upward trend from Group A to Group E, indicating that race ethnicity may be associated with differences in academic performance.

**_Insight 3_**

<img width="1337" height="347" alt="image" src="https://github.com/user-attachments/assets/e09abc78-16d4-4f2e-8778-a87688edd656" />
<img width="861" height="689" alt="image" src="https://github.com/user-attachments/assets/d761f003-794a-461d-a411-3d149ec0f461" />

The data show that there is a difference in average scores between the two genders. The group with gender =0 (probably female) scored significantly higher in writing and reading, while the group with gender 1 (probably male) scored slightly higher in math. This suggests that female students tend to be stronger in language subjects, while male students are stronger in math. Overall, this difference reflects the gender differences in subject-specific learning.

## Conclusion

In summary, the results of the analysis show that many personal and social factors influence students' academic achievement. Parental level of education, gender, and race ethnicity groups are all associated with different mean scores across groups. Specifically, students with more educated parents tend to score higher, girls are stronger in language while boys are stronger in mathematics, and mean scores tend to increase across race ethnicity groups from A to E. These insights highlight the importance of providing appropriate academic support policies to reduce the learning gap between different groups of students
