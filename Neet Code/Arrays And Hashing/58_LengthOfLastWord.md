## 58 - Length of Last Word
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/length-of-last-word/">Leet Code</a>
- Date: 24 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

<br>

### Solution 1
- Approach: Taking Space
- Time Complexity: O(n)
- Space Complexity: O(n)

```java
class Solution {
    public int lengthOfLastWord(String s) {
        String[] words = s.split(" ");
        return words[words.length - 1].length();
    }
}
```

<br>

### Solution 2
- Approach: Linear Traversal
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public int lengthOfLastWord(String s) {
    int length = 0;
    boolean isChar = false;

    for (int i = s.length() - 1; i >= 0; i--) {
        if (isChar && s.charAt(i) == ' ') return length;
        if (s.charAt(i) != ' ') {
            length++;
            isChar = true;
        }
    }

    return length;
}
```