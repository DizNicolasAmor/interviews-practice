# RUST

## TABLE OF CONTENTS

- [BASICS](#basics)
    - What is Rust, and what makes it different from other programming languages?
    - What is the ownership system in Rust and how it helps prevent memory errors?
    - What are the basic data types in Rust, and how are they used?
    - What is a trait in Rust?
    - Differences between traits in Rust and interfaces in other programming languages?
    - How does Rust handle error handling, and what are the main ways to propagate errors in Rust?
    - Mutable and immutable variables in Rust?
    - What is a closure and how is it used?
    - What is a struct and an enum?
    - How does Rust handle concurrency and parallelism, and what are the main concurrency primitives?
    - How do the borrowing rules prevent data races?

<a name="basics" />

## BASICS

### What is Rust, and what makes it different from other programming languages?

Rust is a low-level programming language that was first introduced by Mozilla in 2010. It is designed to be fast, safe, and concurrent, with a focus on performance, memory safety, and thread safety.

One of the main features that sets Rust apart from other programming languages is its ownership system, which enables fine-grained control over memory allocation and deallocation, without the need for a garbage collector. This system helps prevent common errors like null pointer dereferencing and data races, which are often the cause of security vulnerabilities and program crashes in other languages.

Rust offers a number of other advanced features, including pattern matching, closures, traits, and macros, that make it a versatile and powerful language for a wide range of applications. Overall, Rust is a modern programming language that combines performance, safety, and expressiveness.

### What is the ownership system in Rust and how it helps prevent memory errors?

The ownership system in Rust tracks the ownership of heap-allocated memory and ensures that memory is properly deallocated when it is no longer needed. This helps prevent memory errors like null pointer dereferencing and use-after-free errors, which can cause crashes and security vulnerabilities.

### What are the basic data types in Rust, and how are they used?

The basic data types are:

- **Booleans**: `bool`, which can be either true or false. Commonly used in conditional statements and loops.
- **Characters**: `char`, which represents a Unicode scalar value. Commonly used to represent text.
- **Numeric**: `i8`, `i16`, `i32`, `i64`, `i128`, `u8`, `u16`, `u32`, `u64`, `u128`, `f32`, and `f64`. Commonly used for arithmetic operations and to represent values like counts, sizes, and indices.
- **Arrays**: fixed-size sequences of elements of the same type. Commonly used to group values together into collections.
- **Tuples**: heterogeneous collections of values of different types. Commonly used to group values together into collections.

### What is a trait in Rust?

It is a language construct that defines a set of behaviors or capabilities that a type can implement. Traits are similar to interfaces in other programming languages in that they provide a way to specify a contract that a type must follow in order to be considered a member of a particular group.

### Differences between traits in Rust and interfaces in other programming languages?

- **Implementation**: In Rust, a trait can be implemented for any type, including types that are not defined in the same module as the trait itself. This is different from interfaces in some other languages, which are often tightly bound to the class or type that implements them.
- **Associated Types**: Traits in Rust can define associated types, which allow the trait to specify a type that will be used in conjunction with the methods defined in the trait. This can be useful in situations where the type that will be used with the trait is not known at the time the trait is defined.
- **Default Implementations**: Traits in Rust can include default implementations for some or all of their methods. This can make it easier to implement the trait for a new type, since the default implementations can be used as a starting point.
- **OOP**: Rust does not have built-in support for OOP concepts like inheritance and polymorphism. Traits can be used to provide some of the same functionality, but the approach is different from traditional OOP languages.

### How does Rust handle error handling, and what are the main ways to propagate errors in Rust?

Rust uses a combination of return values and the `Result` enum to handle errors. The `Result` enum has two variants: `Ok` and `Err`, which can be used to represent a successful result or an error, respectively.

The main ways to propagate errors in Rust are through `Result` return values, `panic!` macro, `unwrap` and `expect` methods, and the `?` operator, which is shorthand for unwrapping a Result and returning the error if it is an Err variant.

Rust encourages explicit error handling to avoid unexpected panics and to make code more reliable and robust.

### Mutable and immutable variables in Rust?

Immutable variables:

- They are declared with the `let` keyword and cannot be modified once they are assigned a value.
- Useful for situations where the value should not change, such as constants or function parameters.

Mutable variables:

- They are declared with the `let mut` keyword and can be modified after they are assigned a value.
- Useful when the value needs to be modified during the program execution, such as when updating a counter or performing calculations.

Rust's ownership and borrowing system ensures that mutable variables are only modified in safe and controlled ways, preventing common errors like data races and null pointer exceptions.

### What is a closure and how is it used?

A closure is a type of anonymous function that can capture variables from its surrounding environment. The name "closure" referes to the values that are enclosed to the scope of that function.

Closures are defined using the `|args|` expression syntax and can be stored in variables or passed as arguments to other functions.

They are commonly used for operations that require some context or state, such as filtering or mapping collections.

### What is a struct and an enum?

| CRITERIA       | STRUCT                         | ENUM                                   |
| -------------- | ------------------------------ | -------------------------------------- |
| Definition     | A custom data type with fields | A custom data type with variants       |
| Fields         | Can have named fields          | Can have named or unnamed fields       |
| Variants       | N/A                            | Can have multiple variants             |
| Associated Fn  | Yes                            | Yes                                    |
| Implementation | Can be instantiated directly   | Must be instantiated through a variant |
| Usage          | For grouping data              | For representing a set of values       |

### How does Rust handle concurrency and parallelism, and what are the main concurrency primitives?

Concurrency is about managing multiple tasks at the same time, while parallelism is about executing multiple tasks simultaneously.

Rust provides a powerful concurrency and parallelism model through its ownership and borrowing system and its support for low-level threading primitives. The ownership and borrowing system ensures that concurrent access to data is safe and free of data races.

The main concurrency primitives in Rust are:

- **Threads** can be created using the `std::thread` module and allow for parallel execution of multiple functions or closures.
- **Channels** allow for communication between threads
- **Locks** provide a way to synchronize access to shared resources.

Rust also provides abstractions like `Futures` and `async/await` syntax to work with asynchronous programming, which allows for concurrent execution without creating multiple threads.

### How do the borrowing rules prevent data races?

They prevent data races by ensuring that only one mutable reference or any number of shared references can exist at any given time for a given piece of data.

This ensures that the data is not modified while it is being read and that multiple mutable references cannot exist simultaneously, preventing write-write data races.

Additionally, Rust's ownership model ensures that data is not accessed after it has been freed, preventing read-after-free data races.
