# Ex.No:4(A) EXCEPTION HANDLING


## QUESTION:
Write a Java program to demonstrate **NullPointerException handling**.

---

## AIM:
To write a Java program to demonstrate **handling of NullPointerException using try-catch block**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Main`.  
4. Inside the `main()` method create a `Scanner` object.  
5. Read a string input from the user.  
6. Check if the input string is equal to `"null"`.  
7. If yes, manually throw a `NullPointerException`.  
8. Otherwise, convert the string to uppercase using `toUpperCase()`.  
9. Use `try-catch` block to handle the exception.  
10. If exception occurs, print `"Null element"`.  
11. Stop the program.

---

## PROGRAM:

```java
/*
Program to demonstrate NullPointerException handling
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        String str = sc.nextLine();
        
        try{
            if(str.equals("null")){
                throw new NullPointerException();
            }

            System.out.println(str.toUpperCase());

        }catch(NullPointerException e){
            System.out.println("Null element");
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

<img width="439" height="226" alt="image" src="https://github.com/user-attachments/assets/514eab59-d5dc-47b0-84d1-6ce5df3dcda0" />


---

## RESULT:

Thus, the Java program to demonstrate **NullPointerException handling** was executed successfully and the output was verified.
