# Wire Frame 

### 1. What is a wireframe?

**Wireframing** is used by U designers and helps them define and plan information hierarchy of the design for a website, app, or product. Basically an outline or sketch. 

* Wireframes help designers or clients focus on how they want users to process information, based on user research. 

* You want to know how all of the information is gonna look in plain black and white before coding anytning. 

* An argument for wireframing is if a user doesnt know where to go on a plain hand drawn diagram of your site page, then colors and fancy text is irrelevant. 

***Some example of wireframes are***: softwares like invision or Balsmiq.

* Advantages of paper and pencil are they can be easily changed; switching later to software allows you to keep track of more detailed exchange decisions

### 2. Consider this before wireframing

Deciding to use paper and pen or an online tool to wireframe depends more on what the end goal is. 

> ex. deciding which method depends on if you are more focused on visual design in a project or how much uncertainity there is re whats being designed 
>
>> examples of the structure process: 
>> * Wireframe > interactive prototype > visual > Design
>> * Sketch > Code
>> Sketch > Wireframe > Hi-Def Wireframe >Visual > Code 

### 3. 6 steps to wireframing

1. **Do you research** - Understand who your audience is by way of user reasearch, detailing requirements, creating user personas, defiing use cases. Carry out an **analysis** of similar product lines 

2. **Prepare your research for quick reference** - create a cheatsheet with your goals (requirements), personas, use cases, and reminders. 

3. **Map out user flow** - wireframing gets messy if you dont have an idea of how many screens you need to produce the flow you expect users to follow. 

* Have a tight concept of where your users will be coming from `(which marketing channels, and what messaging)`, and where you need them to end up. 

* Good **information architecture** will ensure that users are self sufficient, *are asking less questions on how to do something that should be simple*, lower levels of user frustration *leads to more levels of trust* and lowers drop off/out rates 

4. **Draft, dont draw. Sketch, don't illustrate**

* Remember you are outlining and representing features and formats not illustrating in fine detail. **Don't think about aesthetics and colors** just yet. The UI designer can deal with that. ***Use a thick marker to prevent you from drowning yourself in detail*** 

**Focus on these questions** when sketching: 

* How can you organise the content to support user goals?

* Which info should be most prominent? Where should the main message go? What should the user see first when going to the page?

* What will the user expect to see on certain areas of the page? 

* Which buttons or touch points does the user need to complete desired actions? 

5. **Add some detail and get to testing**

Add some informational details to prepare your wireframe for its upgrade, megatron-style, to prototype-mode.

Add detail in the way you would process a screen or book. Top to bottom, left to right. ***Here you are adding content, not the muscle just yet***. 

* Try to adhere to usability conventions such as putting your navigation bar next to your logo or having a search bar near the far right at the top of the page. 

6. **Turn wireframes into prototypes** 

You can now import your wireframes into a prototyping tool. 


### How to make you wireframe good

1. Clarity - Your wireframe needs to answer what the site page is, what the user can do, and if it satisfies their needs.

2. Confidence - Ease of navigation through your site and clear calls to action. Using familiar navigational processes and putting buttons in commonly used places.

3. Simplicity is key - too much info, copy, links, can be distracting. Your wireframe should be a visual guide to the framework of the site. But also help users and point them to your goals by way of interaction ie. check out cart etc. 


# HTML Basics

**HTML** is a markup language that defines the structure of content. HTML consists of elements which you use to *enclose*, or wrap, different parts of content to make it look a certain way or act a certain way. The enclosing tags can make a word/image hyperlink to somewhere, italicise words, change font size etc. 
 * ex. `<p>My cat is very grumpy</p>`

 #### **Anatomy of an HTML element** 

 1. The opening tag: consist of the name of the element (p for paragraph) wrapped in opening and closing **angle  brackets**; where the element begins to take effect.

 2. The closing tag: This is the same as the opening tag except it includes a forward slash before the element name; where the element ends. 

 3. The content: content of element or text

 4. The element: The opening tag, closing tag, and the content together to comprise the element

 ##### **Attriubutes** contain extra information about the element that you dont want to appear in the actual content - or what you dont want people to see. 

 ex. `<p class="editor-note">My cat is grumpy</p>`

 * `class` is the attribute *name* and `editor-note` is the attribute *value*. The `class` attribute allows you to give the element a non unique identigier that can be used to target it with style information and other things. 

 **Attributes that set a value always have**: 

 1. a space b/w it and the element name or previous attribute if the element already has one or more attributes.

 2. The attribute name followed by an equal sign

 3. The attribute value wrapped by opening and closing quotation marks.

 ##### **Nesting Elements**

 Putting elements inside other elements. to emphasize "very" in the ex. below, wrap text in a `<strong>` element. To properly nest close the strong element first. 

