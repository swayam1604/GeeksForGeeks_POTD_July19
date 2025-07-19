# GeeksforGeeks POTD – Count Unique Vowel Strings (19 July 2025)

### 🔹 Problem Statement:
Given a string `s`, count the number of unique vowel substrings by multiplying vowel frequencies with their position index (1-based). Return the product. If no vowels exist, return `0`.

### 🔹 Solution Approach:
- Use a set to track vowels.
- Count frequency of each vowel using a dictionary.
- Multiply each frequency by its 1-based index in the order of appearance.
- Return the final product.

### 🔹 Python Code:

```python
class Solution:
    def vowelCount(self, s):
        # Streak 19/07/2025 – POTD by Swayam Sharma
        dic = {}
        se = {'a', 'e', 'i', 'o', 'u'}
        for i in s:
            if i in se:
                dic[i] = dic.get(i, 0) + 1
        if not dic:
            return 0
        fact = 1
        for i, j in enumerate(dic.values()):
            fact *= (i + 1) * j
        return fact
```
Submitted by:
Swayam Sharma
