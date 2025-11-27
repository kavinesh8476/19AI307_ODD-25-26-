# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

## AIM:
To write a java program for determine the priority and name of the current thread.


## ALGORITHM :
1.	Start the program.
2.	Get the current thread using Thread.currentThread().
3.	Set the name of the current thread using setName().
4.	Retrieve the thread’s priority and name using getPriority() and getName().
5.	Print the thread's priority, name, and full thread information object.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();  
        
        Thread t = Thread.currentThread();  
        t.setName(threadName);               
        
        // Output
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);   
    }
}

```

## OUTPUT:
<img width="784" height="215" alt="image" src="https://github.com/user-attachments/assets/110e0816-3f02-45a5-b4e4-aba1f835eeb3" />



## RESULT:
Java program for determine the priority and name of the current thread is executed.



