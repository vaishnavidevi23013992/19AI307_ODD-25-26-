# Ex.No:2(B) METHODS

## QUESTION:
Write a Java program to demonstrate the concept of **class and object**.

---

## AIM:
To write a Java program to demonstrate the **class and object concept using static and non-static methods**.

---

## ALGORITHM :
1. Start the program.  
2. Create a class named `Main`.  
3. Define a **static method** `printst()` to print a message.  
4. Define a **non-static method** `printnonst()` to print a message.  
5. Inside the `main()` method call the static method directly.  
6. Create an object of the class `Main`.  
7. Call the non-static method using the object.  
8. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Class and Objects using Java
Developed by: VAISHNAVIDEVI V 
RegisterNumber: 212223040230  
*/
```
```
public class Main{
    static void printst(){
        System.out.println("I am static");
    }

    void printnonst(){
        System.out.println("I am non-static");
    }

    public static void main(String[] args){
        printst();
        Main obj = new Main();
        obj.printnonst();
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

<img width="416" height="184" alt="image" src="https://github.com/user-attachments/assets/665be8dc-b0bf-4631-aad4-67c1449348e8" />


---

## RESULT:

Thus, the Java program to demonstrate the **class and object concept** was executed successfully and the output was verified.
