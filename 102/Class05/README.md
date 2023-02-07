# CSS - Cascading Style Sheet

**What is CSS?** 

Cascading Style Sheets is the style and look of a webpage. It controls how HTML elements look in the browser.

CSS is a language specifying how documents are presented to users - how they are styled, laid out, etc.

CSS can be used for very basic document text styling - for ex. changing the color, size of headings and links. It can be used to create a layout etc. 

It can also be used for animation.

**CSS Syntax**

CSS is a rule based language - ***you define the rules by specifying groups of styles that should be applied to particular elements on your web page. 

For example, you can have a main heading on your page to be shown as a large red text. 
>
> `h1 {`
>    `color: red;`
> `font-size: 5em;`
>`}`
>
>>* In this example the CSS rule opens with a **selector**. This *selects* the HTML element that we are going to style. The h1 heading
>>* We then have a set of curly braces { }
>>* Inside the braces we have one or more **declarations**, which includes **property** and **value** pairs. We specify the *property* (color in this example) before the colon, and then we specify the value of the property after the colon (red in this example).
>>* This ex. has 2 declarations, one for `color` and the other for `font-size`. Each pair specifies a property of the element we are selecting `h1`, and then a value we would like to give the property. 

**How to add CSS**

When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet. 

There are 3 ways to Insert CSS

1. External CSS

With an external CSS you can change the entire look of the website by changing just one file. 

Each HTML page ***must*** include a reference to the external style sheet file inside the `<link>` element inside the **head** section. 

for ex. `<link rel="stylesheet" href="mystyle.css">`

2. Internal CSS

An internal style sheet may be used if one single HTML page has a unique style. (inside the head section)


3. Inline CSS

An inline style can be used to apply a unique style for a single element.

To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.


Using the style tag within html 

If you use more than 1 style sheet, the styles will be used in cascading order. #1 has the highest priority

1. Inline style (inside the HTML element)

2. External and internal (in the head section)

3. Browser default

**How to color in CSS**

RGB
0-16
0-9 and then abcdef which gives a total of 16. 