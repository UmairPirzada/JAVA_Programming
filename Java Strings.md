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
 - [Task 1: Count Total Characters](#task-1-count-total-characters)
  - [Task 2: Find First Character](#task-2-find-first-character)
  - [Task 3: Extract Part of a Word](#task-3-extract-part-of-a-word)
  - [Task 4: Replace Letters in a Word](#task-4-replace-letters-in-a-word)
  - [Task 5: Convert Text to Uppercase](#task-5-convert-text-to-uppercase)

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

### Output:

Hello, World!


# String Methods Explained
Here are 10 useful String methods with explanations and code examples:

### 1. length()
Returns the number of characters in a string.

```java
String text = "Hello";
int length = text.length();
System.out.println("Length: " + length);
// Output: Length: 5
```

### 2. charAt(int index)
Returns the character at the specified index.
```java
String text = "Hello";
char ch = text.charAt(1);
System.out.println("Character at index 1: " + ch);
 // Output: Character at index 1: e
```

### 3. substring(int start, int end)
Extracts a part of the string from the start index up to, but not including, the end index.
```java
String text = "Hello, World!";
String sub = text.substring(0, 5);
System.out.println("Substring: " + sub);
 // Output: Substring: Hello
```

### 4. indexOf(String str)
Returns the index of the first occurrence of the specified substring.

```java
String text = "Hello, World!";
int index = text.indexOf("World");
System.out.println("Index of 'World': " + index);
 // Output: Index of 'World': 7
```

### 5. toLowerCase()
Converts all characters in the string to lowercase.
```java
String text = "HELLO";
String lower = text.toLowerCase();
System.out.println("Lowercase: " + lower);
// Output: Lowercase: hello
```

### 6. toUpperCase()
Converts all characters in the string to uppercase.
```java
String text = "hello";
String upper = text.toUpperCase();
System.out.println("Uppercase: " + upper);
// Output: Uppercase: HELLO
```
### 7. trim()
Removes whitespace from both ends of the string.
```java
String text = "  Hello ";
String trimmed = text.trim();
System.out.println("Trimmed: '" + trimmed + "'");
// Output: Trimmed: 'Hello'

```

### 8. replace(char oldChar, char newChar)
Replaces all occurrences of a specified character with a new character.
```java
String text = "Hello";
String replaced = text.replace('l', 'p');
System.out.println("Replaced: " + replaced);
// Output: Replaced: Heppo
```

### 9. contains(String str)
```java
Checks if the string contains a specified substring.
String text = "Hello, World!";
boolean contains = text.contains("World");
System.out.println("Contains 'World': " + contains);
// Output: Contains 'World': true
```
### 10. equals(String str)
Compares two strings for equality.
```java
String text1 = "Hello";
String text2 = "Hello";
boolean isEqual = text1.equals(text2);
System.out.println("Equal: " + isEqual);
// Output: Equal: true
```

# Tasks for Practice
Try these easy tasks to get comfortable with Java string methods:

### Task 1: Count Total Characters
Use length() to find the total number of characters in a given string.

```java
Your code goes here
```

### Task 2: Find First Character
Use charAt() to get the first character of a string.

```java
Your code goes here
```
### Task 3: Extract Part of a Word
Use substring() to extract the first 3 characters of a word.

```java
Your code goes here
```

### Task 4: Replace Letters in a Word
Use replace() to replace all 'a' characters in a word with 'o'.

```java
Your code goes here
```

### Task 5: Convert Text to Uppercase
Use toUpperCase() to convert a string to uppercase.

```java
Your code goes here
```
