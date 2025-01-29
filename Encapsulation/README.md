# **Encapsulation**
- **Encapsulation** is the practice of keeping fields (variables) private and providing public methods (`getters` and `setters`) to access and modify them.
- It protects the data from unwanted changes and ensures it’s accessed in a controlled way.

### **How to Implement Encapsulation**

**Steps to Implement Encapsulation:**

1. **Make Fields/Variables Private**: The fields (data) of a class should be private so that they cannot be accessed directly from outside the class.
   
2. **Provide Public Getter and Setter Methods**: These methods allow controlled access to the fields. A getter method is used to retrieve the value of a field, while a setter method is used to set or modify the value of a field.

**Example:**
```java
class Person {
    // Private fields
    private String name;
    private int age;

    // Getter method for name
    public String getName() {
        return name;
    }

    // Setter method for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter method for age
    public int getAge() {
        return age;
    }

    // Setter method for age
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("Alice");
        person.setAge(25);

        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());
    }
}
```
In this example:
- The fields `name` and `age` are private, so they cannot be accessed directly from outside the `Person` class.
- The getter and setter methods provide controlled access to these fields. The setter for `age` also includes a validation to ensure that the age is positive.

**Key Points of Encapsulation:**
- The internal state of the object is protected from unauthorized access and modification.
- The object’s data can be manipulated only through defined methods (setters and getters).
- It hides the implementation details from the outside world, only exposing what’s necessary.

   

---

### **How Encapsulation is Different from Abstraction**

- **Encapsulation** is focused on **data hiding** and protecting the internal state of objects by using private fields and public methods (getters/setters). It prevents unauthorized access to the object's data and ensures that the data can be accessed and modified in a controlled way.
  
- **Abstraction** is focused on **hiding the implementation details** and exposing only essential functionality to the user. Abstraction allows you to define a common interface or abstract class for all the objects that follow the same behavior, without worrying about how that behavior is implemented.

### Example of **Abstraction** vs **Encapsulation**:

```java
// Abstraction: Define the interface (What a class can do)
interface Animal {
    void makeSound();  // Abstract method (no implementation)
}

// Encapsulation: Controlling access to data
class Dog implements Animal {
    // Encapsulation: Private fields
    private String name;
    private int age;
    
    // Constructor
    public Dog(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    // Encapsulation: Getter method for name
    public String getName() {
        return name;
    }

    // Encapsulation: Setter method for name
    public void setName(String name) {
        this.name = name;
    }

    // Encapsulation: Getter method for age
    public int getAge() {
        return age;
    }

    // Encapsulation: Setter method for age
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        } else {
            System.out.println("Invalid age");
        }
    }

    // Abstraction: Implementation of makeSound() method
    @Override
    public void makeSound() {
        System.out.println("Woof");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog("Buddy", 3);
        
        // Encapsulation: Accessing data through getters
        System.out.println("Dog's name: " + myDog.getName());   // Outputs: Buddy
        System.out.println("Dog's age: " + myDog.getAge());     // Outputs: 3
        
        // Encapsulation: Modifying data through setters
        myDog.setName("Max");
        myDog.setAge(4);
        
        System.out.println("Updated name: " + myDog.getName());  // Outputs: Max
        System.out.println("Updated age: " + myDog.getAge());    // Outputs: 4
        
        // Abstraction: Calling a method that hides the implementation
        myDog.makeSound();  // Outputs: Woof
    }
}
```

### Key Differences:

| **Aspect**               | **Encapsulation**                             | **Abstraction**                            |
|--------------------------|-----------------------------------------------|--------------------------------------------|
| **Definition**            | Hiding the internal state and protecting data through private fields and public methods (getters and setters). | Hiding complex implementation details and exposing only necessary features via abstract classes or interfaces. |
| **Focus**                 | Protecting the data and controlling how it’s accessed and modified. | Hiding the implementation details and exposing only essential functionality. |
| **Goal**                  | Restrict access to the internal state of an object and enforce valid data through methods. | Simplify interaction with the system by providing a clear and simple interface. |
| **Usage**                 | Used to restrict direct access to fields and ensure controlled access and validation. | Used to define a general behavior or contract for a class, while leaving out details of the implementation. |
| **Example**               | Getters and setters in a class to access and modify data. | Abstract classes or interfaces defining behavior that can be implemented by multiple classes. |

---

### Summary:
- **Encapsulation** is about **protecting the data** by keeping it private and providing public methods to access and modify it in a controlled manner.
- **Abstraction** is about **hiding the complexity** of an implementation and exposing only what is necessary (usually through interfaces or abstract classes).

These two concepts work together: Encapsulation hides the internal details of the object, while Abstraction hides the implementation details, letting the user focus on the higher-level functionality.