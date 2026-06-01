# Ex.No:3(C) ABSTRACTION

## QUESTION:
Write a Java program to demonstrate **abstraction using abstract class and method** to calculate the final score of different games.

---

## AIM:
To write a Java program to demonstrate **abstraction using an abstract class and abstract method**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create an abstract class `GameScore`.  
4. Declare an abstract method `finalScore()` inside the abstract class.  
5. Create a subclass `ArcadeGame` that extends `GameScore`.  
6. Define variables `baseScore` and `level`.  
7. Implement the `finalScore()` method to calculate the score as `baseScore + (level * 100)`.  
8. Create another subclass `PuzzleGame` that extends `GameScore`.  
9. Define a variable `attempts`.  
10. Implement the `finalScore()` method using the condition:  
   - If attempts ≤ 3 → score = `1000 - (attempts * 100)`  
   - Otherwise → score = `500`.  
11. In the main class read the game type from the user.  
12. Based on the game type create the appropriate object (`ArcadeGame` or `PuzzleGame`).  
13. Call the `finalScore()` method and display the result.  
14. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Abstraction using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

abstract class GameScore{
    abstract int finalScore();
}

class ArcadeGame extends GameScore{
    int baseScore,level;
    
    ArcadeGame(int baseScore,int level){
        this.baseScore = baseScore;
        this.level = level;
    }
    
    int finalScore(){
        return (baseScore + (level * 100));
    }
}

class PuzzleGame extends GameScore{
    int attempts;

    PuzzleGame(int attempts){
        this.attempts = attempts;
    }
    
    int finalScore(){
        return (attempts <= 3) ? (1000 - (attempts * 100)) : 500;
    }
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();
        
        if(type == 1){
            int base = sc.nextInt();
            int level = sc.nextInt();

            ArcadeGame arcade = new ArcadeGame(base,level);
            System.out.println(arcade.finalScore());

        }else if(type==2){
            int attempts = sc.nextInt();

            PuzzleGame puzzle = new PuzzleGame(attempts);
            System.out.println(puzzle.finalScore());
        }
    }
}
```

---

## SOURCE CODE:

Compile the program using

```
javac Main.java
```

Run the program using

```
java Main
```

---

## OUTPUT:

<img width="304" height="182" alt="image" src="https://github.com/user-attachments/assets/1f0814b6-d185-4723-bd94-d5e72133a066" />


---

## RESULT:

Thus, the Java program to demonstrate **abstraction using an abstract class and abstract method** was executed successfully and the output was verified.
