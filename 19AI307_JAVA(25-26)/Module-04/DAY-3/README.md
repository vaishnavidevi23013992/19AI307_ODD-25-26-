# Ex.No:4(C) COMPOSITION IN JAVA

## QUESTION:
Write a Java program to demonstrate the concept of **Composition**.

---

## AIM:
To write a Java program to demonstrate **Composition by creating a class that contains objects of another class**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Engine` with an attribute `engineType`.  
4. Create a method `displayEngine()` to display engine details.  
5. Create a class `Car`.  
6. Declare variables `carName` and an object of class `Engine`.  
7. Create a constructor in `Car` to initialize car name and engine object.  
8. Create a method `displayCar()` to display car and engine details.  
9. In the main class, create objects of `Engine` and `Car`.  
10. Call the method to display details.  
11. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement Composition Concepts in Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.*;

class Engine{
    String engineType;

    Engine(String engineType){
        this.engineType = engineType;
    }

    void displayEngine(){
        System.out.println("Engine Type: " + engineType);
    }
}

class Car{
    String carName;
    Engine engine;   // Composition

    Car(String carName, Engine engine){
        this.carName = carName;
        this.engine = engine;
    }

    void displayCar(){
        System.out.println("Car Name: " + carName);
        engine.displayEngine();
    }
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        String carName = sc.nextLine();
        String engineType = sc.nextLine();

        Engine e = new Engine(engineType);
        Car c = new Car(carName, e);

        c.displayCar();
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

```
BMW
Petrol
Car Name: BMW
Engine Type: Petrol
```

---

## RESULT:

Thus, the Java program to demonstrate **Composition in Java** was executed successfully and the output was verified.
