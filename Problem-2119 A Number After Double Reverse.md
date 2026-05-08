# 🔹 2119. A Number After a Double Reversal

## 🧠 Problem Statement
Reversing an integer means to reverse all its digits.

For example:
- Reversing `2021` gives `1202`
- Reversing `12300` gives `321` because leading zeros are removed

Given an integer `num`:
1. Reverse `num` to get `reversed1`
2. Reverse `reversed1` to get `reversed2`

Return `true` if `reversed2` equals `num`, otherwise return `false`.

---

## 📌 Examples

```
Input:  num = 526
Output: true

Explanation:
Reverse 526 -> 625
Reverse 625 -> 526

Since the final number equals the original number,
the answer is true.
```

```
Input:  num = 1800
Output: false

Explanation:
Reverse 1800 -> 81
Reverse 81 -> 18

18 is not equal to 1800,
so the answer is false.
```

```
Input:  num = 0
Output: true

Explanation:
Reverse 0 -> 0
Reverse 0 -> 0

The final number equals the original number.
```

---

## 💡 Approach
- If the number is `0`, return `true`
- If the number ends with `0`, reversing removes trailing zeros
- After reversing twice, the number changes
- So:
  - Return `true` if `num == 0` OR `num % 10 != 0`
  - Otherwise return `false`

---

## ⚡ C++ Solution 

```cpp
class Solution {
public:
    bool isSameAfterReversals(int num) {
        if(num == 0 || num % 10 != 0){
            return true;
        }

        return false;
    }
};

// num = 120  -> false
// num = 123  -> true
```

---

## 🚀 Notes
- Time Complexity: O(1)  
- Space Complexity: O(1)  

---

## 🏷️ Tags
`Math` `Easy`
