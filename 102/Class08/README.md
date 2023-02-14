## Comparison Operators & Assignment Operators

All complex expressions are joined by operators such as `=` and `+`

The precedece of operators determines the order in which they are applied when evaluating an expression. 

ex. `const x = 1+2*3;`
    `const y = 2*3+1;`
>
> Despite `*` and `+` coming in different orders, borth expressions would result in `7` b/c `*` has precedence over `+`. ***you can override operator precedence by using `()`. 

### Assignment Operators 

An assignment operator assigns value to its left operand based on the value of its right operand. That is `x=f()` is an assignemnt expressions that assigns the value of `f()` to `x`.

**Assigning to properties**

If an expression evaluated to an object then the left hand side of an assignment expression may make assignments to properties of that expression. 

For ex1. 

`const obj{}`

`obj.x=3;`

`console.log(obj.x);`//prints 3

`console.log(obj);`//prints {x:3}

For ex2.

`const key = "y";`

`obj[key] = 5;`

`console.log(obj[key]);`//prints 5

`console.log(obj);`//prints{x:3, y:5}

### Comparison Operators

A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. 

**If two operands are not the same type, JavaScript attempts to convert them to an appropriate type for the comparison**.

This typically results in comparing the operands numerically. 

The sole exceptions to type conversion w/in comparisons involve the `===` and `!==` operators which perform strict equality and inequality comparisons. 

Comparison Operators

Equal `==` - returns `true` if the operands are equal

Not Equal `!=` - Returns `true` if the operands are not equal

Strict equal `===` - Returns `true` if the operands are equal and the same type

Strict not equal `!==` - returns true if hte operands are of the same type but not equal or are of different type

Greater than `>` 

Greater than or equal `>=`

Less than `<` 

Less than or equal `<=`

# Loops and iteration

Loops offer a quick way to do something repeatedly 

Think of *loops* as a computertized version of the game where you tell someone to take X steps in one direction and then Y in another. 

For ex. Go 5 steps to the east:
>
> `for (let step = 0; step< 5; stepp++)` `{`
>
>`console.log('Walking east one step");`
>}`

* Loops allow you to run the same code multiple times. 

* While loops run while a specified condition is true and stops once its no longer true. 

var i = 0

while(i < 5>){
myArray.push(i);
i++
}
console.log(myArray)

should show [0,1,2,3,4]

Iterate while loops 

* For Loops

var ourArray = [];
for(var i=0; i<5; i++){
    ourArray.push(i);
}
- instead of `ourarray.push(i)` you'd add console.log(ourArray)
for (var i = 1; i<6; i++){
    myArray.push(i);
}

should show [1,2,3,4,5]

* The various loop mechanisms offer different ways to determine the start and end points of the loop.
