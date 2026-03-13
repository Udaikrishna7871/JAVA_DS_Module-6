# Ex4 
## DATE: 13-mar-2026
## AIM:
To analyze and determine the nature (even/odd/mixed) of the resulting matrix when performing matrix addition between two matrices where Matrix A contains all odd numbers and Matrix B contains all even numbers of the same dimension.

## Algorithm
Start

Read the dimensions of the matrices (rows and columns).

Read Matrix A (all odd numbers).

Read Matrix B (all even numbers).

Add the matrices element-wise:
Result[i][j] = A[i][j] + B[i][j]

For each element in the resulting matrix:
Since Odd + Even = Odd,
every element of the resulting matrix will be ODD.

Display the resulting matrix and conclude its nature as ODD matrix.

End
   

## Program:
```
import java.util.Scanner;

public class MatrixAdditionNature {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read matrix dimensions
        int rows = sc.nextInt();
        int cols = sc.nextInt();

        // Read Matrix A
        int[][] A = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }

        // Read Matrix B
        int[][] B = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }

        // Add matrices
        int[][] result = new int[rows][cols];

        boolean allEven = true;
        boolean allOdd = true;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = A[i][j] + B[i][j];

                // Check nature of elements
                if (result[i][j] % 2 == 0) {
                    allOdd = false;
                } else {
                    allEven = false;
                }
            }
        }

        // Print result matrix
       // System.out.println("Result matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }

        // Nature of matrix
       
    }
}

```

## Output:

<img width="378" height="551" alt="image" src="https://github.com/user-attachments/assets/5eb7a3e3-ca12-4e55-aaa3-20b71e10b095" />

