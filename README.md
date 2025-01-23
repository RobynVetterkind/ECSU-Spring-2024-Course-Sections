# ECSU-Spring-2024-Course-Sections  

Identified slack and shortages in the ECSU Spring 2024 Course Sections database, and provided university insights, value, and recommendations for course improvement by using MS Access SQL query builder in SQL View.  

## Initial Queries  

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

## Then Queried to Find Answers to Questions on What Types of Insights Were Needed  

- **S3Q3Subquery3Final, S3Q3Subquery1..2**: Which subject has the largest percentage of sections taught by Part‐Time instructors?  
- **S3Q4SubqueryFinalOutput, S3Q4Subquery1**: Which subject has the most Unique Full‐Time instructors teaching courses?  
- **S3Q5**: What are the actual Subject Codes that each Instructor marked as teaching “Multi” teaches?  
- **S3Q6FinalOutput & S3Q6Subquery1**: Rank Full‐Time instructors in decreasing order of student credits taught.  
- **S3Q7Subquery1, S3Q7Subquery2, S3Q7Subquery2A, S3Q7Subquery2B, S3Q7Subquery3, S3Q7SubqueryFinalOutput**:  
  Rank the Department/Program Chair, Assistant/Associate Chair, or Program Coordinators by:  
  1. Teaching the most days of the week  
  2. Teaching the most unique courses  
  3. Teaching the most student credits  
  4. Alphabetically.  

  Provide the person’s name, Department, Chair (etc. title), number of days of the week, number of unique courses, and number of student credits taught.  

## Insights for Future Course Setups  

### Query: **S3Q9ProjectSubquery1 and S3Q9ProjectSubquery2**  

- **Query Question/Objective**: Which days and times are courses most run? Ordered by day then time.  
- **Why Query Insightful/Valuable**: Allocation of professors, staff, and faculty effectively. Provides insight for event planning committees at Eastern for which times to avoid setting events due to low student attendance.  
- **Query Finding(s)**:  
  - From **S3Q9ProjectSubquery2**, the most common class day and time was TR at 9:30 am – 10:45 am.  
  - The top three times are TR, midday, or early afternoon.  
  - **S3Q9ProjectSubquery1** counts the days and times, and **S3Q9ProjectSubquery2** sums the days and times.  

### Query: **YS3Q10Subquery1A, YS3Q10Subquery1B, YS3Q10Subquery2…14 and YS3Q10SubqueryFINAL_OUTPUT**  

- **Query Question/Objective**: How many courses sections are available Tuesday and Thursday that are not available on Monday, Wednesday, and Friday?  
- **Why Query Insightful/Valuable**: Identify scheduling patterns and availability of courses. Presents a case of whether students are coerced into taking certain day classes out of no other choice.  
- **Query Finding(s)**:  
  - Queries 1 through 14 identified course sections scheduled for Monday, Wednesday, and Friday and right joined them with Tuesday and Thursday classes, retaining null values.  
  - Comparing the updated Tuesday and Thursday course sections to more MWF variants yielded **283 subject course sections exclusively available on Tuesday and Thursday**.  

### Query: **YS3Q11ProjectSubquery1…3 and YS3Q11ProjectSubquery
