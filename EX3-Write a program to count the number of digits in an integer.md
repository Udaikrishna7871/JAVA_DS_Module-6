# EX3 
## DATE: 13-mar-2026
## AIM:
To write a program that computes the factorial of a given number using both recursion and iteration. The program should take an integer input, calculate its factorial using a recursive function as well as an iterative loop, and then display both results for comparison.
## Algorithm
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

## Program:
```
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

```

## Output:
<img width="666" height="220" alt="image" src="https://github.com/user-attachments/assets/3830dcff-0cbd-43ff-804e-90ca60ac8a25" />




## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