> `<p>My cat is <strong>very</strong> grumpy.</p>`

##### **Void Elements** 

Elements that have no content are void elements. For ex. the `<img>` element.
>
> `<img src="images/google.png" alt="Ex. Image"/>`
>
>> This has two attributes but theres no closing `</img>` tag and no inner content. The image element doesnt wrap content to affect it. Its purpose is to embed an image in the HTML page in the place it appears. 

##### **Anatomy of an HTML document**

* `<!DOCTYPE html>` -- doctype is a required preamble. This makes sure your document behaves correctly. 

* `<html></html>` - the html element wraps all the content on the entire page and is sometimes known as the **root** element. It also includes the `lang` attribute to set the primary language of the document. 

* `<head></head>` - the head element acts as a **container** for all the stuff you want to include on the HTML page that ***isnt*** the content you are showing to your pages viewers. this includes keywords and page description that you want to appear in search results, CSS to style our content, character set declaration, and more. 

* `<meta charset="utf-8">` - This elements sets the character set to your doc. It should include most characters from the vast majority of languages. 

* `<title></title>` - the title element sets the title of hte page and this is what appears in the browser tab the page is loaded in. 

`<body></body>` the body element contains all the content that you want to show to web users when they visit your page. Text, images, videos, audio tracks, etc. 

##### **Images**

The `<img>`  elements embeds the image into the page via the `srs` source attribute which contains the path to the image file.

We also include an `alt` attribute which specifies descriptive tect for users who cannot see the image for possible reasons:

1. They are visually impaires so they use tools called screen readers to read out alt text

2. Something has gone wrong causing the image to not display. So it'll show your alt text instead.

The **keywords** for alt text are **"descriptive text**. The alt text should give the reader enough info to have a good idea about what the image conveys. 

##### Marking up text

**Headings**

Heading elements allow you to specify which parts of the content are headers or sub headers. There are 6 heading levels

`<!-- 4 heading levels: -->` - 

Anything b/w `<! -- and -->` is an html comment

`<h1>My main title</h1>`
`<h2>My top level heading</h2>`
`<h3>My subheading</h3>`
`<h4>My sub-subheading</h4>`

***Dont use heading levels to bold text or make trext bigger b/s its used for accessibilty and other things like SEO*** 

**Lists** 

Ordered lists and Unordered lists

1. Unordered lists - wrapped in `<ul>` element

2. Ordered lists - wrapped in `<ol>` element

Each item inside the list is put inside an `<li>` *list item* element.

##### **Links** 

To add a link we use the **anchor** element or `<a>`; to make text w/in a paragraph into a link:

1. Choose text. 

2. Wrap text in `<a>` 

* `<a href="">Recipes</a>` href stands for hyptertext reference



# Semantics

In programming, **semantics** refers to the *meaning* of a piece of code. For example, "what does that line of code do in JavaScript?" or whats the purpose or role of that HTML element. 

##### **Semantics in JavaScript, CSS, and HTML**

In JavaScript consider a function that takes a string parameter and returns an `<li>` element with that string as its `textContent`. Would you need to looat at the code to understand hwat the function did if it was called `build('Peach')`?

In CSS, consider styling a list with `li` elements representing different types of fruits. Would you know what part of the DOM is being selected iwht `div > ul > li` or `.fruits_item`?

In HTML, the `<h1>` element is a semantic element, which gives the tect it wraps around the role of a top level heading on the page. 

***HTML should be coded to represent the **data** that will be populated and nost based on its default presentation styling***

Presentation is the sole responsibilty of **CSS**

Benefits from writing semantic markup

* search engines will consider its contents as important keywords to influence the page search rankings

* Screen readers can use it as a signpost to help visual impaired

* finding blocks of meaningful code is easier than reading throuhg endless `div`s

* semantic naming mirrors proper custom element/component naming

When using markup ask youself 

* what elements best describe/represent the data that I'm going to populate? Ex. Is it a list of data?, ordered or unordered? etc. 


# Links for elements and descriptions

[Elements and Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

[HTML + Tutorials](https://developer.mozilla.org/en-US/docs/Web/HTML)


UX, UI, -- UX is the overall feel 
ex. Git desktop, git web browser, and git command line is the user experience and the user interaction is thinking about doing things on the website or desktop. 
