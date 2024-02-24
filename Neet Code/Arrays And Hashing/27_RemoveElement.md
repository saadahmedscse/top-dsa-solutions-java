## 27 - Remove Element

- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/remove-element/">Leet Code</a>
- Date: 24 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Linear Traversal
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public int removeElement(int[] nums, int val) {
    int idx = 0;

    for (int i = 0; i < nums.length; i++) {
        if (nums[i] != val) nums[idx++] = nums[i];
    }

    return idx;
}
```