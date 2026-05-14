# 🔹 1342. Number of Steps to Reduce a Number to Zero

## 🧠 Problem Statement
Given an integer `num`, return the number of steps required to reduce it to `0`.

In one step:
- If the current number is even, divide it by `2`
- Otherwise, subtract `1` from it

---

## 📌 Examples

```
Input:  num = 14
Output: 6

Explanation:
Step 1) 14 is even  -> 14 / 2 = 7
Step 2) 7 is odd    -> 7 - 1 = 6
Step 3) 6 is even   -> 6 / 2 = 3
Step 4) 3 is odd    -> 3 - 1 = 2
Step 5) 2 is even   -> 2 / 2 = 1
Step 6) 1 is odd    -> 1 - 1 = 0
```

```
Input:  num = 8
Output: 4
```

```
Input:  num = 123
Output: 12
```

---

## 💡 Approach
- Initialize a variable `steps = 0`
- Repeat until the number becomes `0`
- If the number is even, divide it by `2`
- Otherwise, subtract `1`
- Increase the step count after every operation
- Return the total steps

---

## ⚡ C++ Solution

```cpp
class Solution {
public:
    int numberOfSteps(int num) {

        int steps = 0;

        while(num > 0){

            if(num % 2 == 0){
                num = num / 2;
            }
            else{
                num = num - 1;
            }

            steps++;
        }

        return steps;
    }
};

// num = 8
// Initially, steps = 0

// 8 -> even -> 8 / 2 = 4 --> steps = 1
// 4 -> even -> 4 / 2 = 2 --> steps = 2
// 2 -> even -> 2 / 2 = 1 --> steps = 3
// 1 -> odd  -> 1 - 1 = 0 --> steps = 4
```

---

## 🚀 Notes
- Time Complexity: O(log n)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`Math` `Easy`
