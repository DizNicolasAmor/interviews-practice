# INTERVIEW QUESTIONS

## FRONTEND

### Javascript

**What does "data type" mean and how many data types are in JS?**
Data type in programming is a classification that is used for specifying with kind of operation can be done with a given value.
In Javascript we have 6 different primitive data types:
1. string
2. boolean
3. number
4. null
5. Symbol
6. undefined

Complete

**What is hoisting?**
Is a javascript mechanism where variables and function declarations are moved to the top of their scope before code execution.


**What is Scope?**
It's a policy that manages the availability of variables.
In javascript we have different scopes:
1. Block scope - Using let and const.
2. Function scope - Using let, const and var.
3. Module scope - For variables, functions and classes.
4. Global scope - Is accessible from everywhere, examples: `window` object in browser and `process` object in nodejs.
5. Lexical scope - Is determined statically by the position of the variables within the nested function scopes.


Complete

**What is the Event loop?**
It's the process of dispatching events and executing instructions in a javascript program.


Complete

**Explain Apply, Bind and Call functions**
1. Bind: Creates a new function with a new context assigned by the first argument on `bind` invocation.
2. Call: Call a function with a new context assigned by the first argument.
3. Apply: It's the same as `call` but `apply` taskes an array as a unique argument where the first position is the new context and the rest of them are the arguments.


Complete

**What is Closure?**
It's a combination of a function bundled together with references to its surrounding state.
Basically it's a function that is created inside another one.

**What is Immutability?**
Immutability is an attribute that forbids a data type mutation.

Complete

**How to copy an object?**
We can use a mix of `JSON.parse` and `JSON.stringify` methods to copy an object with any level of deepness. However this is a naive solution.
We also have the method `assign` from the global object `Object` with it we can copy objects with 1 level of deepness in a very performant way.
For object with greeter than 1 level of deepness we have to use another solution as a recursive `Object.assign` call.
Speaking about third-party solutions we could use `lodash.merge` method to achieve that too.

Complete

**What is a HOF (high order function)?**
A high order function is a function that takes at least one function as an argument or returns a function.

Complete

**What is the difference between map, reduce and forEach functions?**

Complete

**What is ECMAScript?**

Complete

**Mention some of the new features in ES6**

Complete

**Mention some of the new features in ES11 (ES 2020)**

Complete

**What are the differences between var, let and const?**
1. `var` declarations are globally scoped or function scoped while `let` and `const` are block scoped.
2. `var` variables can be updated and re-declared within its scope, `let` variables can be updated but not re-declared
    and `const` variables can neither be updated nor re-declared.
3. All of them are hoisted to the top of their scope. But while `var` v ariables are initialized with `undefined`, `let` and `const` variables
    are not initialized.
4. While `var` and `let` can be declared without being initialized, `const` must be initialized during declaration.

Complete

**What are the difference between an arrow function and a traditional function?**

Complete

**What is a Promise?**

Complete

**How a Promise can be consumed?**

Complete


### React

**What is React?**

Complete

**What is COP (component oriented programming)?**

Complete

**What is Immutability and why it is important in React?**

Complete

**What is the Virtual DOM?**

Complete

**What is the Reconciliation in React?**

Complete

**What is Redux?**

Complete

**What is a HOC (High order component)?**

Complete

**What is a middleware?**

Complete

**What is redux-saga?**

Complete

**What is redux-thunk?**

Complete

**What is react-native?**

Complete

**What is different in react-native from react?**

Complete


## METHODOLOGIES

**Question**

Answer


## BACKEND

### Node

**Question**

Answer

### Python

**Question**

Answer


## DATA STRUCTURES

**Question**

Answer


## SOFT SKILLS

**Question**

Answer
