# Ex.No:4(C) COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books cannot exist independently (Composition).

## AIM:

To implement a Composition relationship in Java where a Library contains multiple Book objects, and each Book is created inside the Library, meaning Books cannot exist independently.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Create a `Library` object.
- Read the number of books `n` from the user.
- Read the title and author of each book.
- Create `Book` objects inside the `Library` using the `addBook()` method.
- Add each Book object to the Library's list.
- Display all the books contained in the Library.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement Composition Concept in Java


## SOURCE CODE:

```java
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {

            String title = sc.nextLine();
            String author = sc.nextLine();

            library.addBook(title, author);
        }

        library.showBooks();

        sc.close();
    }
}

class Book {

    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {

    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {

        Book book = new Book(title, author);

        books.add(book);
    }

    public void showBooks() {

        System.out.println("Books in Library:");

        for (Book book : books) {
            System.out.println("- " + book.getDetails());
        }
    }
}
```

# OUTPUT:

<img width="746" height="414" alt="image" src="https://github.com/user-attachments/assets/6d4872e3-b130-4f9d-b058-8446bd4b6072" />



# RESULT:
Thus the program to implement the composition was executed successfully.
