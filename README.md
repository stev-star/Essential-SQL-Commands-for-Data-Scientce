# Essential-SQL-Commands-for-Data-Scientce

SQL (Structured Query Language) is a programming language used to manage and manipulate relational 

database. 

As a data scientist, you may find yourself working with large datasets stored in relational databases. 

Here are some of the essential SQL commands for data scientist.

1.	` SELECT `
This is the most fundamental SQL command is used to retrieve data from a database. The Select command is 

used to specify the columns and tables to retrieve data from.

Syntax:
``` SQL
SELECT column1, column2, …
FROM table_name;
```
Example:

it is used to select name and age of students.
```SQL
SELECT name, age 
FROM students;
```
  
2.	`WHERE`

This command is used to filter data based on specified condition. The WHERE clause is used with the SELECT to 

retrieve specified data that meets the specified criteria.

Syntax:
```SQL
SELECT column1, column2
FROM table_name
WHERE column1 = ‘value’;
```
Example:

This is used to select students who have age greater than 22.
```SQL
SELECT name, age 
FROM students 
WHERE age > 22;
```

3.	`DISTINCT`

This command is used to retrieve unique values from a specified column. The DISTINCT keyword is used in conjunction with 

the SELECT statement. 

Syntax:
```SQL
SELECT DISTINCT column1
FROM table_name;
```
Example:
```SQL
SELECT DISTINCT department 
FROM employees;
```

4.	ORDER BY 

This command is used to Sort the data in a specified order based on a column. The ORDER BY clause can sort in ascending 

or descending order.

Syntax:
```SQL 
SELECT column1, column2
FROM table_name
ORDER BY column1 ASC;
```
Example:

it is used to select students name and age being ordered by their age in Descending order.
```SQL
SELECT name, age 
FROM students 
ORDER BY age DESC;
```
5.	JOIN 

This command is used to combine two or more tables based on a common column. The Join command is used to retrieve data that 

is spread across multiple tables. To perform join you need to use an alias to refer to the same table with different names. 

This is necessary because SQL requires that each table in a join operation has a unique name.

Example:
```SQL
SELECT column1, column2, column3
FROM table1 AS t1
JOIN table2 AS t2
ON t1.common_column=t2.common_column
```
Example:
```SQL
SELECT orders.order_id,
 customers.name,
 orders.order_date 
FROM orders o 
JOIN customers c
ON o.customer_id = c.customer_id;
```

SQL Server supports many kinds of different joins including INNER JOIN, SELF JOIN, CROSS JOIN, and OUTER JOIN. In fact, each join type defines the way two tables are related in a query. OUTER JOINS can further be divided into LEFT OUTER JOINS, RIGHT OUTER JOINS, and FULL OUTER JOINS.

- `INNER JOIN` creates a result table by combining rows that have matching values in two or more tables.

SELECT *
FROM table1
INNER JOIN table2
ON table1.column = table2.column;

- `LEFT JOIN` includes in a result table unmatched rows from the table that is specified before the LEFT OUTER JOIN clause.

SELECT *
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;

- `RIGHT JOIN` creates a result table and includes into it all the records from the right table and only matching rows from the 

left table.

SELECT *
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;

- `SELF JOIN` A self join is a join operation where a table is joined with itself. In other words, it is a way to combine rows 

from the same table based on a related column.

- `CROSS JOIN` creates a result table containing paired combination of each row of the first table with each row of the second table.
```SQL
SELECT *
FROM table1
CROSS JOIN table2;
```


6.	GROUP BY 

This command is used to group data based on a specified column. The GROUP BY command is often in conjunction with aggregated functions

Example:
```SQL
SELECT department, COUNT(*) 
FROM employees GROUP BY department;
```

7. HAVING

This command is used to filter rows based on conditions on aggregated data. 
Syntax:
```SQL
SELECT column1, COUNT(column2) 
FROM table_name 
GROUP BY column1 
HAVING COUNT(column2) > value;
```
Example:

```SQL
SELECT department, COUNT() 
FROM employees GROUP BY department 
HAVING COUNT() > 2;
```

8. UNION

This command is used to combine the results of two or more SELECT statements into a single table. 

Syntax: 
```SQL
SELECT column1 
FROM table1 
UNION 
SELECT column1 
FROM table2;
```
Example:

```SQL 
SELECT name 
FROM students 
WHERE age > 22 
UNION 
SELECT name 
FROM employees
WHERE department = 'Sales';
```

9. LIMIT

This command is used to limit the number of rows returned by a query. 

Syntax: 
```SQL
SELECT column1, column2 
FROM table_name LIMIT 10;
```
Example:

This command selects the first 2 students only.
```SQL
SELECT name 
FROM students LIMIT 2;
```

10. INSERT

This command is used to insert new data into a table. 

Syntax: 
```SQL
INSERT INTO table_name (column1, column2) 
VALUES (value1, value2);
```
Example:

This command inserts a new row into the students table with the name 'David' and age 24.
```SQL
INSERT INTO students (name, age) 
VALUES ('David', 24);
```



These are some of the essential SQL commands for data science. By mastering these commands, you can efficiently manage 

and manipulate relational databases to extract meaningful insights from data.




