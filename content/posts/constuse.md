---
title: "The very basics of constexpr"
date: 2020-04-23T21:01:20+05:30
draft: false 
toc: false
images:
tags:
  - untagged
---

## Introduction to constexpr

C++11 introduced the concept of constexpr, which to put it broadly, evaluates functions and objects at compile time.

Simply put, a constexpr object declaration indirectly means it is declared as const, whereas a constexpr function declaration means it is implicitly declared inline( functions which replace the function call with the function code, thus saving overhead.).

constexpr saves a ton of runtime and since they act in compile time are implicitly thread safe.

A confusion I had was the difference between constexpr and const. A const keyoword specifies that a particular object or variable is unmodifiable, which is a subset of constexpr behaviour.

Over the years, the newer versions of C++ standard have added a steady flux of constexpr compatibility and features. 

For example, in C++11 constexpr functions were only allowed one return statement, whereas from C++14, multiple return statements were allowed.

## Why constexpr ?

* Saves a lot of runtime.
* Are implicitly thread-safe.
* Can be constructed in read-only memory.

## How to constexpr ?

The basic use is prety simple, just use the constexpr keyword before any function or variable declaration.

It is important to note that all object declarations inside a constexpr function must be initialized.

Also, a constexpr function can only call other constexpr functions and not runtime ones (which is obvious).

`constexpr int foo = 42` is the same as `int constexpr foo = 42`

## C++20 newer constexpr features
* constexpr virtual functions.
* constexpr union, try and catch, dynamic\_cast, typeid and std::pointer\_traits.
* constexpr additions.
* std::string and std:: vector have been constexpr-ed.
* constexpr <numeric> library algorithms.

## Some interesting talks and resources about constexpr
[Ben Deane and Jason Turner's CppCon 2017 talk : constexpr ALL things](https://www.youtube.com/watch?v=PJwd4JLYJJY)

[Jason Turner's Meeting C++ 2017 talk : Practical constexpr](https://www.youtube.com/watch?v=xtf9qkDTrZE)

[constexpr cppreference page](https://en.cppreference.com/w/cpp/language/constexpr)

[Rainer Grimm's article](https://www.modernescpp.com/index.php/c-core-guidelines-programming-at-compile-time-with-constexpr)

