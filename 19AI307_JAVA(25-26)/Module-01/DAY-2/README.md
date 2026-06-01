# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Write a Java program to determine the type of triangle (Equilateral, Isosceles, Scalene) using conditional statements.

## AIM:
To write a Java program to determine the type of triangle using conditional statements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.util.
3.	Create a class named Main.
4.	Inside the main() method, create a Scanner object to read input.
5.	Read three integer values representing the sides of the triangle (h, b, w).
6.	Check if the given sides satisfy the triangle condition : (h + b > w) AND (b + w > h) AND (w + h > b).
7.	If the condition is true:
   - If all three sides are equal → print Equilateral.
   - Else if any two sides are equal → print Isosceles.
   - Else → print Scalene.
8. If the triangle condition is false → print Not a triangle.

9. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

```java
import java.util.Scanner;

public class Main{
    public static void main(String[] aths){
        Scanner sc = new Scanner(System.in);
        
        int h = sc.nextInt();
        int b = sc.nextInt();
        int w = sc.nextInt();
        
        if(h+b>w && b+w>h && w+h>b){
        if(h == b && b == w)System.out.println("Equilateral");
        else if(h==b || w==h ||b==w)System.out.println("Isosceles");
        else System.out.println("Scalene");
        }
        else System.out.println("Not a triangle");
    }
}

```

## SOURCE CODE:

Compile the program using
javac Main.java

Run the program using
java Main






## OUTPUT:
<img width="393" height="151" alt="image" src="https://github.com/user-attachments/assets/256ed377-6ded-4d79-bf5a-809e703dce7a" />



## RESULT:
Thus, the Java program to determine the type of triangle using conditional statements was executed successfully and the output was verified.

