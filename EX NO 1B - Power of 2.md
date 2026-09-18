# EX 1B Power of 2
## DATE: 21/07/26
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1.Start the program.
2. Create a Scanner object to take user input.
3. Read an integer input n.
4. Check if n equals 0. If yes, return false (0 is not a power of two).
5. Use the bitwise operation (n & (n - 1)) == 0 to determine if n is a power of two.
6. Return true if the condition is satisfied; otherwise, return false.
7. Display the result.
8. End the program. 

## Program:
```
/*
Program to check if a number is a power of two
Developed by: MANIKANDAN T
Register Number:  212224110037
*/
import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
        if (n == 0) {
            return false;
        }
        return ((n & (n - 1)) == 0);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:
<img width="411" height="224" alt="image" src="https://github.com/user-attachments/assets/a33e39c2-897d-4bc3-984a-12736fbdc56a" />


## Result:
The program successfully implemented and the expected output is verified.
