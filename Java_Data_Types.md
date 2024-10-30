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

