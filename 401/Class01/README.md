 summarize and explain this topic via an analogy from your previous work or home experience

 ## Creating a .NET console Application
 ## Run the app
 ## Enhance the app
 [refer to this link](https://learn.microsoft.com/en-us/dotnet/core/tutorials/with-visual-studio-code?pivots=dotnet-7-0)

 ## C# Methods

 A Method is a block of code which only runs when it is called. You can pass data, known as parameters, into a method.

 Methods are used to perform certain actions, and they are also known as functions. 

 We use methods to reuse code: define the code once and use it many times. 

 ### Create a method

 A method is defined with the name of the method, followed by parentheses (). C# provides some predefined methods which you already are familiar with such as Main(), but you can also create your own methods to perform certain actions:

 ```cs
 class Program
{
  static void MyMethod() 
  {
    // code to be executed
  }
}
```

- `MyMethod()` is the name of the method
- `static` means that the method belongs to the Program class and not an object of the Program class. 
- `void` means that this method does not have a return value.

### Call a Method

To call (execute) a method, write the method's name followed by two parentheses() and a semicolon;
 
 - MyMethod() is used to print a text (the action), when it is called:

```cs
static void MyMethod() 
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
}

// Outputs "I just got executed!"
```

## User Input

Console.WriteLIne() is used to output (print) values. 
Console.ReadLine() is used to get user input. 

The user can input his or hers username, which is stored in the variable userName. Then we print the value of userName:

```cs
// Type your username and press enter
Console.WriteLine("Enter username:");

// Create a string variable and get user input from the keyboard and store it in the variable
string userName = Console.ReadLine();

// Print the value of the variable (userName), which will display the input value
Console.WriteLine("Username is: " + userName);
```

### User Input and Numbers

The Console.ReadLine() method returns a string. Therefore, you cannot get information from another data type, such as int. The following program will cause an error:

```cs
Console.WriteLine("Enter your age:");
int age = Console.ReadLine();
Console.WriteLine("Your age is: " + age);
```

The error message will be something like this:
`Cannot implicitly convert type 'string' to 'int'`

You cannot implicitly convert type 'string' to 'int'.

 you can convert any type explicitly, by using one of the Convert.To methods:

Example
```cs
Console.WriteLine("Enter your age:");
int age = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Your age is: " + age);
```

## Debug a .NET console application
[refer to this link](https://learn.microsoft.com/en-us/dotnet/core/tutorials/debugging-with-visual-studio-code?pivots=dotnet-7-0
)
Debug and Release are .NET's built-in build configurations. You use the Debug build configuration for debugging and the Release configuration for the final release distribution.

### Set a breakpoint

A breakpoint temporarily interrupts the execution of the application before the line with the breakpoint is run.

### Set up for terminal input

The breakpoint is located after a `Console.ReadLine` method call. The Debug Console doesn't accept terminal input for a running program. To handle terminal input while debugging, you can use the integrated terminal (one of the Visual Studio Code windows) or an external terminal. For this tutorial, you use the integrated terminal.

### Start debugging

- Select the green arrow at the top of the pane, next to .NET Core Launch (console). Other ways to start the program in debugging mode are by pressing F5 or choosing Run > Start Debugging from the menu.

- Enter a string in the Terminal window in response to the prompt for a name, and then press Enter.

- Program execution stops when it reaches the breakpoint and before the Console.WriteLine method runs. The Locals section of the Variables window displays the values of variables that are defined in the currently running method.

### Using the Debug Console

The Debug Console window lets you interact with the application you're debugging. You can change the value of variables to see how it affects your program.

### Set a conditional breakpoint

The program displays the string that the user enters. What happens if the user doesn't enter anything? You can test this with a useful debugging feature called a conditional breakpoint.

### Step through a program 

Visual Studio Code also allows you to step line by line through a program and monitor its execution. Ordinarily, you'd set a breakpoint and follow program flow through a small part of your program code. Since this program is small, you can step through the entire program.

1. Set a breakpoint on the opening curly brace of the Main method.

2. Press F5 to start debugging.

Visual Studio Code highlights the breakpoint line.

At this point, the Variables window shows that the args array is empty, and name and currentDate have default values.

3. Select Run > Step Into or press F11. Visual Studio Code highlights the next line.

4. Select Run > Step Into or press F11.

Visual Studio Code runs the Console.WriteLine for the name prompt and highlights the next line of execution. The next line is the Console.ReadLine for the name. The Variables window is unchanged, and the Terminal tab shows the "What is your name?" prompt.

5. Select Run > Step Into or press F11.

Visual Studio highlights the name variable assignment. The Variables window shows that name is still null.

Respond to the prompt by entering a string in the Terminal tab and pressing Enter.

The Terminal tab might not display the string you enter while you're entering it, but the Console.ReadLine method will capture your input.

6. Select Run > Step Into or press F11.

Visual Studio Code highlights the currentDate variable assignment. The Variables window shows the value returned by the call to the Console.ReadLine method. The Terminal tab displays the string you entered at the prompt.

7. Select Run > Step Into or press F11.

The Variables window shows the value of the currentDate variable after the assignment from the DateTime.Now property.

8. Select Run > Step Into or press F11.

Visual Studio Code calls the Console.WriteLine(String, Object, Object) method. The console window displays the formatted string.

10. Select Run > Step Out or press Shift+F11.

Step-Out button

11. Select the Terminal tab.

The terminal displays "Press any key to exit..."

12. Press any key to exit the program.

# Debugging in Visual Studio

The debugger provides many ways to see what your code is doing while it runs. You can step through your code and look at the values stored in variables, you can set watches on variables to see when values change, you can examine the execution path of your code, see whether a branch of code is running, and so on. 

[Debugging for beginners](https://learn.microsoft.com/en-us/visualstudio/debugger/debugging-absolute-beginners?view=vs-2019)

First, you'll create a .NET Core console application project. The project type comes with all the template files you'll need, before you've even added anything!

1. Open Visual Studio.

If the start window is not open, choose File > Start Window.

2. On the start window, choose Create a new project.

3. On the Create a new project window, enter or type console in the search box. Next, choose C# from the Language list, and then choose Windows from the Platform list.

After you apply the language and platform filters, choose the Console Application template for .NET Core, and then choose Next.

4. In the Configure your new project window, type or enter GetStartedDebugging in the Project name box. Then, choose Next.

5. Choose either the recommended target framework (.NET Core 3.1 (Long-term support)) or .NET 5.0 (Current) , and then choose Create.

Visual Studio opens your new project.

## Start the debugger

1. Press F5 (Debug > Start Debugging) or the Start Debugging button Image of the 'Start Debugging' button. in the Debug Toolbar.

F5 starts the app with the debugger attached to the app process, but right now we haven't done anything special to examine the code. So the app just loads and you'll see this console output.

2. Stop the debugger by pressing the red stop Image of the 'Stop Debugging' button. button (Shift + F5).

3. In the console window, press a key to close the console window.

## Set a breakpoint and start the debugger

[refer to this article for debugging in VS](https://learn.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-debugger?toc=%2Fvisualstudio%2Fdebugger%2Ftoc.json&view=vs-2019)