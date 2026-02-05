1. Create a Database: 

CREATE DATABASE database_name;


2. Create a Table:

CREATE TABLE students (
    student_id INT,
	name char(50),
	age INT,
	grade char(1)
);


____________________________ Basic CRUD Operation ________________________________


3. Insert value on a table and show all columns by SELECT * :
INSERT INTO students (student_id, name, age, grade)
VALUES
    (1, 'John Doe', 20, 'A'),
    (2, 'Jane Smith', 21, 'B'),
    (3, 'Bob Johnson', 19, 'A'),
    (4, 'Alice Brown', 22, 'B');


4. Query for all columns:
SELECT * from students;


5. Query for specific columns:
SELECT name FROM students;
SELECT name, age FROM students;


6. Conditional selection by WHERE keywords:
SELECT name FROM students WHERE age = 20;
SELECT name FROM students WHERE age > 20;


7. Update data on a table by UPDATE, SET and WHERE:
UPDATE students
SET age = 25
WHERE name = 'John Doe';


8. Delete data:
DELETE FROM students
WHERE id = 4;







____________________________ Data Type and Constraints _______________________________