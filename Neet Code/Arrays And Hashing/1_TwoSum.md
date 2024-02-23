## 1 - Two Sum

- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/two-sum/">Leet Code</a>
- Date: 24 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Brute Force
- Time Complexity: O(n&sup2;)
- Space Complexity: O(1)

```java
public int[] twoSum(int[] nums, int target) {
    for (int i = 0; i < nums.length - 1; i++) {
        for (int j = i + 1; j < nums.length; j++) {
            if (nums[i] + nums[j] == target) return new int[]{i, j};
        }
    }

    return new int[]{-1, -1};
}
```

<br>

### Solution 2
- Approach: Taking Space for Optimization
- Time Complexity: O(n)
- Space Complexity: O(n)

```java
public int[] twoSum(int[] nums, int target) {
    Map<Integer, Integer> map = new HashMap<>();

    for (int i = 0; i < nums.length; i++) {
        if (map.containsKey(target - nums[i])) return new int[]{map.get(target - nums[i]), i};
        map.put(nums[i], i);
    }

    return new int[]{-1, -1};
}
```

<br>

### Solution 3

- Approach: Another n&sup2; Approach, [ Different Traversal ] -> More Faster
- Time Complexity: O(n&sup2;)
- Space Complexity: O(1)

```java
public int[] twoSum(int[] nums, int target) {
    for (int i = 1; i < nums.length; i++) {
        for (int j = i; j < nums.length; j++) {
            if (nums[j - i] + nums[j] == target) return new int[]{j - i, j};
        }
    }

    return new int[]{-1, -1};
}
```
