# You Are Required To Solve This Problem:
* Table: Person
* +-------------+---------+
* | Column Name | Type    |
* +-------------+---------+
* | personId    | int     |
* | lastName    | varchar |
* | firstName   | varchar |
* +-------------+---------+
* personId is the primary key column for this table.
* This table contains information about the ID of some persons and their first and last names.


* Table: Address
* +-------------+---------+
* | Column Name | Type    |
* +-------------+---------+
* | addressId   | int     |
* | personId    | int     |
* | city        | varchar |
* | state       | varchar |
* +-------------+---------+
* addressId is the primary key column for this table.
* Each row of this table contains information about the city and state of one person with ID = PersonId.

* Example 1:
* Input: 
* Person table:
* +----------+----------+-----------+
* | personId | lastName | firstName |
* +----------+----------+-----------+
* | 1        | Wang     | Allen     |
* | 2        | Alice    | Bob       |
* +----------+----------+-----------+
* Address table:
* +-----------+----------+---------------+------------+
* | addressId | personId | city          | state      |
 +-----------+----------+---------------+------------+
* | 1         | 2        | New York City | New York   |
* | 2         | 3        | Leetcode      | California |
* +-----------+----------+---------------+------------+
* Output: 
* +-----------+----------+---------------+----------+
* | firstName | lastName | city          | state    |
* +-----------+----------+---------------+----------+
* | Allen     | Wang     | Null          | Null     |
* | Bob       | Alice    | New York City | New York |
* +-----------+----------+---------------+----------+
* Explanation: 
* There is no address in the address table for the personId = 1 so we return null in their city and state.
* addressId = 1 contains information about the address of personId = 2.

# answer 


 * create table if not exists person(
	* personId serial primary key,
	* lastName varchar(50) not null,
	* firstName varchar(50) not null
	);
	
Create table if not exists Address (
   * address_id serial primary key,
	* city  varchar(50),
	* state varchar(50),
	* person_Id int references person
);
 * insert
* insert into person (personId, firstName, lastName) values (1, ' Allen', 'Wang');
* insert into person (personId, firstName, lastName) values (2, 'Bob', 'Alice ');

* insert into Address (address_id, person_Id, city, state) values (1, 2, ' New York City', 'New York');
* insert into Address (address_Id, person_Id, city, state) values (2, 3, 'Leetcode', 'California'); 

* select Person.personId  , lastname , firstname , Address.address_Id , city , state from Address INNER JOIN Person ON Address.person_Id = Person.personId ;
