# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To write a Java program to convert a string to an integer using a wrapper class and perform addition.

## ALGORITHM :
1.	Start the program.
2.	Convert the first string to an integer using Integer.parseInt().
3.	Convert the second string to an integer using Integer.parseInt().
4.	Add the two integers and store the result.
5.	Display the sum in the format: "Sum = <value>".

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class StringToIntegerAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String strNum1 = sc.nextLine();
        String strNum2 = sc.nextLine();

        int num1 = Integer.parseInt(strNum1);
        int num2 = Integer.parseInt(strNum2);

        int sum = num1 + num2;
        System.out.println("Sum = " + sum);

        sc.close();
    }
}
```

## OUTPUT:

<img width="959" height="325" alt="image" src="https://github.com/user-attachments/assets/9d5d52fb-bd1e-4c30-9037-5cf3bc9a8fe7" />


## RESULT:
Java program to convert a string to an integer using a wrapper class and perform addition is executed.



