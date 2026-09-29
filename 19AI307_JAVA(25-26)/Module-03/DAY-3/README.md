# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create an abstract class `GameScore` with a method `finalScore()`.

Subclasses:

- `ArcadeGame`: score = `baseScore + (level × 100)`
- `PuzzleGame`: score = `(attempts ≤ 3) ? 1000 - (attempts × 100) : 500`

### Input Format:

- First line: 1 or 2
- Second line: base, level (for ArcadeGame) or attempts (for PuzzleGame)

### Output Format:

Final score (int)

## AIM:

To write a Java program using an abstract class `GameScore` with subclasses `ArcadeGame` and `PuzzleGame`, each implementing its own `finalScore()` method.

## ALGORITHM :

- Start the program.
- Import the necessary package `java.util`.
- Define an abstract class `GameScore` with an abstract method `finalScore()`.
- Define the `ArcadeGame` subclass with `base` and `level` variables.
- Calculate the ArcadeGame score using `base + (level * 100)`.
- Define the `PuzzleGame` subclass with an `attempts` variable.
- If attempts are less than or equal to 3, calculate the score as `1000 - (attempts * 100)`.
- Otherwise, set the score as 500.
- Read the game type from the user.
- If the game type is 1, read the base score and level and create an `ArcadeGame` object.
- If the game type is 2, read the number of attempts and create a `PuzzleGame` object.
- Call the `finalScore()` method and display the final score.
- Stop the program.

## PROGRAM:

Program to implement Abstraction using Java

## SOURCE CODE:

```java
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int base, level;

    ArcadeGame(int base, int level) {
        this.base = base;
        this.level = level;
    }

    int finalScore() {
        return base + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();

        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();

            ArcadeGame game = new ArcadeGame(base, level);
            System.out.println(game.finalScore());
        }
        else if (type == 2) {
            int attempts = sc.nextInt();

            PuzzleGame game = new PuzzleGame(attempts);
            System.out.println(game.finalScore());
        }
    }
}
```
# OUTPUT:

<img width="1147" height="386" alt="image" src="https://github.com/user-attachments/assets/5a765809-f3e0-4b82-959a-de4907f0bdba" />


# RESULT:
The program successfully demonstrates abstraction and inheritance by computing the final score for different game types using subclass-specific logic.

