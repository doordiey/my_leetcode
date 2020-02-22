# 和为s的两个数字

## 题目描述：

```
输入一个递增排序的数组和一个数字s，在数组中查找两个数，使得它们的和正好是s。如果有多对数字的和等于s，则输出任意一对即可。
```

## 我的解答：

- 思路
  - 从最小和最大开始加，如果大于所求值，右边的小一点，如果小于所求值，左边的大一点【双指针

### Python

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        left = 0
        right = len(nums)-1
        while left<right:
            sumthem = nums[left] + nums[right]
            if sumthem == target:
                return [nums[left],nums[right]]
            elif sumthem > target:
                right = right -1
            elif sumthem < target:
                left = left + 1
```

- 

### Java

```java

```

- 