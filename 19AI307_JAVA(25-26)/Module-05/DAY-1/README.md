# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to create a new file and write user-provided content into it.

## AIM:
To create a new file and write user-provided content into it.



## ALGORITHM :
1.	Start the program.
2.	Create the AirTrafficControlImpl object with the given runway status.
3.	For each airplane, read its flight number and create an Airplane object linked to the control tower.
4.	Each airplane calls requestToLand(), which forwards the request to the control tower.
5.	The control tower grants landing to the first plane always, and for the remaining planes, grants or denies landing based on runway availability.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String fileName = sc.nextLine();
        String content = sc.nextLine();  
        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(content);
            writer.close();

            System.out.println("File created: " + fileName);
            System.out.println("Content written to the file successfully.");
        } catch (IOException e) {
            System.out.println("Error while creating or writing to the file.");
        }

       
    }
}
```

## OUTPUT:
<img width="1088" height="331" alt="image" src="https://github.com/user-attachments/assets/2eef3f8b-df98-4743-bff7-701d40a12bcb" />



## RESULT:
Java program to create a new file and write user-provided content into it is executed



