# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a class that uses a constructor to initialize variables and overrides `toString()` method.

## AIM:

To write a Java program that initializes object variables using a constructor and overrides the `toString()` method to display object details in a readable format.

## ALGORITHM :

- Start the program.
- Define a class `Student` with two instance variables:
  - `String name`
  - `int age`
- Create a parameterized constructor to initialize these variables.
- Override the `toString()` method to return the student details in a formatted string.
- In the `main()` method, create a Scanner object to read input from the user.
- Read the name and age from the user.
- Create a `Student` object using the parameterized constructor.
- Print the object using the `toString()` method.
- Stop the program.

## PROGRAM:

Program to implement Variable Scope and Constructor using Java

## SOURCE CODE:

```java
import java.util.Scanner;

class Student {
    String name;
    int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class StudentDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String name = scanner.nextLine();
        int age = scanner.nextInt();

        Student student = new Student(name, age);

        System.out.println(student.toString());
    }
}
```
# OUTPUT:
<img width="896" height="395" alt="image" src="https://github.com/user-attachments/assets/91edbe4d-166a-406b-aa87-00db9d6f27b8" />

# RESULT:
Therefore the program successfully creates a student object using the constructor.
