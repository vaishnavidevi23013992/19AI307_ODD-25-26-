# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check whether a number is **prime using wrapper classes**.

---

## AIM:
To write a Java program to **check whether a number is prime using wrapper class methods**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Main`.  
4. Inside the `main()` method create a `Scanner` object.  
5. Read the input as a string.  
6. Convert the string into an integer using `Integer.parseInt()` (wrapper class).  
7. If the number is less than or equal to 1, print not prime.  
8. Otherwise, check divisibility from `2` to `√n`.  
9. If divisible, mark as not prime.  
10. If not divisible by any number, mark as prime.  
11. Use `try-catch` to handle invalid input.  
12. Display the result.  
13. Stop the program.

---

## PROGRAM:

```java
/*
Program to check prime number using wrapper class
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        String num = sc.nextLine();
        
        try{
            Integer n = Integer.parseInt(num);
            
            if(n <= 1){
                System.out.println(n + " is not a prime number.");
            }else{
                boolean isprime = true;

                for(int i = 2; i <= Math.sqrt(n); i++){
                    if(n % i == 0){
                        isprime = false;
                        break;
                    }
                }
                
                if(isprime){
                    System.out.println(n + " is a prime number.");
                }else{
                    System.out.println(n + " is not a prime number.");
                }
            }
        
        }catch(NumberFormatException e){
            System.out.println("Invalid input. Please enter a valid integer.");
        }

        sc.close();
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

<img width="609" height="225" alt="image" src="https://github.com/user-attachments/assets/395c6981-57e0-40c5-88d6-00beb4034e63" />


---

## RESULT:

Thus, the Java program to check whether a number is **prime using wrapper class** was executed successfully and the output was verified.
