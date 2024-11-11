# Arithmetic Operators in Java

In Java, arithmetic operators allow you to perform basic mathematical operations. This guide covers basic operators, increment/decrement, compound assignment, and flooring/ceiling of division results.

## Table of Contents
1. [Basic Arithmetic Operators](#basic-arithmetic-operators)
2. [Division and Floating Point Precision](#division-and-floating-point-precision)
3. [Increment and Decrement Operators](#increment-and-decrement-operators)
4. [Compound Assignment Operators](#compound-assignment-operators)
5. [Floor and Ceiling Division](#floor-and-ceiling-division)
6. [Easy Tasks](#easy-tasks)

---

# Basic Arithmetic Operators

Arithmetic operations like addition, subtraction, multiplication, and division are performed using operators in Java. Here are some examples:

```java
int result = 10 + 3;       // Addition
System.out.println(result);
// Output: 13

int result1 = 10 - 3;      // Subtraction
System.out.println(result1);
// Output: 7

int result2 = 10 * 3;      // Multiplication
System.out.println(result2);
// Output: 30

int result3 = 10 / 3;      // Division (whole number result)
System.out.println(result3);
// Output: 3
```

# Division and Floating Point Precision
To get a floating-point result from division, at least one operand must be cast to double or float.

```java
double result4 = (double) 10 / (double) 3;  // Casting to double for precision
System.out.println(result4);
// Output: 3.3333333333333335
```

# Increment and Decrement Operators
The increment (++) and decrement (--) operators add or subtract 1 from a variable. These operators can be used as either prefix or postfix.

```java

int x = 1;
int y = x++;  // Post-increment: y gets the value of x, then x increments
System.out.println(x); 
// Output: 2
System.out.println(y); 
// Output: 1

int x1 = 1;
int y1 = ++x1; // Pre-increment: x1 increments first, then y1 gets the new value of x1
System.out.println(x1); 
// Output: 2
System.out.println(y1); 
// Output: 2


```

# Compound Assignment Operators
Compound assignment operators combine an arithmetic operation with assignment. They allow you to write shorter code.

```java
int x = 1;
x += 2;          // Equivalent to x = x + 2;
System.out.println(x);
 // Output: 3

int x1 = 2;
x1 *= 2;         // Equivalent to x1 = x1 * 2;
System.out.println(x1);
// Output: 4

int x2 = 2;
x2 /= 2;         // Equivalent to x2 = x2 / 2;
System.out.println(x2);
// Output: 1
```

# Floor and Ceiling Division
Floor division rounds down to the nearest whole number, while ceiling division rounds up to the nearest whole number. In Java, Math.floorDiv() and Math.ceil() can be used for these purposes.

- Floor Division: Rounds down the result of division.
  
- Ceiling Division: Rounds up the result of division.

### Example of Floor Division

```java 
int a = 10;
int b = 3;
int floorResult = Math.floorDiv(a, b);
System.out.println("Floor Division Result: " + floorResult);
// Output: 3

```

### Example of Ceiling Division
To achieve ceiling division in Java, we can manually calculate it using (a + b - 1) / b.

```java
int a = 10;
int b = 3;
int ceilResult = (a + b - 1) / b;
System.out.println("Ceiling Division Result: " + ceilResult);
// Output: 4
```

# Tasks

### 1. Task 1: Calculate the result of 
8 + 5

8 − 5, 

8 × 5, and 

8 / 5 and print each result.

```java
Your code goes here...
```

### 2. Task 2: Use a compound assignment to add 10 to a variable x, initially set to 5, and print the result.

```java
Your code goes here...
```

### 3. Task 3: Define a variable counter, increment it by 1 using the increment operator, and print the result.


```java
Your code goes here...
```

### 4. Task 4: Perform floor division on 17 and 4, then perform ceiling division on 17 and 4, and print the results.

```java
Your code goes here...
```
