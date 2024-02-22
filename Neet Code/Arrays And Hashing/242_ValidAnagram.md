## 242 - Valid Anagram
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/valid-anagram/">Leet Code</a>
- Date: 23 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>

### Solution 1
- Approach: Frequency Map
- Time Complexity: O(n)
- Space Complexity: O(n)

```java
public boolean isAnagram(String s, String t) {
    if (s.length() != t.length()) return false;
    Map<Character, Integer> map = new HashMap();

    for (char c : s.toCharArray()) {
        map.put(c, map.getOrDefault(c, 0) + 1);
    }

    for (char c : t.toCharArray()) {
        if (!map.containsKey(c)) return false;
        map.put(c, map.get(c) - 1);
    }

    for (Map.Entry<Character, Integer> me : map.entrySet()) {
        if (me.getValue() > 0) return false;
    }

    return true;
}
```
<br>

### Solution 2
- Approach: Frequency Array
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public boolean isAnagram(String s, String t) {
    int[] freq = new int[26];

    for (char c : s.toCharArray()) freq[c - 'a']++;
    for (char c : t.toCharArray()) freq[c - 'a']--;

    for (int n : freq) if (n != 0) return false;

    return true;
}
```