-- Create a Table:
CREATE TABLE students (
     id INT,
	 name char(50),
	 age INT,
	 grade char(1)
);

-- Insert value on a Table:
INSERT INTO students(id, name, age, grade)
VALUES
    (1, 'John Doe', 20, 'A'),
    (2, 'Jane Smith', 21, 'B'),
    (3, 'Bob Johnson', 19, 'A'),
    (4, 'Alice Brown', 22, 'B');

-- find columns by query:
SELECT * FROM students;
SELECT name, age FROM students;
SELECT name FROM students;

-- Where keyword:
SELECT name FROM students WHERE age = 20;
SELECT name FROM students WHERE age > 20;

-- Update data on a table by UPDATE, SET and WHERE:
UPDATE students
SET age = 25
WHERE name = 'John Doe';

-- Delete data:
DELETE FROM students
WHERE id = 4;
