# Java Control Statements | Control Flow in Java

Java compiler executes the code from top to bottom. The statements in the code are executed according to the order in which they appear. However, Java provides statements that can be used to control the flow of Java code. Such statements are called control flow statements. It is one of the fundamental features of Java, which provides a smooth flow of the program.

Java provides three types of control flow statements:
- **Decision Making statements**
    - if statements
    - switch statement
- **Loop statements**
    - do while loop
    - while loop
    - for loop
    - for-each loop
- **Jump statements**
    - break statement
    - continue statement

## Decision-Making statements:

As the name suggests, decision-making statements decide which statement to execute and when. Decision-making statements evaluate the Boolean expression and control the program flow depending upon the result of the condition provided. There are two types of decision-making statements in Java, i.e., If statement and switch statement.

**Real-life Example**:  
Imagine you are in a shopping mall and you have a discount card. The system checks if the card is valid. If it is, the discount is applied; if not, you pay the full price. 
```java
public class DiscountCheck {
    public static void main(String[] args) {
        boolean hasDiscountCard = true; // Change this to false to test the other condition

        if (hasDiscountCard) {
            System.out.println("Discount applied! Enjoy your shopping.");
        } else {
            System.out.println("No discount available. Please pay the full price.");
        }
    }
}
```

### Output 
```java 
when hasDiscountCard is true:


Discount applied! Enjoy your shopping.

when hasDiscountCard is false:

No discount available. Please pay the full price.
```

### 1) If Statement:
In Java, the "if" statement is used to evaluate a condition. The control of the program is diverted depending upon the specific condition. The condition of the If statement gives a Boolean value, either true or false. In Java, there are four types of if-statements given below:

- Simple if statement
- if-else statement
- if-else-if ladder
- Nested if-statement

**Let's understand the `if` statements one by one.**

# 1) Simple if statement:
It is the most basic statement among all control flow statements in Java. It evaluates a Boolean expression and enables the program to enter a block of code if the expression evaluates to true.


**Syntax of if statement**:

```java
if(condition) {    
    statement 1; // executes when condition is true   
}
```
### Example:
```java
public class Student {    
    public static void main(String[] args) {    
        int x = 10;    
        int y = 12;    
        if(x + y > 20) {    
            System.out.println("x + y is greater than 20");    
        }    
    }      
}
```

### Output:
```java
x + y is greater than 20
```

# Why is the If Statement Important?
In normal code execution, every statement is executed in sequence without any condition. The if statement allows your program to make decisions based on conditions, making it flexible and dynamic. By using the if statement, you can:

### 1. Optimize Performance:
- The program only executes certain code when needed, saving time and resources.
### 2. Enhance User Interaction: 
- It lets you interact with the user and take different actions based on their input.
### 3. Increase Code Flexibility: 
- Your program can react to changing situations (like varying inputs or environmental conditions) rather than follow a rigid sequence.


# 2) if-else statement
The if-else statement is an extension to the if-statement, which uses another block of code, i.e., else block. The else block is executed if the condition of the if-block is evaluated as false.

### Syntax:
```java

if(condition) {    
statement 1; //executes when condition is true   
}  
else{  
statement 2; //executes when condition is false   
}
```

### Example
```java
public class Student {  
public static void main(String[] args) {  
int x = 10;  
int y = 12;  
if(x+y < 10) {  
System.out.println("x + y is less than      10");  
}   else {  
System.out.println("x + y is greater than 20");  
}  
}  
}
```

### Output:
```java
x + y is greater than 20
```
An if-else statement checks a condition and executes one block of code if the condition is true, and another block if the condition is false.

### Real-life Example:
Consider a student’s grading system. If the score is greater than or equal to 50, they pass; otherwise, they fail.
```java
public class GradeCheck {
    public static void main(String[] args) {
        int score = 45;
        if (score >= 50) {
            System.out.println("You passed!");
        } else {
            System.out.println("You failed!");
        }
    }
}
```
### Output:
```java
You failed!
```

# 3) if-else-if ladder:
The if-else-if statement contains the if-statement followed by multiple else-if statements. In other words, we can say that it is the chain of if-else statements that create a decision tree where the program may enter in the block of code where the condition is true. We can also define an else statement at the end of the chain.

