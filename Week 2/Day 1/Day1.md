### day 1
## Exercise - 3
* Create ER diagram For The College Management System With following Tables
    * `Faculty` Table With These attributes:
     * `F_id:` Faculty id
     * `F_name:` Faculty Name
    * `Department` Table With These attributes:
     * `D_id:` id
     * `D_Name` Name
     * `F_id` Faculty id
    * `Address` Table With These attributes
     * `A_id` Address id
     * `Gvernorate` Gvernorate
     * `City` City
     * `line_1` Address Line 1 (Required)
     * `line_2` Address Line 2 (Optional)
    * `Student_Address` Table With These attributes
     * `Stu_A_id` id
     * `A_id` Address id
     * `Stu_id` Student id
    * `Student` Table With These attributes
     * `Stu_id` id
     * `F_Name` First Name
     * `L_Name` Last Name
     * `F_Phone` First Phone
     * `L_Phone` Last Phone
     * `Birth_Date` Birth Date
     * `image` Student Image
    * `Professor` Table With These attributes
     * `P_id` id
     * `F_id` Faculty id
     * `D_id` Department id
     * `F_name` First Name
     * `L_Name` Last Name
     * `age` Age
     * `Salary` Salary
     * `image` Student Image
    * `Subjects` Table With These attributes
     * `Sub_id` id
     * `Sub_name` Name
     * `Sub_code` Code (Unique)
     * `F_id` Faculty id
    * `Course` Table With These attributes
     * `C_id` id
     * Sub_id Sub_id
     * `Duration` Duration
     * P_id Professor id
    * `Course_Enrolment` Table With These attributes
     * `C_E_id` id
     * `C_id` Course id
     * `Stu_id` Student id
    * `Exams` Table With These attributes
     * `E_id` id
     * `C_id` Course id
     * `Date` Exam Date
     * `Time` Exam Time
     * Duration Exam Duration


## This is  solution ex.1

create table if not exists faculty (
* id  serial primary key,
	* name varchar(40)
	);
	* create table if not exists debartment (
		* id  serial primary key,
		* name varchar(30),
		* f_id int references faculty (id)
		);
	* create table if not exists address (
		* id  serial primary key,
		* city varchar(40),
		* gevenote varchar(30) not null,
		* address_1 text not null,
		* address_2 text
		);
	* create table if not exists student (
		* id  serial primary key,
		* name varchar(40) not null,
	    * birth_date varchar(30),
		* f_phone int not null,
		* f_name int
		);
	* create table if not exists Student_Address (
			* id  serial primary key,
		* Address_id int references address (id),
		* student_id int references student (id)
		 );
	* create table if not exists professor (
	 	* id  serial primary key,
		* name varchar(40) not null,
	   * age int not null,
		* salary real not null,
		* f_name varchar(10) NOT NULL,
		* l_name varchar(10) NOT NULL,
		* faculty_id int references faculty(id),
		* department_id int references debartment(id)
	 );
	 * create table if not exists subject (
	   * id  serial primary key,
		* sub_name varchar(10)not null,
		* sub_code varchar(10)not null,
		* Faculty_id int references Faculty (id)
	 );
	 
		* create table if not exists course (
			* id  serial primary key,
			* Duration varchar(40),
		    * subject_id int references student (id),
			* professor_id int references professor (id)
			);
			* create table if not exists course_Enrolment (
			* id  serial primary key,
			* course_id int references course (id),
			* student_id int references student (id)	
			);
			* create table if not exists exames (
				* id  serial primary key,
				* Duration varchar(40),
				* course_id int references course (id),
				* exam_date varchar (40),
				* exam_time varchar (30)
			);
			
			
### this is solution ex.2
###link 1 :https://pgexercises.com/questions/basic/selectall.html
sol select *
from cd.facilities

## Link 2 : https://pgexercises.com/questions/basic/selectspecific.html
sol select name,membercost
from cd.facilities			
			
			
		
		
    
