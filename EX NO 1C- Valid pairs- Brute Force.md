# EX 1C Valid Pairs using Brute Force Approach
## DATE: 22/07/26
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Start the program.
2. Create a Scanner object to take input from the user.
3. Read an integer n (the size of the array).
4. Read n integers into an array nums.
5. Read the integer k.
6. Initialize a counter count to 0.
7. Use nested loops:
   - For each element i in the array, compare it with all elements j where j > i.
   - If the absolute difference |nums[i] - nums[j]| equals k, increment count.
8. After checking all pairs, print the value of count.
9. End the program.

## Program:
```
/*
Program to count pairs with a given difference
Developed by: MANIKANDAN T
Register Number: 212224110037
*/
import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count = 0;
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    count++;
                }
            }
        }
        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}

```

## Output:
<img width="483" height="320" alt="image" src="https://github.com/user-attachments/assets/72e245f7-388f-4a35-8838-55a5e0a3a533" />



## Result:
The program successfully implemented and the expected output is verified.
