# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a thread pool to calculate and print the square of each number from input.

## AIM:
To use a thread pool to calculate and print the square of each number from input.

## ALGORITHM :
1.	Start the program.
2.	Create a fixed thread pool with 3 threads using Executors.newFixedThreadPool(3).
3.	For each number, submit a task to the executor that returns the square of the number and store the Future objects.
4.	Shut down the executor to stop accepting new tasks.
5.	Retrieve results using Future.get() for each submitted task and print the square of each number.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        if (!sc.hasNextInt()) return;
        int n = sc.nextInt();  
        List<Integer> nums = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            nums.add(sc.nextInt());
        }

        ExecutorService executor = Executors.newFixedThreadPool(3);
        List<Future<Integer>> results = new ArrayList<>();

        for (int x : nums) {
            results.add(executor.submit(() -> x * x));
        }

        executor.shutdown();

        for (Future<Integer> f : results) {
            try {
                System.out.println("Square: " + f.get());
            } catch (Exception e) {
                e.printStackTrace();
            }
        }
    }
}

```
## OUTPUT:
<img width="455" height="457" alt="image" src="https://github.com/user-attachments/assets/b10fae68-78f2-48da-8e9e-c5cd9bf176f1" />



## RESULT:
Using a thread pool to calculate and print the square of each number from input is executed.


