# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to demonstrate the use of **variable scope and constructor** to initialize and display employee details.

---

## AIM:
To write a Java program to demonstrate **variable scope and constructor initialization in a class**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Employee`.  
4. Declare variables `id`, `name`, and `salary`.  
5. Create a **constructor** to initialize these variables.  
6. Use `this` keyword to assign constructor parameters to class variables.  
7. Create a method `display()` to print employee details.  
8. Create another class `prog` containing the `main()` method.  
9. Read employee id, name, and salary from the user.  
10. Create an object of class `Employee` and pass the values to the constructor.  
11. Call the `display()` method to show employee details.  
12. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/

import java.util.Scanner;

class Employee{
    int id;
    String name;
    double salary;
    
    public Employee(int id,String name,double salary){
        this.id = id;
        this.name = name;
        this.salary = salary;
    }
    
    public void display(){
        System.out.println("Employee Details:");
        System.out.println("Employee ID: "+id);
        System.out.println("Employee Name: "+name);
        System.out.printf("Employee Salary: %.1f",salary);
    }
}

class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int id = sc.nextInt();
        sc.nextLine();
        String name = sc.nextLine();
        double salary = sc.nextDouble();
        
        Employee emp = new Employee(id,name,salary);
        emp.display();
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
<img width="602" height="400" alt="image" src="https://github.com/user-attachments/assets/df638c0e-c766-451f-a381-ae0ed7a2e885" />

```
101
Ravi Kumar
35000
Employee Details:
Employee ID: 101
Employee Name: Ravi Kumar
Employee Salary: 35000.0
```

---

## RESULT:

Thus, the Java program to demonstrate **variable scope and constructor** was executed successfully and the output was verified.
