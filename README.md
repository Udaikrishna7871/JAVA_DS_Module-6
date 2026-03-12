# EXP-1
# AIM:
To write a recursive Java program that computes the factorial of a given non-negative integer N, where 
0
≤
𝑁
≤
15
0≤N≤15. The program should take an integer as input, use recursion instead of loops to calculate the factorial, and display the result in the format:
# ALGORITHM:
Start

Read the integer input N.

If N is 0
→ Return 1 (because 0! = 1).

Else
→ Compute factorial using the recursive formula:
factorial(N) = N × factorial(N − 1)

Return the computed factorial value.

Display the result in the format:
Factorial: <result>

End
# PROGRAM:
~~~
import java.util.Scanner;

public class RecursiveFactorial {

    public static int factorial(int n) {
        if (n == 0) {
            return 1;
        } 
        else
        {
            
         int res = n*factorial(n-1);
         return res;
            
            
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int result = factorial(n);
        System.out.println("Factorial: " + result);
    }
}

~~~
# OUTPUT:
<img width="447" height="131" alt="image" src="https://github.com/user-attachments/assets/56acf4c0-0d56-4b0c-bd04-3a9c33328617" />


# EXP-2
# AIM:
To develop a recursive program that counts how many times a given number appears in an array. The program should take an array of integers and a target number as input, then use recursion (without loops) to determine and display how many times the target value occurs in the array.
# ALGORITHM:
Start

Read the size of the array N.

Read the N elements into the array.

Read the target number to be counted.

Call the recursive function:
countOccurrences(array, index, target)
where index starts at 0.

In the recursive function:

If index equals array size (index == N)
→ Return 0 (base case).

Else
→ If array[index] equals target
→ return 1 + countOccurrences(array, index + 1, target)
→ Else
→ return countOccurrences(array, index + 1, target)

Store the returned value as the total count.

Display:
The number <target> appears <count> time(s) in the array.

End

# PROGRAM:
~~~
import java.util.Scanner;

public class CountOccurrences {

    // Recursive function to count occurrences of a target number
    public static int countOccurrences(int[] arr, int n, int target) {
        //write your code here
         if (n == 0) {
        return 0;
    }

    // Check last element and add 1 if it matches
    int countForThisElement = (arr[n - 1] == target) ? 1 : 0;

    // Recursively count in the rest of the array
    return countForThisElement + countOccurrences(arr, n - 1, target);
        
        
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input: Size of array
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        // Input: Array elements
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        // Compute and display result
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}

~~~
# OUTPUT:
<img width="980" height="529" alt="image" src="https://github.com/user-attachments/assets/1edd36b7-99aa-42af-8fdd-ab32ba961685" />


# EXP-3
# AIM:
To write a program that computes the factorial of a given number using both recursion and iteration. The program should take an integer input, calculate its factorial using a recursive function as well as an iterative loop, and then display both results for comparison.
# ALGORITHM:
Start

Read the input number N.

Recursive Method:

Call function factRecursive(N)

If N == 0, return 1

Else return N × factRecursive(N − 1)

Store the value returned by the recursive function.

Iterative Method:

Initialize result = 1

For i = 1 to N, do
result = result × i

Store the iterative factorial result.

Display:
Factorial (Recursive): <value>
Factorial (Iterative): <value>

End
# PROGRAM:
~~~
import java.util.Scanner;
public class FactorialCalculator {
    // Recursive method to calculate factorial
    static long factorialRecursive(int n) {
      //write your code here
      if (n == 0 || n == 1) {
            return 1;
        }
        // Recursive call
        return n * factorialRecursive(n - 1);
    }

    // Iterative method to calculate factorial
    static long factorialIterative(int n) {
        long result = 1;
        for (int i = 1; i <= n; i++) {
            result *= i;
        }
        return result;
      
      
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int num = sc.nextInt();
        
        if (num < 0) {
            System.out.println("Factorial is not defined for negative numbers.");
        } else {
            System.out.println("Factorial (Recursive): " + factorialRecursive(num));
            System.out.println("Factorial (Iterative): " + factorialIterative(num));
        }
    }
}
~~~
# OUTPUT:
<img width="666" height="220" alt="image" src="https://github.com/user-attachments/assets/3830dcff-0cbd-43ff-804e-90ca60ac8a25" />


# EXP-4
# AIM:
To analyze and determine the nature (even/odd/mixed) of the resulting matrix when performing matrix addition between two matrices where Matrix A contains all odd numbers and Matrix B contains all even numbers of the same dimension.
# ALGORITHM:
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
# PROGRAM:
~~~
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

~~~
# OUTPUT:
<img width="378" height="551" alt="image" src="https://github.com/user-attachments/assets/5eb7a3e3-ca12-4e55-aaa3-20b71e10b095" />

# EXP-5
# AIM:
To implement Bubble Sort to arrange the elements of an unsorted array in ascending order by repeatedly comparing adjacent elements and swapping them if they are in the wrong order.
# ALGORITHM:
Start

Read the size of the array N.

Read the N elements into the array.

Repeat for i = 0 to N - 2:

For j = 0 to N - i - 2:

If array[j] > array[j + 1]
→ Swap the two elements.

After each pass, the largest unsorted element moves to its correct position.

Continue until all elements are sorted in ascending order.

Print the sorted array.

End
# PROGRAM:
~~~
import java.util.Scanner;

class prog {
    
    
    static void bubbleSort(int arr[], int n){
       for (int i = 0; i < n - 1; i++) {
            // Last i elements are already in place
            for (int j = 0; j < n - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    // Swap arr[j] and arr[j+1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }//Type your code
    }

    // Function to print an array
    static void printArray(int arr[], int size){
        int i;
        for (i = 0; i < size; i++)
            System.out.print(arr[i] + " ");
        System.out.println();
    }

    // Driver program
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        
        int arr[] = new int[n];
        for(int i=0;i<n;i++){
            arr[i]= sc.nextInt();
        }
        bubbleSort(arr, n);
       
        printArray(arr, n);
    }
}
~~~
# OUTPUT:
<img width="516" height="238" alt="image" src="https://github.com/user-attachments/assets/65ec5ef9-95a2-4d8c-a0de-19791fb81a89" />
