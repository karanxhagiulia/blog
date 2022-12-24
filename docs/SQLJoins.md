# SQL JOINs

SQL JOINs are a crucial concept in the Structured Query Language (SQL) used to manage and manipulate relational databases. JOINs allow users to combine rows from two or more tables based on a common field between them. This allows a more comprehensive and efficient way to retrieve data from multiple tables.

There are several types of JOINs in SQL, each serving a specific purpose. The most commonly used types are **INNER JOIN, OUTER JOIN, and CROSS JOIN.**

INNER JOIN
----------

An INNER JOIN, also known as an equijoin, combines rows from two or more tables based on a common field between them. It returns only the rows that match the specified criteria. INNER JOINs are used to retrieve data from multiple tables where the data is related. For example, you can use an INNER JOIN to retrieve all the orders placed by a customer from the "Customers" and "Orders" tables based on the common field "Customer ID."

OUTER JOIN
----------

An OUTER JOIN retrieves all the rows from one table and the matching rows from the other table. If a row in one table doesn't have a matching row in the other table, it will still be included in the results with NULL values for the fields from the other table.

_There are three types of OUTER JOINs: LEFT JOIN, RIGHT JOIN, and FULL JOIN._

### LEFT JOIN

A LEFT JOIN retrieves all the rows from the left table and the matching rows from the right table. If there are no matching rows in the right table, the NULL values will be displayed for the right table's fields.

### RIGHT JOIN

A RIGHT JOIN retrieves all the rows from the right table and the matching rows from the left table. If there are no matching rows in the left table, the NULL values will be displayed for the left table's fields.

### FULL JOIN

A FULL JOIN retrieves all the rows from both tables, whether or not there is a matching row in the other table. If there are no matching rows, the NULL values will be displayed for the fields from the other table.

CROSS JOIN
----------

A CROSS JOIN combines every row from one table with every row from the other table. It is used to create a cartesian product of the two tables.

  

* * *

  

To illustrate the use of JOINs, let's consider a hypothetical database for a bookstore. The database has two tables: "Books" and "Authors." The "Books" table contains information about the books in the store, including the title, author, and price. The "Authors" table contains information about the authors, including the name and country of origin.

To retrieve a list of all the books in the store, along with the name and country of the authors, we could use an INNER JOIN like this:

```plain
SELECT Books.title, Authors.name, Authors.country
FROM Books
INNER JOIN Authors ON Books.author = Authors.id


```

This query would return a list of all the books in the store, along with the name and country of the corresponding authors.

To retrieve a list of all the books in the store, along with the name and country of the authors, even if there are no matching rows in the "Authors" table, we could use a LEFT JOIN like this:

  

```sql
SELECT Books.title, Authors.name, Authors.country
FROM Books
LEFT JOIN Authors ON Books.author = Authors.id
``
```

![image](https://user-images.githubusercontent.com/96819403/209449707-703c5d70-1d32-4c4f-8f13-373e888d2417.png)
