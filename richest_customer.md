#1672. Richest Customer Wealth

```python
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        prev = 0
        for i in accounts:
            if sum(i) > prev:
                prev = sum(i)
        return prev
```
