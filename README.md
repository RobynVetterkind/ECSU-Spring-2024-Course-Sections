# ECSU Spring 2024 Course Sections

Background: Took information from tables about instructors, subjects, courses, sections, credits, LACs, times, dates, capacities, actuals, locations, titles, teaching status, departments, and chair coordinators from the Eastern Connecticut State University Spring 2024 course database and performed queries in Microsoft's Access SQL view. 

Objective Achieved: Identified slack and shortages in the ECSU Spring 2024 Course Sections database and provided university insights, value, and recommendations for course improvement by using the MS Access SQL View using the following SQL clauses: 

<pre> 
SELECT 
FROM 
WHERE 
GROUP BY 
HAVING 
ORDER BY 
</pre>

Started off by doing simple queries to find basic information on the tables. These can be found from the following queries in the Access file in SQL View:

- **Average_Section_Size**  
- **Section_Count**  
- **Subject_Count**  
- **Subject_Course_Enrollment**  
- **Subjects_Seats_Filled**  
- **Unique_Courses_In_Subject**  
- **BuildingWithMostSections & BuildingWithMostSectionsSubquery1**  
- **Enter_Room_for_Courses**  
- **Number_Of_Students_Per_Professor**  
- **NumberOfStudentSeatsEachInstructorIsTeaching**  
- **NumberOfUniqueCoursesPerInstructor**  
- **Professor_Number_Days_Week_Teaching**  
- **ProfessorTeachingInformation & ProfessorTeachingInformationSubquery1...3** 


Then Queried to find Answers to Questions on what types of insights were needed: 

### 🔍 S3Q3Subquery3Final, S3Q3Subquery1..2: 
❓ Which subject has the largest percentage of sections taught by Part-Time instructors?

### 🔍 S3Q4SubqueryFinalOutput, S3Q4Subquery1: 
❓ Which subject has the most Unique Full‐Time instructors teaching courses?

### 🔍 S3Q5: 
❓ What are the actual Subject Codes that each Instructor marked as teaching “Multi” teaches?

### 🔍 S3Q6FinalOutput & S3Q6Subquery1: 
Rank Full‐Time instructors in decreasing order of student credits taught.

### 🔍 S3Q7Subquery1, S3Q7Subquery2, S3Q7Subquery2A, S3Q7Subquery2B, S3Q7Subquery3, S3Q7SubqueryFinalOutput: 
Rank the Department/Program Chair, Assistant/Associate Chair, or
Program Coordinators by first: teaching the most days of the week, second:
teaching the most unique courses, and third: teaching the most student credits,
and lastly alphabetically.  Provide the person’s name, Department, Chair (etc.
title), number of days of the week, number of unique courses, and number of
student credits taught.



Lastly, I queried to find insights that could be useful for future course setups: 

### 🔍 S3Q9ProjectSubquery1 and S3Q9ProjectSubquery2:

❓ Query Question/Objective: Which days and times are courses most run? Ordered by day then 
time. 

🧠 Why Query Insightful/Valuable: Allocation of professors, staff, and faculty effectively. Provides 
insight for event planning committees at Eastern for which times to avoid setting events due to low 
student attendance. 

🔗 Query Finding(s): From S3Q9ProjectSubquery2 the most common class day and time was TR at 
9:30 am – 10:45 am. The top three times are TR, midday or early afternoon. S3Q9ProjectSubquery1
counts the days and times and S3Q9ProjectSubquery2 sums the days and times.


### 🔍 YS3Q10Subquery1A, YS3Q10Subquery1B, YS3Q10Subquery2…14 and YS3Q10SubqueryFINAL_OUTPUT: 

❓ Query Question/Objective: How many courses sections are available Tuesday and Thursday that 
are not available on Monday, Wednesday, and Friday? 

🧠 Why Query Insightful/Valuable: Identify scheduling patterns and availability of courses. Presents 
a case of whether students are coerced into taking certain day classes out of no other choice. 

🔗 Query Finding(s): Queries 1 through 14 identified course sections scheduled for all combinations of Monday, 
Wednesday, and Friday and right joined them with all combinations of Tuesday and Thursday classes, retaining null 
values. Comparing the updated Tuesday and Thursday course sections to more MWF variants 
yielded 283 subject course sections exclusively available on Tuesday and Thursday. 


### 🔍 YS3Q11ProjectSubquery1…3 and YS3Q11ProjectSubqueryFinal:

❓ Query Question/Objective: Which instructors have the most seats available? 

🧠 Why Query Insightful/Valuable: Insights into student preferences and perceptions of teaching 
quality. Identify professors with consistently large number of available seats. 

🔗 Query Finding(s): The initial query sorted instructors based on courses neither high-level nor low-level 
due to low enrollment. Then, further queries collected capacity and actual enrollment, 
summed them up. The last query subtracted actual enrollment from capacity, showing that 
Johnson, P (P) has 59 vacant seats, with the top three professors each having over 50 available 
seats.


### 🔍 YS3Q12ProjectSubquery1…2 and YS3Q12ProjectSubquery3FinalOutputPart1...Part3:

❓ Query Question/Objective: Which subject courses, having only one section, have the most 
shortages of sections based on their actual minus capacity?

🧠 Why Query Insightful/Valuable: Planning for future semesters. Addressing shortages can 
enhance student satisfaction, improve retention rates, and contribute to the overall effectiveness 
of the educational experience.

🔗 Query Finding(s): The initial queries determine the capacity and actual enrollment for each subject 
course section and the final output queries count, sum then exclude courses that have more than 
one section. CED 300 exhibits the highest shortage, with its one section exceeding capacity by 9
students, while BIS 373 follows with exceeding capacity of 8 students in its one section.


### 🔍 YS3Q13_A_BISAndCSC, YS3Q13_B_Labs, YS3Q13_C_Times4pmThrough7PM, and YS3Q13_D_LabOccupancy:

❓ Query Question/Objective: Identify which rooms are computer labs and find out what percentage 
of the programs courses and labs are offered between 4 and 7pm.

🧠 Why Query Insightful/Valuable: Gauge computer lab availability and demand and reveal 
percentage of courses between 4 and 7 pm for professor and student preferences.

🔗 Query Finding(s): Query A identified specific locations for subject codes such as BIS, Data Science
and Computer Science. Query B identifies all the labs available on campus. Query D identifies all 
lab times outside of the specified time frame. Query C was used to find labs available between 4 
and 7 pm, revealing that 24.18% of the total 91 computer lab time slots are used by courses 
between 4 and 7 pm.




