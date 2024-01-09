# *Course 401, Entry Prep*

## SQL

Structured Query Language (SQL) is considered the most popular database programming language. SQL is a relational database. A relational database contains tables with fixed columns. Identicle columns might be found across related tables. Relational Database Management Systems (RDBMSs) that support SQL include Oracle, SQL Server, MySQL, Sybase, and PostgreSQL.

Note, keywords are by conventional capitialized for ease of reading.

### Basic Command Keywords

+ INSERT = add
+ SELECT = retrieve
+ DELETE = delete
+ UPDATE = update

### Data Types

+ VARCHAR - Character strings
+ INTEGER - numbers
+ DATE - dates

### Operators

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

### SQL Commands

---

#### CREATE DATABASE

Creates a new Database.

```CREATE DATABASE name```

#### CREATE TABLE

Creates a new table within a given database.

```CREATE TABLE table_name ( column1_name data_type, column2_name, data_type, ...)```

Example:

```CREATE TABLE users ( id INTEGER PRIMARY KEY, username VARCHAR(255), password VARCHAR(255) )```

In this example, "INTEGER PRIMARY KEY" is the data type.

In addition, the "IF NOT EXISTS" can be added after "CREATE TABLE" to conditionally create.

#### INSERT INTO

Inserts a new data row into a table.

```INSERT INTO table_name (column2_name, column3_name) VALUES ('values2', 'values3)```

Example:

```INSERT INTO users (username, password) VALUES ('username', 'password')```

#### UPDATE

With update, the values of one or many can be updated. 

```UPDATE table_name SET column1 = value_or_expr, column2 = another_value_or_expr WHERE condition```

#### ALTER TABLE

Similar to insert, used to modify existing table columns. Changes will be applied to both existing **and** new rows.

```ALTER TABLE table_name ADD column1 DataType DEFAULT default_value;```

```ALTER TABLE table_name DROP column_to_be_deleted```

```ALTER TABLE table_name RENAME TO new_table_name```

#### SELECT

Used to query data from a table. Additionaly, "WHERE" followed by the column name and set value will further filter the results. Anything following "WHERE" is a conditional statement.

```SELECT * FROM table_name WHERE coumn1_name = 'value1'```

#### DELETE FROM

Deletes data enteries from a table based on a specified query. The information after the "WHERE" is a conditional statement.

```DELETE FROM table_name WHERE column1_name = 'value1'```

#### DROP TABLE

In the rare case that it is desireable to delete a table entirely (CAUTION! BEST TO AVOID!), use "DROP TABLE".

```DROP TABLE table_name```

#### INNER JOIN and ON

Combines rows from two or more tables by a common column. Combining with "ON", specific rows from the two tabels can be selected for joining. 

```SELECT column1_name, column2_name FROM table1 INNER JOIN table2 ON table1.id = table2.id```

#### DISTINCT

Using the DISTINCT keyword, rows with specific coumns can be selected down. Will discard duplicates

```SELECT DISTINCT column1_name, column2_name, FROM mytable WHERE condition(s);```

#### ORDER BY

Use the "ORDER BY" keyword to sort results in ascending or descending order, ASC or DESC suffix, respectively.

#### LIMIT and OFFSET

By using "LIMIT" and "OFFSET", the number of results can be limited and starting point can be set, respectively.

```LIMIT num_limit OFFSET num_offset```

### Table Data Types

