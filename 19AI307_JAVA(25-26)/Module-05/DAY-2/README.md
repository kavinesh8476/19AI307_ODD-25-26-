# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## AIM:
To demonstrate reading UTF strings using DataInputStream.

## ALGORITHM :
1.	Start the program.
2.	Read a string input from the user.
3.	Create a DataOutputStream connected to "data.txt" and write the string using writeUTF().
4.	Close the output stream.
5.	Create a DataInputStream connected to "data.txt" and read the stored string using readUTF().

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class Q1_ReadUTF_Final {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            String input = sc.nextLine().trim();
            
            DataOutputStream dos = new DataOutputStream(new FileOutputStream("data.txt"));
            dos.writeUTF(input);
            dos.close();

            DataInputStream dis = new DataInputStream(new FileInputStream("data.txt"));
            String result = dis.readUTF();
            dis.close();

            System.out.print("String read from file: " + result);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

## OUTPUT:
<img width="842" height="220" alt="image" src="https://github.com/user-attachments/assets/6b9a58f4-d3fe-4c6e-8a3f-a454a1f37b71" />



## RESULT:
Program to demonstrate reading UTF strings using DataInputStream is executed



