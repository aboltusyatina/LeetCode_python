# 1. Two Sum

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        a = 1
        for i in nums:
            for j in range(a, len(nums)):
                if i + nums[j] == target:
                    return [nums.index(i), j]
            a += 1
```
