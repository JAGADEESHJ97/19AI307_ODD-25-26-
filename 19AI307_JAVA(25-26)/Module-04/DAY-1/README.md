# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:

To write a Java program that performs integer division on two user-inputted numbers and handles potential division-by-zero errors using a try-catch block.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Create a Scanner object to receive user inputs.
- Read two integer values from the user and store them in variables `num1` and `num2`.
- Open a `try` block to perform the division operation safely.
- Divide `num1` by `num2` and display the result.
- If the second number is zero, an `ArithmeticException` occurs.
- Catch the `ArithmeticException` using a `catch` block.
- Display an appropriate error message for division by zero.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement Exception Handling using Java


## SOURCE CODE:

```java
import java.util.*;

public class DivisionProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();

        try {
            int result = num1 / num2;
            System.out.println("Result: " + result);
        }
        catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }

        scanner.close();
    }
}
```

# OUTPUT:

<img width="651" height="277" alt="image" src="https://github.com/user-attachments/assets/929b5874-219b-4b7b-9dd7-1fa2b6a76f21" />


# RESULT:
Thus the java program to implement the exception handling was executed successfully.
