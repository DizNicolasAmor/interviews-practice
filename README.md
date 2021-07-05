# INTERVIEW QUESTIONS

## FRONTEND

### Javascript

- **What does "data type" mean and how many data types are in JS?**

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

- **What is hoisting?**

Is a javascript mechanism where variables and function declarations are put in the memory before the code execution. For the coder, it is like the variable declarations are moved to the top of their scope.

- **What is Scope?**

It's a policy that manages the availability of variables. That means, it is the specific environment where a variable is accessible and can be used. In javascript we have different scopes:

1. Block scope - Using let and const.
2. Function scope - Using let, const and var.
3. Module scope - For variables, functions and classes.
4. Global scope - Is accessible from everywhere, examples: `window` object in browser and `process` object in nodejs.
5. Lexical scope - Is determined statically by the position of the variables within the nested function scopes.

- **What is Closure?**

It's a combination of a function bundled together with references to its surrounding state. Basically it's a function that is created inside another one. The outer function is said to "enclose" the scope of the inner function.

- **What is the Event loop?**

It's the process of dispatching events and executing instructions in a javascript program.

- **How does the Event loop work in Javascript?**

Answer.

- **Explain Apply, Bind and Call functions**

1. Bind: Creates a new function with a new context assigned by the first argument on `bind` invocation.
2. Call: Call a function with a new context assigned by the first argument.
3. Apply: It's the same as `call` but `apply` taskes an array as a unique argument where the first position is the new context and the rest of them are the arguments.

- **What is Immutability?**

Immutability is an attribute that forbids a data type mutation.

- **How to copy an object?**

It depends on the object.

  - For an object with only primitive values, you could simply use `Object.assign` or the `spread operator`.
  - For an object with many primitive values and only a few complex values, you could use the same tools than before and then override (copy) the specific properties with complex values.
  - For an object with complex levels of deepness you could use a custom function with a recursive `Object.assign` call.
  - Also, you could use third-party solutions from libraries like `lodash`.
  - You could use a mix of `JSON.parse` and `JSON.stringify` methods to copy an object with any level of deepness. However this is a naive solution and there are some issues in border cases.

- **What is a HOF (high order function)?**

A High Order Function is a function that either takes a function as an argument or returns a function.

- **What is the difference between map, reduce and forEach functions?**

Complete

- **What is ECMAScript?**

Complete

- **Mention some of the new features in ES6**

Complete

- **Mention some of the new features in ES11 (ES 2020)**

Complete

- **What are the differences between var, let and const?**

1. `var` declarations are globally scoped or function scoped while `let` and `const` are block scoped.
2. `var` variables can be updated and re-declared within its scope, `let` variables can be updated but not re-declared
    and `const` variables can neither be updated nor re-declared.
3. All of them are hoisted to the top of their scope. But while `var` v ariables are initialized with `undefined`, `let` and `const` variables
    are not initialized.
4. While `var` and `let` can be declared without being initialized, `const` must be initialized during declaration.

- **What are the difference between an arrow function and a traditional function?**

Complete

- **What is a Promise?**

Complete

- **How a Promise can be consumed?**

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
