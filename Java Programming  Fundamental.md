# Java Strings: An In-Depth Guide

## Table of Contents
- [Introduction to Java Strings](#introduction-to-java-strings)
- [Class, Object, Instance, and Methods](#class-object-instance-and-methods)
- [Basic Syntax for Strings](#basic-syntax-for-strings)
- [String Methods Explained](#string-methods-explained)
  - [1. `length()`](#1-length)
  - [2. `charAt()`](#2-charat)
  - [3. `substring()`](#3-substring)
  - [4. `indexOf()`](#4-indexof)
  - [5. `toLowerCase()`](#5-tolowercase)
  - [6. `toUpperCase()`](#6-touppercase)
  - [7. `trim()`](#7-trim)
  - [8. `replace()`](#8-replace)
  - [9. `contains()`](#9-contains)
  - [10. `equals()`](#10-equals)
- [Tasks for Practice](#tasks-for-practice)
  - [Task 1: Count Character Occurrences](#task-1-count-character-occurrences)
  - [Task 2: Check for Palindrome](#task-2-check-for-palindrome)
  - [Task 3: Extract Initials from Name](#task-3-extract-initials-from-name)
  - [Task 4: Replace Words in a Sentence](#task-4-replace-words-in-a-sentence)
  - [Task 5: Convert Sentence to Title Case](#task-5-convert-sentence-to-title-case)

---

## Introduction to Java Strings

In Java, a `String` is an object representing a sequence of characters. Java strings are immutable, meaning they cannot be altered after creation. This immutability ensures thread safety and reduces memory usage, as the same string literal can be reused.

## Class, Object, Instance, and Methods

- **Class**: A blueprint or template that defines a data type. For example, `String` is a class in Java.
- **Object**: An instance of a class, created using the `new` keyword or by directly assigning a string literal in the case of `String`.
- **Instance**: A specific realization of a class, like an individual `String` object.
- **Methods**: Functions defined within a class that operate on instances of that class. Methods allow you to perform operations like checking length, extracting substrings, and converting cases.

## Basic Syntax for Strings

Creating a `String` in Java can be done using a literal or the `new` keyword.

```java
// Using a literal
String text = "Hello, World!";

// Using the String class constructor
String text = new String("Hello, World!");

```
# Example Output
```java

public class Main {
    public static void main(String[] args) {
        String text = "Hello, World!";
        System.out.println(text);
    }
}
```
