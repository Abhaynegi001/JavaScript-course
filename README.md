 JavaScript-course
Certainly! Here's a simple example of a C program that generates a matrix with random numbers and then prints the numbers that are multiples of 3:

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define ROWS 3
#define COLS 3

int main() {
    // Seed for random number generation
    srand(time(NULL));

    // Initialize a 3x3 matrix with random numbers
    int matrix[ROWS][COLS];
    for (int i = 0; i < ROWS; ++i) {
        for (int j = 0; j < COLS; ++j) {
            matrix[i][j] = rand() % 100; // You can adjust the range of random numbers if needed
        }
 Matrix Certainly! Below is a simple example of a C program to multiply two matrices:

```c
#include <stdio.h>

#define ROWS_A 3
#define COLS_A 2
#define ROWS_B 2
#define COLS_B 4

void multiplyMatrices(int firstMatrix[ROWS_A][COLS_A], int secondMatrix[ROWS_B][COLS_B], int result[ROWS_A][COLS_B]) {
    for (int i = 0; i < ROWS_A; ++i) {
        for (int j = 0; j < COLS_B; ++j) {
            result[i][j] = 0;
            for (int k = 0; k < COLS_A; ++k) {
                result[i][j] += firstMatrix[i][k] * secondMatrix[k][j];
            }
        }
    }
}

void displayMatrix(int matrix[ROWS_A][COLS_B]) {
    for (int i = 0; i < ROWS_A; ++i) {
        for (int j = 0; j < COLS_B; ++j) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int firstMatrix[ROWS_A][COLS_A] = {
        {1, 2},
        {3, 4},
        {5, 6}
    };

    int secondMatrix[ROWS_B][COLS_B] = {
        {7, 8, 9, 10},
        {11, 12, 13, 14}
    };

    int resultMatrix[ROWS_A][COLS_B];

    multiplyMatrices(firstMatrix, secondMatrix, resultMatrix);

    printf("First Matrix:\n");
    displayMatrix(firstMatrix);

    printf("\nSecond Matrix:\n");
    displayMatrix(secondMatrix);

    printf("\nResult Matrix:\n");
    displayMatrix(resultMatrix);

    return 0;
}
```

This program defines two matrices, multiplies them, and prints the original matrices along with the result. You can adjust the size and elements of the matrices as needed.