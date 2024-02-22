## 1299 - Replace Elements with Greatest Element on Right Side
- Difficulty: Easy
- Problem: <a href="https://leetcode.com/problems/replace-elements-with-greatest-element-on-right-side/">Leet Code</a>
- Date: 23 Feb, 2024
- Author: <a href="https://saadahmedev.com">Saad Ahmed</a>
- 
<br>

### Solution 1
- Approach: Linear Traversal
- Time Complexity: O(n)
- Space Complexity: O(1)

```java
public int[] replaceElements(int[] arr) {
    int n = arr.length;
    int largest = arr[n - 1];
    arr[n - 1] = -1;

    for (int i = n - 2; i >= 0; i--) {
        int temp = largest;
        if (arr[i] > largest) largest = arr[i];
        arr[i] = temp;
    }

    return arr;
}
```