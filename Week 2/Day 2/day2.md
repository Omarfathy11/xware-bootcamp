# This is Transaction Exercise
* question and answer
Create a new transaction then:
Insert a new record into the Professor table
Insert a new record into the Student table
Select all the Professors and students
Open another session and select all the Professors and students. What is the difference?
Return to the first session and delete the Professors with the salary greater than 20000
Open another session and select all the Professors and students. What is the difference?
Return to the first session and rollback the transaction
Open another session and select all the Professors and students. What is the difference?
Return to the first session Start a new transaction
Insert a new record into the Professor table
Insert a new record into the Student table
Commit the transaction
Open another session and select all the Professors and students. What is the difference?
Return to the first session start a new transaction
Insert a new record into the Professor table with a duplicated id. What happens?
Try to insert a new record into the Student table with a duplicated id. What happens?
Try to commit the transaction. What happens?
Try to rollback the transaction. What happens?
# This is Join Exercise
Using College Management System Database With Joins
Select Subject id, Subject Name, Subject Code, Course Duration in One Query
Select Subject id, Subject Name, Subject Code, Course Duration, Professor First_name, Professor Last_name, in One Query
Select All Students With Thier Address In one Query
Select All Student Name In Every Couse.


Create a new transaction
* begin;
* Insert a new record into th*e Professor table
* insert into professor (id,department_id,faculty_id,f_name,l_name,salary,age) values (1,1,1,'fathy','ahmed',2193,40);
* Insert a new record into the Student table
* insert into student (id,f_name,l_name,f_phone,birth_date,age) values (1,'omar','fathi',01111442600,'23-43-2123','23');
* Select all the Professors and students
* select * from student;
* select * from professor;
* Open another session and select all the Professors and students
* What is the difference? 
* 1 - ctrl + shift + t 
* 2 -  to enter DB : sudo -u postgres psql
**" the insert is not added yet because the transaction not commited "**
* Return to the first session and delete the Professors with the salary greater than 20000
* delete from professor where salary > 20000
* Open another session and select all the Professors and students. What is the difference?
**"the professor isn't deleted because the delete is not done yet because the transaction not commited"**
* Return to the first session and rollback the transaction
* ROLLBACK;
* Open another session and select all the Professors and students. What is the difference?
**"the professor and students is same ,(no insert and delete is done) because we commit the transaction.**
* Return to the first session Start a new transaction
* begin;
* Insert a new record into the Professor table
* insert into professor (id,department_id,faculty_id,f_name,l_name,salary,age) values (2,2,2,'ali','ahmed',4000,50);
* Insert a new record into the Student table
* insert into student (id,f_name,l_name,f_phone,birth_date,age) values (2,'omar','mohmmed',01111442600,'10/3/2022','23');
* Commit the transaction
* commit
* Open another session and select all the Professors and students. What is the difference?
* "the insert is  added  because the transaction is commited"
* start a new transaction
  * begin; 
* Insert  new record into the Professor table with a duplicated id. What happens?
 * ERROR:  duplicate key value violates unique constraint "department_pkey"
* Try to insert a new record into the Student table with a duplicated id. What happens?
* ERROR:  duplicate key value violates unique constraint "student_pkey"
* Try to commit the transaction. What happens?
* ROLLBACK -- > reason : the insert is not done (because we Insert the record with a duplicated id.)
* Try to rollback the transaction. What happens?
* there is no transaction is running and output :
* WARNING:  there is no transaction in progress
* ROLLBACK
* Try to insert a new record into the Student table with a duplicated id. What happens?
* ERROR:  duplicate key value violates unique constraint "student_pkey"


This is Join Exercise

* Using College Management System Database With Joins
* Select Subject id, Subject Name, Subject Code, Course Duration in One Query
* code
* select subject.id,subject.name,subject.code,course.duration 
* from subject
* inner join course 
* on subject.code = course.subject_code;

* Select Subject id, Subject Name, Subject Code, Course Duration, Professor First_name, Professor Last_name, in One Query
* code
* select subject.id,subject.name,subject.code,course.duration,professor.name
* from course 
* inner join subject 
* on course.sub_code = subject.sub_code
* inner join professor
* on course.p_id = professor.p_id;

* Select All Students With Thier Address In one Query
* code
* select student.id,student.f_name,student.l_name,student.f_phone,student.birth_date,student.age,Address.line1
* from student_Address
* inner join student 
* on student_Address.student_id = student.id
* inner join Address 
* on student_Address.address_id= address.id;

* Select All Student Name In Every Couse.
* code
* select student.name
* from student 
* inner join course_Enrollment
* on student.id = course_Enrollment.student_id;
