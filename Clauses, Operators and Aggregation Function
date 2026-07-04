## Clauses

Clauses are mainly used for querying the data and are kind of building blocks of sql queries.
| SQL Clause | Purpose |
| `SELECT`   | Choose which columns to display |
| `FROM`     | Specify the table |
| `WHERE`    | Filter rows based on a condition |
| `GROUP BY` | Group rows for aggregation |
| `HAVING`   | Filter aggregated groups (used after `GROUP BY`) |
| `ORDER BY` | Sort the result in ascending or descending order |
| `LIMIT`    | Limit the number of rows returned |
| `AS`       | Rename columns or tables temporarily (aliasing) |
| `DISTINCT` | Return only unique/distinct values |

use data from learning project 1

CLAUSES TEST

Q1. Show the name and price of all products.
select name,price from products;

Q2. Show all products where the category is 'Electronics'.
select * from products where category = 'Electronics';

Q3. Group products by category. Show each category once.
select category from products group by category;

Q4. Show categories that have more than 1 product. (Use after GROUP BY)
select category from products group by category having count(*)>1;

Q5. Show all products sorted by price in ascending order.
select * from products order by price;

Q6. Show all products sorted by price in descending order.
select * from products order by price desc;

Q7. Show only the first 3 products from the table.
select * from products limit 3;

Q8. Show product name as "Item_Name" and price as "Item_Price".
select name as Item_Name, price as Item_Price from products;

Q9. Show all the unique categories from the products.
select distinct category from products;


## Operators

- Comparison Operators (=,!=,<,>,<=,>=)
eg1 : 
Show all products where the category is not 'Electronics'.
select * from products where category != 'Electronics';
eg2 : 
Show all products where the price is greater than 1000.
select * from products where price > 1000;

- Range Operators (Between)
eg :
Show all products where the price is greater than equal to 400 and less than equal to 1000.
select * from products where price between 400 and 1000;

- Set Operators (In)
eg : 
Show all products where the category is 'Electronics' or 'Fitness' or 'Home & Kitchen'.
select * from products where category in ('Electronics','Fitness','Home & Kitchen');

- Pattern Operators (Like)
eg1 :
Show all products whose SKU starts with 'W'.
select * from products where sku_code like 'W%';
W% implies 1st letter W and then whatever...
eg2 :
Show all products whose SKU contains '123'.
select * from products where sku_code like '%123%';
%123% implies it can start with anything and end with anything but in between somewhere 123 must be there.
eg3 :
Show all products where the 2nd lettter of sku have 'B'.
select * from products where sku_code like '_B%';
_B% implies 1st letter anything, second letter 'B' and then whatever

- Logical Operators (AND,OR,NOT)
eg1 : 
Show all products where the category is not 'Electronics'.
select * from products where not category = 'Electronics';


## Aggregate Functions
used to summarise data
| Function  | Purpose               | Example                     |
| `COUNT()` | Count number of rows  | Total number of products    |
| `SUM()`   | Add numeric values    | Total stock in a category   |
| `AVG()`   | Calculate average     | Average price of accessories|
| `MIN()`   | Find smallest value   | Cheapest product            |
| `MAX()`   | Find highest value    | Most expensive product      |

select count(product_id) from products;
10 -> ans
select sum(stock_quantity) from products;
615 -> ans
select avg(price) from products;
664.3470 -> ans


5 QUESTION TEST
Q1. Display the name and price of the cheapest product in the entire table.
select name , price from products where price = (select min(price) from products);
--we have used query inside query thus the inner query is known as subquery

Q2. Find the average price of products that belong to the 'Home & Kitchen' or 'Fitness' category.
select avg(price) from products where category in ('Fitness','Home & Kitchen');

Q3. Show product names and stock quantity where the product is available, stock is more than 50, and price is not equal to ₹299.
select name , stock_quantity from products where is_available = 'true' and stock_quantity > 50 and not price = 299;
--here instead of "where is_available = 'true'" we can simply write "where is_available"


Q4. Find the most expensive product in each category (name and price).
select category , max(price) as max_price from products group by category;

Q5. Show all unique categories in UPPERCASE, sorted in descending order.
select distinct upper(category) as category_upper from products order by category_upper desc;
