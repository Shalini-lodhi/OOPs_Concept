# **Inheritance**
- **Inheritance** allows one class (child class) to inherit the properties and methods of another class (parent class).
- This promotes code reusability and makes the system hierarchical.

**Example:**
```java
// Parent class
class Animal {
    void sound() {
        System.out.println("Some animal sound");
    }
}

// Child class that inherits from Animal
class Dog extends Animal {
    // The Dog class can use the sound() method from Animal
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();  // Dog object but reference is of Animal type
        myDog.sound();  // Outputs: Bark (method overridden)
    }
}
```
