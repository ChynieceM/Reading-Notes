
## API Best Design Practices

1. REST stands for Representational State Transfer.
2. REST APIs are designed around a resource.
3. An identifier of a resource is a URI (Uniform Resource Identifier). For example, in the URI "https://www.example.com/books/1", "1" is the identifier of the resource "book".
4. The most common HTTP verbs are GET, POST, PUT, PATCH, and DELETE.
5. URIs should be based on the resources they identify.
6. A good URI is one that is easy to read and describes the resource it identifies. For example, "https://api.example.com/products" is a good URI for a resource that lists all the products.
7. A 'chatty' web API is one that requires multiple requests to perform a single operation. This is generally considered a bad thing as it can result in slower performance and increased network traffic.
8. A successful GET request returns a status code of 200 (OK).
9. An unsuccessful GET request returns a status code of 404 (Not Found).
10. A successful POST request returns a status code of 201 (Created).
11. A successful DELETE request returns a status code of 204 (No Content).