An if-else-if ladder is useful when there are multiple conditions to check. It helps to test more than two conditions and executes the corresponding block of code.

### Syntax
```java
if(condition 1) {    
statement 1; //executes when condition 1 is true   
}  
else if(condition 2) {  
statement 2; //executes when condition 2 is true   
}  
else {  
statement 2; //executes when all the conditions are false   
}
```

### Example:

```java
public class Student {  
public static void main(String[] args) {  
String city = "Delhi";  
if(city == "Meerut") {  
System.out.println("city is meerut");  
}else if (city == "Noida") {  
System.out.println("city is noida");  
}else if(city == "Agra") {  
System.out.println("city is agra");  
}else {  
System.out.println(city);  
}  
}  
}  
//Output:

// Delhi
```

### Real-life Example:
Think about an air-conditioning system that adjusts the temperature based on the current room temperature. If it's too cold, it will heat up; if it's too hot, it will cool down; otherwise, it maintains the current temperature.
```java
public class TemperatureCheck {
    public static void main(String[] args) {
        int temperature = 35;
        if (temperature < 15) {
            System.out.println("It's cold.");
        } else if (temperature >= 15 && temperature < 30) {
            System.out.println("It's warm.");
        } else {
            System.out.println("It's hot.");
        }
    }
}
// Output:


// It's hot.
```

# 4). Nested if-statement
In nested if-statements, the if statement can contain a if or if-else statement inside another if or else-if statement.


A nested if statement is an if statement inside another if statement. This is used when there are multiple conditions to check in a hierarchical manner.
### Syntax
```java
if(condition 1) {    
statement 1; //executes when condition 1 is true   
if(condition 2) {  
statement 2; //executes when condition 2 is true   
}  
else{  
statement 2; //executes when condition 2 is false   
}  
}
```
### Example
```java
public class Student {    
public static void main(String[] args) {    
String address = "Delhi, India";    
    
if(address.endsWith("India")) {    
if(address.contains("Meerut")) {    
System.out.println("Your city is Meerut");    
}else if(address.contains("Noida")) {    
System.out.println("Your city is Noida");    
}else {    
System.out.println(address.split(",")[0]);    
}    
}else {    
System.out.println("You are not living in India");    
}    
}    
}
// Output:

// Delhi

```


### Real-life Example:
In an online shopping website, if the user is logged in and has a valid membership, they can access premium discounts. Otherwise, they don’t.
```java
public class MemberDiscount {
    public static void main(String[] args) {
        boolean isLoggedIn = true;
        boolean hasMembership = true;

        if (isLoggedIn) {
            if (hasMembership) {
                System.out.println("You are eligible for a discount.");
            } else {
                System.out.println("You need a membership to get a discount.");
            }
        } else {
            System.out.println("Please log in to check your discount eligibility.");
        }
    }
}


// Output:


// You are eligible for a discount.
```


# 5). Java Switch Statement

In Java, Switch statements are similar to if-else-if statements. The switch statement contains multiple blocks of code called cases, and a single case is executed based on the variable being switched. The switch statement is easier to use instead of if-else-if statements. It also enhances the readability of the program.

### Points to Note About Switch Statement:
- The case variables can be `int`, `short`, `byte`, `char`, or enumeration. String type is also supported since version 7 of Java.
- Cases cannot be duplicate.
- Default statement is executed when none of the cases match the value of the expression. It is optional.
- The `break` statement terminates the switch block when the condition is satisfied. It is optional; if not used, the next case is executed.
- The case expression must be of the same type as the variable and should be a constant value.
- The switch permits only `int`, `string`, and `enum` type variables to be used.

### Syntax of Switch Statement:
```java
switch (expression) {  
    case value1:  
        statement1;  
        break;  
    // Additional cases
    case valueN:  
        statementN;  
        break;  
    default:  
        default statement;  
}
```

### Example of Switch Statement:
Here is a simple example to demonstrate the flow of the switch statement.

**Student.java**
```java
public class Student implements Cloneable {  
    public static void main(String[] args) {  
        int num = 2;  
        switch (num) {  
            case 0:  
                System.out.println("number is 0");  
                break;  
            case 1:  
                System.out.println("number is 1");  
                break;  
            default:  
                System.out.println(num);  
        }  
    }  
}
// Output:
// 2
```

