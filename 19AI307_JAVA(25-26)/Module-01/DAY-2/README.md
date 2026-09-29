# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

A pirate ship has a code lock that only opens if:

- The input code is even, and:
  - If it is less than 100, display "Weak Code".
  - If it is between 100 and 999, display "Strong Code".
- If the code is odd, deny access by displaying "Access Denied".

## AIM:

To write a Java program that accepts a code number and determines the security level based on the given conditions:

- If the code is even and less than 100 → Display "Weak Code"
- If the code is even and between 100 and 999 → Display "Strong Code"
- Otherwise → Display "Access Denied"

## ALGORITHM :

- Start the program.
- Create an object of the Scanner class to take input from the user.
- Read an integer value from the user and store it in variable `num`.
- Check whether the given number is even using `num % 2 == 0`.
- If the number is even, check whether it is less than 100.
- If it is less than 100, display "Weak Code".
- Otherwise, check whether the number is between 100 and 999.
- If it is between 100 and 999, display "Strong Code".
- Otherwise, display "Access Denied".
- If the number is odd, display "Access Denied".
- End the program.

## PROGRAM:

Program to implement conditional statement using Java

```java
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        
        int num=sc.nextInt();
        
        if(num%2==0){
            if(num<100){
                System.out.println("Weak Code");
            }
            else if(num>=100 && num<=999){
                System.out.println("Strong Code");
            }
            else{
                System.out.println("Access Denied");
            }
        }
        else{
            System.out.println("Access Denied");
        }
    }
}
```

# OUTPUT:
<img width="919" height="396" alt="image" src="https://github.com/user-attachments/assets/262ddce1-b277-4c9f-a9ef-5b90cc350d85" />

# RESULT:
Therefore,the program has been executed successfully.
