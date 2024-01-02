# *Course 401, Entry Prep*

## SQL

Structured Query Language (SQL) is considered the most popular database programming language. SQL is a relational database. A relational database contains tables with fixed columns. Identicle columns might be found across related tables. Relational Database Management Systems (RDBMSs) that support SQL include Oracle, SQL Server, MySQL, Sybase, and PostgreSQL.

Note, keywords are by conventional capitialized for ease of reading.

## Basic Command Keywords

+ INSERT = add
+ SELECT = retrieve
+ DELETE = delete
+ UPDATE = update

## Data Types

+ VARCHAR - Character strings
+ INTEGER - numbers
+ DATE - dates

## Operators

+ =, !=, < <=, >, >=
+ AND
+ OR
+ BETWEEN
+ NOT
+ IN - found with said column
+ LIKE - case insensitive
+ % - wildcard, zero or more characters (only used with LIKE and NOT LIKE)
+ _ - single character placeholder (only used with LIKE and NOT LIKE)

String words must be quoted to distringuish from SQL keywords.

## Commands

### CREATE DATABASE

Creates a new Database.

```CREATE DATABASE name```

### CREATE TABLE

Creates a new table within a given database.

```CREATE TABLE table_name ( column1_name data_type, column2_name, data_type, ...)```

Example:

```CREATE TABLE users ( id INTEGER PRIMARY KEY, username VARCHAR(255), password VARCHAR(255) )```

In this example, "INTEGER PRIMARY KEY" is the data type.

In addition, the "IF NOT EXISTS" can be added after "CREATE TABLE" to conditionally create.

### INSERT INTO

Inserts a new data row into a table.

```INSERT INTO table_name (column2_name, column3_name) VALUES ('values2', 'values3)```

Example:

```INSERT INTO users (username, password) VALUES ('username', 'password')```

### UPDATE

With update, the values of one or many can be updated. 

```UPDATE table_name SET column1 = value_or_expr, column2 = another_value_or_expr WHERE condition```

### ALTER TABLE

Similar to insert, used to modify existing table columns. Changes will be applied to both existing **and** new rows.

```ALTER TABLE table_name ADD column1 DataType DEFAULT default_value;```

```ALTER TABLE table_name DROP column_to_be_deleted```

```ALTER TABLE table_name RENAME TO new_table_name```

### SELECT

Used to query data from a table. Additionaly, "WHERE" followed by the column name and set value will further filter the results. Anything following "WHERE" is a conditional statement.

```SELECT * FROM table_name WHERE coumn1_name = 'value1'```

### DELETE FROM

Deletes data enteries from a table based on a specified query. The information after the "WHERE" is a conditional statement.

```DELETE FROM table_name WHERE column1_name = 'value1'```

### DROP TABLE

In the rare case that it is desireable to delete a table entirely (CAUTION! BEST TO AVOID!), use "DROP TABLE".

```DROP TABLE table_name```

### INNER JOIN and ON

Combines rows from two or more tables by a common column. Combining with "ON", specific rows from the two tabels can be selected for joining. 

```SELECT column1_name, column2_name FROM table1 INNER JOIN table2 ON table1.id = table2.id```

### DISTINCT

Using the DISTINCT keyword, rows with specific coumns can be selected down. Will discard duplicates

```SELECT DISTINCT column1_name, column2_name, FROM mytable WHERE condition(s);```

### ORDER BY

Use the "ORDER BY" keyword to sort results in ascending or descending order, ASC or DESC suffix, respectively.

### LIMIT and OFFSET

By using "LIMIT" and "OFFSET", the number of results can be limited and starting point can be set, respectively.

```LIMIT num_limit OFFSET num_offset```

## Table Data Types

INSERT IMAGE

## Table Constraints

INSERT IMAGE

## SQL Lessons 1 - 6 Screenshots

INSERT IMAGES

## SQL Lessons 13 - 18 Screenshots

INSERT IMAGES

## GIT Practice

INSERT IMAGES

Table Images Source: https://sqlbolt.com/lesson/creating_tables