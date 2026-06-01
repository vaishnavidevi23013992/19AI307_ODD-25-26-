# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Write a Java program to demonstrate **inheritance and aggregation** by calculating the final order amount for different types of users in a food delivery system.

---

## AIM:
To write a Java program to demonstrate **inheritance and aggregation concepts using a food delivery order system**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary packages `java.util` and `java.text`.  
3. Create a base class `Order` with attributes `orderId`, `customerName`, `totalAmount`, and `deliveryCharge`.  
4. Create a constructor to initialize these variables.  
5. Create a method `calculateFinalAmount()` to calculate the total order amount.  
6. Create a method `display()` to display order details.  
7. Create a subclass `NormalUser` that extends `Order`.  
8. Override the `display()` method to show details for a normal user.  
9. Create another subclass `PrimeUser` that extends `Order`.  
10. Override the `calculateFinalAmount()` method to apply a **50% discount on delivery charge**.  
11. Override the `display()` method to display prime user details.  
12. In the main class, read user type and order details from the user.  
13. Create the appropriate object (`PrimeUser` or `NormalUser`) based on user type.  
14. Call the `display()` method to print order details.  
15. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

class NormalUser extends Order {
    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    void display(String userType) {
        super.display("Normal");
    }
}

class PrimeUser extends Order {
    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + (deliveryCharge * 0.5);
    }

    @Override
    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: Prime");
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

public class FoodDeliveryApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String type1 = sc.next();
        String id1 = sc.next();
        String name1 = sc.next();
        double amount1 = sc.nextDouble();
        double charge1 = sc.nextDouble();

        Order o1 = type1.equalsIgnoreCase("Prime")
                ? new PrimeUser(id1, name1, amount1, charge1)
                : new NormalUser(id1, name1, amount1, charge1);

        o1.display(type1);

        sc.close();
    }
}
```

---

## SOURCE CODE:

Compile the program using

```
javac FoodDeliveryApp.java
```

Run the program using

```
java FoodDeliveryApp
```

---

## OUTPUT:

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/9d7ae75d-dde6-4203-9442-6e43ad9889f0" />


---

## RESULT:

Thus, the Java program to demonstrate **inheritance and aggregation** was executed successfully and the output was verified.
