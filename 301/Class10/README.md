## Understanding the JavaScript Call Stack

1. What is a ‘call’?
-A 'call' in the context of JavaScript and programming languages, in general, refers to the invocation or execution of a function. When a function is called, it is added to the call stack, which keeps track of the order of function execution.
2. How many ‘calls’ can happen at once?
-In JavaScript, only one call can happen at a time due to its single-threaded nature. This means that function calls are executed one after another, in the order they are added to the call stack.
3. What does LIFO mean?
-LIFO stands for "Last In, First Out." It is a principle used in data structures like stacks, where the last item added is the first one to be removed. In the context of the call stack, the most recently called function is executed first and removed from the stack when it finishes.
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
function multiply(a, b) {
  return a * b;
}
function square(x) {
  return multiply(x, x);
}
function printSquare(square) {
  console.log(square);
}
printSquare(square(5));
Call stack:
1. printSquare (initial call)
2. square (called inside printSquare)
3. multiply (called inside square)

5. What causes a Stack Overflow?
-A Stack Overflow occurs when the call stack exceeds its maximum capacity due to recursive or deeply nested function calls. Since the call stack has a limited amount of space available, an overflow causes the program to crash or throw an error, such as a "RangeError: Maximum call stack size exceeded" in JavaScript.

## JavaScript error messages

1. What is a ‘reference error’?
-A 'reference error' occurs when you try to use a variable that has not been declared or is not defined in the current scope. In JavaScript, a ReferenceError is thrown when you attempt to reference a non-existing variable.
2. What is a ‘syntax error’?
-A 'syntax error' occurs when the code you've written does not adhere to the rules and structure of the programming language. In JavaScript, a SyntaxError is thrown when the code contains incorrect or unexpected tokens, such as missing brackets, parentheses, or semicolons.
3. What is a ‘range error’?
-A 'range error' occurs when a value is outside the acceptable range for a specific operation or data type. In JavaScript, a RangeError is thrown when you try to perform an operation that exceeds the limits, such as calling a function recursively too many times and causing a stack overflow.
4. What is a ‘type error’?
-A 'type error' occurs when an operation is performed on a value of an incorrect or unexpected type. In JavaScript, a TypeError is thrown when you attempt to use a value that is not compatible with the expected type, such as calling a non-function as if it were a function or accessing a property on a null or undefined object.
5. What is a breakpoint?
-A breakpoint is a point in your code where you intentionally pause the execution of a program during debugging. By setting breakpoints, you can inspect the current state of your application, examine variable values, and step through your code to identify and fix issues.
6. What does the word ‘debugger’ do in your code?
-The 'debugger' keyword in JavaScript is used to add a breakpoint directly in your code. When the execution reaches the line with the 'debugger' keyword, it will pause if a debugging tool (like browser DevTools or an Integrated Development Environment) is active. This allows you to inspect the current state of your application and analyze your code's execution to identify and resolve issues.