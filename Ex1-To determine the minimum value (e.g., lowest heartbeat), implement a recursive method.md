# EX 1
## DATE: 13-mar-2026
## AIM:
To write a recursive Java program that computes the factorial of a given non-negative integer N, where 
0
≤
𝑁
≤
15
0≤N≤15. The program should take an integer as input, use recursion instead of loops to calculate the factorial, and display the result in the format:
## Algorithm
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

## Program:
```
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
```

## Output:
<img width="447" height="131" alt="image" src="https://github.com/user-attachments/assets/56acf4c0-0d56-4b0c-bd04-3a9c33328617" />



## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
