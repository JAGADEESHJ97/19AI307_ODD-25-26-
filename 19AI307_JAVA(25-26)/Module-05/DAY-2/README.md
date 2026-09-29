# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:

Write a Java program to serialize a collection of objects (like ArrayList) into a file.

## AIM:

To write a Java program to serialize a collection of objects (ArrayList of Student) into a file and then deserialize the objects back from the file.

## ALGORITHM :

1. Start the program.
2. Create a `Student` class that implements `Serializable`.
3. Create an `ArrayList` to store Student objects.
4. Read the number of students from the user.
5. Input student details such as ID, name, and marks and store them in the list.
6. Serialize the list using `ObjectOutputStream` into a file named `students.dat`.
7. Deserialize the list using `ObjectInputStream`.
8. Display the deserialized student objects.
9. Stop the program.

## PROGRAM:

Program to implement Serialization and Deserialization using Java

## SOURCE CODE:

```java
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos =
                     new ObjectOutputStream(new FileOutputStream(fileName))) {

            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);

        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;

        try (ObjectInputStream ois =
                     new ObjectInputStream(new FileInputStream(fileName))) {

            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);

        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }

        return students;
    }

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();

        for (int i = 0; i < n; i++) {

            int id = scanner.nextInt();
            String name = scanner.next();
            double marks = scanner.nextDouble();

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents =
                deserializeStudents(fileName);

        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");

            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

## OUTPUT:


<img width="941" height="352" alt="image" src="https://github.com/user-attachments/assets/754ad76a-55ad-4dca-9a9e-63f0156a86e9" />


## RESULT:

The Java program successfully serializes an ArrayList of Student objects into a file named `students.dat` and then deserializes the objects back, displaying the stored student details.
