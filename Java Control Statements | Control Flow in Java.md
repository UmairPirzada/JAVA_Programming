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

### 1) If Statement:
In Java, the "if" statement is used to evaluate a condition. The control of the program is diverted depending upon the specific condition. The condition of the If statement gives a Boolean value, either true or false. In Java, there are four types of if-statements given below:

- Simple if statement
- if-else statement
- if-else-if ladder
- Nested if-statement

Let's understand the `if` statements one by one.

#### 1) Simple if statement:
It is the most basic statement among all control flow statements in Java. It evaluates a Boolean expression and enables the program to enter a block of code if the expression evaluates to true.

**Real-life Example**:  
Imagine you are in a shopping mall and you have a discount card. The system checks if the card is valid. If it is, the discount is applied; if not, you pay the full price. 

**Syntax of if statement**:

```java
if(condition) {    
    statement 1; // executes when condition is true   
}
```
