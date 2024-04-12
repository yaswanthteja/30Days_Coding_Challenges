Topic: Arrays
### Repeat and Missing Number Array
You are given a read only array of n integers from 1 to n.

Each integer appears exactly once except A which appears twice and B which is missing.

Return A and B.

Note: Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

Note that in your output A should precede B.

Example:
```
Input:[3 1 2 5 3] 

Output:[3, 4] 

A = 3, B = 4
```
User Code
```
 class Solution:
    # @param A : tuple of integers
    # @return a list of integers
    def repeatedNumber(self, A):
        xor=0
        n=len(A)
        for i in range(1,n+1):
            xor^=i
        for num in A:
            xor^=num
        rmb=xor&-xor
        a=0
        b=0
        for num in A:
            if num &rmb:
                a^=num
            else:
                b^=num
        for i in range(1,n+1):
            if i&rmb:
                a^=i
            else:
                b^=i
        for num in A:
            if num==a:
                return [a,b]
        return [b,a]
 
```



