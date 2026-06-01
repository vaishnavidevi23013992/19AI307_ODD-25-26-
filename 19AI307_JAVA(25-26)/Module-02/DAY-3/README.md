# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to demonstrate the use of **access specifiers (private)** using getter and setter methods.

---

## AIM:
To write a Java program to demonstrate **data hiding using private access specifier with getter and setter methods**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `BankAccount`.  
4. Declare private variables `accno` and `bal`.  
5. Create **getter methods** to return account number and balance.  
6. Create **setter methods** to set account number and balance.  
7. Create another class `prog` containing the `main()` method.  
8. Create an object of `BankAccount`.  
9. Read account number and balance from the user.  
10. Use setter methods to store values in the object.  
11. Use getter methods to display account number and balance.  
12. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Access Specifiers using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;

class BankAccount{
    private String accno;
    private double bal;
    
    public String getAccountNumber(){
        return accno;
    }
    
    public void setAccountNumber(String accno){
        this.accno = accno;
    }
    
    public double getbalance(){
        return bal;
    }

    public void setbalance(double balance){
        this.bal = balance;
    }
}

public class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        BankAccount obj = new BankAccount();

        String tempaccno = sc.nextLine();
        double tempbal = sc.nextDouble();

        obj.setAccountNumber(tempaccno);
        obj.setbalance(tempbal);

        System.out.println("Account Number: " + obj.getAccountNumber());
        System.out.println("Balance: " + obj.getbalance());
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

<img width="700" height="300" alt="image" src="https://github.com/user-attachments/assets/172f8c6f-95e6-4e6f-b448-1fe29e391576" />


---

## RESULT:

Thus, the Java program to demonstrate **access specifiers using private variables and getter/setter methods** was executed successfully and the output was verified.
