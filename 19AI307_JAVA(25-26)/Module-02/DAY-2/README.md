# Ex.No:2(B) METHODS

## QUESTION:

Write a method `int cube(int x)` that calls a method `int square(int x)` internally to calculate the cube as `x * square(x)`.

## AIM:

To write a Java program that defines a method `cube(int x)` which internally calls the method `square(int x)` to compute the cube of a number.

## ALGORITHM :

- Start the program.
- Define a class `demo` with two methods:
  - `square(int n)` → returns `n * n`.
  - `cube(int n)` → returns `n * square(n)` by calling the `square()` method internally.
- In the `main()` method, create a Scanner object to read input from the user.
- Read an integer value from the user and store it in variable `n`.
- Create an object `d` of the `demo` class.
- Call the `cube()` method using the object `d`.
- Display the calculated cube value.
- Stop the program.

## PROGRAM:

Program to implement Methods using Java

## SOURCE CODE:

```java
import java.util.*;

class demo
{
    public int square(int n)
    {
        return n*n;
    }

    public int cube(int n)
    {
        return n*square(n);
    }
}

public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        
        int n=sc.nextInt();
        
        demo d=new demo();
        
        System.out.println(d.cube(n));
    }
}
```

# OUTPUT :
<img width="392" height="243" alt="image" src="https://github.com/user-attachments/assets/c1ce10c4-d6ea-460a-8004-a16be096890f" />


# RESULT:
Therefore the program successfully computes the cube of a number by internally using the square method.
