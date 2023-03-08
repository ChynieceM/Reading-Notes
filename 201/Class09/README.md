## Webforms

1. Why are forms so important in web development?

Webforms are important in web development becuase they are one of the main points of interaction b/w a user and a website or application. 

2. When designing a form, what are some key things to keep in mind when it comes to user experience?

Some key things to keep in mind when designing a form focusing on accessibilty is to make sure you give your forms semantics so they are usable and accessible; understand your sturcture and how it may read out via a screen reader for example. 

3. List 5 form elements and explain their importance.

The `<form>` element defines the form and determines the forms behavior; many assistive technologies and browser plugins can discover form elements and implement special hooks to make them easier to use.

The `<fieldset>` element is a convenient way to create groups of widgets that sahre the same purpose, for styling and sematics. The `<legend>` element inside this element formally describes the purpose of the `<fieldset>` it is inlcuded inside. 

The `<label>` element is the formal way to define a label for an HTML form widget. This is the most important element if you want to build accessible forms, screen readers will speak a form element's label along with any related instuctions. A screen reader will read out something like "Name, edit text" with the`<label>` element associated correctly `<input>` via its `for` attribute. 

## Event Listeners

1. How would you describe events to a non-technical friend?

Think of a class throwing a surpise party for their teacher. One student will  signal the class when their teacher is close so they can all hide. They want to yell "SURPISE" when she walks in. On the students signal they will hide and when she walks in they will yell surprise. The event listener is the class yelling surpise when the teacher walks in. 

2. When using the addEventListener() method, what 2 arguments will you need to provide?

The first argument needs to be the string `click` to indicate that we want to listen to the click event. The second arguemnt is the function to call when the event happens. 

3. Describe the event object. Why is the target within the event object useful?

An event object is automatically passed to event handlers to provide extra features and information. The `target` property of the event object is always a reference to the element the event occurred upon. 

4. What is the difference between event bubbling and event capturing?

Event bubbling describes how the broswer handles events targeted at nested elements.

Event capturing is like event bubbling but the order is reversed: so instead of event firing first on the innermost element targeted and then on successivily nested elements, the event fires first ont he least nested element. 
