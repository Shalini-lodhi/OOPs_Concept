# **Polymorphism**
- **Polymorphism** allows an object to take many forms. It’s mainly achieved through method overriding and method overloading.
  - **Method Overriding**: A child class provides its own version of a method already defined in the parent class.
  - **Method Overloading**: Multiple methods with the same name but different parameters in the same class.

**Example (Method Overriding):**
```java
class Animal {
    void sound() {
        System.out.println("Some sound");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Meow");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myCat = new Cat();
        myCat.sound();  // Outputs: Meow (method overridden in Cat)
    }
}
```

**Example (Method Overloading):**
```java
class Calculator {
    // Overloaded methods for adding numbers
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println(calc.add(5, 10));    // Outputs: 15
        System.out.println(calc.add(5.5, 10.5));  // Outputs: 16.0
    }
}
```