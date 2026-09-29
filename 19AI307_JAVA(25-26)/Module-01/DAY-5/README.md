# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to calculate the power of a given number.

## AIM:

To write a Java program to calculate the power of a given number.

## ALGORITHM :

- Start the program.
- Import the necessary packages `java.util.Scanner` and `java.lang.Math`.
- Create a Scanner object to accept input from the user.
- Read two numerical values, `n` (base) and `m` (exponent), from the user.
- Calculate the power using the predefined function `Math.pow(n, m)` and store the result in the variable `pow`.
- Display the calculated power.
- Stop the program.

## PROGRAM:

Program to implement Strings and Math Function using Java

```java
import java.util.Scanner;
import java.lang.Math;

public class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        
        double n=sc.nextInt();
        double m=sc.nextInt();
        
        double pow=Math.pow(n,m);
        
        System.out.printf(n+" raised to the power of "+m+" is: "+pow);
    }
}
```
# OUTPUT: 
<img width="970" height="340" alt="image" src="https://github.com/user-attachments/assets/556c9d5d-f921-4d8e-98d3-1f2762d6cc9b" />


# RESULT:
Therefore the program successfully reads a number and calculates the power of a given number.
