Database (On SQL Server)

Database
:- an organized collection of structured information, stored and access electronically in a computer system.
:- usually controlled by a database management system.

Comparison between DBMS & RDBMS
DBMS
Data stored in file format
Individual access of data elements
No connection between data
Data in small quantity
Data redundancy is common
There is normalisation
No support for distributed DB
Supports a single user
Lower security
Lower H/W, S/W requirements
Examples: XML, MS Access
RDBMS
Data stored in table format
Multiple data elements accessible
Tables’ data are linked together
Cannot achieve Normalisation
Data in large amount
Reduced Data redundancy
Supports multiple users
Multiple layers of security
Higher H/W, S/W requirements
Examples: SQL Server, Oracle

Important Terminologies
Normalisation
Process of organizing data in a database, which includes creating tables and establishing relationship between those tables, in order to provide protection and flexibility to both data and database respectively.
Distributed Database
Collection of multiple logically interrelated databases distributed over a computer network.
Data Redundancy
Practice of keeping data in 2 or more places within a database or data storage system.
Data Integrity
Overall completeness, accuracy, and consistency of data over its entire life cycle.
By data integrity, it ensures that data-in-use, data-in-transit and data-at-rest cannot be changed by an unauthorized person or program.
Types of Data
Nominal, Ordinal, Discrete, and Continuous

Constraints
Used to limit the type of data that goes into a table.
Ensures data' accuracy and reliability in the table.
In case of violation between constraints and the data action, the action is aborted.
Column level or table level constraints
Common Constraints of SQL
NOT NULL (ensures column cannot have a null value)
UNIQUE (ensures all values in a column are different)
PRIMARY KEY (a combination of a NOT NULL and UNIQUE, which uniquely identifies each row in a table)
FOREIGN KEY (prevents actions that would destroy links between tables)
CHECK (check if values satisfy a specific condition)
DEFAULT (set a default value for a column)
CREATE INDEX (used to create and retrieve data from the database very quickly)

*** Listing all the schemas in the current database:-
SELECT * FROM sys.schemas


SQL Statements
Set of instructions consisting of parameters, variables, names, data types, and SQL reserved words that complies successfully.
Structured Query Language, for querying data in the RDBMS.
Type of SQL Statements
1. DML (Data Manipulation Language)
SELECT, INSERT, UPDATE, DELETE
2. DDL (Data Definition Language)
CREATE, ALTER, DROP
3. DCL (Data Control Language)
GRANT, REVOKE
4. TCL (Transaction Control Language)
BEGIN, TRAN, COMMIT, ROLLBACK, SAVEPOINT


SQL Expressions
Formulas written within SQL queries to perform mathematical operations on the data stored in the database.
It is a combination of one or more values, operators, and SQL functions that evaluate to a value.
Types of SQL Expressions
1. Boolean
2. Numeric
3. Date
SQL CASE Expression
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    ...
    WHEN conditionN THEN resultN
    ELSE result
END;


Alias (AS)
Temporary name given to a table or a column, just for a particular SQL query.


Schema in SQL
A collection of database objects associated with a database.
Username of a database is Schema owner.
Schema belongs to single database, while a database can have single or multiple schemas.
Syntax:
CREATE SCHEMA schema_name;
GO
""""""OR""""""
CREATE SCHEMA [schema_name] [AUTHORIZATION owner_name]
[DEFAULT CHARACTER SET char_set_name]
[PATH Schema_name[...]]
[ANSI CREATE Statements[...]]
[ANSI GRANT Statements[...]];

default schema=dbo
Advantages of using Schemas:
1. Applying security permissions to separate and protect database objects based on user access rights.
2. Also helps in adding security.
3. Helps in manipulating and accessing the objects.


