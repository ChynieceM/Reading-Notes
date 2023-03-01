## JavaScript Objects

1. How would you describe an object to a non-technical friend you grew up with?

An object is like a dictionary. You have a key and values for example. They key is the word and the value is the definition. 

2. What are some advantages to creating object literals?

IT advantageous to use object literals when you want tp transer a series of structured related data items in some manner, for example sending a request to the server to be put into the database. 

It is much more effecient than sending several items individually and it is easier to work with than an array, when you wnat to identify individual items by name. 

3. How do objects differ from arrays?

With an object, you can transfer several items but with an array you have to access one item at a time. 

4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.

Bracket notation provides an alternative way to access object properties. It's similar to an array, and its basically the same thing. Instead of using an index number to select a number, you are using the associated name with each members value. 

For example, If an object's property name is held in a variable, then you can't use dot notation to access the value but you can access the value using bracket notation.

5. Evaluate the code below. What does the term `this` refer to and what is the advantage to using `this`?

The `this` keyword refers to the current object the code is being written inside. This enables you to use the same method definition for every object you create. 

## Intro to the DOM

1. What is the DOM?

The doument object model is the data representation of the object that comprise the structure and content of a document on the web.  It is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; the way programming languages can interact with the page 

2. Briefly describe the relationship between the DOM and JavaScript.

The DOM is not a programming language but without it, the JavaScript landuage wouldn't have any model or notion of web pages, HTMl documents, SVG documents, and their component parts. 

The document as a whole are parts of the document object model for that document. They can all be access and manipulated using the DOM and a scripting language like JavaScript. 

For example, if thinking about the DOM and JavaScript as a puppet. The strings are the document object and the instructions are the DOM. The DOM is just a model. 