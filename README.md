# ccc 
# simple calculator.c
#include <stdio.h>  // Include the standard input-output library

int main() {



    // 'operator' will store the math operator chosen by the user.
    // 'num1' and 'num2' will store the operands.
    // 'result' will store the final computed value.
    char operator;
    double num1, num2, result;

    // Prompt the user to enter an operator
    printf("Enter an operator (+, -, *, /): ");
    // The space before "%c" in the format string ensures any previous whitespace is skipped.
    scanf(" %c", &operator);

    // Prompt the user to enter two numbers
    printf("Enter two numbers: ");
    // Read in two double values from the user.
    scanf("%lf %lf", &num1, &num2);

    // Use a switch statement to perform the appropriate mathematical operation based on the operator input.
    switch (operator) {
        case '+':
            // When the operator is '+', add num1 and num2.
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break; // Terminates the execution of the switch statement after this case is executed, preventing fall-through to the next case.
        case '-':
            // When the operator is '-', subtract num2 from num1.
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;// Terminates the execution of the switch statement after this case is executed, preventing fall-through to the next case.
        case '*':
            // When the operator is '*', multiply num1 and num2.
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;// Terminates the execution of the switch statement after this case is executed, preventing fall-through to the next case.
        case '/':
            // When the operator is '/', first check to ensure we are not dividing by zero.
            if (num2 != 0) {
                result = num1 / num2;
                printf("Result: %.2lf\n", result);
            } else {
                // Print an error message if num2 is zero.
                printf("Error: Division by zero is not allowed.\n");// This line prints an error message to the screen indicating that division by zero is not possible.
            }
            break;// Terminates the execution of the switch statement after this case is executed, preventing fall-through to the next case.
        default:
            // If the operator input does not match any valid case, display an error message.
            printf("Error: Invalid operator.\n");
    }

    // Return 0 to indicate that the program executed successfully.
    return 0;
}
