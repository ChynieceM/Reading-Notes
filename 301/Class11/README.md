## Nosql vs SQL

Fill in the chart below with five differences between SQL and NoSQL databases:

SQL Databases:
-Relational Databases (RDBMS)
-Table-based, with rows and predefined schema
-Vertically scalable, increased capacity by boosting hardware of a single server
-SQL (Structured Query Language), powerful for defining and manipulating data
-MySql, Oracle, Sqlite, Postgres, MS-SQL

NoSQLDatabases:
-Non-relational or Distributed Databases
-Key-value pairs, documents, graph databases, or wide-column stores with dynamic schema for unstructured data
-Horizontally scalable, scaled by adding more servers to the pool
-UnQL (Unstructured Query Language), syntax varies from database to database
-MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j, CouchDb

1. What kind of data is a good fit for an SQL database?
Complex queries: SQL databases are suitable for complex query intensive environments. The SQL query language is powerful, providing rich and versatile query capabilities.

Transactional data: SQL databases are well-suited for heavy-duty transactional type applications. They provide robust and reliable mechanisms to ensure the atomicity and integrity of data.

Structured data: SQL databases work best with structured data where a predefined schema can be determined. The data is typically represented in the form of tables with a fixed number of rows and columns.

Vertical scalability requirements: SQL databases are vertically scalable, meaning they can handle increasing loads by boosting the capabilities (CPU, RAM, SSD, etc.) of a single server.

2. Give a real world example.
An online retailer keeping track of customer information, product information, and order information. 
-Customers table: Each row represents a different customer, with columns for customer ID, name, address, etc.
-Products table: Each row represents a different product, with columns for product ID, name, description, category, and price.
-Orders table: Each row represents a different order, with columns for order ID, customer ID (relating to the Customers table), date/time of order, and shipping information.

3. What kind of data is a good fit a NoSQL database?
Large data sets (Big Data), Hierarchical data, Scalability needs: In terms of scalability, NoSQL databases are horizontally scalable. They are designed to easily add more servers to the database infrastructure to handle increased traffic, Non-complex queries, Non-transactional applications or those with flexible consistency requirements.

4. Give a real world example.
-Twitter handles massive amounts of unstructured data every second, including tweets, user information, images, and more.
User Data: Twitter could use a Document Store NoSQL database like MongoDB to store user profile data. 
Tweets: Tweets could also be stored in a document store, with information like the tweet content, timestamp, author, and associated media.

5. Which type of database is best for hierarchical data storage?
-NoSQL databases are typically a better fit for hierarchical data storage. This is because many NoSQL databases natively support formats that easily map to hierarchical structures.

6. Which type of database is best for scalability?
When it comes to scalability, both SQL and NoSQL databases can be scaled, but they do so in different ways and are suited to different scenarios.Traditional SQL databases are typically scaled vertically, which means adding more resources (such as CPU, RAM, or storage) to a single machine to handle more load. NoSQL databases are typically designed to scale horizontally, meaning that they distribute the data across multiple machines or servers. 

## sql nosql (video)
1. What does SQL stand for?
Structured query language
2. What is a relational database?
A relational database is a type of database that organizes data into tables consisting of rows and columns, with relationships between the tables. 

3. What type of structure does a relational database work with?

A relational database works with a structured data model. The data in a relational database is organized into tables, which have a predefined structure consisting of rows and columns.

4. What is a ‘schema’?
The structure of a relational database is defined by the table schema. The schema specifies the names of the tables, the names and data types of the columns within each table, and any constraints or rules that govern the data.

5. What is a NoSQL database?
A NoSQL database, often referred to as "not only SQL," is a type of database management system that differs from traditional relational databases. NoSQL databases are designed to handle large volumes of unstructured, semi-structured, or varying data types more efficiently and at scale.

6. How does it work?
NoSQL databases prioritize scalability, flexibility, and performance for handling large-scale and diverse data sets. They are often used in scenarios where traditional relational databases may face challenges, such as high-volume data storage, real-time analytics, and distributed systems.

7. What is inside of a MongoDB database?
Inside a MongoDB database, data is organized into collections, which are analogous to tables in a relational database. A MongoDB database can contain one or more collections, and each collection contains multiple documents.
 MongoDB databases store data in a flexible and schema-less manner, using collections to organize documents. This allows for easy adaptation to evolving data requirements and supports the storage of diverse and unstructured data.

8. Which is more flexible - SQL or MongoDB? and why.
SQL databases offer a more rigid and structured approach with a predefined schema, ensuring data integrity and supporting complex relationships and queries. On the other hand, MongoDB provides a higher degree of flexibility with a dynamic schema, accommodating evolving and diverse data models. MongoDB's flexible structure and horizontal scalability make it suitable for scenarios where schema changes are frequent or when handling unstructured or semi-structured data. However, SQL databases are better suited for complex relationships, enforcing data integrity, and handling sophisticated query operations

9. What is the disadvantage of a NoSQL database?
-Limited Querying Capabilities
-Lack of Standardization: NoSQL databases come in various types and implementations, each with its own query language, APIs, and data manipulation mechanisms.
-Weaker Data Consistency
-Limited ACID Transactions: ACID (Atomicity, Consistency, Isolation, Durability) transactions, which ensure data integrity and consistency
-Steeper Learning Curve: NoSQL databases, with their flexible data models and varying implementation details, can have a steeper learning curve compared to traditional SQL databases
