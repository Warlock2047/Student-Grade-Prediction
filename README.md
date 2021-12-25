# Student Grade Prediction
## Information About the Data Set
It describes the success of secondary school students in two Portuguese schools. Data properties; student grades include demographic, social, and school-related characteristics. Data were collected using school reports and questionnaires.
Mathematics (mat) and Portuguese (por).
important note: The G3 target attribute is strongly correlated with the G2 and G1 attributes. This is because G3 corresponds to the final year grade (given in the 3rd semester), while G1 and G2 correspond to the 1st and 2nd semester grades. Without G2 and G1, G3 is harder to predict.

FEATURE INFORMATION
1. School: schools attended by students ( 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
2. Sex : gender of students (M: Male, F: Female)
3. Age: the age of the students (There are numbers from 15 to 22.)
4. Address: students' addresses (U: urban , R: rural)
5. Famsize : family size (“LE3” equal to or less than 3, “GT3”: greater than three)
6. Pstatus: families living together (“T”: living together “A”: living separately)
7. Medu: Mother's education status (numeric: 0 - none, 1 - primary school (4th grade), 2 - from 5th to 9th grade
up to 3 - high school , or 4 - college)
8. Fedu: Father's education status (numeric: 0 - none, 1 - primary school (4th grade), 2 - from 5th to 9th grade
up to 3 - high school , or 4 - college)
9. Mjob: Mother's occupation (nominal)
10. Fjob: Father's occupation (nominal)
11. Reason: The reason for choosing the school
12. Guardian : Student's guardian
13. traveltime – time from home to school (numeric: 1 - < 15 minutes., 2 - 15 to 30 minutes., 3 – 30
minutes minimum. 1 hour, or 4 - >1 hour)
14. studytime – Weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10
hours, or 4 - > 10 hours)
15. faliures: the number of students left in the class.
16. Schoolsup: student scholarship.
17. Famsup: family education support.
18. Paid: extra paid lessons within the course subject.
19. Activities : out-of-school activities
20. Nursery: the status of attending kindergarten
21. Higher: the state of wanting to get higher education
22. Internet: whether there is internet at home or not.
23. Romantic: Whether or not you are in a romantic relationship
24. famrel: quality of family relationship (numeric: 1 - very bad; 5 - 1 to 5 as very good
numbering)
25. freetime : After school free time (numeric: 1 - very low; 5 - very high from 1 to 5
numbering)
26. goout: Go out with friends (numeric: 1 - very low; 5 - very high 1 to 5
numbering)
27. Dalc: weekday alcohol consumption (numeric: 1 - very low; 5 - very high, numbered 1 to 5)
28. Walc: weekend alcohol consumption (numeric: 1 - very low; 5 - very high, numbered 1 to 5)
29. Health: current health status (numeric: 1 - very bad; 5 - very good, numbered 1 to 5)
30. Absences: Number of absences from school (0. to 93.)

## Mathematics and Portuguese language grades
1. G1 – first semester grade (numeric: 0 to 20)
2. G2 - second semester grade (numeric: 0 to 20)
3. G3 - final grade (numeric:0 to 20, output target.)

# REPORT
1. It is a data set that contains the exam grades and Final grades of the students of two secondary schools in Portugal, together with their own and family information.
2. While analyzing our data, graphics such as boxplot, boxplot, scatter plot, kde plot, hist plot were used.
3. When the heatmap is examined, it is observed that G1, G2 and G3 (Final Grades) are highly correlated. Likewise, it is observed that there is a positive and high correlation between Medu (Mother Education Level) and Fedu (Father Education Level).
4. The education levels of the parents were examined. The education levels are between 1 and 4, and under these conditions, it is determined that the fathers are mostly Level 2 with the education level and the mothers are Level 4 with the majority of the education levels. It has been observed that there are very few students with the lowest (0) education level in common as mothers and fathers.
5. Examining the occupational distribution of the students' mothers and fathers, it was determined that the mothers and fathers were members of the "other" category in the selected scales. However, it has been observed that mothers and fathers are mostly in the "service" category and the least in the "health" category, after the "other" category, among the determined professions.
6. When the reasons for students to choose schools are examined, it is thought that those who prefer Gabriel Pereira and Mousinho da Silveira schools are mostly chosen because they are better in terms of "course".
7. When the relationship between age and gender was examined with the density graph, it was observed that the ages of the selected students were generally distributed between the ages of 14 and 20.
8. Looking at the distribution chart, it is observed that the average of the 3 exam grades is separated by gender. When looked at, it was determined that the distribution of men was higher than that of women in terms of grade point average.

* MODELLING

The data set was first separated as dependent and independent variables, and then dummies were applied to the independent variables. Afterwards, it was divided into train and test set, and standardization was done for x_train and x_test and made suitable for the model.
In addition, GridSearchCV was used in order to reach the maximum values in the models and the parameters were adjusted manually in all models.
The measurement values of the models are given in the table. It was determined that the best predictor (successful model) for the data set used was Random Forest Regression.

