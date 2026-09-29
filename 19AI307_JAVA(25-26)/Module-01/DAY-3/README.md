# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.

- Use a for loop to perform the calculation.
- Make sure to handle the case when the user enters 0.
- Display the result in a clear and user-friendly way.

## AIM:

To write a Java program to calculate and display the factorial of the given number.

## ALGORITHM :

- Start the program and prompt the user to enter a non-negative integer n.
- Read the integer n.
- Check if n is equal to 0.
- If n is 0, display the factorial as 1.
- Otherwise, initialize `fact = 1`.
- Use a for loop from 1 to n.
- Multiply `fact` by i in each iteration.
- Display the resulting factorial value.
- End the program.

## PROGRAM:

Program to implement a Looping Statement using Java

```java
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        
        int n=sc.nextInt();
        int fact=1;
        
        if(n==0){
            System.out.println("Factorial of 0 is: "+fact);
        }
        else{
            for(int i=1;i<=n;i++){
                fact=fact*i;
            }
            System.out.println("Factorial of "+n+" is: "+fact);
        }
    }
}
```
# OUTPUT:
<img width="796" height="338" alt="image" src="https://github.com/user-attachments/assets/bb13d241-533e-4447-8f6d-87ed107236fe" />

# RESULT:
Therefore, the program successfully reads a number from the user and computes its factorial.
