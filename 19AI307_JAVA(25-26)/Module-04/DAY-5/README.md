# Ex.No:4(E) DESIGN PATTERN ---- BEHAVIOUR PATTERN

## QUESTION:

Design and implement a system using the Observer Design Pattern where multiple display devices update automatically when weather data changes.

## AIM:

To implement the Observer Design Pattern in Java to automatically notify multiple observers when the state of a subject (weather data) changes.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Create a `Subject` interface with methods to add, remove, and notify observers.
- Create an `Observer` interface with an `update()` method.
- Implement the `WeatherData` class as the Subject.
- Store the registered observers in a list.
- Implement the `CurrentConditionsDisplay` class as an Observer.
- Register multiple display objects with the `WeatherData` object.
- When the weather data changes, call `notifyObservers()`.
- Notify all registered observers using the `update()` method.
- Display the updated temperature and humidity in all observers.
- Stop the program.

## PROGRAM:

Program to implement a Behaviour Pattern using Java


## SOURCE CODE:

```java
import java.util.*;

// Observer Interface
interface Observer {
    void update(float temperature, float humidity);
}

// Subject Interface
interface Subject {
    void addObserver(Observer o);
    void removeObserver(Observer o);
    void notifyObservers();
}

// Concrete Subject
class WeatherData implements Subject {

    private List<Observer> observers;
    private float temperature;
    private float humidity;

    public WeatherData() {
        observers = new ArrayList<>();
    }

    public void addObserver(Observer o) {
        observers.add(o);
    }

    public void removeObserver(Observer o) {
        observers.remove(o);
    }

    public void notifyObservers() {
        for (Observer o : observers) {
            o.update(temperature, humidity);
        }
    }

    public void setMeasurements(float temperature, float humidity) {
        this.temperature = temperature;
        this.humidity = humidity;
        notifyObservers();
    }
}

// Concrete Observer
class CurrentConditionsDisplay implements Observer {

    public void update(float temperature, float humidity) {
        System.out.println("Current Conditions:");
        System.out.println("Temperature: " + temperature);
        System.out.println("Humidity: " + humidity);
        System.out.println("----------------------");
    }
}

// Main Class
public class ObserverPatternDemo {

    public static void main(String[] args) {

        WeatherData weatherData = new WeatherData();

        CurrentConditionsDisplay display1 = new CurrentConditionsDisplay();
        CurrentConditionsDisplay display2 = new CurrentConditionsDisplay();

        weatherData.addObserver(display1);
        weatherData.addObserver(display2);

        weatherData.setMeasurements(30.5f, 65.0f);
        weatherData.setMeasurements(28.0f, 70.0f);
    }
}
```

# OUTPUT:

```
Current Conditions:
Temperature: 30.5
Humidity: 65.0
----------------------
Current Conditions:
Temperature: 30.5
Humidity: 65.0
----------------------
Current Conditions:
Temperature: 28.0
Humidity: 70.0
----------------------
Current Conditions:
Temperature: 28.0
Humidity: 70.0
----------------------
```
# RESULT:
Thus, the program to implement the Observer Design Pattern in Java for automatically updating multiple observers when weather data changes was successfully executed and the output was obtained.
