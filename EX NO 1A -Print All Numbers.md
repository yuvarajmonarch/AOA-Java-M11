
# EX 1A Print All Numbers 
## DATE: 10-11-2025
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Start  
2. Read input integer `n` from the user.  
3. Initialize a loop variable `i` to 1.  
4. Repeat the following steps while `i ≤ n`:  
5. Print the value of `i` followed by a space.  
6. Increment `i` by 1.  
7. End  


## Program:
```
/*
Developed by: YUVARAJ B
Register Number:  212222040186
*/

import java.util.*;

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        
        for(int i=1;i<=n;i++)
        {
            System.out.print(i+" ");
        }
    }
}

```

## Output:

<img width="768" height="297" alt="image" src="https://github.com/user-attachments/assets/0316db62-2960-44b3-bee8-8936fe6a3dbe" />


## Result:
The program successfully print all the numbers from 1 to N. 
