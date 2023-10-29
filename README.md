       #include <stdio.h>
        #include <stdlib.h>
        #include <math.h>

        int main() {
        int choice;
        float result, num1, num2;
        float km; // Declare 'km' outside of the switch-case block

        printf("Welcome to my multitasking converter\n");
        printf("Press a key according to your preferences:\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Modulus\n");
        printf("6. Percentage\n");
        printf("7. Convert Distance\n");
        printf("8. Convert Temperature\n");
        printf("9. Convert Binary Numbers\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
        case 1:
        // Addition
        printf("Enter two numbers for addition: ");
        scanf("%f %f", &num1, &num2);
        result = num1 + num2;
        printf("Result of addition: %.2f\n", result);
        break;

        case 2:
        // Subtraction
        printf("Enter two numbers for subtraction: ");
        scanf("%f %f", &num1, &num2);
        result = num1 - num2;
        printf("Result of subtraction: %.2f\n", result);
        break;

        case 3:
        // Multiplication
        printf("Enter two numbers for multiplication: ");
        scanf("%f %f", &num1, &num2);
        result = num1 * num2;
        printf("Result of multiplication: %.2f\n", result);
        break;

        case 4:
        // Division
        printf("Enter two numbers for division: ");
        scanf("%f %f", &num1, &num2);
        if (num2 != 0) {
        result = num1 / num2;
        printf("Result of division: %.2f\n", result);
        } else {
        printf("Error: Division by zero is not allowed.\n");
        }
        break;

        case 5:
        // Modulus
        printf("Enter two numbers for modulus (a % b): ");
        scanf("%f %f", &num1, &num2);
        result = fmod(num1, num2);
        printf("Result of modulus: %.2f\n", result);
        break;

        case 6:
        // Percentage
        printf("Enter two numbers to find the percentage (a is what percent of b): ");
        scanf("%f %f", &num1, &num2);
        if (num2 != 0) {
        result = (num1 / num2) * 100;
        printf("Result of percentage: %.2f%%\n", result);
        } else {
        printf("Error: Division by zero is not allowed when calculating the percentage.\n");
        }
        break;

        case 7: {
        int subChoice;
        float meters, kilometers, miles;
        printf("Welcome to my distance converter\n");
        printf("Press a key according to your preferences:\n");
        printf("1. Meters to Kilometers\n");
        printf("2. Meters to Miles\n");
        printf("3. Kilometers to Meters\n");
        printf("4. Kilometers to Miles\n");
        printf("5. Miles to Meters\n");
        printf("6. Miles to Kilometers\n");
        printf("Enter your choice: ");
        scanf("%d", &subChoice);

        switch (subChoice) {
        case 1:
        // Meters to Kilometers
        printf("Enter distance in meters: ");
        scanf("%f", &meters);
        kilometers = meters / 1000;
        printf("Distance in kilometers: %.2f\n", kilometers);
        break;

        case 2:
        // Meters to Miles
        printf("Enter distance in meters: ");
        scanf("%f", &meters);
        miles = meters / 1609.34;
        printf("Distance in miles: %.2f\n", miles);
        break;

        case 3: // Moved 'km' declaration here
        // Kilometers to Meters
        printf("Enter distance in kilometers: ");
        scanf("%f", &km);
        meters = km * 1000;
        printf("Distance in meters: %.2f\n", meters);
        break;

        case 4:
        // Kilometers to Miles
        printf("Enter distance in kilometers: ");
        scanf("%f", &km);
        miles = km * 0.621371;
        printf("Distance in miles: %.2f\n", miles);
        break;

        case 5:
        // Miles to Meters
        float miles2;
        printf("Enter distance in miles: ");
        scanf("%f", &miles2);
        meters = miles2 * 1609.34;
        printf("Distance in meters: %.2f\n", meters);
        break;

        case 6:
        // Miles to Kilometers
        printf("Enter distance in miles: ");
        scanf("%f", &miles);
        kilometers = miles * 1.60934;
        printf("Distance in kilometers: %.2f\n", kilometers);
        break;

default: {
        printf("Invalid sub-choice for distance conversion. Please select a valid option.\n");
        break;
        }
        }
        break;
        }

        case 8: {
        int tempChoice;
        float celsius, fahrenheit, fahrenheit2, celsius2;
        printf("Temperature Conversion Options:\n");
        printf("1. Celsius to Fahrenheit\n");
        printf("2. Fahrenheit to Celsius\n");
        printf("Enter your choice: ");
        scanf("%d", &tempChoice);

        switch (tempChoice) {
        case 1:
        printf("Enter temperature in Celsius: ");
        scanf("%f", &celsius);
        fahrenheit = (celsius * 9/5) + 32;
        printf("Temperature in Fahrenheit: %.2f\n", fahrenheit);
        break;

        case 2:
        printf("Enter temperature in Fahrenheit: ");
        scanf("%f", &fahrenheit2);
        celsius2 = (fahrenheit2 - 32) * 5/9;
        printf("Temperature in Celsius: %.2f\n", celsius2);
        break;

default: {
        printf("Invalid sub-choice for temperature conversion. Please select a valid option.\n");
        break;
        }
        }
        break;
        }

        case 9: {
        unsigned long long int decimalNum;
        char hexNum[20];
        char binaryNum[65];
        char octalNum[24];

        printf("Number Base Converter\n");
        printf("1. Hexadecimal to Decimal\n");
        printf("2. Hexadecimal to Octal\n");
        printf("3. Hexadecimal to Binary\n");
        printf("4. Binary to Hexadecimal\n");
        printf("5. Binary to Octal\n");
        printf("6. Binary to Decimal\n");
        printf("7. Octal to Binary\n");
        printf("8. Octal to Decimal\n");
        printf("9. Octal to Hexadecimal\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
        case 1:
        // Hexadecimal to Decimal
        printf("Enter a hexadecimal number: ");
        scanf("%s", hexNum);
        sscanf(hexNum, "%llx", &decimalNum);
        printf("Decimal equivalent: %llu\n", decimalNum);
        break;

        case 2:
        // Hexadecimal to Octal
        printf("Enter a hexadecimal number: ");
        scanf("%s", hexNum);
        sscanf(hexNum, "%llx", &decimalNum);
        printf("Octal equivalent: %llo\n", decimalNum);
        break;

        case 3:
        // Hexadecimal to Binary
        printf("Enter a hexadecimal number: ");
        scanf("%s", hexNum);
        sscanf(hexNum, "%llx", &decimalNum);
        printf("Binary equivalent: ");
        for (int i = 63; i >= 0; i--) {
        binaryNum[i] = (decimalNum & 1) + '0';
        decimalNum >>= 1;
        }
        binaryNum[64] = '\0';
        printf("%s\n", binaryNum);
        break;

        case 4:
        // Binary to Hexadecimal
        printf("Enter a binary number: ");
        scanf("%s", binaryNum);
        decimalNum = strtoull(binaryNum, NULL, 2);
        sprintf(hexNum, "%llx", decimalNum);
        printf("Hexadecimal equivalent: %s\n", hexNum);
        break;

        case 5:
        // Binary to Octal
        printf("Enter a binary number: ");
        scanf("%s", binaryNum);
        decimalNum = strtoull(binaryNum, NULL, 2);
        sprintf(octalNum, "%llo", decimalNum);
        printf("Octal equivalent: %s\n", octalNum);
        break;

        case 6:
        // Binary to Decimal
        printf("Enter a binary number: ");
        scanf("%s", binaryNum);
        decimalNum = strtoull(binaryNum, NULL, 2);
        printf("Decimal equivalent: %llu\n", decimalNum);
        break;

        case 7:
        // Octal to Binary
        printf("Enter an octal number: ");
        scanf("%s", octalNum);
        decimalNum = strtoull(octalNum, NULL, 8);
        printf("Binary equivalent: ");
        for (int i = 63; i >= 0; i--) {
        binaryNum[i] = (decimalNum & 1) + '0';
        decimalNum >>= 1;
        }
        binaryNum[64] = '\0';
        printf("%s\n", binaryNum);
        break;

        case 8:
        // Octal to Decimal
        printf("Enter an octal number: ");
        scanf("%s", octalNum);
        decimalNum = strtoull(octalNum, NULL, 8);
        printf("Decimal equivalent: %llu\n", decimalNum);
        break;

        case 9:
        // Octal to Hexadecimal
        printf("Enter an octal number: ");
        scanf("%s", octalNum);
        decimalNum = strtoull(octalNum, NULL, 8);
        sprintf(hexNum, "%llx", decimalNum);
        printf("Hexadecimal equivalent: %s\n", hexNum);
        break;

default: {
        printf("Invalid choice. Please select a valid option.\n");
        break;
        }
        }
        break;
        }

default: {
        printf("Invalid choice. Please select a valid option.\n");
        break;
        }
        }

        return 0;
        }
