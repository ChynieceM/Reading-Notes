## Getting Started


**JS Basics**

JavaScript adds interactivity to your site. 

JavaScript is compact yet flexible. Developers have written a variety of tools on top of the core of the JS language. These include: 

To include a `main.js` file into your HTML document use 
>
> `<script src="scripts/main.js"></script>`

Language basics crash course:

Variables - containers that store values. You start by delcaring variables with the `let` keyword, followed by the name you want to give the variable.

Heres more on JS basics [More on JS](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)


* Browser application programming interfaces APIs built into we browsers providing functionality such as creating HTML and setting CSS styles; collecting and manipulating a video stream from a users webcam etc. 

* 3rd party APIs that allow developers to incorporate functionality in sites from other content providers such as twitter. 

* 3rd party frameworks and libraries that you can apply to HTML to accelerate the work of bultind sites and applications. 

1. **Compose a short poem describing how HTTP sends data between computers.**

HTTP, my friend, needs a favor, he said hey man I need to get a message to dee dee.  Pass this message along so I can use the phone. 

I cant get this message to my friend of a friend cuz they dont know what language its in. 

But good thing we can drink this goop so he can get the scoop. And then send the message to my dog in a chicken coop. 

2. **Describe how HTML, CSS, and JS files are “parsed” in the browser.**

When the browser requests servers for HTML files, HTML files will have a link element referenceing CSS and JS. The browser searches the HTML file and recognizes any link elements referencing CSS stylsheets and script elements referencing script elements

After the browser parses the HTMl it sends requests back to the server for CSS files and JS files it found and then parses the CSS and JS.

The browser generates an in memory DOM tree from the parsed files and a in memory CSSOM structure from the parsed CSS and compiles and executes the parsed JS. 

As the browser builds the DOM tree and applies the styles from teh CSSOM tree and executes the JS, a visual representation of the page is painted to the screen and the user sees the page content and can interact with it. 

3. **How can you find images to add to a Website?**

You can google suitables images and save that image to your computer for later use. 


4. **How do you create a String vs a Number in JavaScript?**

You create a string using parenthesis and a number with out. The computer recognizes numbers but you'll have to tell it if you want something to be identified as a string. 


5. **What is a Variable and why are they important in JavaScript?**

Variables are containers that store information or values. They are important becuase it allows your site to be dynamic. Variables allow change and are  necesary to do anything "interesting". 



## Introduction to HTML

#### Basic sections of a document

**Header:** `<header>` usually a big strip accross the top with a big heading, logo and perhaps a tagline.

**navigation bar:** `<nav>` links to the sites main sections: usually represented by menu buttons, links, or tabs.

* many designers consider the nav bar to be apart of the header rather than an individual component but not a requirement. Some argue that having the two separate is better for accessiblity. 

**main content:** `<main>`, with various content subsections reped by `<article>`, `<section>`, and `<div>` elements; a big area in the center that contains most of the unique content of a given page

**sidebar:** `<aside>` often placed inside the `<main>`; this is some peripheral informaiton like links, quotes, ads, etc. 

**footer:**`<footer>` a strip accross the bottom that has fine print info. This information typically isnt critcal. This is sometmes used fro SEO purposes.

[elements in more detail](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)


1. What is an HTML attribute?

An attribute contains extra information about the element that wont appear in the elemement. ex. the class or id of an element. 

2. Describe the Anatomy of an HTMl element.

An HTML element has an openeing and closing tag along with the content in the middle. And sometimes has attributes. 

3. What is the Difference between `<article>` and `<section>` element tags?

The `<article>` tag represents a self-contained comporition in a document, page, or site, and is intented to be independently distriutable or reusable. for ex. a widget, forum post, or a blog entry. A document can have many articles; each `<article>` should be identified by including a heading `<h1>-<h6>` element as a child of the `<article>` element. 

A `<section>` tag represents a generic standalone section of a document; a generic sectioning element and should be used if there isnt a more specific element to respresent it. 

Articles may have sections in it. 

4. What Elements does a “typical” website include?

**Header:** `<header>` 

**navigation bar:** `<nav>`

**main content:** `<main>`

**sidebar:** `<aside>` 

**footer:**`<footer>`

5. How does metadata influence Search Engine Optimization?

Specifying a description that includes keywords relating to the content of your page helps the page appear higher in relevant searches performed in search engines. 

6. How is the `<meta>` HTML tag used when specifying metadata?

This tag is used to specify character encoding; the character est that the document is permitted to use -- `utf-8`. This means the webpage will be able to handle displaying any language. 


## Miscellaneous

**How to start to design a website**

1. What is the first step to designing a Website?

Asking yourself these 3 questions for *project ideation*:
What exactly do I wnat to accomplish?

How will a website help me reach my goals?

What needs to be done and in what order to reach my goals? 

Then going into a deeper dive that includes structuring your ideas to get a clear idea on what path you need to take to make your ideas come to life. 

Break out your ideas into smaller actionable steps. 

2. What is the most important question to answer when designing a Website?

Is it reasonable to design a website to cover all of my goals that I want to accomplish? 

**Semantics**

1. Why should you use an <h1> element over a <span> element to display a top level heading?

The `<span>` element will render something to look like a top level heading but it has no semantic value. The `<h1>` element gives the text it wraps around a ***role*** or a meaning. **HTMl** should be coded to represent *data* that will be populated and not what it should look like. That's what CSS is for. 

2. What are the benefits of using semantic tags in our HTML?

* Search englgines will consider its content as important keywords to influence page ranking. 

* Screen readers can use it as a signpist to help visually imparied users navigate a page. 

* Finding blocks of meaningful code is much easier than searching through endless `div`s with or without semantic namspaced classes

* Suggests to the developer the type of data that will be populated

* Semantic naming mirror proper customer element/compoent naming 

**What is JavaScript**

1. Describe 2 things that require JavaScript in the Browser?

Adding interactivity to your site. For example: getting a button to work or a button in the navigation menu to take you to another page. 


2. How can you add JavaScript to an HTML document?

You can add JavaScript internally or Externally. 