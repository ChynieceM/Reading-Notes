## Learn HTML

1. When should you use an unordered list in your HTML document?

You should use an unordered list when you want to group a collection of items that do not have a numerical ordering and their order in the list is meaningless. 


2. How do you change the bullet style of unordered list items?

You change the bullet style in CSS using `list-style-type`. The style isn't defined in HTML.

3. When should you use an ordered list vs an unorder list in your HTML document?

You should use the ordered list when you want to group a collection of items that have a numerical ordering and their order in the list is important. They typically dispay with a preceeding marker such as a # or letter unlike an unordered list in which the order of items are meaningless.

4. Describe two ways you can change the numbers on list items provided by an ordered list?

Using the `type` attribute, you can change the numbers on the list items to roman numerals or letters for example. 

You can set the numbering type as :

* `a` for lowercase letters
* `A` for uppercase letters
* `i` for lowercase roman numerals
* `I` for uppercase roman numerals
* `1` for numbers (default)

## Learn CSS

1. Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?

In Inspect, everything has its own box. Everything in CSS has a box around it and understanding. If this was an HGTV show called 'The Box Model', the margin and padding would be the interior designer saying something like, "the painting is crooked and needs to straigtened". 

2. List and describe the four parts of an HTML elements box as referred to by the box model.

Margin -the fluff around the pillow
Padding - how fluffy the pillow are
Border -how long the fluff
Content - the pillow



## JavaScript

1. What data types can you store inside of an Array?

boolean, string "", integer, array[], object{}

2. Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?

Yes, you can access the values stored by:
`people[0][0]`

3. List five shorthand operators for assignment in javascript and describe what they do.

* += adds the value on the right to the value stored in the variable on the left and assigns the new value to the variable

* -= subtracts the value on the right from the value stored in the variable on the left and assigns the new value to the variable

* /= divides the value in the variable on the left by the value on the right and stores the new value in the variable

* *= multiplies the value in the variable on the left by the value on the right and stores the new value in the variable

* %= stores the remainder from dividing the value stored in the variable on the left by the value on the right into the variable

4. Read the code below and evaluate the last expression and explain what the result would be and why.

This would evaluate to the string `'10dog'`. The `a + c` would be evaluated first because it is in the parentheses. Javascript would change false to 0 and add it to 10. Then it would turn 10 to a string and concatenate it with 'dog' which is the value stored in `b`.

5. Describe a real world example of when a conditional statement should be used in a JavaScript program.

When you have many conditions Sto be met; guessing games. 

Give an example of when a Loop is useful in JavaScript.

Unless someone enters correct information, they will be asked the same question. 