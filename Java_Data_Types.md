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
  
- Non-primitive types can be used to call methods to perform certain operations, wheras primitive types cannot.
  
- Primitive types start with a lowercase letter (like int), while non-primitive types typically starts with an uppercase letter (like String).
  
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

# ASCII and Unicode Code Charts

## ASCII Code Chart (0–127)

| ASCII Code | Character | ASCII Code | Character | ASCII Code | Character | ASCII Code | Character |
|------------|-----------|------------|-----------|------------|-----------|------------|-----------|
| 0          | NUL       | 32         | Space     | 64         | @         | 96         | `         |
| 1          | SOH       | 33         | !         | 65         | A         | 97         | a         |
| 2          | STX       | 34         | "         | 66         | B         | 98         | b         |
| 3          | ETX       | 35         | #         | 67         | C         | 99         | c         |
| 4          | EOT       | 36         | $         | 68         | D         | 100        | d         |
| 5          | ENQ       | 37         | %         | 69         | E         | 101        | e         |
| 6          | ACK       | 38         | &         | 70         | F         | 102        | f         |
| 7          | BEL       | 39         | '         | 71         | G         | 103        | g         |
| 8          | BS        | 40         | (         | 72         | H         | 104        | h         |
| 9          | TAB       | 41         | )         | 73         | I         | 105        | i         |
| 10         | LF        | 42         | *         | 74         | J         | 106        | j         |
| 11         | VT        | 43         | +         | 75         | K         | 107        | k         |
| 12         | FF        | 44         | ,         | 76         | L         | 108        | l         |
| 13         | CR        | 45         | -         | 77         | M         | 109        | m         |
| 14         | SO        | 46         | .         | 78         | N         | 110        | n         |
| 15         | SI        | 47         | /         | 79         | O         | 111        | o         |
| 16         | DLE       | 48         | 0         | 80         | P         | 112        | p         |
| 17         | DC1       | 49         | 1         | 81         | Q         | 113        | q         |
| 18         | DC2       | 50         | 2         | 82         | R         | 114        | r         |
| 19         | DC3       | 51         | 3         | 83         | S         | 115        | s         |
| 20         | DC4       | 52         | 4         | 84         | T         | 116        | t         |
| 21         | NAK       | 53         | 5         | 85         | U         | 117        | u         |
| 22         | SYN       | 54         | 6         | 86         | V         | 118        | v         |
| 23         | ETB       | 55         | 7         | 87         | W         | 119        | w         |
| 24         | CAN       | 56         | 8         | 88         | X         | 120        | x         |
| 25         | EM        | 57         | 9         | 89         | Y         | 121        | y         |
| 26         | SUB       | 58         | :         | 90         | Z         | 122        | z         |
| 27         | ESC       | 59         | ;         | 91         | [         | 123        | {         |
| 28         | FS        | 60         | <         | 92         | \         | 124        | |         |
| 29         | GS        | 61         | =         | 93         | ]         | 125        | }         |
| 30         | RS        | 62         | >         | 94         | ^         | 126        | ~         |
| 31         | US        | 63         | ?         | 95         | _         | 127        | DEL       |

## Unicode Code Examples

| Unicode Code Point | Character  | Description                  |
|--------------------|------------|------------------------------|
| U+00A9             | ©          | Copyright sign               |
| U+00AE             | ®          | Registered sign              |
| U+0391             | Α          | Greek capital letter Alpha   |
| U+03A9             | Ω          | Greek capital letter Omega   |
| U+0416             | Ж          | Cyrillic capital letter Zhe  |
| U+4E00             | 一         | Chinese character for "one"  |
| U+20AC             | €          | Euro sign                    |
| U+221E             | ∞          | Infinity symbol              |
| U+2600             | ☀️          | Sun symbol                   |
| U+1F600            | 😀         | Grinning face emoji          |
| U+1F4A9            | 💩         | Pile of poo emoji            |
| U+1F64F            | 🙏         | Person with folded hands     |

## Key Differences between ASCII and Unicode

- **ASCII** only supports 128 characters (0–127), mainly focusing on English letters, numbers, and control characters.
- **Unicode** supports over 143,000 characters across many languages and includes symbols, emojis, and scripts from all around the world.

