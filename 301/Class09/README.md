## Functional Programming Concepts

1. What is functional programming?
-Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. It emphasizes the application of functions, in contrast to the imperative programming style, which emphasizes changes in state. Functional programming languages, like Haskell, Lisp, and Erlang, are designed to support and encourage functional programming concepts.
2. What is a pure function and how do we know if something is a pure function?
A pure function is a function that meets the following criteria:
a. It always produces the same output for the same input.
b. It does not have any observable side effects, such as modifying global variables, changing the input parameters, or interacting with external systems like databases or I/O.

What is functional programming?
Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. It emphasizes the application of functions, in contrast to the imperative programming style, which emphasizes changes in state. Functional programming languages, like Haskell, Lisp, and Erlang, are designed to support and encourage functional programming concepts.

What is a pure function and how do we know if something is a pure function?
A pure function is a function that meets the following criteria:
a. It always produces the same output for the same input.
b. It does not have any observable side effects, such as modifying global variables, changing the input parameters, or interacting with external systems like databases or I/O.

To determine if a function is pure, examine its behavior and ensure that it adheres to the two criteria mentioned above. If the function consistently returns the same output for the same input and doesn't produce any side effects, then it is a pure function.

3. What are the benefits of a pure function?
a. Simplicity: Pure functions are easier to reason about, test, and debug because they don't depend on external state.
b. Reusability: Since pure functions don't depend on external state, they can be easily reused in different parts of the application.
c. Testability: Pure functions are easier to test because they don't rely on any external factors, making it easier to provide specific input and check the output.
d. Parallelism: Pure functions can be executed in parallel without the risk of race conditions or unexpected behavior, as they don't modify shared state.

4. What is immutability?
Immutability is a principle in which data or objects are not modified after they are created. Instead of changing the original data or object, new data or objects are created with the desired changes. Immutability is an important concept in functional programming, as it helps to prevent unintended side effects and makes code more predictable and easier to reason about.

5. What is Referential transparency?
Referential transparency is a property of pure functions in which a function call can be replaced with its corresponding output value without changing the behavior of the program. In other words, if a function is referentially transparent, any time it is called with the same input, it will produce the same output, and the function call can be replaced with that output value. This property simplifies the process of understanding, reasoning about, and refactoring code, as you can treat referentially transparent functions as "black boxes" without needing to know their internal implementation.

## Node JS Tutorial for Beginners #6 - Modules and require()

1. What is a module?
A module is a self-contained piece of code that encapsulates a specific functionality or a set of related functionalities. Modules help in organizing and structuring code, making it more maintainable and easier to understand. In Node.js, each file is treated as a separate module, and the functionalities can be exported from one module and imported into another module as needed.

2. What does the word ‘require’ do?
The 'require' function in Node.js is used to import the exported functionalities from another module into the current module. It is a built-in function that takes the path of the module file as its argument and returns the exported contents of that module. The 'require' function allows you to use the functionalities of other modules in your current module, enabling code reusability and modular programming.

3. How do we bring another module into the file the we are working in?
To bring another module into the file you are working in, you need to use the 'require' function. You can assign the result of the 'require' function to a variable, which will then hold the exported functionalities of the imported module.

4. What do we have to do to make a module available?
To make a module available for other modules to import, you need to export its functionalities using the 'module.exports' or 'exports' object. You can assign the functionalities you want to export to the 'module.exports' object or add them as properties of the 'exports' object.