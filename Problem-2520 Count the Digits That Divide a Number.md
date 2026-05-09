# 🔹 2520. Count the Digits That Divide a Number

## 🧠 Problem Statement
Given an integer `num`, return the number of digits in `num` that divide `num`.

An integer `val` divides `num` if:

:contentReference[oaicite:0]{index=0}

---

## 📌 Examples

```
Input:  num = 7
Output: 1

Explanation:
7 divides itself, hence the answer is 1.
```

```
Input:  num = 121
Output: 2

Explanation:
121 is divisible by 1, but not by 2.
Since digit 1 appears twice, the answer is 2.
```

```
Input:  num = 1248
Output: 4

Explanation:
1248 is divisible by all of its digits:
1, 2, 4, and 8.
```

---

## 💡 Approach
- Store the original number in another variable  
- Extract each digit using `% 10`  
- Check if the digit divides the original number  
- If divisible, increase the count  
- Remove the last digit using `/ 10`  
- Return the final count  

---

## ⚡ C++ Solution 

```cpp
class Solution {
public:
    int countDigits(int num) {
        int original = num;
        int count = 0;

        while(num > 0){
            int digit = num % 10;

            if(original % digit == 0){
                count++;
            }

            num = num / 10;
        }

        return count;
    }
};

// num = 1248
// digits: 1,2,4,8
// 1248 % 1 = 0 --> count = 1
// 1248 % 2 = 0 --> count = 2
// 1248 % 4 = 0 --> count = 3
// 1248 % 8 = 0 --> count = 4

// Dry Run:
// num = 124
// original = 124, count = 0

// First Iteration:
// digit = 4
// 124 % 4 = 0 --> count = 1
// num = 12

// Second Iteration:
// digit = 2
// 124 % 2 = 0 --> count = 2
// num = 1

// Third Iteration:
// digit = 1
// 124 % 1 = 0 --> count = 3
```

---

## 🚀 Notes
- Time Complexity: O(log n)  
- Space Complexity: O(1)  

---

## 🏷️ Tags
`Math` `Easy`
