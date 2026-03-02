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



____________________________ Data Type and Constraints ________________________________




CREATE TABLE random(
   id SERIAL PRIMARY KEY,
   name VARCHAR(100) NOT NULL,
   email TEXT UNIQUE,
   created_at DATE DEFAULT now(),
   age INT CHECK (age >= 18)
);

Insert into random(name, email, age)
VALUES 
   ('Abdur Rahman', 'abdurrahman321@gmail.com', 23);


SELECT * FROM random;





____________________________ Create a Task to learn Create table, Data Type and Constraints ________________________________





-- Small task about Flipkart

-- Create a Product table:
CREATE TABLE products(
   product_id SERIAL PRIMARY KEY,
   name VARCHAR(100) NOT NULL,
   sku_code CHAR(8) UNIQUE NOT NULL CHECK (CHAR_LENGTH(sku_code) = 8,
   price NUMERIC(10, 2) DEFAULT 0 CHECK (price >= 0),
   stock_quantity INT DEFAULT 0 CHECK (stock_quantity >= 0),
   is_available BOOLEAN DEFAULT TRUE,
   category TEXT NOT NULL,
   added_on DATE DEFAULT CURRENT_DATE,
   last_update TIMESTAMP DEFAULT NOW()
);

-- Insert values:
INSERT INTO products (name, sku_code, price, stock_quantity, is_available, category)
VALUES
-- Electronics (SKU: ELEC-XXX)
('iPhone 15 Pro', 'ELEC001A', 999.99, 45, true, 'Electronics'),
('Samsung Galaxy', 'ELEC002B', 899.99, 32, true, 'Electronics'),
('Sony Headphones', 'ELEC003C', 349.99, 78, true, 'Electronics'),
('MacBook Air M3', 'ELEC004D', 1299.99, 15, true, 'Electronics'),
('Apple Watch 9', 'ELEC005E', 429.99, 0, false, 'Electronics'),

-- Clothing (SKU: CLTH-XXX)
('Nike Air Max', 'CLTH001F', 129.99, 120, true, 'Clothing'),
('Levi''s Jeans', 'CLTH002G', 89.99, 67, true, 'Clothing'),
('Adidas T-shirt', 'CLTH003H', 24.99, 230, true, 'Clothing'),
('North Face Jack', 'CLTH004I', 199.99, 25, true, 'Clothing'),
('Converse Shoes', 'CLTH005J', 65.99, 0, false, 'Clothing'),

-- Books (SKU: BOOK-XXX)
('Atomic Habits', 'BOOK001K', 16.99, 89, true, 'Books'),
('Midnight Library', 'BOOK002L', 14.99, 54, true, 'Books'),
('Python Guide', 'BOOK003M', 39.99, 12, true, 'Books'),
('Dune Novel', 'BOOK004N', 12.99, 0, false, 'Books'),
('Harry Potter', 'BOOK005O', 89.99, 8, true, 'Books'),

-- Kitchen (SKU: KITC-XXX)
('Instant Pot', 'KITC001P', 89.99, 42, true, 'Kitchen'),
('KitchenAid Mix', 'KITC002Q', 399.99, 7, true, 'Kitchen'),
('YETI Bottle', 'KITC003R', 49.99, 96, true, 'Kitchen'),
('Nespresso Mach', 'KITC004S', 179.99, 0, false, 'Kitchen'),
('Dyson Vacuum', 'KITC005T', 699.99, 3, true, 'Kitchen');


SELECT * FROM products;


- Small task about Flipkart

-- Create a Product table:
CREATE TABLE products(
   product_id SERIAL PRIMARY KEY,
   name VARCHAR(100) NOT NULL,
   sku_code CHAR(8) UNIQUE NOT NULL CHECK (CHAR_LENGTH(sku_code) = 8),
   price NUMERIC(10, 2) DEFAULT 0 CHECK (price >= 0),
   stock_quantity INT DEFAULT 0 CHECK (stock_quantity >= 0),
   is_available BOOLEAN DEFAULT TRUE,
   category TEXT NOT NULL,
   added_on DATE DEFAULT CURRENT_DATE,
   last_update TIMESTAMP DEFAULT NOW()
);

-- Insert values:
INSERT INTO products (name, sku_code, price, stock_quantity, is_available, category)
VALUES
-- Electronics (SKU: ELEC-XXX)
('iPhone 15 Pro', 'ELEC001A', 999.99, 45, true, 'Electronics'),
('Samsung Galaxy', 'ELEC002B', 899.99, 32, true, 'Electronics'),
('Sony Headphones', 'ELEC003C', 349.99, 78, true, 'Electronics'),
('MacBook Air M3', 'ELEC004D', 1299.99, 15, true, 'Electronics'),
('Apple Watch 9', 'ELEC005E', 429.99, 0, false, 'Electronics'),

-- Clothing (SKU: CLTH-XXX)
('Nike Air Max', 'CLTH001F', 129.99, 120, true, 'Clothing'),
('Levi''s Jeans', 'CLTH002G', 89.99, 67, true, 'Clothing'),
('Adidas T-shirt', 'CLTH003H', 24.99, 230, true, 'Clothing'),
('North Face Jack', 'CLTH004I', 199.99, 25, true, 'Clothing'),
('Converse Shoes', 'CLTH005J', 65.99, 0, false, 'Clothing'),

-- Books (SKU: BOOK-XXX)
('Atomic Habits', 'BOOK001K', 16.99, 89, true, 'Books'),
('Midnight Library', 'BOOK002L', 14.99, 54, true, 'Books'),
('Python Guide', 'BOOK003M', 39.99, 12, true, 'Books'),
('Dune Novel', 'BOOK004N', 12.99, 0, false, 'Books'),
('Harry Potter', 'BOOK005O', 89.99, 8, true, 'Books'),

-- Kitchen (SKU: KITC-XXX)
('Instant Pot', 'KITC001P', 89.99, 42, true, 'Kitchen'),
('KitchenAid Mix', 'KITC002Q', 399.99, 7, true, 'Kitchen'),
('YETI Bottle', 'KITC003R', 49.99, 96, true, 'Kitchen'),
('Nespresso Mach', 'KITC004S', 179.99, 0, false, 'Kitchen'),
('Dyson Vacuum', 'KITC005T', 699.99, 3, true, 'Kitchen');


SELECT * FROM products;

_________________________ TEST 1 ________________________________

-- Q1. Show the name and price of all products.
SELECT name, price FROM products

-- Q2. Show all products where the category is 'Electronics'.
SELECT * FROM products WHERE category = 'Electronics';

-- Q3. Group products by category. Show each category once.
SELECT category FROM products GROUP BY category;

-- Q4. Show categories that have more than 4 product. (Use after GROUP BY)
SELECT category, COUNT(*) FROM products GROUP BY category
HAVING COUNT(*) > 4;

-- Q5. Show all products sorted by price in ascending and descending order.
SELECT * FROM products ORDER BY price;
SELECT * FROM products ORDER BY price DESC;

-- Q6. Show only the first 5 products from the table.
SELECT * FROM products LIMIT 5;

-- Q7. Show product name as "Item_Name" and price as "Item_Price".
SELECT name AS Item_Name, price AS Item_Price FROM products;

-- Q8. Show all the unique categories from the products table.
SELECT DISTINCT category FROM products;




- CLAUSES WITH OPERATORS:

1. Comparison: (=, !=, <, >, <=, >=)
SELECT name, price FROM products WHERE price != 999.99;


2. Range using BETWEEN keywords:

-- Products priced between $50 and $100
SELECT name, price, category FROM products WHERE price BETWEEN 50 and 100;


3. Set using IN and NOT IN keywords: Checks if a value matches ANY value in a list or not.

IN Example:
-- Products in specific categories
SELECT name, category, price FROM products
WHERE category IN ('Clothing', 'Books');

NOT IN Example:
SELECT name, category, price FROM products
WHERE category NOT IN ('Clothing', 'Books');


4. Pattern (LIKE)

-- in sku_code find that are start with letter B
SELECT sku_code FROM products WHERE sku_code LIKE 'B%';

-- Products ending with 'er'
SELECT name, category FROM products
WHERE name LIKE '%er';
- Returns: Mixer, Blender, Toaster

-- Products containing 'Book' anywhere
SELECT name, category
FROM products
WHERE name LIKE '%Book%';
- Returns: Notebook, Textbook, Bookmark

-- SKU codes with pattern: 2 letters, 4 numbers
SELECT name, sku_code
FROM products
WHERE sku_code LIKE '__1234';


5. Logical (AND, OR, NOT)

- AND Operation:
-- Electronics under $500 with stock available
SELECT name, price, category FROM products WHERE category = 'Electronics' 
AND price <= 500
AND is_available = true;


- OR Operation:
-- Electronics under $500 or stock available
SELECT name, price, category, is_available FROM products WHERE category = 'Electronics' 
AND price <= 500
OR is_available = true;


- NOT Operation:
-- Not electronics under $500 and not stock available
SELECT name, price, category, is_available FROM products WHERE category != 'Electronics' 
AND price <= 500
AND NOT is_available = false;






____________________________ AGGREGATION FUNCTIONS ________________________________


- COUNT, SUM, AVG, MIN, MAX 


-- Total number of products:
SELECT COUNT(*) FROM products;

-- Total price in a category(electronics):
SELECT SUM(price) FROM products WHERE category = 'Electronics';

-- Average price of accessories:
SELECT ROUND(AVG(price), 2) FROM products WHERE category = 'Electronics';

-- Cheapest product:
SELECT MIN(price) FROM products WHERE category = 'Electronics';

-- Most expensive product
SELECT MAX(price) FROM products WHERE category = 'Electronics';







______________________________ TEST 2 _________________________________

-- Q1. Display the name and price of the cheapest product in the entire table.
SELECT name, price FROM products 
WHERE price = (SELECT MIN(price) FROM products);

-- Q2.Find the average price of products that belong to the 'Electronics & Clothing' or 'Books' category.
SELECT ROUND(AVG(price), 2) FROM products
WHERE category IN ('Electronics', 'Clothing')
OR category = 'Books';

-- Q3. Show product names and stock quantity where the product is available, stock is more than 50, and price is not equal to $999.99.
SELECT name, stock_quantity FROM products
WHERE is_available = true
AND stock_quantity > 50
AND price != 999.99;

-- Q4. Find the most expensive product in each category (name and price).
SELECT category, MAX(price) FROM products 
GROUP BY category;

-- Q5. Show all unique categories in uppercase, sorted in descending order.
SELECT UPPER(category) FROM products 
GROUP BY category 
ORDER BY category DESC






______________________________ STRING FUNCTIONS _______________________________


SELECT LENGTH(name) FROM products
SELECT UPPER(name) FROM products
SELECT LOWER(name) FROM products

- Sub string:
SELECT name, SUBSTR(category, 1, 5) FROM products; // output: Elect

- Sub string from left:
SELECT LEFT(category, 5) FROM products // Elect

- Sub string from right:
SELECT RIGHT(category, 5) FROM products // onics

- String Concat:
SELECT CONCAT(name, ' ', category) FROM products; // iPhone 15 Pro Electronics
SELECT CONCAT_WS(' : ', name, category) FROM products; // iPhone 15 Pro : Electronics

- trim() - This function will remove all the spaces from the string

- replace() - This function will replace any thing you want.







________________________________ ALTER _______________________________

- ALTER is a SQL command used to modify the structure of existing database objects (tables, columns, constraints, etc.) without deleting and recreating them.


-- Add a new column
ALTER TABLE products 
ADD COLUMN brand VARCHAR(50) DEFAULT 0;

-- Remove a column
ALTER TABLE products 
DROP COLUMN brand;

-- Change data type
ALTER TABLE products 
ALTER COLUMN price TYPE DECIMAL(12,2);

-- Rename a column
ALTER TABLE products 
RENAME COLUMN last_update TO updated_at;

-- Remove a Default Value
ALTER TABLE products 
ALTER COLUMN price DROP DEFAULT;






____________________________________ CASE ____________________________________

- CASE is a conditional expression in SQL that works like an if-else or switch statement. It lets you
return different values based on different conditions — all within a single query.


# - Syntax of CASE in SQL: when = if and else if

SELECT column1, column2,
CASE
  WHEN condition1 THEN result1
  WHEN condition2 THEN result2
...
  ELSE default_result
END AS new_column_name
FROM table_name;


# -- practice ques 1: Best way to learn the case is using a simple example where you will add a custom column in which you will have price_tag. If the price is above 1000 you will say it is expensive.
If the price is between 500 and 1000 you will say it is moderate. and If the price is below 500 it is cheap.

SELECT name, price,
CASE WHEN (price > 1000) THEN 'Expensive'
     WHEN price BETWEEN 500 AND 1000 THEN 'Moderate'
	 ELSE 'Cheap'
END AS price_tag FROM products;

## this col is not add on real datasets. this is a just snapshot


# => Add same on real data.

-- STEP 1: create a new col
ALTER TABLE products
ADD COLUMN price_tag TEXT;

-- STEP 2: update col val according to the conditions
UPDATE products
SET price_tag =
CASE WHEN (price > 1000) THEN 'Expensive'
     WHEN price BETWEEN 500 AND 1000 THEN 'Moderate'
	 ELSE 'Cheap'
END;




# -- Practice ques 2: Ok now lets do one important question inside is available column you have boolean true and false show case a new column to with in_stock and out of stock.

-- STEP 1: CREATE A COL
ALTER TABLE products
ADD COLUMN is_available_product TEXT;

-- STEP 2: UPDATE COL VALUE
UPDATE products
SET is_available_product =
CASE WHEN is_available = TRUE THEN 'in_stock'
     WHEN is_available = FALSE THEN 'out_of_stock'
END;





________________________________ RELATIONSHIP AND JOIN _______________________________


# what is the purpose of primary and foreign key:

🔑 Primary Key
Purpose: Uniquely identifies each row in a table
Example: Like your passport number - uniquely identifies YOU

🔗 Foreign Key
Purpose: Links tables together (creates relationship)
Example: Like your passport number on a flight booking - connects YOU to your flight



# Join:

📝 Quick Reference 

JOIN Type	        Returns	                      Use When
INNER	          Only matches	                Need only related data
LEFT	          All left + matches	          Need ALL from main table
RIGHT	          All right + matches	          Need ALL from secondary table
FULL	          All from both	                Need complete picture
CROSS	          Every combination	          Need all possibilities
SELF	          Table with itself	          Need hierarchical data




## => ONE TO ONE RELATION:

-- Students table (parent)
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);

