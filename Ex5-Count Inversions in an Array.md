# Ex5 Count Inversions in an Array

## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm

1. Start the program.
2. Declare an integer array arr of size n.
3. Read the value of n (number of elements).
4. Read n elements and store them in the array arr.
5. Initialize a variable count to 0 to store the number of inversions.
6. Use two nested loops:
7. Outer loop variable i from 0 to n - 1
8. Inner loop variable j from i + 1 to n - 1
9. For each pair (i, j), if arr[i] > arr[j] and i < j, increment count by 1.
10. After all comparisons, print the value of count as the total number of inversions in the array.
11. Stop the program.
    
## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
*/
import java.util.Scanner;

public class CountInversions
{
    public static int countInversions(int[] arr)
{
        int n = arr.length;
        int count = 0;
        for (int i = 0; i < n - 1; i++)
{
            for (int j = i + 1; j < n; j++)
{
                if (arr[i] > arr[j]) {
                    count++; 
                }
            }
        }

        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int inversions = countInversions(arr);

        System.out.println("Number of inversions in the array: " + inversions);

        sc.close();
    }
}
```

## Output:

<img width="406" height="243" alt="image" src="https://github.com/user-attachments/assets/6c314097-77b6-4f0e-a6ac-6e5e1cc689f4" />




## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
