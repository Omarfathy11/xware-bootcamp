# Exercise 2
Table: Logins
+----------------+----------+
| Column Name    | Type     |
+----------------+----------+
| user_id        | int      |
| time_stamp     | datetime |
+----------------+----------+
# answer

create table if not exists logins(
       user_id int,
time_stamp varchar(400),
     PRIMARY KEY (user_id, time_stamp)

);

Example 1:
Input: 
Logins table:
+---------+---------------------+
| user_id | time_stamp          |
+---------+---------------------+
| 6       | 2020-06-30 15:06:07 |
| 6       | 2021-04-21 14:06:06 |
| 6       | 2019-03-07 00:18:15 |
| 8       | 2020-02-01 05:10:53 |
| 8       | 2020-12-30 00:46:50 |
| 2       | 2020-01-16 02:49:50 |
| 2       | 2019-08-25 07:59:08 |
| 14      | 2019-07-14 09:00:00 |
| 14      | 2021-01-06 11:59:59 |
+---------+---------------------+
# answer

insert into logins(user_id, time_stamp) values (6, '2020-06-30 15:06:07');
insert into logins(user_id, time_stamp) values (6, '2021-04-21 14:06:06');
insert into logins(user_id, time_stamp) values (6, '2019-03-07 00:18:15');
insert into logins(user_id, time_stamp) values (8, '2020-02-01 05:10:53');
insert into logins(user_id, time_stamp) values (8, '2020-12-30 00:46:50');
insert into logins(user_id, time_stamp) values (2, '2020-01-16 02:49:50');
insert into logins(user_id, time_stamp) values (2, '2019-08-25 07:59:08');
insert into logins(user_id, time_stamp) values (14, '2019-07-14 09:00:00');
insert into logins(user_id, time_stamp) values (14, '2021-01-06 11:59:59');

Output: 
+---------+---------------------+
| user_id | last_stamp          |
+---------+---------------------+
| 6       | 2020-06-30 15:06:07 |
| 8       | 2020-12-30 00:46:50 |
| 2       | 2020-01-16 02:49:50 |
+---------+---------------------+
# answer 

select user_id,
	max(time_stamp)
		as last_stamp from Logins
		WHERE time_stamp >= '2020-01-01'
			and time_stamp < '2021-01-01'
				group by user_id
				
				
+---------+---------------------+
| user_id | last_stamp          |
+---------+---------------------+
| 6       | 2020-06-30 15:06:07 |
| 8       | 2020-12-30 00:46:50 |
| 2       | 2020-01-16 02:49:50 |
+---------+---------------------+

