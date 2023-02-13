# Control Flow 

The **Control Flow** is the order in which te computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs across the extrememly frequent structures that change the contorl flow, such as conditionals and loops.

Control flow means that when you read a script, you must not only look at program structure and how it affects order of execution.

**Function**

A JS function is a block of code designed to performa a particular task.

A JS script function is executed when something invokes or "calls it"

**JS Function Syntax**

A function is defined with the `function` keyword followed by a **name**
followed by a parentheses.

Function names can contain letters, digits, underscores, and dollar signs - same rules as variables
The parentheses may include **parameter** names separated by commas.

The code to be exected by the function is placed inside curly brackets.

* Function **parameters** are listed inside the parentheses in the function definition.

* Function **arguments** are the **values** received by the function when its invoked or called. 

Inside the funtion, the arguments (the parameters) behave as local variables. 

**Function Invocation**

The code inside the functionwill execute when soemthing calls the function. 

* When an event occurs (when a user clicks a button)

* When its called from JavaScript code

* Automatically - self invoked

**Function Return**

When JS reaches a `return` statement the funcion will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after invoking the statement.

Functions often compute a **return value**. The return value is returned back to the caller. 

With functions you can reuse code: define the code once and use it many times

You can use the same code different times with different arguments to produce different results

**The () Operator Invokes the Function**

For example `toCelcius` refers to the function object, and `toCelcius()` refers to the function result

Accessing a function without an () will return the function object instead of the function result. 

**Functions used as variable values**

Instead of using a variable to store the return value of a funtion:
Ex. `let x = toCelcius(77)`

`let text = 'the temperature is' +x+ 'celcius';`

You can use the function directly, as a variable value

`let text = 'the temperature is' + toCelcius(77) + 'celcius'; `

## **Loop**

A **loop** is a  sequence of instructions that is repeated until a certain condition is met. An example would be the process of getting an item of data and changing it and then making sure some condition is checked such as if a counter has reached a prescibed number.

* Loops are one way to execute a statement for a variable a number of times. 
* The same effect can be achieved with recursion, especially in languages where all data is immutable making it impossible to update a counter variable. 

***A function is a code snippet tha can be called by other code or by itself, or a variable that refers tothe function***

A recusive funtion is a function that calls itself. 

**Control flow means that when you read a script you must not only read it from start to finish, but also look at the program structure and how it affects the order of execution**

