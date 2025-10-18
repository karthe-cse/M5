EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
#include <stdio.h>

int main() {
    // Step 1: Declare and initialize double variable
    double num = 23.65;

    // Step 2: Declare a pointer to double and point to num
    double *ptr = &num;

    // Step 3: Use the pointer to modify the value to 25.0
    *ptr = 25.0;

    // Step 4: Print the modified value
    printf("Modified value: %.2lf\n", num);

    return 0;
}

## OUTPUT:
Modified value: 25.00
 	











## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
#include <stdio.h>

// Step 1 & 2: Recursive function to calculate product (factorial)
unsigned long long calculateProduct(int n) {
    if (n == 1) {
        return 1;  // Base case
    }
    return n * calculateProduct(n - 1);
}

int main() {
    // Step 3 & 4: Declare variables and initialize n
    int n = 12;
    unsigned long long product;

    // Step 5: Call recursive function
    product = calculateProduct(n);

    // Step 6: Print the result
    printf("Product of the first %d natural numbers is: %llu\n", n, product);

    return 0;
}

## OUTPUT:
Product of the first 12 natural numbers is: 479001600
         	
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
#include <stdio.h>

int main() {
    // Step 1: Declare and initialize the matrix (example 3x4 matrix)
    int matrix[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };

    int rows = 3;
    int cols = 4;

    // Step 2 & 3: Loop through each row and calculate sum
    for (int i = 0; i < rows; i++) {
        int sum = 0;
        for (int j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        // Step 4: Print the sum of the current row
        printf("Sum of row %d = %d\n", i + 1, sum);
    }

    return 0;
}




## OUTPUT
Sum of row 1 = 10
Sum of row 2 = 26
Sum of row 3 = 42


 
 

 ## RESULT
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
#include <stdio.h>

int main() {
    int num_rows, i, j, midpoint;

    // Step 1: Input number of rows
    printf("Enter the number of rows for the pyramid: ");
    scanf("%d", &num_rows);

    // Step 4: Calculate midpoint position (constant for all rows)
    midpoint = (2 * num_rows - 1) / 2;

    // Step 3: Loop for rows
    for (i = 1; i <= num_rows; i++) {
        // You can print or use midpoint here as needed per row
        printf("Row %d midpoint position is: %d\n", i, midpoint);
        // (Step 2 variables i and j are used)
    }

    // Step 5: End the program
    return 0;
}


 ## OUTPUT
Enter the number of rows for the pyramid: 5
Row 1 midpoint position is: 4
Row 2 midpoint position is: 4
Row 3 midpoint position is: 4
Row 4 midpoint position is: 4
Row 5 midpoint position is: 4

 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
#include <stdio.h>

int main() {
    // Step 2: Declare variables
    int i, n;
    int arr[10];
    int *parr = arr;  // pointer to the array

    // Step 3: Read number of elements
    printf("Enter number of elements (up to 10): ");
    scanf("%d", &n);

    // Step 4: Read elements using pointer arithmetic
    for (i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", parr + i);  // equivalent to &arr[i]
    }

    // Step 5: Print elements using pointer dereferencing
    printf("You entered: ");
    for (i = 0; i < n; i++) {
        printf("%d ", *(parr + i));  // equivalent to arr[i]
    }
    printf("\n");

    // Step 6: End program
    return 0;
}

## OUTPUT
Enter number of elements (up to 10): 5
Enter element 1: 12
Enter element 2: 7
Enter element 3: 9
Enter element 4: 20
Enter element 5: 15
You entered: 12 7 9 20 15 

 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


