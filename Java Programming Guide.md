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

## Java Code: JavaBasics.java

```java
// JavaBasics.java

// This is a simple Java program to demonstrate basic concepts

public class JavaBasics {
    
    // Main method: Entry point of the Java application
    public static void main(String[] args) {
        // Example of primitive data types
        int age = 30; // An integer value
        double price = 19.99; // A double value
        char initial = 'A'; // A character value
        boolean isJavaFun = true; // A boolean value
        
        // Outputting primitive data types
        System.out.println("Age: " + age);
        System.out.println("Price: " + price);
        System.out.println("Initial: " + initial);
        System.out.println("Is Java Fun? " + isJavaFun);
        
        // Example of non-primitive data types
        String greeting = "Hello, Java!"; // A String
        System.out.println(greeting);
        
        // Example of an array
        int[] numbers = {1, 2, 3, 4, 5}; // An array of integers
        System.out.print("Numbers: ");
        for (int number : numbers) { // Enhanced for loop
            System.out.print(number + " ");
        }
        System.out.println();
        
        // Example of a class
        Car myCar = new Car("Toyota"); // Creating an instance of the Car class
        System.out.println("Car Model: " + myCar.model);
        
        // Example of a method
        int sum = calculateSum(5, 10); // Calling a method to calculate the sum
        System.out.println("Sum of 5 and 10: " + sum);
    }
    
    // Method to calculate the sum of two integers
    public static int calculateSum(int a, int b) {
        return a + b; // Returning the sum
    }
}

// Class definition for Car
class Car {
    String model; // Instance variable to store the car model
    
    // Constructor to initialize the car model
    Car(String model) {
        this.model = model; // Assigning the value to the instance variable
    }
}
```

# Explanation
### Class Declaration:
The JavaBasics class contains the main method, which is the entry point for any Java application.

### Main Method: 
The main method is where the program execution starts. It includes various examples of Java's basic syntax and concepts.

### Primitive Data Types: 
Examples of primitive data types such as int, double, char, and boolean are shown. Each type is declared and initialized, followed by output using System.out.println().

### Non-Primitive Data Types:
The String type is demonstrated with a greeting message. An array is also used to store a collection of integers, and a loop is used to print each element.

### Classes and Objects:
A simple Car class is defined, which includes an instance variable and a constructor. An object of the Car class is created in the main method.

### Methods:
A method named calculateSum is created to demonstrate how to define and call methods in Java. It takes two integers as parameters and returns their sum.

###How to Compile and Run
**1. Save the Code:** Save the code in a file named JavaBasics.java.

**2. Open Terminal or Command Prompt:** Open your terminal or command prompt.

**3. Navigate to the Directory:** Navigate to the directory where the file is saved using the cd command.

**4. Compile the Java Program:**
```bash
javac JavaBasics.java
```
**5. Run the Compiled Program:**
```bash
java JavaBasics
```

This will execute the program, and you should see the output printed to the console.
# Output
You should see an output similar to the following:
``` bash
Age: 30
Price: 19.99
Initial: A
Is Java Fun? true
Hello, Java!
Numbers: 1 2 3 4 5 
Car Model: Toyota
Sum of 5 and 10: 15
```



This guide provides a foundational understanding of Java programming essentials, including syntax, rules for file creation, naming conventions, and data types.


