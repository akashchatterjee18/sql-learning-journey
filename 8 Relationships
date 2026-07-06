## Relationships
-- In a relational database, data is stored across multiple tables
-- These tables are connected through relationships.
-- Instead of repeating the same data again and again in one huge table, we split it into smaller, meaningful tables and connect them using keys (Primary Keys and Foreign Keys).
Types of Relationships :
One-to-One (1:1)
Concept :
You have a students table → each student has a unique student_id (Primary Key).
You have a student_profiles table → each profile also has a unique student_id (Foreign Key + Unique).

One-to-Many (1:M)
Concept :
You have a students table → each student has a unique student_id (Primary Key).
You also have a student_marks table → each row stores marks for one subject and contains a student_id as a Foreign Key.
The same student_id can appear multiple times in student_marks, representing that one student has marks in multiple subjects.
So, one student in the students table is connected to many rows in the student_marks table.

Many-to-Many (M:N)
Concept :
In many-to-many, both tables (e.g. students and courses) have multiple entries—and multiple relationships between them.
In a many-to-many relationship, you don't directly connect the two tables using a foreign key.
Instead, you create a third table (called a junction table) that breaks the many-to-many relationship into two one-to-many relationships.
