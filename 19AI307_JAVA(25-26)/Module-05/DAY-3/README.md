# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

## AIM:
To count the number of characters in a file.

## ALGORITHM :
1.	Start the program.
2.	Open a PrintWriter for the file chars.txt.
3.	Write the input text into the file and close the writer.
4.	Count the number of characters in the input string using length().

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

public class Q4_CharCount {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            String text = sc.nextLine();

            PrintWriter pw = new PrintWriter("chars.txt");
            pw.print(text);
            pw.close();

            int count = text.length();
            System.out.println("Number of characters written to the file: " + count);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

## OUTPUT:
<img width="1163" height="271" alt="image" src="https://github.com/user-attachments/assets/5c75cb32-09ea-4e76-9df3-492345d53b0b" />



## RESULT:
Program to count the number of characters in a file is executed.



