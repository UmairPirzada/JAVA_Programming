# Java Control Statements and Control Flow

This project demonstrates the implementation and usage of Java control statements and control flow concepts. It includes examples of decision-making, looping, and jump statements with detailed explanations and sample code.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Control Statements Overview](#control-statements-overview)
   - [Decision-Making Statements](#decision-making-statements)
   - [Loop Statements](#loop-statements)
   - [Jump Statements](#jump-statements)
3. [Code Examples](#code-examples)

---

## Introduction

Java control flow enables programmers to direct the order in which statements execute in a program. This project includes examples of `if-else`, `switch`, loops, and jump statements. It serves as a guide for understanding how these fundamental programming constructs operate.

---

## Control Statements Overview

### Decision-Making Statements

1. **If Statement**
   - Syntax:
     ```java
     if (condition) {
         // Statements
     }
     ```
   - Example: Check if `x + y > 20`.

2. **Switch Statement**
   - Syntax:
     ```java
     switch (expression) {
         case value1:
             // Statements
             break;
         default:
             // Default statements
     }
     ```

### Loop Statements

1. **For Loop**
   - Syntax:
     ```java
     for (initialization; condition; increment/decrement) {
         // Loop statements
     }
     ```
2. **While Loop**
   - Syntax:
     ```java
     while (condition) {
         // Loop statements
     }
     ```

### Jump Statements

1. **Break Statement**
   - Exits the loop prematurely.
2. **Continue Statement**
   - Skips the current iteration and continues with the next.

---

## Code Examples

### Example: Simple If Statement

```java
public class DecisionMaking {
    public static void main(String[] args) {
        int x = 10, y = 12;
        if (x + y > 20) {
            System.out.println("x + y is greater than 20");
        }
    }
}
```