-- Student_profiles table (child) - One-to-One relationship
CREATE TABLE student_profiles (
    student_id INT PRIMARY KEY,
    address TEXT,
    age INT,
    phone VARCHAR(15)
);


-- insert into students table
INSERT INTO students (name) 
VALUES
('Emma Watson'),
('James Smith'),
('Maria Garcia'),
('David Brown'),
('Sophia Lee'),
('Michael Chen'),
('Olivia Johnson'),
('William Taylor'),
('Isabella Martinez'),
('Alexander Wilson');


-- insert into student_profiles table
INSERT INTO student_profiles (student_id, address, age, phone) 
VALUES
(1, '123 Main St, New York, NY 10001', 20, '555-0101'),
(2, '456 Oak Ave, Los Angeles, CA 90001', 22, '555-0102'),
(3, '789 Pine Rd, Chicago, IL 60601', 19, '555-0103'),
(4, '321 Elm St, Houston, TX 77001', 21, '555-0104'),
(5, '654 Maple Dr, Phoenix, AZ 85001', 20, '555-0105'),
(6, '987 Cedar Ln, Philadelphia, PA 19101', 23, '555-0106'),
(7, '147 Birch Blvd, San Antonio, TX 78201', 22, '555-0107'),
(8, '258 Willow Way, San Diego, CA 92101', 20, '555-0108'),
(9, '369 Spruce Ct, Dallas, TX 75201', 21, '555-0109'),
(10, '741 Ash Ave, San Jose, CA 95101', 19, '555-0110');


