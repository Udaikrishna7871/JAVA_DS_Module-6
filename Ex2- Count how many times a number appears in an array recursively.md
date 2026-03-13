# Ex2 
## DATE: 13-mar-2026
## AIM:
To develop a recursive program that counts how many times a given number appears in an array. The program should take an array of integers and a target number as input, then use recursion (without loops) to determine and display how many times the target value occurs in the array.
## Algorithm
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
 

## Program:
```
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


```

## Output:

<img width="980" height="529" alt="image" src="https://github.com/user-attachments/assets/1edd36b7-99aa-42af-8fdd-ab32ba961685" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
