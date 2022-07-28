### day 1
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
			
			
		
		
    
