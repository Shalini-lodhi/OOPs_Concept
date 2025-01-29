# **Abstraction**
- **Abstraction** means hiding complex implementation details and showing only the necessary features.
- It’s typically achieved using **abstract classes** and **interfaces**.
  - An **abstract class** cannot be instantiated directly and may have abstract methods (methods without a body).
  - An **interface** is a contract that any class can implement, and it defines a set of methods without implementation.

**Example (Abstract Class):**
```java
abstract class Animal {
    abstract void sound();  // Abstract method (no implementation)

    void breathe() {
        System.out.println("Breathing...");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        dog.sound();  // Outputs: Bark
        dog.breathe();  // Outputs: Breathing...
    }
}
```

**Example (Interface):**
```java
interface Playable {
    void play();  // Interface method
}

class Dog implements Playable {
    public void play() {
        System.out.println("Dog is playing");
    }
}

public class Main {
    public static void main(String[] args) {
        Playable dog = new Dog();
        dog.play();  // Outputs: Dog is playing
    }
}
```
## Abstract Class V/S Interface
- **Abstract Class**: Use it when you have a base class with some shared implementation, but want to leave certain methods for subclasses to implement.
- **Interface**: Use it when you want to define a common set of behaviors across unrelated classes, allowing flexibility for multiple inheritance of behaviors.
  
### Comparison Table:

| **Aspect**              | **Abstract Class**                            | **Interface**                            |
|-------------------------|-----------------------------------------------|------------------------------------------|
| **Methods**             | Can have both abstract and concrete methods   | All methods are abstract (unless default methods) |
| **Fields**              | Can have instance variables                   | Cannot have instance variables (only constants) |
| **Constructor**         | Can have constructors                         | Cannot have constructors                |
| **Multiple Inheritance**| No (Single inheritance)                       | Yes (Multiple interfaces can be implemented) |
| **Access Modifiers**    | Can use any access modifier (`private`, `protected`, `public`) | Methods are implicitly `public`; fields are `public static final` |
| **Usage**               | Used when classes share common functionality  | Used to define common behaviors for unrelated classes |
