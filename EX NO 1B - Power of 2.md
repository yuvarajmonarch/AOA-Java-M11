
# EX 1B Power of 2
## DATE: 10-11-2025
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1. Start  
2. Read an integer `n` from the user.  
3. Check if `n` is greater than 0 **and** the number of 1's in its binary representation is exactly 1 using `Integer.bitCount(n) == 1`.  
4. If both conditions are true, return `true` — meaning `n` is a power of two. Otherwise, return `false`.  
5. Print the result and end.  
   

## Program:
```
/*

Developed by: YUVARAJ B
Register Number: 212222040186
*/


import java.util.*;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     
     return n>0 && Integer.bitCount(n)==1 ;
     
     
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

<img width="742" height="333" alt="image" src="https://github.com/user-attachments/assets/8df5b9d7-0079-4b5d-9a89-4bf07dcee9e3" />


## Result:
The program successfully implemented and the expected output is verified.
