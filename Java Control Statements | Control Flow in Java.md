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

If the score is 90 or above, print "A".
If the score is 80 to 89, print "B".
If the score is 70 to 79, print "C".
If the score is below 70, print "Fail".
**Hint:**
Use multiple if-else-if conditions.

```java
Your Code Goes Here...
```

### 4. Switch Statement Practice Task
**Task 4:**
Write a program that prints the type of vehicle based on its number:

1: "Car", 2: "Bike", 3: "Truck", 4: "Bus".
If the number is not between 1 and 4, print "Invalid vehicle type".
**Hint:**
Use a switch statement to map numbers to vehicle types.

```java
Your Code Goes Here...
```
