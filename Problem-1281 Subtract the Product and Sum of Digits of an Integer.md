# 🔹 1281. Subtract the Product and Sum of Digits of an Integer

## 🧠 Problem Statement
Given an integer number `n`, return the difference between the product of its digits and the sum of its digits.

---

## 📌 Examples

```
Input:  n = 234
Output: 15

Explanation:
Product of digits = 2 * 3 * 4 = 24
Sum of digits = 2 + 3 + 4 = 9

Result = 24 - 9 = 15
```

```
Input:  n = 4421
Output: 21

Explanation:
Product of digits = 4 * 4 * 2 * 1 = 32
Sum of digits = 4 + 4 + 2 + 1 = 11

Result = 32 - 11 = 21
```

---

## 💡 Approach
- Initialize:
  - `product = 1`
  - `sum = 0`
- Extract each digit using `% 10`
- Multiply the digit with `product`
- Add the digit to `sum`
- Remove the last digit using `/ 10`
- Return `product - sum`

---

## ⚡ C++ Solution 

```cpp
class Solution {
public:
    int subtractProductAndSum(int n) {
        int product = 1;
        int sum = 0;

        while(n > 0){
            int digit = n % 10;

            product *= digit;
            sum += digit;

            n = n / 10;
        }

        return product - sum;
    }
};
```

---

## 🚀 Notes
- Time Complexity: O(log n)  
- Space Complexity: O(1)  

---

## 🏷️ Tags
`Math` `Easy`
