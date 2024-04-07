


Topic : Arrays

### Kth Row of Pascal's Triangle
Problem Description
```
Given an index k, return the kth row of the Pascal's triangle.
Pascal's triangle: To generate A[C] in row R, sum up A'[C] and A'[C-1] from previous row R - 1.

Example: ``` Input : k = 3

Return : [1,3,3,1] ``` Note: k is 0 based. k = 0, corresponds to the row [1].

Note: Could you optimize your algorithm to use only O(k) extra space?

```

User Code
```
 class Solution:
    # @param A : integer
    # @return a list of integers
    def getRow(self, A):
        R=[1]
        for i in range(1,A+1):
            n_r=[1] * (i+1)
            for c in range(1,i):
                n_r[c]=R[c-1]+R[c]
            R=n_r
        return R
```        