### Real-Life Example 1: Weekday Checker
Imagine a calendar application where a user inputs a number to get the corresponding weekday.

**WeekdayChecker.java**
```java
public class WeekdayChecker {  
    public static void main(String[] args) {  
        int day = 3;  
        switch (day) {  
            case 1:  
                System.out.println("Monday");  
                break;  
            case 2:  
                System.out.println("Tuesday");  
                break;  
            case 3:  
                System.out.println("Wednesday");  
                break;  
            case 4:  
                System.out.println("Thursday");  
                break;  
            case 5:  
                System.out.println("Friday");  
                break;  
            case 6:  
                System.out.println("Saturday");  
                break;  
            case 7:  
                System.out.println("Sunday");  
                break;  
            default:  
                System.out.println("Invalid day number!");  
        }  
    }  
}

// Output:


// Wednesday
```

### Real-Life Example 2: Online Order Status
An e-commerce platform checks the status of an order and prints an appropriate message.

**OrderStatus.java**
```java
public class OrderStatus {  
    public static void main(String[] args) {  
        String status = "Shipped";  
        switch (status) {  
            case "Pending":  
                System.out.println("Your order is pending.");  
                break;  
            case "Shipped":  
                System.out.println("Your order has been shipped.");  
                break;  
            case "Delivered":  
                System.out.println("Your order has been delivered.");  
                break;  
            default:  
                System.out.println("Invalid order status.");  
        }  
    }  
}
// Output:

// Your order has been shipped.
```

### Real-Life Example 3: Grade Evaluation
A grading system evaluates a student's performance based on their grade.

**GradeEvaluator.java**

``` java
public class GradeEvaluator {  
    public static void main(String[] args) {  
        char grade = 'B';  
        switch (grade) {  
            case 'A':  
                System.out.println("Excellent!");  
                break;  
            case 'B':  
                System.out.println("Good job!");  
                break;  
            case 'C':  
                System.out.println("You can do better!");  
                break;  
            case 'D':  
                System.out.println("Keep trying!");  
                break;  
            default:  
                System.out.println("Invalid grade.");  
        }  
    }  
}

// Output:

// Good job!
```
# Benefits of Switch Statements
### 1. Improved Readability: 
- Switch statements are more structured and readable than multiple if-else-if blocks.
### 2. Simplified Coding: 
- Using switch reduces the complexity of nested conditional statements.
### 3. Better Performance: 
- In some scenarios, switch statements perform better than if-else due to their optimized implementation in the Java compiler.
### 4. Flexibility:
- Switch supports multiple data types like int, String, and enum for different use cases.
  
- Switch statements are a powerful feature in Java that simplifies decision-making and enhances the efficiency of code.

# Java Decision-Making Statements Practice Tasks

Below are practice tasks for each type of decision-making statement: **Simple if**, **if-else**, **if-else-if**, and **switch**. These tasks will help you understand how to implement these control flow statements in real-world scenarios.

---

### 1. Simple If Practice Task
**Task 1**:  
Write a program that checks if a number is positive. If the number is positive, print `"The number is positive"`.

**Hint**:  
Use a single `if` statement to evaluate the condition.

**Example Code**:
```java
Your Code Goes Here...
```

### 2. If-Else Practice Task
**Task2:**
Write a program to check if a number is even or odd. If the number is even, print "Even number". Otherwise, print "Odd number".

**Hint:**
Use the modulus operator % to check for even or odd.


```java
Your Code Goes Here...
```

### 3. If-Else-If Practice Task
**Task 3:**
Write a program to determine the grade of a student based on their score:

- If the score is 90 or above, print "A".

- If the score is 80 to 89, print "B".

- If the score is 70 to 79, print "C".

- If the score is below 70, print "Fail".

**Hint:**
Use multiple if-else-if conditions.

```java
Your Code Goes Here...
```

### 4. Switch Statement Practice Task
**Task 4:**
Write a program that prints the type of vehicle based on its number:

- 1: "Car",

- 2: "Bike", 

- 3: "Truck", 

- 4: "Bus".

If the number is not between 1 and 4, print "Invalid vehicle type".
**Hint:**
Use a switch statement to map numbers to vehicle types.

