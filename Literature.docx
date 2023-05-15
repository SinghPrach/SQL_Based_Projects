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