![Screenshot_2024-01-01_21-58-49](https://github.com/Bradley-Hower/reading-notes/assets/139923955/441e600a-019c-4022-b376-52a5157ec183)

### Table Constraints

![Screenshot_2024-01-01_21-59-07](https://github.com/Bradley-Hower/reading-notes/assets/139923955/2cafe7ff-7616-4e9b-b7eb-716823be3e52)

### SQL Lessons 1 - 6 Screenshots

![Screenshot_2024-01-01_19-51-03](https://github.com/Bradley-Hower/reading-notes/assets/139923955/f2c6aae2-f441-4a0b-8412-c5e02c38723e)
![Screenshot_2024-01-01_19-40-48](https://github.com/Bradley-Hower/reading-notes/assets/139923955/b5c12e60-f076-42cb-aeed-416b8587743c)
![Screenshot_2024-01-01_19-17-42](https://github.com/Bradley-Hower/reading-notes/assets/139923955/244695f5-58c9-4df6-b7c0-f4d19f4901c0)
![Screenshot_2024-01-01_18-50-43](https://github.com/Bradley-Hower/reading-notes/assets/139923955/783c5cc9-db7a-4fd8-9dcc-5688b4ef3e46)
![Screenshot_2024-01-01_18-42-22](https://github.com/Bradley-Hower/reading-notes/assets/139923955/5638aebe-b21d-40d1-8d5b-94aee65a22f2)
![Screenshot_2024-01-01_18-35-36](https://github.com/Bradley-Hower/reading-notes/assets/139923955/a3e1244b-62f1-4eae-801f-353c191edca4)

### SQL Lessons 13 - 18 Screenshots

![Screenshot_2024-01-01_22-17-24](https://github.com/Bradley-Hower/reading-notes/assets/139923955/e0bff2d6-148e-4c77-881a-e25495c8c031)
![Screenshot_2024-01-01_22-14-09](https://github.com/Bradley-Hower/reading-notes/assets/139923955/40951f6f-6071-498c-b4ae-cc00fd3d3424)
![Screenshot_2024-01-01_22-02-21](https://github.com/Bradley-Hower/reading-notes/assets/139923955/a963cef7-61dc-4896-a330-e6a061b9acc1)
![Screenshot_2024-01-01_21-52-41](https://github.com/Bradley-Hower/reading-notes/assets/139923955/fcc6819e-517d-49dd-b82b-db118dbdf7c2)
![Screenshot_2024-01-01_21-50-36](https://github.com/Bradley-Hower/reading-notes/assets/139923955/caa6ebe8-d1c1-41d7-b500-93c235ef8230)
![Screenshot_2024-01-01_21-38-46](https://github.com/Bradley-Hower/reading-notes/assets/139923955/3cab0ed8-5bf9-4d1e-826b-3af0861d0401)

## Command Line

### Terminology

Ternminal - A terminal is a text-only input and output window. Terminals on a GUI are technically terminal emulators.

Console - A physical terminal with controls and a window.

Shell - The command-line interpreter. Sits on top of the kernal. Takes in user command and convertering them to system calls to interact with the kernal. The ```echo $SHELL``` command prints the shell in use.

![0_Vb7H3gT2TbqMwtGC](https://github.com/Bradley-Hower/reading-notes/assets/139923955/d6305326-9bd2-46e4-8c57-c0cd0ee1390d)

Command Line - Open area in terminal, after the prompt which accepts user inputs.

![Screenshot_2024-01-05_14-01-09](https://github.com/Bradley-Hower/reading-notes/assets/139923955/ae2da957-7b7a-48fb-b9f2-8e1cbf89e141)

### Terminal Commands

pwd - Print Working Directory.

ls [options] [location] - Lists out all subdirectories.

ls -l - The "-l" here is the option to print the long listing.

![Screenshot_2024-01-05_14-35-29](https://github.com/Bradley-Hower/reading-notes/assets/139923955/fb289f73-1b2f-44b1-9e44-e8b02fb1dc1c)

ls -l /etc - The "/etc" lists the directory contents instead of the current directory.

ls -a - Lists all files, including hidden ones.

cd - Change directory. No arguments defaults to home.

### Paths

The two types of paths are absolute and relative. As a hierarchical structure, root is the beginning, marked as "/". Directories are separated with subsequent forward slashes. Paths can either be fully listed out, absolute, or entered using shorthand, relative.

~ - Shorthand for home directory.

. - Shorthand for current directory.

.. - Shorthand for parent directory.

### Nature of Linux

Everything is a file. Even folders and hardware. Additionally, there are no extensions. Linux looks inside the file to determine. To probe what a file is, use ```file [path]```.

Caution, Linux is case-sensitive.

When moving files with spaces, use quotes or "\" prior to the space.

Hidden files are marked by a "." prefix.

### Manugal Pages

```man <command to look up>```

man -k [search term] - Does a query search in manual pages. To search within a current manual page, use "/[search term] Press n' if there are multiple pages.

### File Manipulation

mkdir -p - Makes a directory and any parent directories as needed. If listing out a directory with folders and subfolders, all the folders along the way will be created.

mkdir -v - Prints out what actions are being done by the system when running mkdir.

rmdir - Removes a directory. Also supports, "-p" and "-v" options. The directory must be empty.

touch - Creates a file. Also can be used to modify properties.

cp [source] [destination] - Copy.

cp -r - Recrusive copy. Copies all children of a destination.

cp -i - Interactive option prompts if a copy will result in an overwrite.

rm - Removes a file.

rm -r - Recursively removes file and children also.

rm -r -i - Allows one to select which files and diretories to remove.

mv [source] [destination] - Moves a file. Changing the name can be accomplished by extending destination directory with new name.

## Command Line Activity #1 - Navigation

**Observations:**

Having used all of these before in previous Code Fellows courses, the activity was not new. It was great to get a refresher on terminology though. It is surprising how many files are listed out when running a ls on system directories.

## Command Line Activity #2 - More About Files

**Observations:**

When running "file" on a folder, it indicates it is a directory. Makes sense. When I run "file" on an image it prints out some useful information, such as resolution. I think I will probably use this in the future. I made the mistake at first of using a capital F'. I will have to watch out for this in the future.

## Command Line Activity #3 - Manual Pages

**Observations:**

A great tool to dig into the command line entries. I ran it on 'ls' and was blown away how many there are. Looking through it though, most of these are just to offer alternative formatting on the printout. I ran this on 'cp' and saw some great options to avoid overwriting a file when copying.

## Command Line Activity #4 - File Manipulation

**Observations:**

Fantastic. I have wanted to know well how to do file management in the terminal. I haven't bothered before, but after seeing my last instructor so easily create and manipulate files, I see how much faster it can be. The renaming will take a little getting used to. Hopefully I will remember the recursive and interactive options.

Table Images Source: https://sqlbolt.com/lesson/creating_tables
Kernal Structure Image Source: https://medium.com/analytics-vidhya/difference-between-terminal-console-shell-and-command-line-2441322b9b90


## Engineering Readings

### Act like you make $1000/hr

+ Spend less time on low-quality activities
+ Say yes to less
+ Don't just be busy
+ Value high productivity

### How to think like a programmer

+ Be a more efficient problem solver
+ Don't use brute-force solutions
+ Use a framework
+ Break down big problems into smaller ones

The Process

1. Understand - Know what is being requested. Be able to explain in plain English.
2. Plan - Set yourself out a step-by-step to reach the goal.
3. Divide - Break it down into smaller parts, then connect the dots.
4. Retrace - Go back over your steps and see where you went wrong. Sometimes, start over.
5. Practice - Find an outlet to solve problems.

Among this 70% of the 30 minutes to solve a problem should be spent thinking or brainstorming about it in some way, not writing code.

### Solving Problems

+ Read the problem carefully. Be able to explain it to someone else.
+ Solve it manually.
+ Optimize the manual steps.
+ Write pseudo-code.
+ Replace pseudo-code with code.
+ Optimize code.


### The 5 Whys

The 5 whys technique was developed by Sakichi Toyoda, the founder of Toyota, in the 1930s. The concept is to deeply understand what is actually happening in order to solve the problem, rather than thinking you understand.

How does it work? Ask why five times. Dig deeper with each question.

Tips

+ Might not be suitable for complex problems that require a wholistic view.
+ Move quickly so as to not develop a solution too quickly.
+ Don't keep drilling if the you reach the end of productive answers.

### The Super Mario Effect

+ Gamify how you solve problems.
+ When you fail, don't think of it as "Game Over"
+ See different ways to enjoy the process.
+ Look at the positives.



### Questions

#### What’s the one thing I bring to this career (and a potential employer) that nobody else can?

I have a unique talent at solving complex problems. And, with enough bandwidth, will figure out how to solve any problem that I may have not seen before. This is all due to my persistence.

##### What are 3 things I’ll start doing to “un-stick” myself whenever I get stuck on tough piece of code, logic, or feature?

Take a break. Break it down into smaller pieces. Ask for help.
