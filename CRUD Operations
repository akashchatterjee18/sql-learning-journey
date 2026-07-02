# creating database
create database database_name;

# connecting to database
\c database_name 
"NOTE :  since \c is a psql command, not SQL, so it doesn't require a semicolon."


# creating table
create table table_name (
    column1 datatype constraints,
    column2 datatype constraints,
    column3 datatype constraints,
    ...
);

# inserting values into all columns (in table order)
insert into table_name 
values
(value1, value2, value3, ...);

# inserting values into selected columns
insert into table_name (column1, column2, column3, ...)
values
(value1, value2, value3, ...);

# to view all data from table
select * from table_name;

# to view particular column data from table
select column1, column2, ... from table_name;

# to view all data from table with conditions
select * from table_name where condition1 and/or/not condition2 and/or/not condition3 ...;

# to view particular column data from table with conditions
select column1, column2, ... from table_name where condition1 and/or/not condition2 and/or/not condition3 ...;

# update data in table
update table_name set column1 = value1, column2 = value2, ... where condition1 and/or/not condition2 and/or/not condition3 ...;

# delete data(rows) from table
delete from table_name where condition;
