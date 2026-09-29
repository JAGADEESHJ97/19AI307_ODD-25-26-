# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Define a class Car with brand (String), color (String), and year (int). Create 2 different objects of Car, assign values to their attributes, and print the details of both cars.

## AIM:

To define a class Car with attributes brand, color, and year; create two objects of the class; assign values to their attributes; and print the details of both cars.

## ALGORITHM :

- Start the program.
- Define a class `Car` with three data members: `String brand`, `String color`, and `int year`.
- Define a method `printDetails()` to display the values of the attributes.
- In the `main()` method, create a Scanner object to read user inputs.
- Create the first object `car1` of the Car class.
- Read and assign the brand, color, and year values to `car1`.
- Create the second object `car2` of the Car class.
- Read and assign the brand, color, and year values to `car2`.
- Call the `printDetails()` method for `car1` to display its information.
- Call the `printDetails()` method for `car2` to display its information.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement Class and Object using Java

## SOURCE CODE:

```java
import java.util.Scanner;

class Car {
    String brand;
    String color;
    int year;

    void printDetails() {
        System.out.println("Brand: " + brand);
        System.out.println("Color: " + color);
        System.out.println("Year: " + year);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Car car1 = new Car();
        car1.brand = scanner.nextLine();
        car1.color = scanner.nextLine();
        car1.year = scanner.nextInt();
        scanner.nextLine();

        Car car2 = new Car();
        car2.brand = scanner.nextLine();
        car2.color = scanner.nextLine();
        car2.year = scanner.nextInt();

        car1.printDetails();
        car2.printDetails();

        scanner.close();
    }
}
```
# output :


<img width="597" height="685" alt="image" src="https://github.com/user-attachments/assets/e25fda20-5bf0-4082-a549-26722cc936b9" />

# RESULT:
Therefore,the program successfully creates two Car objects and assigns values to their attributes.
