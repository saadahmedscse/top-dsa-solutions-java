## 1929 - Concatenation of Array
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/concatenation-of-array/">Leet Code</a>
- Date: 23 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Linear Traversal
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public boolean containsDuplicate(int[] nums) {
    for (int i = 0; i < nums.length - 1; i++) {
        for (int j = i + 1; j < nums.length; j++) {
            if (nums[i] == nums[j]) return true;
        }
    }

    return false;
}
```