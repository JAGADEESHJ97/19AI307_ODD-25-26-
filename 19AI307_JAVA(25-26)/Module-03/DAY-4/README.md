# Ex.No:3(D) INTERFACE

## QUESTION:

You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

### Bot Types:

- SunBot: Predicts `"HOT"` if temperature > 30, else `"MODERATE"`.
- RainBot: Predicts `"COLD"` if temperature < 20, else `"WARM"`.

### Input:

Temperature and botType (1 for SunBot, 2 for RainBot)

### Output:

Prediction as a string.

## AIM:

To implement weather prediction using interfaces with two bots — SunBot and RainBot.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define an interface `WeatherBot` with a method `predict()`.
- Create a `SunBot` class that implements the `WeatherBot` interface.
- In `SunBot`, predict `"HOT"` if temperature is greater than 30, otherwise predict `"MODERATE"`.
- Create a `RainBot` class that implements the `WeatherBot` interface.
- In `RainBot`, predict `"COLD"` if temperature is less than 20, otherwise predict `"WARM"`.
- Read the temperature and bot type from the user.
- If bot type is 1, create a `SunBot` object.
- Otherwise, create a `RainBot` object.
- Call the `predict()` method using the interface reference.
- Display the prediction.
- Close the Scanner object.
- Stop the program.

## PROGRAM:

Program to implement an Interface using Java

## SOURCE CODE:

```java
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));

        sc.close();
    }
}
```

# OUTPUT:

<img width="1148" height="334" alt="image" src="https://github.com/user-attachments/assets/59b5e5cb-baed-4731-b802-a61bf337d0db" />


# RESULT:
The program predicts weather conditions using interface implementation and method overriding.
