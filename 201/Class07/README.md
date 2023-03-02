Domain Modeling

1. Explain why we need domain modeling.

We need domain modeling so that we can verify and validate the understanding of a specific problem. 

HTML Table Basics

1. Why should tables not be used for page layouts?

- layout tables reduce ability for visually impaired users. 
- tables produce tag soup - code is harder to write, maintain, and debug
- tables are not automatically responsive - when you use a proper layout, their width default to 100% of their parent element, tables are sized accoring to their content by default.


2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.

`<td>` - table data, `<tr>` - table row, `<table>`

Introducing Constructors

1. What is a constructor and what are some advantages to using it?

A constructor is a function called using the `new` keyword. When you call a constructor it will create a new object, bind `this` to a new object so you can refer to `this` in your construct code, run the code in the constructor, and return a new object. 

This is useful so we don't have to write out the same code for every object like adding a `height` property then we have to remember to update every object. 

2. How does the term this differ when used in an object literal versus when used in a constructor?

`this` used in an object literal refers to the object being created by the literal. In a constructor function `this` refers to the instance of the object being created by the constructor.

`this` in object literals are used to define an object and `this` in a constructor is used to create an object.

Object Prototypes Using A Constructor

1. Explain prototypes and inheritance via an analogy from your previous work experience.

Just as a family tree represents the relationships b/w different family members prototypes and inheritance represent the relationships b/w different objects in JS. 

In a family tree, people inherit certain attributes and behaviors from their parents. For ex, they might inherit certain physical features like eye color and behavioral traits like personality and skills like singing. 

In JS objects can inherit properties and methods from their prototypes. 

A prototype is an object that serves as a template for other objects when an object is created it can inherit properties and methods from its prototye.

But the children are also unique and have their own attributes just as objects can have their own unique properties and methods. 