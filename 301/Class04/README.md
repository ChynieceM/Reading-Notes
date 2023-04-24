## React Docs-Forms

1. What is a ‘Controlled Component’?
In HTML, form elements like `<input>, <textarea>, and <select>` usually have their own internal state that is updated directly by the user's input. However, in React, it's common to manage state using the state property of components, and to update it using the `setState()` method.

To combine these two approaches, we can make React's state the single source of truth for form data. This means that the React component rendering the form manages the state for the form data, and also controls what happens when the user interacts with the form. An input form element whose value is managed by React's state in this way is called a "controlled component" in React.

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
 It's recommended to update the state with the user's responses as they enter them, rather than waiting until the form is submitted. This is because React's state management is designed to be efficient and optimized for handling updates in real-time, and it provides benefits such as re-rendering only the necessary components when state changes.
Updating the state with the user's responses as they enter them has several advantages: Real-time feedback, Improved performance, Easier data synchronization, Enhanced form functionality.

3. How do we target what the user is entering if we have an event handler on an input field?

You can target what the user is entering in an input field by using the `event` object that is passed to the event handler function. The `event` object contains information about the event, including the target element that triggered the event, which in this case is the input field. You can access the value of the input field using the `event.target.value` property.

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
A ternary operator in JavaScript is a shorthand way to write an if statement with a concise syntax. It allows you to write a simple conditional expression in a single line of code.

2. Rewrite the following statement using a ternary statement:

if(x===y){
  console.log(true);
} else {
  console.log(false);
} 

-`console.log(x === y ? true : false);`