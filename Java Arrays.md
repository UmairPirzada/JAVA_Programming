# Arrays in Java

## Table of Contents
- [Introduction to Arrays](#introduction-to-arrays)
  - [What is an Array?](#what-is-an-array)
  - [Data Types of Arrays](#data-types-of-arrays)
  - [Understanding the `new` Keyword](#understanding-the-new-keyword)
- [Array Declaration and Initialization](#array-declaration-and-initialization)
  - [Old Array Declaration Method](#old-array-declaration-method)
  - [New Array Declaration Method](#new-array-declaration-method)
- [Types of Arrays](#types-of-arrays)
  - [1D Arrays](#1d-arrays)
  - [2D Arrays](#2d-arrays)
  - [3D Arrays](#3d-arrays)
- [Array Packages and Methods](#array-packages-and-methods)
- [Beginner Tasks](#beginner-tasks)

## Introduction to Arrays

### What is an Array?
Arrays are used to store lists of items (e.g., numbers, people) in Java. Arrays:
- Are a **reference type** and can only store values of the same data type.
- Are indexed starting from **0** (the first element is at index 0).
- Can be thought of as a single variable that can hold multiple values.

### Data Types of Arrays
Arrays can hold values of any data type, such as:
- `int[]` for integers
- `String[]` for strings
- `double[]` for decimal numbers

### Understanding the `new` Keyword
The `new` keyword is used to create an array and allocate memory for it. It specifies the size of the array and initializes it to default values (e.g., `0` for integers, `null` for objects).

Example:
```java
int[] numbers = new int[5];  // An array of 5 integers, initialized to {0, 0, 0, 0, 0}
```

# Array Declaration and Initialization

### Old Array Declaration Method
Arrays were often initialized by directly specifying their elements:

```java
int[] numbers = {2, 4, 6, 7, 8};
System.out.println("Array Length: " + numbers.length);
System.out.println("Array Element at Index 2: " + numbers[2]);
```

### New Array Declaration Method
Using the new keyword, we can declare and initialize an array as follows:

```java
int[] numbers = new int[3];
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;
System.out.println("Array Element at Index 1: " + numbers[1]);
```

# Types of Arrays
### 1D Arrays
A 1D array is a simple list of elements accessed with a single index.

```java
String[] names = {"Alice", "Bob", "Charlie"};
System.out.println("1D Array: " + Arrays.toString(names));
```

### 2D Arrays
A 2D array is an array of arrays, like a table with rows and columns.

```java
int[][] numbers2D = {
    {1, 2, 3},
    {4, 5, 6}
};
System.out.println("2D Array: " + Arrays.deepToString(numbers2D));
```

### 3D Arrays
A 3D array is an array of 2D arrays, used to represent layers.

```java
int[][][] numbers3D = {
    {
        {1, 2},
        {3, 4}
    },
    {
        {5, 6},
        {7, 8}
    }
};
System.out.println("3D Array: " + Arrays.deepToString(numbers3D));
```

# Array Packages and Methods
Java provides utility methods for array manipulation through the java.util.Arrays package:

- Arrays.toString(array): Converts a 1D array to a string.
  
- Arrays.deepToString(array): Converts multidimensional arrays to a string.
  
- Arrays.sort(array): Sorts the array elements.

- Arrays.binarySearch(array, key): Searches for a value in a sorted array.

# Why Convert to String?
The java.util.Arrays utility methods toString and deepToString are used to make array content more readable, especially for debugging. Without these methods, printing an array directly would display a memory reference rather than its elements.

# Arrays Utility Methods Explained

### 1. Arrays.toString(array):

- This method converts a 1D array (e.g., int[], String[]) to a human-readable string.
  
- When printed, the output shows all elements of the array in square brackets, separated by commas.
  
- This is helpful for quickly seeing the contents of a 1D array.

### 3. Arrays.deepToString(array):


- This method is used for multidimensional arrays (e.g., int[][] or String[][]).
  
- It converts nested arrays to a human-readable string format, showing all elements in multiple levels of brackets.
  
- Essential when working with 2D or 3D arrays to see the complete structure.
  
### Example:

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6}
};
System.out.println(Arrays.deepToString(matrix));

// Output: [[1, 2, 3], [4, 5, 6]]
```

### 3. Arrays.sort(array):

- This method sorts the elements of a 1D array in ascending order.
  
- Sorting makes it easier to perform tasks like finding minimum or maximum values or preparing data for searching.
  
- Works for both primitive types (like int, double) and objects (like String).

### Example:

```java
int[] numbers = {5, 3, 8, 1, 2};
Arrays.sort(numbers);
System.out.println(Arrays.toString(numbers));
// Output: [1, 2, 3, 5, 8]

  ```
### 4. Arrays.binarySearch(array, key):

- This method performs a binary search on a sorted array to find a specified value (the key).
  
- It returns the index of the key if found; otherwise, it returns a negative value.
  
- Requires the array to be sorted first; otherwise, results may be incorrect.

- Useful for fast lookups in a sorted array.

### Example:

```java
int[] numbers = {1, 2, 3, 5, 8};
int index = Arrays.binarySearch(numbers, 5);
System.out.println("Index of 5: " + index);
// Output: Index of 5: 3
```


### Example:

```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(Arrays.toString(numbers));
 // Output: [1, 2, 3, 4, 5]
```
  
 ### Example:

```java
import java.util.Arrays;

int[] numbers = {5, 3, 8, 1, 2};
Arrays.sort(numbers);
System.out.println("Sorted Array: " + Arrays.toString(numbers));
```

**These utility methods from java.util.Arrays simplify working with arrays by providing convenient ways to view, sort, and search for elements in arrays. Using toString and deepToString makes it much easier to understand the data structure at a glance, especially during debugging or when logging data.**

# What is the new Keyword?
In Java, the new keyword is used to create objects, including arrays. When you declare an array, the new keyword allocates memory for the specified number of elements. This is essential because Java requires an explicit allocation of memory when dealing with arrays and other reference types.

### For example:
```java
int[] numbers = new int[5]; 
```

### Here:

- int[] declares an array that will store integers.
 
- new int[5] creates an array of integers with a length of 5.
  
- Each element in the array is automatically initialized to the default value for integers, which is 0.
  
  The new keyword helps Java manage memory efficiently by allowing us to specify exactly how much space we need.

---

# Tasks

### 1. Create a 1D array of 3 favorite colors and print the color at index 1.

```java
Your code goes Here...
```

### 2. Create a 1D array of 4 integers, set the value of the second element to 10, and print it.

```java
Your code goes Here...
```

### 3. Create a 2D array representing a 2x2 matrix, assign values to each element, and print the entire matrix.

```java
Your code goes Here...
```

### 4. Create an array of 5 integers, assign values to the first and last elements, and print both.

```java
Your code goes Here...
```

### 5. Create a 1D array of 3 names, assign your name to the second element, and print the array.

```java
Your code goes Here...
```


# Constants in Java
In Java, a constant is a variable whose value cannot be changed once it has been assigned. Constants are typically used for fixed values that are referenced multiple times throughout a program. Defining constants improves code readability and maintainability, especially when the same value is needed in different places.

To define a constant, we use the final keyword, which prevents modification of the variable after its initial assignment.

### Syntax for Constants:

```java
final dataType CONSTANT_NAME = value;
```
- The final keyword makes the variable a constant, meaning its value cannot be changed.
  
- It’s a common convention to use uppercase letters for constant names to distinguish them from regular variables.


### Examples
Example 1: Defining and Using a Constant

```java 
// Using a regular variable (not a constant)
float pi = 3.14F;
System.out.println(pi);
// Output: 3.14
pi = 4;
// The value can be changed
System.out.println(pi);
// Output: 4

// Using a constant
final float PI = 3.14F;
System.out.println(PI);
// Output: 3.14
// PI = 10;
 // This line will cause an error because PI is a constant
```

### In this example:

- pi is a regular variable, so its value can be changed.
  
- PI, however, is defined with final, making it a constant. Attempting to change PI after its initial assignment will result in a compilation error.
  
# Why Use Constants?
Constants are useful when:

- You want to define fixed values like PI, E, or maximum limits that won’t change.
  
- They make the code more readable, as PI is more meaningful than a raw number like 3.14.
  
- They help avoid errors by preventing changes to values that should remain constant throughout the program.

# Tasks

### Task 1: Define a constant MAX_SCORE with a value of 100 and print it to the console.

```java
Your code goes Here...
```

### Task 2: Define two constants, MIN_AGE and MAX_AGE, with values 18 and 65, respectively. Print them in a message that indicates the valid age range.

```java
Your code goes Here...
```

### Task 3: Create a constant for GRAVITY with a value of 9.8 (representing gravitational acceleration) and use it in a formula to calculate the weight of an object with mass 50 kg. Print the result.

```java
Your code goes Here...
```

### Hint:
## Calculating Weight Using Constants

To calculate the weight of an object, we can use the following formula:

\[
\text{Weight} = \text{Mass} \times \text{Gravity}
\]

where:
- **Mass** is the mass of the object (in kilograms).
- **Gravity** is the gravitational acceleration constant, usually \(9.8 \, m/s^2\) on Earth.


