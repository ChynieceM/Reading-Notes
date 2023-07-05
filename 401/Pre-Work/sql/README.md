# SQL Queries

- Structured Query Language, or SQL, is an accepted industry-standard language. It is a query language used to access a database from a language like C/C++, Java, or a web application. 

-  Used to get data out of the database. A variety of databases supports SQL. Commonly used databases include Oracle, SQL Server, MySQL, Sybase, and PostgreSQL.

Create a new Database:
`CREATE DATABASE sql_name;`

Create a Table:
`CREATE TABLE users ( id INTEGER PRIMARY KEY, username VARCHAR(255), password VARCHAR(255) );`

Insert Data into a table:
`INSERT INTO users (username, password) VALUES ('username', 'password');`

Query from a table:
`SELECT * FROM users;`

Update data into a table:
`UPDATE users SET password = 'new_password' WHERE username = 'username';`

Delete data from a table:
`DELETE FROM users WHERE username = 'username';`

## Basic SQL commands
INSERT: used to add new data to a database.

SELECT: used to retrieve data from a database.

DELETE: used to delete data from a database.

UPDATE: used to modify existing data in a database.

## Data types
VARCHAR stores character strings (such as names or addresses).

INTEGER: used to store numerical data.

DATE: used to store date values.

## Operators
AND: used to combine two or more conditions.

OR: used to specify that either of the two conditions can be true.

BETWEEN: used to specify a range of values.

## Creating tables
CREATE TABLE: used to create a new table in a database.

## Modifying tables
ALTER TABLE: used to modify an existing table in a database.

## Querying data
WHERE: used to filter the results of a SELECT statement based on specified conditions.

## Joining tables
INNER JOIN combines rows from two or more tables based on a common column.

LEFT JOIN: return all the rows from the left table and any rows from the right table that match them.

## BOLT Lessons

ex. Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;

Operator	Condition	SQL Example

- =, !=, < <=, >, >=	Standard numerical operators	col_name != 4
- BETWEEN … AND	Number is within range of two values (inclusive)	col_name BETWEEN 1.5 AND 10.5

- NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	col_name NOT BETWEEN 1 AND 10
- IN (…)	Number exists in a list	col_name IN (2, 4, 6)
- NOT IN (…)	Number does not exist in a list	col_name NOT IN (1, 3, 5)

- LIKE	Case insensitive exact string comparison	col_name LIKE "ABC"
- NOT LIKE	Case insensitive exact string inequality comparison	col_name NOT LIKE "ABCD"
- %	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")
- _	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)	col_name LIKE "AN_"
(matches "AND", but not "AN")


## Filtering and sorting Query results

- SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.

ex. Select query with unique results
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);

-  sort your results by a given column in ascending or descending order using the ORDER BY clause.
- When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value.

ex. Select query with ordered results
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;

- The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.

ex. Select query with limited rows
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;

##  Multi-table queries with JOINs

- entity data in the real world is often broken down into pieces and stored across multiple orthogonal tables using a process known as normalization

- Database normalization minimizes duplicate data in any single table, and allows for data in the database to grow independently of each other (ie. Types of car engines can grow independent of each type of car).

- Tables that share information about a single entity need to have a primary key that identifies that entity uniquely across the databas

- The INNER JOIN is a process that matches rows from the first table and the second table which have the same key (as defined by the ON constraint) to create a result row with the combined columns from both tables. After the tables are joined, the other clauses we learned previously are then applied.

ex. Select query with INNER JOIN on multiple tables
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

# Database Management

In SQL, the database SCHEMA is what describes the structure of each table, and the datatypes that each column of the table can contain.

- Example: Correlated subquery
For example, in our Movies table, the values in the Year column must be an Integer, and the values in the Title column must be a String.

- When inserting data into a database, we need to use an INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert.

ex. Insert statement with values for all columns
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;

- In some cases, if you have incomplete data and the table contains columns that support default values, you can insert rows with only the columns of data you have by specifying them explicitly.

