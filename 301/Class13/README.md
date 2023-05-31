## CRUD Basics

1. Which HTTP method would you use to update a record through an API?
The HTTP method you would use to update a record through an API is PUT or PATCH as per the CRUD (Create, Read, Update, Delete) operations.

PUT: This method is used when you want to update the entire resource with the new data. It's a complete replacement of the resource.

PATCH: This method is used when you want to apply a partial update to the resource, like changing just one field.


2. Which REST methods require an ID parameter?
GET: When used to retrieve a specific resource, as opposed to a collection of resources.

PUT or PATCH: When updating a specific resource. These methods need to know which specific resource to update.

DELETE: When deleting a specific resource. The API needs to know which specific resource to remove.

## Speed Coding: Building a CRUD API (Watch a Twitch streamer code an Express API in 20 minutes!)

1. What’s the relationship between REST and CRUD?
They have a relationship in the sense that they often map onto each other when it comes to the operations they perform on data.

Create -> POST
Read -> GET
Update -> PUT/PATCH
Delete -> DELETE

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?

1. Plan Your API: Determine the data your API will need to handle and the types of operations it will need to support. 

2. Set Up Your Server: Choose your technology stack. This could be Node.js with Express, Python with Django or Flask, Ruby with Rails, etc. 

3. Define Your Routes and Controllers: Create routes for your API endpoints according to the plan you made in step 1. 

4. Implement Middleware (If Needed): Middleware functions are functions that have access to the request object, the response object, and the next function in the application’s request-response cycle. 

5. Test Your API: Use a tool like Postman or cURL to test your API and ensure that it behaves as expected. 





