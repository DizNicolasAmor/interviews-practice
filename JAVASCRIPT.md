# JAVASCRIPT

## TABLE OF CONTENTS

- [Paradigm](#paradigm)
  1. What is Javascript?
  2. What is OOP?
  3. Is JS OOP or Prototype oriented?
  4. Class-based OOP VS Prototype-based OOP
- [Concepts](#concepts)
  5. What does "data type" mean and how many data types are in JS?
  6. What is hoisting?
  7. What is Scope?
  8. What is Closure?
  9. What is a Javascript Hosting Environment?
  10. What is the Event loop?
  11. How does the Event loop work in Javascript?
  12. Microtask and Macrotask
  13. Explain Apply, Bind and Call functions
  14. What is Immutability?
  15. How to copy an object?
  16. What is a HOF (high order function)?
  17. What is the difference between map, reduce and forEach functions?
  18. What is a Promise?
  19. How a Promise can be consumed?
- [ECMAScript](#ecmascript)
  20. What is ECMAScript?
  21. Mention some of the new features in ES6 (ES 2015)
  22. Mention some of the new features in ES11 (ES 2020)
  23. What are the differences between var, let and const?
  24. What are the difference between an arrow function and a regular function?

<a name="paradigm"/>

## Paradigm

### 1. What is Javascript?

JavaScript is a programming language that is mainly used for Web applications.

It is a high-level, often just-in-time compiled language that conforms to the ECMAScript standard. It has dynamic types, prototype-based object-orientation, and first-class functions. It is multi-paradigm, supporting event-driven, functional, and imperative programming styles. It has APIs for working with text, dates, reges and the DOM.

### 2. What is OOP?

Object Oriented Programming (OOP) is a programming paradigm based on the concept of "objects", which can contain attributes (or properties) and methods. It is based on the main principles:

- **Encapsulation**. This principle states that all important information is contained inside an object and only select information is exposed.
- **Abstraction**. Objects only reveal internal mechanisms that are relevant for the use of other objects, hiding any unnecessary implementation code. The derived class can have its functionality extended. This concept can help developers more easily make additional changes or additions over time.
- **Inheritance**. Classes can reuse code from other classes.
- **Polymorphism**. Objects are designed to share behaviors and they can take on more than one form. A child class that extends the functionality of the parent class could overwrite a method with a particular behavior.

### 3. Is JS OOP or Prototype-oriented programming?

There is no such thing as Prototype-oriented programming paradigm.

**Javascript is multiparadigm**, that means it supports various programming paradigms and **OOP** is one of them. **Prototype-based** programming is a style of OOP, just like **class-based**.

### 4. Class-based OOP VS Prototype-based OOP

JavaScript does not have real classes per se. Instead, it uses the concept of **prototypes** for handling inheritance.

On the one hand, in class-based OOP a class defines the structure of the objects that will be instanciated from that class. And a class can extend characteristics from other parent classed. It is more structural. On the another hand, in Prototype-based OOP there is a real object that it is the Prototype, that is reused by new objects. It is more flexible.

Here is how this two styles approach the OOP main principles:

- **Abstraction**: in Class-based style abstraction is handled via interfaces and abstract classes, while in Prototype-based style like Javascript, it is handled with the concept of **closure**.
- **Encapsulation**: in Class-based style there are specific keywords and methods to handle encapsulation, while in Prototype-based style like Javascript it is handled with the concept of **closure**.
- **Inheritance**:
  - On the one hand, in Prototype-based style, inheritance is attached to a live working object called prototype or __proto__ and accessed by all the children. Objects do not get copies of inherited behaviors, they receive the prototype object, and can be changed later.
  - On the another hand, in Class-based style the objects instantiated from a class receive a copy of the class characteristics and they cannot be changed later, so it is important to plan the class structure before start instantiations.
- **Polymorphism**
  - In Javascript (Prototype-style) it is performed using **Prototype chaining**:

  | When we try to read or write something on an object JS engine will firstly look for that property in the object. If found then the search will stop and will return the property. Else it will go to the object’s prototype will search among its properties if not found then will go to prototype’s prototype and so on… until it reaches to null if found anywhere it will stop there and return the property, if not found till the end it will return *undefined*.

  - In class-based style there are other types of polymorphism: runtime, overloading, compile-time and casting.

<a name="concepts"/>

## Concepts

### 5. What does "data type" mean and how many data types are in JS?

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

### 6. What is hoisting?

Is a javascript mechanism where variables and function declarations are put in the memory before the code execution. For the coder, it is like the variable declarations are moved to the top of their scope.

### 7. What is Scope?

It's a policy that manages the availability of variables. That means, it is the specific environment where a variable is accessible and can be used. In javascript we have different scopes:

1. Block scope - Using let and const.
2. Function scope - Using let, const and var.
3. Module scope - For variables, functions and classes.
4. Global scope - Is accessible from everywhere, examples: `window` object in browser and `process` object in nodejs.
5. Lexical scope - Is determined statically by the position of the variables within the nested function scopes.

### 8. What is Closure?

It's a combination of a function bundled together with references to its surrounding state. Basically it's a function that is created inside another one. The outer function is said to "enclose" the scope of the inner function.

### 9. What is a Javascript Hosting Environment?

It's where a JS Engine runs. It consists in the JS Engine itself, a set of environment API's and the Event loop.
Environment API's depends on the context. In a web browser for example we are able to use `onclick` events, in Node Js, file operations such as read, write, delete, etc...

### 10. What is the Event loop?

It's the process of dispatching events and executing instructions in a javascript program.

### 11. How does the Event loop work in Javascript?

The event loop is the process of monitoring 2 parts of a Javascript hosting environment (such as Node js or a Web Browser), those 2 parts are, the **CallStack** and the **Callback Queue**.

The CallStack is where the event loop puts each function call and it follows a LIFO approach to process functions. It means the last function that is executed is the first one that is removed from the CallStack.

The Callback Queue is another place in which function calls are placed to be processed once the CallStack is empty. The Callback Queue follows a FIFO approach to process callback functions, it means that the first function that is added to de queue is the first one that is removed from it. Is used for different environment API's like `setTimeout`, `fetch` or `file.read` to put callback functions inside it once they're required.

In example:

`setTimeout` will put a callback function at the end of the Callback Queue once the timeout value is reached. Once the `setTimeout` callback is added into the Callback Queue, the event loop will wait until the CallStack is empty, when it happens, the event loop will move the `setTimeout` callback from the Callback Queue to the CallStack to be processed by the Javascript Engine.

### 12. Microtask and Macrotask

Inside the **task queue**, the tasks are broadly classified into two categories, namely **microtasks** and **macrotasks**.

**Microtasks**

A microtask is a function which is executed after the function or program which created it exits and only if the JavaScript execution stack is empty, but before returning control to the event loop being used by the user agent to drive the script’s execution environment. A Microtask is also capable of en-queuing other micro-tasks.

Microtasks are often scheduled for things that are required to be completed immediately after the execution of the current script. On completion of one macrotask, the event loop moves on to the microtask queue. The event loop does not move to the next task outside of the microtask queue until all tasks are completed. This implies that the microtask queue has a higher priority.

Once all the microtask are finished, only then does the event loop shifts back to the macrotask queue. The primary reason for this is to improve the user experience.

**Usage cases**

— process.nextTick
- Promises
- queueMicrotask
- MutationObserver

**Macrotasks**.

Macrotask represents some discrete and independent work. These are always executed after the microtask queue is empty.

**Usage cases**

- setTimeout
- setInterval
- setImmediate
- requestAnimationFrame
- I/O (for example the "fetch" method)
- UI Rendering

**Example**

```
function whatIsTheOrder() {
    new Promise((_, reject) => reject())
        .catch(() => { console.log('a') });

    setTimeout(() => { console.log('b') }, 0);

    new Promise((resolve) => resolve())
        .then(() => { console.log('c') });

    console.log('d');
}
```

The log will be: `d a c b`.

### 13. Explain Apply, Bind and Call functions

1. Bind: Creates a new function with a new context assigned by the first argument on `bind` invocation.
2. Call: Call a function with a new context assigned by the first argument.
3. Apply: It's the same as `call` but `apply` taskes an array as a unique argument where the first position is the new context and the rest of them are the arguments.

### 14. What is Immutability?

Immutability is an attribute that forbids a data type mutation.

### 15. How to copy an object?

It depends on the object.

- For an object with only primitive values, you could simply use `Object.assign` or the `spread operator`.
- For an object with many primitive values and only a few complex values, you could use the same tools than before and then override (copy) the specific properties with complex values.
- For an object with complex levels of deepness you could use a custom function with a recursive `Object.assign` call.
- Also, you could use third-party solutions from libraries like `lodash`.
- You could use a mix of `JSON.parse` and `JSON.stringify` methods to copy an object with any level of deepness. However this is a naive solution and there are some issues in border cases.

### 16. What is a HOF (high order function)?

A High Order Function is a function that either takes a function as an argument or returns a function.

### 17. What is the difference between map, reduce and forEach functions?

The `map` method receives a function as a parameter. Then it applies it on each element and returns a new array populated
with the results of calling the provided function. In the case of `forEach` method, it receives a function as a parameter with each array value and returns `undefined`, its proupouse is only iterate an array. And finally `reduce` method is used to reduce the array to a single value, it executes a provided function for each value of the array (from left-to-right) and the return value of the function is stored in an accumulator.

### 18. What is a Promise?

A promise is a function that will return data in some future.

### 19. How a Promise can be consumed?

- Using `then / catch`: you can call the `then` method and pass a callback as a param. The callback will be executed when the promise resolves. After that you can use the`catch` method. Same criteria, but the catch callback will be executed if the promise rejects.
- Using `async / await`: declare an `async` function and inside of it you can use the `await` keyword before your promise.
- Using a generator: you can declare a generator function and consume the promise inside of it, with the yield keyword.

<a name="ecmascript"/>

## ECMAScript

### 20. What is ECMAScript?

Ecmascript (European Computer Manufacturer's Association) is a standard for scripting languages.

### 21. Mention some of the new features in ES6

1. Arrow functions
2. Template strings
3. Let and const keywords.
4. Symbols

### 22. Mention some of the new features in ES11 (ES 2020)

1. Optional chaining
2. Dynamic imports
3. Promise.allSettled
4. Global this.

### 23. What are the differences between var, let and const?

1. `var` declarations are globally scoped or function scoped while `let` and `const` are block scoped.
2. `var` variables can be updated and re-declared within its scope, `let` variables can be updated but not re-declared
   and `const` variables can neither be updated nor re-declared.
3. All of them are hoisted to the top of their scope. But while `var` variables are initialized with `undefined`, `let` and `const` variables are not initialized.
4. While `var` and `let` can be declared without being initialized, `const` must be initialized during declaration.

### 24. What are the difference between an arrow function and a regular function?

They have the following differences:

1. Arrow function have different syntax.
2. Regular functions have an `arguments` binding and arrow functions only have access to `arguments` objects of the closest non-arrow parent function.
3. Arrow ones have "lexical this". Basically in an arrow function, the value of `this` is always inherited from the enclosing scope. In regular functions, the value of `this` is defined whyen it's being executed and it depends on where it has been executed from.
4. Arrow functions are only callable and regular functions are either callable and constructible (can be invoked with the `new` keyboard).
