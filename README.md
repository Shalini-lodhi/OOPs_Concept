# Object Oriented Programming

OOPs a programming paradigm based on the concept of “objects” which are instances of classes. 
`OOP helps in organizing software design around data (objects) and methods (functions) rather than logic.`


### 1. **Class and Object**
- **Class**: A blueprint for creating objects. It defines properties (fields) and methods (functions) that the objects will have.
- **Object**: An instance of a class. It holds the actual values of the properties defined in the class.

**Example:**
```java
// Define a class named Car
class Car {
    // Fields (Properties)
    String model;
    int year;

    // Method (Behavior)
    void start() {
        System.out.println("The car is starting.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating an object of the Car class
        Car myCar = new Car(); 
        myCar.model = "Toyota";
        myCar.year = 2020;
        myCar.start();  // Calls the method from the Car class
    }
}
```
---
### Summary:
- **Class**: Blueprint for creating objects.
- **Object**: Instance of a class.
- **Encapsulation**: Hiding data and providing controlled access.
- **Inheritance**: Reusing functionality from another class.
- **Polymorphism**: One method behaving differently based on context (overloading/overriding).
- **Abstraction**: Hiding complexity and exposing only necessary parts.
---
### Q/A
**1. What is OOP?**
  
OOP (Object-Oriented Programming) is a programming paradigm based on the concept of **objects**, which can contain **data** (attributes) and **methods** (functions). It aims to model real-world entities and behaviors in software design, promoting **reusability**, **modularity**, and **maintainability**.

**2. What are the four pillars of OOP?**
  
The four pillars of OOP are:
1. **Encapsulation** – Hiding the internal state and requiring all interaction to be done through methods.
2. **Abstraction** – Hiding complex implementation details and exposing only essential features.
3. **Inheritance** – Deriving new classes from existing ones to promote code reuse.
4. **Polymorphism** – The ability of a method to take multiple forms based on the object type.

**3. What is the difference between an abstract class and an interface?**
 
- **Abstract Class**: Can have both abstract (unimplemented) and concrete (implemented) methods. It can also have instance variables.
- **Interface**: Only contains abstract methods (prior to Java 8) and constants. Since Java 8, it can have default and static methods but cannot have instance variables.

**4. What is the difference between method overloading and method overriding?**
 
- **Method Overloading**: Same method name but different parameters (compile-time polymorphism).
- **Method Overriding**: Same method signature in both parent and child class, but the child class provides its own implementation (runtime polymorphism).

**5. What is encapsulation?**
  
Encapsulation is the concept of **bundling** the data (attributes) and the methods that operate on the data within a single unit (class). It also involves **restricting access** to the internal state by making fields private and providing access through public getter and setter methods.

**6. What is inheritance in OOP?**
  
Inheritance allows one class (child class) to inherit the properties and behaviors (methods) from another class (parent class), enabling code reuse and establishing an **is-a relationship**.

**7. What is polymorphism in OOP?**
  
Polymorphism allows objects of different classes to be treated as objects of a common superclass. It allows a single method to behave differently based on the object type, typically through **method overriding** (runtime polymorphism) or **method overloading** (compile-time polymorphism).

**8. What is the difference between "this" and "super" in Java?**
  
- **this**: Refers to the current instance of the class.
- **super**: Refers to the superclass (parent class) of the current object and can be used to access parent class methods or constructors.

**9. What is the purpose of the `final` keyword in Java?**
 
- **final variable**: A constant whose value cannot be changed.
- **final method**: A method that cannot be overridden by subclasses.
- **final class**: A class that cannot be inherited.

**10. What is the difference between a constructor and a method?**
 
- **Constructor**: A special method used to initialize objects when they are created. It has the same name as the class and no return type.
- **Method**: A block of code that performs a specific task and can return a value.

**11. What are access modifiers in Java?**
  
Access modifiers control the visibility of classes, methods, and variables:
- **public**: Accessible from any other class.
- **private**: Accessible only within the class.
- **protected**: Accessible within the same package or subclasses.
- **default** (no modifier): Accessible only within the same package.

**12. What is the use of the `super()` keyword?**
  
`super()` is used to call the **parent class constructor**. It can be called implicitly or explicitly in the child class constructor to invoke the parent class's constructor.

**13. What is the significance of the `instanceof` operator in Java?**
  
The `instanceof` operator is used to check whether an object is an instance of a specific class or implements an interface. It returns `true` or `false`.

**14. What is method overriding?**
  
Method overriding occurs when a subclass provides a **specific implementation** for a method that is already defined in its parent class. The method signature in the subclass must be the same as the one in the parent class.

**15. What is the difference between "==" and `.equals()` in Java?**
 
- **"=="**: Compares **references** (memory addresses) to check if two objects refer to the same memory location.
- **`.equals()`**: Compares the **contents** of objects to check if they are logically equivalent.

**16. What is an interface?**
  
An interface in Java is a **contract** that defines a set of abstract methods that a class must implement. It allows for multiple inheritance through classes implementing multiple interfaces.

**17. What is a static method in Java?**
  
A **static method** belongs to the class rather than an instance of the class. It can be called without creating an object of the class. Static methods cannot access instance variables or instance methods.

**18. What is the significance of `abstract` class?**
  
An **abstract class** is a class that cannot be instantiated and is meant to be subclassed. It can contain abstract methods (methods without implementation) and concrete methods (with implementation).

**19. Can we instantiate an abstract class?**
  
No, you **cannot instantiate** an abstract class directly. However, you can create an object of a concrete subclass that implements or overrides the abstract methods.

**20. What is a `constructor` in Java?**
  
A constructor is a special method in Java used to initialize new objects. It has the same name as the class and does not have a return type.

**21. What is the difference between `ArrayList` and `LinkedList`?**
  
- **ArrayList**: Implements a **dynamic array**, provides fast access (index-based) but slower insertion/removal (except at the end).
- **LinkedList**: Implements a **doubly linked list**, provides faster insertion/removal but slower access (linear time).

**22. What is the significance of the `transient` keyword in Java?**
  
The `transient` keyword in Java is used to indicate that a field should not be serialized. When an object is serialized, transient fields are ignored.

**23. What are the differences between `String`, `StringBuilder`, and `StringBuffer`?**
 
- **String**: Immutable, meaning once created, the value cannot be changed.
- **StringBuilder**: Mutable and optimized for **single-threaded** use.
- **StringBuffer**: Mutable and synchronized, suitable for **multi-threaded** environments.

**24. What is an anonymous class?**
  
An anonymous class is a **class without a name**, often used for instantiating objects of a class that extends a class or implements an interface on the fly, especially in GUI or event-driven programming.

**25. What is the purpose of `finally` block in exception handling?**
  
The `finally` block is always executed after the `try` block, regardless of whether an exception is thrown or not. It is used to ensure that resources (like file streams or database connections) are properly closed.