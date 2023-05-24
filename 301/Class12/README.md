## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:

100’s =  Informational
200’s =  Success
300’s = Redirection
400’s = Client Error
500’s = Server Error
2. What is a status code 202?
The status code 202, "Accepted," is often used for asynchronous processing. It indicates that the client's request was valid, but its processing will finish sometime in the future. 

3. What is a status code 308?
 The status code 308 is used for permanent redirects. When a server responds with a 308 status code, it instructs the client to use another URL to access the requested resource and to not use the current URL anymore

4. What code would you use if an update didn’t return data to a client?
If an update operation doesn't return any data to the client, the appropriate status code to use is 204 No Content.

The status code 204 indicates that the server has successfully processed the request and there is no content to send back in the response body.

5. What code would you use if a resource used to exist but no longer does?
If a resource used to exist but no longer does, the appropriate status code to use is 410 Gone.

The status code 410 indicates that the requested resource is permanently gone and will not be available again. 

6. What is the ‘Forbidden’ status code?
The "Forbidden" status code is represented by the status code 403 in the HTTP specification.

The status code 403 Forbidden indicates that the client has been authenticated and successfully communicated with the server, but it lacks the necessary permissions to access the requested resource. 

## Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
We need to pull our MongoDB database string out of our server and put it into our .env file for security and flexibility reasons. Storing sensitive information like database credentials in code files can pose security risks, especially if the code is shared or version controlled. By using environment variables stored in a separate .env file, we can keep our sensitive information separate from the codebase and ensure that it is not exposed unintentionally.

2. What is middleware?
Middleware refers to functions or code snippets that are executed in the middle of the request-response cycle in web applications. It sits between the incoming request and the final route handler and performs various operations such as request parsing, authentication, logging, error handling, and more.

3. What does app.use(express.json()) do?
 This is a middleware function in Express.js that parses incoming requests with JSON payloads. It allows the application to automatically parse the request body if the request header contains the Content-Type of application/json. This middleware parses the JSON data and attaches it to the request.body property, making it accessible for further processing in route handlers.
4. What does the /:id mean in a route?
In a route, /:id represents a route parameter in Express.js. It is a placeholder that captures a specific value from the requested URL and assigns it to the req.params object. For example, in the route /users/:id, accessing req.params.id within a route handler will provide the value captured from the URL segment.

5. What is the difference between PUT and PATCH?
PUT is used for complete replacements of a resource. When sending a PUT request, the entire resource representation should be provided in the request payload, including any fields that are not being updated. The server replaces the existing resource with the provided representation.
PATCH is used for partial updates of a resource. With a PATCH request, only the specified fields or properties that need to be updated are included in the request payload. The server applies the provided changes to the existing resource while leaving other fields unchanged.

6. How do you make a default value in a schema?
To set a default value in a schema, you can use the default property when defining the field in the schema definition.

const userSchema = new mongoose.Schema({
  name: {
    type: String,
    default: 'John Doe'
  },
  age: {
    type: Number,
    default: 30
  }
});


7. What does a 500 error status code mean?
A 500 error status code, specifically the "Internal Server Error," indicates that an unexpected error has occurred on the server while processing the request. It generally represents a server-side issue, such as a bug in the application code, unhandled exceptions, or problems with external dependencies. 

8. What is the difference between a status 200 and a status 201?
-Status 200 (OK): It indicates a successful HTTP request, meaning that the server has processed the request and returned a response with the requested resource
-Status 201 (Created): It indicates a successful creation of a resource. This status code is typically used for POST requests when a new resource is successfully created and stored on the server. 
