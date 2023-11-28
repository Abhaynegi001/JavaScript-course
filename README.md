# JavaScript-course
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
    }

    // Print the original matrix
    printf("Original Matrix:\n");
    for (int i = 0; i < ROWS; ++i) {
        for (int j = 0; j < COLS; ++j) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }

    // Print multiples of 3
    printf("\nMultiples of 3:\n");
    for (int i = 0; i < ROWS; ++i) {
        for (int j = 0; j < COLS; ++j) {
            if (matrix[i][j] % 3 == 0) {
                printf("%d\t", matrix[i][j]);
            } else {
                printf("\t"); // Print empty space for non-multiples
            }
        }
        printf("\n");
    }

    return 0;
}
```

This program first initializes a 3x3 matrix with random numbers, prints the original matrix, and then prints the numbers that are multiples of 3 in the matrix. Adjust the matrix size or range of random numbers as needed.