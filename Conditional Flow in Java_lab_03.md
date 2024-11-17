# Java Conditional Flow and Operators

This repository contains examples and explanations of how to use **Comparison Operators** and **Logical Operators** in Java.

## Table of Contents

- [Introduction](#introduction)
- [Comparison Operators](#comparison-operators)
- [Logical Operators](#logical-operators)
  - [AND Operator (`&&`)](#and-operator-&&)
  - [OR Operator (`||`)](#or-operator-)
  - [NOT Operator (`!`)](#not-operator-)
- [Example Code](#example-code)
- [Tasks](#tasks)

## Introduction

Conditional flow refers to controlling the flow of execution in a program based on certain conditions. This is achieved using **comparison operators** and **logical operators**. These operators allow you to compare values and combine conditions to make decisions in your programs.

## Comparison Operators

Comparison operators are used to compare two values and return a boolean result (`true` or `false`). Below are the most commonly used comparison operators in Java:

```text
| Operand 1  | Operand 2  | Operator | Description                                         | Result |
|------------|------------|----------|-----------------------------------------------------|--------|
| x = 1      | y = 1      | ==       | Checks if two values are equal                       | true   |
| x = 1      | y = 2      | !=       | Checks if two values are not equal                   | true   |
| x = 3      | y = 5      | <        | Checks if left value is less than right value        | true   |
| x = 6      | y = 5      | >        | Checks if left value is greater than right value     | true   |
| x = 4      | y = 4      | <=       | Checks if left value is less than or equal to right  | true   |
| x = 7      | y = 8      | >=       | Checks if left value is greater than or equal to right | false |
```
# Logical Operators
Logical operators are used to combine multiple boolean conditions and return a single boolean value. Below are the most commonly used logical operators in java:

### AND Operator (&&)
The AND operator (&&) returns true only if both conditions are true. If either one of the conditions is false, the result will be false.

###  AND Operator (&&) Truth Table

The **AND** operator (`&&`) returns `true` only when both operands are `true`. In all other cases, it returns `false`.
```text
| Operand 1 | Operand 2 | AND (&&) |
|-----------|-----------|----------|
| *true*  | **true**  | **true** |
| **true**  | **false** | **false**|
| **false** | **true**  | **false**|
| **false** | **false** | **false**|
```
### Explanation:
- **true && true** = `true`
  
- **true && false** = `false`
  
- **false && true** = `false`
  
- **false && false** = `false`


```text
| Operand 1  | Operand 2  | Operator | Description                                         | Result |
|------------|------------|----------|-----------------------------------------------------|--------|
| x = 4      | y = 5      | &&       | Logical AND - true if both conditions are true      | true   |
| x = 4      | y = 2      | &&       | Logical AND - true if both conditions are true      | false  |
```

The AND operator ensures that both conditions must be `true` to produce a `true` result.

---

### OR Operator (||)
The OR operator (||) returns true if either condition is true. If both conditions are false, the result will be false. 

### OR Operator (||) Truth Table

The **OR** operator (`||`) returns `true` if at least one of the operands is `true`. If both operands are `false`, it returns `false`.
```text
| Operand 1 | Operand 2 | OR (||)  |
|-----------|-----------|----------|
| **true**  | **true**  | **true** |
| **true**  | **false** | **true** |
| **false** | **true**  | **true** |
| **false** | **false** | **false**|
```
### Explanation:
- **true || true** = `true`
  
- **true || false** = `true`
  
- **false || true** = `true`
  
- **false || false** = `false`



```text
| Operand 1  | Operand 2  | Operator | Description                                         | Result |
|------------|------------|----------|-----------------------------------------------------|--------|
| x = 4      | y = 4      | ||       | Logical OR - true if either condition is true       | true   |
| x = 4      | y = 5      | ||       | Logical OR - true if either condition is true       | true   |
| x = 4      | y = 3      | ||       | Logical OR - false if both conditions are false     | false  |

```
The OR operator returns `true` if either condition is `true`. If both conditions are `false`, it returns `false`.

---

### NOT Operator (!)
The NOT operator (!) is a logical negation operator. It negates the condition, returning true if the condition is false and vice versa.

### NOT Operator (!) Truth Table

The **NOT** operator (`!`) inverts the truth value of its operand. If the operand is `true`, it returns `false`, and if the operand is `false`, it returns `true`.
```text
| Operand | NOT (!) |
|---------|---------|
| **true**  | **false** |
| **false** | **true**  |
```
### Explanation:
- **!true** = `false`
  
- **!false** = `true`

```text
| Operand 1  |            | Operator | Description                                         | Result |
|------------|------------|----------|-----------------------------------------------------|--------|
| x = 4      |            | !        | Logical NOT - negates the condition                 | false  |
| x = 0      |            | !        | Logical NOT - negates the condition                 | true   |
```
The NOT operator is used to negate or invert the value of a boolean expression.

# Example Code
### **Example 1:** Equality Operator (==)
```java
int x = 1;

int y = 1;

System.out.println(x == y);  // Output: true
```

This checks if x is equal to y. If they are equal, it returns true; otherwise, it returns false.


### **Example 2:** Inequality Operator (!=)


```java
int x = 1;

int y = 2;

System.out.println(x != y);  // Output: true
```

This checks if x is not equal to y. If they are not equal, it returns true; otherwise, it returns false.

### **Example 3:** Logical AND (&&)

```java
int temperature = 22;

boolean isWarm = temperature > 20 && temperature < 30;

System.out.println(isWarm);  // Output: true

```

### **Example 4:** Logical OR (||)
```java
boolean hasHighIncome = true;
boolean hasGoodCredit = false;
boolean isEligible = hasHighIncome || hasGoodCredit;
System.out.println(isEligible);  // Output: true
```

### **Example 5:** Logical NOT (!)
```java
boolean hasCriminalRecord = true;
boolean isEligible = !(hasCriminalRecord);
System.out.println(isEligible);  // Output: false
```
