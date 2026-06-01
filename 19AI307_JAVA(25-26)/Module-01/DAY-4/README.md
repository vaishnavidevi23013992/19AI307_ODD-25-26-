# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the maximum odd number in an array.

## AIM:
To write a Java program to find the maximum odd number in a given array using array concept.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.util.
3.	Create a class named Main.
4.	Inside the main() method create a Scanner object.
5.	Read the number of elements n.
6.	Declare an array arr of size n.
7.	Use a loop to read n elements and store them in the array.
8.	Initialize a variable max with Integer.MIN_VALUE.
9.	Traverse through the array using a loop.
10.	Check if the element is odd (arr[i] % 2 != 0).
11.	If the element is odd and greater than max, update max.
12.	After the loop, check:
    - If max is still Integer.MIN_VALUE, print No odd number found.
    - Otherwise print the maximum odd number.

13. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: VAISHNAVIDEVI V
RegisterNumber: 212223040230
*/
```

```java
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++){
            arr[i] = sc.nextInt();
        }
        
        int max = Integer.MIN_VALUE;
        for(int i=0;i<n;i++){
            if(arr[i] % 2 !=0){
                if(arr[i] > max){
                    max = arr[i];
                }
            }
        }
        System.out.println((max == Integer.MIN_VALUE) ? "No odd number found" : max);
    }
}
```

## SOURCE CODE:

Compile the program using
javac Main.java

Run the program using
java Main




## OUTPUT:
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/cb8cfc09-32f0-49e2-bfbe-618d297832f9" />



## RESULT:
Thus, the Java program to find the maximum odd number in an array was executed successfully and the output was verified.