```java
Your Code Goes Here...
```

# Loop Statements
In programming, sometimes we need to execute the block of code repeatedly while some condition evaluates to true. However, loop statements are used to execute the set of instructions in a repeated order. The execution of the set of instructions depends upon a particular condition.


In programming, we often encounter scenarios where we need to execute a block of code multiple times. Rather than duplicating code, **loop statements** allow us to run a set of instructions repeatedly based on a condition.

In **Java**, loops help automate tasks efficiently by iterating over code blocks until a specific condition is met.

---

In Java, we have three types of loops that execute similarly. However, there are differences in their syntax and condition checking time.

## Types of Loops in Java

Java provides three types of loops:

1. **For Loop**
2. **While Loop**
3. **Do-While Loop**

Each loop functions similarly but differs in syntax and when the condition is checked.

---

**Let's understand the loop statements one by one.**

In programming, we often encounter scenarios where we need to execute a block of code multiple times. Rather than duplicating code, **loop statements** allow us to run a set of instructions repeatedly based on a condition.

In **Java**, loops help automate tasks efficiently by iterating over code blocks until a specific condition is met.

---

## Types of Loops in Java

Java provides three types of loops:

1. **For Loop**
2. **While Loop**
3. **Do-While Loop**

Each loop functions similarly but differs in syntax and when the condition is checked.

---

## Why Do We Use Loops?

Loops are essential in programming because:
- They automate repetitive tasks.
- They simplify working with datasets, arrays, or files.
- They reduce redundancy and improve code readability.
- They make programs dynamic and scalable, adapting to runtime conditions.

---

## Why Do We Need Loops?

Without loops:
- We would need to write the same code multiple times, leading to redundancy.
- Programs would become harder to debug and maintain.
- Handling dynamic or large datasets would be inefficient.

By using loops, we can:
1. Handle repetitive logic with ease.
2. Save time in both coding and execution.
3. Adapt to varying input sizes or conditions dynamically.

---

## Benefits of Loops

1. **Efficiency**: Write less code for repetitive tasks.
2. **Automation**: Handle large datasets or repeated actions programmatically.
3. **Flexibility**: Dynamically adapt to conditions during execution.
4. **Readability**: Simplifies code structure and logic.
5. **Scalability**: Easily handle increasing complexity or input size.

---
# For Loop Execution Explained

In Java, the `for` loop allows repeated execution of a block of code as long as a specified condition is met. The execution of the `for` loop is governed by the following structure:

```java
for (initialization; condition; increment/decrement) {
    // Loop body
}   
```

# Reason Why the Body Executes Before Increment
The reason the body of the loop is executed before the increment happens for the first time lies in the logical flow of the for loop in Java. This logical flow ensures that the current value of the loop variable is used before it is modified by the increment.

**The flow chart for the for-loop is given below.**

