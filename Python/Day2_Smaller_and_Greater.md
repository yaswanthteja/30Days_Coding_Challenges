



![image](https://github.com/yaswanthteja/30Days_Coding_Challenges/assets/93423367/701216b3-d198-4ec7-89d3-388e9f26b803)



### Smaller and Greater
You are given an Array A of size N.

Find for how many elements, there is a strictly smaller element and a strictly greater element.



Input Format
```
Given only argument A an Array of Integers.
```
Output Format
```
Return an Integer X, i.e number of elements.
```
Constraints
```
1 <= N <= 1e5
1 <= A[i] <= 1e6
```
For Example

Example Input:
```
    A = [1, 2, 3]
```
Example Output:
```
    1
 ```  
Explanation:
    only 2 have a strictly smaller and strictly greater element, 1 and 3 respectively.




```python
class Solution:
    #@ param A: list of integers
    #@ return an integer
    def solve(self,A):
        min_element=min(A)
        max_element=max(A)
        count=0
        for i in range(len(A)):
            if A[i]==min_element or A[i]==max_element:
                count+=1
        return (len(A)-count)

```
