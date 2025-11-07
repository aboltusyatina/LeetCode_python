# 3110 - Score Of String

## First version
```python
class Solution:
    def scoreOfString(self, s: str) -> int:
        a = []
        b = list(s)
        sum = 0
        for i in b:
            a.append(ord(i))

        for j in range(len(a)):
            now = a[j]
            try:
                next = a[j+1]
            except:
                pass
            sum += abs(now - next)
        return sum
```

##Second version
```python
class Solution:
    def scoreOfString(self, s: str) -> int:
        sum = 0
        a = list(s)
        for i in range(len(a)):
            now = a[i]
            try:
                next = a[i+1]
            except:
                pass
            sum += abs(ord(now)-ord(next))
            
        return sum
```
