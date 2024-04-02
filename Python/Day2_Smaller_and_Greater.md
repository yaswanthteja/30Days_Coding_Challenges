



![image](https://github.com/yaswanthteja/30Days_Coding_Challenges/assets/93423367/701216b3-d198-4ec7-89d3-388e9f26b803)



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
