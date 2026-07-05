# Datatypes
A data type defines the type of values that can be stored in a column of a table.

## Numeric Data Types
Used to store numbers.

| Data Type          | Description                           | Example          |
|--------------------|---------------------------------------|------------------|
| SMALLINT           | Small integer                         | `250`            |
| INTEGER / INT      | Whole numbers                         | `1500`           |
| BIGINT             | Very large integers                   | `9876543210`     |
| DECIMAL(p,s)       | Exact decimal values                  | `99.95`          |
| NUMERIC(p,s)       | Same as `DECIMAL`                     | `45.678`         |
| REAL               | Single-precision floating-point       | `12.45`          |
| FLOAT              | Approximate decimal number            | `3.14159`        |
| DOUBLE PRECISION   | Double-precision floating-point       | `12345.6789`     |

p (Precision): The total number of digits that can be stored (before and after the decimal point).
s (Scale): The number of digits to the right of the decimal point.

## Character Data Types
Used to store text.

| Data Type    | Description            |
| :----------- | :--------------------- |
| `CHAR(n)`    | Fixed-length string    |
| `VARCHAR(n)` | Variable-length string |
| `TEXT`       | Large amount of text   |

## Boolean Data Type
Used to store logical values.
BOOLEAN is the datatype and the possible values are TRUE, FALSE and NULL.
| Value   | Description                          |
| :------ | :----------------------------------- |
| `TRUE`  | Represents a true condition.         |
| `FALSE` | Represents a false condition.        |
| `NULL`  | Represents an unknown or missing value. |

## Date and Time Data Types
Used to store dates, times, and durations.

| Data Type   | Description      | Example               |
| :---------- | :--------------- | :-------------------- |
| `DATE`      | Date only        | `2026-07-03`          |
| `TIME`      | Time only        | `15:30:45`            |
| `TIMESTAMP` | Date and time    | `2026-07-03 15:30:45` |
| `INTERVAL`  | Time duration    | `2 days 5 hours`      |




# Constraints

A constraint is a rule applied to one or more columns of a table to ensure the accuracy, consistency, and integrity of the data stored in the database.

| Constraint    |                                          Description                                           |
| :------------ | :--------------------------------------------------------------------------------------------- |
| `NOT NULL`    | Ensures that a column cannot store `NULL` values.                                              |
| `UNIQUE`      | Ensures that all values in a column are unique.                                                |
| `PRIMARY KEY` | Uniquely identifies each row in a table. It cannot contain `NULL` values.                      |
| `FOREIGN KEY` | Establishes a relationship between two tables by referencing the primary key of another table. |
| `CHECK`       | Ensures that all values in a column satisfy a specified condition.                             |
| `DEFAULT`     | Assigns a default value to a column if no value is provided during insertion.                  |


CREATE TABLE SYNTAX :
create table table_name(col datatype constraint, ...);

Example:

create table random (
ID serial primary key,
name varchar(100) not null,
email text unique,
created_at date default now(),
age int check(age>=18)
);




** SERIAL Data Type in PostgreSQL

SERIAL is a pseudo-data type in PostgreSQL that is used to automatically generate sequential integer values for a column. It is commonly used for primary keys.

Syntax
CREATE TABLE employee (
    emp_id SERIAL PRIMARY KEY,
    name VARCHAR(50)
);
How It Works

When you declare a column as SERIAL, PostgreSQL automatically:

Creates an integer column.
Creates a sequence (counter).
Sets the column's default value to the next value from that sequence.

So, when you insert rows:

INSERT INTO employee (name)
VALUES
('Akash'),
('Rahul'),
('Priya');

The table becomes:
| emp_id | name  |
| :----- | :---- |
| `1`    | Akash |
| `2`    | Rahul |
| `3`    | Priya |