SELECT * FROM students;
SELECT * FROM student_profiles;


-- This code adds a Foreign Key constraint to an existing table, which creates a rule linking student_profiles to students
ALTER TABLE student_profiles
ADD CONSTRAINT fk_student_id
FOREIGN KEY (student_id)
REFERENCES students(student_id);


-- Join Query to see all data together
SELECT
/*	s.student_id,
	s.name,
	sp.address,
	sp.age,
	sp.phone */  --> this is projection
FROM students s
JOIN student_profiles sp
ON s.student_id = sp.student_id;


## => ONE TO MANY RELATION:

DATASET:
-- Students table (ONE)
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(50) NOT NULL
);


-- Orders table (MANY) - Each student can have multiple orders
CREATE TABLE orders (
    order_id SERIAL PRIMARY KEY,
    student_id INT NOT NULL,
    item VARCHAR(50),
    amount DECIMAL(5,2),
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);


INSERT INTO students (name) 
VALUES
('Emma'),
('James'),
('Maria'),
('David'),
('Sophia');



INSERT INTO orders (student_id, item, amount) 
VALUES
-- Emma (student_id=1) has 3 orders
(1, 'Laptop', 999.99),
(1, 'Mouse', 29.99),
(1, 'Keyboard', 79.99),

-- James (student_id=2) has 2 orders
(2, 'Books', 49.99),
(2, 'Notebook', 4.99),

