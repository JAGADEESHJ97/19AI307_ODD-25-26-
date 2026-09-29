# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to reverse an array.

## AIM:

To write a Java program to reverse an array.

## ALGORITHM :

- Start the program.
- Import the `java.util.Scanner` package.
- Create a Scanner object to read input from the user.
- Read the integer `n` representing the size of the array.
- Declare an integer array `arr` of size `n`.
- Loop from 0 to `n - 1` to accept and store the array elements.
- Loop backwards from `n - 1` down to 0.
- Print each element of the array in reverse order.
- Stop the program.

## PROGRAM:

Program to implement an Array concept using Java


```java
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        
        int n=sc.nextInt();
        int[] arr=new int[n];
        
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        
        for(int i=n-1;i>=0;i--){
            System.out.print(arr[i]+" ");
        }
    }
}
```
# OUTPUT:
<img width="721" height="639" alt="image" src="https://github.com/user-attachments/assets/5e3b4181-3f2d-48f9-a2c1-6b124dedf138" />

# RESULT:
Therefore the program successfully reverse an array.
