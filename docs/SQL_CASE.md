# SQL CASE

The SQL CASE clause is used to specify conditions in a SELECT, UPDATE, or DELETE statement. It allows you to perform different actions based on different conditions.

Here is an example of how to use the CASE clause in a SELECT statement:

```sql
Copy code
SELECT column1, column2,
    CASE
        WHEN column3 > 0 THEN 'positive'
        WHEN column3 = 0 
        THEN 'zero'ELSE 'negative'
    END as status
FROM table1
```

In this example, the CASE expression is used to evaluate the value of column3 in each row of the table1. If column3 is greater than 0, the value 'positive' will be displayed in the "status" column. If column3 is equal to 0, the value 'zero' will be displayed. Otherwise, the value 'negative' will be displayed.

You can also use the CASE clause in an UPDATE statement to update different values based on different conditions:

```sql
UPDATE table1
SET column1 = value1,
    column2 = value2,
    column3 =
        CASE
            WHEN column4 > 0 THEN value3
            ELSE value4
        END
WHERE condition
```

In this example, the CASE expression is used to evaluate the value of column4 in each row of the table1. If column4 is greater than 0, the value of column3 will be updated to value3. Otherwise, it will be updated to value4.

You can also use the CASE clause in a DELETE statement to delete rows based on different conditions:

```sql
DELETE FROM table1
WHERE
    CASE
        WHEN column1 = value1 THEN column2 = value2
        ELSE column3 = value3
    END
```

In this example, the CASE expression is used to evaluate the value of column1 in each row of the table1. If column1 is equal to value1, the row will be deleted if column2 is equal to value2. Otherwise, the row will be deleted if column3 is equal to value3.

The CASE clause is often used in conjunction with the THEN and ELSE clauses to create conditional statements in SQL. It allows you to perform different actions based on different conditions, making it a powerful tool for manipulating and querying data in a database.

  

[For more info, go to the w3school tutorial]([https://www.w3schools.com/sql/sql\_case.asp](https://www.w3schools.com/sql/sql_case.asp))
