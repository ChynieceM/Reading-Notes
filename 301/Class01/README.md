## Component-Based Architecture

Component based architecture focuses on the decomposition of the design into the individual functional or logical components that represent well-defined communicaiton interfaces containing methods, events, and properties. 

1. What is a “component”?
-It is a modular, portable, replaceable, and resuable set of well defined functionality that encapsulates its implementation and exporting it as a higher level interface.

2. What are the characteristics of a component?
-Components are reusable, replaceable, not context specific, extensible, encapsulated, and independent. 

3. What are the advantages of using component-based architecture?
-Some advantages of component based architecture is ease of deployment, reduced cost, ease of development, resuable, modification of technical complexity, reliability, system maintenance and evolution, and independence. 

## Props and how to use it in React

React is a component based library that divides the UI into little reusable pieces. In some cases those components need to communicate (send data to each other) and the way to pass data between components is by using props. 

1. What is “props” short for?
-Props is short for properties and is being used to pass data from one component to another. 
2. How are props used in React?
-Props are used to pass data from one component to another.
3. What is the flow of props?
-Data with props are being passed in a uni directional. This means props data is read only, which means that data coming from the parent should not be changed by the child components. 

