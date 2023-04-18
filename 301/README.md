## React lifecycle

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

-Render happens before the componentDidMount.

2. What is the very first thing to happen in the lifecycle of React?

-The very first thing that happens in the lifecycle of React is mounting. When an instance of a component is being created and inserted into the DOM it occurs during the mountin phase. 

3. Put the following things in the order that they happen: componentDidMount, `render`, `constructor`, `componentWillUnmount`, `React Updates`

1. constructor
2. render
3.componentDidMount 
4. componentWillUnmount
5. reactUpdates

4. What does `componentDidMount` do?
This method is invoked immediates after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This is a good place to set up subscriptions. 

## React State vs Props

1. What types of things can you pass in the props?
-Props might remind you of HTMl attributes you can pass any Javascript value through them including objects, arrays, and functions. 

2. What is the big difference between props and state?
-state is the local state of the component which cannot be acccessed and modified outside of the component. 
-props make components reusable by giving components the ability to receive data from their parent component in the form of props. 

3. When do we re-render our application?
-we re-render our application when React needs to update the app with some data. This happens as a result of a user interacting with the app or some ecternal data coming trhough via asynchronous requests or some subscruption model. 

4. What are some examples of things that we could store in state?
- things that need to be updated or things that will change. 
