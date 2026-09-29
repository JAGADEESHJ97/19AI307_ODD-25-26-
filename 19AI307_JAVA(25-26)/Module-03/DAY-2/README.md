# Ex.No:3(B) POLYMORPHISM

## QUESTION:

Write a Java program demonstrating method overriding. Create a class `Animal` with a method `sound()`. Subclass it as `Dog`, `Cat`, and `Cow`, with each overriding the `sound()` method.

## AIM:

To write a Java program that demonstrates method overriding using inheritance and polymorphism.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define a base class `Animal` with a method `sound()`.
- Create subclasses `Dog`, `Cat`, and `Cow` that inherit from the `Animal` class.
- Override the `sound()` method in each subclass to display the respective animal sound.
- In the `main()` method, create an `Animal` reference.
- Assign different subclass objects to the `Animal` reference based on the input.
- Call the `sound()` method using the `Animal` reference.
- Demonstrate runtime polymorphism through method overriding.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement Polymorphism using Java

## SOURCE CODE:

```java
import java.util.Scanner;

class Animal {
    void sound() {
        System.out.println("Unknown animal");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    @Override
    void sound() {
        System.out.println("Cow moos");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();

            if (input.isEmpty())
                continue;

            Animal a;

            switch(input.toLowerCase()) {
                case "dog":
                    a = new Dog();
                    break;

                case "cat":
                    a = new Cat();
                    break;

                case "cow":
                    a = new Cow();
                    break;

                default:
                    a = new Animal();
            }

            a.sound();
        }

        sc.close();
    }
}
```

# OUTPUT:

<img width="1215" height="500" alt="image" src="https://github.com/user-attachments/assets/f2b55ef6-461b-4921-a78d-742b160686cd" />


# RESULT:
The program successfully demonstrates method overriding, showing different behaviors of the sound() method for different animal subclasses.
