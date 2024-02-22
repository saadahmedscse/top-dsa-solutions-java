## 392 - Is Subsequence
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/is-subsequence/">Leet Code</a>
- Date: 23 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Two Pointer
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public boolean isSubsequence(String s, String t) {
    if (s.isEmpty()) return true;

    int i = 0;
    int j = 0;

    while (j < t.length()) {
        if (s.charAt(i) == t.charAt(j)) {
            i++;
            if (i == s.length()) return true;
        }
        j++;
    }

    return false;
}
```