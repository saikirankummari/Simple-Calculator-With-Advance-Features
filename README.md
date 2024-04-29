# Simple-Calculator-With-Advance-Features
Task1
TITLE: CodTech IT Solutions Internship - Task Documentation: “Simple Calculator With Advance Features” Using java.
INTERN INFORMATION: 
Name: Kummari Saikiran
ID: ICOD6734
 
INTRODUCTION:

The Simple Calculator project is a Java-based program aimed at providing users with a straightforward tool for performing basic arithmetic calculations. With a user-friendly interface and intuitive functionality, this calculator offers a convenient solution for everyday mathematical tasks. Whether it's addition, subtraction, multiplication, division, or exponentiation, users can quickly and easily compute their desired operations using this simple yet effective tool.

OVERVIEW:

The Simple Calculator project comprises a set of functionalities encapsulated within a Java class named `SimpleCalculator`. Upon execution, the program presents users with a menu displaying the available arithmetic operations. Users can interact with the calculator by selecting a specific operation from the menu and providing the necessary inputs. The program then performs the chosen operation and displays the result to the user.

FEATURES:

- Addition: Allows users to add multiple numbers together, providing flexibility and convenience.
- Subtraction: Enables users to subtract one number from another, facilitating basic subtraction calculations.
- Multiplication: Supports the multiplication of multiple numbers, making it easy to compute products.
- Division: Provides users with the ability to divide one number by another, handling potential division by zero scenarios gracefully.
- Exponentiation: Allows users to raise a base number to a specified exponent, facilitating exponentiation calculations.

CONCLUSION:

The Simple Calculator project offers a practical solution for performing basic arithmetic calculations with ease. Its intuitive interface and robust functionality make it suitable for users of all levels, from students to professionals. With support for essential arithmetic operations and error handling, this calculator provides a reliable tool for everyday mathematical tasks. Whether it's simple addition or complex exponentiation, the Simple Calculator simplifies mathematical computations, empowering users to focus on their tasks at hand.


TASK1
import java.util.Scanner;
public class SimpleCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        while (true) {
            // Display menu
            System.out.println("\nAdvanced Calculator Menu:");
            System.out.println("1. Addition");
            System.out.println("2. Subtraction");
            System.out.println("3. Multiplication");
            System.out.println("4. Division");
            System.out.println("5. Exponentiation");
            System.out.println("6. Quit");

            // Get user choice
            System.out.print("Enter your choice (1-6): ");
            int choice = scanner.nextInt();

            // Perform operation based on user choice
            switch (choice) {
                case 1:
                    performAddition(scanner);
                    break;
                case 2:
                    performSubtraction(scanner);
                    break;
                case 3:
                    performMultiplication(scanner);
                    break;
                case 4:
                    performDivision(scanner);
                    break;
                case 5:
                    performExponentiation(scanner);
                    break;
                case 6:
                    System.out.println("Exiting the calculator. Goodbye!");
                    scanner.close();
                    System.exit(0);
                    break;
                default:
                    System.out.println("Invalid choice. Please enter a number between 1 and 6.");
            }
        }
    }

    // Method to perform addition
    public static void performAddition(Scanner scanner) {
        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();
        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();
        double result = num1 + num2;
        System.out.println("Result: " + result);
    }

    // Method to perform subtraction
    public static void performSubtraction(Scanner scanner) {
        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();
        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();
        double result = num1 - num2;
        System.out.println("Result: " + result);
    }

    // Method to perform multiplication
    public static void performMultiplication(Scanner scanner) {
        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();
        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();
        double result = num1 * num2;
        System.out.println("Result: " + result);
    }

    // Method to perform division
    public static void performDivision(Scanner scanner) {
        System.out.print("Enter the dividend: ");
        double dividend = scanner.nextDouble();
        System.out.print("Enter the divisor: ");
        double divisor = scanner.nextDouble();
        if (divisor != 0) {
            double result = dividend / divisor;
            System.out.println("Result: " + result);
        } else {
            System.out.println("Error: Division by zero!");
        }
    }

    // Method to perform exponentiation
    public static void performExponentiation(Scanner scanner) {
        System.out.print("Enter the base: ");
        double base = scanner.nextDouble();
        System.out.print("Enter the exponent: ");
        double exponent = scanner.nextDouble();
        double result = Math.pow(base, exponent);
        System.out.println("Result: " + result);
    }
}
