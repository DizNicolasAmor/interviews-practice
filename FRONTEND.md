# FRONTEND Q&A

## TABLE OF CONTENTS

- [Javascript](#javascript)
  - What does "data type" mean and how many data types are in JS?
  - What is hoisting?
  - What is Scope?
  - What is Closure?
  - What is the Event loop?
  - How does the Event loop work in Javascript?
  - Explain Apply, Bind and Call functions
  - What is Immutability?
  - How to copy an object?
  - What is a HOF (high order function)?
  - What is the difference between map, reduce and forEach functions?
  - What is ECMAScript?
  - Mention some of the new features in ES6
  - Mention some of the new features in ES11 (ES 2020)
  - What are the differences between var, let and const?
  - What are the difference between an arrow function and a regular function?
  - What is a Promise?
  - How a Promise can be consumed?
- [React](#react)
  - What is React?
  - What is COP (component oriented programming)?
  - What is Immutability and why it is important in React?
  - What is the Virtual DOM?
  - What is the Reconciliation in React?
  - What is Redux?
  - What is a HOC (High order component)?
  - What is a middleware?
  - What is redux-saga?
  - What is redux-thunk?
  - What is react-native?
  - What is different in react-native from react?

<a name="javascript"/>

## Javascript

### What does "data type" mean and how many data types are in JS?

Data type in programming is a **classification** that is used for specifying with kind of operation can be done with a given value. In Javascript we have 6 different primitive data types:

1. string
2. boolean
3. number
4. bigint
5. Symbol
6. undefined

and 3 structural data types:

7. object
8. function
9. null

Javascript has **dynamic types**. This means the same variable can be used to hold different data types.

### What is hoisting?

Is a javascript mechanism where variables and function declarations are put in the memory before the code execution. For the coder, it is like the variable declarations are moved to the top of their scope.

### What is Scope?

It's a policy that manages the availability of variables. That means, it is the specific environment where a variable is accessible and can be used. In javascript we have different scopes:

1. Block scope - Using let and const.
2. Function scope - Using let, const and var.
3. Module scope - For variables, functions and classes.
4. Global scope - Is accessible from everywhere, examples: `window` object in browser and `process` object in nodejs.
5. Lexical scope - Is determined statically by the position of the variables within the nested function scopes.

### What is Closure?

It's a combination of a function bundled together with references to its surrounding state. Basically it's a function that is created inside another one. The outer function is said to "enclose" the scope of the inner function.

- **What is a Javascript Hosting Environment?**

It's where a JS Engine runs. It consists in the JS Engine itself, a set of environment API's and the Event loop.
Environment API's depends on the context. In a web browser for example we are able to use `onclick` events, in Node Js, file operations such as read, write, delete, etc...

### What is the Event loop?

It's the process of dispatching events and executing instructions in a javascript program.

### How does the Event loop work in Javascript?

The event loop is the process of monitoring 2 parts of a Javascript hosting environment (such as Node js or a Web Browser), those 2 parts are, the **CallStack** and the **Callback Queue**.
The CallStack is where the event loop puts each function call and it follows a LIFO approach to process functions. It means the last function that is executed is the first one that is removed from the CallStack.
The Callback Queue is another place in which function calls are placed to be processed once the CallStack is empty. The Callback Queue follows a FIFO approach to process callback functions, it means that the first function that is added to de queue is the first one that is removed from it. Is used for different environment API's like `setTimeout`, `fetch` or `file.read` to put callback functions inside it once they're required.
In example:
`setTimeout` will put a callback function at the end of the Callback Queue once the timeout value is reached. Once the `setTimeout` callback is added into the Callback Queue, the event loop will wait until the CallStack is empty, when it happens, the event loop will move the `setTimeout` callback from the Callback Queue to the CallStack to be processed by the Javascript Engine.

### Explain Apply, Bind and Call functions

1. Bind: Creates a new function with a new context assigned by the first argument on `bind` invocation.
2. Call: Call a function with a new context assigned by the first argument.
3. Apply: It's the same as `call` but `apply` taskes an array as a unique argument where the first position is the new context and the rest of them are the arguments.

### What is Immutability?

Immutability is an attribute that forbids a data type mutation.

### How to copy an object?

It depends on the object.

- For an object with only primitive values, you could simply use `Object.assign` or the `spread operator`.
- For an object with many primitive values and only a few complex values, you could use the same tools than before and then override (copy) the specific properties with complex values.
- For an object with complex levels of deepness you could use a custom function with a recursive `Object.assign` call.
- Also, you could use third-party solutions from libraries like `lodash`.
- You could use a mix of `JSON.parse` and `JSON.stringify` methods to copy an object with any level of deepness. However this is a naive solution and there are some issues in border cases.

### What is a HOF (high order function)?

A High Order Function is a function that either takes a function as an argument or returns a function.

### What is the difference between map, reduce and forEach functions?

The `map` method receives a function as a parameter. Then it applies it on each element and returns a new array populated
with the results of calling the provided function. In the case of `forEach` method, it receives a function as a parameter with each array value and returns `undefined`, its proupouse is only iterate an array. And finally `reduce` method is used to reduce the array to a single value, it executes a provided function for each value of the array (from left-to-right) and the return value of the function is stored in an accumulator.

### What is ECMAScript?

Ecmascript (European Computer Manufacturer's Association) is a standard for scripting languages.

### Mention some of the new features in ES6

1. Arrow functions
2. Template strings
3. Let and const keywords.
4. Symbols

### Mention some of the new features in ES11 (ES 2020)

1. Optional chaining
2. Dynamic imports
3. Promise.allSettled
4. Global this.

### What are the differences between var, let and const?

1. `var` declarations are globally scoped or function scoped while `let` and `const` are block scoped.
2. `var` variables can be updated and re-declared within its scope, `let` variables can be updated but not re-declared
   and `const` variables can neither be updated nor re-declared.
3. All of them are hoisted to the top of their scope. But while `var` v ariables are initialized with `undefined`, `let` and `const` variables
   are not initialized.
4. While `var` and `let` can be declared without being initialized, `const` must be initialized during declaration.

### What are the difference between an arrow function and a regular function?

They have the following differences:

1. Arrow function have different syntax.
2. Regular functions have an `arguments` binding and arrow functions only have access to `arguments` objects of the closest non-arrow parent function.
3. Arrow ones have "lexical this". Basically in an arrow function, the value of `this` is always inherited from the enclosing scope. In regular functions, the value of `this` is defined whyen it's being executed and it depends on where it has been executed from.
4. Arrow functions are only callable and regular functions are either callable and constructible (can be invoked with the `new` keyboard).

### What is a Promise?

A promise is a function that will return data in some future.

### How a Promise can be consumed?

- Using `then / catch`: you can call the `then` method and pass a callback as a param. The callback will be executed when the promise resolves. After that you can use the`catch` method. Same criteria, but the catch callback will be executed if the promise rejects.
- Using `async / await`: declare an `async` function and inside of it you can use the `await` keyword before your promise.
- Using a generator: you can declare a generator function and consume the promise inside of it, with the yield keyword.

<a name="react"/>

## React

### What is React?

React is a javascript library for the frontend. It is based on the Component Oriented Programming paradigm. It is very useful for building interactive user interfaces.

In React, you have a state with important data in your app that can change dynamically, and you can show different views depending on each state. Another important topic is that it uses a virtual DOM.

### What is COP (component oriented programming)?

Component Oriented Programming (COP) is a technique for software development that consist on combining independent entitied, called components, in order to build an app.

### What is Immutability and why it is important in React?

Complete

### What is the Virtual DOM?

The VirtualDom, like the DOM, is a node tree that list the webpage elements as objects. reactJS uses the VirtualDOM to compare the changes in the state and props and determinate which updates send to the real DOM for repainting or re-rendering the UI.

### What is the Reconciliation in React?

Complete

### What is Redux?

- Redux is a store manager in reactJS applications. It is a structure that helps to clarify the code when your app scalates. In this structure, there is a `store` where all state variables of all the components can be stored. Then, the components can `connect` to that store and access to them. That way, when a component needs to access a state variable, there is no need to pass it as a prop from parent to child (sometimes in multiple levels) or refactor DOM structure. The component just access to the store and access to the variable.
- Redux is also an architecture that is related to the data flow direction. The data flow is unidirectional. In a Redux app, the data flow is:
  - Initial situation: the `state` describes the condition of the app at a specific point and the `UI` is rendered based on that state.
  - When something happens in the app, such as a user clicking a button, an action is created by an `actionCreator`. Then, that action is `dispatched` to the Redux store, like `dispatch({type: 'SAY_HELLO'})`.
  - The store runs the `reducer` function again with the previous state and the current action, and saves the return value as the new state.
  - The UI renders the changes based on the new `state`. So we go back to the beginning of the cycle.

### What is a HOC (High order component)?

A High Order Component (HOC) is a function that takes a component as parameter and returns another component. For example, the `connect` function in `Redux` is a HOC.

### What is a middleware?

Complete

### What is redux-saga?

It is a redux middleware. It is a javascript library that aims to make app side effects easier to manage, to test, to handle and more efficient. The mental model is like each saga is a separated thread only responsible for side effects. It uses ES6 generators.

### What is redux-thunk?

It is a Redux middleware that allows to handle asynchronicity (because vanilla Redux does not handle asynchronicity).

In redux-thunk it is posible to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.

### What is react-native?

It is a JS framework for writing mobile apps for iOS and Android. It uses reactJS principes and syntax.

### What is different in react-native from react?

- In react-native there is no DOM. Instead, react-native uses a native API to render components.
- react-native does not use HTML or CSS. Instead, there are native views.
- The navigation: in react-native there is a stack of views and the user navigates throw those views.
- All stuff related to hardware usage: camera, microphone, GPS, etc.
