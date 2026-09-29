# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:

To convert string inputs into integers using the wrapper class and perform addition.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Create a Scanner object to read input from the user.
- Read two string values from the user.
- Convert the first string into an integer using the `Integer.parseInt()` wrapper class method.
- Convert the second string into an integer using the `Integer.parseInt()` wrapper class method.
- Add the two integers.
- Display the sum.
- Handle invalid input using `NumberFormatException`.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement a Wrapper Class using Java


## SOURCE CODE:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.next();
        String str2 = scanner.next();

        scanner.close();

        try {
            int num1 = Integer.parseInt(str1);
            int num2 = Integer.parseInt(str2);

            int sum = num1 + num2;

            System.out.println("Sum = " + sum);
        }
        catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid number.");
        }
    }
}
```

# OUTPUT:

<img width="1223" height="414" alt="image" src="https://github.com/user-attachments/assets/0f889258-1b45-42eb-a071-83d3535c6bf5" />


# RESULT:
The program successfully converts strings to integers and displays their sum.
