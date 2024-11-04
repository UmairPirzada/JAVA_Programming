# Java Practice Tasks

This repository contains solutions for basic Java practice tasks aimed at reinforcing foundational programming concepts such as loops, conditionals, and input handling. Each task includes a detailed explanation and a Java code snippet to accomplish the desired outcome.

---

## Table of Contents

1. [Requirements](#requirements)
2. [Tasks](#tasks)
    - [Task 1: Display Even Numbers from 1-20](#task-1-display-even-numbers-from-1-20)
    - [Task 2: Display the First 8 Numbers of the Fibonacci Series](#task-2-display-the-first-8-numbers-of-the-fibonacci-series)
    - [Task 3: Temperature Conversion (Celsius to Fahrenheit and vice versa)](#task-3-temperature-conversion-celsius-to-fahrenheit-and-vice-versa)
    - [Task 4: Calculate Factorial](#task-4-calculate-factorial)
    - [Task 5: Check if a String is a Palindrome](#task-5-check-if-a-string-is-a-palindrome)


---

## Requirements

To compile and run these Java programs, you will need:

- Java Development Kit (JDK) 8 or later
- Command line access or an IDE like IntelliJ IDEA, Eclipse, or VS Code with Java support

---

# Tasks

## Task 1: Display Even Numbers from 1-20

**Functionality:** Display all even numbers between 1 and 20.

**Code:**
```java
public class EvenNumbers {
    public static void main(String[] args) {
        // Start loop from 2 (first even number) and increase by 2 each time
        for (int i = 2; i <= 20; i += 2) {
            System.out.println(i); // Print each even number
        }
    }
}
```
### Explanation: 
**The program uses a for loop that iterates from 2 to 20, printing each even number.**

## Task 2:
- Display the First 8 Numbers of the Fibonacci Series
- Functionality: Display the first 8 numbers in the Fibonacci series.

**Code:**
```java
public class FibonacciSeries {
    public static void main(String[] args) {
        int n1 = 0, n2 = 1, n3;
        System.out.print(n1 + " " + n2); // Print the first two numbers

        for (int i = 2; i < 8; i++) { // Loop to find the next 6 numbers
            n3 = n1 + n2; // Calculate the next number in sequence
            System.out.print(" " + n3); // Print next number
            n1 = n2; // Update first previous number
            n2 = n3; // Update second previous number
        }
    }
}
```

### Explanation: 
- This program calculates Fibonacci numbers by adding the previous two numbers in each loop iteration.

## Task 3:
- Temperature Conversion (Celsius to Fahrenheit and vice versa)
- Functionality: Convert temperatures between Celsius and Fahrenheit using command-line arguments.

**Code:**
```java
public class TemperatureConverter {
    public static void main(String[] args) {
        if (args.length < 2) { // Check if both arguments are provided
            System.out.println("Usage: java TemperatureConverter <C/F> <Temperature>");
            return;
        }

        char type = args[0].charAt(0); // First argument is the type (C or F)
        double temp = Double.parseDouble(args[1]); // Second argument is the temperature

        if (type == 'C' || type == 'c') {
            double fahrenheit = temp * 9/5 + 32; // Celsius to Fahrenheit conversion
            System.out.println(temp + " °C is " + fahrenheit + " °F");
        } else if (type == 'F' || type == 'f') {
            double celsius = (temp - 32) * 5/9; // Fahrenheit to Celsius conversion
            System.out.println(temp + " °F is " + celsius + " °C");
        } else {
            System.out.println("Invalid temperature type! Use 'C' for Celsius or 'F' for Fahrenheit.");
        }
    }
}
```
### Explanation: 
- This program takes temperature type and value as arguments, converting between Celsius and Fahrenheit using specified formulas.

## Task 4: 
- Calculate Factorial
- Functionality: Calculate the factorial of a user-provided number.

**Code:**
```java
import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        int factorial = 1;

        for (int i = 1; i <= number; i++) {
            factorial *= i; // Multiply factorial by each number up to the input
        }
        
        System.out.println("Factorial of " + number + " is " + factorial);
        scanner.close();
    }
}
```
### Explanation: 
- This program uses a loop to calculate the factorial by multiplying all integers from 1 up to the input number. It utilizes the Scanner class from java.util.

## Task 5: 
- Check if a String is a Palindrome
- Functionality: Check if a given string is a palindrome (reads the same forwards and backwards).

**Code:**
```java
import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String original = scanner.nextLine();
        String reversed = new StringBuilder(original).reverse().toString();

        if (original.equalsIgnoreCase(reversed)) { // Check if reversed equals the original
            System.out.println(original + " is a palindrome.");
        } else {
            System.out.println(original + " is not a palindrome.");
        }
        scanner.close();
    }
}
```
### Explanation: 
- The program reverses the string using StringBuilder and compares it with the original string to check for a palindrome.

