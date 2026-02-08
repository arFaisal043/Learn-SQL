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


-- See values:
SELECT * FROM products;
SELECT name, price FROM products WHERE is_available = true; 