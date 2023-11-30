# *Course 301, Entry 11: MongoDB and Mongoose*

## SQL vs NoSQL

Fill in the chart below with five differences between SQL and NoSQL databases:

### SQL

+ Relational Databases
+ Table-based
+ Predefined schema
+ Vertically scalable (faster hardware)
+ Complex query capable
+ Not best fit for Hierarchical data storag
+ Very stable

### NoSQL

+ Non-relational Databases
+ Document-based, key-value pairs, graph databases, or wide-column stores
+ Dynamic schema
+ Horizontally scalable (more servers)
+ Simple query capable
+ Hierarchical data storage, big data
+ Less stable than SQL

### SQL vs SQL Summary

 **SQL**: Atomicity, Consistency, Isolation and Durability

 **NoSQL**: Consistency, Availability and Partition tolerance

----

#### What kind of data is a good fit for an SQL database?

Transactional data. For example, oOnline purchases.

#### What kind of data is a good fit a NoSQL database?

Big data. AI. For example, image matching.

#### Which type of database is best for hierarchical data storage?

NoSQL

#### Which type of database is best for scalability?

NoSQL

## Terms

### SQL

#### What does SQL stand for?

Structured Query Language

#### What is a relational database?

A database with a tables that point to each other. The same IDs are used accross multiple tables. A relational database consists of fields within a table. All tables hold same number of fields.

#### What type of structure does a relational database work with?

One-to-One: one ID to one field

One-to-Many: one ID shared by many fields

Many-to-Many: many IDs shared by many fields

#### What is a ‘schema’?

Schema are a series of data fields. This data organization is standardized - all tables have the same fields.

### NoSQL

#### What is a NoSQL database?

NoSQL is a database consisting just of tables. There is no schema. There are no relations, but relations can be set manually.

#### How does it work?

Each table holds its own data. The data is independently pulled from these.

#### What is inside of a MongoDB database?

A MongoDB database consists of documents, each holding their own data fields and entries. All information is within one place for each table.

#### Which is more flexible - SQL or MongoDB? and why

NoSQL. Database can easily be updated via horizontal or verticle scaling. Being that it is schema-less, lots of read and write queries can be run.

#### What is the disadvantage of a NoSQL database?

Duplicate data. Database has to be updated accross different tables.

## Things I want to know more about

Case examples for each database.
