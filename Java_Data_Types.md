# Java Data Types and Their Ranges

In Java, a **data type** is an attribute that specifies the type of data that a variable can store. Data types are divided into two main categories: **Primitive** and **Non-Primitive**.

## Types of Data Types

### 1. Primitive Data Types
Primitive data types in Java are the most basic types of data. They are predefined by the language and named by a keyword. Primitive data types directly contain values, which makes them more memory-efficient. A primitive data type specifies the size and type of variable values, and it has no additional methods.

**There are eight primitive data types in Java:**



| **Data Type**  | **Size**     | **Description**                                         |
|----------------|--------------|---------------------------------------------------------|
| `byte`         | 1 byte       | Stores whole numbers from **-128** to **127**           |
| `short`        | 2 bytes      | Stores whole numbers from **-32,768** to **32,767**     |
| `int`          | 4 bytes      | Stores whole numbers from **-2,147,483,648** to **2,147,483,647** |
| `long`         | 8 bytes      | Stores whole numbers from **-9,223,372,036,854,775,808** to **9,223,372,036,854,775,807** |
| `float`        | 4 bytes      | Stores fractional numbers, with precision up to **7 decimal digits** |
| `double`       | 8 bytes      | Stores fractional numbers, with precision up to **16 decimal digits** |
| `boolean`      | 1 bit        | Stores **true** or **false**                            |
| `char`         | 2 bytes      | Stores a **single character** or **ASCII value**        |

### 2. Non-Primitive Data Types
Non-primitive data types in Java are more complex structures. Unlike primitive types, they are created by the user, so they do not directly store values but instead reference locations in memory where data is stored. Non-primitive data types are called reference types because they refer to objects.
Non-primitive types include:

| **Data Type**  | **Description**                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------|
| `String`       | Stores a sequence of characters, typically representing text                                     |
| `Array`        | Stores a collection of elements of the same data type                                            |
| `Class`        | Blueprint for creating objects, containing attributes and methods                                |
| `Interface`    | Specifies methods that a class must implement, defining a contract without any method bodies     |

## Differences Between Primitive and Non-Primitive Data Types

**The main difference between primitive and non-primitive data types are:**

- Primitive types in Java are predefined and built into the language, while non-primitive types are created by the programmer (except for String).
- 
- Non-primitive types can be used to call methods to perform certain operations, wheras primitive types cannot.
- 
- Primitive types start with a lowercase letter (like int), while non-primitive types typically starts with an uppercase letter (like String).
- 
- Primitive types always hold a value, wheras non-primitive types can be null.
  

| Feature                    | Primitive Data Types                            | Non-Primitive Data Types                                |
|----------------------------|------------------------------------------------|--------------------------------------------------------|
| **Definition**             | Basic types built into the language            | Created by users and can be more complex               |
| **Memory Usage**           | Directly store values                          | Store references to memory locations                   |
| **Size**                   | Fixed size                                     | Size can vary depending on the data type               |
| **Null Assignment**        | Cannot be assigned `null`                      | Can be assigned `null`                                 |
| **Methods**                | Cannot invoke methods                          | Can invoke methods defined within the class/interface  |
| **Examples**               | `int`, `char`, `boolean`, `float`              | `String`, `Array`, `Class`, `Interface`                |

## Detailed Calculations for Integer Ranges

For signed integer data types in Java (`byte`, `short`, `int`, and `long`), the range is determined based on the number of bits used to represent each type. The formula for calculating the range of an `n`-bit signed integer is:

-(2^{(n-1)}) 
To
 (2^{(n-1)} - 1)


Where `n` is the number of bits used by the type.

### 1. `byte`
- **Size**: 1 byte (8 bits)
- **Range Calculation**:
  - Minimum: `-2^7 = -128`
  - Maximum: `2^7 - 1 = 127`
- **Range**: **-128** to **127**

### 2. `short`
- **Size**: 2 bytes (16 bits)
- **Range Calculation**:
  - Minimum: `-2^15 = -32,768`
  - Maximum: `2^15 - 1 = 32,767`
- **Range**: **-32,768** to **32,767**

### 3. `int`
- **Size**: 4 bytes (32 bits)
- **Range Calculation**:
  - Minimum: `-2^31 = -2,147,483,648`
  - Maximum: `2^31 - 1 = 2,147,483,647`
- **Range**: **-2,147,483,648** to **2,147,483,647**

### 4. `long`
- **Size**: 8 bytes (64 bits)
- **Range Calculation**:
  - Minimum: `-2^63 = -9,223,372,036,854,775,808`
  - Maximum: `2^63 - 1 = 9,223,372,036,854,775,807`
- **Range**: **-9,223,372,036,854,775,808** to **9,223,372,036,854,775,807**

## Floating-Point Data Types

Floating-point types (`float` and `double`) are used for decimal values.

- **`float`**: 4 bytes (32 bits) - Sufficient precision for approximately **6 to 7 decimal digits**.
- **`double`**: 8 bytes (64 bits) - Sufficient precision for approximately **15 to 16 decimal digits**.

Floating-point numbers are stored in a format specified by IEEE 754, and their ranges are not strictly bounded like integer types. Instead, they have a large dynamic range suitable for scientific calculations.

## Boolean and Character Types

- **`boolean`**: 1 bit - Stores `true` or `false` values.
- **`char`**: 2 bytes (16 bits) - Stores a **single character** or **ASCII value**. Java uses Unicode for `char`, so it can store characters from `'\u0000'` (0) to `'\uffff'` (65,535).

---
