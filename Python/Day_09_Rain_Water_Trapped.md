### Rain Water Trapped
Problem Description
```
Given a vector A of non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it is able to trap after raining.

```

Problem Constraints
```
1 <= |A| <= 100000
```


Input Format
```
First and only argument is the vector A
```


Output Format
```
Return one integer, the answer to the question
```


Example Input
```
Input 1:

A = [0, 1, 0, 2]
Input 2:

A = [1, 2]

```
Example Output

```
Output 1:

1
Output 2:

0

```
Example Explanation
```
Explanation 1:

1 unit is trapped on top of the 3rd element.
Explanation 2:

No water is trapped.
````

User Code
```
 class Solution:
    # @param A : tuple of integers
    # @return an integer
    def trap(self, A):
        n=len(A)
        if n<=2:
            return 0
        water_trapped=0
        left=[0]*n
        right=[0]*n
        left[0]=A[0]
        right[n-1]=A[n-1]
        for i in range(1,n):
            left[i]=max(left[i-1],A[i])
        for i in range(n-2,-1,-1):
            right[i]=max(right[i+1],A[i])
        for i in range(1,n-1):
            water_trapped+=max(0,min(left[i],right[i])-A[i])
        return water_trapped

```
