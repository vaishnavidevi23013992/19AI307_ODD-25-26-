# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to find the **longest word in a given sentence**.

---

## AIM:
To write a Java program to **identify the longest word from a given string using string functions**.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Main`.  
4. Inside the `main()` method create a `Scanner` object.  
5. Read a full line string from the user.  
6. Split the string into words using `split("\\s+")`.  
7. Store the first word as the longest word.  
8. Traverse through the remaining words using a loop.  
9. Compare the length of each word with the current longest word.  
10. If a word is longer, update the longest word.  
11. Display the longest word.  
12. Stop the program.

---

## PROGRAM:

```java
/*
Program to find the longest word in a string
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);

        String a=sc.nextLine();

        String[] words=a.split("\\s+");

        String l=words[0];
        
        for(int i=1;i<words.length;i++)
        {
            if(words[i].length()>l.length())
            {
                l=words[i];
            }
        }

        System.out.println("The longest word is: "+l);
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

<img width="747" height="261" alt="image" src="https://github.com/user-attachments/assets/342723c1-b57f-44c9-8b13-95771e3cf7c6" />


---

## RESULT:

Thus, the Java program to find the **longest word in a given string** was executed successfully and the output was verified.
