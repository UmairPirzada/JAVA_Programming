# Java Data Types and Their Ranges

Java provides several primitive data types to store different types of values. Below is a breakdown of each type, its size, range (for numeric types), and usage.

## Data Types Overview

| Data Type | Size      | Description                                                                                                  |
|-----------|-----------|--------------------------------------------------------------------------------------------------------------|
| `byte`    | 1 byte    | Stores whole numbers from **-128** to **127**                                                                |
| `short`   | 2 bytes   | Stores whole numbers from **-32,768** to **32,767**                                                          |
| `int`     | 4 bytes   | Stores whole numbers from **-2,147,483,648** to **2,147,483,647**                                            |
| `long`    | 8 bytes   | Stores whole numbers from **-9,223,372,036,854,775,808** to **9,223,372,036,854,775,807**                    |
| `float`   | 4 bytes   | Stores fractional numbers, sufficient for storing **6 to 7 decimal digits**                                  |
| `double`  | 8 bytes   | Stores fractional numbers, sufficient for storing **15 to 16 decimal digits**                                |
| `boolean` | 1 bit     | Stores **true** or **false** values                                                                          |
| `char`    | 2 bytes   | Stores a **single character** or **ASCII value**                                                             |

## Detailed Calculations for Integer Ranges

For signed integer data types in Java (`byte`, `short`, `int`, and `long`), the range is determined based on the number of bits used to represent each type. The formula for calculating the range of an `n`-bit signed integer is:

\[
-\left(2^{(n-1)}\right) \text{ to } 2^{(n-1)} - 1
\]

Where `n` is the number of bits used by the type.

### 1. `byte`
- **Size**: 1 byte (8 bits)
- **Range Calculation**:
  - Minimum: \(-2^{7} = -128\)
  - Maximum: \(2^{7} - 1 = 127\)
- **Range**: **-128** to **127**

### 2. `short`
- **Size**: 2 bytes (16 bits)
- **Range Calculation**:
  - Minimum: \(-2^{15} = -32,768\)
  - Maximum: \(2^{15} - 1 = 32,767\)
- **Range**: **-32,768** to **32,767**

### 3. `int`
- **Size**: 4 bytes (32 bits)
- **Range Calculation**:
  - Minimum: \(-2^{31} = -2,147,483,648\)
  - Maximum: \(2^{31} - 1 = 2,147,483,647\)
- **Range**: **-2,147,483,648** to **2,147,483,647**

### 4. `long`
- **Size**: 8 bytes (64 bits)
- **Range Calculation**:
  - Minimum: \(-2^{63} = -9,223,372,036,854,775,808\)
  - Maximum: \(2^{63} - 1 = 9,223,372,036,854,775,807\)
- **Range**: **-9,223,372,036,854,775,808** to **9,223,372,036,854,775,807**

## Floating-Point Data Types

Floating-point types (`float` and `double`) are used for decimal values.

- **`float`**: 4 bytes (32 bits) - Sufficient precision for approximately **6 to 7 decimal digits**.
- **`double`**: 8 bytes (64 bits) - Sufficient precision for approximately **15 to 16 decimal digits**.

Floating-point numbers are stored in a format specified by IEEE 754, and their ranges are not strictly bounded like integer types. Instead, they have a large dynamic range suitable for scientific calculations.

## Boolean and Character Types

- **`boolean`**: 1 bit - Stores `true` or `false` values.
- **`char`**: 2 bytes (16 bits) - Stores a **single character** or **ASCII value**. Java uses Unicode for `char`, so it can store characters from **'\u0000'** (0) to **'\uffff'** (65,535).

---

This summary provides the data types in Java, their memory sizes, ranges (where applicable), and a brief explanation of each type’s usage.