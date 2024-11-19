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
### The flow chart for the for-loop is given below.

![image](https://github.com/user-attachments/assets/a677d650-5fcd-45fd-93ae-9307f4e86ef0)


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

Start ->  Evaluate condition ->  If true, execute loop body ->  After execution, go back to condition evaluation

![image](https://github.com/user-attachments/assets/deff6197-fc1c-4dcc-a1c8-69fd09faa8e0)


### Example 1: Printing First 10 Even Numbers
```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int i = 0;
        System.out.println("Printing the list of first 10 even numbers \n");
        
        while(i <= 10) {
            System.out.println(i);
            i = i + 2;
        }
    }
}

// Output:

// Printing the list of first 10 even numbers

// 0
// 2
// 4
// 6
// 8
// 10
```
In this example, the while loop prints the first 10 even numbers starting from 0, incrementing by 2 after each iteration.


### Example 2: Printing Numbers from 1 to 5
``` java

public class Calculation {
    public static void main(String[] args) {
        int i = 1;
        while(i <= 5) {
            System.out.println(i);
            i++; // Incrementing i
        }
    }
}
// Output:

// 1
// 2
// 3
// 4
// 5

```

Here, the while loop prints numbers from 1 to 5. The condition i <= 5 is checked at the start of each iteration. Once i exceeds 5, the loop terminates.

### Example 3: Counting Down from 10 to 1
``` java

public class Calculation {
    public static void main(String[] args) {
        int i = 10;
        while(i >= 1) {
            System.out.println(i);
            i--; // Decrementing i
        }
    }
}
// Output:


// 10
// 9
// 8
// 7
// 6
// 5
// 4
// 3
// 2
// 1

```
In this example, the while loop counts down from 10 to 1, decrementing i after each iteration.


# Why Use a While Loop?
A while loop is useful when:

- The number of iterations is not known beforehand.
  
- You need to keep repeating a task until a certain condition is met (e.g., user input validation, reading data from a file until EOF).

- The condition for the loop is complex or dynamic.

# When to Choose a While Loop Over a For Loop?
### 1. Indeterminate Iterations:

- If the number of iterations is not determined at the beginning, a while loop is a better choice. For example, in cases where the loop continues until a condition changes (e.g., waiting for a user input or checking a dynamic condition).
  
### 2. Infinite Loops:

- A while loop is commonly used for creating infinite loops, where the loop runs forever unless a break condition occurs. For example:
```java
while(true) {
    // Some code here
    if(someCondition) {
        break;
    }
}
```
A for loop is generally less suited for this purpose because it needs a predefined initialization and condition.


# Comparison Between While Loop and For Loop
### Similarities:
- Both loops are used to repeat a block of code multiple times.

- Both loops check a condition before executing the body (entry-controlled).

- Both can be used to achieve the same result with slightly different syntax.

### Differences:
### 1. Initialization and Increment/Decrement:

- **For Loop:** Initialization, condition checking, and increment/decrement all happen within the loop header.
  
- **While Loop:** Initialization is done before the loop starts, and increment/decrement happens inside the loop body.
  
# Use Case:

- **For Loop:** Best when the number of iterations is known in advance.
  
- **While Loop:** Best when the number of iterations is not known in advance or when the loop is dependent on a condition that may change during execution.
  
# Benefits of Using While Loop
- **Flexibility:** It allows more flexibility since the condition can be more complex or dynamic.
  
- **Useful for Indeterminate Conditions:** It’s the right choice when you need the loop to run as long as a condition is true and you don't know beforehand how many iterations will be required.
  
- **Infinite Loop Creation:** While loops are often used for creating infinite loops, which are controlled by break conditions or external factors.
  
# Conclusion
Use a while loop when the number of iterations isn't predetermined or when the loop needs to continue until a condition changes. For loops are more structured when you know the exact number of iterations beforehand. Both loops are valuable tools in Java programming, each suited to different scenarios.


### Explanation:

- **Why Use While Loop**: Clarified when to use the `while` loop, especially when iterations are not known in advance.
- **Comparison with For Loop**: Discussed the differences and use cases for `while` and `for` loops, helping the reader understand which loop is more appropriate for specific scenarios.
- **Benefits**: Emphasized the flexibility and suitability of the `while` loop in certain use cases like indefinite iterations or complex conditions.

---
# Do-While Loop in Java

The do-while loop checks the condition at the end of the loop after executing the loop statements. When the number of iteration is not known and we have to execute the loop at least once, we can use do-while loop.


The `do-while` loop is similar to the `while` loop, but it checks the condition at the end of the loop after executing the loop statements. This ensures that the loop body will execute at least once, even if the condition is `false` initially.

It is also known as the **exit-controlled loop** since the condition is checked after the loop body executes.

## Syntax of the Do-While Loop

```java
do {
    // Statements
} while (condition);
```
The do-while loop guarantees that the loop body will execute at least once, regardless of the condition. After the execution, the condition is evaluated, and if it's true, the loop continues; otherwise, the loop terminates.

### The flow chart for the while loop is given in the following image.

![image](https://github.com/user-attachments/assets/5c7f38c8-f15f-4f8b-8c43-01fa3ec1283d)

### Example 1: Printing the First 10 Even Numbers
```java
public class Calculation {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int i = 0;
        System.out.println("Printing the list of first 10 even numbers \n");
        
        do {
            System.out.println(i);
            i = i + 2;
        } while (i <= 10);
    }
}
```
```text
Output:

Printing the list of first 10 even numbers
0
2
4
6
8
10
```
In this example, the do-while loop prints the first 10 even numbers starting from 0, incrementing by 2 after each iteration.

### Example 2: Printing Numbers from 1 to 5
```java
public class Calculation {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println(i);
            i++; // Incrementing i
        } while (i <= 5);
    }
}
```
```text
Output:

1
2
3
4
5

```
In this example, the do-while loop prints numbers from 1 to 5. The condition i <= 5 is checked after each iteration.


### Example 3: Counting Down from 10 to 1
```java

public class Calculation {
    public static void main(String[] args) {
        int i = 10;
        do {
            System.out.println(i);
            i--; // Decrementing i
        } while (i >= 1);
    }
}
```
```text
Output:

10
9
8
7
6
5
4
3
2
1
```

In this example, the do-while loop counts down from 10 to 1, decrementing i after each iteration.

# Real-Life Example of a Do-While Loop
A common real-life scenario where a do-while loop can be applied is in a user input validation system. For example, let's imagine you're creating a program that asks users to enter a valid age. You want the program to keep asking for the input until the user enters a valid age (i.e., a number between 0 and 120).

Here’s how a do-while loop can handle this situation:

### Example: User Input for Age Validation
```java
import java.util.Scanner;

public class AgeValidation {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int age;

        do {
            System.out.print("Please enter your age (0-120): ");
            age = scanner.nextInt();

            if (age < 0 || age > 120) {
                System.out.println("Invalid age! Please enter a valid age.");
            }
        } while (age < 0 || age > 120);

        System.out.println("Thank you! Your age is: " + age);
    }
}
```

### Explanation:
**User Input:** The program asks the user to input their age.

**Validation:** After each input, the program checks if the age is between 0 and 120. If the input is outside this range, the program prints an error message and asks the user to input the age again.

**Loop Guarantee:** The do-while loop ensures that the program will ask for the age at least once, and will only stop asking if the user inputs a valid age.
# When Is This Useful?
**Real-time Validation:** This is commonly seen in forms or systems where user input must meet certain criteria (e.g., age range, password strength).

**Interactive Systems:** Many applications, such as games or registration systems, require continuous user input until valid data is entered.
---

# Why Use a Do-While Loop?
A do-while loop is useful when:

- **At least one execution is required:** You need the loop body to execute at least once, regardless of the condition.
  
- **User input validation:** It's helpful for scenarios where you want to prompt the user for input at least once and continue prompting until a valid input is received.
- 
### For example:
 - asking a user to input a number until a valid number is entered.


# Comparison with For Loop and While Loop
### Similarities:
- **Looping Constructs:** All three (for, while, and do-while) are used to execute a block of code repeatedly.
  
- **Condition Checking:** The condition is checked at the start of each iteration for the while and for loops, but in the do-while loop, the condition is checked after the loop body.
### Differences:
**Condition Checking:**

- **For Loop:** Initialization, condition, and increment/decrement are all part of the loop header.
  
- **While Loop:** Condition is checked before entering the loop. It is ideal when the number of iterations is unknown, and the condition might fail right at the beginning.

- **Do-While Loop:** Condition is checked after the loop body. This guarantees the loop body executes at least once, making it suitable for situations where the loop body needs to execute initially regardless of the condition.
  
# Use Case:

**For Loop:** Best when the number of iterations is known in advance, like iterating over a fixed range or a collection.

**While Loop:** Best when the number of iterations is not known and the condition is checked at the beginning.

**Do-While Loop:** Best when the loop body should execute at least once, and the condition is checked after the first execution.

# Benefits of Using a Do-While Loop
**At Least One Iteration:** The loop guarantees that the statements inside the loop will run at least once, which is useful in scenarios like user input or menu-driven programs.

**Suitable for User Interaction:** When you want to prompt the user for input until they provide valid data, a do-while loop is ideal.

**Exit-Controlled Loop:** Since the condition is checked after the loop body, it ensures that the loop executes once before deciding whether to continue.

# Conclusion
The do-while loop is a useful construct when you need the loop body to execute at least once, and the condition is evaluated after the loop runs. It is especially effective for situations where an action needs to be performed first, and then a decision is made based on the outcome. When compared to for and while loops, the do-while loop is unique in that it guarantees execution of the loop body before the condition is checked.

---

# Jump Statements in Java

Jump statements are used to transfer the control of the program to specific statements. They allow altering the natural flow of loops and switch cases to handle certain conditions efficiently. In other words, jump statements transfer the execution control to the other part of the program. There are two types of jump statements in Java, i.e., break and continue.

**There are two types of jump statements in Java:**
1. **`break` Statement**
   
3. **`continue` Statement**

---

# Java `break` Statement

As the name suggests, the break statement is used to break the current flow of the program and transfer the control to the next statement outside a loop or switch statement. However, it breaks only the inner loop in the case of the nested loop.

The break statement cannot be used independently in the Java program, i.e., it can only be written inside the loop or switch statement.

The `break` statement is used to terminate the current loop or switch statement prematurely. It transfers control to the statement immediately following the loop or switch.

### Syntax:
```java
break;
```

### Example 1: Basic break in a for loop

Consider the following example in which we have used the break statement with the for loop.

**BreakExample.java**

```java
public class BreakExample {  
    public static void main(String[] args) {  
        for (int i = 0; i <= 10; i++) {  
            System.out.println(i);  
            if (i == 6) {  
                break; // Exit the loop when i equals 6
            }  
        }  
    }  
}
```

```text
Output:

0
1
2
3
4
5
6
```

### Example 2: break with Labeled Loops

```java 
public class Calculation {  
    public static void main(String[] args) {  
        a:  
        for (int i = 0; i <= 10; i++) {  
            b:  
            for (int j = 0; j <= 15; j++) {  
                c:  
                for (int k = 0; k <= 20; k++) {  
                    System.out.println(k);  
                    if (k == 5) {  
                        break a; // Exit the outermost loop
                    }  
                }  
            }  
        }  
    }  
}
```
```text
Output:

0
1
2
3
4
5
```

### Example 3: Real-World Use Case - Searching for an Item
```java

public class RealWorldBreak {  
    public static void main(String[] args) {  
        String[] items = {"Apple", "Banana", "Cherry", "Date"};  
        String search = "Cherry";  
        
        for (String item : items) {  
            System.out.println("Checking: " + item);  
            if (item.equals(search)) {  
                System.out.println("Found " + search + "! Exiting the loop.");  
                break; // Exit the loop when the item is found
            }  
        }  
    }  
}
```
```text
Output:

Checking: Apple
Checking: Banana
Checking: Cherry
Found Cherry! Exiting the loop.
```

### Example 4: Break Nested Loops in a Game
```java

public class GameExample {  
    public static void main(String[] args) {  
        outer:  
        for (int level = 1; level <= 3; level++) {  
            System.out.println("Level " + level);  
            for (int life = 1; life <= 3; life++) {  
                System.out.println("Life " + life);  
                if (life == 2 && level == 2) {  
                    System.out.println("Exiting the game at Level 2, Life 2.");  
                    break outer;  
                }  
            }  
        }  
    }  
}
```
```text
Output:

Level 1
Life 1
Life 2
Life 3
Level 2
Life 1
Life 2
Exiting the game at Level 2, Life 2.
```

# Real-World Benefits
### 1. Efficient Loop Termination:

- Saves computation by stopping unnecessary iterations.
  
- E.g., stopping a file search when the desired file is found.
### 2. Nested Loop Control:

- Exiting specific loops in complex nested scenarios.
  
- E.g., game development, simulation control, etc.
### Error Handling and Early Exit:

- Used to exit loops when encountering an error or invalid state.
  
- E.g., checking system conditions or input validity.

# Java `continue` Statement

The `continue` statement in Java is used to skip the current iteration of a loop and move to the next iteration. Unlike the `break` statement, it does not terminate the loop but skips the rest of the code for the current iteration.

Unlike break statement, the continue statement doesn't break the loop, whereas, it skips the specific part of the loop and jumps to the next iteration of the loop immediately.


---

## Syntax:
```java
continue;
```


# Why Use continue?
- To skip unnecessary or unwanted iterations in a loop.
  
- To handle specific cases without terminating the loop.
  
- Useful in scenarios where certain conditions require bypassing parts of the loop logic.
  
# Benefits of continue:
- **Efficiency:** Reduces redundant code by skipping specific iterations.
  
- **Flexibility:** Allows more granular control of loop execution.

- **Error Handling:** Helps handle invalid or unwanted conditions in loops without terminating them.

  Consider the following example to understand the functioning of the continue statement in Java

 ### Example 1: Skipping Specific Values
```java
 public class ContinueExample {  
    public static void main(String[] args) {  
        for (int i = 0; i <= 2; i++) {  
            for (int j = i; j <= 5; j++) {  
                if (j == 4) {  
                    continue; // Skip the current iteration when j equals 4
                }  
                System.out.println(j);  
            }  
        }  
    }  
}
```
```text
Output:

Copy code
0
1
2
3
5
1
2
3
5
2
3
5
```

# Dry Run:
### - Outer Loop (i loop):
- The outer loop iterates over i from 0 to 2 (i <= 2).
  
### - Inner Loop (j loop):
- For each value of i, the inner loop iterates over j from i to 5 (j <= 5).
### - Key Logic:
- If j == 4, the continue statement skips the current iteration of the inner loop, so System.out.println(j) is not executed for j == 4.
  
# Step-by-Step Execution:
### 1. Iteration 1 (i = 0):

- j = 0: System.out.println(0) → Output: 0.

- j = 1: System.out.println(1) → Output: 1.

- j = 2: System.out.println(2) → Output: 2.

- j = 3: System.out.println(3) → Output: 3.

- j = 4: continue → Skips System.out.println(4).

- j = 5: System.out.println(5) → Output: 5.

### 2. Iteration 2 (i = 1):

- j = 1: System.out.println(1) → Output: 1.

- j = 2: System.out.println(2) → Output: 2.

- j = 3: System.out.println(3) → Output: 3.

- j = 4: continue → Skips System.out.println(4).

- j = 5: System.out.println(5) → Output: 5.

### 3. Iteration 3 (i = 2):

- j = 2: System.out.println(2) → Output: 2.

- j = 3: System.out.println(3) → Output: 3.

- j = 4: continue → Skips System.out.println(4).

- j = 5: System.out.println(5) → Output: 5.

# Explanation:
Each time j == 4, the continue statement skips the System.out.println(j) and moves to the next iteration of the inner loop.

For all other values of j, the value is printed as expected.

### Example 2: Skipping Even Numbers
```java
public class SkipEvenNumbers {  
    public static void main(String[] args) {  
        for (int i = 1; i <= 10; i++) {  
            if (i % 2 == 0) {  
                continue; // Skip even numbers
            }  
            System.out.println("Odd number: " + i);  
        }  
    }  
}
```
```text
Output:

Odd number: 1
Odd number: 3
Odd number: 5
Odd number: 7
Odd number: 9
```

### Example 3: Real-World Use Case - Skipping Invalid Input
```java
public class SkipInvalidInput {  
    public static void main(String[] args) {  
        String[] inputs = {"12", "abc", "45", "xyz", "78"};  
        
        for (String input : inputs) {  
            try {  
                int num = Integer.parseInt(input);  
                System.out.println("Valid number: " + num);  
            } catch (NumberFormatException e) {  
                continue; // Skip invalid inputs
            }  
        }  
    }  
}
```
```text
Output:

Valid number: 12
Valid number: 45
Valid number: 78
```
### Example 4: Skipping Low Scores in a Game
``` java

public class SkipLowScores {  
    public static void main(String[] args) {  
        int[] scores = {45, 32, 85, 91, 28, 67};  

        for (int score : scores) {  
            if (score < 50) {  
                System.out.println("Skipping low score: " + score);  
                continue; // Skip scores below 50
            }  
            System.out.println("High score: " + score);  
        }  
    }  
}
```
```text
Output:

Skipping low score: 45
Skipping low score: 32
High score: 85
High score: 91
Skipping low score: 28
High score: 67
```

# Real-World Benefits of continue:
### 1. Data Filtering:

-    Useful for skipping invalid or irrelevant data in a loop.
  
-    E.g., processing user input, filtering valid numbers or strings.
### 2. Optimized Processing:

- Helps in focusing only on required conditions and avoids unnecessary computations.
  
- E.g., skipping unnecessary steps in algorithms.
### 3. Improved Logic Clarity:

- Keeps the loop clean and focused by explicitly skipping unwanted conditions.
###4. Error Handling:

Efficiently skips iterations with errors or exceptions while continuing the loop execution.
---


# Practice Tasks for Loops and Jump Statements

# 1. **For Loop Task**
**Task Name:** Calculate Total Cost of Items in a Cart  
**Description:**  
Write a program that calculates the total cost of items in a shopping cart. Use a `for` loop to iterate through the prices of 5 items and calculate their sum.

**Real-Life Scenario:**  
This simulates the process of calculating the total cost of items in an online shopping cart.

**Instructions:**  
- Use a `for` loop to iterate over the prices of 5 items stored in an array.
- Calculate and display the total cost.

``` java
Your Code Goes Here...
```
---

# 2. **While Loop Task**
**Task Name:** Countdown Timer  
**Description:**  
Create a program that simulates a countdown timer starting from 10. Use a `while` loop to display the countdown.

**Real-Life Scenario:**  
This simulates the timer used in online exams or games.

**Instructions:**  
- Use a `while` loop to display numbers from 10 to 0.
- Print "Time's up!" when the countdown ends.
  
``` java
Your Code Goes Here...
```
---

# 3. **Do-While Loop Task**
**Task Name:** Password Entry Simulation  
**Description:**  
Simulate a system where a user is repeatedly prompted to enter a password until they get it correct.

**Real-Life Scenario:**  
This simulates password validation in login systems.

**Instructions:**  
- Use a `do-while` loop to repeatedly prompt the user for a password.
- Exit the loop once the correct password is entered.

``` java
Your Code Goes Here...
```
---

# 4. **Break Statement Task**
**Task Name:** Exit on High Temperature  
**Description:**  
Write a program to monitor temperatures from a sensor. Use a `break` statement to stop monitoring if the temperature exceeds 40°C.

**Real-Life Scenario:**  
This simulates a system that shuts down operations when a temperature threshold is reached.

**Instructions:**  
- Use a loop to simulate temperature readings.
- Break the loop if the temperature exceeds 40°C.

``` java
Your Code Goes Here...
```
---

## 5. **Continue Statement Task**
**Task Name:** Skip Out-of-Stock Items  
**Description:**  
Create a program to process items in an inventory. Use a `continue` statement to skip items that are out of stock.

**Real-Life Scenario:**  
This simulates inventory management where out-of-stock items are skipped during processing.

**Instructions:**  
- Use a loop to iterate through an inventory list.
- Skip items marked as "Out of Stock" and process only available items.

``` java
Your Code Goes Here...
```

---
