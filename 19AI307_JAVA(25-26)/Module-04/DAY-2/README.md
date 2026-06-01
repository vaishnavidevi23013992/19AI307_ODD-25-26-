# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION:
Write a Java program to demonstrate **SOLID principles** using the Observer design pattern.

---

## AIM:
To write a Java program to demonstrate **SOLID principles (especially Single Responsibility and Open/Closed Principle)** using the Observer pattern.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create an interface `Observer` with a method `notify()`.  
4. Create a class `Subscriber` that implements `Observer`.  
5. Define a variable `name` and override the `notify()` method.  
6. Create a class `Channel`.  
7. Declare a variable `channelName` and a list of subscribers.  
8. Create a method `subscribe()` to add observers.  
9. Create a method `uploadVideo()` to notify all subscribers.  
10. In the main class, read the channel name.  
11. Create a `Channel` object.  
12. Read the number of subscribers and their names.  
13. Add each subscriber to the channel.  
14. Read the number of videos and their titles.  
15. For each video, call `uploadVideo()` to notify subscribers.  
16. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement SOLID principles using Observer Pattern
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```
```
import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    public void notify(String channelName, String videoTitle) {
        System.out.println(name + ": New video from " + channelName + "! Watch now...");
    }
}

class Channel {
    private String channelName;
    private List<Observer> subscribers = new ArrayList<>();

    public Channel(String name) {
        this.channelName = name;
    }

    public void subscribe(Observer o) {
        subscribers.add(o);
    }

    public void uploadVideo(String videoTitle) {
        System.out.println(channelName + " uploaded: " + videoTitle);
        for (Observer o : subscribers) {
            o.notify(channelName, videoTitle);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String channelName = sc.nextLine();
        Channel channel = new Channel(channelName);

        int n = sc.nextInt(); 
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }

        int v = sc.nextInt(); 
        sc.nextLine();

        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }
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

<img width="1000" height="270" alt="image" src="https://github.com/user-attachments/assets/bcac929b-c9a2-42fd-a786-a573e3fefb4a" />


---

## RESULT:

Thus, the Java program to demonstrate **SOLID principles using Observer pattern** was executed successfully and the output was verified.
