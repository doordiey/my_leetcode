## 实现strStr

```
题目：实现strStr
题库题号：28
要求：给定一个 haystack 字符串和一个 needle 字符串，在 haystack 字符串中找出 needle 字符串出现的第一个位置 (从0开始)。如果不存在，则返回  -1。
```

- 初次提交：

  - 思路：简单粗暴，遍历haystack字符串，切片长度为needle字符串长度，看是否相等，一致则返回i并跳出循环，不一致则返回-1.【暴力解法，上不了台面

  ```python
  class Solution:
      def strStr(self, haystack: str, needle: str) -> int:
          haystack_long = len(haystack)
          needle_long = len(needle)
          k = 0
          if needle_long == 0:
              return 0
          else:
              if needle_long > haystack_long :
                  return -1
              else:
                  for i in range(haystack_long):
                      if haystack[i:i+needle_long]==needle:
                          k = 1
                          return i
                      if k == 1:
                          break
                  if k == 0:
                      return -1
  ```

- 不断优化：

  ```
  
  ```

- 自我分析：