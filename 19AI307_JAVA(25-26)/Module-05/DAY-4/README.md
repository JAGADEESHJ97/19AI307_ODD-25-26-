# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a Java program to determine the priority and name of the current thread.

## AIM:

To write a Java program to determine and display the name and priority of the current thread.

## ALGORITHM :

1. Start the program.
2. Import the required class `Scanner`.
3. Read the thread name from the user.
4. Get the current thread using `Thread.currentThread()`.
5. Set the thread name using `setName()`.
6. Retrieve and display the thread priority using `getPriority()`.
7. Retrieve and display the thread name using `getName()`.
8. Print the thread object details.
9. Stop the program.

## PROGRAM:

Program to implement Thread Priority Concept using Java

## SOURCE CODE:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();
        t.setName(threadName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}
```

## OUTPUT:

<img width="564" height="178" alt="image" src="https://github.com/user-attachments/assets/4841a7dd-15c0-47c1-a1ae-e34e92922105" />


## RESULT:

The Java program successfully determines and displays the current thread's name and priority using the `Thread` class.
