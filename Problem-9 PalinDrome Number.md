# 🔹 9. Palindrome Number

## 🧠 Problem Statement
Given an integer `x`, return `true` if `x` is a palindrome, and `false` otherwise.

A palindrome number reads the same from left to right and from right to left.

---

## 📌 Examples

```
Input:  x = 121
Output: true

Explanation:
121 reads the same from both directions.
```

```
Input:  x = -121
Output: false

Explanation:
From left to right:  -121
From right to left: 121-

Therefore, it is not a palindrome.
```

```
Input:  x = 10
Output: false

Explanation:
From right to left it becomes 01,
which is not equal to 10.
```

---

## 💡 Approach
- Negative numbers are never palindrome
- Store the original number
- Reverse the number digit by digit
- Compare the reversed number with the original number
- If both are equal, return `true`
- Otherwise return `false`

---

## ⚡ C++ Solution (Copy-Paste Ready)

```cpp
class Solution {
public:
    bool isPalindrome(int x) {

        if(x < 0){
            return false;
        }

        int original = x;
        int reverse = 0;

        while(x > 0){

            int digit = x % 10;

            reverse = reverse * 10 + digit;

            x = x / 10;
        }

        return original == reverse;
    }
};

// n = 121 -> reverse = 121
// n = 123 -> reverse = 321

// Negative number:
// n = -121 -> not palindrome

// Dry Run:
// n = 878

// original = 878
// reverse = 0

// First Iteration:
// digit = 8
// reverse = 0 * 10 + 8 = 8
// n = 87

// Second Iteration:
// digit = 7
// reverse = 8 * 10 + 7 = 87
// n = 8

// Third Iteration:
// digit = 8
// reverse = 87 * 10 + 8 = 878
```

---

## 🚀 Notes
- Time Complexity: O(log n)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`Math` `Easy`
