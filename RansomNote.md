# 383. Ransom Note
```python
def canConstruct(ransomNote: str, magazine: str) -> bool:
    from collections import Counter
    st1, st2 = Counter(ransomNote), Counter(magazine)
    if st1 & st2 == st1:
        return True
    return False


print(canConstruct('aa', 'aab'))
```
