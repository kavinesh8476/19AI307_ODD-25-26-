# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write Program to implement a Exception Handling using Java

## ALGORITHM :
1.	Start the program.
2.	Check if the input is null or the text "null" (case-insensitive).
3.	If true, print "Null element".
4.	Otherwise, convert the input string to uppercase.
5.	Print the uppercase result.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();

        if (input == null || input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }
    }
}
```
## OUTPUT:
<img width="703" height="254" alt="image" src="https://github.com/user-attachments/assets/b424b815-904e-492d-9b64-cc2648f55a5b" />

## RESULT:
Program to implement a Exception Handling using Java is executed

