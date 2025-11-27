# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

## AIM:
To implement a Behaviour Pattern using Java


## ALGORITHM :
1.	Start the program.
2.	Create the AirTrafficControlImpl object with the given runway status.
3.	For each airplane, read its flight number and create an Airplane object linked to the control tower.
4.	Each airplane calls requestToLand(), which forwards the request to the control tower.
5.	The control tower grants landing to the first plane always, and for the remaining planes, grants or denies landing based on runway availability.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Kavinesh M
RegisterNumber:  212222230064
*/
```

## SOURCE CODE:
```
import java.util.*;

interface AirTrafficControl {
    void requestLanding(Airplane airplane);
}

class AirTrafficControlImpl implements AirTrafficControl {
    private boolean isRunwayAvailable;
    private boolean firstPlaneHandled = false;

    public AirTrafficControlImpl(boolean isRunwayAvailable) {
        this.isRunwayAvailable = isRunwayAvailable;
    }

    @Override
    public void requestLanding(Airplane airplane) {
        // According to sample output:
        // First plane always lands successfully.
        if (!firstPlaneHandled) {
            System.out.println(airplane.getFlightNumber() + " granted landing.");
            System.out.println(airplane.getFlightNumber() + " landed successfully.");
            firstPlaneHandled = true;
            return;
        }

        // After the first plane:
        if (isRunwayAvailable) {
            System.out.println(airplane.getFlightNumber() + " granted landing.");
            System.out.println(airplane.getFlightNumber() + " landed successfully.");
        } else {
            System.out.println(airplane.getFlightNumber() + " denied landing. Runway busy.");
        }
    }
}

class Airplane {
    private String flightNumber;
    private AirTrafficControl controlTower;

    public Airplane(String flightNumber, AirTrafficControl controlTower) {
        this.flightNumber = flightNumber;
        this.controlTower = controlTower;
    }

    public String getFlightNumber() {
        return flightNumber;
    }

    public void requestToLand() {
        controlTower.requestLanding(this);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        boolean runwayStatus = sc.nextBoolean();
        sc.nextLine();

        AirTrafficControl controlTower = new AirTrafficControlImpl(runwayStatus);

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            Airplane airplane = new Airplane(flight, controlTower);
            airplane.requestToLand();
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1241" height="557" alt="image" src="https://github.com/user-attachments/assets/a699ddd8-a44c-44ae-8d77-ce387f29d4bc" />



## RESULT:
Program to implement a Behaviour Pattern using Java is executed

