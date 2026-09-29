# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class Employee with method `display()`. Inside `display()`, return the current object using `this`. Create another method that calls `display().printName()`.

## AIM:

To create an Employee class where the `display()` method returns the current object using `this`, and demonstrate calling `display().printName()` from another method.

## ALGORITHM :

- Start the program.
- Create a class `Employee` with a variable `name`.
- Write a method `setName()` to assign a value to `name`.
- Write a method `display()` that returns the current object using `return this`.
- Write a method `printName()` to print the employee name.
- In the `main()` method, create a Scanner object to read the employee name from the user.
- Create an `Employee` object.
- Set the employee name using the `setName()` method.
- Call `display().printName()` to return the current object and print the employee name.
- Stop the program.

## PROGRAM:

Program to implement Access Modifiers using Java

## SOURCE CODE:

```java
import java.util.Scanner;

class Employee {
    String name;

    void setName(String name) {
        this.name = name;
    }

    Employee display() {
        return this;
    }

    void printName() {
        System.out.println("Employee Name: " + name);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        String inputName = scanner.nextLine();

        Employee emp = new Employee();
        emp.setName(inputName);
        emp.display().printName();
    }
}
```

# OUTPUT: 
<img width="686" height="326" alt="image" src="https://github.com/user-attachments/assets/a1a5d597-c19c-4b67-8711-a34a357129a6" />


# RESULT:
Therefore the program successfully returns the current object using this inside the display() method.
