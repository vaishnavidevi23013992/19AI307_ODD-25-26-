# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a Java program to demonstrate the use of **access modifiers** in a class.

---

## AIM:
To write a Java program to demonstrate **access modifiers by accessing class members through methods**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class named `Employee`.  
4. Declare a variable `name` inside the class.  
5. Create a method `setName()` to assign a value to the variable.  
6. Create a method `display()` that returns the current object using `this`.  
7. Create a method `printName()` to display the employee name.  
8. Create another class `prog` with the `main()` method.  
9. Read the employee name from the user.  
10. Create an object of class `Employee`.  
11. Call `setName()` to store the name.  
12. Call `display().printName()` to print the employee name.  
13. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Access Modifiers using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

class Employee{
    String name;
    
    void setName(String name){
        this.name = name;
    }

    Employee display(){
        return this;
    }

    void printName(){
        System.out.println("Employee Name: " + name);
    }
}

class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();

        Employee emp = new Employee();
        emp.setName(name);

        emp.display().printName();
    }
}
```

---

## SOURCE CODE:

Compile the program using

```
javac prog.java
```

Run the program using

```
java prog
```

---

## OUTPUT:

<img width="623" height="255" alt="image" src="https://github.com/user-attachments/assets/e7f86a3e-a5f5-4e87-86e8-07a308e1f7de" />


---

## RESULT:

Thus, the Java program to demonstrate **access modifiers** was executed successfully and the output was verified.
