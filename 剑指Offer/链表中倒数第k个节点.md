# 链表中倒数第k个节点

## 题目描述：

```
输入一个链表，输出该链表中倒数第k个节点。为了符合大多数人的习惯，本题从1开始计数，即链表的尾节点是倒数第1个节点。例如，一个链表有6个节点，从头节点开始，它们的值依次是1、2、3、4、5、6。这个链表的倒数第3个节点是值为4的节点。
```

## 我的解答：

- 思路
  - 遍历一遍，记录链表长度，再移动返回头节点位置
  - 快慢指针：先走k步，表示截取的尾部位置

### Python

```python
class Solution:
    def getKthFromEnd(self, head: ListNode, k: int) -> ListNode:
        res = head
        long = 1
        while head.next is not None:
            long = long + 1
            head = head.next
        while long>k:
            res = res.next
            long = long - 1
        return res
```

- 48ms 13.1MB

```python
class Solution:
    def getKthFromEnd(self, head: ListNode, k: int) -> ListNode:
        fhead = head
        lhead = head
        while k!= 0:
            fhead = fhead.next
            k -= 1
        while fhead:
            lhead = lhead.next
            fhead = fhead.next
        return lhead
```

- 56ms 13.2MB

### Java

```java

```

- 