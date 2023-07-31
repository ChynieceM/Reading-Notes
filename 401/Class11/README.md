## Data Models (Review the DB Schema)

1. Do some research on what a Database Schema is.
- What is a Schema?
A database schema is the skeletal structure that represents the logical view of the entire database. It defines how the data is organized and how the relations among them are associated. It formulates all the constraints that are to be applied on the data.

- Why do we use them?
- Structure: They define the structure in which data is stored, which helps in efficient data retrieval and data manipulation.
- Data Consistency: They ensure that all the data in the database adheres to a certain set of consistent rules, aiding in data integrity.
- Relation Representation: Schemas allow us to visualize the relationships between different data types in the database, such as tables and views.
- Query Optimization: With a defined schema, databases can optimize query processing.

- What do they look like?
A database schema is usually represented by a diagram known as an Entity-Relationship (ER) diagram, which depicts the various entities, their attributes, and the relationships among these entities. For example, a schema for a simple database holding customer information might include a 'Customers' table with fields like 'FirstName', 'LastName', 'Address', etc. and a 'Orders' table with fields like 'OrderID', 'CustomerID', 'Product', 'Quantity', etc. There would also be a line or arrow connecting 'Customers' and 'Orders' to indicate the relationship between these two entities.

2. What are the different types of Database Keys?
 Database keys are used to distinguish and establish relationships between rows and tables. They are a set of column(s) that are used for specific purposes.

- What is a Primary Key?
A primary key is a type of database key that is used to uniquely identify each record in a database table. It cannot have null values, and each table can have only one primary key. For example, in a 'Customers' table, 'CustomerID' could be a primary key as it is unique for each customer.

- What is a Foreign Key?
A foreign key is a column or group of columns in a relational database table that provides a link between the data in two tables. It is used to maintain the referential integrity of the data, and is a field in a table that is primary key in another table. For example, 'CustomerID' could be a foreign key in an 'Orders' table, linking each order to a customer.

- What is a Composite Key?
A composite key (also known as a compound key or concatenated key) is a key that consists of two or more columns to ensure uniqueness or to establish a relationship with another table. This is used when a primary key is not sufficient to uniquely identify a row. For instance, in a 'OrderDetails' table, 'OrderID' and 'ProductID' together could form a composite key.

- How are they different? When do you use 1 over the others?
Primary Key vs Foreign Key: Primary keys uniquely identify a record in the table while foreign keys are used to link two tables together. You use a primary key when you want to uniquely identify each record in a table. You use a foreign key when you want to create a link between two tables.

Primary Key vs Composite Key: A primary key is a single column that uniquely identifies a record, whereas a composite key is made up of two or more columns. You use a composite key when a single column is not sufficient to uniquely identify a record.

Foreign Key vs Composite Key: Both can be used to establish relationships between tables. A foreign key establishes a link with a primary key in another table. A composite key establishes a unique identifier when a single column is not sufficient.

1. What are Relationships in a relational database?

Relationships in a relational database describe how tables in a database are linked to each other. They are established using primary and foreign keys. Here are the main types of relationships:

- What is a 1:1 relationship?
One-to-One (1:1) relationship: This occurs when each row in one table is linked to no more than one row in another table. For example, in a school database, each student has only one student ID, and each student ID refers to only one student. This is not a common relationship type, as usually the information for both sides of the relationship could be stored in one table.

- What is a Many:Many relationship?
Many-to-Many (M:N) relationship: This occurs when multiple rows in a table can be related to multiple rows in another table. For example, in a book store database, a book can belong to many categories (like "Fiction", "Horror", "Thriller") and each category can have many books. This is usually implemented with a third, junction table, because most relational databases cannot directly accommodate this relationship.

- How about a 1: Many or a Many:1?
This is the most common type of relationship. In a 1:M relationship, one row in a table can be related to many rows in another table. For instance, a single customer can place many orders, so there's a 1:M relationship between customers and orders. The reverse perspective would be a M:1 relationship, from the perspective of the orders: many orders can be related to one customer.

- the "1" side of the relationship often holds the primary key, while the "Many" side would have a foreign key pointing to the "1" side's primary key.