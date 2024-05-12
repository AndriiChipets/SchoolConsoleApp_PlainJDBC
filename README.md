Application that inserts/updates/deletes data in the database using JDBC.
PostgreSQL DB is used.

Tables:
groups(
	group_id int,
	group_name string
)

students(
	student_id int,
	group_id int,
	first_name string,
	last_name string
)

courses(
	course_id int,
	course_name string,
	course_description string
)

1 Created SQL files with data:
* created a user and database. Assign all privileges on the database to the user. (DB and the user created before application runs)
* created a file with tables creation

2 Created a java application
a. On startup, it runs SQL script with table creation from previously created files. If tables already exist - they are droped.
b. Generated the test data:
* 10 groups with randomly generated names. The name contains 2 characters, hyphen, 2 numbers
* Created 10 courses (math, biology, etc)
* 200 students. Took 20 first names and 20 last names and randomly combined them to generate students.
* Randomly assigned students to groups. Each group contains from 10 to 30 students. It is possible that some groups will be without students or students without groups
* Created the MANY-TO-MANY relation between STUDENTS and COURSES tables. Randomly assigned from 1 to 3 courses for each student

3 Wrote SQL Queries, it is available from the console menu:
* Find all groups with less or equal students’ number
* Find all students related to the course with the given name
* Add a new student
* Delete a student by the STUDENT_ID
* Add a student to the course (from a list)
* Remove the student from one of their courses.

Result:
![image](https://github.com/AndriiChipets/SchoolConsoleApp/assets/137887124/7dee57c1-2e96-46aa-9ead-9bff88634613)
![image](https://github.com/AndriiChipets/SchoolConsoleApp/assets/137887124/67f78f45-d0da-4957-96f3-94565b5bf970)
![image](https://github.com/AndriiChipets/SchoolConsoleApp/assets/137887124/0c05e0eb-94e7-4aa6-bd60-b92902e4679c)
![image](https://github.com/AndriiChipets/SchoolConsoleApp/assets/137887124/fa268ae5-5359-4cb3-a7e1-01b4ad53e6a6)
![image](https://github.com/AndriiChipets/SchoolConsoleApp/assets/137887124/a58468ad-1c28-4133-9ab4-2af645431eff)
