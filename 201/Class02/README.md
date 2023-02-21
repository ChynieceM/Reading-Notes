## HTML cont. & HTML Text Fundamentals /Advanced formatting

1. Why is it important to use semantic elements in our HTML?

* Semantic elements give meaning. It's important that our document has correctly labeled sections for example and that jobs go to the right "people". 

* It makes the content easier to read and later on it allows us to add functionality and to do that we need structure and an organized mark up to make adding functionality and style easier. 

* When we see something we will know what each element means and we will know what function it needs. So giving our content the correct function, meaning, and appearance. 

2. How many levels of headings are there in HTML?

There are 6 levels of headings that also provide your document with structure. 

3. What are some uses for the `<sup>` and `<sub>` elements?

sup - define superscript (exponents)
sub - define subscript (ex. the '2' in h2o)

4. When using the `<abbr>` element, what attribute must be added to provide the full expansion of the term?

We must add a `title` attribute along with the `<abbr>` element to provide the full expansion of the term. 

* This element is used to wrap around an abbreviation or acronym. This provides a hint to user agents on how to announce/display the content while also sayig what it means.

## How CSS is structured 

1. What are ways we can apply CSS to our HTML?

We can apply CSS Externally by including file with the `.css` extension and linking it in our HTML document using `<link rel="stylesheet" href='styles/style.css"/>`, Internally using `<style> </style>` element embedded , or Inline which affect single elements `<p style="color:red;">` For example `</style>`.

2. Why should we avoid using inline styles?

For one, this method is the least effecient use of CSS for maintainenace.

Secondly, inline CSS also mixes the CSS presentational code with HTMl and content, making everything more difficult to read and undersand. 

3. Review the block of code below and answer the following questions:

* What is representing the selector?

`h2` represents the selector

* Which components are the CSS declarations?

color and padding are declarations

* Which components are considered properties?

the properties are the values so black and 5px. 


## JavaScript cont. 

1. What data type is a sequence of text enclosed in single quote marks?

string

2. List 4 types of JavaScript operators.

equals, greater than, less than, strict equals

3. Describe a real world Problem you could solve with a Function.

Giving a certain # of people access to a site. So using login credentials to acces this site. You need functions to allow users to submit their information in log in fields and to make button functional. 

**Making Decisions In Your Code -- Conditionals**

1. An if statement checks a __ and if it evaluates to ___, then the code block will execute.

condition; true

2. What is the use of an `else if`?

This gives us a way to use more than two choices or outcomes. 

3. List 3 different types of comparison operators.

`===`, `<`, `>`

4. What is the difference between the logical operator `&&` and `||`?

`&&` -- AND allows you to chain 2 or more expression so that all of them have to indivudally evaluate to `true` for the whole expression to evaluate to true. 

`||` -- OR allows you to tchain together 2 or more expressions so that 1 or more have to individually evaluate to `true` for the whole expression to return to `true`. 

## How to use Git

[how to use git](https://chris.beams.io/posts/git-commit/)