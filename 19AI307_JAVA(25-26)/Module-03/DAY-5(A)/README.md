# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to create an inner class and access it from the outer class.

## AIM:

To demonstrate accessing an inner class from an outer class in Java.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define an outer class `OuterClass` with a variable `name`.
- Create a constructor to initialize the `name` variable.
- Define a method `display()` inside the outer class.
- Inside the `display()` method, create an object of the inner class.
- Define an inner class `InnerClass` inside the outer class.
- Create a method `showMessage()` in the inner class to display a message.
- In the `main()` method, create a Scanner object and read the name from the user.
- Create an object of the outer class using the input name.
- Call the `display()` method of the outer class.
- The `display()` method creates and accesses the inner class object.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement an Inner Class using Java

## SOURCE CODE:

```java
import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String input = scanner.next();

        OuterClass outer = new OuterClass(input);
        outer.display();

        scanner.close();
    }
}
```


# OUTPUT:

<img width="1223" height="347" alt="image" src="https://github.com/user-attachments/assets/f9f8504c-9647-4b4a-80c7-56827511d538" />


# RESULT:
The program successfully accesses and prints data from the inner class using the outer class.
