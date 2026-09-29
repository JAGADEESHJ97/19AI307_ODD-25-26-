# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

## AIM:

To implement the Factory Design Pattern in Java to create and draw different shapes like Circle, Square, and Rectangle based on user input.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define a `Shape` interface with a `draw()` method.
- Create concrete classes `Circle`, `Square`, and `Rectangle` that implement the `Shape` interface.
- Define a `ShapeFactory` class to create the required shape object based on the shape name.
- Create a `ShapeFactory` object in the `main()` method.
- Read the shape name from the user in a loop.
- If the input is `"exit"`, stop the program.
- Pass the input to the `ShapeFactory` to create the required shape object.
- If the shape is valid, call the `draw()` method.
- If the shape is invalid, display an error message.
- Repeat the process until `"exit"` is entered.
- Close the Scanner object.
- Stop the program.

## PROGRAM:


## SOURCE CODE:

```java
import java.util.*;

interface Shape {
    void draw();
}

class Circle implements Shape {

    public void draw() {
        System.out.println("Drawing Circle");
    }
}

class Square implements Shape {

    public void draw() {
        System.out.println("Drawing Square");
    }
}

class Rectangle implements Shape {

    public void draw() {
        System.out.println("Drawing Rectangle");
    }
}

class ShapeFactory {

    public Shape getShape(String shapeType) {

        if (shapeType.equalsIgnoreCase("circle")) {
            return new Circle();
        }
        else if (shapeType.equalsIgnoreCase("square")) {
            return new Square();
        }
        else if (shapeType.equalsIgnoreCase("rectangle")) {
            return new Rectangle();
        }

        return null;
    }
}

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        ShapeFactory factory = new ShapeFactory();

        while (true) {

            String input = sc.nextLine();

            if (input.equalsIgnoreCase("exit")) {
                break;
            }

            Shape shape = factory.getShape(input);

            if (shape != null) {
                shape.draw();
            }
            else {
                System.out.println("Invalid shape: " + input);
            }
        }

        sc.close();
    }
}
```

# OUTPUT:

<img width="509" height="374" alt="image" src="https://github.com/user-attachments/assets/bb1809c8-6dfc-426b-a598-1b1be9518058" />


# RESULT:
Thus, the program to implement the Factory Design Pattern for creating and drawing different shapes (Circle, Square, Rectangle) based on user input was successfully executed and the output was obtained.
