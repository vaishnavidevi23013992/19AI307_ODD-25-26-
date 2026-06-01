# Ex.No:3(B) POLYMORPHISM

## QUESTION:
Write a Java program to demonstrate **polymorphism using method overloading** to calculate the area of square, rectangle, and circle.

---

## AIM:
To write a Java program to demonstrate **compile-time polymorphism using method overloading**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `AreaCalculator`.  
4. Create a method `area(int side)` to calculate the area of a square.  
5. Create a method `area(int length, int breadth)` to calculate the area of a rectangle.  
6. Create a method `area(double radius)` to calculate the area of a circle.  
7. Create another class `Main` containing the `main()` method.  
8. Create a `Scanner` object to read input values.  
9. Read side, length, breadth, and radius from the user.  
10. Create an object of class `AreaCalculator`.  
11. Call the overloaded `area()` methods using the object.  
12. Display the calculated areas.  
13. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Polymorphism using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

class AreaCalculator{

    void area(int side){
        System.out.println("Area of square: " + (side*side));
    }

    void area(int length,int breadth){
        System.out.println("Area of rectangle: " + (length*breadth));
    }

    void area(double radius){
        System.out.println("Area of circle: " + (Math.PI*radius*radius));
    }
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int side = sc.nextInt();
        int length = sc.nextInt();
        int breadth = sc.nextInt();
        double radius = sc.nextDouble();
        
        AreaCalculator obj = new AreaCalculator();

        obj.area(side);
        obj.area(length,breadth);
        obj.area(radius);
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

<img width="700" height="345" alt="image" src="https://github.com/user-attachments/assets/b0daa3d3-aec0-466a-bb28-2ebeddd2bd40" />


---

## RESULT:

Thus, the Java program to demonstrate **polymorphism using method overloading** was executed successfully and the output was verified.
