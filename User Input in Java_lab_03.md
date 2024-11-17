# User Input in Java

This repository explains how to handle user input in Java using the `Scanner` class. 

The `Scanner` class is part of the `java.util` package and is widely used to read input from the console.

---

## **Table of Contents**

1. [Why Use Scanner?](#why-use-scanner)
2. [Examples](#examples)
   - [Example 1: Reading an Integer Input](#example-1-reading-an-integer-input)
   - [Example 2: Reading a Single Word](#example-2-reading-a-single-word)
   - [Example 3: Reading Full Name](#example-3-reading-full-name)
   - [Example 4: Reading Floating-Point Numbers](#example-4-reading-floating-point-numbers)
   - [Example 5: Reading Multiple Inputs](#example-5-reading-multiple-inputs)
3. [Practice Tasks](#practice-tasks)
   - [Task 1: Personal Information](#task-1-personal-information)
   - [Task 2: BMI Calculator](#task-2-bmi-calculator)
   - [Task 3: Shopping List Total](#task-3-shopping-list-total)

## **Why Use Scanner?**
The `Scanner` class provides methods to read different types of input:
- Numbers (`int`, `float`, `double`, etc.)
- Strings (single words or entire lines)
- Boolean values
- Other data types like `byte`, `short`, and `long`

---

## **Examples**

### Example 1: Reading an Integer Input
```java
import java.util.Scanner;

public class InputExample1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = scanner.nextInt(); // Reads an integer input
        System.out.println("Your age is: " + age);

        scanner.close();
    }
}
```

### Example 2: Reading a Single Word

```java
import java.util.Scanner;

public class InputExample2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your first name: ");
        String firstName = scanner.next(); // Reads a single word
        System.out.println("Hello, " + firstName + "!");

        scanner.close();
    }
}

```

### Example 3: Reading Full Name
```java
import java.util.Scanner;

public class InputExample3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your full name: ");
        String fullName = scanner.nextLine(); // Reads the entire line
        System.out.println("Welcome, " + fullName + "!");

        scanner.close();
    }
}
```

### Example 4: Reading Floating-Point Numbers


```java
import java.util.Scanner;

public class InputExample4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a decimal number: ");
        double decimalNumber = scanner.nextDouble(); // Reads a floating-point number
        System.out.println("You entered: " + decimalNumber);

        scanner.close();
    }
}
```

### Example 5: Reading Multiple Inputs

```java

import java.util.Scanner;

public class InputExample5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = scanner.nextInt(); // Reads age

        System.out.print("Enter your height (in cm): ");
        float height = scanner.nextFloat(); // Reads height

        System.out.println("Age: " + age + ", Height: " + height + " cm");

        scanner.close();
    }
}
```

# Practice Tasks
### Task 1: Personal Information
Write a program to ask the user for:

- Name
  
- Age
  
- Favorite color
  
 -Print a message such as:
 
Hello [Name]! You are [Age] years old, and your favorite color is [Color]!

```java

Your Code Goes Here...
```

### Task 2: BMI Calculator
Create a program that asks the user for:

- Weight (in kg)
  
- Height (in meters)
  
**Calculate and print their BMI using the formula:**

### BMI = weight / (height * height)

```java

Your Code Goes Here...
```

### Task 3: Shopping List Total
Write a program to:

- Ask for the name of an item.
  
- Ask for the quantity and price of the item.
  
- Print the total cost using:
  
**Total = quantity * price**

```java

Your Code Goes Here...
```


# Mortgage Calculator Project

## Table of Contents

1. [Project Overview](#project-overview)
2. [Formula for Mortgage Calculation](#formula-for-mortgage-calculation)
3. [Java Code](#java-code)
4. [Explanation](#explanation)
5. [Sample Output](#sample-output)
6. [Tasks for Students](#tasks-for-students)

---

## Project Overview

This project is a **Mortgage Calculator** that calculates the monthly mortgage payment based on the loan amount, interest rate, and loan term. The program takes input from the user and applies the mortgage calculation formula to compute the monthly payment.

The formula used to calculate the mortgage payment is:

\[
M = \frac{P \cdot r \cdot (1 + r)^n}{(1 + r)^n - 1}
\]

Where:
- \(M\) = Monthly Payment
- \(P\) = Principal loan amount
- \(r\) = Monthly interest rate (Annual rate divided by 12)
- \(n\) = Total number of payments (Loan term in years multiplied by 12)

---

## Formula for Mortgage Calculation

The formula used to calculate the monthly payment for a mortgage is:

\[
M = \frac{P \cdot r \cdot (1 + r)^n}{(1 + r)^n - 1}
\]

Where:
- \(M\) = Monthly Payment
  
- \(P\) = Principal loan amount
  
- \(r\) = Monthly interest rate (Annual rate divided by 12)
  
- \(n\) = Total number of payments (Loan term in years multiplied by 12)

---

## Java Code

```java
import java.util.Scanner;

public class MortgageCalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get principal loan amount
        System.out.print("Enter the principal loan amount: ");
        double principal = scanner.nextDouble();

        // Get annual interest rate
        System.out.print("Enter the annual interest rate (in percentage): ");
        double annualInterestRate = scanner.nextDouble();

        // Get loan term in years
        System.out.print("Enter the loan term (in years): ");
        int loanTermYears = scanner.nextInt();

        // Calculate monthly interest rate
        double monthlyInterestRate = annualInterestRate / 100 / 12;

        // Calculate total number of payments (months)
        int totalPayments = loanTermYears * 12;

        // Calculate monthly mortgage payment using the formula
        double monthlyPayment = calculateMonthlyPayment(principal, monthlyInterestRate, totalPayments);

        // Display the result
        System.out.println("Your monthly mortgage payment is: " + String.format("%.2f", monthlyPayment));

        scanner.close();
    }

    // Method to calculate monthly payment
    public static double calculateMonthlyPayment(double principal, double monthlyInterestRate, int totalPayments) {
        // If the interest rate is 0, the formula would result in a division by zero, so we handle this case separately
        if (monthlyInterestRate == 0) {
            return principal / totalPayments;
        }

        // Formula for calculating monthly mortgage payment
        return (principal * monthlyInterestRate * Math.pow(1 + monthlyInterestRate, totalPayments)) / 
               (Math.pow(1 + monthlyInterestRate, totalPayments) - 1);
    }
}
```


# Tasks for Students
### Task 1: Calculate Monthly Payment with Different Inputs

**Problem:** Modify the program to calculate the monthly payment for different inputs. Try changing the principal amount, interest rate, and loan term, and observe how the monthly payment changes.

### Input Example:

- Principal: 250,000
  
- Interest Rate: 5%
  
- Loan Term: 20 years
  
**Expected Output:** Calculate and print the result for the monthly mortgage payment based on the above inputs.

```java

Your Code Goes Here...
```


### Task 2: Calculate Total Interest Paid Over the Life of the Loan
**Problem:** Modify the program to also calculate the total interest paid over the life of the loan.

Formula for Total Interest Paid:

![image](https://github.com/user-attachments/assets/4f61f2c6-37b2-4af6-a175-6f7690eb4251)


Total Interest= Total Payments−Principal
Input Example:

- Principal: 300,000
  
- Annual Interest Rate: 3.5%

- Loan Term: 30 years

**Output Example:** Display the total interest paid after the loan is paid off.

```java

Your Code Goes Here...
```