Various Syntax in SQL
1. SELECT
SELECT col1, col2, col3, .. FROM table_name;
2. DISTINCT
SELECT DISTINCT col1, col2, col3, .. FROM table_name;
3. WHERE
SELECT col1, col2, col3, .. FROM table_name
WHERE CONDITION;
4. AND/OR
SELECT col1, col2, col3, .. FROM table_name
WHERE CONDITION1 AND/OR CONDITION2;
5. IN
SELECT col1, col2, col3, .. FROM table_name
WHERE col1 IN (val1, val2, val3,..);
6. BETWEEN
SELECT col1, col2, col3, .. FROM table_name
WHERE col1 BETWEEN val1 AND val2;
7. LIKE
SELECT col1, col2, col3, .. FROM table_name
WHERE col1 LIKE '%PATTERN%';
8. ORDER BY
SELECT col1, col2, col3, .. FROM table_name
WHERE CONDITION ORDER BY col1 ASC/DESC;
9. GROUP BY
SELECT col1, col2, col3, .. FROM table_name
WHERE CONDITION GROUP BY col1;
10. HAVING
SELECT col1, col2, col3, .. FROM table_name
WHERE CONDITION GROUP BY col1 HAVING (Condition);
11. COUNT
SELECT COUNT(col1) FROM table_name WHERE CONDITION;
12. CREATE INDEX
CREATE UNIQUE INDEX index_name
ON table_name (col1, col2, ... colN);
13. CREATE TABLE
CREATE TABLE table_name(
col1 datatype,
col2 datatype,
col3 datatype,
...
colN datatype,
PRIMARY KEY (one or more columns)
);
14. DROP 
DROP TABLE table_name;
DROP INDEX index_name;
15. ALTER
ALTER TABLE table_name;
ALTER INDEX index_name;
16. TRUNCATE
TRUNCATE TABLE table_name;
17. RENAME TABLE
ALTER TABLE table_name
RENAME TO new_table_name;
18. INSERT INTO
INSERT INTO table_name (col1, col2, col3, ... colN)
VALUES (val1, val2, val3, ... colN);
19. UPDATE
UPDATE table_name
SET col1=val1, col2=val2, ... colN=valN
WHERE CONDITION;
20. DELETE
DELETE FROM table_name WHERE CONDITION;
21. CREATE DATABASE
CREATE DATABASE database_name;
22. DROP DATABASE
DROP DATABASE database_name;
23. USE
USE database_name;
24. COMMIT
COMMIT;
25. ROLLBACK
ROLLBACK;


Operators
1. Arithmetic
2. Comparison
3. Logical:
ALL, AND, ANY, BETWEEN (end values are inclusive), EXISTS, IN, LIKE, NOT, OR, IS NULL, UNIQUE


Regular Expressions
a generalized expression, used to match patterns with various sequences of characters.
can be a combination of different data types
used in string searching
Patterns:-
*,+,.,?,^,$
[abc],[A-Z],[a-z]
[0-9]
p1|p2|p3
{n},{m,n}
SELECT statements WHERE field_name REGEXP


LEAD Vs LAG functions in SQL
The Lead function is used to access data from subsequent rows along with data from the current row.
The Lag function is used to access data from previous rows along with data from the current row.
An ORDER BY clause is required when working with the LEAD and LAG functions, but a PARTITION BY clause is optional.


Aggregate Functions
COUNT(),SUM(),AVG(),MIN(),MAX()


*** Basic Syntax of an SQL Query
SELECT col_name(s)
FROM table_name
WHERE condition
GROUP BY col_name(s)
HAVING condition (aggregate functions)
ORDER BY col_name(s)


Sub Queries
A query within another query, where outer query is main query and inner query is subquery.
A subquery or inner query or nested query is a query within another SQL and embedded within the WHERE clause.
A subquery is used to return the data that will be used in the main query, as a condition to further restrict the data to be retrieved.
1. Subqueries with the SELECT statement
SELECT col1, col2
FROM table1, table2
WHERE col_name OPERATOR
(SELECT col1, col2
FROM table1, table2
WHERE condition)
2. Subqueries with the INSERT statement
INSERT INTO table_name [(col1,col2,..)]
    SELECT  col1, col2,..
    FROM table table1,table2
    WHERE condition
3.Subqueries with the UPDATE statement
UPDATE table_name
SET col_name = new_value
[WHERE col_n OPERATOR (SELECT col1 FROM table_1 WHERE condition)]
4. Subqueries with the DELETE statement
DELETE FROM table_name
[WHERE col_n OPERATOR (SELECT col1 FROM table_1 WHERE condition)]


SQL Joins
INNER, LEFT, RIGHT, FULL,SELF
Syntax:
SELECT col1, col2, ...
FROM table1 a LEFT JOIN table2 b
ON a.colN = b.colN
Self Join- a regular join but the table is joined with itself.
SELECT col_name(s)
FROM table1 T1, table1 T2
WHERE condition;
T1 and T2 are different aliases for the same table.
UNION Operator
Used to combine the result-set of 2 or more SELECT statements, given they have same number of columns.
Syntax:
SELECT col_name(s) FROM table 1
UNION
SELECT col_name(s) FROM table 2 


Correlated Subquery
- Used for row-by-row processing
- Each subquery is executed once for every row of the outer query.
A correlated subquery is evaluated once for each row, processed by the parent statement. The parent statement can be a SELECT, UPDATE, or DELETE statement.
We can use a correlated subquery to answer a multiple question whose answers depend on the value in each row, processed by the parent statement.
Correlated SELECT 
SELECT col1, col2, ...
FROM table1 outer
WHERE col1 operator 
            (SELECT col1,col2
            FROM table2 
            WHERE expr1 = outer.expr2)
Correlated UPDATE 
UPDATE table1 alias1
SET col1 = (SELECT col1,col2
            FROM table 2 
            WHERE expr1 = outer.expr2)
Correlated DELETE 
DELETE FROM table1 alias1
WHERE col1 operator (SELECT col1,col2
            FROM table 2 
            WHERE expr1 = outer.expr2)
         
