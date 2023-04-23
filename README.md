-- This project involves the creation of a clothing store database using SQL. The database includes a "store" table with columns for item ID, item name, category, price, quantity, and color. 
The data is populated using SQL INSERT statements. Various SQL queries are then used to analyze the data, including displaying the entire database ordered by price, 
finding the total cost of all skirts in the database, and determining the average price of an item in the store. 
This project demonstrates how SQL can be used to create and manipulate databases for retail businesses.

CREATE TABLE store (
    item_id INTEGER PRIMARY KEY,
    item_name TEXT,
    category TEXT,
    price REAL,
    quantity INTEGER,
    color TEXT
);

INSERT INTO store (item_id, item_name, category, price, quantity, color)
VALUES
    (1,'floral dress','dresses', 100, 25, 'pink'),
    (2,'red dress', 'dresses', 150, 30, 'red'),
    (3,'blue skirt', 'skirts', 60, 44, 'blue'),
    (4,'purple skirt', 'skirts', 60, 40, 'purple'),
    (5,'pink dress', 'dresses', 130, 20, 'pink'),
    (6,'teal skirt', 'skirts', 50, 55, 'teal'),
    (7, 'blue top', 'tops', 69, 30, 'blue'),
    (8, 'purple top', 'tops', 70, 20, 'purple'),
    (9, 'red top', 'tops', 60, 40, 'red'),
    (10, 'stripe dress', 'dresses', 200, 10, 'purple'),
    (11,' polka dot skirt', 'skirt', 100, 44, 'pink'),
    (12, 'sheer skirt', 'skirt', 40, 20, 'blue'),
    (13, 'diamond dress', 'dresses', 230, 5, 'pink'),
    (14, 'maxi dress', 'dresses', 170, 33, 'red'),
    (15, 'flare dress', 'dresses', 80, 25, 'pink');
    
-- Display the database ordered by price.
    
SELECT * FROM store
ORDER BY price desc;;

--What is the total cost of all the skirts?
SELECT sum(quantity) from store WHERE category= 'skirts';

--What is the avergae price of an item from this store?
SELECT avg(price) FROM store
