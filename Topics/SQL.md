# SQL Structured Query Language

1. **What is an ERD?**

   Entity Relationship Diagram, describes interrelated things of interest in specific domain of knowledge.

2. **What is a primary key?**

   It represents a unique value in a table which is used to create relationship between other attributes in the same table. It also works as a reference in other table which is called foreign key. 
   
   The main difference between primary key and foreign key is that foreign key can be duplicated in the same row and can contain null values. 

3. **What is a foreign key?**

   Foreign key represents a link to a primary key in other table 

4. **Explain Normalization.**

   Normalization is a database design technique that reduces data redundancy and eliminates undesirable characteristics like Insertion, Update, deletion, anomalies. Normalization rules divides larger tables into smaller tables and links them using relationships. The purpose of Normalization in SQL is to eliminate redundant (repetitive) data and ensure data is stored logically.

   ##### **1NF (First Normal Form) Rules**

   - Each table cell should contain a single value.
   - Each record needs to be unique.

   ##### 2NF (Second Normal Form) Rules

   - Rule 1- Be in 1NF
   - Rule 2- Single Column Primary Key that does not functionally dependent on any subset of candidate key relation

   ##### 3NF (Third Normal Form) Rules

   - Rule 1- Be in 2NF

   - Rule 2- Has no transitive functional dependencies

     

5. **What command would you use if you want to create a table?**

   ```sql
   CREATE TABLE tableName; 
   ```

   

6. **What command would you use if you want to add a column to a table?**

   ````SQL
   ALTER TABLE tableName
   ADD columnName type; 
   ````

   

7. **What command would you use if you want to delete a row of data?**

   ````sql
   DELETE FROM tableName
   WHERE condtion = true; 
   ````

   

8. **What command would you use if you want to insert data into a table?**

   ```sql
   INSERT INTO tableName
   (
       ColumnNames...
   )
   VALUES
   ('Name', 'adress', 'birthday')
   ```

   

9. **What are DML, DDL, DCL and TCL?**

   DML - Data Manipulation language 

   The SQL commands that deals with the manipulation of data present in the database belong to DML

   INSERT, UPDATE, DELETE, LOCK etc.

   

   DDL - Data Definition Language

   consists of the SQL commands that can be used to define the database schema.

   CREATE, DROP, ALTER, TRUNCATE, RENAME etc.

   

   DCL - Data Control Language 

   DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system.

   GRANT, REVOKE

   

   TCL - Transaction Control Language 

   COMMIT, ROLLBACK, SAVEPOINT

   

10. **If you wanted to select only the top 10 highest earners in a table of millionaires, what query would you write?**

    ````SQL
    SELECT TOP 10 earnings
    FROM Milionairs
    ORDER BY earnings DESC;
    ````

    

11. **What is a wildcard?**

    A wildcard character is used to substitute one or more characters in a string.
    
    % zero or many 
    
    _ one 
    
    [abc] any character in brackets 

12. **What is concatenation (with example)**

    > Connection of two strings 
    >
    > ```sql
    > SELECT 
    > firstname + " " + lastname AS "name"
    > FROM Customers;
    > ```

13. **What query would I write if I want to find out all customers who do not have city listed in a table**

    ````sql
    SELECT CustomerID
    FROM Customers
    WHERE City IS NULL;
    ````

    

14. **What does the arithmetic operator % do?**

    One or many characters

15. **What does NULL mean?**

    Represents that value does not exists. 

16. **Can a primary key be NULL?**

    No

17. **How do I select all the values starting with the letter C?**

    ````sql
    SELECT * 
    FROM Customers 
    WHERE CustomersName LIKE 'C%'
    ````

    

18. **What were all the Date Functions covered?**

    `DATE, DATETIME, DATEDIFF, CHARINDEX, LEFTTRIM, RIGHTTRIM`

19. **What were all the Aggregate functions covered?**

    `COUNT(), AVG(), SUM(), MIN(), MAX()`

20. **What were all the string functions covered?**

    `TRIM, CHARINDEX, UPPER, LOWER`

21. **When is the GROUP BY keyword used?**

    The `GROUP BY` statement groups rows that have the same values into summary rows, like "find the number of customers in each country".

22. **What is the HAVING keyword?**

    The `HAVING` clause was added to SQL because the `WHERE` keyword cannot be used with aggregate functions.

23. **Why can't a column alias be used in the GROUP BY clause?**

    Due to the processing sequence of SQL 

24. **Difference between UNION and UNION ALL?**

    The `UNION` operator is used to combine the result-set of two or more `SELECT` statements.
    
    The `UNION` operator selects only distinct values by default. To allow duplicate values, use `UNION ALL`

25. **What is the difference between all the difference between all the different joins?**

    - `(INNER) JOIN`: Returns records that have matching values in both tables
    - `LEFT (OUTER) JOIN`: Returns all records from the left table, and the matched records from the right table
    - `RIGHT (OUTER) JOIN`: Returns all records from the right table, and the matched records from the left table
    - `FULL (OUTER) JOIN`: Returns all records when there is a match in either left or right table

    