![image](https://github.com/user-attachments/assets/853abb52-bffd-4530-91ac-d9dd60c54c2e)

Consider the following example to understand the proper functioning of the for loop in java.

**Calculation.java**
```java
public class Calculattion {  
public static void main(String[] args) {  
// TODO Auto-generated method stub  
int sum = 0;  
for(int j = 1; j<=10; j++) {  
sum = sum + j;  
}  
System.out.println("The sum of first 10 natural numbers is " + sum);  
}  
}  
// Output:

// The sum of first 10 natural numbers is 55
```

![image](https://github.com/user-attachments/assets/21553fc0-299d-46b6-9388-012cf78a1223)

# Execution Steps:

### Initialization (int j = 1):

j is initialized to 1 at the start of the loop. This happens only once before the loop starts.

### Condition Check (j <= 10):

The condition j <= 10 is evaluated. If true, the loop proceeds. If false, the loop terminates.

### Body Execution (sum = sum + j):

The value of j (which is initially 1) is used inside the loop body. In the first iteration, j = 1 is added to sum.
The body of the loop is executed before the increment because we want to use the current value of j in the loop body.

### Increment (j++):

After the body executes, j++ increments the value of j by 1. This happens after the loop body runs.

### Repeat:

The condition j <= 10 is checked again. If true, the loop continues, and the above steps are repeated with the new value of j.

# Execution Order in the First Iteration:

### j = 1 → Initialization.
Check j <= 10 → 1 <= 10 → true (Condition is true).

### Execute 
loop body → sum = sum + j → sum = 0 + 1 → sum = 1.

### Increment 
j++ → j = 2.

Thus, the value of j starts as 1, and the increment (j++) happens only after the loop body is executed. The body always uses the current value of j, and only after that does the value change with the increment.

# Example to Clarify
Consider this loop:

```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

# Execution Breakdown:

- i = 0 → Initialization.
  
- i < 5 → 0 < 5 → true (Condition).
  
- Enter the body: System.out.println("i = 0");.
  
- Increment: i++ → i = 1.
  
- Repeat steps 2-4 until i < 5 becomes false.

# Real-World Analogy
Imagine you are climbing stairs:

- You start on the first step (Initialization: int j = 1).
 
- You check whether there are more steps to climb (Condition: j <= 10).
 
- You climb the current step (Body execution: perform some action).

- After climbing the current step, you move to the next step (Increment: j++).

If you increment first, you would skip the first step. Similarly, in the loop, incrementing first would skip using the initial value of j in the body.

# Key Takeaway
The loop evaluates the current state of the loop variable before it is changed. This ensures that the body of the loop can use the current value of the loop variable for processing, while the increment ensures that the loop variable is updated for the next iteration.

This design allows predictable and logical flow, where:

- **Condition** is checked.
  
- **Body** is executed using the current value.
  
- **Increment** updates the loop variable for the next iteration.


### Explanation:

- **Initialization** happens before the loop starts and only once.
  
- **Condition** checks if the loop body should execute.
  
- **Body execution** happens before increment to ensure the current value of `j` is used.
  
- **Increment** happens after the body executes to ensure the updated value is used in the next iteration.

---

## Real-World Scenarios of Loops

### For Loop Example: Printing Multiplication Tables
- **Scenario**: A school program generates a multiplication table for any given number.
```java
public class MultiplicationTable {
    public static void main(String[] args) {
        int number = 5; // Generate table for 5
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + (number * i));
        }
    }
}
```

# Java for-each loop
Java provides an enhanced for loop to traverse the data structures like array or collection. In the for-each loop, we don't need to update the loop variable. 

The syntax to use the for-each loop in java is given below.

```java
for(data_type var : array_name/collection_name){    
//statements    
}
```

Consider the following example to understand the functioning of the for-each loop in Java.

**Calculation.java**
```java
public class Calculation {    
public static void main(String[] args) {    
// TODO Auto-generated method stub    
String[] names = {"Java","C","C++","Python","JavaScript"};    
System.out.println("Printing the content of the array names:\n");    
for(String name:names) {    
System.out.println(name);    
}    
}    
}

// Output:

// Printing the content of the array names:

// Java
// C
// C++
// Python
// JavaScript
```


# While Loop in Java
The `while` loop is also used to iterate over the number of statements multiple times. However, if we don't know the number of iterations in advance, it is recommended to use a while loop. Unlike for loop, the initialization and increment/decrement doesn't take place inside the loop statement in while loop.

It is also known as the entry-controlled loop since the condition is checked at the start of the loop. If the condition is true, then the loop body will be executed; otherwise, the statements after the loop will be executed.

The `while` loop in Java is used for executing a block of code repeatedly while a specified condition is `true`. 
**It is ideal when the number of iterations is not known in advance.**

Unlike the `for` loop, the `while` loop does not have initialization and increment/decrement within the loop structure. Instead, **they are handled separately before the loop starts.**

## Syntax of the While Loop

```java
while (condition) {
    // Looping statements
}
```
The while loop is an entry-controlled loop, meaning the condition is checked before entering the loop body. If the condition is true, the loop body executes. Otherwise, the loop body is skipped.


# Control Flow of While Loop
1. Condition is evaluated first.
   
2. If the condition is true, the loop body executes.
   
3. After each iteration, the condition is re-evaluated.
   
4. If the condition is false, the loop terminates and the program continues with the statements after the loop.
   
# Flowchart for the While Loop
Start -> Evaluate condition -> If true, execute loop body -> After execution, go back to condition evaluation
                                   |                                 |
                                   V                                 |
                              Stop loop                           End


