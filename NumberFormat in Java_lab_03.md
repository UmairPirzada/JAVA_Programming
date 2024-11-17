# NumberFormat in Java

The `NumberFormat` class in Java is part of the `java.text` package and is used to format numbers, percentages, and currencies in a locale-sensitive manner. It simplifies tasks like formatting values for financial applications, percentages, or user-friendly number displays.

---

## Why Use NumberFormat?

1. **Locale Sensitivity**: Automatically adjusts number formats based on regional settings.
2. **Consistency**: Ensures uniform formatting across the application.
3. **Ease of Use**: Simplifies conversion to formats like currency or percentages.
4. **Customization**: Allows control over fraction digits, grouping, and rounding.
5. **Readability**: Makes numeric data more user-friendly.

---

## Table of Contents

1. [Currency Formatting](#currency-formatting)
2. [Percentage Formatting](#percentage-formatting)
3. [Locale-Specific Currency Formatting](#locale-specific-currency-formatting)
4. [Custom Number Formatting](#custom-number-formatting)
5. [Rounding Numbers](#rounding-numbers)
6. [Student Tasks](#student-tasks)

---

## Examples

### 1. Currency Formatting

Formats a number as currency using the default locale.

```java
import java.text.NumberFormat;

public class CurrencyFormatting {
    public static void main(String[] args) {
        NumberFormat currency = NumberFormat.getCurrencyInstance();
        String result = currency.format(123456789.6666765565);
        System.out.println("Currency (Default Locale): " + result);
    }
}
```

### Output:
```java
Currency (Default Locale): $123,456,789.67
```

### 2. Percentage Formatting
Formats a number as a percentage.

```java
import java.text.NumberFormat;

public class PercentageFormatting {
    public static void main(String[] args) {
        NumberFormat percent = NumberFormat.getPercentInstance();
        String result = percent.format(0.2); // Converts 0.2 to 20%
        System.out.println("Percentage: " + result);
    }
}
```
## Output:
```java
Percentage: 20%
```
### 3. Locale-Specific Currency Formatting
Formats currency based on a specific locale (e.g., Japan).

```java
import java.text.NumberFormat;
import java.util.Locale;

public class LocaleSpecificCurrencyFormatting {
    public static void main(String[] args) {
        NumberFormat currencyLocale = NumberFormat.getCurrencyInstance(Locale.JAPAN);
        String result = currencyLocale.format(98765.43);
        System.out.println("Currency (Japan): " + result);
    }
}

```
### Output:
```java
Currency (Japan): ￥98,765
```

### 4. Custom Number Formatting
Customize the number of fraction digits in a formatted number.

```java
import java.text.NumberFormat;

public class CustomNumberFormatting {
    public static void main(String[] args) {
        NumberFormat number = NumberFormat.getNumberInstance();
        number.setMinimumFractionDigits(2);
        number.setMaximumFractionDigits(4);
        String result = number.format(12345.6789);
        System.out.println("Formatted Number: " + result);
    }
}
```
### Output:
```java
Formatted Number: 12,345.6789
```

### 5. Rounding Numbers
Rounds a number to the nearest integer.

```java
import java.text.NumberFormat;

public class RoundingNumbers {
    public static void main(String[] args) {
        NumberFormat rounding = NumberFormat.getNumberInstance();
        rounding.setMaximumFractionDigits(0);
        String result = rounding.format(12345.6789);
        System.out.println("Rounded Number: " + result);
    }
}
```
### Output:

```java
Rounded Number: 12,346
```

# Student Tasks
Here are three simple tasks to help you practice using NumberFormat in Java:

### 1. Format a Number as Currency in Different Locales
Write a program to format 5000.75 as currency for the following locales:

- US
  
- UK
  
- Pakistan

  ```java
  Your Code Goes Here...
  ```

### 2. Convert Decimal Values to Percentages
Write a program to format the values 0.123, 0.45, and 0.789 into percentages.

 ```java
  Your Code Goes Here...
  ```

### 3. Customize Fraction Digits
Create a program that formats the number 98765.4321 with the following fraction digit settings:

- Minimum 1 digit, Maximum 3 digits
  
- Minimum 2 digits, Maximum 5 digits

  ```java
  Your Code Goes Here...
  ```




