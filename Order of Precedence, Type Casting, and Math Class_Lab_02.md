# Java Basics: Order of Precedence, Type Casting, and Math Class

## Table of Contents
1. [Order of Precedence](#order-of-precedence)
2. [Type Casting](#type-casting)
3. [The Math Class](#the-math-class)

---

### Order of Precedence

The order of precedence (or operator precedence) determines the sequence in which operators are evaluated in expressions. Operators with higher precedence are evaluated before operators with lower precedence.

![image](https://github.com/user-attachments/assets/10c1669e-08e1-4f84-abd6-b8f186ef7818)


#### Example

```java
int x = 10 + 3 * 2;  
System.out.println(x);  // Output: 16 because * is evaluated before +

int x1 = (10 + 3) * 2;
System.out.println(x1);  // Output: 26 because parentheses change the order
```

In the first example, multiplication (*) has higher precedence than addition (+), so it’s evaluated first. Using parentheses allows us to override the default order and perform addition first.


# Type Casting
Type casting is converting a variable from one data type to another. There are two types of casting in Java:

### 1. Implicit Casting (automatic conversion) / Widening Casting

### 2. Explicit Casting (manual conversion) / Narrowing Casting



Widening casting is done automatically when passing a smaller size type to a larger size type:

```java
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```

# 1. Implicit Casting / Widening Casting
In implicit casting, Java automatically converts smaller data types to larger data types. The order of data types in Java from least to most precise is:

Widening casting is done automatically when passing a smaller size type to a larger size type:

byte > short > int > long > float > double

```java
short x = 1;
int y = x + 2;    // `short` is automatically cast to `int`
System.out.println(y);
 // Output: 3

double xDouble = 1.1;
double yDouble = xDouble + 2;  // `int` is automatically cast to `double`
System.out.println(yDouble);
// Output: 3.1
```

```java
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```

# 2. Explicit Casting / Widening Casting
Explicit casting is necessary when converting from a larger to a smaller data type or between incompatible types.

Narrowing casting must be done manually by placing the type in parentheses () in front of the value:

```java 
double xDouble = 1.1;
int yInt = (int) xDouble + 2;  // Casting `double` to `int`
System.out.println(yInt);
 // Output: 3 (fractional part is truncated)

// Converting String to numeric types
String xStr = "1";
int yParsedInt = Integer.parseInt(xStr) + 2;
System.out.println(yParsedInt);
 // Output: 3

String xFloatStr = "1.1";
float yParsedFloat = Float.parseFloat(xFloatStr) + 2;
System.out.println(yParsedFloat);
// Output: 3.1
```




```java 
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```

# The Math Class
The Math class in Java provides various methods for mathematical operations.

### Examples of Common Math Methods
### 1. Rounding:  Math.round(), Math.ceil(), Math.floor()

### Math.round():

- Rounds to the nearest integer.

### Math.ceil(): 
- Rounds up to the nearest integer.

### Math.floor(): 
-Rounds down to the nearest integer.

```java
int rounded = Math.round(1.1F);
System.out.println(rounded);
 // Output: 1

int ceiling = (int) Math.ceil(1.1F);
System.out.println(ceiling);
// Output: 2

int floor = (int) Math.floor(1.1F);
System.out.println(floor);
// Output: 1

```

### 2. Finding Maximum and Minimum: Math.max(), Math.min()

```java

int max = Math.max(1, 2);
System.out.println(max);
// Output: 2

int min = Math.min(1, 2);
System.out.println(min);
// Output: 1

```

### 3. Generating Random Numbers: Math.random()

Generates a random decimal number between 0 and 1. Multiply by 100 to get a range from 0 to 100.

```java
double randomValue = Math.random() * 100;
System.out.println(randomValue);
// Output: random number between 0 and 100

long roundedRandomValue = Math.round(Math.random() * 100);
System.out.println(roundedRandomValue);
// Output: random integer between 0 and 100

int intRandomValue = (int) (Math.random() * 100);
System.out.println(intRandomValue);
 // Output: random integer between 0 and 100
```

# Tasks 


### Task 1: Calculate the Result of a Simple Arithmetic Expression
Write a program to calculate and print the result of the following expression:

10 + 5 * 2

```java
Your code goes here...
```

###  2: Perform Type Casting (Implicit and Explicit)
- **Implicit Casting:** Convert a short value to an int and print the result.
  
- **Explicit Casting:** Convert a double value to an int and print the result.

```java
Your code goes here...
```

### Task 3: Use Math Class Methods

- Round the value 3.7 using Math.round() and print the result.

- Find the maximum between 15 and 10 using Math.max() and print the result.
  
- Generate a random number between 1 and 100 using Math.random() and print the result.

```java
Your code goes here...
```

