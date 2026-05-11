# 🔹 2652. Sum Multiples

## 🧠 Problem Statement
Given a positive integer `n`, find the sum of all integers in the range `[1, n]` inclusive that are divisible by `3`, `5`, or `7`.

Return the sum of all valid numbers.

---

## 📌 Examples

```
Input:  n = 7
Output: 21

Explanation:
Numbers divisible by 3, 5, or 7 are:
3, 5, 6, 7

Sum = 3 + 5 + 6 + 7 = 21
```

```
Input:  n = 10
Output: 40

Explanation:
Numbers divisible by 3, 5, or 7 are:
3, 5, 6, 7, 9, 10

Sum = 40
```

```
Input:  n = 9
Output: 30

Explanation:
Numbers divisible by 3, 5, or 7 are:
3, 5, 6, 7, 9

Sum = 30
```

---

## 💡 Approach
- Initialize `sum = 0`
- Traverse numbers from `1` to `n`
- Check:
  - divisible by `3`
  - OR divisible by `5`
  - OR divisible by `7`
- If true, add the number to `sum`
- Return the final sum

---

## ⚡ C++ Solution

```cpp
class Solution {
public:
    int sumOfMultiples(int n) {

        int sum = 0;

        for(int i = 1; i <= n; i++){

            if(i % 3 == 0 || i % 5 == 0 || i % 7 == 0){
                sum = sum + i;
            }
        }

        return sum;
    }
};

// n = 7

// 1 -> not divisible
// 2 -> not divisible
// 3 -> divisible by 3
// 4 -> not divisible
// 5 -> divisible by 5
// 6 -> divisible by 3
// 7 -> divisible by 7

// Sum = 3 + 5 + 6 + 7 = 21

// Dry Run:
// n = 5
// sum = 0

// 1 -> not divisible
// 2 -> not divisible
// 3 -> divisible by 3 --> sum = 3
// 4 -> not divisible
// 5 -> divisible by 5 --> sum = 8
```

---

## 🚀 Notes
- Time Complexity: O(n)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`Math` `Easy`
