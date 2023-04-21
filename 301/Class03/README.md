## React Docs - lists and keys

1. What does `.map()` return?
 It returns a new array of the same number of elements as the original array.
 
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
 I would use `.map()` to loop through an array and render JSX for each value.

3. Each list item needs a unique ____.
 Key

4. What is the purpose of a key?
Keys differentiate whichever item React is controlling. It keeps track of the items. 

## The Spread Operator

1. What is the spread operator?
 Pass in an array where you want all of the elements to be parameter. It basically "unarrays" an array. 

2. List 4 things that the spread operator can do.
 Copying an array, concatenating or combining arrays, using math functions, using an array as arguments, addding anitem to a list, adding to state in react, combining objects, converting nodelist to an array. 

3. Give an example of using the spread operator to combine two arrays.
`const myArray = [`🤪`,`🐻`,`🎌`]`
`const yourArray = [`🙂`,`🤗`,`🤩`]`
`const ourArray = [...myArray,...yourArray]`
`console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩`

4. Give an example of using the spread operator to add a new item to an array.
`const fewFruit = ['🍏','🍊','🍌']`
`const fewMoreFruit = ['🍉', '🍍', ...fewFruit]`
`console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]`


5. Give an example of using the spread operator to combine two objects into one.

`const objectOne = {hello: "🤪"}`
`const objectTwo = {world: "🐻"}`
`const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}`
`console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }`
`const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}`
`objectFour.laugh() // 😂😂😂😂😂`

## How to pass functions between components

1. In the video, what is the first step that the developer does to pass functions between components?
 
He creates a function that passes in a person object. 

2. In your own words, what does the increment function do?
Increment adds 1 to a variable or increments the value of the variable by 1.

3. How can you pass a method from a parent component into a child component?
 You can pass a method from a parent component into a child component as a prop or an attribute.

4. How does the child component invoke a method that was passed to it from a parent component?
You can invoke a method that was passed to a child component from a parent component using the props or attributes that were passed down. 