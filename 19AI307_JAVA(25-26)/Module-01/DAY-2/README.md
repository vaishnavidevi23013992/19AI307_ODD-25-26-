# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Write a Java program to demonstrate the concept of **class and object** by storing and displaying vehicle details.

---

## AIM:
To write a Java program to demonstrate the **class and object concept by creating objects and accessing their attributes**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class named `Main`.  
4. Define an inner class `Vehicle` with attributes `number`, `type`, and `owner`.  
5. Inside the `main()` method create a `Scanner` object.  
6. Create the first object `v1` of class `Vehicle`.  
7. Read vehicle number, type, and owner name for `v1`.  
8. Create the second object `v2` of class `Vehicle`.  
9. Read vehicle number, type, and owner name for `v2`.  
10. Display the details of both vehicles using the object variables.  
11. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Class and Objects using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230  
*/

import java.util.Scanner;

public class Main {
    public static class Vehicle{
        String number;
        String type;
        String owner;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

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

<img width="800" height="243" alt="image" src="https://github.com/user-attachments/assets/5df587ce-7eee-47ca-86e2-f33f2326dbae" />


---

## RESULT:

Thus, the Java program to demonstrate the **class and object concept** was executed successfully and the output was verified.
