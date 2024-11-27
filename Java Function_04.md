# Java Function
Java is one of the most popular programming languages in the world, and one of its key features is its ability to define and use functions. Functions in Java are blocks of code that perform a specific task, and they are used to organize code and make it more modular and reusable. In this article, we will explore the basics of Java functions, including how to define them, how to pass parameters, and how to return values.

## Defining a Java Function
In order to define a function in Java, you use the keyword "public" (or "private" or "protected") followed by the return type of the function, then the name of the function, and finally a set of parentheses containing any parameters the function may take. For example, here is a simple function that takes no parameters and returns nothing

```java
public void sayHello() {  
  System.out.println("Hello, world!");  
}
```
In this case, the function is called "sayHello", it takes no parameters (i.e., the parentheses are empty), and it returns nothing (i.e., the return type is "void"). To call this function from another part of your code, you simply write its name followed by a set of parentheses, like this:

```java
sayHello();
```
## Passing Parameters to a Java Function
Functions can also take one or more parameters, which are passed in as values when the function is called. To define a function that takes one or more parameters, you simply list them inside the parentheses when you define the function. Here's an example of a function that takes two parameters (both of type "int") and returns their sum:

```java
public int add(int a, int b) {  
  return a + b;  
}
```

In this case, the function is called "add", it takes two parameters (both of type "int"), and it returns their sum (also of type "int"). To call this function and pass in two values, you would write:/p>

```java
int result = add(5, 7);
```
In this case, the values 5 and 7 are passed in as the values of the "a" and "b" parameters, respectively, and the result of the function (12) is assigned to the "result" variable.

## Returning Values from a Java Function
Functions in Java can also return a value, which is specified by the return type of the function. To define a function that returns a value, you simply specify the return type (which can be any data type, including objects) before the function name, like this:

```java
public int doubleValue(int a) {  
  return a * 2;  
}
```
In this case, the function is called "doubleValue", it takes one parameter (an integer), and it returns twice the value of that parameter. To call this function and get the result, you would write:

```java
int result = doubleValue(5);
```

In this case, the value 5 is passed in as the value of the "a" parameter, and the result of the function (10) is assigned to the "result" variable.

Functions are an important part of any programming language, and Java is no exception. With Java functions, you can organize your code into modular, reusable blocks, and pass in values and return results as needed. By mastering the basics of Java functions, you will be well on your way to becoming a skilled Java programmer. Functions in Java are also commonly known as methods, and they play a key role in structuring and organizing code. By encapsulating blocks of code into functions, you can create reusable and modular code that can be called from other parts of the program.

Java functions can take zero or more parameters as input, and they can return a value or perform an action without returning a value. The return type of a function is specified by placing the data type of the return value before the name of the function.

Here's an example Java program with input and output that demonstrates Java functions:

**FunctionExample.java**
```java
import java.util.Scanner;  
public class FunctionExample {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
          
        System.out.print("Enter a number: ");  
        int num1 = scanner.nextInt();  
          
        System.out.print("Enter another number: ");  
        int num2 = scanner.nextInt();  
        int sum = add(num1, num2);  
        System.out.println("The sum of " + num1 + " and " + num2 + " is " + sum + ".");
 public static int add(int a, int b) {  
        return a + b;  
    }  
}
```

### Output:
```text
Enter a number: 5
Enter another number: 7
The sum of 5 and 7 is 12.

```
In this program, the user is prompted to enter two numbers, which are then passed to the add function. The function calculates their sum and returns it, which is then printed to the console along with a message that includes the original numbers.



# Practice Tasks:
### 1. Say Hello
Write a function called sayHello that prints "Hello, [Your Name]!" where [Your Name] is passed as a parameter to the function.

```java
Your Code Goes Here...
```

### 2. Calculate Product
Write a function called multiply that takes two integers as parameters and returns their product.

```java
Your Code Goes Here...
```

### 3. Find Maximum
Write a function called findMax that takes two integers as parameters and returns the larger of the two.

```java
Your Code Goes Here...
```
### 4. Square a Number
Write a function called square that takes an integer as a parameter and returns its square.

```java
Your Code Goes Here...
```

### 5. Temperature Converter
Write a function called celsiusToFahrenheit that takes a temperature in Celsius as a parameter and returns its equivalent in Fahrenheit. Use the formula:

![image](https://github.com/user-attachments/assets/7c931a16-d4c4-4b85-a307-4341a463643a)


```java
Your Code Goes Here...
```


These examples demonstrate defining, using, and returning values from functions in Java.

---
