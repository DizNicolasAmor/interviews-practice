# RUST

## TABLE OF CONTENTS

- [BASIC](#basic)
    1. What is Rust, and what makes it different from other programming languages?
    2. What is the ownership system in Rust and how it helps prevent memory errors?
    3. What are the basic data types in Rust, and how are they used?
    4. What is a trait in Rust?
    5. Differences between traits in Rust and interfaces in other programming languages?
    6. How does Rust handle error handling, and what are the main ways to propagate errors in Rust?
    7. Mutable and immutable variables in Rust?
    8. What is a closure and how is it used?
    9. What is a struct and an enum?
    10. How does Rust handle concurrency and parallelism, and what are the main concurrency primitives?
    11. How do the borrowing rules prevent data races?
- [INTERMEDIATE](#INTERMEDIATE)
    12. What is the concept of "unsafe" code and when it is appropriate to use it?
    13. How does Rust ensure memory safety and prevent common programming errors such as null pointers and data races?
    14. Vec VS Array
    15. How to handle error propagation between functions?
    16. What are Lifetimes in Rust and how they are used?
    17. How to write a custom macro in Rust?
    18. How do you approach writing efficient Rust code?
    19. Closure VS function
    20. Option VS Result and when to use each one?
    21. Rust testing framework
    22. What is the Module system and how it can be used to organize code?
- [ADVANCED](#ADVANCED)
    23. What is Rust's low-level control of hardware and how it can be used in system programming?
    24. How Rust's type system enables zero-cost abstractions and how this can improve performance?
    25. How Rust's memory layout and alignment works and how it affects performance and portability?
    26. How to use FFI capabilities to interact with foreign languages?
    27. How Rust's macros can be used to generate code and improve code readability and maintainability?
    28. What is lifetime elision rules and when to use explicit lifetime annotations in code?
    29. Have you ever used Rust's unsafe features to optimize performance-critical code? If so, give an example.
    30. How trait system enables generic programming and how this can be used to write reusable code?
    31. Can you explain Rust's monomorphization process and how it can improve performance by eliminating dynamic dispatch overhead?
    32. What is Rust's procedural macro system and how it can be used to generate code at compile-time?
    33. Have you ever used Rust's code-generation capabilities to generate code for specific hardware architectures? If so, can you give an example of a project you worked on?

<a name="basic" />

## BASICS

### 1. What is Rust, and what makes it different from other programming languages?

Rust is a low-level programming language that was first introduced by Mozilla in 2010. It is designed to be fast, safe, and concurrent, with a focus on performance, memory safety, and thread safety.

One of the main features that sets Rust apart from other programming languages is its ownership system, which enables fine-grained control over memory allocation and deallocation, without the need for a garbage collector. This system helps prevent common errors like null pointer dereferencing and data races, which are often the cause of security vulnerabilities and program crashes in other languages.

Rust offers a number of other advanced features, including pattern matching, closures, traits, and macros, that make it a versatile and powerful language for a wide range of applications. Overall, Rust is a modern programming language that combines performance, safety, and expressiveness.

### 2. What is the ownership system in Rust and how it helps prevent memory errors?

The ownership system in Rust tracks the ownership of heap-allocated memory and ensures that memory is properly deallocated when it is no longer needed. This helps prevent memory errors like null pointer dereferencing and use-after-free errors, which can cause crashes and security vulnerabilities.

### 3. What are the basic data types in Rust, and how are they used?

The basic data types are:

- **Booleans**: `bool`, which can be either true or false. Commonly used in conditional statements and loops.
- **Characters**: `char`, which represents a Unicode scalar value. Commonly used to represent text.
- **Numeric**: `i8`, `i16`, `i32`, `i64`, `i128`, `u8`, `u16`, `u32`, `u64`, `u128`, `f32`, and `f64`. Commonly used for arithmetic operations and to represent values like counts, sizes, and indices.
- **Arrays**: fixed-size sequences of elements of the same type. Commonly used to group values together into collections.
- **Tuples**: heterogeneous collections of values of different types. Commonly used to group values together into collections.

### 4. What is a trait in Rust?

It is a language construct that defines a set of behaviors or capabilities that a type can implement. Traits are similar to interfaces in other programming languages in that they provide a way to specify a contract that a type must follow in order to be considered a member of a particular group.

### 5. Differences between traits in Rust and interfaces in other programming languages?

- **Implementation**: In Rust, a trait can be implemented for any type, including types that are not defined in the same module as the trait itself. This is different from interfaces in some other languages, which are often tightly bound to the class or type that implements them.
- **Associated Types**: Traits in Rust can define associated types, which allow the trait to specify a type that will be used in conjunction with the methods defined in the trait. This can be useful in situations where the type that will be used with the trait is not known at the time the trait is defined.
- **Default Implementations**: Traits in Rust can include default implementations for some or all of their methods. This can make it easier to implement the trait for a new type, since the default implementations can be used as a starting point.
- **OOP**: Rust does not have built-in support for OOP concepts like inheritance and polymorphism. Traits can be used to provide some of the same functionality, but the approach is different from traditional OOP languages.

### 6. How does Rust handle error handling, and what are the main ways to propagate errors in Rust?

Rust uses a combination of return values and the `Result` enum to handle errors. The `Result` enum has two variants: `Ok` and `Err`, which can be used to represent a successful result or an error, respectively.

The main ways to propagate errors in Rust are through `Result` return values, `panic!` macro, `unwrap` and `expect` methods, and the `?` operator, which is shorthand for unwrapping a Result and returning the error if it is an Err variant.

Rust encourages explicit error handling to avoid unexpected panics and to make code more reliable and robust.

### 7. Mutable and immutable variables in Rust?

Immutable variables:

- They are declared with the `let` keyword and cannot be modified once they are assigned a value.
- Useful for situations where the value should not change, such as constants or function parameters.

Mutable variables:

- They are declared with the `let mut` keyword and can be modified after they are assigned a value.
- Useful when the value needs to be modified during the program execution, such as when updating a counter or performing calculations.

Rust's ownership and borrowing system ensures that mutable variables are only modified in safe and controlled ways, preventing common errors like data races and null pointer exceptions.

### 8. What is a closure and how is it used?

A closure is a type of anonymous function that can capture variables from its surrounding environment. The name "closure" referes to the values that are enclosed to the scope of that function.

Closures are defined using the `|args|` expression syntax and can be stored in variables or passed as arguments to other functions.

They are commonly used for operations that require some context or state, such as filtering or mapping collections.

### 9. What is a struct and an enum?

| CRITERIA       | STRUCT                         | ENUM                                   |
| -------------- | ------------------------------ | -------------------------------------- |
| Definition     | A custom data type with fields | A custom data type with variants       |
| Fields         | Can have named fields          | Can have named or unnamed fields       |
| Variants       | N/A                            | Can have multiple variants             |
| Associated Fn  | Yes                            | Yes                                    |
| Implementation | Can be instantiated directly   | Must be instantiated through a variant |
| Usage          | For grouping data              | For representing a set of values       |

### 10. How does Rust handle concurrency and parallelism, and what are the main concurrency primitives?

Concurrency is about managing multiple tasks at the same time, while parallelism is about executing multiple tasks simultaneously.

Rust provides a powerful concurrency and parallelism model through its ownership and borrowing system and its support for low-level threading primitives. The ownership and borrowing system ensures that concurrent access to data is safe and free of data races.

The main concurrency primitives in Rust are:

- **Threads** can be created using the `std::thread` module and allow for parallel execution of multiple functions or closures.
- **Channels** allow for communication between threads
- **Locks** provide a way to synchronize access to shared resources.

Rust also provides abstractions like `Futures` and `async/await` syntax to work with asynchronous programming, which allows for concurrent execution without creating multiple threads.

### 11. How do the borrowing rules prevent data races?

They prevent data races by ensuring that only one mutable reference or any number of shared references can exist at any given time for a given piece of data.

This ensures that the data is not modified while it is being read and that multiple mutable references cannot exist simultaneously, preventing write-write data races.

Additionally, Rust's ownership model ensures that data is not accessed after it has been freed, preventing read-after-free data races.

<a name="intermediate" />

## INTERMEDIATE

### 12. What is the concept of "unsafe" code and when it is appropriate to use it?

In Rust, "unsafe" is a keyword used to indicate code that can potentially violate memory safety and other language invariants. It should only be used when necessary for implementing low-level system interfaces or performance-critical operations, and must be accompanied by careful manual memory management and other safety checks.

### 13. How does Rust ensure memory safety and prevent common programming errors such as null pointers and data races?

Rust ensures memory safety through ownership and borrowing, lifetimes, safe abstractions, and compiler checks.

1. Ownership and Borrowing: ownership means that each value is only modified by a single owner at a time. Additionally, borrowing system allows for temporary access to values without transferring ownership.
2. Lifetimes: this tool tracks the lifetime of a value and ensure that references to that value are only used while it is valid.
3. Safe Abstractions: it automatically handle memory management and safety for common programming patterns, such as strings and vectors.
4. Compiler Checks: Rust's compiler performs a variety of static checks to prevent common programming errors.

### 14. Vec VS Array

| Feature       | Vec                   | Array                  |
| ------------- | --------------------- | ---------------------- |
| Size          | Dynamic               | Fixed                  |
| Allocation    | Heap                  | Stack                  |
| Element Types | Flexible              | Same                   |
| Resize        | Yes                   | No                     |
| Efficiency    | Lower for small sizes | Higher for small sizes |

### 15. How to handle error propagation between functions?

Using the `Result` type.

A function that can produce an error returns a `Result` enum, which can either contain an `Ok` value representing the successful result, or an `Err` value containing the error. The calling function can then use pattern matching to handle the error, either by propagating it further up the call stack or by handling it directly. The `?` operator can also be used to propagate errors automatically, allowing for concise error handling code.

### 16. What are Lifetimes in Rust and how they are used?

Lifetimes are a mechanism for tracking the lifetime of a variable and ensuring that references to it are only used while it is valid. Lifetimes are used to prevent dangling pointer errors and other memory safety issues. They are specified using a special syntax:

```
fn foo<'a>(x: &'a str) -> &'a str {
    // code
}
```

### 17. How to write a custom macro in Rust?

```
macro_rules! say_hello {
    () => {
        println!("Hello, world!");
    };
}
```

### 18. How do you approach writing efficient Rust code?

- Use appropriate data structures
- Avoid unnecessary copying of data. Instead, use references or borrow the data.
- Avoid unnecessary allocations.
- Optimize hot code paths.
- Profile and measure. Use profiling tools to identify bottlenecks.
- Write idiomatic Rust.
- Stay up to date.

### 19. Closure VS function

In Rust, Closures are similar to Functions but with some key differences. Closures are defined inline, can capture variables from their surrounding scope, and can have their own unique types. Functions, on the other hand, are standalone units of code with a fixed signature and cannot capture variables from their surrounding scope.

### 20. Option VS Result and when to use each one?

`Option` and `Result` are two enum types used to handle errors and absent values.

- **Option** is used to represent a value that may or may not be present. It can either be `Some(value)` or `None`. Option is useful when a value may or may not exist and allows for handling of these cases in a concise and safe way. Option is used when there is a possibility of no value.
- **Result** is used to represent an operation that may or may not succeed. It can either be `Ok(value)` or `Err(error)`. Result is useful when an operation may fail and allows for handling of errors in a concise and safe way. Result is used when there is a possibility of failure.

### 21. Rust testing framework

Rust has a built-in testing framework that allows developers to write tests for their code. Tests are defined using the `#[test]` attribute and can be run using the `cargo test` command. The testing framework includes support for running tests in parallel, testing both successful and error cases, and generating code coverage reports.

### 22. What is the Module system and how it can be used to organize code?

It is a system used to organize code into a logical structure that can be easily navigated and maintained. Modules can be defined using the `mod` keyword and can be nested to create a hierarchy. Modules can contain types, functions, constants, and other modules, and their visibility can be controlled using the `pub` keyword.

<a name="advanced" />

## ADVANCED

### 23. What is Rust's low-level control of hardware and how it can be used in system programming?

Rust's low-level control of hardware allows developers to write system-level programs that have direct access to hardware resources. Rust provides support for writing low-level code using the unsafe keyword, which allows for manual memory management, direct access to hardware registers, and other low-level operations.

### 24. How Rust's type system enables zero-cost abstractions and how this can improve performance?

In Rust, zero-cost abstractions are achieved through mechanisms such as generic programming, trait bounds, and monomorphization, which enable the compiler to generate specialized code for each use case, while still maintaining safety and correctness.

### 25. How Rust's memory layout and alignment works and how it affects performance and portability?

Memory layout and alignment rules define how data is organized in memory and affect performance and portability.

- Memory is typically aligned to the largest primitive component, with padding as needed.
- Proper alignment can improve performance by enabling the CPU to load and store data in larger chunks.
- Rust's ownership model can enable aggressive optimizations, such as eliminating unnecessary memory copies.
- The `#[repr(C)]` attribute can ensure compatibility with `C`.
- Rust's rules balance performance, portability, type safety, and memory safety.

### 26. How to use FFI capabilities to interact with foreign languages?

Rust's FFI (Foreign Function Interface) capabilities enable Rust code to interact with code written in other languages, such as C and C++.

To use it, the `extern` keyword is used to define external functions or variables, and the `unsafe` keyword is used to indicate that the function may have side effects or violate Rust's safety rules. Additionally, Rust's `std::ffi` module provides facilities for working with C-style strings and pointers.

### 27. How Rust's macros can be used to generate code and improve code readability and maintainability?

### 28. What is lifetime elision rules and when to use explicit lifetime annotations in code?

### 29. Have you ever used Rust's unsafe features to optimize performance-critical code? If so, give an example.

### 30. How trait system enables generic programming and how this can be used to write reusable code?

### 31. Can you explain Rust's monomorphization process and how it can improve performance by eliminating dynamic dispatch overhead?

### 32. What is Rust's procedural macro system and how it can be used to generate code at compile-time?

### 33. Have you ever used Rust's code-generation capabilities to generate code for specific hardware architectures? If so, can you give an example of a project you worked on?
