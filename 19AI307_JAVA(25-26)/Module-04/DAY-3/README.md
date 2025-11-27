# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
You need to clone documents. Implement the Prototype Pattern to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone.

## AIM:
To implement the Prototype Pattern to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone.

## ALGORITHM :
1.	Start the program.
2.	Read the title and content of the document from the user.
3.	Create an original Document object using the given title and content.
4.	Create a clone of the original document using the overridden clone() method.
5.	Display the original document using display("Original").
6.	Display the cloned document using display("Cloned").

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Document implements Cloneable {
    String title, content;

    Document(String title, String content) {
        this.title = title;
        this.content = content;
    }

    @Override
    protected Document clone() {
        try {
            return (Document) super.clone();
        } catch (CloneNotSupportedException e) {
            return null;
        }
    }

    void display(String label) {
        System.out.println(label + ": " + title + " - " + content);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String title = scanner.nextLine();
        String content = scanner.nextLine();

        Document original = new Document(title, content);
        Document clone = original.clone();

        original.display("Original");
        clone.display("Cloned");
    }
}

```

## OUTPUT:

<img width="1259" height="335" alt="image" src="https://github.com/user-attachments/assets/566b5778-8488-4cfc-a88d-2ebddbddf49f" />


## RESULT:
Implementation to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone is executed

