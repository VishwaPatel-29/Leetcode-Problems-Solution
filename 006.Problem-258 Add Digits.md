# 🔹 258. Add Digits

## 🧠 Problem Statement
Given an integer `num`, repeatedly add all its digits until the result has only one digit, and return it.

---

## 📌 Examples

```
Input:  num = 38
Output: 2

Explanation:
38 --> 3 + 8 = 11
11 --> 1 + 1 = 2

Since 2 has only one digit, return 2.
```

```
Input:  num = 0
Output: 0
```

---

## 💡 Approach 1 (Loop Method)
- Repeat the process while the number has more than one digit  
- Extract each digit using `% 10`  
- Add all digits together  
- Replace `num` with the new sum  
- Continue until a single digit remains  

---

## ⚡ C++ Solution 

```cpp
class Solution{
public:
    int addDigits(int num){
        while(num >= 10){

            int sum = 0;

            while(num > 0){
                int digit = num % 10;
                sum = sum + digit;
                num = num / 10;
            }

            num = sum;
        }

        return num;
    }
};
```

---

## 💡 Approach 2 (Mathematical Trick)

Using the Digital Root formula:

:contentReference[oaicite:0]{index=0}

- If `num == 0`, return `0`
- Otherwise use the formula above to get the answer in O(1)

---

## ⚡ Optimized C++ Solution

```cpp
class Solution {
public:
    int addDigits(int num) {
        if(num == 0){
            return 0;
        }

        return 1 + (num - 1) % 9;
    }
};
```

---

## 🧪 Dry Run

```cpp
num = 38

3 + 8 = 11
1 + 1 = 2

Final Answer = 2
```

---

## 🚀 Notes
### Loop Method
- Time Complexity: O(log n)  
- Space Complexity: O(1)

### Mathematical Method
- Time Complexity: O(1)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`Math` `Easy`
