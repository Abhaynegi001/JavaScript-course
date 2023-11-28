 // C program to multiply 3 matrices using a function
#include <stdio.h>
#define N 3 // size of the matrices

// Function to multiply 3 matrices A, B and C
void multiply3(int A[N][N], int B[N][N], int C[N][N], int D[N][N])
{
    int i, j, k, l; // loop variables
    int temp[N][N]; // temporary matrix to store the product of A and B

    // Initialize temp and D matrices to zero
    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            temp[i][j] = 0;
            D[i][j] = 0;
        }
    }

    // Multiply A and B matrices and store the result in temp matrix
    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            for (k = 0; k < N; k++)
            {
                temp[i][j] += A[i][k] * B[k][j];
            }
        }
    }

    // Multiply temp and C matrices and store the result in D matrix
    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            for (l = 0; l < N; l++)
            {
                D[i][j] += temp[i][l] * C[l][j];
            }
        }
    }
}

// Function to print a matrix
void printMatrix(int M[N][N])
{
    int i, j; // loop variables
    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            printf("%d ", M[i][j]);
        }
        printf("\n");
    }
}

// Main function
int main()
{
    // Declare and initialize 3 matrices
    int A[N][N] = {{1, 2, 3},
                   {4, 5, 6},
                   {7, 8, 9}};

    int B[N][N] = {{10, 11, 12},
                   {13, 14, 15},
                   {16, 17, 18}};

    int C[N][N] = {{19, 20, 21},
                   {22, 23, 24},
                   {25, 26, 27}};

    int D[N][N]; // matrix to store the product of A, B and C

    // Call the function to multiply 3 matrices
    multiply3(A, B, C, D);

    // Print the result matrix
    printf("The product of the 3 matrices is:\n");
    printMatrix(D);

    return 0;
}

     