-- Maria (student_id=3) has 3 orders
(3, 'Phone', 599.99),
(3, 'Case', 19.99),
(3, 'Charger', 29.99),

-- David (student_id=4) has 2 orders
(4, 'Shoes', 89.99),
(4, 'Socks', 9.99),

-- Sophia (student_id=5) has 2 orders
(5, 'Bag', 49.99),
(5, 'Pen', 2.99);


SELECT * FROM students;
SELECT * FROM orders;



# -- Inner Join:
SELECT * FROM students s INNER JOIN orders o
ON s.student_id = o.student_id;

# -- LEFT Join:
SELECT * FROM students s LEFT JOIN orders o
ON s.student_id = o.student_id;



## => MANY TO MANY RELATION:

📋 What is Many-to-Many?
A many-to-many relationship occurs when multiple records in Table A relate to multiple records in Table B.

Examples:
Students can take many Courses / Courses can have many Students
Authors can write many Books / Books can have many Authors

🔧 How It Works: The Junction Table
Many-to-many relationships require a third table (junction/linking table) to connect them.


Schemas:

-- Table 1: Students (ONE side of many-to-many)
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);

-- Table 2: Courses (OTHER side of many-to-many)
CREATE TABLE courses (
    course_id SERIAL PRIMARY KEY,
    course_name VARCHAR(100) NOT NULL,
    credits INT
);

