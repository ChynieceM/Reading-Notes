## Create Data Transfer Objects (DTOs)

Problem: Directly exposing database entities to clients can cause several issues:

Potential for revealing sensitive properties.
Risk of circular references.
Payloads can become unnecessarily large.
Over-posting vulnerabilities.
Tightly coupling the service layer with the database layer.
Sending nested object graphs that are complex for clients.
Solution: Introduce a Data Transfer Object (DTO).

Purpose of DTO: Defines the structure of data sent over the network.
Allows you to reshape data before sending to clients.
Implementation:

Two DTO classes were added for the Book entity: BookDto and BookDetailDto.
BookDto has properties: Id, Title, AuthorName.
BookDetailDto is more detailed with properties: Id, Title, Year, Price, AuthorName, Genre.
GET methods in BooksController were replaced to return DTOs.
Uses LINQ Select to transform Book entities to DTOs.
SQL is auto-generated by Entity Framework based on LINQ statement.
Example: SQL statement for GetBooks method joins Books and Authors tables.
The PostBook method was also modified to return a DTO after creating a new book.
Example Code:

BookDto and BookDetailDto class definitions.
Modified GetBooks and GetBook methods in BooksController to use DTOs.
SQL representation of the GetBooks LINQ query.
Modified PostBook to return BookDto after creating a new book.
Significance:
Using DTOs can enhance API security, efficiency, and flexibility by ensuring clients receive only the necessary data in an appropriate format. It also decouples your application's layers, fostering better maintainability.

## How to use Data Transfer Objects

Definition and Context

A Data Transfer Object (DTO) is essentially a container used to encapsulate data and move it between different application layers. It is usually an instance of a POCO (plain old CLR object).
Commonly found in the service layer, returning data to the presentation layer.
Advantages of DTOs

Decoupling: Allows clients to remain decoupled from internal data structures.
Abstraction: Abstracts domain objects from the user interface, making it easier to make changes to different layers without affecting others.
Data Hiding: Ensures only the necessary data is exposed. For instance, hiding salary details while exposing basic employee information.
Implementation in ASP.NET Core 3.1

You need Visual Studio 2019.
Steps to create a new ASP.NET Core API project in Visual Studio 2019 are provided.
In the project, you can define your main classes (e.g., Employee) and the associated DTOs (e.g., EmployeeDTO) that limit the properties exposed.
Reasons for Using DTOs

Avoid exposing internal structures: Sending data directly from models to presentation layers exposes internal data structures, a major design flaw.
Facilitates API, MVC applications, and Messaging patterns: DTOs are particularly beneficial for bandwidth-constrained mediums.
DTOs for Immutability: DTOs should ideally be immutable. This ensures that the receiver of the data doesn't modify it post-receipt.
Immutability can be achieved using ReadOnlyCollection, thread-safe immutable collection types, or record types in C# 9.
Serialization Challenges with DTOs: Care must be taken when serializing DTOs, especially when objects reference multiple other objects. Lazy or asynchronous loading can help to only load necessary entities.
Use Cases

An example is provided where an Employee model contains sensitive information like salary details. By using an EmployeeDTO, one can limit the data sent to just the Id, FirstName, LastName, and Department Name.
DTO Serialization

DTOs need to be serialized and deserialized effortlessly for network transfer.
Complex object relationships can lead to challenges during serialization.
Lazy loading or asynchronous loading can address these challenges.
Characteristics of DTOs

DTOs typically lack business logic and only carry data.
Immutability is a desired feature of DTOs.
Further Information

