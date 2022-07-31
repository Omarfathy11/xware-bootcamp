SQL

```
create table if not exists Person(
  id serial primary key,
  email varchar(30) not null check(lower(email)=email)
);
```	

# Person table:
```
+----+------------------+
| id | email            |
+----+------------------+
| 1  | john@example.com |
| 2  | bob@example.com  |
| 3  | john@example.com |
+----+------------------+
```

insert into Person(email) values ('JOHN@EXAMPLE.COM');
insert into Person(email) values ('JOHN@EXAMPLE.COM');
insert into Person(email) values ('BOB@EXAMPLE.COM');
insert into Person (email) values ('OMAR@EXAMPLE.COM');
insert into Person(email) values ('OMAR@EXAMPLE.COM');
 select lower(email) from person;
 ```
  id |      email       
----+------------------
  1 | john@example.com
  2 | BOO@EXAMPLE.COM
 11 | JOHN@EXAMPLE.COM
 12 | BOB@EXAMPLE.COM
 14 | OMAR@EXAMPLE.COM
 15 | JOHN@EXAMPLE.COM
 16 | JOHN@EXAMPLE.COM
 17 | BOB@EXAMPLE.COM
 18 | OMAR@EXAMPLE.COM
 19 | OMAR@EXAMPLE.COM
```
```
Output: 
+----+------------------+
| id | email            |
+----+------------------+
| 1  | john@example.com |
| 2  | bob@example.com  |
+----+------------------+
```
DELETE FROM person a USING person b WHERE a.id < b.id AND a.email = b.email;
select lower(email) from person;
```
       id |      email       
----+------------------
  1 | john@example.com
  2 | BOO@EXAMPLE.COM
 21 | JOHN@EXAMPLE.COM
 22 | BOB@EXAMPLE.COM
 24 | OMAR@EXAMPLE.COM
```
     


