# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 10-11-2025
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Start  
2. Read the size `m` of the first sorted array and input `m` integers into `nums1`.  
3. Read the size `n` of the second sorted array and input `n` integers into `nums2`.  
4. Merge both arrays `nums1` and `nums2` into a new array `merge`.  
5. Sort the merged array using `Arrays.sort()`.  
6. Find the total length `tot` of the merged array.  
7. If `tot` is odd, the median is the middle element `merge[tot/2]`.  
8. If `tot` is even, the median is the average of the two middle elements `merge[tot/2 - 1]` and `merge[tot/2]`.  
9. Print the median value.  
10. End  
   

## Program:
```
/*
Developed by: YUVARAJ B
Register Number:  212222040186
*/

import java.util.*;

public class Solution {

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) 
    {
        int n = nums1.length;
        int m = nums2.length;
        int k=0;
        int [] merge = new int[n+m];
        
        for(int i=0;i<n;i++)
        {
            merge[k++] = nums1[i];
        }
        
        for(int i=0;i<m;i++)
        {
            merge[k++] = nums2[i];
        }
        
        Arrays.sort(merge);
        
        int tot = merge.length;
        
        if(tot%2==1)
        {
            return (double) merge[tot/2];
        }
        else
        {
            int mid1 = merge[tot/2-1];
            int mid2 = merge[tot/2];
            
            return ((double) mid1 +(double)mid2)/2.0;
        }
       
    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        //System.out.print("Enter size of first sorted array: ");
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        //System.out.println("Enter " + m + " sorted integers for first array:");
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        //System.out.print("Enter size of second sorted array: ");
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        //System.out.println("Enter " + n + " sorted integers for second array:");
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:

<img width="1228" height="455" alt="image" src="https://github.com/user-attachments/assets/873dcab2-6a8b-4a93-ac19-8b670e235511" />


## Result:
The program successfully implemented and the expected output is verified.
