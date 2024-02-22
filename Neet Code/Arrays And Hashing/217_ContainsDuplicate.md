## 217 - Contains Duplicate
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/contains-duplicate/">Leet Code</a>
- Date: 23 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

### Solution 1
- Approach: Brute Force
- Time Complexity: O(n&sup2;)
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
<br>

### Solution 2
- Approach: Hashing
- Time Complexity: O(n)
- Space Complexity: O(n)

```java
public boolean containsDuplicate(int[] nums) {
    Set<Integer> set = new HashSet<>();

    for (int n : nums) {
        if (set.contains(n)) return true;
        set.add(n);
    }

    return false;
}
```