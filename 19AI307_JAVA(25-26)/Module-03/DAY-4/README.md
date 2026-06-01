# Ex.No:3(D) INTERFACE

## QUESTION:
Write a Java program to demonstrate the concept of **interface** by implementing different types of judges to decide the result of a game.

---

## AIM:
To write a Java program to demonstrate **interface implementation using different classes**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create an interface named `Judge`.  
4. Declare an abstract method `decide(int p1, int p2)` inside the interface.  
5. Create a class `LenientJudge` that implements the `Judge` interface.  
6. Implement the `decide()` method with the condition:  
   - If difference ≥ 5 → WIN  
   - If difference ≤ -5 → LOSE  
   - Otherwise → DRAW  
7. Create another class `StrictJudge` that implements the `Judge` interface.  
8. Implement the `decide()` method with the condition:  
   - If difference ≥ 10 → WIN  
   - If difference ≤ -10 → LOSE  
   - Otherwise → DRAW  
9. Create the `Main` class with the `main()` method.  
10. Read player1 score, player2 score, and judge type from the user.  
11. Create the appropriate judge object (`LenientJudge` or `StrictJudge`).  
12. Call the `decide()` method and display the result.  
13. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Interface using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.*;

interface Judge {
    String decide(int p1, int p2);
}

class LenientJudge implements Judge {
    public String decide(int p1, int p2) {
        int diff = p1 - p2;
        if (diff >= 5) return "WIN";
        else if (diff <= -5) return "LOSE";
        else return "DRAW";
    }
}

class StrictJudge implements Judge {
    public String decide(int p1, int p2) {
        int diff = p1 - p2;
        if (diff >= 10) return "WIN";
        else if (diff <= -10) return "LOSE";
        else return "DRAW";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int p1 = sc.nextInt();
        int p2 = sc.nextInt();
        int type = sc.nextInt();

        Judge judge;

        if (type == 1)
            judge = new LenientJudge();
        else
            judge = new StrictJudge();

        System.out.println(judge.decide(p1, p2));
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

<img width="310" height="266" alt="image" src="https://github.com/user-attachments/assets/3c12dac9-03ae-42ee-bc57-203de54bcaa7" />


---

## RESULT:

Thus, the Java program to demonstrate **interface implementation** was executed successfully and the output was verified.
