# Java OOPs Concepts
Object-Oriented Programming is a paradigm that provides many concepts, such as inheritance, data binding, polymorphism, etc.

**Simula** is considered the first object-oriented programming language. The programming paradigm where everything is represented as an object is known as a truly object-oriented programming language.

**Smalltalk** is considered the first truly object-oriented programming language.

The popular object-oriented languages are **Java, C#, PHP, Python, C++,** etc.

The main aim of object-oriented programming is to implement real-world entities, for example, object, classes, abstraction, inheritance, polymorphism, etc.

# OOPs (Object-Oriented Programming System)
**Object** means a real-world entity such as a pen, chair, table, computer, watch, etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies software development and maintenance by providing some concepts:

### Object
### Class
### Inheritance
### Polymorphism
### Abstraction
### Encapsulation
Apart from these concepts, there are some other terms which are used in Object-Oriented design:

### Coupling
### Cohesion
### Association
### Aggregation
### Composition

![image](https://github.com/user-attachments/assets/d46d55e4-4269-4d41-9822-a36e5a0bf796)


### Object

![image](https://github.com/user-attachments/assets/083617b6-0730-4b44-8b8e-38064fb0f395)

**Any entity that has state and behavior is known as an object.** For example, a chair, pen, table, keyboard, bike, etc. It can be physical or logical.

**An Object can be defined as an instance of a class.** An object contains an address and takes up some space in memory. Objects can communicate without knowing the details of each other's data or code. The only necessary thing is the type of message accepted and the type of response returned by the objects.

### Example: 
A dog is an object because it has states like color, name, breed, etc. as well as behaviors like wagging the tail, barking, eating, etc.


### Class
Collection of objects is called class. It is a logical entity.

A class can also be defined as a blueprint from which you can create an individual object. Class doesn't consume any space.

# Inheritance
When one object acquires all the properties and behaviors of a parent object, it is known as inheritance. It provides code reusability. It is used to achieve runtime polymorphism.

![image](https://github.com/user-attachments/assets/db3fd3a2-718f-460f-bb98-943525952c5d)


# Polymorphism
If one task is performed in different ways, it is known as polymorphism. For example: to convince the customer differently, to draw something, for example, shape, triangle, rectangle, etc.

In Java, we use method overloading and method overriding to achieve polymorphism.

Another example can be to speak something; for example, **a cat speaks meow, dog barks woof, etc.**

# Abstraction
Hiding internal details and showing functionality is known as abstraction. For example phone call, we don't know the internal processing.

In Java, we use abstract class and interface to achieve abstraction.

![image](https://github.com/user-attachments/assets/17f6185a-e795-48e2-990d-703a8cb2ccbc)

# Encapsulation
Binding (or wrapping) code and data together into a single unit are known as encapsulation. For example, a capsule, it is wrapped with different medicines.

A java class is the example of encapsulation. Java bean is the fully encapsulated class because all the data members are private here.


# Coupling
Coupling refers to the knowledge or information or dependency of another class. It arises when classes are aware of each other. If a class has the details information of another class, there is strong coupling. In Java, we use private, protected, and public modifiers to display the visibility level of a class, method, and field. You can use interfaces for the weaker coupling because there is no concrete implementation.

# Cohesion
Cohesion refers to the level of a component which performs a single well-defined task. A single well-defined task is done by a highly cohesive method. The weakly cohesive method will split the task into separate parts. The java.io package is a highly cohesive package because it has I/O related classes and interface. However, the java.util package is a weakly cohesive package because it has unrelated classes and interfaces.

# Association
Association represents the relationship between the objects. Here, one object can be associated with one object or many objects. There can be four types of association between the objects:

### One to One
### One to Many
### Many to One, and
### Many to Many

Let's understand the relationship with real-time examples. For example, One country can have one prime minister (one to one), and a prime minister can have many ministers (one to many). Also, many MP's can have one prime minister (many to one), and many ministers can have many departments (many to many).

**Association can be undirectional or bidirectional.**

# Aggregation
Aggregation is a way to achieve Association. Aggregation represents the relationship where one object contains other objects as a part of its state. It represents the weak relationship between objects. It is also termed as a has-a relationship in Java. Like, inheritance represents the is-a relationship. It is another way to reuse objects.

# Composition
The composition is also a way to achieve Association. The composition represents the relationship where one object contains other objects as a part of its state. There is a strong relationship between the containing object and the dependent object. It is the state where containing objects do not have an independent existence. If you delete the parent object, all the child objects will be deleted automatically.


# Advantage of OOPs over Procedure-oriented programming language
1) OOPs makes development and maintenance easier, whereas, in a procedure-oriented programming language, it is not easy to manage if code grows as project size increases.

2) OOPs provides data hiding, whereas, in a procedure-oriented programming language, global data can be accessed from anywhere.

![image](https://github.com/user-attachments/assets/318c23f6-8183-4930-951e-49bb3fa988ab)

Figure: Data Representation in Procedure-Oriented Programming

![image](https://github.com/user-attachments/assets/97d1d1f8-adc3-4282-a1d5-2aa815952caf)

Figure: Data Representation in Object-Oriented Programming

3) OOPs provides the ability to simulate real-world event much more effectively. We can provide the solution of real word problem if we are using the Object-Oriented Programming language.

---
# Java Naming Convention

Java naming convention is a rule to follow as you decide what to name your identifiers such as class, package, variable, constant, method, etc.

But, it is not forced to follow. So, it is known as convention not rule. These conventions are suggested by several Java communities such as Sun Microsystems and Netscape.

All the classes, interfaces, packages, methods and fields of Java programming language are given according to the Java naming convention. If you fail to follow these conventions, it may generate confusion or erroneous code.

### Advantage of Naming Conventions in Java
By using standard Java naming conventions, you make your code easier to read for yourself and other programmers. Readability of Java program is very important. It indicates that less time is spent to figure out what the code does.

### Naming Conventions of the Different Identifiers
The following table shows the popular conventions used for the different identifiers.

![image](https://github.com/user-attachments/assets/72c59804-df0b-4eb5-8bb1-58c3d70f2d30)


![image](https://github.com/user-attachments/assets/0a2715f3-0d50-4872-a16a-7cfd9a6815ad)

![image](https://github.com/user-attachments/assets/8a077c48-f7c2-431a-9af7-b2497c0059fd)


![image](https://github.com/user-attachments/assets/4b9293b1-6615-456c-b949-81437c73b2c2)

CamelCase in Java naming conventions
Java follows camel-case syntax for naming the class, interface, method, and variable.

If the name is combined with two words, the second word will start with uppercase letter always such as actionPerformed(), firstName, ActionEvent, ActionListener, etc.

---



















