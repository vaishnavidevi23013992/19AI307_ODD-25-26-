# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to find the factorial of a given number using a looping statement.

## AIM:
To write a Java program to calculate the factorial of a given number using a loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.util.
3.	Create a class named Main.
4.	Inside the main() method create a Scanner object to read input.
5.	Read an integer value n from the user.
6.	Initialize a variable f to 1 to store the factorial result.
7.	Use a for loop from 1 to n.
8.	Multiply f with each number in the loop.
9.	Store the result in f.
10.	Display the factorial of the number.
11.	Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

```java
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int f = 1;
        
        for(int i=1;i<=n;i++){
            f = f*i;
        }
        
        System.out.println("Factorial of "+n+" is: "+f);
    }
}
```

## SOURCE CODE:

Compile the program using
javac Main.java

Run the program using
java Main






## OUTPUT:

<img width="681" height="248" alt="image" src="https://github.com/user-attachments/assets/84152090-2f71-4b81-8a32-a27112032aa9" />


## RESULT:
Thus, the Java program to find the factorial of a number using a looping statement was executed successfully and the output was verified.
