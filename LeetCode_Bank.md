```python
class Solution:
    def totalMoney(self, n: int) -> int:
        sums = 0
        step = 1
        week_step = 1
        for i in range(1, n+1):
            sums += step
            step = step + 1
            if i % 7 == 0:
                week_step += 1
                step = week_step
        return sums
```
