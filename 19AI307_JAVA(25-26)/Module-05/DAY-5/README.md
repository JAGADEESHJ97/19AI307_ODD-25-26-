# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

For example:

Input:
5
10

Result:
a = 10
b = 5

## AIM:

To write a Java program to swap two integer values using a synchronized block to ensure thread-safe operation.

## ALGORITHM :

1. Start the program.
2. Read two integer values `a` and `b` from the user.
3. Create a shared object for synchronization.
4. Use a synchronized block on the shared object.
5. Inside the block, swap the values of `a` and `b`.
6. Print the swapped values.
7. Stop the program.

## PROGRAM:

Program to implement Synchronization concept using Java

## SOURCE CODE:

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        final Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);

        sc.close();
    }
}
```

## OUTPUT:

<img width="304" height="256" alt="image" src="https://github.com/user-attachments/assets/ec6aa514-e533-452d-9fc0-3d8780400816" />


## RESULT:

The Java program successfully demonstrates the use of a synchronized block to safely swap two integer values and display the swapped output.
