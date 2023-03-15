## Debugging

1. Name some key differences between a Syntax Error and a Logic Error.

Syntax errors are errors in your code that will cause the program not to run or stop working part way through. 

Logic errors are errors where the syntax is actually correct but the code is not what you intended it to be, meaning the program runs successfully but gives incorrect results. These are harder to fix becuase there usually isn't an error message. But we've typically console logged our functions to make sure they are doing what we want them to do.

2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.

I have gotten syntax errors and logic errors: for example, "not a function" and "unexpected `{` token". I typically refernce the line that the error message indicates and to fix whatever is wrong. I also have had issues where no error message shows up and I `console.log` my functions to see what they are returning and sometimes this is what helps me figure out for example if I returned anything in the function. 

3. How will this topic continue to influence your long term goals?

This will make debugging my projects a little easier. When I run into issues I know where to look for the bug and with that I can google whatever it is I need to look up. This also helps me with knowing what questions I need to answer in order to solve the issues I'm having. 

## The JS Debugger

1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?

The deBugger tool is similar to the pilots manual for hot to fix a plane or a car mechanic for how to fix a car.

The DOM editor is like making notes on how you want to fix something but not implementing it yet. 

2. Define what a breakpoint is.

The JS debugger allows you to watch the value of variables and set breakpoints-- places in your code that you want to pause execution and identify the problems that prevent your code from executing properly.

3. What is the call stack?

"The call stack section shows you what code was executed to get to the current line." 

-List of functions that were called in sequence until your broswer reaches that line of code that was invalid. 
"All of these things ran and then this line is where the code broke".

This section will appear when the code is running. 

## I want to know more about these things