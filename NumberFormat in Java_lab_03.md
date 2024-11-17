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
6. [How to Use](#how-to-use)

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
