# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Write a Java program to demonstrate the use of variables and operators (pre-decrement and post-decrement).

## AIM:
To write a Java program to demonstrate the use of variables and decrement operators (pre and post).

## ALGORITHM :
1.	Start the program.
2.	Import the Scanner class to read input from the user.
3.	Create a class named Main.
4.	Inside the main() method, create a Scanner object.
5.	Declare an integer variable n.
6.	Read the value of n from the user.
7.	Display the initial value of n.
8.	Apply post-decrement operator (n--) and print the result.
9.	Apply pre-decrement operator (--n) and print the result
10.	Stop the program.




## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
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
        
        System.out.println("Initial countdown = "+n);
        System.out.println("After post-decrement (a--) = "+(n--)+", Now a = "+n);
        System.out.println("After pre-decrement (--a) = "+(--n)+", Now a = "+n);
    }
}
```



## Sourcecode.java:

Compile the program using
javac Main.java

Run the program using
java Main

## OUTPUT:

<img width="978" height="295" alt="image" src="https://github.com/user-attachments/assets/662cfb16-1b23-4a4c-8438-76875fc0c33d" />




## RESULT:
Thus, the Java program to demonstrate the use of variables and decrement operators was successfully executed and the output was verified.
