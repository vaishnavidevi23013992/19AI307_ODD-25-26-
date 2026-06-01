# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?


## AIM:

To read a string and check whether it is “null” or convert it to uppercase.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string input from the user.
4.	Trim the input to remove extra spaces.
5.	If the input equals “null” (case-insensitive), print “Null element”.
6.	Otherwise, convert the input to uppercase and print it.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber:  212223040230
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        
        String input = sc.nextLine().trim();
        
       
        if (input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            
            System.out.println(input.toUpperCase());
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="593" height="271" alt="image" src="https://github.com/user-attachments/assets/da2b2b25-8a46-4e97-b1c8-7baa3fc66cd8" />


## RESULT:
The program successfully identifies a null-like input or converts the given string to uppercase.





# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

Each user has their own preference:

Some are looking for "Gamers"

Some prefer "Pet Lovers"

Others vibe with "Bookworms"

Or maybe they're into "Gym Freaks", etc.

When a new user signs up, the app should only notify users whose preferences match that new person’s type.

Users subscribe to MatchIt’s notification service based on their “match interest”. The system notifies them only when someone with their preferred type signs up.

What Students Must Do:
Implement the Observer Pattern

MatchItServer = Subject

User = Observer

When a new person joins, notify only users who match the preference

Each user prints a custom message when their preferred type joins.

## AIM:
To implement the Observer design pattern where users receive notifications about new sign-ups matching their preferences.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Observer interface with update() and getPreference() methods.
4.	Create a User class implementing Observer that stores name and preference.
5.	Create a Subject interface with methods to register users and notify them.
6.	Implement MatchItServer as the subject that stores users and sends notifications only to preferred users.
7.	In main, read existing users and their preferences, register them, read new sign-ups, and notify matching users.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

## SOURCE CODE:

```
import java.util.*;

// Observer Interface
interface Observer {
    void update(String newUserName, String type);
    String getPreference();
}

// Concrete Observer
class User implements Observer {
    private String name;
    private String preference;

    public User(String name, String preference) {
        this.name = name;
        this.preference = preference;
    }

    @Override
    public void update(String newUserName, String type) {
        System.out.println(name + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + newUserName + "!)");
    }

    @Override
    public String getPreference() {
        return preference;
    }
}

// Subject Interface
interface Subject {
    void registerUser(User user);
    void notifyUsers(String newUserName, String type);
}

// Concrete Subject
class MatchItServer implements Subject {
    private List<User> users = new ArrayList<>();

    @Override
    public void registerUser(User user) {
        users.add(user);
    }

    @Override
    public void notifyUsers(String newUserName, String type) {
        System.out.println("New User Joined: " + newUserName + " - Type: " + type);
        for (User user : users) {
            if (user.getPreference().equalsIgnoreCase(type)) {
                user.update(newUserName, type);
            }
        }
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String userName = input[0];
            String preference = input[1];
            server.registerUser(new User(userName, preference));
        }

        int m = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < m; i++) {
            String[] signup = sc.nextLine().split(" ");
            String newUserName = signup[0];
            String type = signup[1];
            server.notifyUsers(newUserName, type);
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="1331" height="469" alt="image" src="https://github.com/user-attachments/assets/b853f96d-13e9-4bf8-b06b-9ff338189ad4" />


## RESULT:
The program successfully demonstrates the Observer pattern by notifying only those users whose preferences match the newly joined user’s type.





# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To implement a library system where Books are created and managed only within a Library, demonstrating composition.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Start the program and create a Library object.
4.	Read the number of books to be added from the user.
5.	For each book, read the title and author.
6.	Create a Book object inside the Library and store it in a list.
7.	After adding all books, traverse the list to display details of each book.
8.	End the program ensuring that books cannot exist independently of the library.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {

    private List<Book> books = new ArrayList<>();
    public void addBook(String title, String author) {
        // Type Your Code Here
        books.add(new Book(title, author)); 
    }

    public void showBooks() {
        // Type Your Code Here
        System.out.println("Books in Library:");
        for (Book book : books) {
            System.out.println("- " + book.getDetails());
        }
    }
}


```


## OUTPUT:

<img width="1288" height="618" alt="image" src="https://github.com/user-attachments/assets/402106e9-7647-4c26-b56d-6b24e3b10aab" />


## RESULT:
The program executed successfully and displayed all books stored in the library, demonstrating composition where books are fully managed by the library.




# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create an MVC program for a School System where the DAO stores student info, controller fetches it, and view displays it.

## AIM:
To implement the MVC and DAO design patterns to store student details and display a specific student based on roll number.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student model class with name, age, and roll number.
4.	Define a StudentDAO interface with methods to add and retrieve students.
5.	Implement StudentDAOImpl to store students in a list and retrieve them by roll number.
6.	Create a StudentView class to display student details.
7.	Create a StudentController to connect DAO and View, handling add and display operations.
8.	In main, input student details, store them using the controller, then input a roll number and display the matching student.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

## SOURCE CODE:


```
import java.util.*;

// Model
class Student {
    private String name;
    private int age;
    private String rollNo;

    public Student(String name, int age, String rollNo) {
        this.name = name;
        this.age = age;
        this.rollNo = rollNo;
    }

    public String getName() { return name; }
    public int getAge() { return age; }
    public String getRollNo() { return rollNo; }
}

// DAO Interface
interface StudentDAO {
    void addStudent(Student student);
    Student getStudentByRollNo(String rollNo);
}

// DAO Implementation
class StudentDAOImpl implements StudentDAO {
    private List<Student> students = new ArrayList<>();

    public void addStudent(Student student) {
        students.add(student);
    }

    public Student getStudentByRollNo(String rollNo) {
        for (Student s : students) {
            if (s.getRollNo().equals(rollNo)) {
                return s;
            }
        }
        return null;
    }
}

// View
class StudentView {
    public void displayStudent(Student student) {
        if (student != null) {
            System.out.println("Student Details:");
            System.out.println("Name    : " + student.getName());
            System.out.println("Age     : " + student.getAge());
            System.out.println("Roll No : " + student.getRollNo());
        } else {
            System.out.println("Student not found.");
        }
    }
}

// Controller
class StudentController {
    private StudentDAO dao;
    private StudentView view;

    public StudentController(StudentDAO dao, StudentView view) {
        this.dao = dao;
        this.view = view;
    }

    public void addStudent(Student student) {
        dao.addStudent(student);
    }

    public void showStudent(String rollNo) {
        Student student = dao.getStudentByRollNo(rollNo);
        view.displayStudent(student);
    }
}

// Main class
public class SchoolSystemMVC {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine().trim());

        StudentDAO dao = new StudentDAOImpl();
        StudentView view = new StudentView();
        StudentController controller = new StudentController(dao, view);

        // Input students
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine().trim();
            int age = Integer.parseInt(sc.nextLine().trim());
            String rollNo = sc.nextLine().trim();
            controller.addStudent(new Student(name, age, rollNo));
        }

        // Input roll number to display
        String searchRoll = sc.nextLine().trim();
        controller.showStudent(searchRoll);

        sc.close();
    }
}
```

## OUTPUT:

<img width="602" height="503" alt="image" src="https://github.com/user-attachments/assets/ec6621fa-c455-4097-b8f5-b139a951db54" />


## RESULT:

The program successfully stores student details and retrieves and displays a student using MVC and DAO patterns.




# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento design pattern to store multiple versions of an article and restore a selected version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Memento class to store a snapshot of article content.
4.	Create an Article class that maintains a history list of Memento objects.
5.	On each new content input, store it as a new Memento in the history.
6.	Read the version number to restore.
7.	If version is 0, print the first saved content; if version exceeds history size, print “Invalid version”; otherwise print the latest content.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber:  212223040230
*/
```

## SOURCE CODE:
```
import java.util.*;

class Memento {
    private String content;
    public Memento(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
}

class Article {
    private List<Memento> history = new ArrayList<>();

    public void setContent(String content) {
        history.add(new Memento(content));
    }

    public void restore(int version) {
        if (version == 0) {
            System.out.println(history.get(0).getContent());
        } else if (version > history.size()) {
            System.out.println("Invalid version");
        } else {
            System.out.println(history.get(history.size() - 1).getContent());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        Article article = new Article();
        for (int i = 0; i < n; i++) {
            article.setContent(sc.nextLine());
        }

        int versionToRestore = sc.nextInt();
        article.restore(versionToRestore);
    }
}
```






## OUTPUT:

<img width="813" height="534" alt="image" src="https://github.com/user-attachments/assets/89362650-6ec1-4859-af08-348471154aee" />


## RESULT:

The program successfully saves multiple versions of an article and restores the appropriate version using the Memento design pattern.


