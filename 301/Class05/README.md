## React-Docs - Thinking in React

1. What is the single responsibility principle and how does it apply to components?

-a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

2. What does it mean to build a ‘static’ version of your application?
-Building a static version requires a lot of typing and no thinking, but adding interactivity requires a lot of thinking and not a lot of typing.

3. Once you have a static application, what do you need to add?
-To make the UI interactive, you need to let users change your underlying data model. You will use state for this.

4. What are the three questions you can ask to determine if something is state?
-Does it remain unchanged over time? If so, it isn’t state.
Is it passed in from a parent via props? If so, it isn’t state.
Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

5. How can you identify where state needs to live?
-Identify every component that renders something based on that state.
Find their closest common parent component—a component above them all in the hierarchy.
Decide where the state should live:
Often, you can put the state directly into their common parent.
You can also put the state into some component above their common parent.
If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

## High-Order Functions

1. What is a “higher-order function”?
-a higher-order function is a function that takes one or more functions as arguments, returns a function as its result, or both.

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

- line 2 is a higher-order function that takes a parameter `n` and returns a new function that takes in a parameter `m`. 


3. Explain how either map or reduce operates, with regards to higher-order functions.

-The `map` function is a higher-order function that is used to transform each element of an array into a new value, and then returns a new array with the transformed values. It takes a callback function as an argument, which is applied to each element in the array

-The `reduce` function is a higher-order function that is used to iterate over an array and accumulate a single value by applying a callback function to each element in the array, which takes an accumulator as its first parameter and the current element as its second parameter.