ACID Properties
Transaction- It is a single logical unit of work that accesses and possibly modifies the content of a database. Transactions access data using read and write operations. In order to maintain consistency in a database, before and after the transaction, certain properties are followed, which are called ACID properties.
A- Atomicity
Transaction Manager
The entire transaction takes place at once or doesn't happen at all
C- Consistency
Application Programmer
The database must be consistent before and after the transaction
I- Isolation
Concurrency Control Manager
Multiple transactions occur independently without interference
D- Durability
Recovery Manager
The changes of a successful transaction occurs even if the system failure occurs

The ACID properties, in totality, provide a mechanism to ensure the correctness and consistency of a database in a way such that each transaction is a group of operations that acts as a single uniy, produces consistent results, acts in isolation from other operations, and updates that it makes are durably stored.


Functions in SQL
1. Single Row Functions
They work on a single row and return one output per row
For example: length and case conversion functions are single row functions
2. Multiple Row Functions
They work upon group of rows and return one result for the complete set of rows.


Wildcards
Search for patterns made form literal texts, wildcard characters or a combination
Use LIKE as an operator


Views
They are kind of virtual tables, having rows and columns.
We can create a view by selecting fields from one or more tables present in the database.
A view can either have all the rows of a table or specific rows based on condition.
Syntax:-
CREATE VIEW view_name AS
SELECT col1, col2, ..
FROM table_name
WHERE condition
Deleting View: DROP VIEW view_name
Updating Views:
There are certain conditions needed to be satisfied to update a view. If any of these conditions is not met, then we will not be allowed to update the view.
1. The SELECT statement which is used to create the view should not include the GROUP BY clause or ORDER BY clause.
2. The SELECT statement should not have the DISTINCT keyword.
3. The View should have all NOT NULL values.
4. The View should not be created using Nested queries or complex queries.
5. The View should be created from a single table. In case the view is created from multiple tables, then updating the view is not possible.
Syntaxes:-
1. To add or remove fields from a view
CREATE OR REPLACE VIEW view_name AS
SELECT col1, col2, ..
FROM table_name
WHERE condition
2. To insert a row in a view
INSERT INTO view_name (col1, col2,...,colN)
VALUES (val1,val2,val3,...,valN)
3. To delete a row in a view
DELETE FROM view_name
WHERE condition

WITH CHECK OPTION
This clause is applicable to an updatable view.
It is used to prevent the insertion of rows in the view where the condition in the WHERE clause in CREATE VIEW statement is not satisfied.
If we have used the WITH CHECK OPTION clause in the CREATE VIEW statement and if the UPDATE or INSERT clause does not satisfy the condition, then they will return an error.

Uses of a view:-
A good database should contain views for the given reasons:-
1. Restricting Data Access
Views provide an additional level of table security by restricting access to a predetermined set of rows and columns of a table.
2. Hiding Data Complexity
A view can hide the complexity that exists in a multiple table join.
3. Simplify commands for the user
Views allow the user to select information from multiple tables without requiring the users to actually know how to perform a join.
4. Store Complex queries
5. Rename Columns
Without affecting the original tables.
6. Multiple View Facility
Different views can be created on the same table for different users.


Temporary (Temp) Tables
They are most likely as Permanent tables.
They are created in Temp DB and are automatically deleted as soon as the last connection is terminated.
They help us to store and process intermediate results.
They are very useful when we need to store temporary data.

To create temporary table
CREATE TABLE #EmpDetails (id INT, name VARCHAR(25))

To insert values into temporary table
INSERT INTO #EmpDetails VALUES (01,'Lalit'),(02,'Atharva')

Kinds of Temp Tables:-
1. Local Temp Table (#)
    Available only for the session that has created it.
2. Global Temp Table (##)
    Visible to all connections and dropped when the last connection referencing the table is closed.
  
Index
Indexes are special lookup tables that the database search engine can use to speed up data retrieval.
An index is a pointer to data in a table.
An index helps to speed up SELECT queries and WHERE clauses, but it slows down data with the UPDATE and the INSERT statements.
Indexes can be created or dropped with no effect on the data.

Creating Index:
CREATE INDEX statement allows us to name the index, to specify the table and which column or columns to index, and to indicate whether the index is in an ascending or descending order.
Syntax:
    CREATE INDEX index_name ON table_name;
Single Column Indexes:
    CREATE INDEX index_name
    ON table_name(column_name);
Unique Indexes- good for performance as well as data integrity.
Syntax:
    CREATE UNIQUE INDEX index_name
    ON table_name(column_name);
Composite Indexes (Syntax):
    CREATE INDEX index_name
    ON table_name(col1,col2);
Dropping Index:
    DROP INDEX index_name;
Indexes should be avoided when:
1. Indexes should not be used on small tables.
2. Tables that have frequent, large batches update or insert operations.
3. Indexes should not be used on columns that contain a high number of NULL values.
4. Columns that are frequently manipulated should not be indexed.


