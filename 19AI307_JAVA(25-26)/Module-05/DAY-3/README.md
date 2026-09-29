# Ex.No:5(C) FILE HANDLING USING JAVA

## QUESTION:

Write a program to overwrite the content of a file.

## AIM:

To write a Java program to overwrite the content of a file using FileWriter.

## ALGORITHM :

1. Start the program.
2. Import the required classes `FileWriter` and `Scanner`.
3. Take input content from the user.
4. Create a `FileWriter` object for the file `output.txt`.
5. Write the input content into the file in overwrite mode.
6. Close the file writer.
7. Display the success message.
8. Stop the program.

## PROGRAM:

Program to implement File Handling using Java


## SOURCE CODE:

```java
import java.io.FileWriter;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String content = sc.nextLine();

        try {
            // Overwrite mode (default behavior)
            FileWriter fw = new FileWriter("output.txt");

            fw.write(content);
            fw.close();

            System.out.println("File content overwritten successfully.");

        } catch (Exception e) {
            System.out.println("Error occurred while writing file.");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="894" height="173" alt="image" src="https://github.com/user-attachments/assets/08ccb734-6d6a-4b49-9109-1d6bba85983a" />


## RESULT:

The program successfully overwrites the existing content of a file named `output.txt` with new user-provided data using FileWriter.
