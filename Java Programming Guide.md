# Java Programming Basics

This document provides essential information on Java programming, including important terminologies, basic syntax, file-making rules, naming conventions, and data types.

## Table of Contents
1. [Important Java Terminologies](#important-java-terminologies)
2. [Basic Java Syntax](#basic-java-syntax)
3. [File Making Extension Class Rules](#file-making-extension-class-rules)
4. [Naming Conventions](#naming-conventions)
5. [Primitive and Non-Primitive Data Types](#primitive-and-non-primitive-data-types)

---

## Important Java Terminologies

1. **Java**: A high-level programming language used for creating applications.
2. **Class**: A blueprint for creating objects. Contains methods and variables.
3. **Method**: A function defined within a class that performs an action.
4. **Variable**: A container for storing data values.
5. **Statement**: A single line of code that performs an action.

---

## Basic Java Syntax

### Structure of a Java Program

```java
public class MyFirstProgram {
    public static void main(String[] args) {
        // Print message to console
        System.out.println("Hello, World!");
    }
}
```

# Key Elements
### Class Declaration: 
- public class MyFirstProgram
### Main Method: 
-public static void main(String[] args)
### Print Statement:
- System.out.println("Hello, World!");

## Naming Conventions

1. **Class Names**: Use PascalCase (capitalize each word).
   - **Example**: `MyClass`, `StudentRecord`

2. **Method Names**: Use camelCase (first word lowercase, subsequent words capitalized).
   - **Example**: `calculateTotal()`, `printName()`

3. **Variable Names**: Use camelCase and choose meaningful names.
   - **Example**: `totalAmount`, `studentName`

4. **Constants**: Use uppercase letters with underscores.
   - **Example**: `MAX_VALUE`, `PI_VALUE`
  
## Primitive and Non-Primitive Data Types

### Primitive Data Types

1. **int**: Represents a 32-bit signed integer.
   - **Example**:
     ```java
     int age = 30;
     ```

2. **double**: Represents a double-precision 64-bit floating point.
   - **Example**:
     ```java
     double price = 19.99;
     ```

3. **char**: Represents a single 16-bit Unicode character.
   - **Example**:
     ```java
     char initial = 'A';
     ```

4. **boolean**: Represents a value of true or false.
   - **Example**:
     ```java
     boolean isJavaFun = true;
     ```

### Non-Primitive Data Types

1. **String**: A sequence of characters.
   - **Example**:
     ```java
     String greeting = "Hello, Java!";
     ```

2. **Array**: A collection of similar types.
   - **Example**:
     ```java
     int[] numbers = {1, 2, 3, 4, 5};
     ```

3. **Class**: A user-defined type.
   - **Example**:
     ```java
     class Car {
         String model;
         Car(String model) {
             this.model = model;
         }
     }
     ```

4. **Interface**: A reference type that can contain only method signatures.
   - **Example**:
     ```java
     interface Animal {
         void sound();
     }
     ```

This guide provides a foundational understanding of Java programming essentials, including syntax, rules for file creation, naming conventions, and data types.


