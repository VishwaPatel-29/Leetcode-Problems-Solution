# 🔹 2413. Smallest Even Multiple

## 🧠 Problem Statement
Given a positive integer `n`, return the smallest positive integer that is a multiple of both `2` and `n`.

---

## 📌 Examples

```
Input:  n = 5
Output: 10
Explanation: The smallest multiple of both 5 and 2 is 10.
```

```
Input:  n = 6
Output: 6
Explanation: The smallest multiple of both 6 and 2 is 6. Note that a number is a multiple of itself.
```

---

## 💡 Approach
- Check if `n` is even  
- If yes, return `n` (already a multiple of 2)  
- If not, return `n * 2`  

---

## ⚡ C++ Solution (Copy-Paste Ready)

```cpp
class Solution {
public:
    int smallestEvenMultiple(int n) {
        if(n % 2 == 0){
            return n;
        }
        else{
            return n * 2;
        }
    }
};
```

---

## 🚀 Notes
- Time Complexity: O(1)  
- Space Complexity: O(1)  

---

## 🏷️ Tags
`Math` `Easy`
