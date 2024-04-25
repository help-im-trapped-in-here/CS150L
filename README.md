# CS150L

## Exercise P6

```java
// 1. Divisor

public class DivisorCalculator {
    public static int numOfDivisors(int number) {
        int count = 0;
        // Iterate from 2 to number/2
        for (int i = 2; i <= number / 2; i++) {
            // If number is divisible by i, increment count
            if (number % i == 0) {
                count++;
            }
        }
        return count;
    }

    public static void main(String[] args) {
        // Example usage
        int num = 12;
        int divisors = numOfDivisors(num);
        System.out.println("Number of divisors for " + num + ": " + divisors);
    }
}

```

```java
// 2. Leap Years
public class LeapYearChecker {
    public static boolean isLeapYear(int year) {
        if ((year % 4 == 0) && (year % 100 != 0 || year % 400 == 0)) {
            return true;
        } else {
            return false;
        }
    }

    public static void main(String[] args) {
        // Example usage
        int year = 2024;
        if (isLeapYear(year)) {
            System.out.println(year + " is a leap year.");
        } else {
            System.out.println(year + " is not a leap year.");
        }
    }
}
```

```java
// 3. Display Sold Out

public class TicketManager {
    // Example method to simulate tickets availability
    public static int ticketsAvail(int performanceNumber) {
        // Assume some logic to determine available tickets
        // For demonstration, let's assume performances 5, 10, 15 are sold out
        if (performanceNumber == 5 || performanceNumber == 10 || performanceNumber == 15) {
            return 0; // Sold out
        } else {
            return 100; // Some tickets available
        }
    }

    // Method to display sold out performances in a given range
    public static void displaySoldOut(int startPerformance, int endPerformance) {
        System.out.println("Sold out performances:");
        for (int i = startPerformance; i <= endPerformance; i++) {
            if (ticketsAvail(i) == 0) {
                System.out.println("Performance " + i);
            }
        }
    }

    public static void main(String[] args) {
        // Example usage
        int startPerformance = 1;
        int endPerformance = 30;
        displaySoldOut(startPerformance, endPerformance);
    }
}

```

```java
// 4. Reading Positive Integers

import java.util.Scanner;

public class PositiveInputReader {
    public static int readPositive() {
        Scanner scanner = new Scanner(System.in);
        int number;
        do {
            System.out.print("Enter a positive integer: ");
            while (!scanner.hasNextInt()) {
                String input = scanner.next();
                System.out.println("\"" + input + "\" is not a valid integer. Please enter a positive integer.");
                System.out.print("Enter a positive integer: ");
            }
            number = scanner.nextInt();
            if (number <= 0) {
                System.out.println("Please enter a positive integer.");
            }
        } while (number <= 0);
        return number;
    }

    public static void main(String[] args) {
        int p = readPositive();
        System.out.println("You entered: " + p);
    }
}

```
