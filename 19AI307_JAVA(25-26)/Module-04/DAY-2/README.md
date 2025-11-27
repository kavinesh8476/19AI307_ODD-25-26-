# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

## AIM:
To write a program to implement a SOLID Principles in Java Program


## ALGORITHM :
1.	Start the program.
2.	For each request, read the department name.
3.	Get the single shared instance of PrintSpoolerManager using getInstance() (Singleton pattern).
4.	Submit the job using submitJob(), which increments and returns the total job count.
5.	Display the department name along with the updated total number of jobs in the queue.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; 
    private int jobCount = 0;  

    private PrintSpoolerManager() {}
    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();  
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```


## OUTPUT:
<img width="1209" height="379" alt="image" src="https://github.com/user-attachments/assets/3355a045-a3c7-4d73-9ac3-d5164417d890" />



## RESULT:
Program to implement a SOLID Principles in Java Program is executed

