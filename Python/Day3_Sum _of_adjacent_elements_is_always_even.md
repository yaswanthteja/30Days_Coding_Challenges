## Sum of adjacent elements is always even
Given an array of integers A, find and return the minimum elements to be removed such that
in the resulting array the sum of any two adjacent values is even.



Input Format
```
The only argument given is the integer array A.
```
Output Format
```
Return the minimum number of elements to be removed.
```
Constraints
```
1 <= length of the array <= 100000
-10^9 <= A[i] <= 10^9
```
For Example
```
Input 1:
    A = [1, 2, 3, 4, 5]
Output 1:
    2

Input 2:
    A = [5, 17, 100, 11]
Output 2:
    1
```

```

 class Solution:
    # @param A : list of integers
    # @return an integer
    def solve(self, A):
        n=len(A)
        sd=0
        for i in range(n):
            if (A[i]%2):
                sd+=1
        return min(sd,n-sd)

```
