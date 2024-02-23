## 14 - Longest Common Prefix

- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/longest-common-prefix/">Leet Code</a>
- Date: 24 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Linear Traversal on Words
- Time Complexity: O(n * avg L) -> L is the length of average word
- Space Complexity: O(1)

```java
public String longestCommonPrefix(String[] strs) {
    if (strs.length == 0) return "";
    String first = strs[0];

    for (int i = 1; i < strs.length; i++) {
        while (strs[i].indexOf(first) != 0) {
            first = first.substring(0, first.length() - 1);
        }
    }

    return first;
}
```
