## 1:1 Relationship

-- Create 2 tables

1st table :
create table students (
student_id serial primary key,
name varchar(100) not null
);

insert into students (name)
values
('Akash Chatterjee'),
('Ayush Chatterjee'),
('Rohan Gupta');

2nd table :
create table student_profiles (
student_id int primary key,
address text,
age int
phone varchar(15)
);

insert into student_profiles (student_id,address,age,phone)
values
(1,'Kolkata, India',20,9999999999),
(2,'Delhi, India',15,9999998999),
(3,'Mumbai, India',19,9999997999);

-- now create a foreign key and connect using references

alter table student_profiles add constraint fk_student_id foreign key (student_id) references students(student_id);

-- now to see the data together we have to use the joins

select
s.student_id,
s.name,
sp.address,
sp.age,
sp.phone
from students s
join student_profiles sp
on s.student_id = sp.student_id;

-- to understand more about join have to understand one to many...