ex. Insert statement with specific columns
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;       

- you can use mathematical and string expressions with the values that you are inserting.
This can be useful to ensure that all data inserted is formatted a certain way.

ex. Example Insert statement with expressions
INSERT INTO boxoffice
(movie_id, rating, sales_in_millions)
VALUES (1, 9.9, 283742034 / 1000000);     

##  Updating rows

Update statement with values
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;

- The statement works by taking multiple column/value pairs, and applying those changes to each and every row that satisfies the constraint in the WHERE clause.

## Deleting Rows

Delete statement with condition
DELETE FROM mytable
WHERE condition;

## Creating tables

Create table statement w/ optional table constraint and default value
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);

- The structure of the new table is defined by its table schema, which defines a series of columns. Each column has a name, the type of data allowed in that column, an optional table constraint on values being inserted, and an optional default value.

### Table Data Types 
Data type	
- INTEGER, BOOLEAN	The integer datatypes can store whole integer values like the count of a number or an age. In some implementations, the boolean value is just represented as an integer value of just 0 or 1.

- FLOAT, DOUBLE, REAL	The floating point datatypes can store more precise numerical data like measurements or fractional values. Different types can be used depending on the floating point precision required for that value.

CHARACTER(num_chars), VARCHAR(num_chars), TEXT	
The text based datatypes can store strings and text in all sorts of locales. The distinction between the various types generally amount to underlaying efficiency of the database when working with these columns.

Both the CHARACTER and VARCHAR (variable character) types are specified with the max number of characters that they can store (longer values may be truncated), so can be more efficient to store and query with big tables.

- DATE, DATETIME	SQL can also store date and time stamps to keep track of time series and event data. They can be tricky to work with especially when manipulating data across timezones.

- BLOB	Finally, SQL can store binary data in blobs right in the database. These values are often opaque to the database, so you usually have to store them with the right metadata to requery them.

### Table Constraints
Constraint

- PRIMARY KEY	This means that the values in this column are unique, and each value can be used to identify a single row in this table.

- AUTOINCREMENT	For integer values, this means that the value is automatically filled in and incremented with each row insertion. Not supported in all databases.

- UNIQUE	This means that the values in this column have to be unique, so you can't insert another row with the same value in this column as another row in the table. Differs from the `PRIMARY KEY` in that it doesn't have to be a key for a row in the table.

- NOT NULL	This means that the inserted value can not be `NULL`.

- CHECK (expression)	This allows you to run a more complex expression to test whether the values inserted are valid. For example, you can check that values are positive, or greater than a specific size, or start with a certain prefix, etc.

- FOREIGN KEY	This is a consistency check which ensures that each value in this column corresponds to another value in a column in another table.

For example, if there are two tables, one listing all Employees by ID, and another listing their payroll information, the `FOREIGN KEY` can ensure that every row in the payroll table corresponds to a valid employee in the master Employee list.

Movies table schema
CREATE TABLE movies (
    id INTEGER PRIMARY KEY,
    title TEXT,
    director TEXT,
    year INTEGER, 
    length_minutes INTEGER
);

## Altering tables

Altering table to add new column(s)
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;

- You need to specify the data type of the column along with any potential table constraints and default values to be applied to both existing and new rows.

Altering table to remove column(s)
ALTER TABLE mytable
DROP column_to_be_deleted;

- If you need to rename the table itself, you can also do that using the RENAME TO clause of the statement.

Altering table name
ALTER TABLE mytable
RENAME TO new_table_name;

## Dropping Tables 
You  may want to remove an entire table including all of its data and metadata, and to do so, you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely.

Drop table statement
DROP TABLE IF EXISTS mytable;

-  If you have another table that is dependent on columns in table you are removing (for example, with a FOREIGN KEY dependency) then you will have to either update all dependent tables first to remove the dependent rows or to remove those tables entirely.