-- Table 3: Junction/Enrollment table (connects both)
CREATE TABLE enrollments (
    enrollment_id SERIAL PRIMARY KEY,  -- Optional
    student_id INT NOT NULL,
    course_id INT NOT NULL,
    enrollment_date DATE,
    grade CHAR(2),
    -- Composite foreign keys
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id),
    -- Prevent duplicate enrollments
    UNIQUE(student_id, course_id)
);



Data:

-- Students
INSERT INTO students (name) VALUES
('Emma'), ('James'), ('Maria'), ('David');

-- Courses
INSERT INTO courses (course_name, credits) VALUES
('Math', 3), ('Physics', 4), ('Chemistry', 3), ('Biology', 3);

-- Enrollments (junction table)
INSERT INTO enrollments (student_id, course_id, enrollment_date, grade) VALUES
-- Emma takes Math and Physics
(1, 1, '2024-01-15', 'A'),
(1, 2, '2024-01-15', 'B+'),
-- James takes Math, Physics, and Chemistry
(2, 1, '2024-01-15', 'B'),
(2, 2, '2024-01-15', 'A-'),
(2, 3, '2024-01-15', 'C+'),
-- Maria takes Chemistry and Biology
(3, 3, '2024-01-15', 'A'),
(3, 4, '2024-01-15', 'B-'),
-- David only takes Math
(4, 1, '2024-01-15', 'A');



🔍 How the Data Looks

# Students Table:
student_id	 name
1	          Emma
2	          James
3	          Maria
4	          David


# Courses Table:
course_id	  course_name	      credits
1	            Math	               3
2	            Physics	            4
3	            Chemistry	         3
4	            Biology	            3


# Enrollments Table (Junction):
enrollment_id	  student_id	  course_id	  grade
1	                  1	           1	       A
2	                  1	           2	       B+
3	                  2	           1	       B
4	                  2	           2	       A-
5	                  2	           3	       C+
6	                  3	           3	       A
7	                  3	           4	       B-
8	                  4	           1	       A



1. Get all students with their courses:

SELECT 
    s.name AS student,
    c.course_name,
    e.grade
FROM students s
JOIN enrollments e ON s.student_id = e.student_id
JOIN courses c ON e.course_id = c.course_id
ORDER BY s.name, c.course_name;


- Result:

student	      course_name	        grade
Emma	            Math	             A
David	            Math	             A
Emma	            Physics	          B+
James	            Chemistry	       C+
James	            Math	             B
James	            Physics	          A-
Maria	            Biology	          B-
Maria	            Chemistry	       A







______________________________ Views ___________________________


# WHAT IS A VIEW IN SQL?

A view is a virtual table based on a SQL query.
It does not store actual data, but shows results when
accessed — just like a saved query

structure:

CREATE VIEW view_name AS
SELECT column1, column2
FROM table_name
WHERE condition;









______________________________ PROCEDURES ___________________________


# A procedure is a block of SQL code that performs a series of operations — like inserting, updating, deleting, or selecting data — and is stored in the database.

“ Think of it like a function in programming — once
defined, you can call it again and again without rewriting
the logic.


- structure:

// create a like function
CREATE PROCEDURE procedure_name(param1 datatype, param2 datatype)
LANGUAGE plpgsql
AS $$
BEGIN
-- Your SQL logic here
END;
$$;

// call the function
CALL procedure_name(value1, value2);