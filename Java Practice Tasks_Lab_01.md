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

# Fibonacci Formula
- The **Fibonacci Series** is a sequence where each number is the sum of the two preceding ones, starting from 0 and 1. This sequence is widely used in mathematics, computer science, and even appears in natural patterns.

## Definition

The Fibonacci sequence starts as follows:
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...

### Fibonacci Formula
The formula to calculate the \( n \)-th term in the Fibonacci series is:
\[
F(n) = F(n-1) + F(n-2)
\]
where:
- \( F(0) = 0 \)
- \( F(1) = 1 \)

### Explanation
Each term is the sum of the previous two terms:
- \( F(2) = F(1) + F(0) = 1 \)
- \( F(3) = F(2) + F(1) = 2 \)
- \( F(4) = F(3) + F(2) = 3 \)
- and so on.

## Example Java Code

Here’s a Java program to display the first few numbers in the Fibonacci series.

```java
public class FibonacciSeries {
    public static void main(String[] args) {
        int n1 = 0, n2 = 1, n3;
        System.out.print(n1 + " " + n2); // Print the first two numbers

        for (int i = 2; i < 10; i++) { // Adjust 10 for more terms
            n3 = n1 + n2; // Calculate the next number in sequence
            System.out.print(" " + n3); // Print next number
            n1 = n2; // Shift n1 to n2
            n2 = n3; // Shift n2 to n3
        }
    }
}
```
### How It Works
- Initialize the first two terms as n1 = 0 and n2 = 1.
- Loop to calculate the next terms by adding the last two terms:
- n3 = n1 + n2
- Print each term, updating n1 and n2 as you move forward in the sequence.
   This program will output the first 10 terms of the Fibonacci series. You can change the loop limit to display more terms as needed.


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

# Temperature Conversion (Celsius to Fahrenheit and Fahrenheit to Celsius)

This program converts temperatures between Celsius and Fahrenheit using the following formulas.

## Conversion Formulas
![image](https://github.com/user-attachments/assets/5ad263eb-30aa-4828-b1ae-696004e7aa12)

### Celsius to Fahrenheit
To convert a temperature from Celsius to Fahrenheit:
\[
°F = (°C \times \frac{9}{5}) + 32
\]

### Fahrenheit to Celsius
To convert a temperature from Fahrenheit to Celsius:
\[
°C = (°F - 32) \times \frac{5}{9}
\]

## Example Java Code

The following Java program uses command-line arguments to convert a given temperature between Celsius and Fahrenheit.

```java
public class TemperatureConversion {
    public static void main(String[] args) {
        if (args.length < 2) {
            System.out.println("Usage: java TemperatureConversion <temperature> <C/F>");
            return;
        }

        double temperature = Double.parseDouble(args[0]);
        String scale = args[1].toUpperCase();

        if (scale.equals("C")) {
            // Celsius to Fahrenheit conversion
            double fahrenheit = (temperature * 9 / 5) + 32;
            System.out.printf("%.2f°C is %.2f°F\n", temperature, fahrenheit);
        } else if (scale.equals("F")) {
            // Fahrenheit to Celsius conversion
            double celsius = (temperature - 32) * 5 / 9;
            System.out.printf("%.2f°F is %.2f°C\n", temperature, celsius);
        } else {
            System.out.println("Invalid scale. Use 'C' for Celsius or 'F' for Fahrenheit.");
        }
    }
}
```

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

