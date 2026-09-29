# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION: A

In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

## AIM:

To implement the Singleton design pattern in Java to ensure that only a single instance of a `MasterPowerSwitch` class controls global access tracking across multiple players.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define a class `MasterPowerSwitch`.
- Declare a private static instance of the `MasterPowerSwitch` class.
- Declare a private variable `accessCount` to maintain the global access count.
- Create a private constructor to prevent direct instantiation from outside the class.
- Define a static method `getInstance()` to create the object only once and return the same instance whenever it is accessed.
- Define a method `logAccess()` to increment and return the global access count.
- In the `main()` method, create a Scanner object to read input.
- Read the total number of players.
- Read each player's name using a loop.
- Retrieve the single instance of `MasterPowerSwitch` using `getInstance()`.
- Call `logAccess()` to increment the shared access count.
- Display the player's name and the total number of accesses.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement SOLID Principles in Java Program

## SOURCE CODE:

```java
import java.util.*;

class MasterPowerSwitch {

    private static MasterPowerSwitch instance;
    private int accessCount = 0;

    private MasterPowerSwitch() {
    }

    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {

            String player = sc.nextLine();

            MasterPowerSwitch power = MasterPowerSwitch.getInstance();

            int count = power.logAccess();

            System.out.println(player +
                " accessed Master Power Switch. Total accesses so far: "
                + count);
        }

        sc.close();
    }
}
```
# OUTPUT:

<img width="943" height="192" alt="image" src="https://github.com/user-attachments/assets/d9bb453b-04c3-479c-90c2-24cd6da9f56c" />

# RESULT:
Thus the program to implement SDP was executed successfully.
